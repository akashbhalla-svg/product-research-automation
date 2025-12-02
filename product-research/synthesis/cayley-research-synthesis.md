---
product_area: cayley
last_updated: 2025-12-02
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- **SPO (Stake Pool Operator):**
  - Users are running and maintaining expensive, heavy infrastructure primarily to get reliable access to historical on-chain data for analysis and debugging (e.g., a delegator's full history). Existing tools and APIs are built for querying the latest state, not for this kind of longitudinal analysis, leading them to build fragile, time-consuming internal solutions.
- **Developer (Head of Engineering):**
  - Users lack financial visibility and control over their on-chain and API usage. They cannot easily track costs by feature, fear surprise bills from traffic spikes, and struggle to justify infrastructure spending to non-technical stakeholders like finance teams due to opaque billing models.

## Cross-cutting pains
- **Infrastructure Overhead and Cost Management:** Both personas struggle with the cost and complexity of their on-chain operations. The SPO experiences this as the direct operational cost of running nodes for historical data, while the Developer experiences it as opaque and unpredictable API bills. Both lack the tools to effectively manage and justify these costs.
- **Need for Purpose-Built Tooling:** Existing solutions are too generic. The SPO finds that standard APIs don't support historical analysis, and the Developer finds that billing systems aren't designed for granular, finance-friendly reporting and control.

## Mapped requirements
- REQ-001 – First-class 'delegation history' data slice
- REQ-002 – Subscription to managed historical data slices
- REQ-003 – Per-project and per-feature cost dashboards
- REQ-004 – Project-level budget caps and alerts
- REQ-005 – Finance-friendly data export (CSV/API)

## Open questions
- Are both the SPO and the SaaS Developer core target personas for this product, or should we prioritize one? Their needs for deep data access vs. financial tooling seem quite distinct.
- For SPOs, what other historical data slices beyond "delegation history" are critical for their operations?
- For Developers, what specific dimensions are needed for cost attribution (e.g., per-project, per-API-key, per-end-user)?
- How do these two sets of needs (historical data access and cost management) fit into a single, cohesive product vision?