# UNICEF Venture Fund — Application Form Answers
## Cartagena Onchain — Cartagena POAP Route Pilot

---

### Q1: What need or challenge is addressed? (120–150 words)

Local tourism and commerce programs in mid-sized cities like Cartagena lack reliable, verifiable systems for tracking participation across multiple independent stakeholders. Current approaches rely on paper stamps, printable coupons, or centralized databases — all of which are vulnerable to duplication, manipulation, and single-point failure. Vendors, sponsors, and municipal tourism offices have no neutral way to audit participation data independently; they must trust whichever organization controls the database. This opacity reduces accountability, enables reward fraud, and prevents programs from demonstrating that incentives are genuinely routing tourist spend to small local merchants. At the same time, tourists and residents have no incentive mechanism to complete curated routes that benefit local commerce. The result is a measurable gap between the stated goals of local tourism programs and actual, verifiable outcomes for the small businesses they claim to support.

---

### Q2: Describe the solution. (120–150 words)

The Cartagena POAP Route is a gamified, blockchain-verified participation program. Participants collect a Proof of Attendance Protocol (POAP) token at each of five real-world checkpoints across Cartagena — a mix of cultural landmarks and small local vendors — by scanning a QR code after a verifiable action such as a visit or purchase. When a single wallet holds all five POAPs, the participant qualifies for a completion POAP and redeems a limited-edition physical reward at an official redemption point. POAP tokens are non-transferable ERC-721 tokens recorded on a public blockchain, providing tamper-resistant, independently auditable proof of participation. The infrastructure is provided by HOOP/Pulse, a production smart-contract platform. Cartagena Onchain leads implementation: route design, vendor onboarding, community activation, and impact reporting. No single administrator can alter participation records after the fact, making the program verifiable to all stakeholders.

---

### Q3: What specific problem requires blockchain rather than a database? (100–150 words)

The Cartagena POAP Route involves multiple independent parties — vendors, a municipal tourism office, sponsors, and the implementing organization — none of whom share a pre-existing trust relationship or common administrative authority. If participation records live in a database controlled by any one party, the others must trust that administrator not to modify records. That trust cannot be independently verified, creating disputes and reducing confidence in program data. A public blockchain serves as a neutral third party: once a POAP token is issued to a wallet, no party — including the issuer — can alter or delete it without the wallet owner's private key. Any stakeholder can independently verify participation counts using a public block explorer, without requesting data from Cartagena Onchain. Additionally, the physical reward redemption step requires live on-chain verification, making counterfeit or duplicated proof technically impractical in a way that paper or database records cannot achieve.

---

### Q4: Which blockchain network/protocol does your solution use? (1–2 sentences)

The solution uses the POAP Protocol (ERC-721 non-transferable token standard) deployed on a primary EVM-compatible network — most likely Gnosis or Polygon — selected in coordination with our technology partner HOOP/Pulse, whose Pulse platform supports multi-chain deployment across Gnosis, Polygon, Base, Arbitrum, Celo, Mantle, Linea, ApeChain, Chiliz, and Unichain.

---

### Q5: Current technical status and what needs to be done. (100–150 words)

The core technology infrastructure is provided by HOOP/Pulse's Pulse platform, which is currently in production and supports POAP issuance, QR management, and verification across multiple EVM networks. Cartagena Onchain has confirmed this technology partnership. What remains to be completed on the technical side: POAP events must be created in Pulse for each of the five pilot checkpoints, QR codes generated and tested, and the verification workflow confirmed with redemption point staff. No custom smart-contract development is required. On the implementation side, route design, vendor onboarding, physical reward production, and community activation are pending grant award and the completion of partner discussions — particularly with local public-sector stakeholders whose involvement affects checkpoint placement. Exact timelines depend on partner approvals and logistics that cannot be fully scheduled before funding is confirmed.

---

### Q6: Are smart contracts used? Are they audited? (transparency answer)

Yes, smart contracts are used — specifically the POAP Protocol's ERC-721 smart contracts deployed through HOOP/Pulse's Pulse platform. However, Cartagena Onchain does **not** deploy or own these contracts. All smart-contract infrastructure is provided and operated by HOOP/Pulse. Security and audit documentation for the contracts is managed by HOOP/Pulse. Evaluators requiring audit references or technical security documentation should be directed to the HOOP/Pulse team; Cartagena Onchain will facilitate that introduction as part of due diligence.

---

### Q7: Pilot targets/milestones — next 12 months. (100–150 words)

Over 12 months from grant award, the pilot targets: (1) deployment of 5 POAP checkpoints across Cartagena, combining cultural landmarks and local vendor locations; (2) at least 500 unique wallet addresses claiming at least one checkpoint POAP; (3) at least 150 completed routes, defined as a wallet holding all five checkpoint POAPs; (4) at least 150 physical rewards redeemed at the official redemption point; (5) at least 1,000 total POAP claims across all checkpoints; and (6) at least two community activation events including a POAPthon-style guided walk. All on-chain metrics are independently verifiable via public block explorer. The pilot concludes with a final public impact report submitted to UNICEF and published to the project's public GitHub repository. Quarterly progress reports will be submitted at months six and nine.

---

### Q8: Key partners and advisors. (≤150 words)

**Confirmed Technology Partner:** HOOP / Pulse — provides all POAP issuance, smart-contract infrastructure, QR management, and verification tooling for the pilot. This partnership is confirmed.

**Protocol:** POAP Protocol — the ERC-721 non-transferable token standard underlying all checkpoint and completion tokens.

**In Discussions (not confirmed):**
- **Uniswap** — potential ecosystem education support and grant coordination
- **Base (Coinbase)** — potential consumer wallet onboarding and L2 ecosystem support
- **Tether / USDT** — potential stablecoin payment rails for merchant-friendly transactions
- **Mayor's Office of Cartagena** — potential institutional endorsement and checkpoint placement support
- **Corpoturismo** — potential tourism authority coordination and cultural site access
- **Local vendor and artisan associations** — potential checkpoint hosting

No commitments have been made by any of the "in discussions" parties. Letters of intent will be pursued during the pilot design phase if funding is awarded.

---

### Q9: Capital and other contributions. (100–150 words)

Cartagena Onchain's founders are leading this initiative and will contribute their time to design, project management, community engagement, and grant reporting throughout the pilot — this represents a meaningful in-kind contribution not captured in the budget. If funded, we will engage local contracted staff for vendor support, event coordination, and operational logistics. We plan to run a community design contest to select the visual identity for the completion reward, engaging local artists at a modest honorarium rather than a large design fee. We will also organize a POAPthon activation walk, which requires minimal direct cost but significant staff time. We are not seeking or taking on any loans. The organization's gross revenue last year was $5,000 USD; this is an early-stage service-based organization applying for grant funding to execute a measurable, time-bound city pilot with defined deliverables and public reporting.

---

### Q10: Recommended Checkbox Answers

- **Share application with partners?** ✅ YES
- **Receive funding opportunities updates?** ✅ YES
