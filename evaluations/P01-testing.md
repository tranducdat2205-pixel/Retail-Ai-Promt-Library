# P01 — Data Quality Validation

## Version 1.0 — Testing

### Test Environment
- Tool: ChatGPT Temporary Chat
- Input: Raw Sales dataset (screenshot)
- Reference answers: Not provided to AI
- Records: 33
- Expected issues: 5

### Observed Results
- Detected issues: 5/5
- Missed issues: 0
- Detection rate: 100% for this test

### Strengths
- Identified all five expected data quality issues.
- Explained potential business consequences.
- Recognised that numerical corrections require verification.

### Limitations
- Suggested numerical corrections without confirmed source data.
- No standardised severity classification.
- No explicit validation status.
- No predefined output schema.

### Lesson Learned
Accurate error detection alone does not ensure reliable
workflow automation. Explicit validation rules, structured
outputs and human approval controls are necessary.

### Planned Improvements
- Introduce a defined analyst role.
- Specify validation rules.
- Standardise output fields and severity levels.
- Prevent unsupported numerical corrections.
- Introduce a validation status and human review gate.
## Version 1.1 — Retesting

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input: Same Raw Sales screenshot
- Records: 33
- Expected issues: 5

### Observed Results

- Detected issues: 5/5
- Missed expected issues: 0
- Detection rate: 100% for this test
- High severity issues: 3
- Medium severity issues: 2
- Validation status: REVIEW REQUIRED
- Data corrections performed: None
- Human approval status: Pending

### Iteration Audit Log

| Change Made | Observed Effect |
|---|---|
| Added analyst role and business context | Output aligned with the retail validation workflow |
| Defined validation rules | All five expected issues were identified |
| Added severity criteria | Three High and two Medium issues classified |
| Added grounding constraints | No numerical corrections were estimated |
| Specified output fields | Consistent issue-reporting structure |
| Added human approval gate | Corrections remained pending verification |

### Evaluation Scores

| Criterion | v1.0 | v1.1 |
|---|---:|---:|
| Faithfulness | 4 | 5 |
| Completeness | 5 | 5 |
| Format Compliance | 3 | 5 |
| Business Usability | 4 | 4 |
| Risk Control | 3 | 5 |
| Total | 19/25 | 24/25 |

### Lesson Learned

Prompt refinement improved workflow suitability
and risk control rather than error detection accuracy.

Both versions detected all expected issues, but v1.1
provided clearer severity classification, traceable
record reconciliation and explicit human approval.

### Remaining Limitations

Testing was limited to one synthetic dataset.
Performance across unseen, ambiguous and adversarial
inputs has not yet been established.

The prompt supports human decision-making and does
not replace deterministic validation systems.

### Final Decision

Retain v1.1 for the proposed workflow, subject to
further testing and human supervision.
