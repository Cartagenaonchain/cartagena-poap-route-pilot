# Anti-Fraud & Threat Model

## Purpose

This document identifies the primary fraud and abuse risks for the Cartagena POAP Route pilot, the controls in place to mitigate each risk, and the incident response process if controls fail.

---

## Threat Categories & Controls

### 1. QR Code Sharing / Remote Claims

**Threat:** A participant photographs or screenshots a QR code and shares it online or with friends who are not physically present at the checkpoint.

**Impact:** Fraudulent POAP claims; route integrity compromised; rewards redeemed without completing real-world actions.

**Controls:**
- **Rotating QR codes:** Pulse generates time-limited claim links that expire after a defined window (e.g., every 2–4 hours or daily). A shared static QR becomes invalid quickly.
- **Operating-hours time windows:** Claims are only valid during checkpoint operating hours. Off-hours claims are blocked.
- **Staff awareness:** Vendors and location staff are trained to display QR codes only during operating hours and to protect codes from photography when possible.

---

### 2. Duplicate Claims / Multiple Claims Per Wallet

**Threat:** A participant attempts to claim the same POAP more than once from the same wallet (e.g., re-scanning a QR).

**Impact:** Inflated claim counts; wasted POAP allocations.

**Controls:**
- **Per-wallet claim limits:** Pulse enforces one POAP per wallet per event at the smart-contract level. A second claim attempt from the same wallet is rejected automatically.

---

### 3. Sybil Wallets (One Person, Many Wallets)

**Threat:** A single person creates multiple wallet addresses and claims POAPs to each, then redeems multiple physical rewards.

**Impact:** Physical reward inventory depleted; data inflated.

**Controls:**
- **Physical redemption requirement:** Reward redemption requires in-person presence at the redemption point. A single person can only present once.
- **Staff verification:** Redemption staff can note if the same individual returns multiple times and apply a per-person limit.
- **Reward inventory control:** Physical reward stock is limited and tracked in a redemption ledger. Stock exhaustion naturally caps fraud.
- **Completion POAPs:** The completion POAP is issued after verification; staff can limit completion POAPs to one per in-person presentation.

---

### 4. Vendor Abuse / Insider Claims

**Threat:** A vendor or staff member at a checkpoint claims POAPs to their own wallet(s) without completing the route, or allows associates to claim without visiting.

**Impact:** Inflated vendor participation data; fraudulent reward redemptions.

**Controls:**
- **Vendor agreement:** Vendors sign an onboarding agreement acknowledging prohibited behaviors and consequences (removal from program).
- **QR custody rules:** QR codes are for public display during operating hours only. Vendors are prohibited from claiming POAPs from their own checkpoint.
- **Cross-checkpoint pattern monitoring:** If a wallet claims all POAPs in an implausibly short time window (e.g., all 5 in 10 minutes across geographically distributed locations), it is flagged for manual review.
- **Separation of roles:** Vendors are not involved in the redemption verification process.

---

### 5. Fake Redemptions / Counterfeit Proof

**Threat:** A participant presents a screenshot of POAPs or a manipulated wallet interface rather than live on-chain proof.

**Impact:** Physical reward distributed without valid on-chain claims.

**Controls:**
- **Live verification only:** Redemption staff verify POAP holdings using the Pulse verification interface or a public block explorer in real time. Screenshots are not accepted.
- **Staff training:** Redemption staff receive a step-by-step verification guide and practice before the pilot launch.

---

### 6. QR Code Leakage or Compromise

**Threat:** A QR code is posted publicly online, photographed by a bad actor, or obtained through a vendor's negligence before rotation.

**Impact:** Mass remote claims; route integrity compromised for that window.

**Controls:**
- **Rapid rotation:** Because Pulse supports short rotation windows, exposure windows are limited.
- **Incident response:** See below. A compromised code can be invalidated and replaced quickly.

---

### 7. Smart Contract Vulnerabilities

**Threat:** A bug or exploit in the POAP smart contracts could allow unauthorized minting or other manipulation.

**Impact:** Data integrity failure; unauthorized reward eligibility.

**Controls:**
- **Managed by HOOP/Pulse:** Cartagena Onchain does not deploy custom contracts. HOOP/Pulse's production contracts are subject to their security and audit processes.
- **Audit documentation:** Available from HOOP/Pulse on request.

---

## Incident Response Process

### If a QR Code is Compromised

1. **Detect:** Unusual spike in claims at a checkpoint (Pulse dashboard alert or manual monitoring).
2. **Contain:** Cartagena Onchain contacts HOOP/Pulse to invalidate the compromised claim link immediately.
3. **Replace:** New QR code/link generated and delivered to the checkpoint.
4. **Review:** Assess anomalous wallet addresses; flag for exclusion from reward eligibility if abuse is confirmed.
5. **Document:** Log the incident, estimated exposure window, and wallets flagged.
6. **Report:** Include in quarterly report to UNICEF if material.

### If Vendor Abuse is Detected

1. **Detect:** Cross-checkpoint time analysis or community report.
2. **Contain:** Suspend vendor's participation pending review.
3. **Investigate:** Review on-chain data for wallet patterns associated with the vendor.
4. **Respond:** Remove vendor from program if abuse confirmed; adjust data in aggregate report with a note.
5. **Document and Report:** Log incident, include in reporting.

### If a Sybil Campaign is Detected

1. **Detect:** Unusual spike in completion redemptions; same individual presenting multiple times.
2. **Contain:** Pause redemption at discretion of staff; apply per-person limits.
3. **Investigate:** Cross-reference redemption ledger with in-person log.
4. **Respond:** Exclude confirmed abusive wallets from completion count in reporting; note in methodology.

---

## Summary Controls Table

| Threat | Primary Control | Secondary Control |
|--------|----------------|------------------|
| QR sharing | Rotating codes (Pulse) | Time windows |
| Duplicate claims | Per-wallet limit (smart contract) | — |
| Sybil wallets | Physical redemption requirement | Per-person staff limit |
| Vendor abuse | Vendor agreement | Pattern monitoring |
| Fake redemption | Live on-chain verification | Staff training |
| Code leakage | Rapid rotation | Incident response |
| Contract exploit | HOOP/Pulse audited contracts | — |
