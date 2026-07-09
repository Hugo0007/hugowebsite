# Loom Walkthrough Script — AI Lead-Qualification Agent

Target: 90–120 seconds. Tone: calm, concrete, zero hype. Record screen showing
the n8n canvas (sanitized workflow), switching briefly to Airtable and the README diagram.

---

**[0:00–0:15] The problem — talk over the README**

"Small revenue teams lose deals in the gap between a lead arriving and a
qualified person looking at it. I built a system that closes that gap
completely — I'll show you how it works in about ninety seconds."

**[0:15–0:45] The flow — n8n canvas**

"A lead comes in by webhook — form, email, any source. First thing that happens
is validation and de-duplication — before any AI touches it, because that's the
cheapest place to catch bad data. Clean leads land in Airtable as structured
records. Then Claude scores each one — and this is the important part: it
scores against structured business data and versioned prompt templates, so
qualification criteria live in data we control, not in the model's imagination.
The output is constrained to machine-readable fields — no prose parsing."

**[0:45–1:15] The routing — follow one lead through**

"Based on the score, the lead routes automatically: qualified leads get an
owner assigned and the CRM updated in seconds; nurture-tier leads enter a
follow-up sequence; edge cases go to a human queue *with Claude's reasoning
attached*, so review takes seconds. Nobody triages manually anymore."

**[1:15–1:30] The result — back to README**

"In production this cut lead response times thirty to sixty percent and
removed manual lead processing from the sales workflow entirely. Not a chatbot —
a system that finishes work. The architecture and design decisions are all in
the README. Thanks for watching."

---

Recording checklist: sanitized workflow only · no client names on screen ·
no credentials visible · 1080p · mic check first.
