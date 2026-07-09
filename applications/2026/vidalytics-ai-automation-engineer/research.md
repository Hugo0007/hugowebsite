# Vidalytics — Company Research

**Role:** AI Automation Engineer, In-House (MarTech Video SaaS) — reports to CEO
**Researched:** 2026-07-09 by Company Intelligence agent
**Note on access:** vidalytics.com, Built In Austin, Himalayas, and WeWorkRemotely were blocked by the proxy (HTTP 403). Findings below come from web-search snippets of those pages plus podcast/directory sources. Items marked *(inference)* were not directly verified.

---

## Company Brief

- **What they do:** Video hosting + player + analytics platform built specifically for direct-response marketers — every feature is aimed at increasing conversions on VSLs (Video Sales Letters) and marketing videos, not just playing video. Flagship capabilities: conversion analytics, "smart autoplay" (restarts with sound when unmuted), Interactive Smart Vids (choose-your-path video), and a growing AI Suite.
- **Customers:** Direct-response marketers, entrepreneurs, and 8–10 figure DTC/info brands — named customers include Primal Labs, V Shred, iClosed, and Frank Kern. Typical customers reportedly pay ~$100–$1,000/mo. Claims videos hosted on the platform have driven **$3B+ (now $3.5B+) in tracked sales**.
- **Founder/CEO:** **Patrick Stiles** — founder & CEO, serial entrepreneur (~half a dozen businesses). Public backstory: overcame addiction and jail before building Vidalytics; frequent podcast guest (Inspired Insider "Top SaaS Series," EO 360°, ClickBank Affiliated ep. 173, List Building Lifestyle, One Stop Dev Shop — where he described growing 0 → $72K MRR in ~3 years).
- **Funding:** **Bootstrapped — no VC/outside funding** (GetLatka, Starter Story). GetLatka lists $697K ARR / 16 employees, but that data appears dated (2024 or earlier); podcast/company sources describe the business as "growing 100%+ per year and profitable." *(inference: current ARR is meaningfully above the Latka figure)*
- **Size:** ~16–22 employees (GetLatka: 16; RocketReach: 22; Indeed/LinkedIn bracket: 11–50). Founded ~2016–2017.
- **Location:** HQ Austin, TX; distributed/remote team (multiple fully-remote job posts, including Europe-only roles).
- **Competitors:** Wistia, Vimeo, VTurb, Voomly, Vidyard, SproutVideo/Adilo. Vidalytics runs aggressive comparison pages (vidalytics.com/compare/wistia, /vimeo, /vturb) positioning on price, conversion features, and analytics depth vs. general-purpose hosts.
- **Recent launches (last ~9 months, from their blog):**
  - **Oct 2025:** **Vids AI** — AI video insights trained on aggregated performance data from $3.5B+ in tracked video revenue (detects drop-off patterns); **Vid Stats Funnel View**.
  - **Nov 2025:** AI-powered **Captions Translation** (FR/DE/PT/ES/IT), Player Themes, and a **public API**.
  - **AI Suite** (ongoing): AI Script Analyzer (rewrites script sections against performance data), AI-Optimized Embed (SEO/LLM-discoverable summaries & chapters) — pitched as a closed loop: analyze → diagnose → fix → scale.
- **Tech stack:** Not publicly verifiable via search (no engineering blog, StackShare, or public GitHub org found). Known signals: they ship a JS embed player, a REST-style public API (Nov 2025), and the job posting names **n8n, Zapier, custom code, MCP, RAG, databases, APIs** as the automation toolchain. *(inference: web app backend stack unconfirmed)*

## The Role (from job listing, via search snippets — WWR page itself blocked)

- Reports **directly to the CEO**; mandate: "make Vidalytics AI native from top to bottom."
- Build agents, chains, prompts (written/versioned/tested like code), reusable org-wide "skills," and cross-system automations (n8n, Zapier, custom orchestration) so work flows without human intervention.
- Sequence: **revenue teams first (sales, marketing, customer success), then whole org**; includes coaching each team member to become AI-native.
- Hard requirements: shipped production AI systems others depend on ("not a learn-on-the-job role"), comfort with databases/APIs/MCP, RAG grounding for accuracy, judgment on managed tools vs. custom orchestration; a few years of AI on top of solid broader engineering experience.
- Benefits mentioned: 20 days PTO, paid classes/conferences/professional development.
- Hiring process (per Indeed snippets on Vidalytics generally): 5-minute video answers, personality assessment, and a **job simulation** mirroring real work. *(applies to their hiring generally; likely for this role too — inference)*

## Other Current Openings (hiring signals)

- **GTM MarTech Engineer (Growth & Attribution), Europe-only** — WWR. Signals heavy investment in revenue-ops/attribution tooling, adjacent to this role.
- An **Engineering** role posted ~June 29, 2026 (Built In).
- **Account Manager** (remote, "2 parts sales, 1 part CS") and a **VP of Sales** page on their site (date unverified).
- Read: they are scaling the GTM engine and want automation leverage rather than headcount. *(inference)*

## Pain Points (concrete AI/automation value for Vidalytics)

1. **High-touch revenue ops at ~20 headcount.** Two GTM hires (AM, VP Sales) plus a GTM MarTech Engineer posting = small teams drowning in lead routing, trial follow-up, and account touchpoints. Agentic lead-enrichment, scoring, and CRM hygiene automations directly multiply that team. *(inference from hiring pattern)*
2. **Support/CS triage for a self-serve SMB base.** Hundreds-to-thousands of $100–$1,000/mo customers means high ticket volume per CS head. RAG over docs/changelog for ticket deflection and draft-response agents is a classic first win — and the JD explicitly starts with customer success.
3. **Churn/expansion ops.** Direct-response marketers churn when campaigns end. Usage-signal pipelines (video uploads, play volume, API activity → alerts/playbooks in CRM) are automatable end to end. *(inference)*
4. **Content/comparison-page ops.** They compete on SEO comparison pages (vs. Wistia/Vimeo/VTurb) and a monthly-update blog cadence — AI-assisted content pipelines with human review fit their existing motion.
5. **Product-side AI leverage.** They already ship customer-facing AI (Vids AI, Script Analyzer, caption translation). Internal AI infrastructure (prompt versioning, evals, shared skills) can double as scaffolding for product AI features — a bootstrapped company will value that dual use. *(inference)*
6. **Onboarding/activation.** Conversion-obsessed company; trial-to-paid activation flows (personalized onboarding emails/videos triggered by in-app behavior) are on-brand and measurable. *(inference)*

## Talking Points (evidence-backed angles)

1. **"AI-native" is their word — mirror it with production proof.** The JD's core mandate is making the company AI native, starting with sales/marketing/CS. Lead with a shipped n8n/Claude automation that did real revenue-team work end to end (lead enrichment → CRM → outreach), stated in their own vocabulary: agents, reusable skills, prompts versioned like code.
2. **MCP + n8n is literally the listed toolchain.** The posting names n8n, Zapier, custom code, MCP, and RAG. Speak to specific architecture choices — when n8n suffices vs. when custom orchestration wins — since the JD explicitly tests that judgment.
3. **Their own AI Suite proves AI-forward DNA.** Reference Vids AI (Oct 2025) and AI Script Analyzer by name: "You've made your customers' video ops AI-native; this role does the same for your internal ops." Shows real research, no template smell.
4. **Bootstrapped + profitable = leverage over headcount.** They've grown 100%+/yr with no VC. Frame automation ROI in bootstrapper terms: each automation is a fractional hire that never churns. This matches Patrick Stiles' operator mindset from his podcast appearances.
5. **Their Nov 2025 public API is an open invitation.** Concrete hook: propose wiring Vidalytics' own API into internal workflows (e.g., video-performance data → CS health scores → churn-save plays) — demonstrates you'd automate *with* their product, not just around it.
6. **Conversion-metrics fluency.** Their culture is direct-response: everything measured in CVR and revenue. Express past automation wins in their language (response time cut, conversion lift, hours saved), not generic "efficiency."

## People / Outreach Channels

- **Patrick Stiles — Founder & CEO (the hiring manager for this role):**
  - LinkedIn: https://www.linkedin.com/in/patrickstiles/ (active; posts about Vidalytics and hiring)
  - X/Twitter: **@pj_stiles** (https://x.com/pj_stiles)
  - Email pattern: a public LinkedIn post by Stiles about a past Marketing Manager opening showed **p@vidalytics.com** as the contact address. *(historical; may still route to him — treat as plausible, verify before use)*
  - Podcast hooks for outreach personalization: Inspired Insider "Top SaaS Series" ($3B story), EO 360° (personal comeback story), ClickBank Affiliated ep. 173 (VSL metrics), One Stop Dev Shop (0→$72K MRR).
- **Recruiter/hiring contact for this specific role:** none named publicly; WWR posting page inaccessible. Given company size and direct-to-CEO reporting, Stiles is almost certainly the decision-maker. *(inference)*
- The Org lists Stiles at the top of the org chart; no CTO/VP Eng surfaced in search results (could not verify engineering leadership names).

## Sources

- WWR job posting (blocked; details via search snippets): https://weworkremotely.com/remote-jobs/vidalytics-ai-automation-engineer-in-house-martech-video-saas
- Vidalytics careers (blocked; via snippets): https://www.vidalytics.com/careers
- Vidalytics AI Suite: https://www.vidalytics.com/ai-suite
- Blog — Oct 2025 update (Vids AI, Funnel View): https://www.vidalytics.com/blog/10-2025-monthly-marketing-update
- Blog — Nov 2025 update (AI captions, API, themes): https://www.vidalytics.com/blog/11-2025-monthly-marketing-update-0d479
- Compare pages: https://www.vidalytics.com/compare/wistia , https://www.vidalytics.com/compare/vimeo , https://www.vidalytics.com/compare/vturb
- Inspired Insider — Patrick Stiles interview: https://www.inspiredinsider.com/patrick-stiles-interview/
- EO 360° podcast — Stiles episode: https://entrepreneursorg.libsyn.com/addict-to-entrepreneur-patrick-stiles
- One Stop Dev Shop podcast (0→$72K MRR): https://www.onestopdevshop.io/podcast/how-patrick-stiles-created-a-video-analytics-company-and-found-his-0-to-72000-mrr-in-3-years/
- ClickBank Affiliated ep. 173: https://podcasts.apple.com/in/podcast/173-unveiling-the-secrets-behind-the-vsl-ft/id1547482335?i=1000668862567
- GetLatka (ARR/headcount, dated): https://getlatka.com/companies/vidalytics
- Starter Story (bootstrapped breakdown): https://www.starterstory.com/vidalytics-breakdown
- Crunchbase: https://www.crunchbase.com/organization/vidalytics
- The Org — Stiles profile: https://theorg.com/org/vidalytics/org-chart/patrick-stiles
- Patrick Stiles LinkedIn: https://www.linkedin.com/in/patrickstiles/ ; X: https://x.com/pj_stiles
- LinkedIn post showing p@vidalytics.com: https://www.linkedin.com/posts/patrickstiles_vidalytics-marketing-manager-position-p-activity-6893784530428190720--da5
- Built In Austin (blocked; via snippets): https://www.builtinaustin.com/company/vidalytics-llc
- Indeed company page (hiring process): https://www.indeed.com/cmp/Vidalytics
- WWR company page / GTM MarTech Engineer (Europe): https://weworkremotely.com/company/vidalytics , https://weworkremotely.com/remote-jobs/vidalytics-europe-only-gtm-martech-engineer-growth-attribution-at-video-martech-saas
- G2 alternatives: https://www.g2.com/products/vidalytics/competitors/alternatives
