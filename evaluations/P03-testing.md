# P03 — Sales Performance Analysis

## Version 1.0 — Testing

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input: Clean Sales dataset screenshot
- Records: 32
- Products: 8
- Categories: 4
- Reporting period: Four weeks
- Data source: Synthetic reference dataset

The Clean Sales dataset was used for independent
prototype testing. It was not released or approved
through P02.

### Observed Results

- Total revenue: AUD 43,680
- Total units sold: 938
- Average weekly revenue: AUD 10,920
- First-to-last-week revenue growth: 26.94%
- Product revenue totals verified: 8/8
- Category revenue totals verified: 4/4
- Weekly revenue totals verified: 4/4

All listed financial totals matched independent
calculations from the Clean Sales worksheet.

### Strengths

- Accurate revenue and sales volume calculations.
- Correct product and category revenue rankings.
- Distinguished revenue from sales volume.
- Recognised missing profitability information.
- Acknowledged the short reporting period.

### Limitations

- Performance metrics were not predefined.
- Calculation formulas were not explicitly documented.
- No formal revenue reconciliation was presented.
- Inventory recommendations were made without
  inventory availability or supplier information.
- Overall underperformance was not objectively defined.
- Output was lengthy and lacked a predefined structure.

### Business Risks

Accurate sales figures may still lead to inappropriate
inventory decisions when stock availability,
profit margins and operational constraints are unknown.

### Lesson Learned

Reliable business analysis requires explicit metrics,
reproducible calculations and evidence-based insights.

Accurate calculations alone do not guarantee
appropriate business recommendations.

### Planned Improvements

- Define revenue and growth formulas.
- Standardise product and category ranking criteria.
- Introduce numerical reconciliation.
- Separate observations from recommendations.
- Restrict unsupported inventory decisions.
- Require human verification before business action.
## Version 1.1 — Retesting

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input: Same Clean Sales screenshot
- Records: 32
- Products: 8
- Categories: 4
- Reporting period: Four weeks

### Observed Results

- Total revenue: AUD 43,680
- Total units sold: 938
- Average weekly revenue: AUD 10,920
- Revenue growth: 26.94%
- Record-level revenue verified: 32/32
- Weekly revenue totals verified: 4/4
- Product revenue totals verified: 8/8
- Category revenue totals verified: 4/4
- Product growth rates verified: 8/8
- Category growth rates verified: 4/4
- Numerical reconciliation: PASS
- Unsupported inventory purchase recommendations: None
- Management observations: 3
- Human verification: Required

The checked numerical results matched independent
calculations using the Clean Sales worksheet.

### Iteration Audit Log

| Change Made | Observed Effect |
|---|---|
| Defined calculation formulas | Improved calculation transparency |
| Standardised ranking metric | Products and categories ranked consistently by revenue |
| Separated revenue and volume | Reduced metric ambiguity |
| Required numerical reconciliation | Revenue totals reconciled across all aggregations |
| Limited management observations | Three focused analytical insights |
| Restricted inventory recommendations | No unsupported stock purchase recommendations |
| Required human verification | Explicit review status provided |

### Evaluation Scores

| Criterion | v1.0 | v1.1 |
|---|---:|---:|
| Faithfulness | 4 | 5 |
| Completeness | 5 | 5 |
| Format Compliance | 4 | 5 |
| Business Usability | 4 | 4 |
| Risk Control | 3 | 5 |
| Total | 20/25 | 24/25 |

These are qualitative evaluation scores based
on observed prototype test outputs.

### Lesson Learned

Prompt refinement improved analytical transparency,
reporting consistency and evidence-based interpretation.

Accurate calculations alone do not guarantee
appropriate business decisions.

Numerical reconciliation improves error detection
but does not replace independent verification.

### Remaining Limitations

- Testing was limited to one synthetic dataset.
- Missing-value and zero-denominator scenarios
  have not yet been tested.
- No actual POS or reporting system integration.
- Profitability and inventory availability
  cannot be assessed using sales data alone.
- Human verification remains necessary.

### Final Decision

Retain v1.1 for the proposed workflow, subject
to further testing and independent verification.
