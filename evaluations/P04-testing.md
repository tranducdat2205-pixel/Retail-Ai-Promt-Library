# P04 — KPI Performance Monitoring

## Version 1.0 — Testing

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input 1: P03 v1.1 sales performance report
- Input 2: Business Rules screenshot
- Data source: Synthetic retail business scenario

### Observed Results

- Latest weekly revenue: AUD 12,320
- Revenue target: AUD 14,000
- Target achievement: 88%
- Revenue shortfall: AUD 1,680
- Percentage shortfall: 12%
- Week-on-week revenue growth: 11.49%
- Week-on-week sales volume growth: 12.97%
- Revenue target status: NOT MET

The checked KPI calculations were consistent
with the supplied P03 report and expected results.

### Strengths

- Correctly evaluated revenue target achievement.
- Distinguished revenue growth from target achievement.
- Applied the latest-week target appropriately.
- Did not invent additional performance targets.
- Recognised missing inventory information.
- Maintained human verification requirements.

### Limitations

- Produced an excessively detailed nine-section report.
- Repeated product and category analysis from P03.
- Extended into inventory and replenishment analysis.
- Did not provide a standardised KPI monitoring table.
- Provided recommendations overlapping with P09.
- Key KPI calculation formulas were not fully documented.

### Business Risks

Overlapping workflow responsibilities may increase
review time, create duplicated reports and reduce
the consistency of management information.

### Lesson Learned

Effective workflow automation requires clearly
defined task boundaries and predictable outputs.

A correct but unnecessarily broad report may
reduce operational efficiency.

### Planned Improvements

- Define explicit KPI calculation formulas.
- Restrict analysis to supplied performance targets.
- Standardise KPI status classifications.
- Separate target achievement from sales growth.
- Route inventory-related tasks to P06-P08.
- Reserve detailed management actions for P09.
- Introduce a concise reporting structure.
## Version 1.1 — Retesting

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input 1: P03 v1.1 sales performance report
- Input 2: Same Business Rules screenshot
- Data source: Synthetic retail business scenario

### Observed Results

- Latest weekly revenue: AUD 12,320
- Revenue target: AUD 14,000
- Target achievement: 88.00%
- Revenue variance: AUD -1,680
- Percentage variance: -12.00%
- Absolute weekly revenue change: AUD 1,270
- Week-on-week revenue growth: 11.49%
- Target status: NOT MET
- Invented targets: 0
- Report sections: 4
- Management observations: 3
- Out-of-scope inventory calculations: 0
- Human verification: Required

The checked KPI calculations matched the
supplied sales report and expected results.

### Iteration Audit Log

| Change Made | Observed Effect |
|---|---|
| Defined explicit KPI formulas | Improved calculation transparency |
| Restricted target applicability | Target applied only to the latest week |
| Standardised KPI classifications | Missing targets classified as NOT ASSESSABLE |
| Introduced four-section structure | Reduced report from nine sections to four |
| Restricted task scope | Avoided repeated product and category analysis |
| Defined workflow routing | Inventory tasks assigned to P06-P08 |
| Limited management observations | Three focused observations |
| Required human verification | Explicit review status provided |

### Prompt Chaining Evaluation

P04 successfully extracted relevant sales
performance figures from the P03 report and
applied the supplied business rules.

The output identified downstream workflow
destinations without executing those tasks.

Actual automated system routing was not implemented.

### Evaluation Scores

| Criterion | v1.0 | v1.1 |
|---|---:|---:|
| Faithfulness | 5 | 5 |
| Completeness | 5 | 5 |
| Format Compliance | 3 | 5 |
| Business Usability | 3 | 4 |
| Risk Control | 4 | 5 |
| Total | 20/25 | 24/25 |

These are qualitative evaluation scores based
on observed prototype test outputs.

### Lesson Learned

Effective workflow automation requires clear
task boundaries as well as accurate calculations.

Prompt refinement improved reporting consistency,
calculation transparency and workflow coordination.

Positive revenue growth does not necessarily
indicate successful target achievement.

### Remaining Limitations

- Testing was limited to one synthetic business scenario.
- Missing-input and zero-denominator cases remain untested.
- The improved output remains relatively detailed.
- No automated dashboard or workflow integration.
- Time savings have not been measured.
- Human verification remains necessary.

### Final Decision

Retain v1.1 for the proposed workflow because
it demonstrated stronger scope control,
reporting consistency and calculation transparency.
