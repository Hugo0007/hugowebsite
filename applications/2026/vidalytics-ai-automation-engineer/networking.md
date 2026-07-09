# Networking Plan — Vidalytics: AI Automation Engineer

- **Prepared by:** Networking Strategist agent
- **Date:** 2026-07-09
- **Investment level (application):** Level 3 Premium
- **Status:** DRAFTS ONLY — nothing sent. All messages require user approval.
- **Prior contact check:** `memory/recruiters.json` empty — no prior interaction with Vidalytics or Patrick Stiles. This is a first, cold touch.

---

## 1. People identified (public information only)

| Person | Role | Channels | Notes |
|---|---|---|---|
| **Patrick Stiles** | Founder & CEO — **the hiring manager**; role reports directly to him | LinkedIn: https://www.linkedin.com/in/patrickstiles/ (active; posts about Vidalytics and hiring) · X: https://x.com/pj_stiles (activity level **unverified** — check before engaging) · Email: p@vidalytics.com (**unverified, from a Feb 2022 LinkedIn post** — see §5) | Direct-response marketer: metrics-obsessed, allergic to fluff, "GSD" culture. Podcast hooks: One Stop Dev Shop (0→$72K MRR), Inspired Insider ($3B tracked sales), EO 360°, ClickBank Affiliated ep. 173. |
| No recruiter / no other named engineering leadership | — | — | ~20-person bootstrapped company; The Org shows Stiles at the top, no CTO/VP Eng surfaced. Stiles is the only outreach target — do **not** manufacture secondary contacts. |

## 2. Chosen strategy: Level 4 — Value-first outreach (single target)

**Reasoning:**

- There is no recruiter to message and no referral network to activate (no known mutual connections; Level 5 not viable). Level 1–2 waste the strongest fact about this opportunity: the decision-maker is publicly reachable and reads his own LinkedIn.
- Stiles is a direct-response operator. The JD explicitly rejects "chatbots that just talk" — the outreach must itself be a proof-of-work: one quantified result + one concrete automation idea built on *his* product (the Nov 2025 public API). A specific, measurable idea is the only outreach format this audience respects.
- The formal WWR process (5-min video, assessment, simulation) is the actual gate. Outreach **supplements** it: the goal is name recognition when the application hits his queue, not a side-channel around his own process. Every message acknowledges the formal process implicitly by referencing the submitted application.
- Sequencing: **application first, connection request same day, value message only after connection is accepted.** Never send the value message as a cold InMail — it reads as pitch spam to a DR marketer.
- Risk control: one target means one shot at a first impression. Zero pressure, no "pick my resume out of the pile" asks, hard stop after Day 14.

## 3. Drafted messages (for user approval — DO NOT SEND)

### 3a. LinkedIn connection request (send same day as application submission)

**Primary — product hook (recommended, 262 chars):**

> Hi Patrick — I just applied for your AI Automation Engineer role. Shipping a public API a month after Vids AI stood out: that API is the raw material for the internal automations the role describes. I build revenue-team agents in n8n + Claude. Glad to connect.

**Alternate — podcast hook (232 chars, use if user prefers the operator angle):**

> Hi Patrick — your One Stop Dev Shop episode (0→$72K MRR) stuck with me: leverage over headcount. I just applied for your AI Automation Engineer role — I build n8n/Claude agents that do revenue-team work end to end. Glad to connect.

*Why these pass the "could this go to anyone else?" test: both name a Vidalytics-specific artifact (the Nov 2025 API + Vids AI sequence; his specific podcast episode and MRR figure) that would be meaningless sent to any other founder.*

### 3b. Follow-on LinkedIn message (send after connection accepted; ~125 words)

> Hi Patrick, thanks for connecting. I applied for the AI Automation Engineer role this week and wanted to add one idea that didn't fit the application.
>
> Your November public API is the part of this role that interests me most: polling it for per-account video-performance deltas, piping those into CS health scores as HubSpot properties, and triggering churn-save playbooks *before* a customer's campaign winds down — Vidalytics' own product becomes the data source for retention ops. I've shipped the same shape of system: an AI lead-qualification agent (Claude + n8n + Airtable) that cut response times 30–60% by scoring, routing, and updating the CRM end to end.
>
> Happy to sketch that health-score pipeline on one page if it's useful — either way, good luck with the search.

*Notes: one quantified achievement (30–60%, verified in master resume), one Vidalytics-specific idea (API → CS health scores → churn-save plays, from research.md hooks), soft CTA, no pressure. Portfolio/Calendly deliberately withheld until Day 3+ — first message carries value only.*

### 3c. X/Twitter engagement option (@pj_stiles) — conditional

Research confirms the handle but **not** current activity. **Precondition: user checks https://x.com/pj_stiles first.** If active (posted within ~30 days): 1–2 substantive replies in the week around the application — never a DM, never a repeat of the LinkedIn message, never "I applied." Engage as a practitioner, not an applicant.

**Example reply (if he posts about Vids AI / AI features / hiring):**

> The underrated part of Vids AI is the training set — $3.5B in tracked sales means the drop-off patterns are learned from buyer behavior, not view counts. Curious whether the same aggregate data ends up powering internal ops (churn signals) as well as customer-facing insights.

If his X is dormant: skip entirely. One dead-channel reply looks like research theater.

### 3d. Follow-up drafts (only if no response to 3b)

**Day 3 — short nudge (LinkedIn):**

> Quick follow-up on the API → health-score idea, Patrick — no reply needed if you're mid-pipeline. If a one-pager of the flow would help evaluate my application, say the word. My recent builds are at ugo-landing.vercel.app.

**Day 7 — additional value (LinkedIn):**

> I went ahead and sketched it: one page covering the n8n flow — Vidalytics API polling → usage-delta scoring → HubSpot health properties → tiered churn-save plays (Slack alert / email sequence / AM task), with cost controls and a human-approval gate on anything customer-facing. Attached. Built to be thrown away or torn apart — it cost you nothing either way.

*(Dependency: requires user to approve creating the one-page sketch — a written architecture page, ~1–2 hours, no code. Flag to orchestrator. If not approved, substitute: a short note linking one relevant portfolio item with a sentence on how it maps to the CS-first mandate.)*

**Day 14 — final, graceful close (LinkedIn):**

> Last note from me, Patrick — I know the hiring process has its own track and I'm happy to be judged on it. If Vidalytics ever wants a second opinion on internal automation architecture, even outside this role, the offer stands. Thanks for reading, and good luck making the team AI native.

**After Day 14: archive. No further contact. Never exceed this cadence.**

## 4. Schedule (dates assume application submitted 2026-07-10; shift all dates by the actual submission date)

| Date | Day | Action | Channel | Gate |
|---|---|---|---|---|
| 2026-07-10 | 0 | Submit application (WWR process: video, assessment, simulation) | WWR | User approval of full packet |
| 2026-07-10 | 0 | Connection request (3a) | LinkedIn | User approval |
| 2026-07-10 → 13 | 0–3 | Optional: 1–2 substantive X replies (3c) | X | Only if @pj_stiles verified active; user approval per reply |
| On acceptance | — | Value message (3b) | LinkedIn | User approval |
| +3 days after 3b | 3 | Short nudge | LinkedIn | Only if no response |
| +7 days after 3b | 7 | One-page pipeline sketch (or portfolio note) | LinkedIn | Only if no response; sketch needs separate approval |
| +14 days after 3b | 14 | Final close | LinkedIn | Only if no response |
| After day 14 | — | Archive; update recruiters.json | — | — |

## 5. Email fallback — flagged

`p@vidalytics.com` comes from a **February 2022** public LinkedIn post about a different (Marketing Manager) opening. Four years old; may be dead, rerouted, or assistant-monitored. **Recommendation: LinkedIn first, exclusively.** Consider email only if (a) the connection request sits unanswered >7 days AND (b) the address is re-verified (e.g., current careers page or a verification tool) — and even then, send only the 3b message adapted, once, never the full follow-up sequence on a second channel in parallel. Running both channels simultaneously reads as pursuit, not professionalism.

## 6. Expected impact

- **Primary:** name recognition + "sent me a real idea" association when the application reaches Stiles's review queue — realistic lift on screen-pass probability, given hundreds of WWR "anywhere" applicants and a reader who filters for GSD signal.
- **Secondary:** the API → health-score idea pre-frames the interview/simulation conversation on ground the candidate has actually built on (n8n + Claude + CRM), and quietly counters the one Tier-1 gap (RAG) by demonstrating data-grounded system design.
- **Honest odds:** busy bootstrapping CEOs often accept connections but skip messages. The plan is calibrated so that zero response costs nothing: every message leaves value on the table and ends cleanly.
- **Failure mode avoided:** anything resembling pressure or flattery. Each draft was tested against "could this be sent to another company unchanged?" — none can.
