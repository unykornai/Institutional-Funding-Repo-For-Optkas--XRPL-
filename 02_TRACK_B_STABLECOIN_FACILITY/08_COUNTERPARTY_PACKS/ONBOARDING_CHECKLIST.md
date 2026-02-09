# Counterparty Onboarding Checklist — Track B

**Version:** 1.0 | **Date:** February 9, 2026 | **Owner:** OPTKAS1 PMO

---

## ONBOARDING WORKFLOW

### Phase 1: Initial Contact (Day 0–1)

- [ ] Receive counterparty inquiry or make introduction
- [ ] Send Facility Overview 1-Pager
- [ ] Confirm counterparty type (private credit / market maker / bank / crypto-native)
- [ ] Confirm preferred facility size and chain
- [ ] Execute NDA (if required by counterparty)
- [ ] Assign counterparty to internal tracking (silo folder)

### Phase 2: KYB/KYC Exchange (Day 1–5)

**We provide:**
- [ ] Entity KYB package (formation, operating agreement, good standing)
- [ ] UBO disclosure + ID copies
- [ ] Sanctions self-certification
- [ ] Source of funds statement
- [ ] Wallet addresses + ownership attestation
- [ ] Wallet Controls Policy summary

**We require from counterparty:**
- [ ] Entity KYB documents
- [ ] UBO disclosure + ID copies (25%+ owners)
- [ ] Authorized signer list + specimen signatures
- [ ] Sanctions self-certification
- [ ] Source of funds confirmation
- [ ] Wallet address(es) + ownership attestation
- [ ] Bank wire instructions (fallback)
- [ ] AML/CTF program summary (if available)

### Phase 3: Sanctions & Compliance Screening (Day 3–7)

- [ ] Screen counterparty against OFAC SDN + Consolidated Lists
- [ ] Screen all UBOs against OFAC + PEP databases
- [ ] Run adverse media check
- [ ] Document screening results in compliance file
- [ ] Clear any "possible match" flags with counsel
- [ ] **GO / NO-GO decision on compliance**

### Phase 4: Term Negotiation (Day 5–10)

- [ ] Send indicative term sheet (customized from template)
- [ ] Receive counterparty markup / counter-proposal
- [ ] Negotiate: facility size, advance rate, interest, term, covenants
- [ ] Agree indicative terms
- [ ] Engage counsel (both sides) for documentation

### Phase 5: Settlement Setup (Day 8–14)

- [ ] Exchange and verify wallet addresses (per Wallet Verification Protocol)
- [ ] Complete test transfers (both directions, $100 equivalent)
- [ ] Confirm chain selection (USDC on Ethereum/Base or USDT on Tron)
- [ ] Lock addresses in allowlists
- [ ] Confirm fallback wire instructions
- [ ] Agree reporting cadence (daily / weekly)
- [ ] Set up data room access for counterparty

### Phase 6: Legal Documentation (Day 10–20)

- [ ] Draft Facility Agreement
- [ ] Draft Security Agreement + Pledge Agreement
- [ ] Draft Account Control Agreement (if STC involvement)
- [ ] Counterparty counsel review + redlines
- [ ] Negotiate and finalize all documents
- [ ] Prepare UCC-1 filing
- [ ] Request insurance endorsements from C.J. Coleman

### Phase 7: Closing (Day 18–25)

- [ ] Execute all facility documents
- [ ] Execute Account Control Agreement (if applicable)
- [ ] File UCC-1 in Wyoming
- [ ] Receive insurance endorsements
- [ ] Deliver legal opinion (if required)
- [ ] Deliver initial Borrowing Base Certificate
- [ ] All representations and warranties confirmed
- [ ] **Closing confirmed — facility is live**

### Phase 8: First Draw + Operations Begin

- [ ] Borrower submits first drawdown request
- [ ] Lender sends USDC/USDT to Treasury Wallet
- [ ] Borrower confirms receipt + issues Receipt Memo
- [ ] Daily reporting begins
- [ ] Covenant monitoring begins
- [ ] Repayment schedule activated

---

## COUNTERPARTY FILE STRUCTURE

For each counterparty, create:

```
08_COUNTERPARTY_PACKS/[COUNTERPARTY_NAME]/
    01_KYB_KYC/               — Entity docs, UBO, IDs
    02_COMPLIANCE_SCREENING/  — OFAC results, PEP screen, adverse media
    03_TERMS/                 — Term sheets, markups, final agreed terms
    04_SETTLEMENT/            — Wallet addresses, test transfer records
    05_LEGAL/                 — Executed docs, opinions
    06_REPORTING/             — Ongoing reports
    07_CORRESPONDENCE/        — Emails, meeting notes
```

---

## ESCALATION TRIGGERS

| Trigger | Action |
|:--------|:-------|
| Compliance screening flag | Pause onboarding → counsel review |
| Counterparty unresponsive >5 BD | Escalate to Manager |
| Counterparty refuses standard KYB/KYC | Do not proceed |
| Wallet verification fails | Do not proceed until resolved |
| Terms cannot be agreed within 15 BD | Re-evaluate or walk away |

---

*Maintained by OPTKAS1 PMO. Use for every new counterparty engagement.*
