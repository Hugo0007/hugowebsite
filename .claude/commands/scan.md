---
description: Discover fresh worldwide-remote jobs across all configured sources and score them
---

Run the daily opportunity scan:

1. Launch the **opportunity-scout** agent to search all sources in
   `config/sources.yaml` for roles matching `config/career.yaml`. It must
   dedupe against `memory/applications.json` and record new finds with
   status DISCOVERED.
2. For each new find, launch the **qualification** agent to run the Strategic
   Decision Engine: score, tier, investment level, priority, recommendation.
3. Present a ranked results table: Company | Role | Score | Tier | Level |
   Recommendation | URL. Highlight anything Tier S or A.
4. For the top recommendation, ask whether to start the application pipeline
   (`/apply`). Do not start it without approval.

Extra arguments (optional): a specific source, title, or keyword to focus the
scan, e.g. `/scan wellfound` or `/scan "solutions architect"`.

$ARGUMENTS
