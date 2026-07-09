---
description: Record an outcome — recruiter response, interview invite, rejection, or offer — and extract the lessons
---

Log an outcome for: $ARGUMENTS

1. Find the application in `memory/applications.json`.
2. Determine the outcome type from the arguments (ask if unclear):
   - **Response** — recruiter/hiring manager replied → status FOLLOW-UP
   - **Interview** — invite received → status INTERVIEW; capture date/format;
     offer to launch **interview-prep** immediately
   - **Rejection** — status REJECTED; capture any feedback verbatim
   - **Offer** — status OFFER; capture terms; offer salary-negotiation support
3. Record the outcome with timestamp and details on the application record
   and in `memory/interviews.json` / `memory/recruiters.json` as relevant.
4. Launch the **learning** agent to extract the lesson and update
   `memory/learning.json` and `memory/metrics.json`.
5. Commit to git and report the updated pipeline picture.
