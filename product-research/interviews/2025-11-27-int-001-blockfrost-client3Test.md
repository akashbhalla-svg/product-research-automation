---
interview_id: client3-001
persona: Developer
segment: Individual
date: 2025-11-27
product_area: Blockfrost
pm_owner: akash
source: "Gemini transcript + notes"
project_tag: cayley
---

## Context (human-curated)
Mid-size SaaS company building a Cardano-enabled feature set into their product.
We spoke to the Head of Engineering to understand how they think about API billing, rate limits, and on-chain cost visibility.

## Raw notes (human-curated)
- They embed Cardano actions behind their own REST API; end users never see “Blockfrost” directly.
- Current usage is spiky: release days and campaigns cause big traffic bursts.
- Feels current tiering and limits are “a bit opaque” – they’re afraid of surprise bills.
- Wants clearer mapping from “our users did X” → “this is what it cost us on infra”.
- Likes the idea of on-chain PAYG but worries about operational complexity.
- Requests per-project and per-feature cost breakdowns, not just global account metrics.
- Mentioned that monthly budget approvals are strict; predictable caps and alerts are essential.
- Said they’d like to experiment more, but finance push back because they don’t understand the cost model.

## Transcript link
https://docs.google.com/document/d/1nYSxzZNyHzRm9guPZHH6auT9MaF21DgL1ri1RWfmu5o/edit?usp=sharing

## Key pains (human-curated)
- Lack of cost transparency per feature / project.
- Fear of surprise bills from traffic spikes.
- Difficulty explaining chain + API costs to finance.

## Jobs-to-be-done (human-curated)
- “When I ship a new chain-backed feature, I want to forecast and monitor its cost so I can get finance sign-off.”
- “When traffic spikes, I want guardrails so we don’t accidentally blow the budget.”

## Candidate requirements (human-curated)
- REQ-010 – Per-project and per-feature cost dashboards with historical views.
- REQ-011 – Budget caps and soft/hard alerts at the project level.
- REQ-012 – Simple finance-friendly export (CSV / API) for internal reporting.

## Gemini-normalised summary

## Note - how to use this:

When you do an interview, copy this file, rename it e.g.: yyyy-mm-dd-int-001-{product}-{user name}.md and update the front-matter + sections.
