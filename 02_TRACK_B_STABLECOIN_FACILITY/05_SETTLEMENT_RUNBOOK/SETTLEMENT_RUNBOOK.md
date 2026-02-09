# Settlement Runbook — Stablecoin Facility (Track B)

**Version:** 1.0 | **Date:** February 9, 2026 | **Owner:** OPTKAS1 PMO  
**Applies To:** All stablecoin-based settlement under Track B

---

## 1. PRE-SETTLEMENT SETUP

### 1.1 Address Exchange Protocol

Before any value transfer, both parties must complete:

| Step | Action | Owner | Verification |
|:-----|:-------|:------|:------------|
| 1 | Borrower provides wallet address(es) + chain + asset | Borrower | Signed letter on entity letterhead |
| 2 | Lender provides wallet address(es) + chain + asset | Lender | Signed letter on entity letterhead |
| 3 | Both parties verify addresses independently | Both | Phone/video call confirmation (not email alone) |
| 4 | Addresses added to respective allowlists | Both | Per Wallet Controls Policy |
| 5 | Address verification recorded in settlement file | Borrower | Filed in `02_LEGAL/` |

### 1.2 Chain Selection

| Priority | Chain | Asset | When to Use |
|:---------|:------|:------|:-----------|
| 1 | Ethereum / Base | USDC | Default — best institutional optics |
| 2 | Tron | USDT | If counterparty prefers or for liquidity reasons |
| 3 | XRPL | USDC/USDT equivalent | Only if counterparty explicitly requests |
| Fallback | Bank wire (USD) | USD | Chain outage, counterparty preference, or regulatory concern |

### 1.3 Test Transfer (Mandatory)

Before the first real transaction:

1. Borrower sends $100 equivalent to Lender address
2. Lender confirms receipt (out-of-band: call or secure message)
3. Lender sends $100 equivalent to Borrower address
4. Borrower confirms receipt
5. Both log transaction hashes
6. Test transfer completion recorded in settlement file

---

## 2. DRAWDOWN PROCEDURE

### 2.1 Drawdown Request

| Step | Action | Owner | Timeline |
|:-----|:-------|:------|:---------|
| 1 | Borrower submits Drawdown Request (amount, purpose, wallet address) | Borrower | T-1 BD minimum |
| 2 | Lender verifies: coverage ratio OK, no default, covenants satisfied | Lender | Same day |
| 3 | Lender approves or rejects (with reason) | Lender | Same day |
| 4 | Lender sends stablecoin to Borrower's Treasury Wallet | Lender | T0 (draw date) |
| 5 | Borrower confirms receipt + issues Receipt Memo | Borrower | Within 2 hours of receipt |
| 6 | Borrower updates Daily Balance Report | Borrower | Same day |

### 2.2 Drawdown Request Format

```
DRAWDOWN REQUEST
Date: [DATE]
From: OPTKAS1 LLC (Borrower)
To: [Lender Name]

Requested Amount: [AMOUNT] [USDC/USDT]
Chain: [Ethereum / Base / Tron]
Receiving Wallet: [ADDRESS]
Purpose: [Permitted use description]
Borrowing Base Availability: $[AMOUNT] (per most recent BBC)
Coverage Ratio Post-Draw: [XXX]%

Authorized By: [Signer 1 Name]
Co-Approved By: [Signer 2 Name]
```

### 2.3 Receipt Memo Format

```
RECEIPT CONFIRMATION
Date: [DATE]
From: OPTKAS1 LLC (Borrower)
To: [Lender Name]

Amount Received: [AMOUNT] [USDC/USDT]
Chain: [CHAIN]
Transaction Hash: [HASH]
Block Number: [BLOCK]
Timestamp: [UTC TIME]
Receiving Wallet: [ADDRESS]

Confirmed By: [Name]
```

---

## 3. REPAYMENT PROCEDURE

### 3.1 Scheduled Repayment (Interest / Principal)

| Step | Action | Owner | Timeline |
|:-----|:-------|:------|:---------|
| 1 | Borrower calculates amount due per facility terms | Borrower | T-3 BD |
| 2 | Borrower prepares Repayment Instruction (amount, wallet, purpose) | Borrower | T-2 BD |
| 3 | Dual approval obtained per Wallet Controls Policy | Borrower | T-1 BD |
| 4 | Borrower sends stablecoin to Lender's repayment wallet | Borrower | T0 (payment date) |
| 5 | Borrower sends Payment Confirmation (with tx hash) | Borrower | Within 2 hours |
| 6 | Lender confirms receipt | Lender | Same day |
| 7 | Borrower updates Daily Balance Report + outstanding balance | Borrower | Same day |

### 3.2 Prepayment

- Borrower may prepay without penalty unless term sheet specifies otherwise
- 2 BD written notice required
- Same dual-approval and confirmation process as scheduled repayment

### 3.3 Final Repayment / Facility Termination

1. Calculate all outstanding principal + accrued interest + fees
2. Send final payment
3. Lender issues Payoff Confirmation
4. Security interest released (UCC-3 termination filed)
5. Control Agreement terminated
6. Insurance endorsements removed
7. Final reporting delivered
8. Facility archived

---

## 4. FALLBACK: BANK WIRE SETTLEMENT

### 4.1 When to Use

- Chain outage lasting > 4 hours
- Counterparty requests wire settlement
- Regulatory or compliance concern requires fiat
- Technical issue with wallet infrastructure

### 4.2 Wire Settlement Process

| Step | Action |
|:-----|:-------|
| 1 | Notify Lender of switch to wire settlement (email + call) |
| 2 | Lender provides wire instructions (bank, routing, account, reference) |
| 3 | Borrower initiates wire via banking partner |
| 4 | Borrower sends wire confirmation (reference number, amount, date) |
| 5 | Lender confirms receipt |
| 6 | Both parties reconcile wire against on-chain ledger |
| 7 | Resume on-chain settlement when chain stable for 2+ hours |

### 4.3 Wire Instructions Template

```
WIRE INSTRUCTIONS (LENDER)
Bank: [BANK NAME]
Address: [BANK ADDRESS]
Routing (ABA): [ROUTING NUMBER]
Account Number: [ACCOUNT NUMBER]
Account Name: [LENDER ENTITY NAME]
Reference: [FACILITY REFERENCE / OPTKAS1]
SWIFT (if international): [SWIFT CODE]
```

---

## 5. SETTLEMENT CALENDAR

| Event | Frequency | Day | Method |
|:------|:----------|:----|:-------|
| Interest payment | Monthly / Quarterly | [1st / 15th] of period | Stablecoin (wire fallback) |
| Principal repayment | Per schedule or bullet | As agreed | Stablecoin (wire fallback) |
| Drawdown | As needed | Per request (T-1 BD notice) | Stablecoin (wire fallback) |
| BBC delivery | Monthly | 5th BD of month | Email + data room |
| STC confirmation | Quarterly | 10th BD of quarter | Direct from STC |

---

## 6. RECONCILIATION

### 6.1 Daily Reconciliation

Every business day:
1. Compare on-chain wallet balances to internal ledger
2. Verify all transactions match approved requests
3. Flag any discrepancy > $100
4. Resolve within same day or escalate

### 6.2 Monthly Reconciliation

At month-end:
1. Full transaction log vs. facility records
2. Outstanding balance confirmation (Borrower ↔ Lender)
3. Coverage ratio recalculation
4. BBC preparation
5. File monthly reconciliation report

---

## 7. COMMUNICATION PROTOCOL

| Type | Channel | Timeline |
|:-----|:--------|:---------|
| Drawdown request | Email (encrypted) + secure portal | T-1 BD |
| Payment confirmation | Email + tx hash | Within 2 hours |
| Incident notification | Phone + email | Within 1 hour |
| Routine reporting | Data room upload + email notification | Per schedule |
| Address change | Signed letter + phone verification | 5 BD advance notice |

---

## 8. SETTLEMENT CONTACTS

| Role | Name | Email | Phone |
|:-----|:-----|:------|:------|
| Borrower Treasury | [Name] | [Email] | [Phone] |
| Borrower Manager | Jimmy | jimmy@optkas.com | [Phone] |
| Borrower Operator | Kevan | kevan@xxxiii.io | [Phone] |
| Lender Settlement | [To be provided] | [To be provided] | [To be provided] |
| Lender Ops | [To be provided] | [To be provided] | [To be provided] |

---

*This runbook is effective upon Track B activation. Review quarterly and after any settlement incident.*
