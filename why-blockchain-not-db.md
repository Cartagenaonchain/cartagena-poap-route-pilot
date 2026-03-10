# Why Blockchain and Not a Database

## The Core Question

A centralized database can record participation events. So why use a blockchain? This document answers that question specifically for the Cartagena POAP Route context.

---

## The Multi-Stakeholder Problem

The Cartagena POAP Route involves multiple independent parties with no pre-existing trust relationship and no shared authority:

- **Vendors** at individual stops (each an independent small business)
- **The municipal tourism office** (a public-sector entity)
- **Sponsors** (private sector, in discussions)
- **Cartagena Onchain** (the implementing organization, a for-profit entity)
- **Participants** (tourists and residents)

If participation records live in a database owned and operated by any one of these parties, the others must trust that operator not to modify, inflate, or delete records. That trust is not warranted — and cannot be independently verified.

**A blockchain is a neutral third party.** No participant in the program, including Cartagena Onchain, can alter a POAP record after it is issued.

---

## Why a Database Falls Short Here

### 1. Tamper Resistance
A traditional database administrator can insert, update, or delete records. Even with audit logs, those logs can also be altered. On a public blockchain, once a token is issued to a wallet, no party — including the token issuer — can remove it or move it without the wallet owner's private key. The historical record is immutable.

### 2. Independent Auditability
Blockchain transactions are publicly readable. A vendor, sponsor, auditor, journalist, or UNICEF evaluator can independently verify how many wallets claimed a given POAP without requesting data from Cartagena Onchain. This eliminates the "trust the implementer" requirement.

### 3. Fraud Resistance at the Reward Redemption Step
The reward redemption step requires on-chain proof. Staff check that a wallet holds all five POAPs. Because POAPs are non-transferable and tied to individual wallets, a participant cannot simply share a screenshot or paper certificate. The verification is done live against the blockchain state.

### 4. Participant Data Portability
A POAP is held in the participant's own wallet. They own their proof of participation. If Cartagena Onchain ceases to operate, or the tourism office changes programs, participant records persist independently. This is not possible with a centralized database.

### 5. Multi-Issuer Coordination Without a Central Database
In future iterations of the route, different organizations (a hotel, a museum, a vendor association) could each issue their own checkpoint POAP using the same protocol. A blockchain provides a common coordination layer without requiring every stakeholder to share database access or trust a single admin.

---

## What Blockchain Does NOT Solve

We are transparent about blockchain's limitations in this context:

| Limitation | Our Mitigation |
|------------|---------------|
| A fake QR scan is still possible (user photographs code from home) | Rotating / time-windowed QR codes; see [`anti-fraud-threat-model.md`](./anti-fraud-threat-model.md) |
| Sybil wallets (one person, many wallets) | Per-wallet limits; physical redemption requires in-person presence |
| On-chain data is public (wallet address visible) | Data minimization; no PII linked to wallet by default; see [`privacy-data-minimization.md`](./privacy-data-minimization.md) |
| Smart-contract bugs | Contracts provided and audited by HOOP/Pulse; we do not deploy custom contracts |

---

## Summary

Blockchain is the right tool here **not because it is novel**, but because it solves a specific coordination problem: enabling multiple independent stakeholders — none of whom fully trust each other — to share a tamper-resistant, auditable participation record without requiring a trusted central administrator. A traditional database controlled by any one party cannot provide this.
