# P02 — Retail Data Standardisation

## Version 1.0 — Testing

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input: Raw Sales screenshot and P01 v1.1 output
- Original records: 33
- Identified issues: 5

### Observed Results

- All five identified issues were addressed.
- Output contained 32 records.
- Two unverified numerical corrections were applied.
- One duplicate record was removed without approval.
- Category and SKU formatting were standardised.

### Strengths

- Produced a structured sales dataset.
- Correctly standardised category and SKU formatting.
- Disclosed assumptions regarding numerical corrections.

### Limitations

- Changed S004 from -18 to 18 without verification.
- Imputed AUD 55 for S010 without confirmation.
- Removed a duplicate without human approval.
- Did not enforce the approval requirement from P01.
- Presented unverified corrections as cleaned data.

### Business Risks

Unsupported corrections may distort revenue,
sales performance and inventory decisions.

### Lesson Learned

Data standardisation requires explicit correction
rules, traceability and human approval.

A completed dataset is not necessarily a reliable
or authorised dataset.

### Planned Improvements

- Preserve original numerical values.
- Separate proposed corrections from approved changes.
- Introduce a structured change log.
- Flag unresolved records.
- Require human approval before downstream analysis.
## Version 1.1 — Complete-input Retesting

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input 1: Raw Sales screenshot
- Input 2: P01 v1.1 validation report
- Original records: 33
- Expected issues: 5

### Observed Results

- Original records retained: 33/33
- Identified issues: 5/5
- Proposed formatting corrections: 2
- Unresolved numerical issues: 2
- Duplicate record groups: 1
- Unverified numerical corrections: 0
- Unauthorised record removals: 0
- Pending approval items: 5
- Release status: BLOCKED

### Prompt Chaining Evaluation

The output explicitly used the P01 validation
report and reconciled its findings.

Both outputs identified five issues affecting
six records, including both duplicate occurrences.

### Iteration Audit Log

| Change Made | Observed Effect |
|---|---|
| Explicit numerical constraints | No unverified numerical corrections |
| Record preservation rule | All 33 records retained |
| Structured change log | Five traceable proposed actions |
| Approval requirements | All actions marked PENDING APPROVAL |
| Release conditions | Downstream analysis marked BLOCKED |
| P01 input placeholder | Upstream findings reconciled |

### Evaluation Scores

| Criterion | v1.0 | v1.1 |
|---|---:|---:|
| Faithfulness | 3 | 5 |
| Completeness | 4 | 5 |
| Format Compliance | 4 | 5 |
| Business Usability | 3 | 4 |
| Risk Control | 2 | 5 |
| Total | 16/25 | 24/25 |

These are qualitative evaluation scores based
on the observed test outputs.

### Lesson Learned

Explicit constraints and approval requirements
improved the reliability of AI-assisted data
standardisation.

Prompt chaining maintained consistency between
data validation and proposed corrective actions.

Automation should not remove accountable human
judgement from high-impact data corrections.

### Remaining Limitations

Testing used one synthetic dataset and a
missing-input variation.

No actual POS integration, authorised correction
process or production release gate was implemented.

Additional testing with unseen and adversarial
inputs is required before deployment.

### Final Decision

Retain v1.1 for the proposed workflow because
it demonstrated stronger risk control,
traceability and exception handling.
