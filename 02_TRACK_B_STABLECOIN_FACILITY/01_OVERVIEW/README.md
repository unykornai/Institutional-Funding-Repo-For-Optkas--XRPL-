# Track B — Stablecoin-Funded Credit Facility

**Risk Rating:** 🟢 Low–Medium  
**Status:** Documents Staged  
**Priority:** **PRIMARY FALLBACK** — fastest path to alternative capital

---

## Purpose

Track B is a secured credit facility where the **funding rail is stablecoin** (USDC/USDT). The legal structure remains traditional — facility agreement, security agreement, covenants, reporting. Only the settlement mechanism uses on-chain rails, with bank wire as a permanent fallback.

**Critical distinction:** In Track B, the borrower does NOT issue anything. The borrower **receives** existing USDC/USDT from a capital provider.

---

## How It Works

1. Counterparty lends USDC/USDT to borrower's controlled wallet
2. Facility documented via traditional legal agreements
3. Borrower uses funds per permitted purposes
4. Borrower repays in stablecoin + interest
5. Collateral released upon full repayment

---

## Supported Chains (by priority)

| Chain | Asset | Rationale |
|:------|:------|:----------|
| Ethereum / Base | USDC | Cleanest institutional optics |
| Tron | USDT | Most liquid stablecoin market |
| XRPL | USDC/USDT equivalents | Depends on counterparty preference |

---

## Folder Structure

```
02_TRACK_B_STABLECOIN_FACILITY/
    01_OVERVIEW/          — This README + track summary
    02_LEGAL/             — Term sheet template, facility agreement skeleton
    03_COMPLIANCE/        — KYB/KYC, sanctions, source of funds
    04_TREASURY_CONTROLS/ — Wallet policy, signer matrix, allowlists
    05_SETTLEMENT_RUNBOOK/— Address exchange, test transfers, draw/repay procedures
    06_REPORTING/         — Daily/weekly reporting templates
    07_RISK_ENGINE/       — Haircuts, LTV, margin calls, liquidation
    08_COUNTERPARTY_PACKS/— Onboarding packs per counterparty type
    09_SIMULATIONS/       — Counterparty response scenarios
```

---

## Timeline (NDA → Funding)

| Phase | Days | Deliverables |
|:------|:-----|:------------|
| Counterparty Onboarding | 0–2 | KYB/KYC, NDA, wallet + signer matrix |
| Terms + Legal | 3–7 | Term sheet, facility + security docs |
| Controls + Settlement | 8–12 | Allowlisted addresses, test transfer, reporting cadence |
| Closing | 13–20 | Execute docs, control agreement, closing checklist |
| **Funding Event (T0)** | 20+ | USDC/USDT sent → receipt confirmed → reporting begins |

---

## Key Documents in This Track

| Document | Location | Status |
|:---------|:---------|:-------|
| Wallet Controls Policy | `04_TREASURY_CONTROLS/WALLET_CONTROLS_POLICY.md` | ✅ Ready |
| Term Sheet Template | `02_LEGAL/STABLECOIN_FACILITY_TERM_SHEET_TEMPLATE.md` | ✅ Ready |
| Settlement Runbook | `05_SETTLEMENT_RUNBOOK/SETTLEMENT_RUNBOOK.md` | ✅ Ready |
| Daily Reporting Template | `06_REPORTING/DAILY_REPORTING_TEMPLATE.md` | ✅ Ready |
| Risk Policy | `07_RISK_ENGINE/RISK_POLICY_HAIRCUTS_LTV_MARGIN.md` | ✅ Ready |

---

*Track B is the fastest path to alternative capital. All documents are staged and ready to deploy upon activation.*
