# Getting Started

## 1. One-time setup (30–60 minutes — this determines everything)

1. **`memory/profile.json`** — replace every TODO with real data. Work
   authorization and timezone matter: they gate which "remote" jobs you're
   actually eligible for.
2. **`memory/master-resume.md`** — paste your complete, truthful resume and
   fill the Achievement Library table. This is the only evidence base the
   agents may use. The Resume Intelligence agent refuses to run against a
   placeholder.
3. **`config/career.yaml`** — set your salary floor (enables automatic
   rejection of underpaying roles) and weekly capacity.
4. **`config/sources.yaml`** — add 5–10 dream companies under
   `target_companies`; their career pages get checked on every scan.

Commit these changes. Your memory is now version-controlled.

## 2. Daily rhythm

```
/briefing        # morning: theme of the day, top 3 actions, follow-ups due
/scan            # discover + score fresh jobs (run once a day, not obsessively)
/apply <company> # run the pipeline on an accepted recommendation
/followups       # draft any due follow-up messages
/log-submission <company>   # right after you actually submit
/log-outcome <company> ...  # any time you hear back
```

## 3. Weekly rhythm

```
/weekly-review   # honest scoreboard + next week's plan
/status          # anytime: pipeline dashboard
```

## 4. What the system will and won't do

**It will**: find and score jobs, research companies, decode job descriptions,
engineer tailored resumes and cover letters, plan and build demos, draft all
outreach, prep you for interviews, track everything, and learn from outcomes.

**It won't**: submit applications, send messages, or publish anything — those
are always your actions, after your approval. This is both a safety guarantee
and a practical one (accounts, CAPTCHAs, and platform rules make autonomous
submission unreliable).

## 5. Automation options (optional, later)

- Run this repo on claude.ai/code and use scheduled Routines to fire `/scan`
  every morning and `/weekly-review` on Fridays.
- Pair with n8n/Make for notification plumbing (e.g. new Tier S find → push
  notification) — the memory files are plain JSON, easy to read from any tool.

## 6. First week goal

Don't chase volume. Aim for: profile + master resume complete, 2–3 Tier A/B
applications out at Level 2–3 quality, one follow-up cadence running, and a
first `/weekly-review` to calibrate the scoring against reality.
