# Roles & Technology Partners

## Overview

This document clarifies the division of responsibilities between Cartagena Onchain, HOOP/Pulse, and the POAP Protocol. Transparency about ownership, contract deployment, and accountability is essential for grant evaluators.

---

## Cartagena Onchain — Pilot Lead & Implementing Organization

**Role:** Design, operations, community activation, vendor onboarding, reporting

**Responsibilities:**
- Route design and checkpoint selection (in coordination with local stakeholders)
- Vendor recruitment, onboarding, and training
- QR code distribution and custody logistics at each checkpoint
- Community activation and public launch events (e.g., POAPthon)
- Participant support and communications
- Aggregate data collection and impact reporting to UNICEF
- Redemption point coordination (in discussions with municipal partners)
- Grant compliance and milestone reporting

**What Cartagena Onchain does NOT do:**
- Deploy, own, or operate smart contracts
- Issue POAPs directly (this is handled by HOOP/Pulse infrastructure)
- Manage contract security or audits (this is HOOP/Pulse's responsibility)

---

## HOOP / Pulse — Technology Partner (Confirmed)

**Role:** Smart-contract infrastructure, POAP issuance, verification platform

**About HOOP/Pulse:**
HOOP provides the Pulse platform, a production-grade infrastructure layer for POAP issuance and management. Pulse supports multi-chain deployments across EVM-compatible networks including Gnosis, Polygon, Base, Arbitrum, Celo, Mantle, Linea, ApeChain, Chiliz, and Unichain.

**Responsibilities:**
- Deploying and maintaining smart contracts for POAP events
- Generating and managing QR claim links with time-window and per-wallet controls
- Providing verification tools for redemption staff
- Managing contract security and audit documentation
- Supporting Cartagena Onchain's operational team with technical guidance

**Smart Contract Ownership:**
> HOOP/Pulse **owns and deploys** all smart contracts used in this pilot. Cartagena Onchain is a **user/operator** of the Pulse platform, not a contract deployer.

**Audit References:**
Evaluators requiring smart-contract audit documentation should contact HOOP/Pulse directly. Cartagena Onchain will facilitate introductions to the HOOP/Pulse technical team for grant due diligence purposes.

---

## POAP Protocol

**Role:** Token standard and protocol

**About POAP:**
POAP (Proof of Attendance Protocol) defines the standard for non-transferable ERC-721 tokens used to record attendance and participation events on EVM-compatible blockchains. The POAP standard is widely adopted in the Ethereum ecosystem.

**Responsibilities in this pilot:**
- Defines the token standard and metadata format used for all checkpoint and completion POAPs
- Provides the underlying protocol infrastructure that Pulse builds upon

---

## Prospective & In-Discussion Partners

The following organizations have been identified as potential ecosystem partners. **None of these partnerships are confirmed.** They are in early-stage discussions only.

| Organization | Potential Role | Status |
|-------------|---------------|--------|
| Uniswap | Ecosystem education support, potential ecosystem grant coordination | In discussions |
| Base (Coinbase) | Consumer wallet onboarding, L2 ecosystem support | In discussions |
| Tether / USDT | Stablecoin payment rails for merchant settlements | In discussions |
| Mayor's Office of Cartagena | Institutional endorsement, checkpoint placement, redemption venue | In discussions |
| Corpoturismo | Tourism authority coordination, cultural site access | In discussions |
| Local vendor/artisan associations | Checkpoint hosting, community engagement | In discussions |

> **Note to evaluators:** No claims are made regarding confirmed commitments from any of the above organizations. Letters of intent or MOUs will be pursued during the pilot design phase if funding is awarded.

---

## Summary Accountability Table

| Function | Accountable Party |
|----------|------------------|
| Pilot design and implementation | Cartagena Onchain |
| Vendor and community relations | Cartagena Onchain |
| Impact reporting to UNICEF | Cartagena Onchain |
| Smart-contract deployment | HOOP / Pulse |
| POAP issuance and QR management | HOOP / Pulse |
| Contract security and audits | HOOP / Pulse |
| Token standard | POAP Protocol |
| Blockchain network (ledger) | Selected EVM chain (public) |
