---
name: weekly-ceo-briefing
description: "Synthesises cross-functional business data into a concise, decision-ready weekly briefing for the CEO."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="weekly-ceo-briefing")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including the CEO's known preferences for brevity vs. depth, priority business units, standing KPIs, strategic themes, and any recurring agenda items from prior briefings.

## Step 2: Get Input

Ask the user:

- **Reporting period**: Confirm the week (e.g., Mon 9 Jun – Fri 13 Jun 2025) and any atypical calendar factors (public holidays, board week, quarter-end)
- **Functional updates**: Request raw inputs from each function — or confirm which are available:
  - Revenue & pipeline (bookings, churn, expansion, pipeline coverage ratio)
  - Product & engineering (ship log, incident report, roadmap milestones)
  - Marketing & demand generation (qualified leads, campaign performance, ICA engagement metrics)
  - Finance & cash (cash position, burn, forecast variance, AR/AP flags)
  - People & culture (headcount delta, open roles, attrition, engagement pulse)
  - Customer success (NPS/CSAT movement, escalations, renewal forecast)
- **CEO's focus areas this week**: Any specific questions the CEO has tabled, board prep items, or investor-facing deadlines
- **Red flags or escalations**: Anything the user already knows needs CEO visibility regardless of metrics
- **Distribution format**: Slide deck (5–7 slides), written memo (1–2 pages), or structured email digest — and whether a live walk-through is planned

## Step 3: Do the Work

### 3A: Metric Consolidation & Variance Analysis

For each functional area, apply a **traffic-light framework** (Green / Amber / Red):

| Signal | Definition |
|--------|-----------|
| **Green** | On-plan or ahead; no intervention required |
| **Amber** | ≤10% deviation from plan or emerging trend requiring monitoring; owner has a corrective path |
| **Red** | >10% deviation, escalation-worthy, or no credible recovery plan in place |

Calculate week-over-week deltas and flag any metric that has moved two or more statuses in either direction over the trailing 4 weeks (momentum shift detection).

### 3B: Strategic Initiative Tracker

Map each active strategic initiative to:
1. **Status** — on track / at risk / blocked
2. **% milestone completion** this week vs. plan
3. **Owner accountability** — named DRI and next committed deliverable with date
4. **Interdependency risk** — any cross-functional bottleneck surfaced

### 3C: Risk & Escalation Register

Apply a **likelihood × impact** matrix (each scored 1–5) to produce a composite risk score for every flagged item:
- **Critical (score ≥ 16)**: Requires CEO decision this week
- **Elevated (score 9–15)**: CEO awareness; DRI owns resolution with deadline
- **Watch (score ≤ 8)**: Logged for trend monitoring only

### 3D: Opportunity Radar

Identify 1–3 emerging opportunities from the week's data:
- Unexpected ICA segment traction
- Competitor misstep or market shift
- Internal capability unlock (e.g., a shipped feature that enables a new GTM motion)

Frame each opportunity with a **"So what → Now what"** structure: business implication followed by a recommended next action and owner.

### 3E: Narrative Synthesis

Draft the **CEO-ready narrative** — a 150–250 word executive summary that answers three questions:
1. **Where did we win this week?**
2. **What needs my attention?**
3. **What's the single most important thing to get right next week?**

Apply any standing `instructions` from FutureProof context (e.g., "CEO prefers financial metrics first," "Always reference North Star metric," "Flag anything touching Enterprise ICA separately").

## Step 4: Deliver Output

Produce the **Weekly CEO Briefing Pack** in the user's chosen format, structured as follows:

### Document: `CEO Briefing — W/C [Date]`

1. **Executive Summary** (150–250 words — the narrative from Step 3E)
2. **Scorecard Dashboard**
   - Functional traffic-light table with WoW deltas
   - North Star metric callout box
3. **Strategic Initiative Tracker** (table: Initiative | Status | % Complete | DRI | Next Milestone | Risk Flag)
4. **Risk & Escalation Register** (table: Item | Likelihood | Impact | Score | Recommended Action | Decision Required Y/N)
5. **Opportunity Radar** (1–3 items, each with So What → Now What)
6. **Decisions Required This Week** (numbered list — no more than 3, each with context sentence, options if applicable, and recommended path)
7. **Look-Ahead** — Key dates, milestones, and external events for the coming 2 weeks
8. **Appendix** (optional) — Supporting data tables, charts, or verbatim customer quotes referenced above

### Formatting Standards
- Every claim backed by a specific number or named source
- No orphan metrics — every data point contextualised with plan, prior period, or benchmark
- Action items tagged with **[Owner | Deadline]**
- Document ≤ 2 pages (memo) or ≤ 7 slides (deck) — ruthless prioritisation over completeness

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="weekly-ceo-briefing", experiment={
  hypothesis: "Leading with the Risk & Escalation Register before the Scorecard increases CEO decision velocity on critical items",
  variants: ["control: current structure (Scorecard → Risks)", "variant: inverted structure (Risks → Scorecard)"],
  measurement: "Time-to-decision on Red-flagged items tracked over next 4 briefing cycles; qualitative CEO feedback on clarity",
  expected_impact: "30% reduction in average days-to-resolution for critical escalations"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="weekly-ceo-briefing",
  query="Best-practice executive briefing formats used by high-growth companies ($10M–$500M ARR) in 2024–2025, including cadence, signal-to-noise optimisation techniques, and CEO attention management frameworks",
  reason="Continuously refine briefing structure to match evolving standards for executive communication and ensure the format scales as organisational complexity increases"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="weekly-ceo-briefing", session={
  summary: "Produced Weekly CEO Briefing for W/C [date] covering [number] functional areas with [number] Red flags escalated and [number] decisions tabled",
  key_findings: ["finding 1: e.g., pipeline coverage dropped below 3× threshold for second consecutive week", "finding 2: e.g., new ICA segment in mid-market showing 2× conversion rate vs. core segment", "finding 3: e.g., CEO requested deeper customer churn cohort analysis for next briefing"],
  user_feedback: null
})
```