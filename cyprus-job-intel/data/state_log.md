# State Log

Running changelog of what changed between Cyprus Job Intelligence reports.
Newest entries at the top.

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

