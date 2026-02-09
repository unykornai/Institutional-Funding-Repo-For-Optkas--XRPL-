# Risk Policy — Haircuts, LTV & Margin Calls (Track B)

**Version:** 1.0 | **Date:** February 9, 2026 | **Owner:** OPTKAS1 PMO  
**Applies To:** Stablecoin Facility under Track B

---

## 1. ADVANCE RATE & HAIRCUT SCHEDULE

### 1.1 Base Advance Rate

| Valuation Basis | Advance Rate | Maximum Facility | Coverage Ratio |
|:----------------|:-------------|:----------------|:---------------|
| **Face Value ($5B)** | 40% | $2,000,000,000 | 250% |
| **Cost Basis ($3B)** | 50% | $1,500,000,000 | 200% |
| **Independent Valuation** | Per valuation | Per valuation | Minimum 200% |

**Default basis for Track B:** Cost basis ($3B) — more conservative, easier to defend with Issuance Resolution evidence.

### 1.2 Haircut Schedule by Collateral Quality Tier

| Tier | Description | Haircut | Effective Advance Rate (vs Face) |
|:-----|:-----------|:--------|:--------------------------------|
| **Tier 1** | Full documentation + BOV + STC holder statement + control agreement executed | 50% | 50% |
| **Tier 2** | Full documentation + Issuance Resolution (no BOV yet) | 60% | 40% |
| **Tier 3** | Partial documentation (pre-control agreement) | 70% | 30% |
| **Tier 4** | Indicative only (pre-STC confirmation) | 80% | 20% |

**Current status:** Tier 2 (full documentation + Issuance Resolution; BOV pending as CP-18).

### 1.3 Haircut Adjustment Triggers

| Event | Haircut Impact | Action |
|:------|:-------------|:-------|
| BOV obtained (CP-18 closed) | Move to Tier 1 | Advance rate increases |
| Control agreement executed (CP-31 closed) | Confirm Tier 1 eligibility | Security perfected |
| Insurance endorsement obtained (CP-34 closed) | No tier change but strengthens recovery | Update risk model |
| Collateral impairment event | Increase haircut by 10–20% | Margin call if needed |
| Issuer credit event | Increase haircut by 20–40% | Potential default trigger |
| Market dislocation (broad) | Review on case-by-case basis | Monitoring escalation |

---

## 2. LOAN-TO-VALUE (LTV) FRAMEWORK

### 2.1 LTV Calculation

$$
LTV = \frac{\text{Outstanding Principal}}{\text{Collateral Value (per agreed basis)}} \times 100
$$

### 2.2 LTV Thresholds

| Level | LTV Range | Status | Action |
|:------|:----------|:-------|:-------|
| 🟢 **Normal** | ≤ 40% | Compliant | Standard reporting |
| 🟡 **Watch** | 40.1% – 50% | Monitoring | Increase reporting frequency to daily; prepare margin call |
| 🟠 **Warning** | 50.1% – 60% | Margin call triggered | Borrower must cure within [5] BD |
| 🔴 **Critical** | > 60% | Event of default risk | Lender may exercise remedies per facility agreement |

### 2.3 LTV Monitoring Frequency

| LTV Level | Monitoring | Report |
|:----------|:----------|:-------|
| 🟢 Normal | Monthly | Monthly BBC |
| 🟡 Watch | Weekly | Weekly LTV snapshot |
| 🟠 Warning | Daily | Daily LTV + cure plan |
| 🔴 Critical | Continuous | Lender discretion |

---

## 3. MARGIN CALL FRAMEWORK

### 3.1 Margin Call Trigger

A margin call is issued when:
- LTV exceeds the Warning threshold (50.1%)
- OR collateral coverage ratio falls below 200%
- OR a collateral impairment event occurs

### 3.2 Margin Call Process

| Step | Action | Owner | Timeline |
|:-----|:-------|:------|:---------|
| 1 | Lender issues Margin Call Notice (amount required to cure) | Lender | Day 0 |
| 2 | Borrower acknowledges receipt | Borrower | Same day |
| 3 | Borrower presents Cure Plan | Borrower | Within 1 BD |
| 4 | Borrower executes cure (repay principal / post additional collateral) | Borrower | Within [5] BD |
| 5 | Lender confirms LTV restored to Normal range | Lender | Same day as cure |
| 6 | Reporting returns to standard frequency | Both | Upon cure confirmation |

### 3.3 Cure Options

| Option | Mechanism | Effect |
|:-------|:---------|:-------|
| **A) Repay principal** | Borrower sends stablecoin to reduce outstanding balance | LTV decreases |
| **B) Post additional collateral** | Borrower pledges additional eligible assets (if available) | Denominator increases |
| **C) Cash margin deposit** | Borrower deposits cash/stablecoin into margin account | Creates cash cushion |

### 3.4 Failure to Cure

If Borrower fails to cure within the [5] BD cure period:
1. Lender may declare Event of Default
2. Lender may exercise remedies under Security Agreement
3. Lender may instruct STC directly under Control Agreement
4. Lender may accelerate facility (all amounts immediately due)
5. Lender may initiate UCC foreclosure

---

## 4. COLLATERAL VALUATION METHODOLOGY

### 4.1 Valuation Approaches (in order of preference)

| Priority | Method | Source | Frequency |
|:---------|:-------|:------|:----------|
| 1 | **Independent Broker Opinion of Value (BOV)** | Third-party broker-dealer | Annual (minimum); on request |
| 2 | **Cost Basis** | Subscription Agreement + Issuance Resolution | Static (updated if new purchases) |
| 3 | **Face Value** | PPM + Issuance Resolution | Static |
| 4 | **Negotiated Floor** | Agreed between Borrower and Lender | Per facility terms |

### 4.2 Current Valuation Status

| Basis | Value | Source | Status |
|:------|:------|:------|:-------|
| Face Value | $5,000,000,000 | PPM + Issuance Resolution (Jan 22, 2026) | ✅ Documented |
| Cost Basis | $3,000,000,000 | Subscription Agreement | ✅ Documented |
| BOV | Pending | CP-18 (primary gating item) | 🟡 In progress |
| Negotiated Floor | TBD | Per facility negotiation | 🔲 Not yet |

### 4.3 Revaluation Events

Collateral must be revalued if:
- Issuer credit event (rating change, default, restructuring)
- Material change in comparable market values
- Lender requests (with reasonable basis)
- 12 months since last independent valuation
- Insurance coverage changes materially

---

## 5. RECOVERY ANALYSIS

### 5.1 Recovery Scenarios

| Scenario | Assumptions | Recovery Rate | Recovery Amount (on $300M draw) |
|:---------|:-----------|:-------------|:-------------------------------|
| **Base Case** | Orderly liquidation, no impairment, insurance intact | 90–100% | $270M–$300M |
| **Stress** | Forced sale, 40% discount, partial insurance | 60–80% | $180M–$240M |
| **Catastrophic** | Deep discount, legal delay, insurance dispute | 30–45% | $90M–$135M |

### 5.2 Recovery Waterfall

1. **Primary:** Direct sale of pledged notes via DTC/DWAC (STC facilitates)
2. **Secondary:** Insurance claim (C.J. Coleman / Lloyd's, up to $625M)
3. **Tertiary:** Coupon income capture (5% × $5B = $250M/yr gross)
4. **Quaternary:** UCC foreclosure and judicial enforcement
5. **Final:** Deficiency claim against Borrower SPV

---

## 6. STRESS TESTING

### 6.1 Scenarios to Run Quarterly

| Scenario | Parameter Shocked | Magnitude | Metrics to Track |
|:---------|:-----------------|:----------|:----------------|
| Collateral devaluation | Valuation basis | -20%, -40%, -60% | LTV, coverage ratio, margin call trigger |
| Interest rate shock | SOFR | +200bps, +400bps | Debt service coverage, interest cost |
| Liquidity freeze | Ability to sell notes | 0% recovery for 6 months | Cash runway, cure ability |
| Issuer default | Issuer stops coupon | Full stop | Coverage without coupon, insurance trigger |
| Insurance failure | Insurance payout | $0 | Recovery rate without insurance |

### 6.2 Stress Test Output Format

For each scenario, produce:
1. New LTV
2. New coverage ratio
3. Margin call amount (if triggered)
4. Days to default (if unable to cure)
5. Expected recovery rate and amount
6. Recommended action

---

## 7. RISK LIMITS

| Limit | Value | Rationale |
|:------|:------|:----------|
| Maximum single-counterparty exposure | $300M | Per institution cap from institutional package |
| Maximum aggregate facility | $2B | Total program capacity |
| Minimum coverage ratio | 200% | Standard ABL |
| Maximum LTV | 50% (hard cap) | Even Tier 1 capped at 50% |
| Minimum insurance coverage | $500M | Must exceed single-lender max exposure |
| Maximum tenor | 24 months | Reduces rollover risk |

---

## 8. POLICY GOVERNANCE

| Item | Frequency |
|:-----|:----------|
| Full policy review | Semi-annual |
| Haircut schedule review | Quarterly |
| Stress test execution | Quarterly |
| LTV monitoring | Per Section 2.3 |
| Recovery analysis update | Annual or after material event |

---

*Maintained by OPTKAS1 PMO. Effective upon Track B activation. Subject to counterparty negotiation on specific thresholds.*
