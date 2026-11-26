# P05 — Sales Trend Identification

## Version 1.0 — Testing

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input 1: Clean Sales screenshot
- Input 2: Business Rules screenshot
- Data source: Synthetic reference dataset
- Products: 8
- Comparison: 9 November to 16 November 2026

### Observed Results

- Correct product growth calculations: 8/8
- Correct trend classifications: 8/8
- Increasing products: 5
- Decreasing products: 3
- Stable products: 0
- Highest percentage growth: 25.00%
- Largest percentage decline: Hoodie, -28.57%
- Largest absolute volume increase: Basic Tee, 15 units

### Strengths

- Applied the supplied week-on-week trend rule.
- Calculated all eight product growth rates correctly.
- Distinguished historical trends from forecasts.
- Provided an explicit percentage-change formula.
- Recognised insufficient inventory information.

### Limitations

- Did not explicitly identify all four products
  sharing the highest percentage growth.
- Repeated KPI monitoring results from P04.
- Extended analysis beyond the required comparison period.
- Produced management recommendations overlapping with P09.
- No predefined handling of missing or zero previous sales.
- No explicit final human verification status.

### Business Risks

Inconsistent ranking criteria may cause management
to overlook equally performing products.

Duplicated analysis may increase reporting and review
effort without adding sufficient business value.

### Lesson Learned

Reliable trend reporting requires explicit comparison
periods, consistent metrics and transparent tie handling.

Historical sales movements must not be interpreted
as confirmed future demand.

### Planned Improvements

- Restrict analysis to the latest two reporting weeks.
- Define absolute and percentage growth separately.
- Identify all tied highest and lowest performers.
- Introduce missing-data and zero-denominator handling.
- Restrict output to product-level trend analysis.
- Require human verification before downstream use.
## Version 1.1 — Retesting

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input 1: Same Clean Sales screenshot
- Input 2: Same Business Rules screenshot
- Data source: Synthetic reference dataset
- Products: 8
- Comparison: 9 November to 16 November 2026

### Observed Results

- Correct product growth calculations: 8/8
- Correct trend classifications: 8/8
- Increasing products: 5
- Decreasing products: 3
- Stable products: 0
- Not-assessable products: 0
- Highest percentage growth: 25.00%
- Tied highest-growth products identified: 4/4
- Largest absolute increase: Basic Tee, 15 units
- Largest percentage decline: Hoodie, -28.57%
- SKU count reconciliation: PASS
- Report sections: 4
- Unsupported forecasts: None
- Out-of-scope inventory calculations: None
- Human verification: Required

The numerical results matched the expected
values established for the prototype test.

### Iteration Audit Log

| Change Made | Observed Effect |
|---|---|
| Restricted comparison period | Used the latest two reporting weeks |
| Defined absolute and percentage growth | Distinguished volume from percentage leadership |
| Introduced explicit tie handling | Identified all four tied products |
| Standardised trend classifications | Correctly classified all eight SKUs |
| Required SKU reconciliation | Classification counts reconciled to eight |
| Restricted task scope | Avoided duplicated KPI and inventory analysis |
| Defined P09 handover | Prepared trend findings for management review |
| Required human verification | Explicit review status provided |

### Evaluation Scores

| Criterion | v1.0 | v1.1 |
|---|---:|---:|
| Faithfulness | 5 | 5 |
| Completeness | 5 | 5 |
| Format Compliance | 3 | 5 |
| Business Usability | 4 | 4 |
| Risk Control | 4 | 5 |
| Total | 21/25 | 24/25 |

These are qualitative evaluation scores based
on observed prototype test outputs.

### Lesson Learned

Explicit tie handling reduces the risk of
overlooking products with equivalent performance.

Percentage growth and absolute sales growth
represent different business indicators.

Clear temporal constraints and task boundaries
improve the consistency of trend reporting.

### Remaining Limitations

- Testing was limited to one synthetic dataset.
- Stable-sales cases have not been tested.
- Missing-data and zero-denominator scenarios
  remain untested.
- No actual POS or workflow integration.
- Historical trends do not establish future demand.
- Human verification remains necessary.

### Final Decision

Retain v1.1 for the proposed workflow because
it demonstrated stronger tie handling, scope
control and reporting consistency.
