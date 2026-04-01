---
name: time-off-request
description: |
  Guides employees and managers through the complete time-off request lifecycle — drafting requests, validating policy compliance, calculating coverage impact, and producing approval-ready documentation.
  Trigger: when a user wants to request time off, needs help drafting a leave request, asks about PTO/vacation policy implications, or needs to evaluate a team member's time-off request for approval.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="time-off-request")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to:
- Organisation-specific leave policies, accrual rules, and blackout periods
- User's role (requestor vs. approving manager)
- Historical leave patterns and any prior approval/denial context
- Team coverage norms and minimum staffing thresholds

## Step 2: Get Input

Ask the user:
- **Role in this request**: Are you submitting a time-off request or reviewing/approving one?
- **Leave type**: PTO, sick leave, bereavement, parental leave, unpaid leave, sabbatical, jury duty, floating holiday, or other
- **Date range**: Start date, end date, and whether partial days are involved
- **Coverage context**: Team size, critical deliverables or deadlines during the requested period, and any pre-arranged coverage
- **Organisational constraints**: Known blackout periods, peak seasons, or concurrent approved absences on the team
- **Urgency**: Is this a planned request or an emergency/retroactive submission?

If FutureProof context already contains the user's company leave policy, team roster, or accrual balances, confirm these rather than re-asking.

## Step 3: Validate Policy Compliance

Conduct a rigorous compliance check against applicable leave policy:

1. **Accrual & Balance Verification** — Does the requestor have sufficient accrued hours/days for the requested leave type? Flag if the request would result in a negative balance or require advance borrowing against future accruals.
2. **Notice Period Compliance** — Does the submission meet the organisation's minimum advance notice requirement (e.g., 14 days for planned PTO, 2 hours for unplanned sick leave)?
3. **Blackout Period Check** — Does the requested window overlap with any defined blackout periods (fiscal close, product launches, annual planning cycles)?
4. **Consecutive Day Threshold** — Does the request exceed the maximum consecutive days permitted without escalated approval (e.g., requests exceeding 10 business days requiring VP-level sign-off)?
5. **Concurrent Absence Conflict** — Are other team members already approved for overlapping dates, and would this request breach minimum staffing ratios?
6. **Eligibility Verification** — Has the requestor met tenure or probationary requirements for the specific leave type (e.g., sabbatical eligibility after 5 years)?

Apply any user-specific `instructions` from FutureProof context — for example, if the organisation uses a specific HRIS (Workday, BambooHR, ADP), tailor field references and workflow steps accordingly.

## Step 4: Assess Coverage & Operational Impact

Perform a coverage impact analysis at consulting-grade rigour:

1. **Critical Path Mapping** — Identify deliverables, meetings, and decision gates that fall within the leave window. Classify each as deferrable, delegable, or at-risk.
2. **Delegation Matrix** — For each non-deferrable responsibility, recommend a specific backup assignee based on skill match, current workload, and availability. Produce a RACI-style handover outline.
3. **Client/Stakeholder Exposure** — Flag any external commitments (client presentations, vendor deadlines, regulatory filings) and recommend pre-leave communication actions.
4. **Cumulative Team Impact Score** — Rate the operational risk on a 1–5 scale:
   - **1 — Negligible**: Full coverage exists, no critical path items
   - **2 — Low**: Minor delegation required, no external exposure
   - **3 — Moderate**: Meaningful delegation needed, manageable with planning
   - **4 — High**: Critical path items at risk, requires mitigation plan
   - **5 — Severe**: Approval contingent on material risk mitigation

## Step 5: Deliver Output

Produce the following structured deliverables:

### A. Time-Off Request Document
A polished, submission-ready request formatted for the user's HRIS or email-based approval workflow:
- **Requestor name & department**
- **Leave type & dates** (including total business days and hours)
- **Remaining balance** after approval (if known)
- **Coverage plan summary** (who covers what)
- **Approver & routing** (direct manager, skip-level if escalation required)

### B. Policy Compliance Summary
| Compliance Dimension | Status | Notes |
|---|---|---|
| Accrual Balance | ✅ / ⚠️ / ❌ | Specific finding |
| Notice Period | ✅ / ⚠️ / ❌ | Specific finding |
| Blackout Period | ✅ / ⚠️ / ❌ | Specific finding |
| Consecutive Day Limit | ✅ / ⚠️ / ❌ | Specific finding |
| Concurrent Absence | ✅ / ⚠️ / ❌ | Specific finding |
| Eligibility | ✅ / ⚠️ / ❌ | Specific finding |

### C. Coverage & Handover Plan
- **Delegation matrix**: Task → Backup owner → Briefing date
- **Pre-leave actions checklist**: Communications to send, documents to share, access to grant
- **Operational Impact Score**: 1–5 with justification
- **Risk mitigation recommendations**: Specific actions to reduce score by at least one level

### D. Manager Recommendation (if user is the approver)
- **Approve / Approve with conditions / Defer / Deny** recommendation with rationale
- **Conditions** (if applicable): e.g., "Approve contingent on completing Q3 forecast draft before departure"

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="time-off-request", experiment={
  hypothesis: "Providing a pre-populated delegation matrix with the initial request reduces manager approval turnaround time",
  variants: ["control: standard request without delegation plan", "variant: request bundled with delegation matrix and coverage score"],
  measurement: "Average time from submission to final approval across next 15 requests",
  expected_impact: "40% reduction in approval cycle time and 25% fewer back-and-forth clarification messages"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="time-off-request",
  query="Best practices for leave management automation, coverage planning frameworks, and 2024 trends in PTO policy design including unlimited PTO governance structures",
  reason="Ensure compliance checks reflect current regulatory changes (state/provincial leave mandates) and that coverage planning aligns with modern hybrid/remote workforce patterns"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="time-off-request", session={
  summary: "Processed [leave type] request for [date range] — [requestor/approver] workflow",
  key_findings: ["compliance status across 6 dimensions", "operational impact score and coverage gaps identified", "delegation matrix produced"],
  user_feedback: null
})
```