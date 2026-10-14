# Abeer job search

A Claude routine that runs on Mondays, Wednesdays, and Fridays, and searches for UK finance and operations jobs for Abeer Kirmani. The jobs must pay at least £55,000 and come from employers licensed to sponsor a Skilled Worker visa. It covers both startups and large corporates.

- `PROMPT.md`: the routine prompt. Point the routine at this file (for example "Follow PROMPT.md in this repository"), so edits here take effect on the next run.
- `abeer_companies.csv`: the companies to check, with job feeds and sponsor register results. The routine adds to it each run.
  - `segment` marks a company as a startup or a corporate.
  - `last_checked` drives the search window. Blank means the company has never been checked, so the next run looks back 30 days. After that, each run looks back only to the last check, normally 24 hours.
- `seen_jobs.csv`: jobs already reported (`reported`) or ruled out (`excluded`, with a reason), so they aren't repeated.
- `runs/`: one results file per run.

The company list was first built on 13 October 2026 against that day's Home Office register of licensed sponsors. Large corporates were added on 14 October 2026.
