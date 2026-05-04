# CLP Tokenomics

## Overview

CLP (Calipso) is the cultural infrastructure token of the Calipso Universe ecosystem. This document defines the final and immutable token structure: total supply, allocation, vesting schedules, monthly unlock rates, and the resulting year by year distribution profile.

Detailed security architecture is in the Security Model document. Custody and wallet topology are in the Vesting Architecture document.

---

## Token Identity

- **Token Name:** Calipso
- **Ticker:** CLP
- **Network:** Solana (SPL Token Standard)
- **Decimals:** 9
- **Total Supply:** 100,000,000 CLP (one hundred million)
- **Supply Type:** Fixed. Permanently capped.
- **Mint Authority:** Permanently revoked
- **Freeze Authority:** Permanently revoked
- **Update Authority:** Active for metadata updates only
- **Initial Circulating Supply (TGE):** 11,000,000 CLP (11%)
- **Locked at Launch:** 89,000,000 CLP (89%)
- **Primary Swap Venue:** Jupiter (Solana DEX aggregator). Live.

### Official Contract Address

CLPoEzjVkT73SPnM113U9qTJMzMdevujhGisPqbDEw8D

This is the only authentic CLP token contract.

---

## Design Priorities

- **Long-term alignment:** Vesting structures synchronize founder and treasury incentives with multi-year ecosystem health.
- **Supply discipline:** Total supply is permanently capped. No discretionary minting exists.
- **Transparency:** All allocations, lock periods, and emission rates are publicly defined and on-chain verifiable.
- **Ecosystem stability:** Circulation grows predictably. No surprise unlocks. No mechanism for sudden supply expansion.
- **Zero inflation risk:** Mint authority is permanently revoked. The token cannot be inflated under any condition.

---

## Allocation Structure

Top-level breakdown:

- **Founder Reserve:** 30,000,000 CLP (30%)
- **Company Reserve:** 60,000,000 CLP (60%)
- **Network Circulation:** 10,000,000 CLP (10%)
- **Total:** 100,000,000 CLP (100%)

Sub-allocation breakdown:

- **Founder Operational** (under Founder Reserve): 5,000,000 CLP (5%)
- **Founder Long Term Asset Pool** (under Founder Reserve): 25,000,000 CLP (25%)
- **Treasury and Ecosystem** (under Company Reserve): 35,000,000 CLP (35%)
- **Marketing and Partnerships** (under Company Reserve): 25,000,000 CLP (25%)
- **Network Circulation** (standalone): 10,000,000 CLP (10%)

No allocation grants disproportionate control over creative direction. Narrative authority remains structurally independent from token distribution.

---

## Circulating Supply at Launch

- **Network Circulation:** 10,000,000 CLP (full TGE deployment via liquidity gateways)
- **Founder Operational TGE Unlock:** 1,000,000 CLP
- **Total Circulating at Launch:** 11,000,000 CLP (11%)
- **Total Locked at Launch:** 89,000,000 CLP (89%)

---

## Vesting and Unlock Schedule

The 11 / 89 circulation model is enforced through structured vesting. All vesting is implemented through Streamflow, an audited Solana-based vesting protocol, under a manual claim model.

### Founder Operational (5%, 5,000,000 CLP)

- **Total Allocation:** 5,000,000 CLP
- **TGE Unlock:** 1,000,000 CLP (1% of total supply, 20% of operational pool)
- **Cliff Period:** 1 month after TGE
- **Vesting Period:** 12 months linear, beginning after the cliff
- **Monthly Vest Rate:** Approximately 333,333 CLP per month
- **Full Vest Date:** End of Month 13

### Founder Long Term Asset Pool (25%, 25,000,000 CLP)

- **Total Allocation:** 25,000,000 CLP
- **Initial Lock Period:** 24 months from TGE (zero access during lock)
- **TGE Unlock:** 0 CLP
- **Vesting Begins:** Month 25
- **Monthly Unlock Rate:** 2% of pool per month (500,000 CLP)
- **Vesting Duration:** 50 months
- **Full Unlock Date:** End of Month 74

### Treasury and Ecosystem (35%, 35,000,000 CLP)

- **Total Allocation:** 35,000,000 CLP
- **Initial Lock Period:** 12 months from TGE
- **TGE Unlock:** 0 CLP
- **Vesting Begins:** Month 13
- **Monthly Unlock Rate:** 2% of pool per month (700,000 CLP)
- **Vesting Duration:** 50 months
- **Full Unlock Date:** End of Month 62

### Marketing and Partnerships (25%, 25,000,000 CLP)

- **Total Allocation:** 25,000,000 CLP
- **Initial Lock Period:** 12 months from TGE
- **TGE Unlock:** 0 CLP
- **Vesting Begins:** Month 13
- **Monthly Unlock Rate:** 2% of pool per month (500,000 CLP)
- **Vesting Duration:** 50 months
- **Full Unlock Date:** End of Month 62

### Network Circulation (10%, 10,000,000 CLP)

- **Total Allocation:** 10,000,000 CLP
- **TGE Unlock:** 100% (10,000,000 CLP)
- **Cliff or Vesting:** None. Released in full at launch.
- **Gateway Status:** Liquidity gateway keys permanently locked or burned at deployment.

---

## Year by Year Circulation Profile

Projected circulating supply at the end of each period, derived directly from the vesting mechanics above:

- **TGE (Launch):** 11,000,000 CLP (11%) — Network 10M plus Founder TGE 1M
- **End of Year 1 (Month 12):** approximately 14,667,000 CLP (14.7%) — Only Founder Operational vesting
- **End of Year 2 (Month 24):** approximately 29,400,000 CLP (29.4%) — Treasury and Marketing begin Month 13
- **End of Year 3 (Month 36):** approximately 49,800,000 CLP (49.8%) — Founder LT begins Month 25
- **End of Year 4 (Month 48):** approximately 70,200,000 CLP (70.2%) — Three streams active at peak rate
- **End of Year 5 (Month 60):** approximately 90,600,000 CLP (90.6%) — Approaching Treasury and Marketing completion
- **Month 62:** approximately 94,000,000 CLP (94%) — Treasury and Marketing fully unlocked
- **End of Year 6 (Month 72):** approximately 99,000,000 CLP (99%) — Only Founder LT continues to vest
- **Month 74 (Final):** 100,000,000 CLP (100%) — Full distribution complete

All vesting rates are fixed percentages of their respective allocations. No discretionary minting exists.

---

## Key Distribution Milestones

- **Month 0 (TGE):** 11% of supply in circulation
- **Month 12 (End of Year 1):** Founder Operational nearly fully vested
- **Month 13:** Treasury and Marketing vesting begins. Peak combined emission window opens.
- **Month 25:** Founder Long Term vesting begins. Maximum monthly emission rate reached.
- **Month 62:** Treasury and Marketing complete. Combined emission drops to 500K per month.
- **Month 74:** Full distribution complete. All 100M CLP in circulation.

---

## Supply Discipline and Inflation Protection

- **Hard Cap Enforcement:** Total supply of 100,000,000 CLP is enforced at the protocol level. Mint authority is permanently revoked.
- **No Discretionary Issuance:** No vesting schedule, no governance proposal, and no future event can introduce additional CLP into existence.
- **Predictable Emission:** Every monthly unlock rate is fixed and publicly verifiable. No variable rates, no discretionary adjustments.
- **Lock Verification:** All vesting locks are enforced on-chain through Streamflow smart contract mechanisms, publicly verifiable through Solana explorers.

Anti-inflation properties:

- No mint function
- No rebase mechanism
- No buyback or burn obligation
- No staking rewards from issuance
- No governance-driven inflation

---

## Legal and IP Position

CLP is a utility token within the Calipso Universe ecosystem. Token ownership does not represent equity, dividends, revenue share, or governance rights over the Calipso Universe intellectual property or Calipso Universe Studios.

The Calipso Universe intellectual property, including all worldbuilding, mythology, characters, narrative architecture, and creative direction, remains the exclusive property of Furkan Tireli.

This document does not constitute investment, financial, legal, or tax advice.

---

## Authorship

The Calipso Universe, including its mythology, characters, story arcs, themes, and creative direction, is the work of **Furkan Tireli**. The prose realization of the six published chronicles was developed in collaboration with AI tools, under the author's creative direction. The intellectual property remains the exclusive creation and ownership of Furkan Tireli.

### Founding Team

- **Furkan Tireli**, Founder, Creator, IP Owner
- **Murat Tavli**, Co-Founder, Chief Architect
- **Cihan Onur**, Co-Founder, Chief Operating Officer

---

© 2026 Calipso Universe Studios. All rights reserved.
