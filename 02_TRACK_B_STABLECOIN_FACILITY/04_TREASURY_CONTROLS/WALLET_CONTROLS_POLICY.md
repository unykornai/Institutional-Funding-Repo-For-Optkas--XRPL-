# Wallet Controls Policy

**Version:** 1.0 | **Date:** February 9, 2026 | **Owner:** OPTKAS1 PMO  
**Applies To:** All wallet-based operations under Track B (Stablecoin Facility)

---

## 1. WALLET ARCHITECTURE

### 1.1 Wallet Types

| Wallet | Purpose | Chain(s) | Access Level |
|:-------|:--------|:---------|:-------------|
| **Treasury Wallet** | Primary receipt + holding of facility proceeds | Ethereum/Base, Tron | Restricted — dual approval |
| **Operations Wallet** | Day-to-day disbursements within permitted uses | Same as Treasury | Restricted — dual approval |
| **Repayment Wallet** | Outbound payments to Lender | Same as Treasury | Restricted — dual approval |
| **Cold Storage** | Long-term holding (if balances exceed operating needs) | Hardware wallet | Restricted — Manager + Operator |

### 1.2 Wallet Ownership

All wallets are owned and controlled by OPTKAS1 LLC (Borrower SPV). The Manager/Operator provides administrative and technical support but does not independently control funds.

---

## 2. AUTHORIZED SIGNERS

### 2.1 Signer Matrix

| Role | Name | Authority | Limits |
|:-----|:-----|:----------|:-------|
| **Primary Signer** | Manager (OPTKAS1 LLC) | Initiate + approve transactions | Unlimited (within facility terms) |
| **Secondary Signer** | Operator (Unykorn) | Co-approve transactions | Required for amounts > $[50,000] |
| **Emergency Signer** | [Designated backup] | Activate only if Primary unavailable for 48+ hours | Same as Primary, with written justification |

### 2.2 Dual Approval Rule

**All outbound transactions require approval from at least two authorized signers.**

Exceptions:
- Test transfers under $1,000 (single signer, logged)
- Pre-approved recurring payments (interest, reporting fees) — set up once with dual approval, then execute automatically

### 2.3 Signer Changes

Any change to the authorized signer matrix requires:
1. Written notice from the Manager
2. 48-hour cooling period before activation
3. Notification to Lender (if facility is active)
4. Updated record in this document

---

## 3. ALLOWLIST POLICY

### 3.1 Outbound Address Allowlist

**Only pre-approved addresses may receive funds from any Borrower wallet.**

| Address Type | Approval Process | Modification |
|:-------------|:----------------|:-------------|
| Lender repayment address | Verified at facility execution | Requires Lender written confirmation to change |
| Vendor / service provider | Dual-approved before first payment | Manager + Operator both approve |
| Borrower's own wallets | Pre-registered at setup | Dual approval to add new wallet |
| Exchange / OTC desk | Dual-approved, purpose-documented | Re-verified quarterly |

### 3.2 Adding a New Address

1. Requestor submits address + purpose + chain + supporting evidence
2. Both signers verify address independently (different devices)
3. Small test transfer sent ($10–$100 equivalent)
4. Recipient confirms receipt out-of-band (email/call)
5. Address added to allowlist with effective date
6. Logged in Allowlist Register (maintained separately)

### 3.3 Inbound Addresses

No restrictions on inbound, but:
- Only accept from verified counterparty addresses
- Flag and investigate any unexpected inbound
- Report to Lender if unexpected inbound exceeds $10,000

---

## 4. TRANSACTION LIMITS & ESCALATION

| Tier | Amount (USD equivalent) | Approval Required | Timeline |
|:-----|:----------------------|:------------------|:---------|
| Tier 1 | ≤ $50,000 | Single signer (logged) | Same day |
| Tier 2 | $50,001 – $500,000 | Dual approval | Same day |
| Tier 3 | $500,001 – $5,000,000 | Dual approval + written justification | 1 BD notice |
| Tier 4 | > $5,000,000 | Dual approval + Manager written authorization + Lender notification | 2 BD notice |

---

## 5. DAILY OPERATIONS

### 5.1 Daily Balance Check

Every business day at 9:00 AM ET:
1. Record balance of all wallets (Treasury, Operations, Repayment, Cold)
2. Compare against expected balance (previous day + inflows − outflows)
3. Investigate any discrepancy > $100
4. File daily balance report per `06_REPORTING/DAILY_REPORTING_TEMPLATE.md`

### 5.2 Transaction Log

Every transaction is logged with:
- Date/time (UTC)
- Chain + transaction hash
- From address → To address
- Amount (stablecoin) + USD equivalent
- Purpose category (drawdown, repayment, operations, fee, other)
- Approved by (signer names)
- Notes

---

## 6. SECURITY MEASURES

### 6.1 Key Management

| Control | Requirement |
|:--------|:-----------|
| Private keys | Never stored on email, cloud, or shared drives |
| Hardware wallets | Required for cold storage; recommended for all wallets |
| Seed phrases | Stored in two separate physical locations (sealed envelopes in safes) |
| Key rotation | Rotate operational wallet keys every [90] days |
| Device hygiene | Dedicated devices for wallet operations; no personal use |

### 6.2 Network Security

- Dedicated IP allowlisting for wallet management interfaces (where supported)
- VPN required for remote wallet operations
- 2FA on all exchange/custodian accounts
- No public Wi-Fi for any wallet operation

---

## 7. INCIDENT RESPONSE

### 7.1 Incident Types

| Type | Response |
|:-----|:---------|
| Unauthorized transaction detected | Immediately freeze all wallets; notify Lender within 1 hour; engage counsel |
| Compromised key suspected | Rotate immediately; transfer to new wallet; investigate; notify Lender |
| Chain outage (>4 hours) | Switch to bank wire fallback; notify Lender; document |
| Signer unavailability (>48 hours) | Activate Emergency Signer; notify Lender |
| Regulatory inquiry | Pause operations; engage counsel; cooperate fully; notify Lender |

### 7.2 Incident Log

Every incident is documented with:
- Date/time of detection
- Description
- Actions taken
- Resolution
- Lessons learned
- Notification records (who was told, when)

---

## 8. REPORTING TO LENDER

| Report | Frequency | Content |
|:-------|:----------|:--------|
| Daily Balance Report | Daily | All wallet balances, movements, variances |
| Transaction Log | Weekly (or on request) | Full transaction detail |
| Allowlist Register | Quarterly | All approved addresses with verification dates |
| Incident Report | As needed | Per Section 7 |
| Signer Matrix Update | As needed | Any changes to authorized signers |

---

## 9. CHAIN OUTAGE / FALLBACK PROTOCOL

If the primary settlement chain (Ethereum/Base or Tron) is unavailable for more than 4 hours:

1. Switch to bank wire settlement
2. Notify Lender of chain outage and estimated restoration
3. Continue all reporting in the same format
4. Resume on-chain settlement when chain is confirmed stable for 2+ hours
5. Reconcile any wire-based transactions against on-chain ledger

---

## 10. POLICY REVIEW

This policy is reviewed:
- Quarterly (routine)
- After any incident
- Before onboarding a new counterparty
- After any material change in wallet infrastructure

---

*Maintained by OPTKAS1 PMO. Effective upon Track B activation.*
