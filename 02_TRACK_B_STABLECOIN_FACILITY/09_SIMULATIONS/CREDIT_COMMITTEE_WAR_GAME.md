# Credit Committee War Game — Track B Stablecoin Facility

**Version:** 1.0 | **Date:** February 9, 2026 | **Owner:** OPTKAS1 PMO  
**Purpose:** Simulate credit committee responses from 4 counterparty types to stress-test Track B readiness.  
**Usage:** Role-play each scenario internally before approaching counterparties. Identify gaps. Close them.

---

## HOW TO USE THIS DOCUMENT

1. **Assign roles:** Someone plays the Credit Committee. Someone plays the OPTKAS1 team.
2. **Pick a counterparty type** (1 of 4 below).
3. **Run all 3 scenarios** (A: Approve with conditions, B: Reject, C: Slow-walk).
4. **Answer every question** — if you can't, that's a gap. Log it.
5. **After each run:** Update the GAP tracker and CP Tracker with any new items.

---

## COUNTERPARTY TYPE 1: PRIVATE CREDIT FUND

**Profile:** $2B–$20B AUM. Direct lending desk. Familiar with ABL, structured credit, note-backed facilities. Likely has in-house legal, compliance, and portfolio management. Examples: Ares, HPS, Fortress, Benefit Street.

**What they care about most:** Collateral quality, valuation certainty, recovery analysis, covenant structure, reporting quality.

**Stablecoin comfort level:** 🟡 LOW-MEDIUM. Will need extensive education. Settlement in stablecoin is non-standard for these firms. Must be framed as "alternative settlement rail" with wire fallback always available.

---

### Scenario 1A: CONDITIONAL APPROVAL

**Decision:** APPROVE — subject to 10 conditions

**Credit Committee Questions (Top 15):**

| # | Role | Question |
|:--|:-----|:---------|
| 1 | Credit MD | What is the independent third-party valuation of the collateral? Who performed it? |
| 2 | Credit MD | Why are we settling in stablecoin instead of wire? What's the business justification? |
| 3 | Credit MD | Walk me through the recovery waterfall if the borrower defaults. What's our expected recovery rate? |
| 4 | Credit MD | Who is the custodian? Is there a tri-party or ACA in place? |
| 5 | Portfolio Mgr | How does this fit our fund's allocation? What's the concentration risk to a single issuer? |
| 6 | Legal | Is the UCC-1 perfected in Wyoming? Any conflicting liens? |
| 7 | Legal | What governing law applies to the stablecoin settlement component? Is it enforceable? |
| 8 | Legal | Can we perfect a security interest in the wallet? How? |
| 9 | Compliance | Has the borrower been screened against OFAC/SDN? What about the issuer? |
| 10 | Compliance | Does settling in USDC/USDT trigger additional AML/KYC obligations for our fund? |
| 11 | Compliance | Is Tether/Circle exposure acceptable under our fund docs? |
| 12 | Ops | How do we reconcile stablecoin receipts with our NAV calculations? |
| 13 | Ops | What happens if the chain goes down during a drawdown or repayment? |
| 14 | Ops | Who are the wallet signers? What controls are in place? |
| 15 | Risk | What's the haircut schedule? What happens between margin call and cure? |

**Required Conditions for Approval:**
1. Independent valuation from a recognized firm (Houlihan Lokey, Duff & Phelps, or equivalent)
2. Wire fallback for all settlements — stablecoin must be optional, not required
3. Account Control Agreement with STC executed before first draw
4. UCC-1 filed and confirmed — no prior liens
5. Insurance endorsement naming lender as loss payee
6. Borrower maintains minimum 250% collateral coverage at all times
7. Quarterly independent collateral verification
8. Compliance approval from our in-house AML team
9. Right to convert all settlement to wire at any time with 5 BD notice
10. Maximum 18-month initial term with mutual extension option

**Red Flags They'll Look For:**
- No independent valuation → immediate rejection
- Borrower insists on stablecoin-only settlement → suspicion of banking issues
- Insurance policy not naming lender → unsecured exposure
- Cost basis below face value without explanation → impairment concerns
- XRPL mentioned in any counterparty-facing document → "crypto deal" stigma

**Documents They'll Require:**
- Independent valuation report
- Borrower KYB + UBO disclosure
- Collateral schedule with CUSIP / ISIN
- STC custodian letter / ACA
- Insurance certificate + endorsement
- Borrower financial statements (2 years)
- Legal opinion on enforceability
- Wallet Controls Policy (sanitized)
- Draft term sheet + security agreement

**Fastest Path to Close:** 25–35 business days (assuming valuation in hand)

**Revised Term Sheet Summary:**
| Term | Counterparty Likely Position |
|:-----|:----------------------------|
| Size | $75M–$150M (start small, expand) |
| Advance Rate | 35–40% of face (conservative) |
| Rate | SOFR + 400–550 bps |
| Term | 12–18 months |
| Settlement | Wire primary, stablecoin optional |
| Covenants | Coverage ≥250%, monthly reporting, quarterly valuation |

---

### Scenario 1B: REJECTION

**Decision:** REJECT

**Reason:** "We don't have internal infrastructure to custody, reconcile, or account for stablecoin receipts. Our fund documents don't contemplate digital asset settlement. Our compliance team cannot approve Circle/Tether counterparty exposure without a 6-month review."

**Top 5 Rejection Drivers:**
1. No internal stablecoin custody or reconciliation capability
2. Fund LPA doesn't authorize digital asset transactions
3. Compliance cannot approve stablecoin exposure on required timeline
4. No independent collateral valuation available
5. Borrower entity too new (formed December 2025)

**What Would Change Their Mind:**
- 100% wire settlement (remove stablecoin entirely) → re-review as traditional ABL
- Independent valuation from tier-1 firm delivered before next IC meeting
- 24+ months of borrower operating history or guarantor with track record
- Insurance coverage from A-rated carrier with explicit lender-as-loss-payee endorsement

**Lesson:** For private credit funds without digital asset infrastructure, **present Track A framing** (traditional ABL with XRPL as internal ledger only). Stablecoin settlement is optional, not default.

---

### Scenario 1C: SLOW-WALK

**Decision:** DELAY — "Interesting. Let us take it to our next IC meeting."

**What They Actually Mean:** They're interested in the collateral but uncomfortable with settlement mechanics. They'll study it for 4–8 weeks, ask repetitive questions, and ultimately request wire-only settlement.

**Pattern:**
- Week 1: Request full data room access. Download everything.
- Week 2: Radio silence.
- Week 3: Follow-up — "Still reviewing internally."
- Week 4: Junior associate asks 15 questions (most already answered in docs).
- Week 5: Request call with "our head of operations."
- Week 6: After ops call, request wire-only option.
- Week 7: Send markup of term sheet with wire-only settlement.
- Week 8: IC meeting. Conditional approval (wire-only).

**How to Accelerate:**
1. At initial meeting, proactively offer wire fallback as primary
2. Provide a 1-page "FAQ for Credit Committees" addressing top 10 concerns
3. Offer to present directly to their IC (15-minute slot)
4. Deliver the independent valuation before their IC date
5. Offer a smaller pilot facility ($25M–$50M) to build comfort

**Timeline Impact:** 45–60 business days (vs. 25–35 if properly prepared)

---

---

## COUNTERPARTY TYPE 2: MARKET MAKER / OTC DESK

**Profile:** Digital asset native. $500M–$5B in daily trading volume. Familiar with stablecoin settlement. Likely uses Fireblocks, BitGo, or similar custody. In-house compliance team focused on crypto AML/KYC. Examples: Galaxy, Cumberland, Wintermute, B2C2.

**What they care about most:** Settlement speed, chain compatibility, counterparty risk, collateral liquidity (can they liquidate the notes?), operational efficiency.

**Stablecoin comfort level:** 🟢 HIGH. This is their native environment. They settle in stablecoin daily. Their concern is counterparty risk, not settlement mechanics.

---

### Scenario 2A: CONDITIONAL APPROVAL

**Decision:** APPROVE — subject to 8 conditions

**Credit Committee Questions (Top 15):**

| # | Role | Question |
|:--|:-----|:---------|
| 1 | Head of Lending | What's the secondary market liquidity for TC Advantage 5% notes? Can we liquidate in a default? |
| 2 | Head of Lending | Why do you need stablecoin if you could get a bank wire facility? Is there a banking problem? |
| 3 | Head of Lending | What's the borrower's track record? Any prior defaults or restructurings? |
| 4 | Risk | What chain do you prefer? We need to match our custody infrastructure. |
| 5 | Risk | What's the haircut if USDT depegs during the facility term? Who bears that risk? |
| 6 | Risk | What's the mark-to-market methodology for the collateral? |
| 7 | Legal | Is this a loan or a repo? How is it structured for tax purposes? |
| 8 | Legal | Can we get a UCC filing on medium-term notes held at STC? |
| 9 | Legal | What jurisdiction governs? Can we get a legal opinion on enforceability in Wyoming? |
| 10 | Compliance | Has the issuer (TC Advantage Traders, Ltd.) been through our KYB? They're Bahamas-registered. |
| 11 | Compliance | What's the source of the notes? Were they purchased or gifted? |
| 12 | Ops | Which wallet infrastructure does the borrower use? Fireblocks? BitGo? Self-custody? |
| 13 | Ops | What's the settlement window? T+0? T+1? |
| 14 | Ops | Can we automate reporting via API? |
| 15 | Trading | Can we hedge our exposure to the collateral? Is there a CDS or repo market for these notes? |

**Required Conditions for Approval:**
1. Collateral must be held at a recognized custodian (STC acceptable if ACA in place)
2. Borrower must demonstrate note acquisition (trade confirmations or issuance evidence)
3. Issuer (TC Advantage) KYB must pass our compliance screening (Bahamas entity)
4. Settlement in USDC on Ethereum or Base (not USDT on Tron — our custody doesn't support it)
5. Insurance policy must explicitly cover custodian risk
6. Weekly collateral valuation (not monthly)
7. Right to liquidate collateral within 10 BD of default
8. Maximum 12-month term (rolling quarterly renewal)

**Red Flags They'll Look For:**
- Self-custody wallets without institutional-grade security
- No secondary market for the notes (recovery uncertainty)
- Cost basis significantly below face → potential impairment or distressed acquisition
- Bahamas issuer with no US regulatory touchpoint
- Borrower entity formed <90 days ago

**Documents They'll Require:**
- Note purchase agreement or issuance evidence
- STC custodian confirmation + ACA draft
- Insurance certificate (full policy if available)
- Wallet infrastructure documentation
- Entity docs + UBO for borrower AND issuer
- Borrower compliance self-certification
- Draft term sheet

**Fastest Path to Close:** 10–15 business days (they move fast)

**Revised Term Sheet Summary:**
| Term | Counterparty Likely Position |
|:-----|:----------------------------|
| Size | $50M–$100M (standard for OTC) |
| Advance Rate | 30–35% of face (more conservative — no secondary market) |
| Rate | 8–12% fixed (they price risk, not SOFR-based) |
| Term | 6–12 months, quarterly rollover |
| Settlement | USDC on Ethereum, T+0 |
| Covenants | Weekly reporting, 300%+ coverage, rapid liquidation rights |

---

### Scenario 2B: REJECTION

**Decision:** REJECT

**Reason:** "The underlying collateral (medium-term notes from a Bahamas issuer) has zero secondary market liquidity. In a default scenario, we cannot liquidate. We'd be holding illiquid paper in a market where we can't find a bid. Our risk committee requires a clear exit path."

**Top 5 Rejection Drivers:**
1. No secondary market for TC Advantage notes — can't price recovery
2. Bahamas-registered issuer raises compliance concerns for US-regulated entities
3. Entity formed December 2025 — no operating history
4. Cannot determine market value without independent valuation or comparable trades
5. Internal policy requires minimum $100M AUM for borrowers in this category

**What Would Change Their Mind:**
- Evidence of secondary market trades or indicative bids from broker-dealers
- Independent valuation from a firm they trust
- Guarantor with verifiable assets and operating history
- Structure as a repo rather than a loan (cleaner for their books)
- Pilot facility at $10M to test operations before scaling

**Lesson:** Market makers think in terms of liquidity and exit. Show them a path to liquidation or they won't engage.

---

### Scenario 2C: SLOW-WALK

**Decision:** DELAY — "Send us the full package. We'll review and circle back."

**What They Actually Mean:** Their lending desk is interested but needs to get sign-off from risk and compliance. Risk wants to model recovery scenarios. Compliance needs to clear the Bahamas issuer. This takes 3–4 weeks, not their usual 5 business days.

**Pattern:**
- Day 1: Strong interest. Request all docs immediately.
- Day 3: Compliance flags Bahamas entity. Requests additional issuer KYB.
- Day 7: Risk asks for collateral valuation. "Who's valued these notes?"
- Day 10: You provide everything. Silence.
- Day 15: They ask if you'd consider a repo structure instead of a loan.
- Day 20: Counter-proposal arrives — materially different terms.

**How to Accelerate:**
1. Proactively provide issuer KYB, formation docs, regulatory status
2. Send independent valuation (even if indicative)
3. Offer both loan and repo structure options
4. Propose a $25M pilot with expansion clause
5. Provide a pre-formatted compliance package matching their standard intake

**Timeline Impact:** 20–30 business days (vs. 10–15 if prepared)

---

---

## COUNTERPARTY TYPE 3: BANK-ADJACENT LENDING DESK

**Profile:** Lending platform affiliated with or spun out of a bank. Subject to bank-like compliance but more flexible on collateral types. May have treasury desk that handles stablecoin. $5B–$50B in assets. Examples: Goldman Sachs Digital Assets, JPM Onyx-adjacent desks, Nomura/Laser Digital, Standard Chartered Zodia.

**What they care about most:** Regulatory compliance, institutional reputation risk, documentation quality, structured finance precedent, audit trail.

**Stablecoin comfort level:** 🟡 MEDIUM. They understand stablecoin but require extensive documentation. Every settlement must look like a traditional transaction with an alternative payment rail. Wire fallback is mandatory.

---

### Scenario 3A: CONDITIONAL APPROVAL

**Decision:** APPROVE — subject to 12 conditions

**Credit Committee Questions (Top 15):**

| # | Role | Question |
|:--|:-----|:---------|
| 1 | MD, Structured Lending | Has this type of facility been done before? Show me precedent transactions. |
| 2 | MD, Structured Lending | What's the credit profile of the issuer? Is there a rating or shadow rating? |
| 3 | MD, Structured Lending | Why is a Wyoming Series LLC the borrower? Is there a parent guarantor? |
| 4 | Legal (External) | Is the security interest enforceable under Wyoming law? Bahamas law? |
| 5 | Legal (External) | What's the treatment of stablecoin settlement under the Facility Agreement? Is it a "payment" or a "transfer"? |
| 6 | Legal (External) | Can you provide a legal opinion from both Wyoming and Bahamas counsel? |
| 7 | Compliance | Has this passed our enhanced due diligence process for digital asset-related transactions? |
| 8 | Compliance | Does the borrower have a FinCEN registration or MSB license? |
| 9 | Compliance | What's our exposure to Tether Limited / Circle Internet Financial as a settlement counterparty? |
| 10 | Risk | Run me through the 5 stress scenarios: rate shock, collateral impairment, chain outage, stablecoin depeg, borrower default. |
| 11 | Risk | What's the correlation between the collateral and stablecoin? If one fails, does the other? |
| 12 | Ops | Can we integrate settlement reporting into our existing middle office systems? |
| 13 | Ops | What's the reconciliation process? Who reconciles — us or the borrower? |
| 14 | Audit | Will our auditors accept stablecoin receipts as "cash equivalents"? What accounting treatment applies? |
| 15 | Board Rep | What's the reputational risk if this transaction becomes public? How do we explain it to our regulators? |

**Required Conditions for Approval:**
1. Independent valuation from Houlihan Lokey, Duff & Phelps, or Kroll
2. Legal opinions from both Wyoming and Bahamas counsel
3. Wire settlement as primary — stablecoin as alternative only
4. Full KYB/KYC/EDD on borrower, issuer, and all UBOs
5. Insurance policy review by our insurance counsel
6. ACA executed with STC before any draw
7. UCC-1 filed, first-priority confirmed
8. Borrower financial projections + use of proceeds detailed
9. Quarterly board-level reporting on collateral status
10. Engagement of independent collateral monitor
11. Right to demand full wire conversion at any time
12. Annual facility review with full re-underwriting

**Red Flags They'll Look For:**
- Any reference to "blockchain" or "crypto" or "XRPL" in counterparty-facing docs
- Borrower entity formed <6 months ago with no parent guarantor
- Insurance from non-rated or unfamiliar carriers
- No independent valuation — rely on issuer's own assessment
- Stablecoin presented as "innovative" rather than "alternative settlement"

**Documents They'll Require:**
- Everything a private credit fund requires (see Type 1), PLUS:
- Borrower business plan / use of proceeds memo
- Independent collateral monitor engagement letter
- Legal opinions (2: Wyoming + Bahamas)
- Insurance policy review memo from their counsel
- Tax memo on stablecoin settlement treatment
- Accounting memo on cash equivalent treatment
- Draft regulatory notification (if required by their regulator)

**Fastest Path to Close:** 45–60 business days

**Revised Term Sheet Summary:**
| Term | Counterparty Likely Position |
|:-----|:----------------------------|
| Size | $100M–$300M (they go big or don't bother) |
| Advance Rate | 35–40% of face |
| Rate | SOFR + 350–500 bps |
| Term | 24–36 months (longer terms, fewer renewals) |
| Settlement | Wire primary, stablecoin optional with 10 BD conversion right |
| Covenants | Full suite — coverage, financial covenants, reporting, independent monitor |

---

### Scenario 3B: REJECTION

**Decision:** REJECT

**Reason:** "Our internal digital asset policy committee has not yet approved lending against medium-term notes settled via stablecoin. This requires a policy-level approval that typically takes 3–6 months. Additionally, the borrower entity lacks operating history and there is no independent valuation. We suggest you return to us in Q3 2026 with an updated package."

**Top 5 Rejection Drivers:**
1. Internal digital asset policy not yet established or approved
2. Reputational risk — cannot be seen as a "crypto lender"
3. No precedent transaction in their portfolio for this structure
4. Regulatory uncertainty — uncertain treatment by their primary regulator
5. Borrower too new, no guarantor, no operating history

**What Would Change Their Mind:**
- Remove all stablecoin references — present as pure traditional ABL
- Provide a parent or personal guarantor with verifiable net worth
- Independent valuation + independent collateral monitor already engaged
- Structure matches an existing facility template they've done before
- Wait 6+ months for policy committee to clear digital asset lending

**Lesson:** Bank-adjacent desks need everything to look like something they've done before. Frame it as "traditional ABL with an optional alternative settlement rail" or go 100% traditional.

---

### Scenario 3C: SLOW-WALK

**Decision:** DELAY — "We need to socialize this internally."

**What They Actually Mean:** Multiple committees need to approve. Structured Lending likes it. Legal has questions. Compliance needs 4–6 weeks. Risk needs to model. The deal champion needs to navigate internal politics.

**Pattern:**
- Week 1–2: Initial enthusiasm. Data room request. "This is interesting."
- Week 3–4: Legal sends 30-page due diligence questionnaire.
- Week 5–6: You respond. Silence while they circulate internally.
- Week 7–8: Compliance raises concerns. Requests meeting with your compliance officer.
- Week 9–10: Risk models scenarios. Requests independent valuation.
- Week 11–12: Internal pre-committee meeting. "We need a few more items."
- Week 13–14: Full committee meeting. Conditional approval or table to next quarter.

**How to Accelerate:**
1. Identify and cultivate the internal deal champion (usually the MD)
2. Proactively address every likely committee concern in the initial package
3. Provide a pre-formatted DDQ response (anticipate their 30-page questionnaire)
4. Offer to present to each committee separately (legal, risk, compliance)
5. Deliver the independent valuation before they ask for it
6. Structure as 100% wire settlement to remove the stablecoin friction entirely

**Timeline Impact:** 60–90 business days (vs. 45–60 if properly prepared)

---

---

## COUNTERPARTY TYPE 4: CRYPTO-NATIVE LENDER

**Profile:** Digital asset lending platform or fund. $100M–$2B in lending capacity. Fully comfortable with stablecoin settlement. May lack traditional structured finance expertise. Focused on yield and collateral coverage. Examples: Maple Finance, Clearpool, Goldfinch, Centrifuge ecosystem participants.

**What they care about most:** Yield, collateral coverage ratio, operational simplicity, smart contract integration (if applicable), borrower reputation in crypto community.

**Stablecoin comfort level:** 🟢🟢 VERY HIGH. This is all they do. Settlement mechanics are a non-issue. Their concern is whether the collateral is real and recoverable.

---

### Scenario 4A: CONDITIONAL APPROVAL

**Decision:** APPROVE — subject to 6 conditions

**Credit Committee Questions (Top 15):**

| # | Role | Question |
|:--|:-----|:---------|
| 1 | CIO | What's the yield? How does this compare to our other lending opportunities? |
| 2 | CIO | What's the LTV? What's the coverage ratio at our advance rate? |
| 3 | CIO | Can we verify the collateral exists? Can we see the STC statements? |
| 4 | Risk | What happens if the issuer defaults on the notes? Does our security interest survive? |
| 5 | Risk | What's the recovery timeline? In a default, how long until we get our money back? |
| 6 | Risk | Have you stress-tested a 50% collateral value decline? |
| 7 | Legal | Is a UCC-1 filing sufficient? Do we need additional security in the Bahamas? |
| 8 | Legal | Can we get a pledge agreement directly on the notes? |
| 9 | Legal | Is the insurance assignment enforceable? |
| 10 | Ops | Which chain? USDC or USDT? We prefer USDC on Ethereum. |
| 11 | Ops | Can we set up automated interest payments? |
| 12 | Ops | What reporting do we receive? Is there an API? |
| 13 | Compliance | Is the borrower a US entity? What's our tax withholding obligation? |
| 14 | Compliance | Has the borrower passed KYC with a recognized provider? |
| 15 | Community | Can we disclose this transaction to our LPs / token holders? Is there a co-marketing opportunity? |

**Required Conditions for Approval:**
1. STC custody confirmation + direct verification of note holdings
2. Insurance certificate naming lender
3. UCC-1 filed (they may not require ACA — less institutional rigor)
4. Settlement in USDC on Ethereum (standard for their platform)
5. Monthly reporting minimum (daily preferred)
6. Right to publicize the transaction (may be a dealbreaker if declined)

**Red Flags They'll Look For:**
- Borrower refusing to share custody statements → collateral doesn't exist
- No insurance or insurance from unknown carrier
- Wire-only settlement → "Why are you borrowing from us if you have bank access?"
- Excessive legal complexity → "This should be simpler"
- Borrower asking for confidentiality → can't market the deal

**Documents They'll Require:**
- Entity KYB + UBO (standard, not extensive)
- STC custody confirmation letter
- Insurance certificate
- Collateral schedule
- Draft term sheet
- Wallet addresses
- (Much lighter package than Types 1–3)

**Fastest Path to Close:** 5–10 business days

**Revised Term Sheet Summary:**
| Term | Counterparty Likely Position |
|:-----|:----------------------------|
| Size | $10M–$50M (smaller, faster) |
| Advance Rate | 25–35% of face (crypto-native applies heavy haircuts to TradFi collateral) |
| Rate | 10–15% fixed (yield-focused) |
| Term | 3–6 months (short, rollover) |
| Settlement | USDC on Ethereum, T+0, automated |
| Covenants | Coverage ≥300%, weekly reporting, rapid liquidation |

---

### Scenario 4B: REJECTION

**Decision:** REJECT

**Reason:** "We don't lend against TradFi collateral. We can't verify it, we can't liquidate it, and our LPs don't understand it. We need on-chain collateral or tokenized assets we can price in real-time."

**Top 5 Rejection Drivers:**
1. Cannot verify or liquidate traditional securities collateral
2. No on-chain representation of the notes (can't "see" the collateral)
3. Recovery process (UCC enforcement, court process) is too slow for their model
4. Their platform requires on-chain collateral for automated liquidation
5. LP/token holder base doesn't understand medium-term note collateral

**What Would Change Their Mind:**
- Tokenize the notes on Ethereum with real-time proof of reserve → enables automated monitoring
- Create a Chainlink proof-of-reserve feed for the collateral
- Offer a much lower LTV (20%) to compensate for illiquidity risk
- Provide a short pilot ($5M) to build track record
- Use Track C (tokenized credit facility) instead of Track B

**Lesson:** Crypto-native lenders want on-chain visibility. If collateral can't be verified on-chain, they're uncomfortable. This is the best argument for eventually activating Track C.

---

### Scenario 4C: SLOW-WALK

**Decision:** DELAY — "Cool. Let us look at this. Can you join our Discord?"

**What They Actually Mean:** They're intrigued but it's not their standard product. Someone needs to champion it internally. They may be exploring whether to build a new product category for TradFi-collateral lending.

**Pattern:**
- Day 1: Excited DM from their BD team. "Love this. Let's move fast."
- Day 3: Request docs. You send everything.
- Day 5: They share with their CIO. CIO wants a call.
- Day 7: Call goes well. "We need to talk to our risk team."
- Day 14: Risk team comes back with questions about recovery mechanics.
- Day 21: They propose a materially different structure (higher rate, lower LTV, shorter term).
- Day 30: Internal discussion about whether to create a new lending pool.
- Day 45: Either counter-proposal arrives or they go quiet.

**How to Accelerate:**
1. Offer to create a co-branded lending product if their platform supports it
2. Provide a complete "plug-and-play" package they can integrate into their existing infrastructure
3. Offer very attractive yield (12%+) to make it worth the operational effort
4. Agree to their publicity requirements (many need to announce deals)
5. Be willing to accept their standard loan agreement format rather than pushing yours

**Timeline Impact:** 30–45 business days (vs. 5–10 if it matches their standard product)

---

---

## GAP ANALYSIS — CROSS-COUNTERPARTY

| Gap | Impact | Counterparty Types Affected | Mitigation | Priority |
|:----|:-------|:----------------------------|:-----------|:---------|
| No independent valuation | CRITICAL — blocks every serious counterparty | 1, 2, 3, 4 | Engage Houlihan Lokey / Duff & Phelps immediately | 🔴 P1 |
| Entity formed <90 days | HIGH — concern for all institutional counterparties | 1, 3 | Provide guarantor or demonstrate operator track record (Unykorn 7777) | 🟠 P2 |
| No secondary market evidence | HIGH — market makers require liquidation path | 2, 4 | Obtain indicative bids or dealer quotes for TC Advantage notes | 🟠 P2 |
| Bahamas issuer jurisdiction risk | MEDIUM — compliance flags for regulated entities | 2, 3 | Provide comprehensive issuer KYB, legal opinions, regulatory status | 🟡 P3 |
| Stablecoin settlement unfamiliarity | MEDIUM — friction for traditional lenders | 1, 3 | Default to wire settlement; present stablecoin as optional | 🟡 P3 |
| No financial statements / projections | MEDIUM — required by institutional counterparties | 1, 3 | Prepare borrower financials + use of proceeds memo | 🟡 P3 |

---

## READINESS SCORECARD

| Dimension | Ready? | Notes |
|:----------|:-------|:------|
| Entity KYB package | ✅ Yes | Formation, OA, good standing available |
| Collateral documentation | ✅ Yes | Issuance Resolution, custodian, schedule |
| Insurance | ✅ Yes | C.J. Coleman, $625M, Lloyd's backed |
| Legal framework | ✅ Yes | Term sheet template, security agreement draft |
| Wallet controls | ✅ Yes | Policy documented, controls designed |
| Compliance package | ✅ Yes | KYB/KYC, sanctions, SoF documented |
| Independent valuation | ❌ No | **MUST OBTAIN — #1 gating item for all counterparties** |
| Independent collateral monitor | ❌ No | Required by bank-adjacent counterparties |
| Financial statements | ❌ No | Borrower is newly formed — limited financials |
| Secondary market evidence | ❌ No | No known dealer quotes for TC Advantage notes |
| Legal opinions (dual jurisdiction) | ❌ No | Wyoming + Bahamas opinions not yet engaged |
| Guarantor / credit enhancement | ❌ No | Consider personal guarantee or Unykorn support letter |

---

## COUNTERPARTY PRIORITY MATRIX

| Priority | Counterparty Type | Rationale | Target Close |
|:---------|:-----------------|:----------|:-------------|
| 1st | Market Maker / OTC | Fastest close (10–15 BD), native stablecoin, smaller initial size | Q1 2026 |
| 2nd | Private Credit Fund | Larger facilities, longer relationships, need valuation first | Q2 2026 |
| 3rd | Bank-Adjacent | Largest facilities but longest process — start early, close later | Q2–Q3 2026 |
| 4th | Crypto-Native | Quick but small, may not accept TradFi collateral | Opportunistic |

---

*This document is for internal simulation purposes only. Not for distribution to counterparties.*  
*Update gap analysis after every simulation run.*
