---
description: Run the full application pipeline for a qualified opportunity (ends at the human approval gate)
---

Run the application pipeline for: $ARGUMENTS

0. **Locate** the opportunity in `memory/applications.json` (match by company
   or id). It must be QUALIFIED with an accepted recommendation to apply —
   if not, run /evaluate first. Create the folder
   `applications/<year>/<company-slug>-<role-slug>/` if missing.
   Set status: RESEARCHING.

1. **Research (parallel)**: launch **company-intelligence** and
   **ats-intelligence** simultaneously. Wait for both:
   `research.md` + `ats-report.md`.

2. **Resume**: launch **resume-intelligence** → `resume-v<N>.md` with ATS
   score. Status: READY FOR RESUME → done.

3. **Cover letter** (investment Level ≥ 2): launch **cover-letter** →
   `cover-letter-v<N>.md`.

4. **Demo decision** (Level ≥ 3, or when qualification flagged it): launch
   **demo-strategy**. If it recommends building, present the plan and STOP
   for approval before any build. Only after approval, launch **demo-factory**.

5. **Networking** (Level ≥ 3): launch **networking** → drafted messages and
   follow-up schedule in `networking.md`.

6. **Quality gates**: verify resume self-score ≥ 95 / ATS ≥ 90, letter is
   company-specific, zero fabrication (spot-check claims against
   `memory/master-resume.md`), folder complete. Fix anything failing.

7. **HUMAN APPROVAL GATE** — status: WAITING FOR APPROVAL. Present the packet:
   - Opportunity summary + score/tier + interview probability
   - The resume (with ATS report summary)
   - The cover letter
   - Demo plan/build (if any)
   - Networking messages and schedule (if any)
   - Recommended submission path: company careers page > referral > recruiter
     > hiring manager > LinkedIn > job board
   - Time invested so far

   **Wait. Never mark READY TO SUBMIT without explicit approval.**

8. On approval: status READY TO SUBMIT, give the user exact submission steps
   and copy-paste-ready answers for common application-form questions. Remind
   them to run `/log-submission <company>` once submitted. Commit the
   application folder to git.
