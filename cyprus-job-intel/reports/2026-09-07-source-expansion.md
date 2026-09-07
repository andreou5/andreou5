# Cyprus Job Intelligence — Source Expansion & Cross-Check Addendum (2026-09-07)

This is a same-day addendum to the regular 2026-09-07 daily report, covering
two user-requested actions: (1) a direct cross-check of every tracked job
and URL, and (2) an expansion of the source list to include the Cyprus
Official Gazette and every known Cyprus job board.

## 1. Cross-check results (see also `data/state_log.md`)

- **ΕΟΑ Πάφου Administrative Officer — user-verified CLOSED.** The user
  opened the carierista.com listing directly (Ref #CA96542) and confirmed
  "This job post is expired." Settles what 9 automated checks could not.
  `status` → `closed`.
- **CING Laboratory Scientific Officer — deadline corrected.** Was recorded
  as "~8 September"; confirmed actual deadline is **7 September (today)**.
  Also recovered: reference code 360426, salary €76,184.17/yr gross (Scale
  A15/A16), and a specific third-party posting URL.
- **Polis Chrysochous Assistant Secretarial Officer — downgraded.** No
  dedicated posting URL found; a fresh check of the municipality's
  announcements page showed no trace of it. `status` → `unverified_possibly_stale`.
- **Biopsy Diagnosis Ltd — still unverified**, no specific posting URL found.

## 2. Source list expansion (user-requested)

Added to `skills/cyprus-job-search/SKILL.md` Section 3:
- **Cyprus Official Gazette** (Επίσημη Εφημερίδα) — mof.gov.cy/mof/gpo/gazette.nsf
- Corrected OKYPY's real domain (shso.org.cy, not the originally-guessed okypy.org.cy)
- Full Cyprus job-board sweep: Ergodotisi, CyprusWork, Alpha.jobs, CyprusJobs,
  FindJobsInCyprus, Bazaraki, CareerJet Cyprus, GRS Recruitment, CY Recruitment
  (Carierista and AnergosJobs were already in use)

Ran the expanded list immediately rather than waiting for tomorrow's run.

## 3. New vacancies found (6)

### Paphos city — strong (score 72, likely_eligible)
- **Administrative Officer / Personal Assistant** — GRS Recruitment, client:
  online marketing/affiliate group. Permanent, hybrid office admin + CEO
  executive support. **Salary confirmed: €18,000–€24,000/yr gross.**
  https://jobs.grsrecruitment.com/job/administrative-officerpersonal-assistant-11205.aspx
- **Executive Assistant / Office Coordinator** — GRS Recruitment (client
  unnamed). Supports senior management/board activities.
  https://jobs.grsrecruitment.com/job/office-manager-10902.aspx
- **Office Manager & Operations Coordinator** — Flexsy (online gaming
  tech), new Paphos office, explicit growth path into HR/operations/
  corporate support. No dedicated ad URL found — only Bazaraki's Paphos
  category page.

### Paphos city — moderate (score 60, likely_eligible)
- **Office Administrator / Receptionist** — GRS Recruitment, more junior
  than the listings above; full requirements not yet pulled.
  https://jobs.grsrecruitment.com/job/office-administrator--receptionist-11538.aspx
- **Office Administrator** — INEX Group (a different role from their
  already-tracked QA Manager posting). C1 English required. No dedicated
  ad URL found.

### Logged, not recommended
- **Project Manager (Civil Engineering)** — GRS Recruitment, Latsi (within
  the Polis Chrysochous municipal area). Domain mismatch — requires a
  Civil Engineering background.
  https://jobs.grsrecruitment.com/job/project-manager-10484.aspx

## 4. Checked, nothing added
- **Official Gazette itself**: search-indexed content only reproduced what
  PSC/gov.cy already surface — no unique Paphos/Polis-relevant vacancy
  found in this pass. Worth periodic direct checks since it's the
  authoritative source PSC/gov.cy draw from.
- **St George & Blue Cross Private Hospital, Paphos**: has a Clinical
  Laboratory Department directly relevant to the candidate's profile, but
  no current specific vacancy found — not logged, per the tracker's own
  no-fabrication rule. Worth checking their site/FindJobsInCyprus profile
  directly on a future run.

## Net effect

Paphos city went from 0 confirmed open matches (after ΕΟΑ Πάφου closed
this morning) to **5 open leads**, three of them tied for the register's
highest score (72/100). This is the first time the register has had a
genuine cluster rather than one fragile lead. Full detail: the dashboard
("The Paphos Register") and `data/vacancies.json`.
