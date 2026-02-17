---
product_area: agora
last_updated: 2026-02-17
interviews_considered: ["agora-liqwid-001"]
---

# agora – Research Synthesis

## Top themes by persona
- **DApp Developer / DeFi Protocol:**
  - **Urgent, Actionable Alerting:** Protocols need to send time-sensitive notifications to users via real-world channels (like SMS) to prompt critical actions, such as adding collateral to prevent liquidation.
  - **Targeted Communication:** There is a need to move beyond noisy, public broadcast channels (like Twitter) to directly message specific user segments, such as all token holders for a governance vote or only borrowers at risk.
  - **Establishing a Trusted Channel:** Existing communication platforms like Discord and Telegram are compromised by scammers, creating a strong need for an authenticated, official channel where users can be certain messages are legitimate and not phishing attempts.

## Cross-cutting pains
- **Users lose funds due to lack of urgent alerts:** Protocols cannot send notifications through real-world channels like SMS, meaning users are often unaware when their loan positions are at risk of liquidation.
- **Inability to reach specific user segments:** Communication is limited to broad, public channels, making it impossible to effectively contact targeted groups like at-risk users or token holders for governance votes.
- **Trust is eroded by scams on existing channels:** When users seek support on Discord or Telegram, they are vulnerable to sophisticated scams, leading to loss of funds and damage to the protocol's reputation.

## Mapped requirements
- **REQ-001 – Web2 Notification Bridge:** A system to deliver on-chain alerts to users via traditional off-chain channels like SMS or email.
- **REQ-002 – Cardano "Blobs" for Storage:** A need for an on-chain data storage solution, likely to support messaging content or user targeting information.
- **REQ-003 – DApp-Defined Programmatic Triggers:** The ability for DApps to create custom, on-chain triggers (e.g., loan health factor) that automatically initiate a notification.
- **REQ-004 – Prioritize MVP Notification Delivery:** The core focus should be on building a reliable system for delivering notifications as the minimum viable product.
- **REQ-005 – High-Throughput API Limits:** The system must support a high volume of API calls to serve protocols with many users and frequent events.

## Open questions
- Are these communication pains (urgent alerts, targeting, trust) shared by other types of DApps beyond DeFi lending?
- What specific Web2 channels (SMS, email, push notification) do end-users prefer for different types of alerts?
- From the end-user perspective, what are the privacy implications or concerns with receiving these notifications?
- What is the expected cost or business model for a notification service? Who pays for it—the protocol or the user?