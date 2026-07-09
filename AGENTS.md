# Agent Registry

Every agent has one responsibility. No agent works outside its scope.
Each agent's structured output becomes the next agent's input.
Always activate the smallest number of agents required for the mission.

| # | Agent | File | Responsibility | Primary output |
|---|-------|------|----------------|----------------|
| 1 | Opportunity Scout | `.claude/agents/opportunity-scout.md` | Discover fresh worldwide-remote jobs across sources | Opportunity records in `memory/applications.json` (state: DISCOVERED) |
| 2 | Qualification Strategist | `.claude/agents/qualification.md` | Strategic Decision Engine: score, tier, pick investment level | Score, tier, priority, recommendation |
| 3 | ATS Intelligence | `.claude/agents/ats-intelligence.md` | Decode the job description: keywords, hidden requirements | `ats-report.md` |
| 4 | Company Intelligence | `.claude/agents/company-intelligence.md` | Research the employer: product, funding, pain points | `research.md` |
| 5 | Resume Intelligence | `.claude/agents/resume-intelligence.md` | Engineer the strongest truthful tailored resume | `resume-vN.md` + ATS score |
| 6 | Cover Letter Writer | `.claude/agents/cover-letter.md` | Personalized, evidence-based cover letters | `cover-letter-vN.md` |
| 7 | Demo Strategist | `.claude/agents/demo-strategy.md` | Decide whether a demo is worth building (ROI-gated) | Demo recommendation + estimate |
| 8 | Demo Factory | `.claude/agents/demo-factory.md` | Build production-quality demonstrations | Working demo + repo + docs in `demos/` |
| 9 | Networking Strategist | `.claude/agents/networking.md` | Recruiter/hiring-manager outreach, referrals, follow-ups | `networking.md` + drafted messages |
| 10 | Interview Coach | `.claude/agents/interview-prep.md` | Interview prep: STAR stories, questions, mock interviews | Interview prep pack |
| 11 | Learning Analyst | `.claude/agents/learning.md` | Turn every outcome into training data; find patterns | Updates to `memory/learning.json` + reports |
| 12 | Chief of Staff | `.claude/agents/chief-of-staff.md` | Manage the user's time: daily focus, follow-ups, balance | Daily briefing + priority queue |

## Human approval and submission

Two roles from the original design are deliberately **not** autonomous agents:

- **Human Approval (Agent 10 in the spec)** is a hard gate enforced by CACO
  (`CLAUDE.md`): every packet is presented to the user, and nothing proceeds
  without explicit approval.
- **Submission (Agent 11 in the spec)** is executed by the human (accounts,
  CAPTCHAs, and ToS make autonomous form submission unreliable and risky).
  The system prepares everything — best submission path (careers page > referral
  > recruiter > hiring manager > LinkedIn > job board), copy-paste-ready answers
  to application questions, and the tracking record — then logs the submission
  in `memory/applications.json` via `/log-submission`.

## Routing table

| Trigger | Agents activated (in order) |
|---|---|
| `/scan` | Opportunity Scout → Qualification Strategist |
| `/evaluate <url>` | Qualification Strategist (+ Company Intelligence if borderline) |
| `/apply <company>` | Company Intelligence ∥ ATS Intelligence → Resume Intelligence → Cover Letter → Demo Strategist → Networking Strategist → **human approval** |
| Demo approved | Demo Factory |
| Interview scheduled | Interview Coach |
| Outcome recorded (offer/rejection/response) | Learning Analyst |
| `/briefing` | Chief of Staff |
| `/weekly-review` | Learning Analyst + Chief of Staff |

∥ = run in parallel.

## Contract

Every agent must:

1. Read `memory/profile.json`, `config/career.yaml`, and relevant memory files first.
2. Reuse existing assets when possible; never duplicate work.
3. Write outputs to the conventional locations (see `CLAUDE.md` → File conventions).
4. Include reasoning, evidence, and confidence with every recommendation.
5. Never fabricate. Never bypass the human approval gate.
