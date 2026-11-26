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
