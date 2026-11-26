# P07 — Overstock Identification

## Version 1.0 — Testing

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input 1: Clean Sales screenshot
- Input 2: Inventory screenshot
- Input 3: Business Rules screenshot
- Data source: Synthetic reference dataset

### Observed Results

- Products analysed: 8
- Overstocked products: 3
- Overstock percentage: 37.50%
- Overstocked SKUs: F02, F04, F05
- Highest stock cover: Hoodie, 9.00 weeks
- Total excess inventory: 78 units
- Reported excess retail value: AUD 4,830

All eight reported stock coverage values matched
the provisional reference calculations based
on P06 reported inputs.

Independent source inventory verification
remains pending.

### Strengths

- Applied the correct stock coverage formula.
- Used on-hand inventory rather than available stock.
- Applied the strict four-week threshold.
- Identified all three expected overstocked products.
- Distinguished retail value from financial loss.
- Recognised potentially conflicting signals
  between overstock and replenishment rules.

### Limitations

- Detailed table included only overstocked SKUs.
- No explicit SKU count reconciliation.
- Introduced undefined priority classifications.
- Calculated excess retail value outside the core task.
- Recommended promotions without cost or margin data.
- Extended into replenishment and management decisions.
- No explicit zero-denominator handling.

### Business Risks

Unsupported priority classifications and promotional
recommendations may influence management decisions
without sufficient financial or operational evidence.

Conflicting inventory rules require human review
before purchasing decisions are made.

### Lesson Learned

Overstock classification should be separated
from replenishment and promotional decisions.

Conflicting business rules should be escalated
rather than silently resolved by AI.

### Planned Improvements

- Require a complete eight-SKU assessment table.
- Define explicit stock coverage and excess formulas.
- Apply the threshold before rounding.
- Standardise overstock classifications.
- Introduce zero-sales and missing-data handling.
- Require SKU reconciliation.
- Restrict purchasing and promotional recommendations.
- Require human verification and workflow handover.
## Version 1.1 — Retesting

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input 1: Same Clean Sales screenshot
- Input 2: Same Inventory screenshot
- Input 3: Same Business Rules screenshot
- Data source: Synthetic reference dataset

### Observed Results

- Total distinct SKUs: 8
- Reported matched SKUs: 8/8
- Overstocked SKUs: 3
- Not-overstocked SKUs: 5
- Not-assessable SKUs: 0
- Overstock percentage: 37.50%
- Overstocked products: F02, F04, F05
- Total calculable excess units: 78
- Highest stock cover: Hoodie, 9.00 weeks
- Calculation consistency: 8/8
- Classification reconciliation: PASS
- Report sections: 4
- Conflicting operational signals identified: 2
- Unsupported promotional recommendations: None
- Human verification: Required

### Calculation Verification

| SKU | Stock Cover | Excess Units | Classification |
|---|---:|---:|---|
| F01 | 0.27 | 0 | NOT OVERSTOCK |
| F02 | 5.00 | 20 | OVERSTOCK |
| F03 | 0.70 | 0 | NOT OVERSTOCK |
| F04 | 4.44 | 8 | OVERSTOCK |
| F05 | 9.00 | 50 | OVERSTOCK |
| F06 | 0.60 | 0 | NOT OVERSTOCK |
| F07 | 1.67 | 0 | NOT OVERSTOCK |
| F08 | 0.00 | 0 | NOT OVERSTOCK |

All eight calculations were consistent with
the previously reported inventory inputs.

Independent verification against the original
Inventory worksheet remains pending.

### Iteration Audit Log

| Change Made | Observed Effect |
|---|---|
| Required complete assessment table | Presented all eight SKUs |
| Defined stock cover and excess formulas | Improved calculation transparency |
| Specified unrounded classification values | Explicitly documented precision control |
| Standardised classifications | Removed undefined priority labels |
| Required SKU reconciliation | All eight SKUs accounted for |
| Restricted operational recommendations | No purchasing or promotional decisions |
| Introduced conflict escalation | Flagged two conflicting operational signals |
| Defined workflow handover | Prepared findings for P08 and P09 |
| Required human verification | Explicit review status provided |

### Business Rule Conflict

Two overstocked products also contained
positive suggested order quantities:

- F02 Oxford Shirt: 30 units
- F04 Chinos: 17 units

The revised output reported these existing
values without recalculating, validating
or endorsing them.

The conflicts were escalated for management
review rather than automatically resolved.

### Evaluation Scores

| Criterion | v1.0 | v1.1 |
|---|---:|---:|
| Faithfulness | 4 | 4 |
| Completeness | 5 | 5 |
| Format Compliance | 3 | 5 |
| Business Usability | 4 | 4 |
| Risk Control | 3 | 5 |
| Total | 19/25 | 23/25 |

These are provisional qualitative evaluation
scores based on observed prototype outputs.

### Lesson Learned

Correct inventory calculations do not
automatically justify operational decisions.

Conflicting business rules require transparent
escalation and human judgement.

Not-overstocked inventory is not necessarily
healthy inventory.

### Remaining Limitations

- Testing was limited to one synthetic dataset.
- Independent inventory source verification is pending.
- Threshold equality cases remain untested.
- Zero-sales and missing-input cases remain untested.
- Numerical precision controls have not been
  tested using near-threshold values.
- Inventory snapshot timing remains unverified.
- No actual inventory system integration.
- Human verification remains necessary.

### Final Decision

Retain v1.1 for the proposed workflow because
it demonstrated stronger calculation transparency,
scope control and conflict escalation.

Further exception testing and independent
source verification are required.
