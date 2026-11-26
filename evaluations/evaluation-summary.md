# Prompt Library Evaluation Summary

## 1. Evaluation Methodology

Ten business prompts were developed and
evaluated through two main versions.

Version 1.0 established the initial instruction.

Version 1.1 incorporated improvements based
on observed output limitations.

Testing used ChatGPT Temporary Chats and
equivalent inputs for each version comparison.

The evaluation criteria were:

- Faithfulness
- Completeness
- Format Compliance
- Business Usability
- Risk Control

Each criterion was scored from 1 to 5,
with a maximum of 25 points per version.

The scores represent qualitative assessments
rather than independent performance benchmarks.

## 2. Scoring Framework

| Score | Interpretation |
|---:|---|
| 1 | Major failure |
| 2 | Significant limitations |
| 3 | Partially satisfactory |
| 4 | Strong performance with limitations |
| 5 | Meets the evaluated criterion in the tested case |

## 3. Evaluation Results

| Prompt | v1.0 | v1.1 | Improvement |
|---|---:|---:|---:|
| P01 Data Quality | 19 | 24 | +5 |
| P02 Standardisation | 16 | 24 | +8 |
| P03 Sales Performance | 20 | 24 | +4 |
| P04 KPI Monitoring | 20 | 24 | +4 |
| P05 Sales Trends | 21 | 24 | +3 |
| P06 Stockout Risk | 19 | 23 | +4 |
| P07 Overstock | 19 | 23 | +4 |
| P08 Replenishment | 19 | 23 | +4 |
| P09 Business Actions | 21 | 24 | +3 |
| P10 Executive Summary | 21 | 24 | +3 |
| Total | 195 | 237 | +42 |

Initial score: 78.0%

Revised score: 94.8%

Improvement: 16.8 percentage points.

Scores remain subject to further validation
and should not be interpreted as production
accuracy or actual business performance.

## 4. Key Improvements

| Prompt | Initial Limitation | Revised Improvement |
|---|---|---|
| P01 | Unstructured validation | Severity classifications and review status |
| P02 | Unauthorised data corrections | Approval gate and blocked status |
| P03 | Recommendations beyond supplied evidence | Explicit calculations and scope control |
| P04 | Excessive analysis | Structured KPI assessment |
| P05 | Incomplete treatment of tied trends | Consistent trend classifications |
| P06 | Replenishment decisions beyond scope | Transparent stockout calculations |
| P07 | Unsupported operational priorities | Complete assessment and conflict escalation |
| P08 | Discretionary quantity adjustment | Preservation of calculated quantities |
| P09 | Inconsistent evidence references | Evidence-based action plan and decision options |
| P10 | Excessive reporting detail | Concise executive communication |

## 5. Selected Case Studies

### Case Study 1: P02 — Data Governance

The initial prompt made proposed corrections
to ambiguous numerical records.

The revised prompt preserved the original
records and required human approval before
releasing corrected data.

This demonstrates the importance of maintaining
data integrity and preventing unauthorised
assumptions during data preparation.

### Case Study 2: P08 — Responsible AI

Both versions calculated 960 replenishment units.

Version 1.0 proposed reducing the recommended
quantity to 913 units because of two policy
conflicts involving 47 units.

Version 1.1 preserved all 960 calculated units
and separated standard approval from unresolved
policy decisions.

No purchasing decision was authorised.

This demonstrates the distinction between
analytical accuracy and decision authority.

### Case Study 3: P10 — Executive Communication

The initial report contained eight sections
and seven management actions.

The revised report contained five sections
and four priority management actions.

All fifteen checked business metrics and
both unresolved policy conflicts were preserved.

This demonstrates information compression
without sacrificing material decision requirements.

## 6. Critical Reflection

The testing process demonstrated that
generative AI can support repetitive business
analysis and structured reporting.

However, accurate calculations alone do not
guarantee appropriate business decisions.

Initial prompts sometimes encouraged AI to
extend beyond the intended task, introduce
discretionary policy preferences or make
unsupported assumptions.

Explicit formulas, structured outputs,
scope restrictions, evidence references
and human approval requirements improved
the observed prototype outputs.

Prompt chaining also introduces the risk
that inaccurate upstream information may
propagate into later management reports.

Consequently, consistency between reports
must not be confused with independent
verification of source data.

## 7. Evaluation Limitations

- Limited synthetic business scenario.
- Qualitative and non-independent scoring.
- Some source verification remains outstanding.
- Limited testing of unusual and adversarial inputs.
- No repeated-run reliability benchmark.
- No actual senior management usability study.
- No production system integration.
- No measured financial benefits or time savings.

## 8. Recommended Next Steps

- Independently verify source data and calculations.
- Test missing and conflicting inputs.
- Test threshold boundary conditions.
- Evaluate adversarial instructions embedded in data.
- Conduct repeated-run reliability testing.
- Integrate deterministic calculation controls.
- Implement enforceable approval mechanisms.
- Evaluate usability with actual business users.

## 9. Detailed Testing Records

Individual testing observations and iteration
audit logs are available in the P01-P10
testing files within this directory.
