---
product_area: agora
last_updated: 2025-12-03
interviews_considered: ["2025-11-03-int-001-agora-pi-lanningham","agora-liqwid-001"]
---

# agora – Research Synthesis

## Top themes by persona
- **DApp Developer / Infrastructure Builder:**
  - Needs a unified, high-performance messaging standard to reduce ecosystem fragmentation and developer workload from supporting multiple competing protocols.
  - Requires low-latency, sub-second communication capabilities to enable interactive applications like gaming and intents, which are impossible with on-chain settlement delays.
- **DApp Developer / DeFi Protocol:**
  - Needs a trusted and direct communication channel to send urgent, time-sensitive alerts to users to prevent financial loss (e.g., liquidations).
  - Wants the ability to target messages to specific on-chain user segments (e.g., at-risk borrowers, token holders) to drive specific actions like adding collateral or voting in governance.

## Cross-cutting pains
- **Insecurity of Existing Channels:** Both personas highlighted that current communication channels like Discord, Twitter, and Telegram are rife with sophisticated impersonation scams and phishing attacks. This leads directly to user financial loss and erodes trust in their DApps.
- **Lack of Targeted, Reliable Delivery:** Developers have no reliable way to reach specific groups of users based on their on-chain status. Their only options are noisy, public broadcasts that are easily missed or insecure direct messages that are often scams.

## Mapped requirements
- **REQ-001 – Unified & Multi-Protocol Support:** The system should provide a single, unified messaging standard to reduce developer overhead, while also supporting existing protocols like libp2p to avoid further fragmentation.
- **REQ-002 – DApp-Defined On-Chain Triggers:** DApps need the ability to programmatically trigger notifications based on on-chain events, such as a loan's health factor dropping or a new governance proposal being created.
- **REQ-003 – Web2 Notification Bridge:** The system must be able to bridge on-chain triggers to real-world notification channels that users will see immediately, such as SMS and mobile push notifications.
- **REQ-004 – High-Performance, Language-Agnostic APIs:** The service requires robust, language-agnostic APIs with high throughput to support both large-scale notification delivery and low-latency interactive use cases.
- **REQ-005 – Hybrid On/Off-Chain Architecture:** To enable high-speed, interactive use cases and avoid L1 finality delays, the system should use a hybrid on/off-chain model for tasks like identity registration and message delivery.

## Open questions
- What is the viable economic model? A "capacity-based" payment model was suggested, but the willingness to pay and specific pricing structure are unknown.
- How will sender identity be technically established and verified to create the "trusted channel" that both DApps and their users need to combat phishing?
- Should the MVP prioritize high-reliability, urgent notifications (for DeFi) or low-latency interactive messaging (for gaming/intents)? These use cases may have conflicting architectural requirements.