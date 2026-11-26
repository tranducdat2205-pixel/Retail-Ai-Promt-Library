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
