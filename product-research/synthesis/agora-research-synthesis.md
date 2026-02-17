---
product_area: agora
last_updated: 2026-02-17
interviews_considered: ["agora-liqwid-001"]
---

# agora – Research Synthesis

## Top themes by persona
- **DApp Developer / DeFi Protocol:**
  - **Urgent, Targeted Communication:** Protocols need to send critical, time-sensitive alerts (like liquidation warnings) to specific user segments through real-world channels like SMS, which are more effective than noisy public broadcasts.
  - **Secure & Trusted Channel:** There is a strong need for a communication channel that is verifiably from the protocol's team to protect users from prevalent scams on Discord and Telegram, thereby preserving trust and preventing user fund loss.
  - **Governance & Community Engagement:** Protocols want to reliably notify specific on-chain groups, such as all token holders, about important events like new governance proposals to drive participation and ensure quorum is met.

## Cross-cutting pains
- **Inability to prevent user fund loss:** DApps lack the tools to send urgent, real-world notifications (e.g., SMS) to users whose on-chain positions are at risk of liquidation.
- **Lack of targeted communication channels:** The only available channels are noisy, public broadcasts (e.g., Twitter), making it impossible to reach specific, relevant user segments like at-risk borrowers or all token holders.
- **Erosion of trust due to scams:** Users are frequently targeted by sophisticated scams on common support channels like Discord and Telegram, which damages the protocol's reputation and leads to significant financial losses for users.

## Mapped requirements
- **REQ-001 – Web2 Notification Bridge:** A system to send notifications triggered by on-chain events to users via traditional Web2 channels (e.g., SMS, email).
- **REQ-002 – Cardano "Blobs" for Storage:** A mechanism for on-chain data storage, likely to support messaging or trigger definitions.
- **REQ-003 – DApp-Defined Programmatic Triggers:** The ability for DApps to define specific on-chain conditions (e.g., a loan's health factor dropping below a threshold) that automatically trigger a notification.
- **REQ-004 – Prioritize MVP Notification Delivery:** The core focus for an initial product should be on the reliable and fast delivery of notifications.
- **REQ-005 – High-Throughput API Limits:** The system must provide an API capable of handling a large volume of notification requests to support protocols with many users and events.

## Open questions
- What specific Web2 notification channels (SMS, email, push notifications) are most critical for an MVP?
- How do protocols want to define user segments? Is it based on token holdings, wallet activity, or other on-chain data?
- What are the technical expectations for defining programmatic triggers? Do developers prefer a simple UI, a configuration file, or an SDK?
- What scale of notifications do large protocols anticipate sending? (e.g., messages per minute/hour) to better define "high-throughput".