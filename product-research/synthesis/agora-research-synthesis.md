---
product_area: agora
last_updated: 2025-12-03
interviews_considered: ["2025-11-03-int-001-agora-pi-lanningham","agora-liqwid-001"]
---

# agora – Research Synthesis

## Top themes by persona
- **DApp Developer / Core Infrastructure:** This persona is focused on the foundational layer of communication. They are pained by the lack of a secure, high-performance standard, which leads to fragmented developer effort and an inability to build interactive, low-latency applications (e.g., gaming, intents). Their primary goal is to establish a unified, multi-protocol infrastructure that is both secure and performant.
- **DApp Developer / DeFi Protocol:** This persona is focused on application-level communication to solve urgent business needs. They are pained by their inability to protect users from financial loss (liquidations, scams) and drive specific actions (e.g., governance votes) because current channels are insecure, untargeted public broadcasts. Their primary goal is to send trusted, targeted, and timely notifications to specific user groups based on on-chain events.

## Cross-cutting pains
- **Insecure Communication Channels Lead to Costly Scams:** Both personas highlighted that their current channels (Discord, Twitter, Telegram) are rife with impersonators, leading to sophisticated phishing attacks and scams that cause users to lose funds and erode trust in their DApps.
- **Inability to Target Specific User Segments:** Existing communication methods are primarily public broadcasts. This prevents developers from reaching specific, relevant groups, such as token holders for a governance vote or a small set of borrowers nearing liquidation.
- **Technical Limitations Block Critical Use Cases:** Both personas are blocked by the technical constraints of current solutions. On-chain messaging is too slow for interactive applications, and there is no reliable bridge to send urgent, real-world notifications like SMS to users.

## Mapped requirements
- **REQ-001 – Secure, Authenticated Messaging Channel:** A core requirement is a trusted channel where users can be certain a message originated from the legitimate DApp team, eliminating the risk of impersonation and scams.
- **REQ-002 – Multi-Channel & Protocol Support:** The system must support communication across different protocols (e.g., Cardano native, libp2p) and be able to bridge to Web2 notification systems (e.g., SMS) to reach users with urgent alerts.
- **REQ-003 – High-Performance, Low-Latency Communication:** To enable interactive use cases like gaming and intents, the system must support sub-second message delivery, which implies a hybrid or off-chain settlement model.
- **REQ-004 – DApp-Defined On-Chain Triggers:** DApps need the ability to programmatically trigger notifications to specific users based on on-chain events, such as a loan position becoming risky or a new governance proposal being created.
- **REQ-005 – Developer-Friendly, High-Throughput APIs:** The service must provide language-agnostic APIs with high rate limits to make integration simple and support applications with a large user base or high message volume.

## Open questions
- What is the preferred payment model for this service? One interview suggested a capacity-based model, but this needs to be validated across different DApp types.
- How should user identity and notification preferences (e.g., opting into SMS alerts) be managed securely and privately?
- What is the ideal technical balance between on-chain components (for trust and discovery) and off-chain infrastructure (for performance and cost)?
- What specific trust mechanisms are required to prove a message's origin? Is a signed message sufficient, or is a more complex on-chain identity registry needed?