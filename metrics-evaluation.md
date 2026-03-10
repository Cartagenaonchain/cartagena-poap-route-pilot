# Metrics & Evaluation Plan

## Overview

The Cartagena POAP Route pilot uses on-chain data as its primary measurement source, supplemented by operational records. All metrics are defined here to ensure consistent measurement and reporting to UNICEF.

---

## Primary KPIs (12-Month Targets)

| KPI | Definition | Data Source | 12-Month Target |
|-----|-----------|-------------|-----------------|
| **Total POAP Claims** | Number of individual POAP tokens claimed across all 5 checkpoints | On-chain (Pulse dashboard / block explorer) | ≥1,000 |
| **Unique Wallets Claiming ≥1 POAP** | Count of distinct wallet addresses that claimed at least one checkpoint POAP | On-chain | ≥500 |
| **Route Completion Count** | Number of unique wallets that hold all 5 checkpoint POAPs | On-chain | ≥150 |
| **Completion Rate** | Route completions ÷ unique wallets claiming ≥1 POAP | Calculated | ≥30% |
| **Physical Rewards Redeemed** | Count of physical rewards distributed at redemption point | Redemption ledger | ≥150 |
| **Participating Vendors / Locations** | Count of active checkpoint hosts | Operational records | ≥5 |
| **Completion POAPs Issued** | Count of completion POAPs minted (proxy for verified full completions) | On-chain | ≥150 |

---

## Secondary KPIs

| KPI | Definition | Data Source | Target |
|-----|-----------|-------------|--------|
| **Activation Events Held** | Number of organized community walk or activation events | Operational records | ≥2 |
| **Vendor Retention Rate** | % of vendors who remain active through end of pilot | Operational records | ≥80% |
| **Incident Rate** | Number of confirmed fraud incidents per 100 claims | Incident log | <2% |
| **Checkpoint Uptime** | % of planned operating days each checkpoint QR was active | Operational records | ≥90% |

---

## KPI Definitions in Detail

### Total POAP Claims
A "POAP claim" is recorded when a wallet address successfully mints a POAP token from a checkpoint event. One wallet claiming from Checkpoint 1 = 1 claim. The same wallet claiming from Checkpoint 2 = a second claim. Total claims across all 5 checkpoints is the broadest engagement signal.

### Unique Wallets Claiming ≥1 POAP
This is the reach metric — how many distinct individuals (as proxied by wallet addresses) engaged with the route at any level. Because one person may use multiple wallets (Sybil behavior), this is an upper-bound estimate. Physical redemption limits help correct for this at the completion stage.

### Route Completion Count
A wallet is counted as a "completion" if it holds POAPs from all 5 designated checkpoint events in the pilot. This is verified on-chain. It is the primary impact metric and is required for physical reward redemption.

### Completion Rate
Completion Rate = Route Completion Count ÷ Unique Wallets Claiming ≥1 POAP × 100. A rate above 30% would indicate strong route engagement and incentive design effectiveness.

### Physical Rewards Redeemed
Count of physical rewards distributed at the official redemption point. This is logged in the operational redemption ledger. It must equal or closely match Route Completion Count; discrepancies are flagged for investigation.

### Completion POAPs Issued
The completion POAP is issued after staff verify all 5 checkpoint POAPs are held. Count of completion POAPs issued is an on-chain cross-check against the redemption ledger.

---

## Data Collection Methods

| Source | Method | Frequency |
|--------|--------|-----------|
| On-chain POAP data | Pulse dashboard export or public block explorer API | Quarterly + final |
| Redemption ledger | Manual log maintained by redemption point staff | Ongoing; reviewed quarterly |
| Incident log | Recorded by Cartagena Onchain operations team | Ongoing |
| Vendor status | Check-in calls / visit with each vendor | Monthly |
| Activation events | Event records and attendance estimates | Per event |

---

## Reporting Schedule

| Report | Timing | Contents |
|--------|--------|----------|
| Quarterly Report #1 | Month 6 (approx.) | Phase 1–2 milestones, preliminary POAP data, incident log summary |
| Quarterly Report #2 | Month 9 (approx.) | Phase 3 milestones, updated KPIs, vendor status |
| Final Report | Month 12 | All KPIs, full pilot narrative, financial summary, lessons learned |

All reports will be submitted to UNICEF and the final report will be published publicly to this repository.

---

## What We Will Not Report

- Individual wallet address data (only aggregate counts)
- Any PII collected incidentally
- Speculation about economic value of POAPs or token appreciation

---

## Evaluation Questions

At close-out, the final report will address:

1. Did the route successfully verify participation across multiple independent stakeholders without a trusted central administrator?
2. Did the anti-fraud controls perform as designed? What was the confirmed incident rate?
3. Did route completion incentives measurably direct tourist engagement to small local vendors?
4. What would need to change to scale this model to additional cities or routes?
5. Is the model financially sustainable beyond the grant period, and under what conditions?
