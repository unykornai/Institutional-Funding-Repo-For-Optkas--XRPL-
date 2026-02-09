# Track B — Compliance Package

**Version:** 1.0 | **Date:** February 9, 2026 | **Owner:** OPTKAS1 PMO  
**Applies To:** All counterparty onboarding under Track B (Stablecoin Facility)

---

## 1. KYB / KYC CHECKLIST (Borrower Side — What We Provide)

### Entity-Level (KYB)

| # | Document | Source | Status |
|:--|:---------|:-------|:-------|
| 1 | Certificate of Formation (Wyoming) | Institutional package | ✅ On file |
| 2 | Operating Agreement (executed) | Institutional package | ✅ On file |
| 3 | Registered Agent confirmation | Institutional package | ✅ On file |
| 4 | Good Standing Certificate | Wyoming SOS | ✅ Obtainable same day |
| 5 | EIN / Tax ID confirmation | IRS | ✅ On file |
| 6 | Board / Manager resolution authorizing facility | Internal | 🔲 Draft upon activation |
| 7 | Authorized Signer List | Internal | ✅ Per Wallet Controls Policy |

### UBO-Level (KYC)

| # | Document | Source | Status |
|:--|:---------|:-------|:-------|
| 8 | UBO Disclosure (25%+ ownership) | Institutional package | ✅ On file |
| 9 | Government-issued ID (passport/DL) per UBO | UBO | ✅ On file |
| 10 | Proof of address per UBO (utility bill / bank statement, <90 days) | UBO | ✅ On file |
| 11 | Manager identification (Jimmy) | Manager | ✅ On file |
| 12 | Operator identification (Kevan, Unykorn) | Operator | ✅ On file |

### Wallet-Specific (Additive for Stablecoin)

| # | Document | Source | Status |
|:--|:---------|:-------|:-------|
| 13 | Wallet ownership attestation (signed letter confirming control) | Borrower | 🔲 Prepare upon activation |
| 14 | Wallet address(es) + chain(s) | Borrower | 🔲 Provide at setup |
| 15 | Wallet control policy summary | This repo | ✅ Ready |
| 16 | Authorized signer matrix for wallet operations | This repo | ✅ Ready |

---

## 2. KYB / KYC CHECKLIST (Counterparty Side — What We Require)

### From Capital Provider / Lender

| # | Document | Required | Notes |
|:--|:---------|:---------|:------|
| 1 | Entity name, jurisdiction, registration number | ✅ Mandatory | Verify against public registry |
| 2 | Certificate of incorporation / formation | ✅ Mandatory | Certified copy |
| 3 | Operating / partnership agreement (or equivalent) | ✅ Mandatory | Identify authorized signers |
| 4 | UBO disclosure (25%+ ownership) | ✅ Mandatory | Government ID per UBO |
| 5 | Authorized signer list + specimen signatures | ✅ Mandatory | For facility docs + settlement |
| 6 | Proof of regulated status (if applicable) | 🟡 If available | Fund license, SEC/CFTC registration |
| 7 | AML/CTF program summary | 🟡 Recommended | Comfort that counterparty screens too |
| 8 | Wallet address(es) + chain(s) | ✅ Mandatory | For settlement |
| 9 | Wallet ownership attestation | ✅ Mandatory | Signed confirmation of control |
| 10 | Bank wire instructions (fallback) | ✅ Mandatory | For fallback settlement |

---

## 3. SANCTIONS / OFAC SCREENING

### Borrower Self-Certification

> **SANCTIONS CERTIFICATION**
>
> OPTKAS1 LLC hereby certifies that:
>
> (a) No beneficial owner, manager, officer, director, or affiliate of the Borrower appears on any list maintained by the U.S. Department of the Treasury, Office of Foreign Assets Control (OFAC), including the Specially Designated Nationals (SDN) List, the Consolidated Sanctions List, and the Sectoral Sanctions Identifications List.
>
> (b) The Borrower is not organized or domiciled in, and does not conduct business with, any country or territory subject to comprehensive U.S. sanctions (currently: Cuba, Iran, North Korea, Syria, and the Crimea, Donetsk, and Luhansk regions of Ukraine).
>
> (c) The Borrower will cooperate fully with any counterparty's independent sanctions screening and will provide all information reasonably requested for such screening.
>
> (d) The Borrower will promptly notify the Lender if any of the above representations ceases to be true.

### Counterparty Screening (What We Do)

| Check | Source | Frequency |
|:------|:-------|:----------|
| OFAC SDN List | U.S. Treasury | Before onboarding + quarterly |
| Consolidated Sanctions List | U.S. Treasury | Before onboarding + quarterly |
| EU Sanctions List | EU Council | Before onboarding + quarterly (if applicable) |
| UN Security Council List | United Nations | Before onboarding + quarterly (if applicable) |
| Adverse media screening | Commercial vendor | Before onboarding + annually |
| PEP screening | Commercial vendor | Before onboarding + annually |

### Ongoing Monitoring

- Re-screen all counterparties quarterly
- Re-screen immediately upon any sanctions list update affecting relevant jurisdictions
- Document all screening results (date, source, result) in counterparty compliance file
- Flag any "possible match" for legal counsel review before proceeding

---

## 4. SOURCE OF FUNDS / USE OF PROCEEDS

### Source of Funds (Borrower — Collateral Acquisition)

> The collateral securing this facility (500 units of TC Advantage 5% Secured Medium Term Notes) was acquired by OPTKAS1 LLC pursuant to Subscription Agreement with TC Advantage Traders, Ltd. at a cost basis of $3,000,000,000 ($6,000,000 per note × 500 notes). The subscription was funded through SPV capital contributions. Supporting documentation (Subscription Agreement, payment records) is available upon request under NDA.

### Source of Funds (Counterparty — Capital Provided)

We require counterparties to confirm:

| # | Question | Required Response |
|:--|:---------|:-----------------|
| 1 | Source of funds for the facility advance | Written description |
| 2 | Are funds derived from or connected to any sanctioned activity? | Must be "No" |
| 3 | Are funds derived from or connected to any criminal activity? | Must be "No" |
| 4 | Is the counterparty acting on behalf of any undisclosed third party? | Must be "No" or fully disclosed |
| 5 | Are there any restrictions on the counterparty's ability to transfer USDC/USDT? | Must disclose |

### Use of Proceeds (Borrower)

Facility proceeds will be used for:
- General corporate purposes of OPTKAS1 LLC
- Working capital
- Investment activities consistent with SPV purpose
- Repayment of existing obligations (if any)

Facility proceeds will NOT be used for:
- Any activity in sanctioned jurisdictions
- Any activity involving sanctioned persons or entities
- Speculative cryptocurrency trading
- Any purpose prohibited by the facility agreement

---

## 5. WALLET VERIFICATION PROTOCOL

### Before First Transaction

| Step | Action | Evidence |
|:-----|:-------|:--------|
| 1 | Counterparty provides wallet address + chain + asset type | Written on entity letterhead |
| 2 | Borrower verifies address format is valid for stated chain | Technical check |
| 3 | Borrower checks address against known sanctioned addresses (if available) | Blockchain analytics |
| 4 | Both parties confirm addresses via independent channel (phone/video, not email alone) | Call log record |
| 5 | Small test transfer ($100 equivalent) in both directions | Transaction hashes |
| 6 | Both parties confirm receipt out-of-band | Written confirmation |
| 7 | Addresses locked in allowlists | Per Wallet Controls Policy |

### Address Change Protocol

- 5 BD advance written notice required
- New address verified via same protocol as above
- Old address removed from allowlist only after new address confirmed
- Counterparty notified of change via two independent channels

---

## 6. TRAVEL RULE COMPLIANCE

### Applicability

If transaction amounts exceed applicable Travel Rule thresholds ($3,000 for certain US-regulated entities, $1,000 for some international frameworks), the following information must accompany the transfer:

**Originator Information:**
- Entity name
- Wallet address
- Physical address (registered)
- Account reference (if applicable)

**Beneficiary Information:**
- Entity name
- Wallet address

### Implementation

- For regulated counterparties: use their preferred Travel Rule solution (e.g., Notabene, TRP, Shyft)
- For non-regulated counterparties: exchange information via signed settlement instruction letters
- All Travel Rule data filed in counterparty compliance folder

---

## 7. RECORD RETENTION

| Record Type | Retention Period | Storage |
|:------------|:----------------|:--------|
| KYB/KYC documents | 7 years after relationship ends | Encrypted, access-controlled |
| Sanctions screening results | 7 years | Compliance archive |
| Transaction records | 7 years | On-chain + off-chain backup |
| Source of funds documentation | 7 years | Compliance archive |
| Wallet verification records | 7 years | Compliance archive |
| Travel Rule data | 7 years | Compliance archive |
| Incident / SAR records | 7 years (or as legally required) | Counsel-controlled |

---

*Maintained by OPTKAS1 PMO. Review and update upon activation and before each new counterparty onboarding.*
