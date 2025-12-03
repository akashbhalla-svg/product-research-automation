---
product_area: agora
last_updated: 2025-12-03
interviews_considered: ["2025-11-03-int-001-agora-pi-lanningham","agora-liqwid-001"]
---

# agora – Research Synthesis

## Top themes by persona
- **DApp / Infrastructure Developer:**
  - Focused on the foundational layer of communication, this persona is pained by the lack of a secure, unified, and high-performance messaging standard in the ecosystem. They see current solutions (Discord, Twitter) as insecure and fragmented. Their goal is to build a robust and simple infrastructure that enables new, low-latency applications (like gaming or intents) and protects all users from scams at a protocol level.
- **DeFi Protocol Lead:**
  - Focused on application-level use cases, this persona needs to solve specific business problems that current channels cannot. They need to send urgent, targeted alerts to prevent user financial loss (e.g., liquidations), increase engagement (e.g., governance votes), and protect their brand's trust by providing a scam-proof alternative to public support channels like Discord.

## Cross-cutting pains
- **Pervasive Insecurity and Scams:** Both personas identified the insecurity of existing communication channels (Twitter, Discord, Telegram) as a critical pain point. This leads directly to users losing funds through sophisticated phishing attacks and impersonation scams, which erodes trust in their DApps and the ecosystem as a whole.
- **Lack of a Fit-for-Purpose Channel:** Current solutions are generic and not designed for Web3 needs. This forces developers to deal with a fragmented landscape of competing standards, while also lacking the core functionality needed for DApp-specific tasks like sending urgent, on-chain-event-driven, or targeted messages to specific user segments (e.g., token holders).
- **Performance Bottlenecks:** Relying on L1 on-chain transactions for messaging is too slow for interactive or real-time applications. This blocks entire categories of use cases, such as intent matching or gaming, that require sub-second communication.

## Mapped requirements
- **REQ-001 – Secure, Verifiable Identity & Messaging:** The system must provide a trusted channel where users can be certain a message's origin is authentic, eliminating the risk of impersonation and scams. This likely involves a hybrid on/off-chain registry to verify sender identity.
- **REQ-002 – High-Performance, Low-Latency Communication:** The protocol must support high-throughput messaging with sub-second latency to enable interactive applications. This explicitly rules out relying on L1 finality for every message.
- **REQ-003 – DApp-Driven, Targeted Notifications:** DApps need the ability to programmatically trigger messages based on on-chain events (e.g., a loan position nearing liquidation) and send them to specific user groups (e.g., all token holders, at-risk borrowers). This includes bridging to Web2 channels like SMS for urgent alerts.
- **REQ-004 – Unified & Interoperable Protocol:** To reduce developer overhead and prevent network fragmentation, the solution should support multiple underlying protocols (e.g., Cardano native, libp2p) and provide a single, unified, language-agnostic API for developers to build on.

## Open questions
- What is the right architectural balance between on-chain verifiability for security and off-chain infrastructure for performance and cost?
- How should the economic model function? A capacity-based payment model was suggested, but who pays (DApps, users), for what (messages, storage, capacity), and how?
- For a Web2 notification bridge, which specific channels (SMS, email, push notifications) are most critical for an MVP to solve urgent user needs like liquidation warnings?
- How will the system manage the mapping of on-chain identities (wallet addresses, token ownership) to off-chain communication endpoints (API hooks, phone numbers) in a secure and privacy-preserving way?