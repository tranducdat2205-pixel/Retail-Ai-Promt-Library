# Retail AI Workflow Documentation

## 1. Workflow Overview

The proposed workflow supports weekly retail sales
analysis, inventory management and management
decision-making through ten interconnected prompts.

The workflow is designed as a human-supervised
AI decision-support prototype.

Trigger: Weekly sales and inventory reporting cycle.

Primary users:
- Business Analyst
- Inventory Manager
- Purchasing Manager
- Senior Management

## 2. Workflow Architecture

| Stage | Prompts | Objective |
|---|---|---|
| Data Preparation | P01-P02 | Validate and standardise data |
| Sales Performance Analysis | P03-P05 | Evaluate sales performance and trends |
| Inventory Management | P06-P08 | Identify inventory risks and replenishment requirements |
| Management Decision Support | P09-P10 | Develop and communicate management recommendations |

## 3. Input and Output Dependencies

| Prompt | Required Input | Output | Downstream Destination |
|---|---|---|---|
| P01 | Raw Sales | Data validation report | P02 |
| P02 | Raw Sales, P01 report | Proposed corrections and approval status | Human reviewer |
| P03 | Validated Sales | Sales performance report | P04 |
| P04 | P03 report, Business Rules | KPI assessment | P09 |
| P05 | Validated Sales, Business Rules | Product sales trends | P09 |
| P06 | Validated Sales, Inventory, Business Rules | Stockout risk report | P08, P09 |
| P07 | Validated Sales, Inventory, Business Rules | Overstock assessment | P08, P09 |
| P08 | Inventory, Business Rules, P06, P07 | Calculated replenishment and policy conflicts | P09 |
| P09 | P04-P08 reports | Management action recommendations | P10 |
| P10 | P09 report | Executive summary | Senior Management |

## 4. Workflow Execution

### Stage 1: Data Preparation

P01 identifies missing values, duplicate records,
invalid numerical values and formatting inconsistencies.

P02 proposes corrections without independently
modifying unresolved source values.

Human verification is required before corrected
records can be released for downstream analysis.

During prototype testing, P02 returned a blocked
status because unresolved corrections required
human approval.

An independent synthetic Clean Sales worksheet
was therefore used to test downstream prompts.

This worksheet was not an approved output of P02.

### Stage 2: Sales Performance Analysis

P03 calculates sales performance across reporting
weeks, products and categories.

P04 evaluates performance against supplied
business targets.

P05 identifies increasing and decreasing
product sales trends.

The resulting KPI and trend reports are
provided to P09.

### Stage 3: Inventory Management

P06 identifies stockout risks using available
inventory, lead-time demand and safety stock.

P07 identifies overstock using the applicable
on-hand stock coverage threshold.

P08 combines inventory inputs with P06 and P07
to calculate replenishment quantities.

Conflicting inventory policies are escalated
rather than automatically resolved.

### Stage 4: Management Decision Support

P09 consolidates five analytical reports and
develops evidence-based management recommendations.

P10 converts these recommendations into a
concise executive briefing.

Senior management retains final decision authority.

## 5. Human Verification and Decision Gates

| Control Point | Required Review | Failure Response |
|---|---|---|
| After P01 | Verify identified data issues | Investigate flagged records |
| After P02 | Approve proposed corrections | Block downstream release |
| After P03-P05 | Verify calculations and reporting scope | Return for correction |
| After P06-P07 | Verify inventory inputs and classifications | Escalate discrepancies |
| After P08 | Review quantities and policy conflicts | Withhold purchasing approval |
| After P09-P10 | Review evidence and proposed actions | Revise or reject recommendations |

These controls represent proposed workflow
requirements rather than implemented technical
access controls.

## 6. Exception Handling

The workflow is designed to identify and escalate:

- Missing required input data.
- Invalid numerical values.
- Duplicate or conflicting SKU records.
- Undefined calculation denominators.
- Unresolved data corrections.
- Inconsistent upstream reports.
- Conflicting inventory policy signals.
- Missing management approval.

Affected calculations should not be presented
as reliable when mandatory inputs are unresolved.

## 7. Business Rule Conflict Example

P08 identified two products that were overstocked
while generating positive replenishment quantities.

| Product | Overstock Cover | Calculated Replenishment |
|---|---:|---:|
| Oxford Shirt | 5.00 weeks | 30 units |
| Chinos | 4.44 weeks | 17 units |

The revised prompt preserved the calculated
47 units and escalated the conflict.

P09 subsequently presented three management options:

- Retain the calculated proposals.
- Defer purchasing decisions.
- Commission an authorised policy review.

No option was selected or implemented by AI.

## 8. Automation Feasibility

| Business Stage | Automation Potential | Human Dependency |
|---|---|---|
| Data Preparation | High for detection | High for unresolved corrections |
| Sales Analysis | High for repetitive calculations | Verification required |
| Inventory Management | High for rule-based calculations | Policy and purchasing approval |
| Management Decision Support | High for report drafting | High for operational decisions |

A future implementation could integrate retail
databases, deterministic calculation services
and approval workflows.

Such integration was not implemented or tested
in this educational prototype.

## 9. Workflow Limitations

- Manually coordinated prompt chaining.
- Limited synthetic dataset.
- Potential propagation of upstream errors.
- Non-deterministic AI responses.
- Incomplete exception and adversarial testing.
- Independent source verification required.
- No live retail system integration.
- No automated purchasing authority.
- No measured commercial outcomes.

## 10. Final Workflow Principle

Generative AI supports analysis, reporting
and management decision-making.

Human reviewers remain responsible for
data integrity, policy interpretation,
financial commitments and authorised
operational decisions.
