---
product_area: cayley
last_updated: 2025-12-02
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- **SPO:** Stake Pool Operators need reliable, managed access to historical on-chain data. They currently bear the high operational cost and complexity of running their own infrastructure for analysis and debugging, as existing APIs are not built for historical queries.
- **Developer:** Developers (e.g., Heads of Engineering) building on Cardano need tools for cost visibility, forecasting, and control. They struggle to manage budgets and justify infrastructure spend due to opaque billing models and the fear of unexpected costs from traffic spikes.

## Cross-cutting pains
- Both personas face significant, hard-to-manage overhead when building on Cardano. For SPOs, this manifests as the operational cost and effort of maintaining infrastructure for historical data access. For developers, it's the financial cost of API usage and on-chain fees, which is opaque and difficult to control.

## Mapped requirements
- **REQ-001 – Managed historical data slices:** Provide managed, queryable historical data products (e.g., a first-class 'delegation history' slice) that users can subscribe to, removing their need to run and maintain their own indexing infrastructure.
- **REQ-002 – Cost management dashboards:** Offer dashboards that provide granular visibility into costs, broken down by project and/or feature.
- **REQ-003 – Budgeting and alerting tools:** Implement project-level budget caps and alerts to help teams prevent cost overruns during traffic spikes.
- **REQ-004 – Finance-friendly reporting:** Create a data export feature (CSV/API) that provides cost and usage data in a format easily consumable by finance departments.

## Open questions
- Are both the SPO and the SaaS Developer personas primary targets for `cayley`, or should we prioritize one over the other?
- For SPOs, what are the highest-value historical data sets they need beyond delegation history?
- For Developers, what specific metrics and formats are required for a 'finance-friendly' data export to be effective for their internal reporting?