---
product_area: cayley
last_updated: 2025-12-02
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- **SPO (Stake Pool Operator):**
  - SPOs are burdened by the cost and complexity of running their own infrastructure to get reliable historical on-chain data. Current APIs are optimized for "latest state" queries, not the longitudinal analysis they need for tasks like debugging delegator issues or monitoring stake movements over time. They need managed, queryable, and pre-packaged historical data to reduce their operational overhead.
- **Developer (Head of Engineering):**
  - Developers building on-chain applications lack tools for financial management and predictability. They struggle to understand the cost of their services on a per-feature basis, fear unexpected bills from traffic spikes, and find it difficult to justify infrastructure spending to finance teams due to opaque billing models. They need cost dashboards, budget controls, and reporting tools to align technical operations with business objectives.

## Cross-cutting pains
- Both personas face significant operational and financial overhead with their current solutions. Whether it's the cost of running heavy infrastructure for historical data (SPOs) or the unpredictable cost of API usage (Developers), there's a clear need for more managed, cost-effective, and predictable services.
- Both personas need data to be transformed from its raw on-chain state into a more usable, business-friendly format. SPOs need "clean, pre-packaged data primitives" for analysis, while Developers need "finance-friendly data exports" for reporting.

## Mapped requirements
- **REQ-001 – Managed historical data slices:** Provide access to queryable, managed historical data sets as a service, with a specific priority on delegator history for SPOs.
- **REQ-002 – Cost visibility dashboards:** Offer dashboards that break down API and on-chain costs by project and/or feature.
- **REQ-003 – Budgeting controls and alerts:** Implement project-level budget caps and automated alerts to prevent cost overruns during traffic spikes.
- **REQ-004 – Finance-friendly reporting:** Allow for the export of cost and usage data in formats easily consumable by finance teams, such as CSV or via an API.

## Open questions
- Are we building a single platform for both historical data access (for SPOs) and cost management (for Developers), or are these separate product offerings?
- For budget controls, is the primary need for alerts, or for hard enforcement (e.g., rate-limiting or blocking requests) once a cap is reached?
- Beyond delegation history, what are the other highest-priority historical data sets required by SPOs and other potential users?
- Is there an overlap in needs? Do developers building applications also struggle with historical data queries? Do SPOs need better cost management tools for their own operations?