---
product_area: cayley
last_updated: 2025-12-02
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- **Stake Pool Operator (SPO):**
  - Needs reliable and performant access to queryable historical on-chain data without the cost and maintenance burden of running their own heavy infrastructure. They are blocked by existing tools that focus on the "latest state" and want pre-packaged, managed data slices (e.g., delegation history) to build their own monitoring and analytics tools more efficiently.
- **Developer (SaaS):**
  - Needs financial visibility and control over their on-chain and API usage. They currently cannot attribute costs to specific features, fear unexpected bills from traffic spikes, and struggle to justify budgets to non-technical stakeholders like finance. They require tools for cost forecasting, monitoring, and setting budget guardrails.

## Cross-cutting pains
- Both personas are struggling with the total cost and complexity of using on-chain data. For the SPO, this manifests as high operational overhead for self-hosted infrastructure. For the SaaS Developer, it's a lack of visibility and control over direct financial costs (API fees), leading to budget uncertainty and risk.

## Mapped requirements
- **REQ-001 – Managed, queryable historical data services:** Users need access to managed, pre-packaged historical data slices (e.g., full delegation history) via subscriptions or queries, removing the need to run and maintain their own indexing infrastructure.
- **REQ-002 – Comprehensive cost management and reporting tools:** Users need a suite of financial tools including granular cost dashboards (by project/feature), project-level budget caps with alerts, and finance-friendly data exports to enable forecasting and budget control.

## Open questions
- What specific historical data slices, beyond delegation history, are most critical for our target personas?
- For cost management, what level of granularity (e.g., by API key, by feature tag) is required for effective cost attribution?
- How do users weigh the direct cost of a managed service against the indirect operational cost and complexity of running their own infrastructure?