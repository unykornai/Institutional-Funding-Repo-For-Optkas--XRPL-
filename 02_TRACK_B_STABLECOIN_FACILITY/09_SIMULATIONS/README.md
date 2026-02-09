# Track B — Simulations

This folder contains counterparty response simulations and scenario testing for the stablecoin facility track.

## Simulation Scenarios

### By Counterparty Type

| Scenario | Counterparty | Expected Response |
|:---------|:-------------|:-----------------|
| S1 | Private credit fund | Approve with conditions (wallet controls, reporting) |
| S2 | Market maker (repo) | Approve with haircut + margin terms |
| S3 | Bank-adjacent desk | Slow-walk (extensive diligence, chain comfort questions) |
| S4 | Crypto-native lender | Fast approve (familiar with stablecoin rails) |

### By Stress Event

| Scenario | Event | Test |
|:---------|:------|:-----|
| S5 | Chain outage during repayment | Fallback wire settlement process |
| S6 | LTV breach (collateral devaluation) | Margin call + cure workflow |
| S7 | Counterparty default | Recovery waterfall activation |
| S8 | Regulatory inquiry | Pause + counsel + cooperation protocol |

## Simulation Pack Format

Each simulation should include:
- **Decision:** APPROVE / CONDITIONAL / REJECT / DELAY
- **Top 15 questions** the counterparty asks
- **Required conditions** list
- **Red flags** they identify
- **Exact documents** we must provide
- **Fastest path to close** (days)
- **Revised term sheet** they would propose
