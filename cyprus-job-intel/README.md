# Cyprus Job Intelligence

Automated daily job-market intelligence for a Biomedical Science / Medical
Laboratory Technology + MBA candidate job-hunting in Cyprus.

- `skills/cyprus-job-search/SKILL.md` — the reusable search/report spec (candidate
  profile, source list, eligibility rules, location priority, scoring, report
  format). Edit this file to change how future runs behave.
- `data/vacancies.json` — persistent vacancy database.
- `data/state_log.md` — changelog of what changed between runs.
- `reports/` — one dated Markdown report per run.

Runs daily at 07:00 Cyprus time via a scheduled Routine.
