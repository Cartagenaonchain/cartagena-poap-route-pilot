# Privacy & Data Minimization

## Principles

The Cartagena POAP Route is designed with **data minimization as a default**, not an afterthought. We collect only what is necessary to operate the pilot and report impact. We do not collect, store, or process personally identifiable information (PII) as part of the core participation flow.

---

## What We Collect

### Onchain Data (Public, Pseudonymous)

| Data | What It Is | Why Collected |
|------|-----------|---------------|
| Wallet address | A pseudonymous identifier on the blockchain | Required to issue and verify POAPs |
| POAP claim timestamp | When each POAP was claimed | Required for time-window enforcement and anti-fraud monitoring |
| POAP event ID | Which checkpoint POAP was claimed | Required to verify route completion |

**This data is public on the blockchain.** It is pseudonymous — not directly linked to a real-world identity — but wallet addresses can potentially be linked to individuals through other on-chain activity. Participants are notified of this before claiming.

### Operational Data (Held by Cartagena Onchain)

| Data | What It Is | Why Collected | Retention |
|------|-----------|---------------|-----------|
| Redemption log | Timestamp and completion POAP ID presented at redemption | Verifies reward distribution; anti-duplicate redemption | 12 months post-pilot |
| Incident log | Anonymous records of suspected fraud events | Anti-fraud review | 12 months post-pilot |

**No names, email addresses, phone numbers, or government IDs are collected in the redemption log.** The log records POAP IDs and timestamps only.

---

## What We Do NOT Collect

- Full name
- Email address
- Phone number
- Physical address
- Government ID or passport number
- Payment card information
- Device identifiers or IP addresses
- Location tracking beyond checkpoint visit (no GPS tracking)
- Social media profiles

---

## Aggregate Reporting Only

All impact reports published to UNICEF and publicly will present **aggregate data only**:
- Total wallet addresses that claimed ≥1 POAP
- Total wallets that completed the route
- Total physical rewards redeemed
- Total POAP claims per checkpoint
- Completion rate (completions ÷ total starters)

No individual wallet-level data will appear in public reports.

---

## Participant Notice

Before or at the point of claiming their first POAP, participants will receive clear notice (displayed at the checkpoint or via the claim link landing page):

> **Participation Notice**
> Claiming this POAP records your wallet address and claim timestamp permanently on a public blockchain. This data is pseudonymous but publicly visible. No other personal information is required or collected. Your participation data is used only in aggregate for the Cartagena POAP Route impact report. For questions, contact [info@cartagenaonchain.xyz].

---

## Data Held by HOOP/Pulse

HOOP/Pulse, as the infrastructure provider, may retain technical logs associated with POAP claim events as required for the operation of their platform. Cartagena Onchain will ensure that its data processing agreement with HOOP/Pulse aligns with the data minimization principles in this document.

---

## Retention Policy

| Data Category | Retention Period | Disposal Method |
|--------------|-----------------|-----------------|
| On-chain POAP records | Permanent (public blockchain; cannot be deleted) | N/A |
| Operational redemption log | 12 months post-pilot end | Secure deletion |
| Incident logs | 12 months post-pilot end | Secure deletion |
| Vendor onboarding records | 24 months post-pilot end | Secure deletion |

---

## Applicable Framework

This pilot operates in Colombia. Data handling follows the principles of **Ley 1581 de 2012** (Colombia's personal data protection law) and its implementing decrees. Where participants include international tourists, we apply data minimization standards consistent with international best practices.

Because the core participation flow does not collect PII, formal data registration may not be required, but we will consult with legal counsel before pilot launch to confirm compliance obligations.

---

## Contact

Privacy questions related to this pilot: **Cartagena Onchain**  
*Contact information to be published at pilot launch.*
