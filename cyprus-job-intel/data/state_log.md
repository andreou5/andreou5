# State Log

Running changelog of what changed between Cyprus Job Intelligence reports.
Newest entries at the top.

---

## 2026-09-08 — Record removed (user-requested): Polis Chrysochous Assistant Secretarial Officer

User did their own deep check and also could not verify this vacancy —
asked for it to be removed. Deleted `polis-chrysochous-assistant-secretarial-officer-20260904`
outright rather than marked closed. Distinction from the ΕΟΑ Πάφου
handling: that one was a confirmed real posting that later closed (kept
as a closed historical record); this one was never confirmed to exist as
an actual specific listing in the first place, across 5 days and multiple
targeted checks (2026-09-04 through 2026-09-08) — nothing but the
municipality's generic announcements page and unrelated staff-directory
pages ever turned up. Removing a record that was never substantiated is
not the same as erasing a verified finding, so this doesn't conflict with
the tracker's own keep-closed-records rule.

Total tracked: 14.

---

## 2026-09-08 — Daily run (using the expanded source list)

- **New (2):** both via Bazaraki, Paphos city, unverified eligibility,
  posting dates from July 2026 (currency unconfirmed, not assumed stale):
  - `vrissiana-hotel-paphos-administration-officer-20260908` — Vrissiana
    Beach Hotel, Administration Officer.
  - `stasis-estates-paphos-real-estate-admin-marketing-20260908` — A.N.
    Stasis Estates PLC, Real Estate Administration and Marketing Officer
    (admin + marketing combination — more MBA-relevant than pure admin).
- **Corrected again — CING deadline.** Yesterday's cross-check confirmed
  7 September; today's search instead states the deadline is 8 September
  (today). Neither has been settled by a direct page read (cing.ac.cy
  still blocked). Moved the deadline to today on the strength of today's
  search also surfacing a genuinely new detail — a stated degree
  requirement ("BA/BSc in any Biological Science, or related field such
  as Zoology") — which reads as more complete/authoritative than
  yesterday's pass. `eligibility` upgraded `unverified` → `likely_eligible`
  accordingly. If today really is the last day, this is same-day-actionable.
- **Enriched, not new:**
  - GRS Executive Assistant: contact confirmed (Ioulia Ananikidou,
    ioulia@grsrecruitment.com) — different GRS consultant than the
    Administrative Officer/PA listing.
  - GRS Office Administrator/Receptionist: fuller detail found — it's for
    an expanding Paphos real-estate company, covering tax and compliance
    processes as well as admin, not pure reception. `match_score` 60 → 64.
- **Unchanged:** ΕΟΑ Πάφου (closed), AMC (closed), INEX QA Manager (not
  eligible), Polis Chrysochous Municipal Engineer (not eligible), Polis
  Chrysochous Assistant Secretarial Officer (still unverified — no new
  information either way), GRS Administrative Officer/PA, Flexsy Office
  Manager, INEX Office Administrator, GRS Latsi Project Manager
  (not eligible) — all re-confirmed still live/unchanged.
- Gazette re-checked: nothing new surfaced this run either.
- Total tracked: 15.

---

## 2026-09-07 — Source list expanded (user-requested): 6 new leads found

User asked to add the Cyprus Official Gazette and expand the private-sector
source list to all known Cyprus job boards. `skills/cyprus-job-search/SKILL.md`
Section 3 updated: added the Gazette (mof.gov.cy/mof/gpo/gazette.nsf),
corrected OKYPY's real domain (shso.org.cy, not okypy.org.cy), and added
Ergodotisi, CyprusWork, Alpha.jobs, CyprusJobs, FindJobsInCyprus, Bazaraki,
CareerJet Cyprus, GRS Recruitment, and CY Recruitment to the job-board list
(Carierista and AnergosJobs were already tracked).

Ran the expanded source list immediately rather than waiting for tomorrow's
run. Result — **6 new records, 3 of them tied for the register's top score
(72)**, all in Paphos city:

- **New, strong (Paphos city, likely_eligible, score 72):**
  - `grs-paphos-administrative-officer-pa-20260907` — GRS Recruitment,
    Administrative Officer/PA for an online marketing/affiliate group.
    Salary confirmed: €18,000–€24,000 gross/year. Real specific URL.
  - `grs-paphos-executive-assistant-20260907` — GRS Recruitment, Executive
    Assistant/Office Coordinator supporting senior management. Real
    specific URL (note: page title says "Executive Assistant," the URL
    slug says "office-manager" — flagged, not silently resolved).
  - `flexsy-paphos-office-manager-20260907` — Flexsy (online gaming tech),
    Office Manager & Operations Coordinator, explicit growth path into
    HR/operations/corporate support. **No dedicated ad URL found** — only
    Bazaraki's Paphos category page; flagged rather than guessed at.
- **New, moderate (Paphos city, likely_eligible, score 60):**
  - `grs-paphos-office-administrator-receptionist-20260907` — GRS
    Recruitment, more junior/front-of-house than the other two GRS
    listings; full requirements not yet pulled.
  - `inex-paphos-office-administrator-20260907` — INEX Group (different
    role from their already-tracked QA Manager posting), general office
    admin, C1 English required. **No dedicated ad URL found** either.
- **New, not eligible (Polis Chrysochous area, logged low-priority):**
  - `grs-latsi-project-manager-20260907` — GRS Recruitment, construction
    Project Manager in Latsi (part of the Polis Chrysochous municipal
    area) — but requires a Civil Engineering background. Domain mismatch,
    logged for completeness given the location.
- **Checked, nothing added:** the Official Gazette itself (search-indexed
  content only reproduced what PSC/gov.cy already surface, no unique
  Paphos/Polis-relevant vacancy found this pass); St George & Blue Cross
  Private Hospital, Paphos (has a Clinical Laboratory Department — genuinely
  worth watching directly — but no current specific vacancy found, so not
  logged, consistent with the tracker's own no-fabrication rule).

This is the first run where the register has a genuine cluster of
Paphos-city leads rather than a single fragile one — worth noting given
ΕΟΑ Πάφου closed earlier today.

---

## 2026-09-07 — User-verified: ΕΟΑ Πάφου listing is expired

The user opened the carierista.com listing directly (Ref #CA96542) and it
shows "This job post is expired." This settles the deadline question that
9 consecutive automated runs could not resolve — `eoap-pafou-dioikitikos-leitourgos-20260830`
`status` changed `open` → `closed`. It stays the top-scored record
historically (72/100) but is no longer the register's live top match;
`eoap.org.cy`/ΕΟΑ Πάφου's own site was never directly reachable in this
environment to catch this sooner. If ΕΟΑ Πάφου reposts an Administrative
Officer role, it will be evaluated as a new listing on the next run, not
assumed to be this one reopened.

---

## 2026-09-07 — Cross-check correction (user-requested)

User asked to cross-check every job and URL directly. Result — one real
error caught and corrected, one record downgraded, one confirmed sound:

- **CING Laboratory Scientific Officer — corrected, not just re-confirmed.**
  The deadline was wrong: previously recorded as "~8 September," the
  actual confirmed deadline is **Monday 7 September 2026 — today**. Also
  found: reference code (360426), a real salary figure (€76,184.17 gross
  annual, incl. 13th salary, Scale A15/A16, + allowance), and a specific
  third-party posting URL (ergodotisi.com/en-CY/jobs/6966391/...). Also
  discovered a *different*, already-closed CING LSO batch (4 posts,
  General Core Facility, deadline 30 Apr 2026) that could easily have been
  confused with this one — confirmed they are separate postings.
- **Δήμος Πόλεως Χρυσοχούς Assistant Secretarial Officer — downgraded.**
  Could not find a dedicated posting URL on a second, more targeted pass;
  a fresh check of polis.org.cy/el/announcements today surfaced only
  unrelated notices (permits, vehicle sales), not this vacancy. `status`
  changed `open` → `unverified_possibly_stale`, `eligibility` changed
  `likely_eligible` → `unverified`. Should not be relied on without a
  direct call to the municipality.
- **Biopsy Diagnosis Ltd — still no specific posting URL found**, despite
  additional targeted searches. Relative-time language ("posted 13 days
  ago, expires in 17 days") could imply a deadline in the low-to-mid
  twenties of September, but this was deliberately left uncalculated
  (`deadline: null`) rather than presented as a stated fact.
- **ΕΟΑ Πάφου Administrative Officer — confirmed sound, still incomplete.**
  `source_url` is a genuine specific job listing (carierista.com id
  96542), not a category page — the record's underlying URL was fine.
  Deadline remains unconfirmed after 9 daily checks; this is a real gap,
  not a sourcing mistake.

## 2026-09-07 — Daily run

- **No changes** to the 7 tracked vacancies. `last_checked` updated to
  2026-09-07; CING and Biopsy Diagnosis records moved `status` `new` →
  `open`.
- CING Laboratory Scientific Officer: found a fuller role description
  (Mouse Facility duties — transgenic/wild-type colony management,
  supporting Neuroscience Dept. experimental projects, permanent
  full-time) but **still no confirmed deadline** from search snippets.
  The 8 September 2026 date already on record stays as the best-available
  estimate, not newly confirmed — today is the 7th, so this is still
  urgent if not already checked directly.
- ΕΟΑ Πάφου deadline unconfirmed for the **9th consecutive run**.
- Δήμος Πόλεως Χρυσοχούς Assistant Secretarial Officer: deadline still
  unconfirmed.
- No new vacancies found this run.
- Same source-access limitations persist (network egress policy).

---

## 2026-09-06 — Daily run

- **New (2):**
  - `cing-nicosia-laboratory-scientific-officer-20260906` — Cyprus
    Institute of Neurology and Genetics, Laboratory Scientific Officer
    (Mouse Facility, Neuroscience Dept), Nicosia. **Time-sensitive:**
    application deadline appears to be 7–8 September 2026 (two slightly
    different dates seen in search snippets for what may be the same
    batch — could not reconcile, flagged rather than guessed). Given how
    close this is, recommend checking cing.ac.cy/en/vacancies directly
    today rather than waiting for tomorrow's run.
  - `biopsy-diagnosis-nicosia-biomedical-scientist-20260906` — Biopsy
    Diagnosis Ltd, "Junior Medical Doctor / Biomedical Scientist",
    Nicosia. Title bundles two tracks; could not confirm which
    requirements apply to the Biomedical Scientist half. Logged with
    `eligibility: unverified` rather than guessed.
- **Unchanged (5):** ΕΟΑ Πάφου Administrative Officer (deadline
  unconfirmed — **8th consecutive run**), Δήμος Πόλεως Χρυσοχούς Assistant
  Secretarial Officer (deadline still unconfirmed), AMC (closed), INEX
  (not eligible), Polis Chrysochous Municipal Engineer (not eligible).
- Same source-access limitations persist (network egress policy);
  cing.ac.cy and ergodotisi.com both blocked to direct fetch, so today's
  two new records rely entirely on search-snippet content — flagged as
  such in their notes given the time-sensitivity of one of them.

---

## 2026-09-05 — Daily run

- **No changes.** All 5 tracked vacancies re-checked, same status as
  yesterday. `last_checked` updated to 2026-09-05; the Polis Chrysochous
  Assistant Secretarial Officer record moved `status` from `new` to `open`
  now that it's been seen on a second run.
- ΕΟΑ Πάφου deadline unconfirmed for the **7th consecutive run**.
- Δήμος Πόλεως Χρυσοχούς Assistant Secretarial Officer: no deadline
  surfaced either, still unconfirmed.
- One search surfaced a note that the AMC Medical Laboratory Scientist
  posting "was from May 2026" — inconsistent with the 26 Aug 2026 deadline
  already recorded. Given the conflict and that both figures come from the
  same kind of indexed/aggregated search content (not a direct page read),
  neither is treated as more authoritative — the record stays `closed` on
  the basis of the previously-confirmed deadline having passed; noted here
  for transparency rather than silently overwritten.
- ΕΟΑ Πάφου's wider posting batch (Economic Director, Accountant, Internal
  Auditor, Executive Engineer, etc.) is the same batch first seen around
  the Administrative Officer posting — not new, and none of the other
  titles in it were judged a clear enough profile fit to log (Internal
  Auditor is the closest, but typically needs an accounting/audit
  qualification beyond a general MBA — left out rather than guessed at).
- Same source-access limitations persist (network egress policy).

---

## 2026-09-04 — Daily run

- **New (1):**
  - `polis-chrysochous-assistant-secretarial-officer-20260904` — Δήμος
    Πόλεως Χρυσοχούς, Assistant Secretarial Officer (2 permanent posts).
    First non-engineering, admin-track vacancy ever found at Polis
    Chrysochous. Likely an entry/junior clerical grade rather than an
    MBA-level role — flagged honestly as strong-on-location,
    weak-on-seniority rather than oversold as a perfect match.
  - (Not logged: an Assistant IT Officer post from the same Polis
    Chrysochous announcement batch — IT-specific requirement, no fit.)
- **Unchanged (4):** ΕΟΑ Πάφου Administrative Officer (deadline still
  unconfirmed — **6th consecutive run**), AMC Medical Laboratory Scientist
  (still closed), INEX QA Manager (still not eligible), Polis Chrysochous
  Municipal Engineer (still not eligible — possibly the same announcement
  batch as today's new find, given a "Technical Services Officer, Civil
  Engineering" post also appeared in today's search).
- Same source-access limitations persist (network egress policy).

---

## 2026-09-03 — Daily run

- **No changes** to the 4 tracked vacancies. `last_checked` updated to
  2026-09-03.
- ΕΟΑ Πάφου deadline unconfirmed for the **5th consecutive run**.
- AMC Medical Laboratory Scientist re-confirmed still closed, no repost
  found yet.
- **Not logged as a formal vacancy, but worth surfacing:** Neapolis
  University Pafos's site indicates they take administrative-staff
  applications on a standing basis (email — check nup.ac.cy/vacancies/ or
  call +357 26843327). This is generic recruiting language, not a specific
  dated posting with a title/deadline, so it doesn't meet the bar for a
  trackable database record — flagging it in the report as a lead to
  pursue directly rather than fabricating specifics to force-fit it into
  the schema.
- Same source-access limitations persist (network egress policy).

---

## 2026-09-02 — Daily run

- **No changes.** All 4 tracked vacancies re-checked, same status as
  yesterday for all of them. `last_checked` updated to 2026-09-02.
- ΕΟΑ Πάφου deadline unconfirmed for the 4th consecutive run — one search
  result surfaced a deadline of 28/07/2025, but the source itself flagged
  that this was for a *different* EOAP position, not the current
  Administrative Officer posting, so it was correctly not applied here.
- OKYPY: another physician vacancy found (deadline 4/9/2026) — still not a
  lab-technologist fit, not logged, consistent with prior runs.
- CYTA: found Store Operator (retail) and Technical Officer
  (infrastructure/submarine cable) postings — neither matches the tracked
  profile, not logged.
- No new vacancy found at Polis Chrysochous or Paphos Municipality this run.
- Same source-access limitations persist (network egress policy).

---

## 2026-09-01 — Daily run

- **No changes.** All 4 tracked vacancies re-checked (ΕΟΑ Πάφου
  Administrative Officer, AMC Medical Laboratory Scientist, INEX QA
  Manager, Polis Chrysochous Municipal Engineer) — same status as
  yesterday for all of them. `last_checked` updated to 2026-09-01 on
  every record.
- ΕΟΑ Πάφου deadline is now unconfirmed for the 3rd consecutive run —
  still recommend calling them directly (26 818202 / 26 818276) rather
  than waiting on this tracker.
- AMC Medical Laboratory Scientist re-confirmed closed (deadline 26 Aug
  2026 already passed); no repost found yet.
- No new vacancy found at any tracked location this run, including
  Polis Chrysochous.
- PSC search surfaced a "Senior Administrative Officer" / "Social
  Insurance Officer" / "Archives and Communications Officer" public-service
  announcement, but it appears to be the same batch first indexed around
  13 May 2026 with no clear current-run confirmation and no stated
  location — not added as a new record; will re-check with a more
  targeted search next run rather than log stale/ambiguous data.
- Same source-access limitations persist (network egress policy).

---

## 2026-08-31 — Daily run

- **New (1):**
  - `polis-chrysochous-dimotikos-mixanikos-20260831` — Δήμος Πόλεως
    Χρυσοχούς, Municipal Engineer (permanent). First vacancy ever found at
    Polis Chrysochous since tracking began — but a civil/municipal
    engineering role, domain mismatch with the candidate's profile.
    Logged low-priority, not recommended.
- **Updated (1):**
  - `amc-nicosia-medical-laboratory-scientist-20260830` — a re-indexed
    listing for the same role surfaced a deadline (Wed 26 Aug 2026, 23:19)
    that has already passed as of this run → `status` changed `new` →
    `closed`. Worth re-checking in future runs in case AMC reposts it.
- **Unchanged (2):** `eoap-pafou-dioikitikos-leitourgos-20260830` (ΕΟΑ
  Πάφου Administrative Officer, still open, deadline still unconfirmed),
  `inex-paphos-qa-manager-20260830` (INEX QA Manager, still open,
  not eligible).
- **Sources still not directly fetchable:** same set as 2026-08-30 (gov.cy,
  psc.gov.cy, shso.org.cy, eac.com.cy, cyta.com.cy, pafos.org.cy,
  polis.org.cy, eoap.org.cy, and the major job aggregators) — network
  egress policy in this environment, unchanged from yesterday.
- OKYPY: still only physician (Ιατρικός Λειτουργός) vacancies found
  (deadlines now 4 Sep and 18 Sep 2026) — not a fit for the tracked
  profile, not logged.

---

## 2026-08-30 — First run (initial population)

- Database initialized empty; this run is the baseline, so everything found
  is "new" by definition.
- **New (3):**
  - `eoap-pafou-dioikitikos-leitourgos-20260830` — ΕΟΑ Πάφου, Administrative
    Officer (3 posts), Paphos city.
  - `amc-nicosia-medical-laboratory-scientist-20260830` — American Medical
    Center, Medical Laboratory Scientist, Nicosia.
  - `inex-paphos-qa-manager-20260830` — INEX Group, Quality Assurance
    Manager, Paphos city (logged low-priority, not eligible — domain
    mismatch).
- **Sources that could not be directly verified:** gov.cy, psc.gov.cy,
  shso.org.cy (OKYPY), eac.com.cy, cyta.com.cy, pafos.org.cy, polis.org.cy,
  eoap.org.cy, alpha.jobs, anergosjobs.com, carierista.com, cypruswork.com,
  cy-recruitment.com, newsincyprus.com — all blocked to direct fetch by this
  environment's network egress policy. Findings for these sources are based
  on WebSearch's indexed/synthesized content, with source URLs cited on each
  record; nothing was fabricated, but nothing from these sources was
  independently page-verified either. See the report's Caveats section.
- **No current match found** at Polis Chrysochous (top-priority location) —
  the only municipal listing found there was a General Duties Worker post
  whose deadline (11 Nov 2024) has long passed.

