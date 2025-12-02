---
product_area: cayley
last_updated: 2025-12-02
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- **Stake Pool Operator (SPO):**
  - The primary challenge is the difficulty and high cost of accessing and querying historical on-chain data. They are forced to run and maintain their own complex, brittle infrastructure because existing APIs are optimized for the latest state, not for historical analysis like a delegator's full transaction history.
- **Developer (SaaS):**
  - The main concern is the lack of financial visibility and control over on-chain and API costs. They cannot easily track spending per feature, fear unpredictable bills from traffic spikes, and struggle to justify budgets to non-technical stakeholders like finance teams.

## Cross-cutting pains
- Both personas are forced to build and maintain time-consuming, brittle internal tools to solve for gaps in the existing infrastructure—whether for historical data indexing or for financial monitoring and reporting.
- There is a clear need for more "managed" or "productized" services that abstract away the raw operational complexities of building on the chain, specifically around data access and cost management.

## Mapped requirements
- **REQ-001** – Subscription-based access to managed, queryable historical data slices (e.g., "delegation history").
- **REQ-002** – Granular cost dashboards with breakdowns by project or feature.
- **REQ-003** – Budgeting tools, including project-level caps and alerts, to prevent cost overruns.
- **REQ-004** – Finance-friendly data exports for cost analysis and reporting.

## Open questions
- What specific historical data slices, beyond delegator history, are most valuable to users?
- For cost management, what specific metrics and dimensions are required for finance teams to confidently approve budgets?
- Is there a desire to correlate on-chain activity (the SPO's focus) with its associated cost (the Developer's focus)?