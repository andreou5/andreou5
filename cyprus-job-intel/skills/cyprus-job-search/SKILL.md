---
name: cyprus-job-search
description: Daily Cyprus job-market intelligence run for a Biomedical Science / Medical Laboratory Technology + MBA candidate job-hunting in Cyprus. Searches government, semi-government, and private sources; diffs against data/vacancies.json; produces a daily report.
---

# Cyprus Job Intelligence — Search & Report Skill

> **Provenance note:** this spec was reconstructed by Claude from the candidate
> context supplied in the original `/goal` request (background, location
> priorities, KPMG exclusion). The requester's own detailed spec text was not
> actually included in that request (a placeholder shipped in its place), so
> the rules below are Claude's best operational design for the stated goal,
> not a verbatim transcription. Edit this file directly to correct or refine
> any rule below — it is the single source of truth for every future run.

## 1. Candidate Profile

- **Education:** Bachelor's degree in Biomedical Science / Medical Laboratory
  Technology; MBA.
- **Target role families:**
  - Medical laboratory technologist / biomedical scientist roles (state
    hospitals, public health labs, State General Laboratory, private
    clinical/diagnostic labs).
  - Roles that use the MBA: healthcare administration, quality
    assurance/quality management (incl. lab accreditation/ISO 15189), business
    development, operations, project management, general administrative or
    management-track government/semi-government positions.
  - Hybrid roles (lab QA manager, healthcare operations, medical affairs
    coordinator) score highest — they use both degrees.
- **Hard exclusion:** any vacancy at **KPMG** (any KPMG Cyprus entity), at any
  location, any role — exclude entirely, do not list even as "not a fit."

## 2. Location Priority (strict ranking, used in match scoring and report grouping)

1. **Polis Chrysochous** (Πόλις Χρυσοχούς) — top priority, any sector.
2. **Paphos city** (Πάφος town proper).
3. **Paphos district** (other Paphos-district towns/villages: Peyia, Yeroskipou,
   Chlorakas, Tala, Emba, etc.).
4. **Government / semi-government, anywhere else in Cyprus** (Nicosia,
   Limassol, Larnaca, Famagusta-area) — public sector only.
5. **Exceptional private-sector roles, anywhere else in Cyprus** — only listed
   if clearly strong (senior title, direct profile match, or notably high
   compensation); ordinary private-sector listings outside Paphos/Polis are
   left out of the daily report to keep it focused, but logged in
   `vacancies.json` with `status: "logged_low_priority"` so nothing is lost.

Location is classified from the vacancy's stated work location, not the
employer's headquarters (e.g., a Nicosia-HQ ministry advertising a post based
in Polis Chrysochous is classified as Polis Chrysochous).

## 3. Source Priority (search in this order every run)

1. **Cyprus Government vacancies portal** — https://www.pspd.gov.cy (Public
   Service jobs) and the central e-recruitment listings.
2. **Public Service Commission (PSC / Επιτροπή Δημόσιας Υπηρεσίας)** —
   https://psc.gov.cy — competition/vacancy announcements.
3. **OKYPY** (Οργανισμός Κρατικών Υπηρεσιών Υγείας — State Health Services
   Organisation, runs the state hospitals incl. Paphos General Hospital) —
   https://okypy.org.cy.
4. **Paphos Municipality** — https://paphos.org.cy — and **Polis Chrysochous
   Municipality** — https://polis-chrysochous.org.cy (or successor domain).
5. **Semi-government organisations**: CYTA (https://www.cyta.com.cy), EAC/ΑΗΚ
   (https://www.eac.com.cy), Water Development Department / Water Boards
   (https://www.wdd.moa.gov.cy and local Paphos water board), Cyprus Ports
   Authority, CyBC.
6. **Universities**: University of Cyprus, Cyprus University of Technology,
   Open University of Cyprus, Neapolis University Pafos (Paphos-based —
   check first among universities given location priority).
7. **Private-sector backups**: LinkedIn Cyprus, CareerJet Cyprus, Bizcyprus,
   EURES Cyprus, major private hospital/lab groups (e.g. Bio-Ideal, Ygia
   Polyclinic, American Medical Center) and general business/management
   listings — **excluding KPMG** (Section 1).

If a source is unreachable (blocked, timed out, structurally unscrapable),
record that plainly in the run's notes and move to the next source rather
than stopping the run.

## 4. Eligibility Labels

Applied per vacancy based on stated requirements vs. candidate profile:

- **`eligible`** — candidate clearly meets stated minimum qualifications.
- **`likely_eligible`** — requirements are compatible but the posting is
  ambiguous or a specific detail (e.g. years of experience, professional
  registration) cannot be confirmed from the source.
- **`not_eligible`** — stated requirements clearly exclude the candidate
  (e.g. requires a specific unrelated degree, or a professional license the
  candidate does not hold).
- **`unverified`** — could not confirm eligibility criteria at all (source
  didn't state requirements, or the listing could not be fully loaded).

## 5. Duplicate / Change Detection

- **`tracking_id`** is a stable slug: `{source-prefix}-{employer-slug}-{title-slug}-{first_seen-YYYYMMDD}`.
- A vacancy already in `vacancies.json` is matched by (employer + title +
  location) fuzzy match, not by URL alone (URLs change across postings of the
  same job).
- On each run, for every previously-known open vacancy:
  - If still listed and unchanged → update `last_checked` only.
  - If details changed (deadline extended, salary revealed, status changed)
    → update the record, log the change in `state_log.md`.
  - If no longer listed and past its deadline → `status: "closed"`.
  - If no longer listed and *before* its deadline → `status: "removed_early"`
    (flag for the report — sometimes means filled early or pulled).
- New listings not matching any existing record → new entry, `status: "new"`,
  logged in `state_log.md`.

## 6. Salary Rules

- Only record a salary figure if the source **states it explicitly**. Cyprus
  public-sector posts usually cite a salary scale (e.g. "Κλίμακα Α8"); record
  the scale/grade as given, don't convert or estimate a number.
- If a posting gives a range, record the range as given.
- If no salary/scale is stated, `salary: null` — never estimate, infer from
  similar roles, or leave a fabricated placeholder.

## 7. Match Scoring (0–100)

Composite score used to sort within each location tier:

- **Location fit** (0–40): Polis Chrysochous = 40, Paphos city = 32, Paphos
  district = 24, other gov/semi-gov = 14, other private = 6.
- **Profile fit** (0–40): direct lab/biomedical role = 40, hybrid
  lab+management/QA role = 40, MBA-relevant management/admin/healthcare-admin
  role = 28, general admin/business role with no health-sector link = 16,
  weak/tangential fit = 6.
- **Eligibility confidence** (0–20): `eligible` = 20, `likely_eligible` = 12,
  `unverified` = 6, `not_eligible` = 0 (excluded from ranked list regardless
  of other scores, but still logged).

Vacancies scoring below 30 are still stored (for completeness/history) but
omitted from the "Top Matches" section of the report.

## 8. Daily Report Format

Each run produces `reports/YYYY-MM-DD.md` with this structure:

```markdown
# Cyprus Job Intelligence Report — {date}

## Run Summary
- Sources checked: N/M (list any that failed and why)
- New vacancies found: N
- Vacancies updated: N
- Vacancies closed/removed: N
- Total open vacancies tracked: N

## Top Matches
(Ranked by match_score, grouped by location tier, highest tier first.
Each entry:)

### {employer} — {title}
- **Location:** {location} (tier: {tier})
- **Match score:** {score}/100
- **Eligibility:** {label}
- **Deadline:** {date or "not stated"}
- **Salary:** {as stated, or "not stated"}
- **Source:** {source_url}
- **Official source:** {official_source_url}
- **Notes:** {anything relevant — exam required, application method, etc.}

## Changes Since Last Report
(from state_log.md — new/updated/closed since the previous run)

## Sources Checked This Run
(list with status: OK / blocked / no vacancies matching profile / error)

## Excluded
- KPMG listings seen and excluded: N (if any)

## Caveats / Unverifiable Items
(anything the run could not confirm — do not fabricate to fill this section)
```

## 9. Execution Steps (what a run actually does)

1. Read `data/vacancies.json` and `data/state_log.md` for prior state.
2. Search each source in priority order (Section 3); for each, extract
   vacancies matching the profile (Section 1) at any of the tracked
   locations or in government/semi-government generally.
3. Apply eligibility labels (Section 4), location tiers (Section 2), salary
   rule (Section 6), and match score (Section 7) to each new/updated listing.
4. Diff against prior state (Section 5); update `vacancies.json` in place.
5. Append a dated entry to `state_log.md` describing what changed.
6. Write `reports/YYYY-MM-DD.md` using the format in Section 8.
7. Commit `data/vacancies.json`, `data/state_log.md`, and the new report file
   with a descriptive commit message.
8. Report any source failures or ambiguous eligibility calls plainly in the
   run summary — never silently drop them.
