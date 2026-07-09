---
description: Run the Strategic Decision Engine on one specific job (pass a URL or pasted job description)
---

Evaluate a single opportunity end to end.

Input (URL or pasted job description): $ARGUMENTS

1. If a URL was given, fetch the posting. If text was pasted, use it directly.
   If neither, ask for one.
2. Launch the **qualification** agent to run all 10 stages of the Strategic
   Decision Engine on it. If the company is unknown and the score is
   borderline (within 5 points of a tier boundary), also launch
   **company-intelligence** to firm up the company-quality signal.
3. Record the opportunity and verdict in `memory/applications.json` and
   `logs/decisions.md`.
4. Present the full analysis: score with breakdown, tier, competition
   estimate, investment level, demo and networking recommendations, risks,
   interview/offer probability, and the single final recommendation.
5. If the recommendation is to apply, offer to start `/apply`. Wait for the
   user's decision.
