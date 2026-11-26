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
