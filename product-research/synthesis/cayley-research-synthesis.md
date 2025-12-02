---
product_area: cayley
last_updated: 2025-12-02
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- **Persona A: Stake Pool Operator (SPO)**
  - SPOs are burdened by the cost and complexity of running their own infrastructure to get the historical on-chain data they need for analysis and debugging. Existing APIs are insufficient for their longitudinal analysis needs.
- **Persona B: Developer**
  - Developers building on the chain lack financial visibility and control. They struggle with opaque billing models, fear unexpected cost spikes, and find it difficult to forecast or justify infrastructure expenses to finance teams.

## Cross-cutting pains
- **High Operational & Financial Overhead:** Both personas face significant, hard-to-manage costs. For the SPO, it's the expense of running heavy infrastructure. For the Developer, it's the unpredictable cost of API usage. In both cases, the true cost of their on-chain activities is difficult to control and justify.
- **Inadequacy of Existing Tooling:** Current tools are not fit for purpose. Standard APIs are built for "latest state" queries, not historical analysis, and billing systems lack the granular dashboards, budget controls, and reporting needed for proper financial management.

## Mapped requirements
- **REQ-001 – Managed Historical Data Slices:** Provide reliable, managed, and queryable slices of historical on-chain data (e.g., 'delegation history') to eliminate the user's need to run and maintain their own indexing infrastructure.
- **REQ-002 – Granular Cost Dashboards:** Offer dashboards that break down API and on-chain costs by project and/or feature, providing clear visibility into spending.
- **REQ-003 – Budget Controls and Alerts:** Implement project-level budget caps and automated alerts to prevent cost overruns and surprise bills.
- **REQ-004 – Finance-Friendly Reporting:** Allow cost and usage data to be exported (e.g., CSV, API) in a simple format for non-technical stakeholders like finance departments.

## Open questions
- Are SPOs and SaaS Developers both primary personas for this product, or should we prioritize one set of needs?
- For historical data, what is the trade-off between offering powerful pre-defined slices (like 'delegation history') versus allowing users to configure their own custom slices?
- For cost management, what level of granularity is most critical for users to track (e.g., per-project, per-API key, per-feature tag)?
- Is there any overlap in needs? Would SPOs also find value in cost-management features for their operations?