```markdown
---
product_area: cayley
last_updated: 2025-12-03
interviews_considered: ["client2-001","client3-001"]
---

# cayley – Research Synthesis

## Top themes by persona
- **SPO (Stake Pool Operator):** SPOs need reliable, managed access to historical on-chain data to support their operational and development needs (e.g., investigating delegator issues, building monitoring tools) without the high cost and maintenance overhead of running their own indexing infrastructure.
- **Developer (SaaS):** Developers building on-chain applications need tools for cost visibility, budget control, and financial reporting. They struggle to manage expenses, prevent unexpected bills from traffic spikes, and justify new projects to non-technical stakeholders like finance.

## Cross-cutting pains
- Building and maintaining internal tooling for operational needs—whether for re-indexing historical data or for monitoring on-chain costs—is a significant, brittle, and time-consuming burden that distracts from core product development.

## Mapped requirements
- REQ-001 – Managed, queryable historical data slices (e.g., full delegation history) available via subscription.
- REQ-002 – Granular cost dashboards that can be filtered by internal project or feature.
- REQ-003 – Project-level budgeting controls with configurable spending caps and alerts.
- REQ-004 – Exportable, finance-friendly cost and usage reports.

## Open questions
- What specific historical data "primitives" are most valuable to users beyond delegation history?
- For developers, what is the desired behavior when a budget cap is reached (e.g., hard stop on API calls vs. continued service with notifications)?
- How do teams currently attempt to forecast on-chain costs for new projects, and what data would make that process easier?
- Is there an overlap in needs? Do SPOs also struggle with cost visibility, or do developers also need better access to historical chain data for their applications?
```