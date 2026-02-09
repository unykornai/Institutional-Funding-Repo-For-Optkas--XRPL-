# Funds-Flow Architecture — Track B Stablecoin Facility

**Version:** 1.0 | **Date:** February 9, 2026 | **Owner:** OPTKAS1 PMO  
**Purpose:** Map every dollar movement from facility origination through repayment and termination.

---

## OVERVIEW

Two settlement rails operate in parallel. **Wire is always available as fallback.**

```
┌─────────────────────────────────────────────────────────────────────┐
│                    SETTLEMENT RAIL SELECTION                        │
│                                                                     │
│   PRIMARY (if counterparty supports):    Stablecoin (USDC/USDT)    │
│   FALLBACK (always available):           Bank Wire (USD)            │
│                                                                     │
│   Decision made during onboarding. Documented in Term Sheet.        │
│   Either rail may be used for any transaction with mutual consent.  │
└─────────────────────────────────────────────────────────────────────┘
```

---

## 1. FACILITY SETUP FLOW

```
                    ┌──────────────────────┐
                    │   TERM SHEET SIGNED   │
                    │   (Day 0)             │
                    └──────────┬───────────┘
                               │
                    ┌──────────▼───────────┐
                    │   LEGAL DOCS EXECUTE  │
                    │   • Facility Agreement│
                    │   • Security Agreement│
                    │   • Pledge Agreement  │
                    │   • ACA (with STC)    │
                    └──────────┬───────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
    ┌─────────▼──────┐ ┌──────▼──────┐ ┌───────▼────────┐
    │  UCC-1 FILED   │ │  INSURANCE  │ │   WALLET /     │
    │  Wyoming SoS   │ │  ENDORSED   │ │   BANK SETUP   │
    │  First-priority│ │  C.J.Coleman│ │                │
    │  lien confirmed│ │  Lender as  │ │  Stablecoin:   │
    │                │ │  loss payee │ │  Exchange addr  │
    └────────┬───────┘ └──────┬──────┘ │  Test transfer │
             │                │        │                │
             │                │        │  Wire:         │
             │                │        │  Bank acct     │
             │                │        │  verified      │
             └────────┬───────┘        └───────┬────────┘
                      │                        │
                      └───────────┬────────────┘
                                  │
                    ┌─────────────▼──────────────┐
                    │   ALL CPs SATISFIED         │
                    │   Closing Certificate Issued│
                    │   FACILITY IS LIVE          │
                    └─────────────┬──────────────┘
                                  │
                                  ▼
                         ┌────────────────┐
                         │  OPERATIONS    │
                         │  BEGIN         │
                         └────────────────┘
```

---

## 2. DRAWDOWN FLOW — STABLECOIN (PRIMARY)

```
                         BORROWER                              LENDER
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 1. Submit Drawdown   │                                     │
     │    Request            │──── Drawdown Request Form ────────►│
     │    (email + signed)   │     (amount, wallet, purpose)      │
     └──────────────────────┤                                     │
                            │                              ┌──────┤
                            │                              │ 2.   │
                            │                              │ Verify│
                            │                              │ - BorrowingBase│
                            │                              │ - Coverage ≥250%│
                            │                              │ - No EOD│
                            │                              │ - Wallet on│
                            │                              │   allowlist│
                            │                              └──────┤
                            │                                     │
                            │         USDC/USDT Transfer          │
                            │◄────────────────────────────────────│
                            │     3. Lender sends to              │
     ┌──────────────────────┤        Treasury Wallet              │
     │ 4. Confirm receipt   │        (on-chain tx)                │
     │    Issue Receipt Memo│                                     │
     │    (tx hash, amount, │──── Receipt Memo ──────────────────►│
     │     timestamp)       │                                     │
     └──────────────────────┤                                     │
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 5. Transfer to       │                                     │
     │    Operations Wallet │                                     │
     │    (internal move)   │                                     │
     └──────────────────────┤                                     │
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 6. Deploy funds per  │                                     │
     │    Use of Proceeds   │                                     │
     │    (convert to USD   │                                     │
     │     via bank or OTC) │                                     │
     └──────────────────────┤                                     │
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 7. Daily Report      │──── Daily Report ─────────────────►│
     │    (balances, txns,  │     (wallet balances, coverage,     │
     │     covenants)       │      covenant status)               │
     └──────────────────────┤                                     │
```

---

## 3. DRAWDOWN FLOW — WIRE (FALLBACK)

```
                         BORROWER                              LENDER
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 1. Submit Drawdown   │──── Drawdown Request Form ────────►│
     │    Request (wire)    │     (amount, bank acct, purpose)    │
     └──────────────────────┤                                     │
                            │                              ┌──────┤
                            │                              │ 2.   │
                            │                              │ Verify│
                            │                              │ (same │
                            │                              │ checks)│
                            │                              └──────┤
                            │                                     │
                            │          USD Wire Transfer          │
                            │◄────────────────────────────────────│
                            │     3. Lender wires to              │
     ┌──────────────────────┤        EagleBank Account            │
     │ 4. Confirm receipt   │        (Bethesda, MD)               │
     │    via bank statement│                                     │
     │    Issue Receipt Memo│──── Receipt Memo ──────────────────►│
     └──────────────────────┤                                     │
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 5. Deploy funds per  │                                     │
     │    Use of Proceeds   │                                     │
     └──────────────────────┤                                     │
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 6. Daily Report      │──── Daily Report ─────────────────►│
     └──────────────────────┤                                     │
```

---

## 4. REPAYMENT FLOW — STABLECOIN

```
                         BORROWER                              LENDER
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 1. Acquire USDC/USDT │                                     │
     │    (OTC desk or      │                                     │
     │     exchange)         │                                     │
     └──────────────────────┤                                     │
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 2. Fund Repayment    │                                     │
     │    Wallet             │                                     │
     │    (internal transfer)│                                     │
     └──────────────────────┤                                     │
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 3. Send scheduled    │                                     │
     │    payment            │                                     │
     │    (principal +       │         USDC/USDT Transfer         │
     │     interest)         │────────────────────────────────────►│
     │                      │     To: Lender Designated Wallet    │
     └──────────────────────┤                                     │
                            │                              ┌──────┤
                            │                              │ 4.   │
                            │                              │ Confirm│
                            │     Payment Confirmation     │ receipt│
                            │◄────────────────────────────────────│
                            │                              └──────┤
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 5. Update facility   │                                     │
     │    ledger             │                                     │
     │    (outstanding bal,  │──── Updated Statement ────────────►│
     │     coverage ratio)   │                                     │
     └──────────────────────┤                                     │
```

---

## 5. REPAYMENT FLOW — WIRE (FALLBACK)

```
                         BORROWER                              LENDER
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 1. Fund from         │                                     │
     │    EagleBank account  │                                     │
     └──────────────────────┤                                     │
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 2. Initiate wire     │         USD Wire Transfer           │
     │    (principal +       │────────────────────────────────────►│
     │     interest)         │     To: Lender Bank Account        │
     └──────────────────────┤                                     │
                            │                              ┌──────┤
                            │     Payment Confirmation     │ 3.   │
                            │◄─────────────────────────────│Confirm│
                            │                              └──────┤
                            │                                     │
     ┌──────────────────────┤                                     │
     │ 4. Update facility   │──── Updated Statement ────────────►│
     │    ledger             │                                     │
     └──────────────────────┤                                     │
```

---

## 6. END-TO-END LIFECYCLE

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                         FACILITY LIFECYCLE                                       │
│                                                                                 │
│  ORIGINATION          OPERATIONS             MATURITY / TERMINATION             │
│  ───────────          ──────────             ──────────────────────             │
│                                                                                 │
│  ┌───────────┐   ┌─────────────────┐   ┌──────────────────────────┐            │
│  │ Onboarding│   │ Draw / Repay    │   │ Final Repayment          │            │
│  │ KYB/KYC   │   │ Cycle           │   │ (all principal + accrued │            │
│  │ Compliance│   │                 │   │  interest + fees)        │            │
│  │ Legal Docs│──►│ Daily Reporting │──►│                          │            │
│  │ Settlement│   │ Covenant Monitor│   │ OR Refinance             │            │
│  │ Setup     │   │ Coverage Check  │   │ (new facility replaces)  │            │
│  │ Test Xfer │   │ Margin Calls    │   │                          │            │
│  │ Close     │   │ (if triggered)  │   │ OR Default               │            │
│  └───────────┘   └─────────────────┘   │ (enforcement begins)     │            │
│                                        └──────────────────────────┘            │
│       10-25 BD        Ongoing (6-36 mo)       Per Term Sheet                   │
│                                                                                 │
└─────────────────────────────────────────────────────────────────────────────────┘
```

---

## 7. DEFAULT & ENFORCEMENT FLOW

```
         EVENT OF DEFAULT TRIGGERED
                    │
                    ▼
    ┌───────────────────────────────┐
    │  LENDER DELIVERS NOTICE OF   │
    │  DEFAULT TO BORROWER         │
    │  (via registered mail + email)│
    └──────────────┬────────────────┘
                   │
                   ▼
    ┌───────────────────────────────┐
    │  CURE PERIOD                  │
    │  5 Business Days (payment)    │
    │  10 Business Days (covenant)  │
    │  Immediate (fraud/insolvency) │
    └──────────────┬────────────────┘
                   │
          ┌────────┴────────┐
          │                 │
    ┌─────▼─────┐    ┌─────▼──────────────────┐
    │  CURED    │    │  NOT CURED              │
    │  Facility │    │  Lender may:            │
    │  continues│    │                         │
    └───────────┘    │  1. Accelerate all      │
                     │     outstanding amounts  │
                     │                         │
                     │  2. Exercise rights      │
                     │     under Security Agmt  │
                     │                         │
                     │  3. Direct STC to        │
                     │     transfer collateral  │
                     │     (per ACA)            │
                     │                         │
                     │  4. File insurance claim │
                     │     (C.J. Coleman)       │
                     │                         │
                     │  5. Pursue legal         │
                     │     remedies (NY law)    │
                     └─────────────────────────┘

         ┌─────────────────────────────────┐
         │  RECOVERY WATERFALL             │
         │                                 │
         │  1. Collateral liquidation      │
         │     (500 notes, face $5B)       │
         │                                 │
         │  2. Insurance proceeds          │
         │     (C.J. Coleman, $625M)       │
         │                                 │
         │  3. Guarantor assets            │
         │     (if personal guarantee)     │
         │                                 │
         │  4. Entity assets               │
         │     (OPTKAS1 LLC)               │
         │                                 │
         │  5. Legal judgment              │
         │     (court-ordered)             │
         └─────────────────────────────────┘
```

---

## 8. WALLET ARCHITECTURE

```
    ┌─────────────────────────────────────────────────────────┐
    │                    BORROWER WALLETS                      │
    │                                                         │
    │   ┌──────────────┐    ┌──────────────┐                 │
    │   │  TREASURY    │    │  OPERATIONS  │                 │
    │   │  WALLET      │    │  WALLET      │                 │
    │   │              │    │              │                 │
    │   │  Receives    │───►│  Day-to-day  │                 │
    │   │  all inbound │    │  disbursement│                 │
    │   │  from lender │    │              │                 │
    │   │              │    │  Max: $500K  │                 │
    │   │  Dual-sign   │    │  per day     │                 │
    │   │  required    │    │              │                 │
    │   └──────────────┘    └──────────────┘                 │
    │                                                         │
    │   ┌──────────────┐    ┌──────────────┐                 │
    │   │  REPAYMENT   │    │  COLD        │                 │
    │   │  WALLET      │    │  STORAGE     │                 │
    │   │              │    │              │                 │
    │   │  Funded for  │    │  Emergency   │                 │
    │   │  scheduled   │    │  reserve     │                 │
    │   │  payments    │    │              │                 │
    │   │              │    │  Offline     │                 │
    │   │  Outbound to │    │  3-of-5      │                 │
    │   │  lender only │    │  multisig    │                 │
    │   └──────────────┘    └──────────────┘                 │
    │                                                         │
    └─────────────────────────────────────────────────────────┘

    ┌─────────────────────────────────────────────────────────┐
    │                    LENDER WALLETS                        │
    │                                                         │
    │   ┌──────────────┐    ┌──────────────┐                 │
    │   │  FUNDING     │    │  COLLECTION  │                 │
    │   │  WALLET      │    │  WALLET      │                 │
    │   │              │    │              │                 │
    │   │  Sends draws │    │  Receives    │                 │
    │   │  to borrower │    │  repayments  │                 │
    │   │  treasury    │    │  from        │                 │
    │   │              │    │  borrower    │                 │
    │   └──────────────┘    └──────────────┘                 │
    │                                                         │
    └─────────────────────────────────────────────────────────┘
```

---

## 9. REPORTING LOOP

```
    ┌──────────┐                                    ┌──────────┐
    │          │   DAILY (by 10 AM ET):             │          │
    │          │   • Wallet balances                │          │
    │          │   • Transaction log                │          │
    │ BORROWER │   • Coverage ratio                 │  LENDER  │
    │          │   • Covenant snapshot               │          │
    │          │──────────────────────────────────►  │          │
    │          │                                    │          │
    │          │   WEEKLY (Friday by 5 PM ET):      │          │
    │          │   • Draw/repay summary             │          │
    │          │   • Collateral movement            │          │
    │          │──────────────────────────────────►  │          │
    │          │                                    │          │
    │          │   MONTHLY (5th BD):                │          │
    │          │   • Full facility statement        │          │
    │          │   • Borrowing Base Certificate     │          │
    │          │   • Covenant compliance cert       │          │
    │          │   • Insurance confirmation         │          │
    │          │──────────────────────────────────►  │          │
    │          │                                    │          │
    │          │   QUARTERLY (15th BD):             │          │
    │          │   • Collateral revaluation         │          │
    │          │   • Stress test results            │          │
    │          │   • Financial statements           │          │
    │          │──────────────────────────────────►  │          │
    │          │                                    │          │
    └──────────┘                                    └──────────┘
```

---

## 10. BANK ↔ STABLECOIN CONVERSION POINTS

```
    FIAT WORLD                          STABLECOIN WORLD
    ──────────                          ────────────────

    ┌──────────────┐                    ┌──────────────┐
    │  EAGLEBANK   │                    │  TREASURY    │
    │  (Bethesda)  │                    │  WALLET      │
    │              │    ┌──────────┐    │              │
    │  USD Account │───►│ OTC DESK │───►│  USDC/USDT  │
    │              │    │ or       │    │              │
    │              │◄───│ Exchange │◄───│              │
    │              │    └──────────┘    │              │
    └──────────────┘                    └──────────────┘

    CONVERSION RULES:
    ─────────────────
    • All fiat-to-stablecoin conversions via licensed OTC desk or exchange
    • Borrower bears conversion cost (typically 5-15 bps)
    • Conversion must complete within same business day
    • Conversion records retained for 7 years
    • Preferred partners: [To be determined during onboarding]
    
    SUPPORTED CHAINS & TOKENS:
    ──────────────────────────
    ┌────────────────┬──────────────┬────────────────┐
    │ Token          │ Chain        │ Priority       │
    ├────────────────┼──────────────┼────────────────┤
    │ USDC           │ Ethereum     │ 1st (default)  │
    │ USDC           │ Base         │ 2nd            │
    │ USDT           │ Tron         │ 3rd            │
    │ USDT           │ Ethereum     │ 4th            │
    │ RLUSD / equiv  │ XRPL         │ Future (Track  │
    │                │              │ enhancement)   │
    └────────────────┴──────────────┴────────────────┘
```

---

## KEY CONTACTS FOR FUND FLOW OPERATIONS

| Function | Entity | Contact |
|:---------|:-------|:--------|
| Borrower Manager | OPTKAS1 LLC | Jimmy (jimmy@optkas.com) |
| Infrastructure | Unykorn 7777, Inc. | Kevan (kevan@xxxiii.io) |
| Custodian | Securities Transfer Corp | Operations Desk |
| Banking | EagleBank | Relationship Manager |
| Insurance | C.J. Coleman & Co Ltd | Claims / Endorsement Desk |
| Legal (Borrower) | K. Knowles & Co. | Lead Partner |

---

*This document is for internal planning only. Customize for each counterparty based on their preferred settlement rail.*
