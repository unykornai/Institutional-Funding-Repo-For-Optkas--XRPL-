# Shared Components

**Purpose:** Cross-track infrastructure shared by Tracks A–D.

---

## Contents (When Populated)

| Component | Description | Used By |
|:----------|:-----------|:--------|
| Wallet policy templates | Standard wallet governance | All tracks |
| Address allowlist format | Approved address registry | B, D |
| Monitoring alerts schema | LTV breach, balance variance, outage detection | B, C, D |
| Reporting templates | Shared formatting for daily/weekly/monthly reports | All tracks |
| Risk engine primitives | LTV calculation, haircut tables, margin call logic | B, C |
| Reconciliation tools | On-chain ↔ off-chain matching | A, B |
| Compliance checklists | KYB/KYC/AML shared templates | All tracks |
| Incident response playbook | Shared escalation framework | All tracks |

---

## Design Principle

Shared components are **track-agnostic**. Any track can import them without creating dependencies on other tracks. When a component is track-specific, it lives in that track's folder, not here.

---

*Populate as tracks are activated. Keep components generic and reusable.*
