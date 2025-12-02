---
interview_id: 2025-11-03-int-001-agora-pi-lanningham
persona: DApp Developer / SPO
segment: DeFi / Infrastructure
date: 2025-11-03
product_area: Cardano PubSub (Agora)
pm_owner: reza
source: "Gemini transcript + notes"
project_tag: agora
---

## Context
Interview with Pi Lanningham, Lead/CTO at Sunday Labs (SundaeSwap). We spoke to him to validate the "Agora" decentralized PubSub communication protocol, gather feedback on its architecture (specifically regarding latency and developer experience), and discuss potential collaboration. Pi represents a key user persona (DApp developer and infrastructure builder) who faces the current challenges of secure user communication.

## Raw notes
-   **Current State:** Uses Twitter, Website, and Discord for announcements (governance, features).
-   **Pain Points:** Security is critical; compromised Twitter accounts lead to wallet-draining scams. "Trust-dependent channels" are a major vulnerability.
-   **Protocol Feedback:**
    -   **Overlap:** Concerned about overlap with Mithril’s DMQ protocol. Strongly advises extending DMQ rather than creating a new standard to avoid developer fatigue.
    -   **Architecture:** Wants APIs to be generic and well-documented (e.g., gRPC) for use in Rust/Go, not just wrapped in a TypeScript SDK (cited Midnight's mistake here).
    -   **Latency/Economics:** Pointed out that on-chain settlement for *every* message kills sub-second delivery. Suggested "capacity payment" or "credit-based" models (pay upfront, debit messages) or using Hydra.
    -   **Interoperability:** Advised supporting both Cardano native mini-protocols and industry standard **libp2p** to allow easy bridging from chains like Polygon or Midnight.
-   **Collaboration:** Sunday Labs is very interested in contributing dev expertise (Decentralized systems, Cardano, Midnight) to the working group.

## Transcript link
https://docs.google.com/document/d/1hGtEtGCKqbRWwYapWLBKcYRalbss9SZkPlFIHTdNfM0/

## Key pains (human-curated)
-   **Phishing & Scam Risk:** Reliance on Web2 channels (Twitter, Discord, Telegram) exposes users to impersonators and wallet drainers; there is no authenticated, secure channel to reach users.
-   **Developer Fragmentation:** Proliferation of different messaging standards (e.g., Mithril DMQ vs. Agora) creates unnecessary cognitive load and implementation work for node/DApp developers.
-   **Latency Limitations:** Current L1 transaction finality (minutes) makes sub-second messaging impossible if every message requires an on-chain proof, blocking use cases like gaming or intents.
-   **SDK Lock-in:** Protocols often launch with only a TypeScript SDK, forcing non-TS developers (e.g., Rust) to reverse-engineer undocumented APIs.

## Jobs-to-be-done
-   **Securely Announce Updates:** Reach users with critical news (governance votes, new features) without fear of platform compromise or impersonation.
-   **Enable Low-Latency Interaction:** Support interactive applications (e.g., poker rooms, intent matching) that require sub-second message delivery.
-   **Simplify Infrastructure:** Run a single node/software stack that handles multiple protocols (native Cardano + libp2p) without complex sidecars.

## Candidate requirements
-   **REQ-001 – Unified Messaging Standard:** The protocol MUST extend or align with the existing Mithril DMQ work rather than introducing a conflicting standard.
-   **REQ-002 – Capacity-Based Payment Model:** The system SHOULD support prepaid capacity or credit accounts to allow message transmission without per-message L1 transaction latency.
-   **REQ-003 – Language-Agnostic APIs:** APIs MUST be generic, well-documented, and accessible directly (e.g., via gRPC) for developers using languages other than TypeScript (e.g., Rust).
-   **REQ-004 – Dual-Stack Support:** The protocol SHOULD support message ingestion via both Cardano native mini-protocols and **libp2p** to facilitate interoperability with other chains.
-   **REQ-005 – Hybrid Registry:** Use L1 for long-lived topic discovery but allow off-chain/ephemeral registries for short-lived topics to reduce chain overhead.

## Gemini-normalised summary
- Persona: Lead/CTO of a major DApp (Sunday Labs), representing both DApp developers and core infrastructure builders.
- Top 3 pains:
  - My current communication channels (Twitter, Discord) are insecure, exposing my users to costly phishing attacks and scams from impersonators.
  - The ecosystem is creating multiple, competing messaging standards, forcing me to learn and implement different protocols which increases my workload and fragments the network.
  - On-chain settlement for every message makes low-latency use cases impossible due to L1 finality times, blocking interactive applications like gaming or intents.
- JTBD:
  - Securely announce critical updates to users without fear of platform compromise or impersonation.
  - Enable sub-second, interactive communication for applications like gaming or intent matching.
  - Simplify infrastructure by supporting multiple messaging protocols (e.g., Cardano native, libp2p) within a single stack.
- Suggested requirements:
  - REQ-001 – Unified Messaging Standard
  - REQ-002 – Capacity-Based Payment Model
  - REQ-003 – Language-Agnostic APIs
  - REQ-004 – Dual-Stack Protocol Support
  - REQ-005 – Hybrid On/Off-Chain Registry

SOURCE_ANALYSIS = {
  "used_pm_notes": 70,
  "used_transcript": 30,
  "reasoning": "The PM draft provided a highly accurate and structured summary, which was validated and refined with specific details from the transcript."
}
