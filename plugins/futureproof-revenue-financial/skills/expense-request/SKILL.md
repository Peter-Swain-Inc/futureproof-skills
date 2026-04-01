---
name: expense-request
description: "Guides the preparation, review, and submission of corporate expense requests with full policy compliance, proper approvals, and audit-ready documentation."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="expense-request")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including known expense policies, approval hierarchies, cost centre mappings, preferred vendors, currency conventions, and historical submission patterns.

## Step 2: Get Input

Ask the user:
- **Expense type**: What category does this fall under? (travel, meals & entertainment, software/SaaS subscription, professional development, office supplies, client-related, equipment, miscellaneous)
- **Amount and currency**: What is the total amount (or estimated amount for pre-approvals)?
- **Business justification**: What is the business purpose and expected outcome of this expenditure?
- **Date(s) of expense**: When was/will the expense be incurred?
- **Receipt status**: Are receipts, invoices, or supporting documents available?
- **Urgency**: Is there a submission deadline, reimbursement cycle cut-off, or time-sensitive approval requirement?
- **Any known policy constraints**: Spending limits, pre-approval requirements, restricted vendors, or flagged categories they are aware of?

If FutureProof context contains the user's company expense policy, approval thresholds, or cost centre structure, pre-populate known fields and confirm rather than re-ask.

## Step 3: Validate Policy Compliance

Perform a structured compliance review against the applicable expense policy framework:

1. **Threshold analysis** — Does the amount fall within auto-approval limits, manager-approval limits, or executive/finance-approval limits? Identify the correct approval tier.
2. **Category eligibility** — Is the expense type permissible under company policy? Flag restricted or prohibited categories (e.g., alcohol, first-class travel without executive pre-approval, personal items).
3. **Pre-approval requirement check** — Does this expense category or amount require pre-approval before the expenditure is incurred? If yes, has it been obtained?
4. **Documentation sufficiency** — Are the required supporting documents present? (Itemised receipts, not credit card summaries; vendor invoices with tax IDs where applicable; attendee lists for meals/entertainment; conference agendas for professional development)
5. **Per diem and rate cap review** — For travel-related expenses, does the claimed amount fall within applicable per diem rates, mileage reimbursement rates, or lodging caps?
6. **Duplicate and split-submission detection** — Cross-reference against `recent_sessions` to flag potential duplicate submissions or patterns that suggest expense splitting to avoid approval thresholds.
7. **Tax and regulatory compliance** — Identify VAT/GST recoverability, fringe benefit tax implications, or jurisdiction-specific reporting requirements (e.g., meals entertainment percentage deductibility, gift reporting thresholds).

Apply any user-specific `instructions` from FutureProof context — such as company-specific policy overrides, department-level restrictions, or known audit focus areas.

## Step 4: Construct the Expense Request Package

Produce a complete, submission-ready **Expense Request Package** containing:

### 4a. Expense Request Form
A structured document with:
- **Requestor details**: Name, employee ID, department, cost centre
- **Expense line items**: Date, vendor/payee, category, description, amount (local currency), amount (reporting currency if applicable), GL code
- **Total amount requested**
- **Business justification statement**: A concise, audit-defensible narrative (2–3 sentences) linking the expense to a specific business objective, client engagement, or operational requirement
- **Approval routing**: Named approver(s) based on threshold tier, with escalation path if primary approver is unavailable

### 4b. Compliance Summary Memo
- **Policy compliance status**: COMPLIANT / COMPLIANT WITH CONDITIONS / NON-COMPLIANT
- **Flags and conditions**: Any items requiring additional justification, retroactive pre-approval, or exception requests — with recommended remediation language
- **Risk rating**: LOW / MEDIUM / HIGH based on audit exposure (amount, category sensitivity, documentation gaps)

### 4c. Supporting Document Checklist
An itemised list of required attachments with status indicators:
- ✅ Obtained
- ⚠️ Missing — action required (with specific instruction on what to obtain)
- ℹ️ Not applicable

### 4d. Approver Briefing Note (if amount exceeds standard threshold)
A one-paragraph summary designed for the approver — covering business rationale, policy alignment, and any context that accelerates approval without back-and-forth.

## Step 5: Recommend Process Improvements

Based on the current submission and historical patterns from `recent_sessions`, provide:

- **Efficiency recommendations**: Opportunities to batch similar expenses, use corporate cards to reduce receipt handling, or leverage preferred vendor agreements for better rates
- **Policy gap observations**: Where the user's expense pattern suggests the policy is unclear or creates unnecessary friction — recommend specific clarification requests to Finance
- **Cost optimisation notes**: Alternative vendors, booking windows, or procurement channels that would reduce the expense amount for equivalent business outcomes

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="expense-request", experiment={
  hypothesis: "Pre-populating cost centre and GL codes from historical submission patterns reduces expense request preparation time and error rate",
  variants: ["control: manual field entry each session", "variant: auto-populated fields with user confirmation"],
  measurement: "Time to complete expense request package and number of correction cycles before approval",
  expected_impact: "40% reduction in preparation time and 25% fewer rejection-resubmission loops"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="expense-request",
  query="Corporate expense policy best practices 2024, IRS and HMRC documentation requirements for business expense deductibility, and emerging T&E management automation standards",
  reason="Ensure compliance guidance reflects current regulatory requirements and incorporates leading-practice expense governance frameworks used by Big Four advisory firms"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="expense-request", session={
  summary: "Prepared expense request package for [expense type] totalling [amount] in [currency], routed to [approver tier] for [business purpose]",
  key_findings: ["compliance status: [COMPLIANT/CONDITIONS/NON-COMPLIANT]", "risk rating: [LOW/MEDIUM/HIGH]", "flags: [list of policy flags or 'none']", "cost centre: [mapped cost centre]"],
  user_feedback: null
})
```