---
product_area: agora
last_updated: 2026-02-17
interviews_considered: ["agora-liqwid-001"]
---

# agora – Research Synthesis

## Top themes by persona
- **DApp Developer / DeFi Protocol:**
  - **Urgent, Real-World Notifications:** Protocols need to send time-sensitive alerts, like liquidation warnings, to users through off-chain channels like SMS to prevent financial loss.
  - **Targeted On-Chain Communication:** There is a strong need to communicate with specific, on-chain user segments (e.g., at-risk borrowers, token holders) rather than relying on noisy, broadcast-only channels like Twitter.
  - **Trusted & Secure Channels:** Existing support channels like Discord and Telegram expose users to sophisticated scams, eroding trust. Protocols need a verifiable, secure channel to ensure users can distinguish official communication from fraudulent messages.

## Cross-cutting pains
- Users are losing money from liquidations because protocols lack a mechanism to send urgent, real-world alerts (e.g., SMS) when their positions are at risk.
- Protocols cannot effectively reach specific user segments, forcing them to use inefficient and noisy public broadcast channels for critical communications like governance proposals.
- The use of third-party platforms like Discord and Telegram for user support exposes users to scams, which damages the protocol's reputation and leads to user loss of funds.

## Mapped requirements
- **REQ-001 – Web2 Notification Bridge:** A system to connect on-chain events to off-chain notification services like SMS and email.
- **REQ-002 – Cardano "Blobs" for Storage:** A proposed solution for on-chain data storage.
- **REQ-003 – DApp-Defined Programmatic Triggers:** The ability for DApps to create custom, automated triggers for notifications based on on-chain conditions (e.g., loan health factor).
- **REQ-004 – Prioritize MVP Notification Delivery:** Focus initial development on the core functionality of delivering notifications reliably.
- **REQ-005 – High-Throughput API Limits:** The system must support a high volume of requests to serve large protocols.

## Open questions
- ...