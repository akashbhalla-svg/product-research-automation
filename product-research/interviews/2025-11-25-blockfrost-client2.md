---
interview_id: client2-001
persona: SPO
segment: Mid-market / B2B
date: 2025-11-27
product_area: Blockfrost
pm_owner: akash
source: "Gemini transcript + notes"
---

## Context
Kora operates a mid-size Cardano SPO and uses several indexers and analytics tools.
We spoke to them to understand how they query historical chain data and what gaps they see in today’s tooling.

## Raw notes
- Currently uses a mix of Blockfrost, custom Postgres, and ad-hoc scripts for historical queries.
- Complains that most APIs are optimised for “latest state” not “longitudinal analysis”.
- They often need to re-index specific address sets or epochs to debug delegation issues.
- Has built internal tooling to cache slices of data (e.g. delegations per epoch) but it’s fragile.
- Mentions pain around syncing costs and infra: “I don’t want to maintain my own full index any more.”
- Wants a way to subscribe to a “slice” and trust it stays fresh and correct over time.
- Says they would pay more for reliability + support than for pure raw throughput.

## Transcript link
https://docs.google.com/document/d/1oTAdwK8Pxj-do_FwNbI9m9cAxWvv6b41XuaoOHiaTvc/edit?tab=t.mmry5tltwyaj

## Key pains (human-curated)
- Hard to get consistent, queryable historical views without running heavy infra.
- Current APIs don’t expose domain concepts (delegation histories, stake journeys) as first-class slices.
- Internal re-indexing is brittle and time-consuming for the team.

## Jobs-to-be-done
- “When I need to investigate a delegator’s history, I want to query a reliable slice instead of re-indexing data myself.”
- “When I ship monitoring / alerting, I want clean primitives for stake movement over time.”

## Candidate requirements
- REQ-001 – Define “delegation history” slice as a first-class primitive.
- REQ-002 – Allow SPOs to subscribe to managed historical slices without running infra.
- REQ-003 – Provide strong SLAs and observability for slice freshness and correctness.

## Gemini-normalised summary
- Persona: Mid-size Cardano SPO (Kora) managing indexers and analytics tools.
- Top 3 pains:
  - Hard to obtain consistent, queryable historical views (e.g., delegation history) without maintaining heavy, full-node infrastructure.
  - Current APIs are optimized for "latest state" and lack domain-specific longitudinal slices.
  - Internal custom tooling for re-indexing and caching data is brittle, costly, and time-consuming to maintain.
- JTBD:
  - When investigating a delegator's history, I want to query a reliable, pre-indexed slice so I don't have to re-index the chain myself.
  - When setting up monitoring, I want clean primitives for stake movement over time to ensure accuracy without building custom scripts.
- Suggested requirements:
  - REQ-001 – Define "delegation history" slice as a first-class primitive.
  - REQ-002 – Allow SPOs to subscribe to managed historical slices without running infra.
  - REQ-003 – Provide strong SLAs and observability for slice freshness and correctness.

SOURCE_ANALYSIS = {
  "used_pm_notes": 100,
  "used_transcript": 0,
  "reasoning": "The transcript describes an internal R&D meeting regarding 'Kfish', intents, and ZK proofs, which is entirely unrelated to the user interview with the SPO 'Kora' described in the PM notes; therefore, the transcript was ignored."
}
## Note - how to use this:

When you do an interview, copy this file, rename it e.g.: yyyy-mm-dd-int-001-{product}-{user name}.md and update the front-matter + sections.
