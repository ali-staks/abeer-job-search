# Abeer job search

A weekly Claude routine that searches for UK finance and operations jobs for Abeer Kirmani that pay at least £55,000 and come from employers licensed to sponsor a Skilled Worker visa.

- `PROMPT.md`: the routine prompt. Paste it into the routine, or point the routine at this file.
- `abeer_companies.csv`: the companies to check, with job feeds and sponsor register results. The routine adds to it each run.
- `seen_jobs.csv`: jobs already reported, so they aren't repeated.
- `runs/`: one results file per run.

The company list was first built on 13 October 2026 against that day's Home Office register of licensed sponsors.
