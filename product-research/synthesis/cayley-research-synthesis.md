---
product_area: cayley
last_updated: 2025-12-02
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- **SPO (Stake Pool Operator):** Needs reliable, managed access to historical on-chain data to avoid the high cost and complexity of running and maintaining their own indexing infrastructure. Current tools are built for "latest state" queries, not the longitudinal analysis they require for tasks like debugging delegator issues.
- **Developer (Head of Engineering):** Needs tools for cost visibility, predictability, and control for their on-chain usage. They struggle to track costs per feature, fear surprise bills from traffic spikes, and find it difficult to justify infrastructure spending to non-technical stakeholders like finance.

## Cross-cutting pains
- **High and unpredictable operational/financial overhead:** Both personas are struggling with the cost of building on the platform. For SPOs, it's the cost of running their own heavy infrastructure to get the data they need. For developers, it's the opaque and unpredictable cost of API usage and on-chain fees. Both lack the tools to efficiently manage and justify these costs.

## Mapped requirements
- **REQ-001 – Managed historical data slices:** Provide queryable, pre-packaged historical data sets (e.g., "delegation history") as a managed service to eliminate the need for users to run their own indexers.
- **REQ-002 – Cost visibility dashboards:** Offer dashboards that break down usage and costs by project and/or feature.
- **REQ-003 – Budgeting and alerting tools:** Implement project-level budget caps and alerts to prevent unexpected cost overruns during traffic spikes.
- **REQ-004 – Finance-friendly data exports:** Provide a simple way to export cost and usage data (e.g., CSV or dedicated API) for financial reporting and analysis.

## Open questions
- For historical data, what are the most critical data slices beyond "delegation history"? What are the latency and freshness requirements for these queries?
- For cost management, what is the ideal level of granularity for tracking costs (e.g., per API key, per endpoint, per-feature tag)?
- How should budget caps be enforced? Should they trigger a hard limit (stopping service) or soft alerts (notifications)?
- What is the willingness to pay for these distinct capabilities (managed data vs. cost controls)? Are they part of a core subscription tier or add-on products?