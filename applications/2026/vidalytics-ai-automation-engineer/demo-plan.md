# Demo Plan — Vidalytics: AI Automation Engineer

- **Prepared by:** Demo Strategist
- **Date:** 2026-07-09
- **Application:** vidalytics-ai-automation-engineer-20260709 (Level 3, Priority A)
- **Status:** RECOMMENDATION ONLY — nothing built. Requires explicit user approval before any packaging, publishing, or outreach.

---

## Recommendation: **ADAPT/PACKAGE + thin Vidalytics one-pager** (Option B) — no new build

Package the existing **AI Lead Qualification Workflow** (Claude AI + n8n + Airtable, real 30–60% response-time metric) as a public proof asset, plus a single architecture one-pager tying Vidalytics' own public API (Nov 2025) into a revenue-team workflow. **Do not build anything new and runnable.**

### Why this beats the alternatives

The qualification stage's read ("package existing, spend remaining hours on CEO outreach") is directionally correct but understates one thing: **the resume links to github.com/Hugo0007, which currently has no public automation repos.** For a JD whose first hard requirement is "shipped production AI systems others depend on" ("not chatbots that just talk"), an empty GitHub is active negative signal when Patrick Stiles clicks the link. Packaging is therefore not polish — it patches a hole in the application. And because the demo library (`memory/demos.json`) is empty, this becomes the seed portfolio asset amortized across the entire pipeline (Axe Automation and every future AI-automation application), so most of its cost should not be charged to this one application.

The thin one-pager is added because the Level 3 plan centers on **direct CEO outreach**, and outreach to a bootstrapped direct-response operator converts far better with a concrete artifact than with prose. It also demonstrates, on paper, exactly the judgment the JD tests: when n8n suffices vs. when custom orchestration wins, guardrails, and cost control.

---

## Options considered

| Option | Hours (honest) | Interview-probability lift | Presumptuous-vs-impressive risk | Verdict |
|---|---|---|---|---|
| (a) Package existing project only (repo + README + diagram + Loom script) | 3–4 h (≈0.5 h is user recording time) | **Medium** — converts "trust me" resume claims into inspectable proof; fixes the empty-GitHub liability | Near zero — it's a portfolio, not a pitch | Good, but leaves the CEO-outreach artifact on the table |
| **(b) Package + Vidalytics one-pager (architecture sketch, not a build)** | **4–5.5 h total** (~3 h of it fully reusable) | **Medium-High** — proof asset + company-specific substance for outreach; pre-empts "another generic applicant" at hundreds-of-applicants WWR volume | **Low** — framed as "how I'd think about a first win, based on public info," not a prescription. Mitigate wrong-assumption risk with explicit "from public signals only" caveat | **RECOMMENDED** |
| (c) Full new demo build (e.g., working Vidalytics API → HubSpot lead-score pipeline) | 8–14 h honestly (sandbox HubSpot + Vidalytics API access + sample data + eval/guardrail layer to be credible; no real company data available) | **Medium at best, with downside** — without their data it risks looking like exactly the AI theater the JD warns about | **Moderate–High** — JD explicitly names "shiny-object syndrome"; an unsolicited 10-hour speculative build to a bootstrapper can read as poor prioritization. They also run a **job simulation** in hiring — build skill gets proven there anyway | Reject now; revisit **only** if they respond and an interview is scheduled (then a small pre-interview RAG/retrieval demo becomes the highest-ROI move, since RAG is the sole Tier 1 gap) |
| (d) Skip demos entirely | 0 h | **Below baseline** — leaves the empty-GitHub link contradicting the "shipped systems" claim, and leaves CEO outreach with nothing concrete to point at | n/a | Reject — this is the rare case where skipping costs probability |

---

## Specification (Option B)

### Deliverable 1 — Sanitized public repo: "AI Lead-Qualification Agent (Claude + n8n + Airtable)"

- **Demo type:** packaged production AI agent walkthrough (documentation-grade, not a fresh build)
- **Business problem it proves:** autonomous lead scoring, routing, and CRM updates for a lean revenue team — precisely the JD's "start where the money is: sales, marketing, CS" mandate
- **Contents:**
  - `README.md`: problem → architecture → outcomes (30–60% response-time reduction, stated exactly as verified in master resume — no inflation), plus a short "reliability" section covering validation, error handling, and how Claude's decisions are grounded in structured Airtable/CRM data (**verify exact mechanics with user first; never use the word "RAG" unless it truly applies**)
  - Architecture diagram (Mermaid in README): webhook intake → n8n orchestration → Claude scoring → Airtable/CRM sync → routing/notification
  - Sanitized n8n workflow export (client identifiers, credentials, real data all stripped) and example prompt(s) — only what the user confirms is shareable
  - Prompt-versioning note **only if** the user confirms prompts were genuinely iterated/versioned (per ats-report.md §5.4)
- **Loom script** (~90–120 seconds, written by us, recorded by user): problem, live n8n canvas walkthrough, one lead flowing end-to-end or a narrated dry run, outcomes in CEO language (response time, hours, errors)
- **Hours:** repo + README + diagram ≈ 2–2.5 h; Loom script 0.5 h; user recording ≈ 0.5 h
- **Reuse value:** **Very high** — first entry in `memory/demos.json`; attachable to every AI-automation application; fixes the GitHub-link liability permanently

### Deliverable 2 — Vidalytics-specific architecture one-pager (NOT a build)

- **Title (working):** "First 90 days of AI-native revenue ops at Vidalytics — one concrete example"
- **Content:** one-page sketch wiring the **Vidalytics public API (Nov 2025)** → engagement/usage signals → **HubSpot** lead-score & lifecycle updates → Slack alerts / CS churn-save plays. Annotated with the judgment calls the JD screens for: where n8n suffices, where custom orchestration (TypeScript) wins, where retrieval grounding is needed for accuracy, guardrails, and LLM cost control. Explicitly framed: "based on public information only — the real version starts by listening to your revenue team."
- **Use:** attached/linked in Patrick Stiles outreach and optionally referenced in the cover letter; echoes research.md talking point #5 (automating *with* their product, not around it)
- **Hours:** 1–1.5 h
- **Reuse value:** Medium — the pattern (target-company API → CRM → revenue play, annotated with orchestration judgment) is a reusable template even though the content is bespoke

### Total investment

- **4–5.5 hours**, of which ~3 h builds a permanent, pipeline-wide portfolio asset. Marginal cost attributable to Vidalytics alone: ~1.5–2.5 h — inside the Level 3 envelope alongside resume, letter, and outreach.
- **Expected interview-probability impact: Medium-High** (packaging converts claims to proof for a proof-demanding CEO reader; one-pager materially raises outreach response odds; neither can be mistaken for AI theater).

---

## Explicitly deferred

- **RAG/retrieval mini-demo** (sole Tier 1 gap): do **not** build speculatively. If Vidalytics responds or schedules an interview, escalate a small retrieval demo (est. 3–5 h) as a pre-interview asset — that is the moment its ROI turns positive.
- Any working Vidalytics/HubSpot integration build (Level 4 effort on an unproven response — not justified).

## Requires user approval before proceeding

1. Confirmation of what from the Manny Hall lead-qualification work may be **published publicly** (sanitization boundaries, client confidentiality).
2. Verification of workflow mechanics: how Claude outputs are grounded in Airtable/CRM data, and whether prompts were versioned/iterated (controls truthful wording).
3. Recording the Loom (user's voice/screen).
4. Publishing the repo on github.com/Hugo0007.
5. Any outreach send to Patrick Stiles (separate approval gate, per networking plan).
