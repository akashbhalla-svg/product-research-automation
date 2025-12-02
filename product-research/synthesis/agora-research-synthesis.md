---
product_area: agora
last_updated: 2025-12-02
interviews_considered: ["2025-11-03-int-001-agora-pi-lanningham","agora-liqwid-001"]
---

# agora – Research Synthesis

## Top themes by persona
- **DApp Developer / Infrastructure Builder:**
  - Needs a unified, low-latency communication protocol to simplify development and enable new real-time application types. They are frustrated by the fragmentation of competing standards and the inability to build interactive experiences due to L1 transaction latency.
- **DApp Developer / DeFi Protocol Lead:**
  - Needs a reliable, targeted notification system to alert users about time-sensitive events (like liquidations and governance) and drive specific actions. They struggle to reach users on effective channels (SMS, Email) and cannot easily segment their audience.

## Cross-cutting pains
- **Insecurity of Web2 Channels:** Both personas are forced to use channels like Discord and Twitter for user communication, which they know are insecure. This exposes their users to sophisticated phishing and wallet-draining scams, creating significant risk and reputational damage. Building a secure, in-house alternative is seen as a major distraction from their core product.

## Mapped requirements
- **REQ-001 – Unified & Performant Protocol:** The system must provide a unified messaging standard to reduce ecosystem fragmentation and developer overhead. It needs to support low-latency, sub-second message delivery to enable real-time applications, moving beyond the limitations of L1 transactions for every message.
- **REQ-002 – Targeted & Trigger-Based Notifications:** DApps need the ability to target specific user segments (e.g., at-risk borrowers, token holders) and define programmatic triggers for sending alerts.
- **REQ-003 – Web2 Channel Integration:** The solution must be able to link on-chain wallet addresses to off-chain communication channels like SMS and Email to ensure users receive critical, "push-style" notifications.
- **REQ-004 – Developer-Friendly APIs & Go-to-Market:** Provide language-agnostic APIs with clear, developer-friendly rate limits. The project should prioritize a rapid MVP delivery and explore a capacity-based payment model for DApps.
- **REQ-005 – Hybrid On/Off-Chain Architecture:** The system should use a hybrid architecture, such as an on/off-chain registry and on-chain data storage (e.g., Cardano "Blobs"), to balance security, performance, and cost.

## Open questions
- What is the right balance between building a generalized, unified protocol (per the Infrastructure Builder persona) versus a specialized, high-value notification service for DeFi use cases (per the DeFi Lead)?
- How should the system handle user consent, privacy, and PII (Personally Identifiable Information) when linking wallets to Web2 channels like SMS and Email?
- What specific metrics (e.g., messages per second, active users, data storage) should a capacity-based pricing model be based on to align with the value DApp developers receive?
- What is the ideal trust and decentralization model for a hybrid on/off-chain registry to prevent it from becoming a centralized point of failure or censorship?