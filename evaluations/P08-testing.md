# P08 — Replenishment Recommendations

## Version 1.0 — Testing

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input 1: P06 v1.1 stockout risk report
- Input 2: P07 v1.1 overstock assessment
- Input 3: Inventory screenshot
- Input 4: Business Rules screenshot
- Data source: Synthetic retail business scenario

### Observed Results

- Total SKUs assessed: 8
- Calculation consistency: 8/8
- Formula-based replenishment: 960 units
- AI-recommended replenishment: 913 units
- Deferred replenishment: 47 units
- Conflicting policy signals: 2
- Stockout-risk replenishment: 795 units
- Other replenishment: 118 units
- Negative calculated quantities: 0
- Purchase orders authorised: 0
- Report sections: 11

The calculated order quantities matched the
provisional reference calculations based on
previously reported inventory inputs.

Independent source-data verification remains pending.

### Strengths

- Applied the supplied replenishment formula.
- Correctly calculated all eight order quantities.
- Applied the non-negative quantity constraint.
- Identified conflicting overstock signals.
- Distinguished calculated and recommended quantities.
- Disclosed the discretionary nature of proposed holds.
- Maintained management approval requirements.

### Limitations

- Proposed reducing replenishment from 960 to 913 units
  without an established policy precedence rule.
- Introduced undefined purchasing priority categories.
- Produced an excessively detailed eleven-section report.
- Did not expose every calculation variable per SKU.
- Introduced an unnecessary interactive order selection.
- Did not explicitly reconcile all upstream input values.

### Business Rule Conflict

F02 Oxford Shirt and F04 Chinos were classified
as overstocked while generating positive
formula-based replenishment quantities.

The AI proposed reducing their recommended
orders from 30 and 17 units respectively to zero.

This was disclosed as an advisory adjustment,
not an authorised purchasing decision.

### Business Risks

AI-generated policy preferences may influence
management decisions without sufficient authority
or operational evidence.

Errors in upstream reports may propagate through
the replenishment workflow.

### Lesson Learned

Formula-based calculations must remain separate
from discretionary purchasing decisions.

Conflicting business policies require explicit
escalation and authorised human judgement.

### Planned Improvements

- Preserve original calculated quantities.
- Require SKU-level calculation traceability.
- Reconcile upstream reports against inventory inputs.
- Flag conflicting policy signals.
- Separate calculated quantities from approval status.
- Prevent unauthorised policy overrides.
- Standardise output and workflow handover.
## Version 1.1 — Retesting

### Test Environment

- Tool: ChatGPT Temporary Chat
- Input 1: P06 v1.1 stockout risk report
- Input 2: P07 v1.1 overstock assessment
- Input 3: Same Inventory screenshot
- Input 4: Same Business Rules screenshot
- Data source: Synthetic retail business scenario

### Observed Results

- Total distinct SKUs: 8
- Calculation consistency: 8/8
- Total formula-based replenishment: 960 units
- Stockout-risk replenishment: 795 units
- Policy conflict replenishment: 47 units
- Other replenishment: 118 units
- SKUs pending standard approval: 5
- Units pending standard approval: 913
- SKUs requiring policy decisions: 2
- SKUs with no order indicated: 1
- Not-assessable SKUs: 0
- Discretionary quantity adjustments: 0
- Reported source quantity discrepancies: 0
- Quantity reconciliation: PASS
- SKU reconciliation: PASS
- Report sections: 5
- Authorised purchasing quantity: 0

### Calculation Verification

| SKU | Calculated Units | Decision Status |
|---|---:|---|
| F01 | 310 | PENDING APPROVAL |
| F02 | 30 | POLICY CONFLICT |
| F03 | 230 | PENDING APPROVAL |
| F04 | 17 | POLICY CONFLICT |
| F05 | 0 | NO ORDER INDICATED |
| F06 | 120 | PENDING APPROVAL |
| F07 | 118 | PENDING APPROVAL |
| F08 | 135 | PENDING APPROVAL |
| Total | 960 | NOT AUTHORISED |

All eight calculated quantities matched the
provisional reference calculations.

The non-negative quantity constraint was
correctly applied independently to each SKU.

Independent verification against the original
Inventory worksheet remains pending.

### Iteration Audit Log

| Change Made | Observed Effect |
|---|---|
| Required SKU-level input traceability | Presented all calculation variables |
| Introduced cross-source validation | Reported consistent input values |
| Preserved formula-based quantities | Retained the full 960 units |
| Defined decision statuses | Separated calculation from approval |
| Introduced policy conflict escalation | Preserved 47 conflicting units |
| Restricted decision authority | No discretionary quantity override |
| Required quantity reconciliation | All categories reconciled to 960 units |
| Standardised output structure | Reduced report from 11 sections to 5 |
| Defined P09 handover | Prepared consolidated findings |
| Required management approval | No purchasing authority exercised |

### Policy Conflict Evaluation

Version 1.0 calculated 960 units but proposed
reducing recommended replenishment to 913 units.

The 47-unit difference consisted of:

- F02 Oxford Shirt: 30 units
- F04 Chinos: 17 units

Version 1.1 retained both calculated quantities
and classified them as requiring a management
policy decision.

No policy precedence was assumed.

The 913 remaining positive units were classified
as pending standard approval rather than
approved purchase quantities.

### Prompt Chaining Evaluation

P08 consolidated the P06 stockout assessment,
P07 overstock assessment, inventory records
and business rules.

The revised output reported cross-source
consistency and prepared consolidated findings
for P09.

This was a manually coordinated prototype.
No automated workflow integration or purchasing
system execution was implemented.

### Evaluation Scores

| Criterion | v1.0 | v1.1 |
|---|---:|---:|
| Faithfulness | 4 | 4 |
| Completeness | 5 | 5 |
| Format Compliance | 3 | 5 |
| Business Usability | 4 | 4 |
| Risk Control | 3 | 5 |
| Total | 19/25 | 23/25 |

These are provisional qualitative evaluation
scores based on observed prototype outputs.

### Lesson Learned

Accurate calculations must be separated from
discretionary business decisions.

AI should identify and explain conflicting
business policies without independently
determining which policy takes precedence.

Prompt chaining improves workflow continuity
but may also propagate upstream errors.

Human approval remains essential for purchasing
and policy decisions.

### Remaining Limitations

- Testing was limited to one synthetic scenario.
- Independent source-data verification is pending.
- Conflicting source-data scenarios remain untested.
- Missing-input scenarios remain untested.
- Existing suggested-order discrepancies remain untested.
- Inventory snapshot timing remains unverified.
- Supplier constraints and purchasing budgets are unknown.
- No actual purchasing system integration.
- Prompt instructions do not enforce technical
  access controls or purchasing restrictions.
- Management approval remains outstanding.

### Final Decision

Retain v1.1 for the proposed prototype workflow
because it demonstrated stronger calculation
transparency, policy conflict escalation and
human decision authority control.
