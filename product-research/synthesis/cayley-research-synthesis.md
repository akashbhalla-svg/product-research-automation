---
product_area: cayley
last_updated: 2025-12-01
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- SPO (Mid-size):
  - Struggles with APIs optimized only for "latest state," making longitudinal analysis difficult.
  - High operational burden and cost associated with maintaining full nodes just to access specific domain slices (e.g., delegation history).
  - Willingness to pay a premium for guaranteed reliability and support rather than raw throughput.
- Developer (Head of Engineering):
  - severe anxiety regarding cost management, specifically surprise bills from traffic spikes.
  - Difficulty securing budget approval due to complex cost models and lack of visibility into per-feature usage.
  - Needs automated guardrails and clear reporting to satisfy strict finance teams.

## Cross-cutting pains
- **Visibility Gaps:** Users lack granular visibility, whether it is historical chain data (SPO) or cost breakdowns by feature (Developer).
- **Barriers to Scaling:** Both personas face friction scaling their operations—SPOs are limited by fragile infrastructure maintenance, while Developers are limited by finance pushback on unpredictable costs.
- **Need for Historical Context:** There is a shared need for historical views; SPOs need historical ledger data, while Developers need historical cost/usage data for forecasting.

## Mapped requirements
- REQ-001 – First-class "delegation history" slice primitive
- REQ-002 – Managed historical slice subscriptions
- REQ-003 – SLAs for slice freshness and correctness
- REQ-010 – Per-project and per-feature cost dashboards with historical views
- REQ-011 – Budget caps and soft/hard alerts at the project level
- REQ-012 – Simple finance-friendly export (CSV / API) for internal reporting

## Open questions
- How do we balance the SPO need for premium, high-reliability SLAs with the Developer need for strict budget caps and cost containment?
- Can the pricing model accommodate the "spiky" nature of SaaS campaigns (Developer) while supporting the continuous, heavy historical queries required by SPOs?