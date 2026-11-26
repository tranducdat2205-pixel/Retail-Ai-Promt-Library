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
