---
product_area: cayley
last_updated: 2025-12-02
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- **SPO:**
  - Needs reliable, managed access to historical on-chain data without the cost and complexity of running their own infrastructure. Current tools are built for "latest state" queries, not the longitudinal analysis required for tasks like debugging delegator history.
- **Developer:**
  - Needs financial visibility and control over on-chain and API costs. The primary challenge is understanding, forecasting, and justifying infrastructure spending to non-technical stakeholders like finance teams, especially in the face of unpredictable user traffic.

## Cross-cutting pains
- **Operational overhead and opaque costs are a major burden.** Whether it's the technical overhead of maintaining fragile data-indexing infrastructure (SPO) or the financial overhead of managing unpredictable, hard-to-justify bills (Developer), both personas are spending significant resources on non-core activities.

## Mapped requirements
- **REQ-001 – Managed historical data slices:** Provide queryable, pre-packaged historical data sets (e.g., a first-class 'delegation history' slice) as a managed service.
- **REQ-002 – Cost management dashboards:** Offer dashboards that break down API and on-chain costs by project and/or feature.
- **REQ-003 – Budgeting and alerting:** Implement project-level budget caps and alerts to prevent surprise bills and control spending during traffic spikes.
- **REQ-004 – Finance-friendly reporting:** Allow for easy export of cost data (e.g., CSV/API) for internal financial reporting and justification.

## Open questions
- Are the needs for historical data access (SPO) and cost management (Developer) mutually exclusive, or do our personas experience both pains to some degree?
- What other historical data slices are most critical for SPOs beyond delegation history?
- For developers, what specific metrics and level of granularity are most crucial for their cost dashboards and finance reports?