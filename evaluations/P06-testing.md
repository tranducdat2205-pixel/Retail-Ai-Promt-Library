# P06 — Stockout Risk Detection

## Version 1.0 — Testing

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input 1: Clean Sales screenshot
- Input 2: Inventory screenshot
- Input 3: Business Rules screenshot
- Data source: Synthetic reference dataset
- Products: 8

### Observed Results

- Products analysed: 8
- Products classified as high risk: 4
- Products classified as low risk: 4
- High-risk SKUs: F01, F03, F06, F08
- Reported total stock shortfall: 255 units
- Reported zero-stock products: 1
- Report sections: 10
- Suggested priority order: 795 units

Risk classifications and shortfall calculations
were internally consistent with the reported
available and required stock values.

Independent verification of source inventory
values remains pending.

### Strengths

- Applied the supplied stockout risk formula.
- Included inbound inventory and safety stock.
- Used the latest reporting week as the sales baseline.
- Identified four potential stockout risks.
- Recognised the timely inbound delivery assumption.
- Maintained the manager approval requirement.

### Limitations

- Did not present all calculation inputs for every SKU.
- Introduced undefined urgency classifications.
- Estimated days until stockout using additional assumptions.
- Extended into overstock and replenishment analysis.
- Recommended a priority order of 795 units.
- Repeated sales trend and KPI analysis.
- Produced an excessively broad ten-section report.

### Business Risks

Combining risk detection with purchasing
recommendations may create duplicated or
inconsistent operational decisions.

Undefined urgency classifications may influence
management priorities without sufficient evidence.

### Lesson Learned

Stockout risk detection should be separated from
replenishment decisions and purchasing approval.

Transparent calculation inputs are necessary
for reliable inventory risk assessment.

### Planned Improvements

- Define explicit calculation formulas.
- Require SKU-level input traceability.
- Standardise risk classifications.
- Apply the strict stockout threshold.
- Introduce missing-data and invalid-input handling.
- Distinguish zero on-hand stock from potential stockout.
- Restrict replenishment calculations to P08.
- Require human verification.
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
- Stockout-risk SKUs: 4
- No-risk SKUs: 4
- Not-assessable SKUs: 0
- Stockout-risk products: F01, F03, F06, F08
- Total calculated shortfall: 255 units
- Zero on-hand products: 1 (F08)
- Calculation consistency: 8/8
- Classification reconciliation: PASS
- Report sections: 4
- Undefined urgency classifications: None
- Replenishment recommendations: None
- Overstock calculations: None
- Human verification: Required

### Calculation Verification

| SKU | Available | Required | Shortfall |
|---|---:|---:|---:|
| F01 | 20 | 105 | 85 |
| F02 | 100 | 70 | 0 |
| F03 | 45 | 125 | 80 |
| F04 | 80 | 43 | 0 |
| F05 | 90 | 40 | 0 |
| F06 | 20 | 65 | 45 |
| F07 | 70 | 62 | 0 |
| F08 | 0 | 45 | 45 |

All eight calculations and classifications
were consistent with the reported input values.

Independent verification against the original
Inventory worksheet remains pending.

### Iteration Audit Log

| Change Made | Observed Effect |
|---|---|
| Required SKU-based matching | Reported successful matching of eight SKUs |
| Defined explicit formulas | Improved calculation transparency |
| Required input traceability | Presented all calculation variables |
| Standardised risk classifications | Removed undefined urgency categories |
| Introduced zero on-hand flag | Identified Canvas Bag separately |
| Required reconciliation | All eight SKUs accounted for |
| Restricted task scope | Removed replenishment and overstock calculations |
| Defined workflow handover | Prepared findings for P08 and P09 |
| Required human verification | Explicit review status provided |

### Evaluation Scores

| Criterion | v1.0 | v1.1 |
|---|---:|---:|
| Faithfulness | 4 | 4 |
| Completeness | 5 | 5 |
| Format Compliance | 3 | 5 |
| Business Usability | 4 | 4 |
| Risk Control | 3 | 5 |
| Total | 19/25 | 23/25 |

These are provisional qualitative scores
based on observed prototype outputs.

### Lesson Learned

Stockout detection and purchasing decisions
should remain separate workflow responsibilities.

Transparent calculation inputs improve
auditability and support independent verification.

A calculated stock shortfall represents risk
exposure, not an approved replenishment quantity.

### Remaining Limitations

- Testing was limited to one synthetic dataset.
- Independent source inventory verification is pending.
- Threshold equality cases remain untested.
- Missing-input and conflicting-SKU cases remain untested.
- Timely inbound delivery remains an assumption.
- No actual inventory system integration.
- No automatic purchasing controls implemented.
- Human verification remains necessary.

### Final Decision

Retain v1.1 for the proposed prototype workflow,
subject to independent source-data verification
and further exception testing.
