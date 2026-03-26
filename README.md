# 🛡️ JavaSweep & King Solidity Protocol
### *The Final Gatekeeper: A Dual-Layer Emergency Asset Recovery Framework*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Category: Web3 Security](https://img.shields.io/badge/Category-Web3%20Security-blue)](https://metamask.io/snaps/)
[![Tech: MetaMask Snaps](https://img.shields.io/badge/Tech-MetaMask%20Snaps-orange)](https://metamask.io/snaps/)
[![Tech: Account Abstraction](https://img.ethereum.org/EIPS/eip-4337)](https://eips.ethereum.org/EIPS/eip-4337)

---

## 📌 Vision & Narrative
In the current Web3 landscape, a compromised seed phrase often results in immediate total loss. Recent discussions within the **Consensys** community highlight a critical need: users require a rapid, automated "Panic Button" to rescue holdings before drainer bots can react.

**JavaSweep & King Solidity** is a specialized rescue protocol designed to bridge the gap between human reaction time and blockchain finality. By combining the off-chain execution power of **MetaMask Snaps** with the on-chain resilience of **Account Abstraction (AA)**, we create a secure corridor for asset migration during a security crisis.

---

## 🏗️ Architecture Blueprint

```mermaid
graph TD
    %% Actors & Environments
    subgraph Compromised_Env [User Environment - Compromised]
        A[User MetaMask EOA - Seed Leaked]
        B[Hacker Wallet]
    end

    subgraph Gatekeeper [MetaMask Snap - The Gatekeeper]
        C[JavaSweep Protocol Logic]
    end

    subgraph Secure_Dest [Secure Destination]
        D[King Solidity Vault - AA Contract]
    end

    %% Event Flow
    A -- "1. Phishing / Seed Leak" --> B
    A -- "2. User Activates Snap" --> C

    %% Rescue Flow
    C -- "3. Scan Balance & NFTs" --> A
    C -- "4. Generate Rescue Tx" --> A
    A -- "5. Signs & Sends Assets" --> C
    C -- "6. Transfers Assets" --> D

    %% Security Flow
    D -- "7. New Owner: Multi-Sig/Hardware" --> D
    D -- "8. Rules: Spend Limits / Time Locks" --> D

    %% Hacker Prevention
    B -. "9. Fails to Access Vault" .-> D

    %% Styling for Clarity
    style A fill:#ffcccc,stroke:#333
    style C fill:#ffe5cc,stroke:#f96,stroke-width:2px
    style D fill:#ccffcc,stroke:#28a745,stroke-width:2px
