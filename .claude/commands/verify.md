---
description: Browser-verify tracked postings — live check + free-application check + direct apply URL resolution
---

Run posting verification:

1. Collect target postings from `memory/applications.json`: everything in
   READY_TO_SUBMIT, WAITING_FOR_APPROVAL, and QUALIFIED states (or the
   specific company passed as an argument).
2. Launch the **posting-verifier** agent on them. It must:
   - probe network access first and report honestly if the environment's
     policy blocks job sites (do not fake results)
   - confirm each posting is live
   - classify the application path (FREE_DIRECT / FREE_ACCOUNT / PAYWALL /
     LOGIN_WALL_UNKNOWN)
   - resolve and record the direct, free employer apply URL
3. Present the verification table. For any PAYWALL or dead posting:
   recommend re-sourcing (find the employer's own listing) or archiving,
   and propose a source-priority downgrade in `config/sources.yaml`.
4. Update `memory/applications.json` and commit.

$ARGUMENTS
