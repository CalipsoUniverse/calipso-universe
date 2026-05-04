# CLP Vesting Architecture

## Overview

CLP follows a structured long-term vesting model. All locked allocations are managed through Streamflow, an audited Solana-based vesting protocol, under a manual claim model. No discretionary unlocks exist. No off-chain promises substitute for on-chain enforcement.

This document covers vesting mechanics, claim process, and wallet topology. Token economics are detailed in Tokenomics. Authority status and security properties are in Security Model. Infrastructure overview is in Infrastructure Model.

---

## Vesting Summary

Out of the total CLP supply of 100,000,000 tokens, 89,000,000 tokens (89%) are locked under structured vesting contracts at launch. The remaining 11,000,000 tokens (11%) form the launch-day circulating supply.

- **Vesting Protocol:** Streamflow (audited, Solana-based)
- **Enforcement:** Smart contract level, on-chain
- **Override Capability:** None. Vesting cannot be modified after deployment.
- **Claim Model:** Manual. Each release requires physical Ledger device confirmation.
- **Full Distribution Completion:** Month 74 from TGE

---

## Founder Allocation (30%, 30,000,000 CLP)

The Founder allocation is segmented into two pools to balance operational continuity against long-term alignment.

### Operational Reserve (5%, 5,000,000 CLP)

- **TGE Unlock:** 1,000,000 CLP (released at launch)
- **Remaining Locked:** 4,000,000 CLP
- **Cliff:** 1 month after TGE
- **Vesting:** 12 month linear unlock after cliff
- **Monthly Rate:** approximately 333,333 CLP per month
- **Full Vest Date:** End of Month 13

This allocation supports operational continuity during the first year of ecosystem development.

### Long-Term Reserve (25%, 25,000,000 CLP)

- **Initial Lock:** 24 months from TGE (zero access during lock)
- **TGE Unlock:** 0 CLP
- **Vesting Begins:** Month 25
- **Monthly Rate:** 500,000 CLP per month (2% of pool per month)
- **Vesting Duration:** 50 months
- **Full Unlock Date:** End of Month 74

This is the largest single founder allocation. It is structurally locked for the entire first two years of ecosystem operation, then releases gradually over an additional fifty months. The structure enforces founder commitment to multi-year ecosystem health.

---

## Treasury and Ecosystem (35%, 35,000,000 CLP)

The largest single allocation in the entire token structure. Reserved for sustained development, infrastructure scaling, partner integrations, and operational continuity across digital and physical extensions of Calipso Universe.

- **Initial Lock:** 12 months from TGE
- **TGE Unlock:** 0 CLP
- **Vesting Begins:** Month 13
- **Monthly Rate:** 700,000 CLP per month (2% of pool per month)
- **Vesting Duration:** 50 months
- **Full Unlock Date:** End of Month 62

Treasury allocations support ecosystem expansion, development, strategic integrations, and infrastructure scaling.

---

## Marketing and Partnerships (25%, 25,000,000 CLP)

Reserved for strategic growth: marketing campaigns, partnership activations, community-building initiatives, and adaptation conversations across film, television, animation, and gaming.

- **Initial Lock:** 12 months from TGE
- **TGE Unlock:** 0 CLP
- **Vesting Begins:** Month 13
- **Monthly Rate:** 500,000 CLP per month (2% of pool per month)
- **Vesting Duration:** 50 months
- **Full Unlock Date:** End of Month 62

Marketing allocations support strategic partnerships, brand expansion, and growth campaigns.

---

## Network Circulation (10%, 10,000,000 CLP)

Not held under a vesting contract. Released in full at TGE through liquidity gateways. After deployment, the gateway mechanisms used to seed initial liquidity are permanently locked or burned.

- **TGE Unlock:** 100% (10,000,000 CLP)
- **Cliff or Vesting:** None
- **Gateway Status:** Liquidity gateway keys permanently locked or burned

---

## Manual Claim Mechanism

Vesting releases in the Calipso Universe token system are not automatic. When tokens reach their unlock date, they do not transfer to the cold wallet on their own. Each release requires explicit, manual action by the wallet holder.

### Why Manual

- **No unauthorized access:** A vesting unlock cannot become a token movement without a Ledger device, the correct seed phrase, and physical button presses confirming the transaction.
- **No unexpected movement:** Every claim happens on a deliberate date chosen by the founder or treasury operator. There are no surprise releases.
- **No hidden activity:** Every claim is a transaction visible on-chain at the moment of execution.

### Claim Process

1. Tokens become visible as claimable within the Streamflow vesting contract. Anyone can verify the claimable amount on-chain at any time.
2. The relevant Ledger device is physically connected to a secure computer.
3. The wallet is authenticated on the Streamflow platform using the Ledger device.
4. A claim transaction is explicitly approved on the Ledger device through physical button presses.
5. Tokens are transferred from the vesting contract to the cold wallet address. The transaction is permanently recorded on-chain.

Claims may be executed at any time after a vesting tranche unlocks. The cold wallet balance reflects only what has been actively claimed, not the cumulative entitled amount.

---

## Wallet Architecture

The Calipso Universe token system is structured around four distinct wallets. Each wallet is assigned a single, clearly defined responsibility.

### Cold Wallets (Hardware Isolated)

- **Founder Cold Wallet (Ledger):** Holds long-term founder token allocations. Acts as the beneficiary of the founder vesting contract. Not used for daily transactions or market activity.
- **Company Cold Wallet (Ledger):** Holds company-allocated tokens. Acts as the beneficiary of the company vesting contract. Functions as a protected treasury vault.

Cold wallets remain offline by default and are only connected for the explicit purpose of executing a manual vesting claim authorized by the wallet holder.

### Hot Wallets (Online Operations)

- **Founder Hot Wallet (Phantom):** Used for public network interactions. Network circulation and ecosystem-related transfers.
- **Company Hot Wallet (Phantom):** Used for operational expenses. Marketing, circulation provisioning, and ecosystem-related costs.

Tokens are never circulated, transferred, or deployed directly from cold wallets. All circulation activity requires an explicit transfer from a cold wallet to a hot wallet, ensuring that every token movement is deliberate and traceable on-chain.

---

## Public Wallet Addresses

For full transparency and independent verification:

- **Founder Wallet (Hot):** JADR9yCUto9JvRjSujs5BPzo5TFvSWC1DmHRCtQay7uz
- **Founder Cold Wallet (Ledger):** FvWJH3vZmor1GNYEoVr1VNCeHjMCCFkdQjxTjqLYcwG1
- **Company Wallet (Hot):** 2xb9SKp9JeVUhWUXX79qSsNfkLT7PQ7jC39mZFkVfvSW
- **Company Cold Wallet (Ledger):** BcmkX9a4eNQj2QWWCByamgWTfh1SKd269hWu3STfJ1Mc

### Official Contract Address

CLPoEzjVkT73SPnM113U9qTJMzMdevujhGisPqbDEw8D

This is the only authentic CLP token contract.

---

## Year by Year Distribution

Projected circulating supply at the end of each period, derived from the vesting mechanics above:

- **TGE (Launch):** 11,000,000 CLP (11%)
- **End of Year 1 (Month 12):** approximately 14,667,000 CLP (14.7%)
- **End of Year 2 (Month 24):** approximately 29,400,000 CLP (29.4%)
- **End of Year 3 (Month 36):** approximately 49,800,000 CLP (49.8%)
- **End of Year 4 (Month 48):** approximately 70,200,000 CLP (70.2%)
- **End of Year 5 (Month 60):** approximately 90,600,000 CLP (90.6%)
- **Month 62:** approximately 94,000,000 CLP (94%) — Treasury and Marketing fully unlocked
- **End of Year 6 (Month 72):** approximately 99,000,000 CLP (99%)
- **Month 74 (Final):** 100,000,000 CLP (100%) — Full distribution complete

---

## Verification

All vesting locks are enforced on-chain. Anyone can independently verify:

- Vesting contract status (locked, claimable, claimed amounts)
- Manual claim transactions (timestamped, recorded permanently)
- Token movements between wallets (cold to hot, hot to ecosystem)
- Real-time balance of any wallet

Verification tools:

- Solscan: solscan.io
- SolanaFM: solana.fm
- Solana Explorer: explorer.solana.com
- Streamflow (vesting contract details): streamflow.finance

No private dashboards. No centralized reporting. No reliance on Calipso Universe Studios for verification.

---

## Design Principle

All vesting is structured for long-term ecosystem growth and stability. The token follows the same logic that governs the universe itself: paced expansion, restraint over speed, integrity over reach. The universe moves first. The infrastructure follows.

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

This document does not constitute investment, financial, legal, or tax advice.

---

© 2026 Calipso Universe Studios. All rights reserved.
