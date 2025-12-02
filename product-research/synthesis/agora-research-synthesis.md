---
product_area: agora
last_updated: 2025-12-02
interviews_considered: ["2025-11-03-int-001-agora-pi-lanningham","agora-liqwid-001"]
---

# agora – Research Synthesis

## Top themes by persona
- **DApp Developer / Technical Lead:**
  - **Security & Trust:** Developers are deeply concerned about exposing their users to phishing and scams through insecure Web2 channels like Discord and Twitter. They need a trusted, authenticated communication channel to protect their community and brand.
  - **Real-time & Urgent Communication:** There is a critical need for low-latency messaging that cannot be met by L1 transactions. Use cases range from urgent, "push-style" liquidation warnings to enabling interactive, real-time application features.
  - **Developer Experience & Simplicity:** Building and maintaining secure communication infrastructure is a major distraction. Developers are burdened by a fragmented ecosystem of competing standards and want a unified, simple-to-integrate solution.

## Cross-cutting pains
- **User security is compromised by insecure Web2 channels.** Both interviewees explicitly stated that relying on platforms like Discord, Twitter, and Telegram for critical announcements exposes their users to sophisticated phishing and wallet-draining scams.
- **Inability to deliver urgent, actionable messages.** Current on-chain methods are too slow for real-time needs. This prevents developers from building interactive applications and, more critically, from sending time-sensitive alerts like liquidation warnings that users will actually see in time.
- **High developer overhead due to ecosystem fragmentation.** Developers are forced to either build their own complex and secure communication solutions or learn and implement multiple, competing messaging protocols, which complicates their infrastructure and distracts from their core product.

## Mapped requirements
- **REQ-001 – Secure, Targeted & Triggered Notifications:** The system must allow DApps to send authenticated messages to specific user segments (e.g., at-risk borrowers, token holders) and allow these messages to be triggered programmatically by on-chain events.
- **REQ-002 – Unified Protocol Support:** To simplify developer infrastructure, the service should support multiple underlying communication protocols through a single, language-agnostic API.
- **REQ-003 – Web2 Channel Bridge:** The system must be able to link wallet addresses to off-chain notification channels like SMS and Email to ensure urgent alerts are delivered effectively to users.
- **REQ-004 – Flexible Architecture & Business Model:** The solution should consider a hybrid on/off-chain registry for identity, explore capacity-based payment models, and use efficient on-chain storage like Cardano "Blobs".

## Open questions
- What is the right architectural approach for message storage and identity, balancing decentralization, performance, and cost?
- How can we balance the desire for a unified standard that supports multiple protocols with the need for rapid MVP delivery? Which protocols are most critical to support first?
- What are the privacy and user consent models for linking on-chain wallets to off-chain personal identifiers like phone numbers and email addresses?
- What specific pricing model (e.g., capacity-based) is most viable and attractive for a wide range of DApp developers, from small projects to large protocols?