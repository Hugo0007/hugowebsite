# Architecture

## Design principles

- **Modular**: every agent has one responsibility and its own file.
- **Observable**: every decision is logged (`logs/decisions.md`), every asset
  is a file, every change is a git commit.
- **Versioned**: nothing is overwritten — resumes and letters get version
  numbers; git is the rollback layer.
- **Memory-first**: agents read `memory/` before creating; outputs are written
  back so nothing is ever recreated from scratch.
- **Human-gated**: the system prepares; the human approves and submits.

## Layers

```
┌─────────────────────────────────────────────────────┐
│  CACO / Mission Control  —  CLAUDE.md               │
│  strategy, routing, quality gates, approval gate    │
├─────────────────────────────────────────────────────┤
│  Workflows  —  .claude/commands/                    │
│  /scan /evaluate /apply /briefing /followups        │
│  /weekly-review /status /log-submission /log-outcome│
├─────────────────────────────────────────────────────┤
│  Specialists  —  .claude/agents/  (12 subagents)    │
│  scout · qualification · ats · company · resume ·   │
│  cover-letter · demo-strategy · demo-factory ·      │
│  networking · interview-prep · learning · CoS       │
├─────────────────────────────────────────────────────┤
│  Memory  —  memory/*.json + master-resume.md        │
│  Config  —  config/*.yaml                           │
│  Assets  —  applications/ demos/ portfolio/ reports/│
│  Audit   —  logs/ + git history                     │
└─────────────────────────────────────────────────────┘
```

## Why files instead of a database

Claude Code's native strengths are reading, writing, and reasoning over files.
JSON + Markdown + git gives us: zero infrastructure, full version history,
human-readable state, easy portability (the whole system is one `git clone`),
and trivial integration with external tools (n8n, Airtable sync) later. If
volume ever demands it, `memory/*.json` maps 1:1 onto Airtable tables or
Postgres — the schemas are already defined in each file's `_schema` block.

## Data flow for one application

```
/scan → opportunity-scout ─→ applications.json (DISCOVERED)
        qualification ─────→ score/tier/level (QUALIFIED) + decisions.md
/apply → company-intelligence ∥ ats-intelligence
              └→ research.md        └→ ats-report.md
         resume-intelligence ──→ resume-vN.md (ATS-scored)
         cover-letter ─────────→ cover-letter-vN.md
         demo-strategy ────────→ demo plan (approval required to build)
         networking ───────────→ networking.md (drafts only)
         quality gates ────────→ HUMAN APPROVAL GATE
user submits → /log-submission → SUBMITTED + follow-up schedule
outcome      → /log-outcome    → learning agent → learning.json + metrics.json
```

## Extension points

- **New agent**: add a file to `.claude/agents/`, register it in `AGENTS.md`.
- **New workflow**: add a command to `.claude/commands/`.
- **Scoring changes**: edit `config/scoring.yaml` (learning agent proposes,
  user approves).
- **External sync**: scripts that push `memory/*.json` into Airtable/n8n can
  live in `scripts/`.
