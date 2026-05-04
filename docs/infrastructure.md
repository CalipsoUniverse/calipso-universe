# CLP Infrastructure Architecture

## Overview

CLP (Calipso) is deployed as the cultural infrastructure layer of the Calipso Universe ecosystem.

The launch model, circulation structure, and authority configuration are intentionally designed for long-term stability, not short-term speculation. Every parameter described here is fixed at the protocol level and publicly verifiable on-chain.

This document covers infrastructure architecture. Detailed token economics are in the [Tokenomics](tokenomics.md) document. Custody, wallet topology, and security architecture are in the [Security Model](security.md) and [Vesting Architecture](vesting.md) documents.

---

## Token Identity

- **Token Name:** Calipso
- **Ticker:** CLP
- **Network:** Solana (SPL Standard)
- **Decimals:** 9
- **Total Supply:** 100,000,000 CLP (permanently fixed)
- **Standard:** Solana Program Library (SPL) Token

### Official Contract Address

```
CLPoEzjVkT73SPnM113U9qTJMzMdevujhGisPqbDEw8D
```

This is the only authentic CLP token contract. Any token presented under the same name but deployed at a different address is unrelated to Calipso Universe Studios.

---

## Launch Model

CLP follows a decentralized network circulation launch model.

- **Circulation Gateway:** Public Network Access
- **Routing Layer:** Decentralized Network Aggregators
- **Primary Swap Venue:** Jupiter (Solana DEX aggregator). Live.
- **Initial Circulation Pool:** 10,000,000 CLP paired with SOL
- **Founder TGE Unlock:** 1,000,000 CLP (direct transfer to Founder Cold Wallet)
- **Total Initial Circulating Supply:** 11,000,000 CLP (11% of total supply)
- **Locked at Launch:** 89,000,000 CLP (89% of total supply)

The token is not pre-sold. There is no private allocation round. There is no insider distribution outside the documented allocation structure.

---

## Circulation Architecture

- Circulation gateways are permanently locked or burned at launch.
- No circulation withdrawal mechanism is retained.
- No hidden circulation channels exist.
- All circulation activity occurs on-chain through public Solana infrastructure.

This ensures structural ecosystem continuity and mitigates disruption risk. Once the gateway mechanisms used to seed initial liquidity are deployed, they cannot be reused for additional discretionary release.

---

## Authority Configuration

CLP authority model is minimized at the protocol level.

| Authority | Status |
|-----------|--------|
| Mint Authority | Revoked (permanent) |
| Freeze Authority | Revoked (permanent) |
| Update Authority | Restricted to non-monetary metadata only |
| Metadata | Immutable for supply, transferability, and balances |

**No future token supply expansion is possible.** No wallet can be frozen by the issuer. No retroactive change can affect supply, transferability, or any holder balance.

These revocations are publicly verifiable through Solscan, SolanaFM, and Solana Explorer.

---

## Allocation Structure

| Allocation | Amount | Percent |
|------------|--------|---------|
| Founder Reserve | 30,000,000 CLP | 30% |
| Treasury and Ecosystem | 35,000,000 CLP | 35% |
| Marketing and Partnerships | 25,000,000 CLP | 25% |
| Network Circulation | 10,000,000 CLP | 10% |
| **Total** | **100,000,000 CLP** | **100%** |

No allocation grants disproportionate control over creative direction. Narrative authority remains structurally independent from token distribution.

---

## Founder Reserve Structure

Founder allocations are segmented, time-locked, and structured via documented vesting architecture.

### Operational Tier (5%, 5,000,000 CLP)

- **TGE Unlock:** 1,000,000 CLP
- **Cliff:** 1 month
- **Vesting:** 12-month linear after cliff at approximately 333,333 CLP per month
- **Full Vest:** Month 13

### Long-Term Asset Pool (25%, 25,000,000 CLP)

- **Initial Lock:** 24 months full lock from TGE
- **Vesting Begins:** Month 25
- **Monthly Rate:** 2% of pool per month (500,000 CLP)
- **Duration:** 50 months
- **Full Unlock:** Month 74

Operational reserve is separated from long-term strategic reserve. Cold storage principles are applied to long-term holdings via Ledger hardware wallets.

---

## Treasury Model

Treasury is structured for ecosystem growth, development funding, brand expansion, and infrastructure maintenance.

### Treasury and Ecosystem (35%, 35,000,000 CLP)

- **Initial Lock:** 12 months full lock from TGE
- **Vesting Begins:** Month 13
- **Monthly Rate:** 2% of pool per month (700,000 CLP)
- **Duration:** 50 months
- **Full Unlock:** Month 62

### Marketing and Partnerships (25%, 25,000,000 CLP)

- **Initial Lock:** 12 months full lock from TGE
- **Vesting Begins:** Month 13
- **Monthly Rate:** 2% of pool per month (500,000 CLP)
- **Duration:** 50 months
- **Full Unlock:** Month 62

Treasury unlocks follow the documented vesting schedule. All vesting is enforced through Streamflow, an audited Solana-based vesting protocol, under a manual claim model.

---

## Network and Ecosystem Access

CLP is accessible via:

- Decentralized network routing through Jupiter
- Direct circulation pool interaction
- On-chain ecosystem transfers
- Standard Solana wallet compatibility (Phantom, Solflare, Backpack, Ledger)

No centralized platform dependency exists for baseline network access. CLP holders interact with the token through the same Solana infrastructure used by any standard SPL token.

---

## Vesting Enforcement

All locked allocations are managed through Streamflow vesting contracts:

- **Protocol:** Streamflow (audited, Solana-based)
- **Enforcement:** Smart contract level, on-chain
- **Claim Model:** Manual. Each release requires physical Ledger device confirmation.
- **Override Capability:** None. Vesting cannot be modified after deployment.
- **Full Distribution Completion:** Month 74 from TGE

No off-chain promises substitute for on-chain enforcement. Every claim transaction is publicly recorded and timestamped on the Solana blockchain.

---

## Public Wallet Architecture

The Calipso Universe token system is structured around four distinct wallets, each with a single defined responsibility.

| Wallet | Type | Device | Address |
|--------|------|--------|---------|
| Founder Wallet (Hot) | Hot | Phantom | `JADR9yCUto9JvRjSujs5BPzo5TFvSWC1DmHRCtQay7uz` |
| Founder Cold Wallet | Cold | Ledger | `FvWJH3vZmor1GNYEoVr1VNCeHjMCCFkdQjxTjqLYcwG1` |
| Company Wallet (Hot) | Hot | Phantom | `2xb9SKp9JeVUhWUXX79qSsNfkLT7PQ7jC39mZFkVfvSW` |
| Company Cold Wallet | Cold | Ledger | `BcmkX9a4eNQj2QWWCByamgWTfh1SKd269hWu3STfJ1Mc` |

Cold wallets remain offline by default. Hot wallets handle public network interactions. Tokens never circulate directly from cold wallets.

---

## Design Philosophy

The infrastructure prioritizes:

- **Transparency:** Every parameter, lock, claim, and transfer is publicly verifiable on-chain.
- **Authority minimization:** Mint and freeze authorities are permanently revoked. Update authority is limited to metadata only.
- **Circulation permanence:** Gateway mechanisms are locked at deployment. No discretionary supply expansion is possible.
- **Long-term narrative continuity:** The infrastructure follows the universe's pace. The universe moves first. The infrastructure follows.

CLP is designed as infrastructure, not a hype-driven asset.

---

## Transparency Commitment

The following references are publicly documented and on-chain verifiable:

- **Official Contract Address:** `CLPoEzjVkT73SPnM113U9qTJMzMdevujhGisPqbDEw8D`
- **Public Wallet Registry:** Four wallet addresses listed above
- **Vesting Architecture:** Streamflow contracts viewable at streamflow.finance
- **Security Configuration:** Authority states queryable via Solscan, SolanaFM, Solana Explorer

No private dashboards. No centralized reporting. Anyone, anywhere, can audit the system without permission.

---

## Authorship

The Calipso Universe, including its mythology, characters, story arcs, themes, and creative direction, is the work of **Furkan Tireli**. The prose realization of the six published chronicles was developed in collaboration with AI tools, under the author's creative direction. The intellectual property remains the exclusive creation and ownership of Furkan Tireli.

### Founding Team

- **Furkan Tireli**, Founder, Creator, IP Owner
- **Murat Tavli**, Co-Founder, Chief Architect
- **Cihan Onur**, Co-Founder, Chief Operating Officer

---

## Legal Position

CLP is a utility token within the Calipso Universe ecosystem. Token ownership does not represent equity, dividends, revenue share, or governance rights over the Calipso Universe intellectual property or Calipso Universe Studios.

This document does not constitute investment, financial, legal, or tax advice. It is provided for informational purposes only.

---

© 2026 Calipso Universe Studios. All rights reserved.

Calipso Universe infrastructure is built for durability.
