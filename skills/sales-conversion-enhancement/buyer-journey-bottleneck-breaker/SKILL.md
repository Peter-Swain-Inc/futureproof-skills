---
name: buyer-journey-bottleneck-breaker
description: |
  Diagnoses and resolves conversion bottlenecks across every stage of the buyer journey using FutureProof context, historical experiment data, and structured diagnostic frameworks.
  Trigger: when a user describes a stalled pipeline, drop-off between funnel stages, or asks why prospects are not converting from one buyer journey stage to the next.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="buyer-journey-bottleneck-breaker")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to previously identified bottlenecks, ICA definitions, offer architecture, and any prior funnel diagnostics to avoid redundant analysis.

## Step 2: Get Input

Ask the user to provide:

1. **Buyer journey map or funnel definition** — the discrete stages prospects move through (e.g., Awareness → Interest → Evaluation → Decision → Close → Onboarding). If none exists, co-create one before proceeding.
2. **Stage-by-stage conversion data** — volume and conversion rate at each transition. Acceptable formats: spreadsheet, CRM export, dashboard screenshot, or verbal estimates with confidence levels.
3. **ICA definition** — who is the ideal buyer? Confirm segment, role, buying authority, and primary pain. Cross-reference with any ICA stored in FutureProof context.
4. **Suspected bottleneck** — where do they *believe* the problem is? (Record this separately to test against diagnostic findings.)
5. **Revenue context** — average deal value, sales cycle length, and current pipeline velocity so impact can be quantified in currency, not just percentages.

If the user cannot provide conversion data, switch to qualitative diagnostic mode: gather last 5 lost-deal narratives and primary objection themes instead.

## Step 3: Do the Work — Bottleneck Diagnostic

Execute a four-layer diagnostic framework:

### 3A: Conversion Waterfall Analysis

Build a **stage-over-stage conversion waterfall** from the data provided:

| Stage Transition | Volume In | Volume Out | Conversion Rate | Benchmark | Variance |
|---|---|---|---|---|---|
| Awareness → Interest | — | — | — | — | — |
| Interest → Evaluation | — | — | — | — | — |
| Evaluation → Decision | — | — | — | — | — |
| Decision → Close | — | — | — | — | — |
| Close → Onboarding | — | — | — | — | — |

Apply industry benchmarks from FutureProof context or research. Flag any transition performing ≥20% below benchmark as a **critical bottleneck** and any ≥10% below as a **watch zone**.

### 3B: Root Cause Classification

For each critical bottleneck, classify the root cause using the **FMOT Framework** (Five Moments of Truth):

1. **Message–Market Misalignment** — the value proposition does not resonate with the ICA at this stage
2. **Friction Overload** — too many steps, forms, meetings, or decisions required to advance
3. **Trust Deficit** — insufficient proof, authority, or social validation for the commitment level being asked
4. **Timing Disconnect** — the prospect is being asked to act before urgency or readiness is established
5. **Competitive Displacement** — a rival alternative (including inaction) is winning the comparison at this stage

Assign a primary and secondary root cause to each bottleneck. Reference any objection patterns or lost-deal reasons from FutureProof `recent_sessions` to validate classification.

### 3C: Impact Quantification

For each bottleneck, calculate:

- **Revenue leak**: (lost volume at bottleneck) × (average deal value) × (historical close rate from that stage forward)
- **Velocity drag**: estimated days added to sales cycle due to bottleneck friction
- **Cumulative pipeline impact**: compound effect of fixing this bottleneck on downstream stages

Rank bottlenecks by **revenue leak × feasibility of fix** to produce a prioritised action list.

### 3D: ICA Journey Empathy Map

For the #1 bottleneck, construct a micro-empathy map of the ICA *at that exact stage*:

- **Thinking**: What questions are unresolved?
- **Feeling**: What fear, doubt, or competing priority dominates?
- **Doing**: What actions (or inactions) are observable?
- **Needing**: What would move them forward with confidence?

Apply any ICA-specific `instructions` from FutureProof context to deepen this analysis beyond generic archetypes.

## Step 4: Deliver Output

Produce the **Buyer Journey Bottleneck Diagnostic Report** containing:

### Section 1: Executive Summary
- Number of critical bottlenecks identified
- Total estimated monthly revenue leak across all bottlenecks
- Single highest-impact fix with projected uplift

### Section 2: Conversion Waterfall (completed table from 3A)

### Section 3: Bottleneck Deep Dives (one per critical bottleneck)
Each includes:
- Stage transition and current conversion rate vs. benchmark
- Root cause classification with supporting evidence
- Revenue leak and velocity drag calculations
- ICA empathy map (for #1 bottleneck)

### Section 4: Prescriptive Action Plan
For each bottleneck, provide **three specific interventions** ranked by impact:

- **Intervention description** — concrete action, not a vague recommendation (e.g., "Replace the 45-minute discovery call with a 12-minute async video qualification using Loom, gated by a 3-question intake form that pre-qualifies budget authority" — not "streamline the discovery process")
- **Asset or deliverable required** — name the exact asset to create (e.g., "ICA Pain-First Case Study One-Pager", "Objection Pre-emption Email Sequence — 3 emails", "ROI Calculator Spreadsheet for CFO Stakeholder")
- **Owner** — recommended function or role responsible (e.g., Sales Enablement, Product Marketing, AE)
- **Expected conversion lift** — percentage improvement estimate with reasoning
- **Implementation priority** — Immediate (this week), Short-term (30 days), Strategic (quarterly)

### Section 5: Quick-Win Rewrite
Rewrite or create the single most impactful asset identified in the action plan — in full, ready-to-deploy form. This may be a follow-up email, landing page section, objection-handling script, proposal template section, or qualification framework depending on where the bottleneck sits.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="buyer-journey-bottleneck-breaker", experiment={
  hypothesis: "Addressing [root cause] at [bottleneck stage] by implementing [intervention] will increase stage conversion rate from [current]% to [target]%",
  variants: ["control: current journey experience at bottleneck stage", "variant: journey with intervention deployed"],
  measurement: "Stage conversion rate tracked over 30-day window or minimum 50 prospects passing through stage, whichever comes first",
  expected_impact: "[X]% conversion lift at bottleneck stage, translating to approximately $[Y] additional monthly revenue at current pipeline volume",
  review_date: "30 days from implementation"
})
```

Generate one experiment per critical bottleneck identified (minimum 1, maximum 3). Each experiment must have a falsifiable hypothesis and a concrete measurement protocol.

## Step 6: Request Research

```
FutureProof:request_research(skill="buyer-journey-bottleneck-breaker",
  query="Current conversion benchmarks and buyer psychology patterns for [user's industry/segment] buyer journeys 2024–2025, with emphasis on [primary root cause category] reduction tactics",
  reason="Ensure bottleneck benchmarks and intervention recommendations reflect current buyer behaviour shifts, not legacy funnel assumptions. Priority: stage-specific conversion benchmarks for the user's ICA segment and emerging friction-reduction patterns."
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="buyer-journey-bottleneck-breaker", session={
  summary: "Diagnosed buyer journey bottlenecks for [ICA segment] across [number]-stage funnel. Identified [number] critical bottlenecks with total estimated revenue leak of $[amount]/month.",
  key_findings: [
    "Primary bottleneck at [stage] → [stage] transition ([current]% vs [benchmark]% benchmark) — root cause: [classification]",
    "Highest-impact intervention: [brief description] — projected [X]% conversion lift",
    "Total addressable revenue recovery: $[amount]/month if top 2 bottlenecks resolved"
  ],
  bottlenecks_identified: ["stage transition 1", "stage transition 2"],
  interventions_prescribed: ["intervention 1", "intervention 2", "intervention 3"],
  experiments_proposed: [number],
  user_feedback: null
})
```