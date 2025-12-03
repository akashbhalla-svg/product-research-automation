---
product_area: cayley
last_updated: 2025-12-03
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- **SPO (Stake Pool Operator):**
  - **Difficulty accessing historical data:** Existing tools are built for the latest state of the chain, making it difficult and expensive to get queryable historical views (e.g., a delegator's full history) without running heavy, custom infrastructure.
  - **High overhead of self-managed tools:** Internal tools for indexing and querying chain data are brittle, time-consuming to maintain, and require significant operational effort. Users want managed, pre-packaged solutions to ship features faster.
- **Developer (Head of Engineering):**
  - **Lack of cost visibility and control:** It's impossible to see how much specific features or projects are costing in API/chain fees, leading to fears of unexpected bills from traffic spikes.
  - **Difficulty justifying and managing budget:** Without clear cost forecasting and reporting, it's hard to get budget approval from finance for new projects and experiments.

## Cross-cutting pains
- **Unpredictable costs and high overhead:** Both personas struggle with the unmanaged nature of accessing chain data. For SPOs, this manifests as high operational costs for running their own infrastructure. For Developers, it's the financial cost of API usage. Both lack the tools to forecast, control, and report on these costs effectively.
- **Need for managed, "out-of-the-box" solutions:** Both users are building their own brittle, time-consuming tooling to solve their problems. They want to offload this complexity to a managed service that provides clean, pre-packaged data slices, dashboards, and financial controls so they can focus on their core product.

## Mapped requirements
- **REQ-001 – Managed historical data slices:** Provide access to queryable, managed historical data sets as a service, with specific slices like "delegation history" available via subscription.
- **REQ-002 – Granular cost dashboards:** Offer dashboards that break down API and on-chain costs by user-defined projects or features.
- **REQ-003 – Budgeting and alerting tools:** Implement project-level budget caps and automated alerts to prevent unexpected overspending.
- **REQ-004 – Finance-friendly reporting:** Allow for the export of cost and usage data in a format easily digestible by non-technical teams like finance.

## Open questions
- What other specific historical data slices are most critical for SPOs beyond delegation history?
- How can we technically enable users to attribute costs to a specific project or feature (e.g., via API keys, tags)?
- What specific formats and data points are required for a "finance-friendly" data export?
- Are the needs for historical data access and cost management part of a single, unified product, or do they represent two distinct user journeys and potential offerings?