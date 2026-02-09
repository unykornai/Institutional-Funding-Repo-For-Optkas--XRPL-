# TRACK B — ACTIVATION PLAYBOOK

**Entity:** OPTKAS1 LLC  
**Prepared by:** Unykorn 7777, Inc.  
**Date:** February 9, 2026  
**Classification:** 🟠 STRATEGIC — Operational Execution Guide  
**Status:** 🔴 NOT ACTIVATED — For planning purposes only

---

## Purpose

This is the step-by-step operational playbook for activating Track B (Stablecoin Facility). It covers the complete activation sequence from board authorization through first funding, including counterparty targeting, outreach strategy, and expected terms.

**Track B activates ONLY when:**
- Track A has stalled for 60+ business days, OR
- Board/Management explicitly authorizes parallel execution, OR
- Market conditions require faster deployment of capital

---

## TABLE OF CONTENTS

| # | Section | Priority |
|:--|:--------|:---------|
| 1 | [Activation Prerequisites](#1-activation-prerequisites) | 🔴 CORE |
| 2 | [7-Day Activation Sequence](#2-7-day-activation-sequence) | 🔴 CORE |
| 3 | [Counterparty Targeting Framework](#3-counterparty-targeting-framework) | 🟠 STRATEGIC |
| 4 | [Expected Terms Matrix](#4-expected-terms-matrix) | 🟠 STRATEGIC |
| 5 | [Outreach Sequence](#5-outreach-sequence) | 🟡 OPERATIONAL |
| 6 | [Track B as Bridge to Track A](#6-track-b-as-bridge-to-track-a) | 🟠 STRATEGIC |
| 7 | [Risk Management](#7-risk-management) | 🔴 CORE |
| 8 | [Timeline to First Funding](#8-timeline-to-first-funding) | 🟡 OPERATIONAL |

---

## 1. Activation Prerequisites

### Before Activating Track B — Complete This Checklist

```
╔══════════════════════════════════════════════════════════════════════════╗
║  ACTIVATION PREREQUISITES                                              ║
║                                                                        ║
║  □ Board/Manager has signed ACTIVATION_DECISION_MEMO.md               ║
║  □ Track A status documented (stalled/delayed/parallel decision)       ║
║  □ Legal counsel notified of Track B activation                        ║
║  □ STC custody posture confirmed (no changes to collateral)            ║
║  □ Compliance package current (KYB/KYC/AML within 30 days)            ║
║  □ Wallet infrastructure vendor selected (Fireblocks or BitGo)         ║
║  □ OTC desk relationship established (Galaxy Digital or Cumberland)    ║
║  □ Banking partner notified of potential stablecoin settlement          ║
║                                                                        ║
╚══════════════════════════════════════════════════════════════════════════╝
```

### Activation Authority Matrix

| Action | Who Approves | Document |
|:-------|:------------|:---------|
| Activate Track B | Manager (Jimmy) | ACTIVATION_DECISION_MEMO.md |
| Deploy wallets | Operator (Unykorn 7777) | WALLET_CONTROLS_POLICY.md |
| First counterparty outreach | Manager + Operator jointly | This playbook |
| Sign term sheet | Manager (as authorized signer) | STABLECOIN_FACILITY_TERM_SHEET_TEMPLATE.md |
| Accept first draw | Manager + dual-signature wallet | SETTLEMENT_RUNBOOK.md |

---

## 2. 7-Day Activation Sequence

### Day-by-Day Execution Plan

```
════════════════════════════════════════════════════════════════════════════
  DAY 0 — AUTHORIZATION
════════════════════════════════════════════════════════════════════════════

  ┌─────────────────────────────────────────────────────────────────────┐
  │  □ Manager signs ACTIVATION_DECISION_MEMO.md                       │
  │  □ Document reason for activation:                                 │
  │    ○ Track A stalled (specify reason)                              │
  │    ○ Market timing opportunity                                     │
  │    ○ Strategic parallel execution decision                         │
  │  □ Notify legal counsel                                            │
  │  □ Confirm no change to institutional lane messaging               │
  │                                                                     │
  │  DELIVERABLE: Signed activation memo                               │
  └─────────────────────────────────────────────────────────────────────┘

════════════════════════════════════════════════════════════════════════════
  DAY 1–2 — INFRASTRUCTURE SETUP
════════════════════════════════════════════════════════════════════════════

  ┌─────────────────────────────────────────────────────────────────────┐
  │  □ Lock wallet controls per WALLET_CONTROLS_POLICY.md              │
  │    ○ Deploy 4-wallet architecture (Collection, Treasury,           │
  │      Operations, Reserve)                                          │
  │    ○ Configure dual-signature requirements                         │
  │    ○ Set daily/weekly transaction limits                            │
  │  □ Finalize compliance package for Track B counterparties          │
  │  □ Stage SETTLEMENT_RUNBOOK.md for execution                       │
  │  □ Activate DAILY_REPORTING_TEMPLATE.md                            │
  │  □ Confirm OTC desk relationship (stablecoin on/off ramp)          │
  │                                                                     │
  │  DELIVERABLE: Operational wallet infrastructure + compliance pack  │
  └─────────────────────────────────────────────────────────────────────┘

════════════════════════════════════════════════════════════════════════════
  DAY 3–4 — COUNTERPARTY IDENTIFICATION
════════════════════════════════════════════════════════════════════════════

  ┌─────────────────────────────────────────────────────────────────────┐
  │  □ Identify 5–7 Track B counterparties (see Section 3)             │
  │    ○ Minimum 2 per category recommended                            │
  │    ○ Priority: Market Makers > Crypto Credit > International       │
  │  □ Prepare customized FACILITY_OVERVIEW_1PAGER.md per counterparty │
  │  □ Customize ONBOARDING_CHECKLIST.md per counterparty type         │
  │  □ Stage compliance documentation for rapid deployment             │
  │  □ Prepare term sheet negotiation positions                        │
  │                                                                     │
  │  DELIVERABLE: Target list + customized materials                   │
  └─────────────────────────────────────────────────────────────────────┘

════════════════════════════════════════════════════════════════════════════
  DAY 5–7 — OUTREACH BEGINS
════════════════════════════════════════════════════════════════════════════

  ┌─────────────────────────────────────────────────────────────────────┐
  │  □ Direct outreach to top 3 counterparties                         │
  │  □ Send FACILITY_OVERVIEW_1PAGER.md + compliance snapshot          │
  │  □ Schedule first diligence calls                                  │
  │  □ Run internal war game (CREDIT_COMMITTEE_WAR_GAME.md)            │
  │  □ Begin daily tracking of counterparty engagement                 │
  │                                                                     │
  │  DELIVERABLE: Active pipeline with 3+ engaged counterparties       │
  └─────────────────────────────────────────────────────────────────────┘
```

### Post Day 7 — Path to Closing

```
    DAY 7–10 ──► Initial diligence calls completed
                  Counterparty Q&A resolved
                  Internal pricing analysis

    DAY 10–15 ──► Indicative term sheet received
                   Internal review + negotiation
                   Legal markup begins

    DAY 15–25 ──► Legal documentation finalized
                   Security agreement executed
                   Wallet controls confirmed by counterparty

    DAY 25–35 ──► Test settlement (small amount)
                   Verify settlement mechanics
                   Final compliance clearance

    DAY 30–45 ──► ⚡ FIRST FUNDING
                   Full draw per term sheet
                   Daily reporting activated
                   Margin monitoring live
```

---

## 3. Counterparty Targeting Framework

### Who Track B Is For

```
╔══════════════════════════════════════════════════════════════════════════╗
║                                                                        ║
║  CATEGORY 1: CRYPTO-NATIVE CREDIT FUNDS                               ║
║  ──────────────────────────────────────                                 ║
║                                                                        ║
║  Profile:    Structured credit desks with USDC/USDT balance sheets    ║
║  Why them:   Already comfortable with stablecoin settlement            ║
║  Size:       $25M – $75M per tranche                                   ║
║  Speed:      30–60 BD to close                                         ║
║  Pricing:    SOFR + 600–800 bps                                        ║
║  Key need:   Conservative LTV, transparent reporting, clean docs       ║
║                                                                        ║
╠══════════════════════════════════════════════════════════════════════════╣
║                                                                        ║
║  CATEGORY 2: MARKET MAKERS / OTC BALANCE SHEETS                       ║
║  ──────────────────────────────────────────────                         ║
║                                                                        ║
║  Profile:    Firms that warehouse risk, run OTC desks                  ║
║  Why them:   FASTEST path to capital — decision makers, not committees ║
║  Size:       $10M – $50M per tranche                                   ║
║  Speed:      ⚡ 10–15 BD to close (fastest lane)                      ║
║  Pricing:    SOFR + 800–1000 bps (premium for speed)                   ║
║  Key need:   Escrow controls, daily reporting, clear collateral        ║
║                                                                        ║
╠══════════════════════════════════════════════════════════════════════════╣
║                                                                        ║
║  CATEGORY 3: INTERNATIONAL FUNDS (NON-US BANKS)                       ║
║  ──────────────────────────────────────────────                         ║
║                                                                        ║
║  Profile:    Non-US lenders comfortable with hybrid structures         ║
║  Why them:   More flexible settlement rails, less SPV-age sensitive    ║
║  Size:       $15M – $50M per tranche                                   ║
║  Speed:      20–45 BD to close                                         ║
║  Pricing:    SOFR + 500–700 bps                                        ║
║  Key need:   Compliance package (FATF, travel rule), NY governing law  ║
║                                                                        ║
╠══════════════════════════════════════════════════════════════════════════╣
║                                                                        ║
║  CATEGORY 4: FAMILY OFFICES WITH CRYPTO/DIGITAL MANDATE               ║
║  ──────────────────────────────────────────────────────                  ║
║                                                                        ║
║  Profile:    Single/multi-family offices with digital asset allocation ║
║  Why them:   Faster decision-making, fewer committee layers            ║
║  Size:       $5M – $25M per tranche                                    ║
║  Speed:      15–30 BD to close                                         ║
║  Pricing:    SOFR + 700–900 bps                                        ║
║  Key need:   Conservative structure, transparency, wallet controls     ║
║                                                                        ║
╚══════════════════════════════════════════════════════════════════════════╝
```

### Who Track B is NOT For (Do NOT Contact)

```
╔══════════════════════════════════════════════════════════════════════════╗
║  ❌ TRACK A COUNTERPARTIES — NEVER OFFER TRACK B TO:                  ║
║                                                                        ║
║  • Ares Management          • Apollo Global                           ║
║  • KKR Credit               • HPS Partners                           ║
║  • Fortress Investment      • Stonebriar Commercial                   ║
║  • Oaktree Capital          • Cerberus Capital                        ║
║  • Any regulated bank (Standard Chartered, Deutsche, etc.)            ║
║  • Any lender from the Wave 1 institutional package                   ║
║                                                                        ║
║  RULE: If they have a bank charter, bank-adjacent compliance,         ║
║  or traditional fund governance → Track A ONLY.                       ║
║                                                                        ║
╚══════════════════════════════════════════════════════════════════════════╝
```

---

## 4. Expected Terms Matrix

### Track B vs. Track A Comparison

| Dimension | Track A (Institutional) | Track B (Stablecoin) |
|:----------|:----------------------|:--------------------|
| **Facility Size** | $75M–$300M | $25M–$75M |
| **Advance Rate** | 40% LTV | 30%–40% LTV |
| **Pricing** | SOFR + 200–400 bps | SOFR + 600–1000 bps |
| **Tenor** | 2–5 years | 6–12 months |
| **Settlement** | Wire only | USDC/USDT + wire fallback |
| **Reporting** | Monthly | Daily |
| **Covenants** | Standard ABL | Standard ABL + wallet controls |
| **Collateral** | TC Notes at STC | TC Notes at STC (same) |
| **Governing Law** | New York | New York (same) |
| **Time to Close** | 60–120 BD | 10–45 BD |
| **Committee Process** | Full credit committee | Principal decision |
| **Cost of Capital** | Lower | Higher |
| **Speed** | Slower | ⚡ Faster |

### Key Insight

> Track B costs more but funds faster. It is **bridge capital**, not replacement capital. Use it to prove execution, then leverage that track record to close Track A at better terms.

---

## 5. Outreach Sequence

### Contact Protocol

```
┌─────────────────────────────────────────────────────────────────────────┐
│  STEP 1: WARM INTRODUCTION                                             │
│                                                                         │
│  • Use existing network connections                                     │
│  • Do NOT cold-email                                                    │
│  • Frame as: "Structured credit opportunity, stablecoin settlement"    │
│  • Send: Facility Overview 1-Pager ONLY (not full documentation)       │
│                                                                         │
├─────────────────────────────────────────────────────────────────────────┤
│  STEP 2: INITIAL CALL (15-20 min)                                      │
│                                                                         │
│  Cover:                                                                 │
│  • Collateral overview ($5B face, $3B cost, Lloyd's insured)           │
│  • Conservative advance rate (30-40% LTV)                               │
│  • Settlement mechanics (USDC/USDT, dual-signature wallets)            │
│  • Daily reporting framework                                            │
│  • Ask: "Does this fit your mandate?"                                  │
│                                                                         │
├─────────────────────────────────────────────────────────────────────────┤
│  STEP 3: DILIGENCE PACK                                                │
│                                                                         │
│  If interest confirmed, send:                                           │
│  • COMPLIANCE_PACKAGE.md (KYB/KYC/AML)                                 │
│  • WALLET_CONTROLS_POLICY.md                                            │
│  • SETTLEMENT_RUNBOOK.md                                                │
│  • RISK_POLICY_HAIRCUTS_LTV_MARGIN.md                                   │
│  • STABLECOIN_FACILITY_TERM_SHEET_TEMPLATE.md                           │
│                                                                         │
├─────────────────────────────────────────────────────────────────────────┤
│  STEP 4: TERM SHEET NEGOTIATION                                        │
│                                                                         │
│  • Negotiate on: pricing, advance rate, reporting frequency             │
│  • Do NOT negotiate on: collateral structure, governing law, custody    │
│  • Target: signed term sheet within 10-15 BD of first contact           │
│                                                                         │
├─────────────────────────────────────────────────────────────────────────┤
│  STEP 5: DOCUMENTATION + CLOSING                                       │
│                                                                         │
│  • Security agreement execution                                         │
│  • Wallet setup + test settlement                                       │
│  • Final compliance clearance                                           │
│  • First draw                                                           │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

### Language Guide — What To Say and What NOT To Say

| ✅ Say This | ❌ Never Say This |
|:-----------|:-----------------|
| "Secured credit facility" | "Crypto loan" |
| "Alternative settlement rail" | "Blockchain-based funding" |
| "Stablecoin settlement" | "DeFi lending" |
| "Digital settlement infrastructure" | "On-chain credit" |
| "Designated account" | "Wallet" (in formal docs) |
| "Reconciliation platform" | "XRPL" (in initial conversations) |
| "Borrower's controlled account" | "Cold wallet" |

---

## 6. Track B as Bridge to Track A

### The Bridge Strategy

```
╔══════════════════════════════════════════════════════════════════════════╗
║                                                                        ║
║  Track B is NOT a replacement for Track A.                             ║
║  Track B is the BRIDGE to Track A.                                     ║
║                                                                        ║
║  Here's how:                                                            ║
║                                                                        ║
║  1. Fund $25M–$50M via Track B (fast, 30–45 BD)                       ║
║  2. Execute flawlessly (daily reporting, zero incidents)               ║
║  3. Build 90-day track record of performance                            ║
║  4. Present to Track A lenders: "We've already executed."              ║
║  5. Track A closes faster because execution risk is PROVEN             ║
║                                                                        ║
║  Many institutional deals ONLY close after a smaller,                  ║
║  faster tranche proves execution capability.                           ║
║                                                                        ║
╚══════════════════════════════════════════════════════════════════════════╝
```

### Track B → Track A Acceleration

```
    WITHOUT TRACK B:                      WITH TRACK B:
    ┌──────────────────┐                  ┌──────────────────┐
    │                  │                  │                  │
    │ Track A: 90-120  │                  │ Track B: 30-45   │
    │ BD to close      │                  │ BD to first draw │
    │                  │                  │       │          │
    │ Risk: "Unproven  │                  │       ▼          │
    │ borrower"        │                  │ Track A: 60-90   │
    │                  │                  │ BD to close      │
    │                  │                  │ (accelerated)    │
    │                  │                  │                  │
    │ Total: 90-120 BD │                  │ Total: 60-90 BD  │
    └──────────────────┘                  └──────────────────┘
```

---

## 7. Risk Management

### Track B Specific Risks

| Risk | Severity | Mitigation |
|:-----|:---------|:-----------|
| Stablecoin depeg event | 🟠 Medium | Wire fallback clause, 24-hour conversion right |
| Wallet compromise | 🔴 High | Dual-signature, Fireblocks/BitGo MPC, cold storage reserve |
| Regulatory action on stablecoins | 🟡 Low-Medium | NY governing law, wire conversion clause, bank backup |
| Counterparty default | 🟠 Medium | Conservative LTV (30-40%), daily margin monitoring |
| Reputational cross-contamination | 🟡 Low | Strict lane separation, different counterparty sets |
| Settlement delay | 🟡 Low | USDC/USDT on major chains, OTC desk relationship |

### Firewall Between Lanes

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                         │
│  Track A Counterparties ◄──── FIREWALL ────► Track B Counterparties   │
│                                                                         │
│  • Different contact lists                                              │
│  • Different outreach materials                                         │
│  • Different email threads                                              │
│  • Different legal counsel teams                                        │
│  • Different positioning language                                       │
│  • ZERO overlap in communications                                       │
│                                                                         │
│  If a Track A lender asks about Track B:                                │
│  → "We have documented internal controls and reporting infrastructure.  │
│     It's dormant. It doesn't affect your facility."                    │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## 8. Timeline to First Funding

### Optimistic Path (Market Maker / OTC)

```
    Day 0  ──► Activation authorized
    Day 2  ──► Wallet infrastructure live
    Day 3  ──► Outreach begins
    Day 5  ──► First call completed
    Day 8  ──► Indicative term sheet
    Day 12 ──► Legal documentation
    Day 15 ──► Test settlement
    Day 18 ──► ⚡ FIRST FUNDING ($10M–$25M)
```

### Standard Path (Crypto Credit Fund)

```
    Day 0  ──► Activation authorized
    Day 2  ──► Wallet infrastructure live
    Day 4  ──► Outreach begins
    Day 10 ──► First diligence call
    Day 15 ──► Indicative term sheet
    Day 25 ──► Legal documentation
    Day 35 ──► Test settlement
    Day 40 ──► ⚡ FIRST FUNDING ($25M–$50M)
```

### Conservative Path (International Fund)

```
    Day 0  ──► Activation authorized
    Day 2  ──► Wallet infrastructure live
    Day 5  ──► Outreach begins
    Day 12 ──► First diligence call
    Day 20 ──► Indicative term sheet
    Day 35 ──► Legal documentation
    Day 42 ──► Test settlement + compliance
    Day 50 ──► ⚡ FIRST FUNDING ($15M–$50M)
```

---

## Status

| Item | State |
|:-----|:------|
| **Playbook Status** | 📋 Staged — NOT activated |
| **Board Authorization** | ⏳ Pending (unsigned) |
| **Wallet Infrastructure** | 📋 Vendor selected, not deployed |
| **Counterparty List** | 📋 Categories defined, names TBD |
| **Track A Status** | 🟢 Active — continues as primary |

---

*Maintained by OPTKAS1 LLC. Contact jimmy@optkas.com for activation authorization.*
