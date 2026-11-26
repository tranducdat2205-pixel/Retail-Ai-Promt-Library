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
