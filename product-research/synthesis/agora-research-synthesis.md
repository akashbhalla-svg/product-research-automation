---
product_area: agora
last_updated: 2026-02-17
interviews_considered: ["agora-liqwid-001"]
---

# agora – Research Synthesis

## Top themes by persona
- **DApp Developer / DeFi Protocol:**
  - **Urgent, Real-World Notifications:** There is a critical need to send time-sensitive alerts to users on Web2 channels (like SMS) for on-chain events, especially to prevent financial loss from liquidations.
  - **Targeted & Segmented Communication:** Protocols need to move beyond noisy, public broadcast channels (like Twitter) and message specific user groups, such as at-risk borrowers or token holders, to drive specific actions like adding collateral or voting.
  - **Trusted & Secure Channel:** Existing community channels (Discord, Telegram) are rife with sophisticated scams, eroding user trust and causing financial loss. A verifiable, official communication channel is needed to ensure users can distinguish legitimate messages from scams.

## Cross-cutting pains
- Users are losing money from liquidations because protocols lack a mechanism to send them urgent, off-chain alerts when their positions are at risk.
- Protocols cannot effectively reach or mobilize specific segments of their user base (e.g., token holders for governance votes), as their only channels are public broadcasts.
- User trust is damaged and funds are lost due to prevalent scams on support channels like Discord and Telegram, with no way for users to verify the source of a message.

## Mapped requirements
- **REQ-001 – Web2 Notification Bridge:** Addresses the need to send urgent, real-world alerts (e.g., SMS, email) to users based on on-chain events.
- **REQ-002 – Cardano "Blobs" for Storage:** A suggested technical implementation for on-chain data storage.
- **REQ-003 – DApp-Defined Programmatic Triggers:** Enables protocols to define the specific on-chain conditions (e.g., loan health factor dropping) that should trigger a notification.
- **REQ-004 – Prioritize MVP Notification Delivery:** A strategic requirement to focus initial development on the core value proposition of reliable, urgent notifications.
- **REQ-005 – High-Throughput API Limits:** A technical requirement to ensure the system can scale to handle notifications for a large user base.

## Open questions
- What specific Web2 notification channels (SMS, email, push notification) are most critical for an MVP?
- How do DApps envision defining and managing programmatic triggers? Via an SDK, a dashboard, or another method?
- What are the key user segments protocols want to target, and what on-chain data is required to define them?
- How can we ensure the notification channel itself is and remains a trusted, verifiable source for users?