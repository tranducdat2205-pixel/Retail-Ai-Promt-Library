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
