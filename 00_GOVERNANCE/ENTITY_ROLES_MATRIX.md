# Entity Roles Matrix — XRPL Parallel Execution Framework

**Version:** 1.0 | **Date:** February 9, 2026 | **Owner:** OPTKAS1 PMO

---

## Core Operating Entities (Borrower Controls)

| # | Role | Entity | Jurisdiction | Function | Contact |
|:--|:-----|:-------|:-------------|:---------|:--------|
| 1 | **Borrower SPV** | OPTKAS1 LLC | Wyoming, USA (File# 2025-001184729) | Signs facility agreement, receives/repays stablecoins, pledges collateral | jimmy@optkas.com |
| 2 | **Manager / Operator** | Unykorn 7777, Inc. | USA | Admin, reporting, controls, coordination, technology infrastructure | kevan@xxxiii.io |
| 3 | **Treasury Function** | Borrower-controlled | — | Wallet governance, dual-approval, allowlists, daily reporting | Internal |
| 4 | **Banking Partner** | [To be confirmed] | — | Fiat fallback rail, operating expenses, wire settlement | — |

---

## External Counterparties (Third Parties)

| # | Role | Entity | Function | Track Relevance |
|:--|:-----|:-------|:---------|:---------------|
| 5 | **Capital Provider / Lender** | [To be engaged] | Advances USDC/USDT or cash; facility agreement counterparty | B, B2 |
| 6 | **Custodian / Collateral Agent** | STC (existing) or third-party | Holds collateral, issues confirmations, runs control agreement | A, B |
| 7 | **Legal Counsel (Borrower)** | [To be engaged] | Drafts facility/security/control agreements, delivers opinions | All |
| 8 | **Legal Counsel (Lender)** | [Lender-appointed] | Diligence, redlines, closing conditions | B, C |
| 9 | **Compliance / KYB-KYC Vendor** | [To be engaged] | Company verification, UBO screening, sanctions, adverse media | All |
| 10 | **Blockchain Analytics** | [Optional] | Transaction monitoring, wallet risk scoring | B, D |
| 11 | **Exchange / OTC Desk** | [If conversion needed] | Stablecoin ↔ fiat conversion, block trades | B |
| 12 | **Auditor / Attestation** | [CPA firm] | Reserve attestation (Track D), periodic reporting review | D (required), B (recommended) |

---

## Entity Separation Rules

### Rule 1: Borrower SPV is the contracting party
All facility agreements, security agreements, and settlement instructions are signed by the Borrower SPV (OPTKAS1 LLC). The Manager/Operator acts only in an administrative and technology capacity.

### Rule 2: No entity in this framework is an issuer
Unless Track D is explicitly activated, no entity in this framework issues, creates, or mints any digital asset, token, or stablecoin. Track B involves **receiving** existing USDC/USDT only.

### Rule 3: Banking partner is always a fallback
Every track must maintain a fiat wire fallback path. No counterparty should be told "we can only settle on-chain."

### Rule 4: Custodian role is optional but recommended
For Track B (stablecoin facility), a custodian/collateral agent increases counterparty confidence but is not structurally required if wallet controls are documented.

### Rule 5: Track D requires a separate entity analysis
If Track D (XRPL issuer) is ever activated, a separate entity structure analysis must be completed. The issuing entity should ideally be distinct from the borrowing entity.

---

## Counterparty Types by Track

### Track B (Stablecoin Facility) — Target Counterparties

| Type | Description | Expected Comfort Level |
|:-----|:-----------|:----------------------|
| Private credit funds | Warehouse lines, bridge facilities | 🟢 High — familiar structure |
| Market makers / liquidity providers | Repo-style, margin-based | 🟢 High — native to stablecoin rails |
| Hedge funds / family offices | Structured notes, secured lending | 🟡 Medium — depends on crypto comfort |
| Bank structured finance desks | Traditional but exploring digital rails | 🟡 Medium — slowest but strongest |
| Crypto-native lenders | Fast underwriting, higher rates | 🟢 High — this is their core business |

### Track C (Tokenized Credit) — Target Counterparties

| Type | Description | Expected Comfort Level |
|:-----|:-----------|:----------------------|
| Innovation-focused funds | Digital asset strategies | 🟡 Medium |
| Trade finance platforms | Tokenized receivables experience | 🟡 Medium |

### Track D (XRPL Issuer) — Target Counterparties

| Type | Description | Expected Comfort Level |
|:-----|:-----------|:----------------------|
| Non-bank capital | Alternative investment structures | 🟠 Low initially |
| Innovation partners | R&D-stage capital | 🟠 Low initially |

---

*Maintained by OPTKAS1 PMO. Updated as counterparties are engaged.*
