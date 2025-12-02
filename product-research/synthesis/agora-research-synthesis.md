---
product_area: agora
last_updated: 2025-12-02
interviews_considered: ["2025-11-03-int-001-agora-pi-lanningham","agora-liqwid-001"]
---

# agora – Research Synthesis

## Top themes by persona
- **DApp/Infrastructure Developer:** This persona is focused on the foundational layer of communication. They are pained by protocol fragmentation, which increases their workload, and the technical limitations of on-chain messaging (e.g., high latency) that block real-time, interactive use cases. Their primary goal is to establish a secure, unified, and high-performance communication standard for the entire ecosystem.
- **DeFi DApp Leader:** This persona is focused on the application layer and solving specific, high-value user problems. They are pained by the inability to send targeted, urgent notifications to users (e.g., liquidation warnings), which leads to direct financial loss. Their primary goal is to establish a trusted, scam-proof channel to communicate critical, time-sensitive information to specific user segments.

## Cross-cutting pains
- **Insecure Communication Channels Lead to Financial Loss:** Both personas highlighted that current channels like Discord, Twitter, and Telegram are plagued by sophisticated phishing attacks, scams, and impersonators. This erodes user trust and results in significant, direct financial losses for their users.
- **Inability to Reach the Right Users:** Existing communication methods are limited to noisy, public broadcasts. DApps lack the ability to send targeted messages to specific user segments (e.g., at-risk borrowers, token holders) or to reliably deliver critical updates without them getting lost in the noise.
- **Technical Limitations Block High-Value Use Cases:** Current solutions are insufficient for modern DApp needs. On-chain messaging is too slow for interactive applications like gaming or intents, while a lack of off-chain integrations prevents critical real-world alerts like SMS notifications for liquidations.

## Mapped requirements
- **REQ-001 – Trusted, Targeted & Verifiable Messaging:** The system must provide a secure channel where users can be certain a message's origin is authentic, eliminating impersonation and scams. It must also enable DApps to target messages to specific user groups based on on-chain criteria (e.g., token holders, at-risk loan positions).
- **REQ-002 – Hybrid Architecture for Low-Latency & Off-Chain Actions:** To support interactive use cases and urgent alerts, the system must use a hybrid on/off-chain model. This avoids L1 finality delays for low-latency communication and enables bridges to Web2 notification systems (e.g., SMS, email) triggered by on-chain events.
- **REQ-003 – Unified Protocol & Developer-Friendly APIs:** To combat ecosystem fragmentation, the solution should promote a unified messaging standard while supporting interoperability with existing protocols (e.g., libp2p). This should be exposed through language-agnostic, high-throughput APIs to simplify developer integration.
- **REQ-004 – DApp-Defined Programmatic Triggers:** DApps need the ability to programmatically define the conditions under which a notification is sent. For example, triggering an alert when a loan's collateral ratio drops below a specific threshold.
- **REQ-005 – Capacity-Based Pricing Model:** A suggested business model is for DApps to pay based on capacity or usage, rather than a per-message fee which could be prohibitive for high-frequency use cases.

## Open questions
- What is the underlying identity model for ensuring messages are from a verified source and not an impersonator?
- How will the bridge to Web2 notifications (e.g., SMS) handle user privacy and the secure management of personal contact information?
- What are the specific performance benchmarks required for "low-latency" use cases like intent matching and gaming?
- What is the go-to-market strategy for driving adoption of a "unified standard" in an ecosystem with existing, competing solutions?
- How would a capacity-based payment model be structured? What units define "capacity" (e.g., messages/sec, data throughput, active connections)?