# Architecture — Cartagena POAP Route

## System Components

| Component | Provider | Role |
|-----------|----------|------|
| POAP Smart Contracts | HOOP / Pulse | Token issuance, on-chain storage, verification |
| QR Code Generation & Management | HOOP / Pulse (Pulse platform) | Rotating claim links, time windows, per-wallet limits |
| Blockchain Network | EVM-compatible (primary: Gnosis or Polygon) | Public ledger for POAP records |
| Wallet (Participant) | Any EVM wallet (e.g., MetaMask, Coinbase Wallet) | Holds participant's POAPs |
| Verification Interface | Pulse dashboard / public block explorer | Real-time check at redemption point |
| Operations & Vendor Management | Cartagena Onchain | QR distribution, vendor training, redemption logistics |
| Reporting & Evaluation | Cartagena Onchain | Aggregate on-chain data export, impact report |

---

## System Flow Diagram (ASCII)

```
PARTICIPANT JOURNEY
═══════════════════════════════════════════════════════════════════════

  [Participant arrives at Checkpoint]
             │
             ▼
  [Scans QR code at location]
  (QR contains time-limited claim link, managed by Pulse/HOOP)
             │
             ▼
  [Opens link in mobile browser or wallet app]
             │
             ▼
  [Connects EVM wallet]
  (MetaMask, Coinbase Wallet, or equivalent)
             │
             ▼
  [Claims POAP] ──────────────────────────────────────────────────────┐
             │                                                         │
             ▼                                                         ▼
  [POAP minted to wallet]                              [HOOP/Pulse smart contract]
  (ERC-721 non-transferable token)                     (production contract on EVM chain)
  (stored in participant's wallet)                     (immutable record on-chain)
             │
             ▼
  [Repeat at each of 5 checkpoints]
             │
             ▼
  [Wallet holds all 5 route POAPs?]
        /         \
      YES          NO
       │            │
       ▼            ▼
  [Visit          [Continue
  redemption       route]
  point]
       │
       ▼
  [Staff verifies on Pulse dashboard
   or public block explorer]
  (confirms wallet holds all 5 POAPs)
       │
       ▼
  [Completion POAP issued]
  + [Physical reward distributed]
  (logged in redemption ledger)


VENDOR / CHECKPOINT SETUP FLOW
═══════════════════════════════════════════════════════════════════════

  [Cartagena Onchain]
        │
        ├── Designs route (5 checkpoints)
        ├── Coordinates with HOOP/Pulse to create POAP events
        ├── Receives QR codes / claim links from Pulse
        ├── Delivers printed QR + instructions to vendor/location
        └── Trains vendor on custody rules and incident response
                    │
                    ▼
            [Vendor / Location]
            Displays QR at checkpoint
            Follows custody and rotation schedule
            Reports incidents to Cartagena Onchain


DATA & REPORTING FLOW
═══════════════════════════════════════════════════════════════════════

  [On-chain POAP records]
        │
        ▼
  [Cartagena Onchain exports aggregate data]
  (wallet count, completion count, redemption count)
  (NO names, NO email, NO phone — wallet address only)
        │
        ▼
  [Quarterly progress reports → UNICEF]
        │
        ▼
  [Final public impact report published to this repository]
```

---

## Network Selection

The pilot will deploy on a **single primary EVM-compatible chain**, selected in coordination with HOOP/Pulse and prospective ecosystem partners. Candidate networks supported by Pulse include:

- **Gnosis** — low fees, established POAP ecosystem
- **Polygon** — widely used, strong wallet support
- **Base** — prospective partner (in discussions) with strong consumer wallet onboarding
- Arbitrum, Celo, Mantle, Linea, ApeChain, Chiliz, Unichain (multi-chain capable via Pulse)

Final network selection will be confirmed before pilot launch.

---

## Smart Contracts

> **Important:** Cartagena Onchain does **not** deploy, own, or maintain smart contracts for this pilot.

All POAP issuance is handled through HOOP/Pulse's production smart-contract infrastructure. These contracts are:
- Deployed and maintained by HOOP/Pulse
- Subject to HOOP/Pulse's security and audit processes
- Available for evaluator review by contacting HOOP/Pulse directly

For audit documentation, evaluators should contact the HOOP/Pulse team. See [`roles-tech-partners.md`](./roles-tech-partners.md).

---

## Security Architecture Summary

See [`anti-fraud-threat-model.md`](./anti-fraud-threat-model.md) for the full threat model. Key controls at the architecture level:

- **Rotating QR codes** — claim links expire; Pulse manages rotation
- **Per-wallet claim limits** — one POAP per wallet per event
- **Time-windowed claims** — claims only valid during checkpoint operating hours
- **On-chain redemption verification** — physical reward requires live on-chain proof
- **No PII stored in system** — wallet address is the only identifier
