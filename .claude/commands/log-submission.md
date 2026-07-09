---
description: Record that an application was submitted (company, method, confirmation)
---

Log a submission for: $ARGUMENTS

1. Find the application in `memory/applications.json` (must be READY TO SUBMIT
   or WAITING FOR APPROVAL — if the latter, confirm the user really approved
   and submitted).
2. Ask for (or extract from the arguments): submission method (careers page /
   referral / recruiter / hiring manager / LinkedIn / job board), submission
   time, confirmation number or email if any, and which resume/letter versions
   were used.
3. Update the record: status SUBMITTED, `submitted_at`, method, versions,
   confirmation. Write `submission.md` in the application folder.
4. Create the follow-up schedule in `follow-up.md`: day 3 check, day 7 value
   follow-up, day 14 final — with concrete dates.
5. Update `memory/metrics.json` counters, append to `logs/decisions.md`,
   and commit to git.
6. Confirm back with the follow-up dates.
