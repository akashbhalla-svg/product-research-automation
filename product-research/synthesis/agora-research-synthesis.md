---
product_area: agora
last_updated: 2025-12-02
interviews_considered: ["2025-11-03-int-001-agora-pi-lanningham","agora-liqwid-001"]
---

# agora – Research Synthesis

## Top themes by persona
- **DApp Developer / Core Infrastructure Builder:**
  - This persona is focused on the foundational layer of communication. They are blocked by the lack of a unified, high-performance messaging standard. Their primary needs are eliminating protocol fragmentation, enabling low-latency use cases (like gaming or intents) that are impossible with on-chain settlement, and providing a secure, verifiable communication primitive for the entire ecosystem.
- **DApp Developer / DeFi Protocol:**
  - This persona is focused on specific, high-value application use cases that directly impact user funds and engagement. They are unable to effectively protect and engage their users due to a lack of targeted, urgent, and trusted communication channels. Their primary needs are sending time-sensitive alerts (e.g., liquidation warnings) to prevent user loss, targeting specific user segments (e.g., token holders for governance), and providing a secure alternative to scam-ridden platforms like Discord.

## Cross-cutting pains
- **Insecurity of Existing Channels Leads to User Harm:** Both personas highlighted that their current communication channels (Discord, Twitter, Telegram) are fundamentally insecure. This directly leads to sophisticated phishing attacks, impersonation scams, and significant financial loss for their users, which erodes trust in their DApps and the ecosystem.
- **Inability to Reliably Target Specific Users:** Developers lack the tools to send messages to specific, relevant user groups. They are forced to use noisy, public broadcast channels (like Twitter) which are ineffective for critical, targeted information like liquidation warnings or governance proposals for token holders.
- **Technical Limitations Block Critical Use Cases:** Current solutions are insufficient. On-chain messaging is too slow for interactive or urgent applications, while off-chain solutions lack the security, verifiability, and trust needed. This blocks both low-latency applications (intents, gaming) and high-stakes financial alerts (DeFi notifications).

## Mapped requirements
- **REQ-001 – Trusted & Verifiable Messaging Channel:** The system must provide a way for users to be certain that a message originates from the legitimate DApp, eliminating the risk of impersonation and phishing scams. This could be achieved through a hybrid on/off-chain identity registry.
- **REQ-002 – High-Performance, Low-Latency Communication:** To support use cases like intents, gaming, and urgent alerts, the protocol must enable sub-second communication, which means avoiding L1 finality for every message.
- **REQ-003 – DApp-Defined Triggers & User Segmentation:** Developers need the ability to programmatically send messages based on on-chain events (e.g., loan health) and to target messages to specific user segments (e.g., all holders of a specific token).
- **REQ-004 – Unified Protocol & Developer-Friendly APIs:** The solution should simplify the developer experience by offering a single, unified standard that can support multiple underlying protocols (e.g., libp2p, Cardano native). It must expose its functionality through language-agnostic, high-throughput APIs.
- **REQ-005 – Web2 Notification Bridge:** To meet users where they are for urgent alerts, the system must be able to bridge on-chain events to real-world notification channels like SMS or push notifications.

## Open questions
- What is the right economic model? How do we balance the cost for developers (e.g., capacity-based payments vs. per-message) while preventing spam on the network?
- How should identity and key management work to ensure trust? Who controls the registry, and how do DApps and users securely enroll and manage their identities?
- What is the minimum viable product (MVP)? Should we prioritize the infrastructure for low-latency messaging or focus first on the application-level need for triggered, high-value notifications like liquidation alerts?
- How do users manage their notification preferences and opt-in to receive messages from different DApps? What does the user-facing experience look like?