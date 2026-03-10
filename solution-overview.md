# Solution Overview — Cartagena POAP Route

## Summary

The Cartagena POAP Route is a gamified, verifiable city participation program that uses blockchain-based Proof of Attendance Protocol (POAP) tokens to track and reward tourist and resident engagement with local landmarks and small vendors.

Participants collect one POAP at each of five designated checkpoints across Cartagena by scanning a QR code after completing a real-world action — a visit, a purchase, or a photo check-in at a vendor or heritage site. When a single wallet holds all five POAPs, the participant qualifies for a completion POAP and may redeem a limited-edition physical reward (e.g., a collectible magnet or local artisan item) at a designated redemption point such as the city's tourism office or a partner location.

---

## The Problem in Detail

Tourism programs in mid-sized cities like Cartagena rely on analog or centralized digital systems to incentivize route completion and track vendor participation. These systems share common failure modes:

**Fraud and Duplication**
Paper stamps and printable QR codes can be duplicated without detection. A participant — or even a vendor — can claim rewards without completing the required steps. A single administrator can silently modify records.

**Lack of Verifiability**
Vendors, sponsors, and municipal partners have no independent way to verify how many participants visited a given stop, making it impossible to audit reward programs or allocate sponsorship value fairly.

**Siloed Data**
Participation history is locked in a single operator's database. If the operator changes, all historical participation data is lost or inaccessible. Participants have no portable proof of their engagement.

**Weak Incentive-to-Merchant Link**
Without a verified connection between tourist activity and specific vendor stops, programs cannot demonstrate that incentives are actually routing spend to small local merchants.

---

## The Solution in Detail

### Five-Checkpoint Route

Cartagena Onchain, in coordination with local partners (in discussions), will design a route of five checkpoints combining:
- **Heritage and cultural landmarks** (e.g., city walls, plazas)
- **Small local vendor locations** (e.g., artisans, food vendors, craft shops)

The mix ensures tourist spend reaches local commerce, not only institutional attractions.

### POAP Issuance via HOOP/Pulse

Each checkpoint issues a POAP via a QR code, managed through the Pulse platform operated by HOOP. The QR contains a time-limited, rotating claim link. A participant scans the QR with a wallet-enabled mobile browser or a simple wallet app and receives their POAP directly to their wallet address.

**No personal data is required to claim a POAP.** A wallet address is the only identifier. Cartagena Onchain does not collect names, phone numbers, or email addresses as part of the core route.

### Completion Verification and Redemption

A participant who holds all five route POAPs in a single wallet can present their wallet at the official redemption point. Staff verify on-chain using the Pulse verification interface (or a public blockchain explorer). Upon verification, the participant receives:

1. A **completion POAP** — a permanent, on-chain record of full route completion
2. A **physical reward** — a limited-edition item produced locally

### What Makes This Different

| Feature | Traditional Program | Cartagena POAP Route |
|---------|--------------------|-----------------------|
| Participation proof | Paper stamp / database entry | On-chain, wallet-held POAP |
| Fraud resistance | Low (copyable, editable) | High (per-wallet, time-windowed, tamper-resistant) |
| Auditability | Admin-only | Public blockchain explorer |
| Data portability | None | Participant owns their proof |
| Multi-stakeholder trust | Requires central admin | Neutral third-party (blockchain) |

---

## Scope of the Pilot

The 12-month pilot will:
- Deploy 5 POAP checkpoints across Cartagena
- Onboard participating vendors with operational guides and training
- Run at least one public activation event (e.g., a POAPthon walk)
- Collect aggregate participation data for reporting
- Produce a final public impact report for UNICEF and the community

Detailed milestones are in [`pilot-plan-12-months.md`](./pilot-plan-12-months.md).

---

## Technology Stack (Summary)

- **Protocol:** POAP (ERC-721 non-transferable token standard)
- **Infrastructure:** HOOP / Pulse (production smart-contract layer, QR generation, verification)
- **Network:** Primary EVM-compatible chain (e.g., Gnosis or Polygon); multi-chain capable via Pulse
- **Wallet Access:** Any EVM-compatible wallet; wallet onboarding support planned in collaboration with prospective partners

> Cartagena Onchain does **not** deploy custom smart contracts. All smart-contract infrastructure is provided and managed by HOOP/Pulse.
