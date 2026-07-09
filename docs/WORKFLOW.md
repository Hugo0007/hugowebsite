# The Application Lifecycle

Every opportunity moves through these states (tracked in
`memory/applications.json`). Only move forward when the state's required
outputs exist and quality gates pass.

| State | Entered when | Required outputs to advance |
|---|---|---|
| DISCOVERED | Scout finds the job | Opportunity record with URL + details |
| QUALIFIED | SDE scores ≥ 70 and recommendation accepted | Score, tier, level, priority, reasoning |
| REJECTED | Hard filter or score < 70 | Reason logged in decisions.md |
| RESEARCHING | /apply starts | research.md + ats-report.md |
| READY_FOR_RESUME | Research complete | resume-vN.md with ATS ≥ 90 |
| READY_FOR_DEMO | Level ≥ 3 and demo approved | Demo built, quality ≥ 95 (or explicitly skipped) |
| WAITING_FOR_APPROVAL | Packet complete + gates pass | **Explicit user approval** |
| READY_TO_SUBMIT | User approved | Submission instructions delivered |
| SUBMITTED | User confirms via /log-submission | submission.md + follow-up.md schedule |
| FOLLOW_UP | Day 3/7/14 checkpoints | Drafted messages approved & sent by user |
| INTERVIEW | Invite received via /log-outcome | interview-prep.md pack |
| OFFER | Offer received | Negotiation support, decision |
| CLOSED_REJECTED | Rejection received | Feedback captured verbatim |
| ARCHIVED | Day 14 passed silent, or user archived | Lesson recorded |

Terminal states (OFFER accepted, CLOSED_REJECTED, ARCHIVED) always trigger the
**learning** agent: lesson → `memory/learning.json`, aggregates →
`memory/metrics.json`.

## Investment levels

| Level | Time | Deliverables | When |
|---|---|---|---|
| 1 Quick Apply | 10–20 min | Tailored resume | Tier B/C with strong existing fit |
| 2 Customized | 30–60 min | + cover letter | Default for Tier B |
| 3 Premium | 2–4 h | + networking | Tier A, or Tier B at a dream company |
| 4 Elite | 4–12 h | + demo, architecture, repo, docs | Tier S only, max 1/week |

## Hard rules

1. No state skipping. 2. No submission without approval. 3. No fabrication —
every claim traces to `memory/master-resume.md`. 4. Every transition is
committed to git. 5. Quality gates are never lowered to hit a deadline.
