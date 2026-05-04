# CLP Security Architecture

## Overview

The CLP token security model relies on Solana's native protocol guarantees, irreversible authority revocations, hardware-isolated custody, and transparent on-chain verification. No off-chain trust assumptions are required for the token's core integrity.

This document covers the security architecture. Detailed wallet topology and manual claim mechanics are in the Vesting Architecture document. Token economics are in Tokenomics. Infrastructure overview is in Infrastructure Model.

---

## Authority Status

- **Mint Authority:** Permanently Revoked. No new CLP can ever be minted. Total supply is permanently capped at 100,000,000.
- **Freeze Authority:** Permanently Revoked. No wallet holding CLP can be frozen, restricted, or blacklisted by the issuer.
- **Update Authority:** Restricted. Active for non-monetary metadata only. Cannot affect supply, transferability, or balances.
- **Metadata:** Immutable for supply-relevant parameters.
- **Circulation Gateways:** Permanently locked or burned at deployment.

These revocations are publicly verifiable on-chain through Solscan, SolanaFM, and Solana Explorer. They are irreversible.

---

## Token-Level Properties

- **Fixed supply enforcement:** Mint authority revocation is enforced at the protocol level. No actor, including the issuer, can mint additional tokens.
- **Transferability protection:** Freeze authority revocation prevents the issuer from blocking, freezing, or restricting any wallet. CLP is permanently transferable.
- **Smart contract immutability:** The token contract follows Solana SPL token standards. No upgrade mechanism exists that would allow retroactive changes to core parameters.
- **No rebase mechanism:** CLP balances cannot expand or contract algorithmically.
- **No governance-driven inflation:** No on-chain governance can modify the supply cap.

---

## Vesting-Level Properties

- **Smart Contract Enforcement:** All locks are enforced through Streamflow vesting contracts at the Solana protocol level.
- **No Override Mechanism:** Once deployed, vesting schedules cannot be modified, accelerated, or canceled.
- **Manual Claim Required:** Every release requires physical Ledger device confirmation. No automatic transfers exist.
- **Fixed Emission Rates:** All monthly unlock rates are fixed and publicly verifiable.
- **Full Distribution Schedule:** 89% of total supply is locked at launch. Full distribution completes at Month 74 from TGE.

---

## Custody-Level Properties

The Calipso Universe token system is structured around a four-wallet topology that enforces hot-cold separation:

- **Founder Wallet (Hot, Phantom):** Public network interactions, ecosystem transfers
- **Founder Cold Wallet (Ledger):** Long-term founder allocations, vesting beneficiary
- **Company Wallet (Hot, Phantom):** Operational expenses, marketing, provisioning
- **Company Cold Wallet (Ledger):** Company allocations, treasury vault

Properties:

- **Hardware Isolation:** Long-term reserves held on offline Ledger devices, isolated from network attack vectors.
- **Hot-Cold Separation:** Operational wallets never hold long-term reserves. Cold wallets never execute public transactions.
- **Manual Transfer Requirement:** Tokens leaving a cold wallet always move to a corresponding hot wallet first.
- **Address Disclosure:** All four operational wallets are publicly known. Any transfer is immediately visible on-chain.

---

## Public Wallet Addresses

- **Founder Wallet (Hot):** JADR9yCUto9JvRjSujs5BPzo5TFvSWC1DmHRCtQay7uz
- **Founder Cold Wallet (Ledger):** FvWJH3vZmor1GNYEoVr1VNCeHjMCCFkdQjxTjqLYcwG1
- **Company Wallet (Hot):** 2xb9SKp9JeVUhWUXX79qSsNfkLT7PQ7jC39mZFkVfvSW
- **Company Cold Wallet (Ledger):** BcmkX9a4eNQj2QWWCByamgWTfh1SKd269hWu3STfJ1Mc

### Official Contract Address

CLPoEzjVkT73SPnM113U9qTJMzMdevujhGisPqbDEw8D

This is the only authentic CLP token contract.

---

## Transparency-Level Properties

- **On-Chain Verification:** Every parameter, lock, claim, and transfer is publicly queryable on Solana.
- **No Private Reporting:** No reliance on internal dashboards or centralized reporting for verification.
- **Independent Auditability:** Anyone, anywhere, can audit the system without permission or credentials.

Verification Tools:

- Solscan: solscan.io
- SolanaFM: solana.fm
- Solana Explorer: explorer.solana.com
- Streamflow (vesting contract details): streamflow.finance

---

## Disclosed Risks

No security model is absolute. Holders should be aware of risks inherent to all blockchain-based assets:

- **Network-level risks:** Solana network downtime, congestion, or protocol-level changes are outside the issuer's control.
- **Wallet-level risks:** Compromised wallets, phishing attacks, and malicious dApps can result in loss of CLP. These risks rest with the holder.
- **Exchange-level risks:** CLP held on third-party exchanges is subject to those exchanges' security and operational risks.

---

## Custody Recommendations

- **Self-custody by default:** Holders are responsible for the security of their own wallets and private keys.
- **Hardware wallet support:** Hardware wallets (Ledger, Trezor) are recommended for long-term storage of meaningful balances.
- **Never share private keys:** Calipso Universe Studios will never request a holder's private keys, seed phrases, or wallet credentials. Any such request should be treated as fraudulent.

---

## Infrastructure Model

CLP is structured with:

- Reduced authority control
- Long-term circulation commitment
- Transparent tokenomics
- Documented vesting architecture
- Hardware-isolated custody for treasury reserves

The token is designed as infrastructure, not speculation.

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
