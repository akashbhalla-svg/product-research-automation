---
product_area: cayley
last_updated: 2025-12-03
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- **Stake Pool Operator (SPO):**
  - Needs to offload the significant cost and effort of running and maintaining their own infrastructure to get queryable, historical on-chain data.
  - Wants reliable, pre-packaged "data slices" (e.g., a delegator's full history) to accelerate the development of their own monitoring tools and to resolve customer issues more efficiently.
- **Developer (SaaS):**
  - Needs financial visibility and predictability for their on-chain operations.
  - Wants tools to monitor, forecast, and control costs at a granular level (per-project or feature) to manage budgets and gain internal approval for new initiatives.

## Cross-cutting pains
- Both personas are struggling with the operational and financial overhead of building on Cardano, though from different perspectives. For SPOs, the pain is the cost and complexity of running data infrastructure. For developers, it's the lack of visibility and control over API and on-chain fees, leading to fear of unexpected bills and difficulty in financial planning.

## Mapped requirements
- **REQ-001 – Managed, queryable historical data slices:** Provide access to specific, managed historical data sets, such as a first-class "delegation history" slice, via a subscription model.
- **REQ-002 – Granular cost dashboards:** Offer dashboards that break down API and on-chain costs by user-defined projects or features.
- **REQ-003 – Budgeting and alerting tools:** Implement project-level budget caps and alerts to prevent unexpected cost overruns during traffic spikes.
- **REQ-004 – Finance-friendly data exports:** Allow users to export cost and usage data in a format easily digestible by finance teams.

## Open questions
- Are the data infrastructure needs of SPOs and the cost management needs of SaaS developers part of the same core product offering, or do they represent two distinct user journeys?
- Beyond "delegation history," what are the next most valuable pre-packaged historical data sets for builders?
- For cost management, what is the ideal level of granularity for tracking? Is it by API key, a user-defined 'project' tag, or something else?
- What specific metrics and formats are required for a "finance-friendly" data export to be useful?