---
product_area: cayley
last_updated: 2025-12-02
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- **SPO (Stake Pool Operator):**
  - Needs reliable and performant access to historical on-chain data (e.g., full delegator history) without the cost and maintenance burden of running their own indexing infrastructure. Existing tools are built for "latest state" queries, not longitudinal analysis.
- **Developer (Head of Engineering):**
  - Needs visibility and control over API and on-chain costs. They cannot currently attribute costs to specific features, forecast expenses, or prevent budget overruns, which creates friction with finance and business planning.

## Cross-cutting pains
- **Unpredictable and unmanageable infrastructure costs:** Both personas struggle with the financial and operational overhead of their on-chain activities. One faces the high cost of running their own data infrastructure, while the other faces opaque and uncontrollable API billing from a third-party service.
- **Lack of purpose-built, business-ready tools:** The raw infrastructure and APIs available are insufficient. Users are forced to build fragile internal tools (SPOs for data indexing) or operate without key business controls (Developers for cost management), creating significant operational drag.

## Mapped requirements
- **REQ-001 – Managed Historical Data Slices:** Users need access to pre-packaged, queryable historical on-chain data sets (e.g., first-class "delegation history") via a managed subscription to avoid building and maintaining their own complex, expensive, and fragile indexing solutions.
- **REQ-002 – Cost & Budget Management Suite:** Users need tools to monitor, attribute, and control their on-chain/API costs. This includes per-project/feature cost dashboards, project-level budget caps with alerts, and finance-friendly data exports (CSV/API) for reporting.

## Open questions
- Are the needs for historical data access (SPO) and cost management (Developer) mutually exclusive, or do some users experience both pains?
- For SPOs, what other historical data slices beyond "delegation history" are most critical for their operations?
- For Developers, what specific level of granularity is required for cost attribution (e.g., per-API-key, per-feature tag)?
- What specific actions and thresholds are desired for budget alerts (e.g., email notification at 80%, hard stop at 100%)?