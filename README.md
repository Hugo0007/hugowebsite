# AI Career Operating System (AI-COS)

An autonomous, agent-driven job search system built to run on **Claude Code**.

AI-COS does not optimize for the number of applications submitted.
It optimizes for **interview invitations and job offers**.

## What this is

This repository is a complete operating system for a job search, run by a team of
specialized AI agents orchestrated by Claude Code:

| Layer | Where it lives | What it does |
|---|---|---|
| Chief AI Career Officer (CACO) | `CLAUDE.md` | Master strategy, decision rules, quality gates |
| 12 specialist agents | `.claude/agents/` | Discovery, scoring, ATS, research, resume, cover letter, demos, networking, interviews, learning |
| Workflows (slash commands) | `.claude/commands/` | `/scan`, `/evaluate`, `/apply`, `/briefing`, `/followups`, `/weekly-review`, `/status` |
| Memory & Knowledge System | `memory/` | Profile, applications, companies, recruiters, interviews, demos, learning — all versioned in git |
| Configuration | `config/` | Career targets, job sources, scoring weights, thresholds |
| Working assets | `applications/`, `demos/`, `portfolio/`, `reports/` | Everything generated per opportunity |

## Quick start

1. **Install Claude Code** (or open this repo on claude.ai/code).
2. **Fill in your profile**: edit `memory/profile.json` and paste your real resume
   into `memory/master-resume.md`. The system never fabricates — it can only work
   with truthful evidence you provide.
3. **Tune your targets**: review `config/career.yaml` (titles, salary floor,
   locations) and `config/scoring.yaml` (how jobs are scored).
4. Run your first commands:

```
/scan            # discover fresh remote jobs and score them
/status          # see the pipeline dashboard
/evaluate <url>  # run the Strategic Decision Engine on one job
/apply <company> # run the full application pipeline (ends at human approval)
/briefing        # daily briefing: priorities, follow-ups, pending approvals
/weekly-review   # weekly intelligence report
```

## Core guarantees

- **Truth**: no fabricated experience, metrics, or memories — ever.
- **Human-in-the-loop**: nothing is ever submitted without your explicit approval.
- **Memory-first**: agents consult `memory/` before creating anything new; nothing
  useful is ever lost or overwritten (git is the version control layer).
- **Quality over volume**: applications below the quality bar are revised, not sent.

## Workflow states

```
DISCOVERED → QUALIFIED → RESEARCHING → READY FOR RESUME → READY FOR DEMO
→ WAITING FOR APPROVAL → READY TO SUBMIT → SUBMITTED → FOLLOW-UP
→ INTERVIEW → OFFER / REJECTED → LEARNING
```

Every opportunity lives in exactly one state, tracked in `memory/applications.json`.

## Documentation

- `docs/GETTING-STARTED.md` — setup and first week of use
- `docs/ARCHITECTURE.md` — how the agents, memory, and workflows fit together
- `docs/WORKFLOW.md` — the end-to-end application lifecycle
- `AGENTS.md` — the agent registry and routing rules
