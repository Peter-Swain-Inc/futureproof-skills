---
name: revenue-compounding-map
description: "Maps and quantifies revenue compounding dynamics across the business — identifying where retention loops, expansion triggers, referral flywheels, and pricing leverage stack to produce non-linear reven"
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="revenue-compounding-map")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any existing revenue metrics, ICA segmentation, pricing architecture, churn data, or prior growth analyses.

## Step 2: Get Input

Ask the user to provide:

- **Revenue model overview** — recurring revenue structure (subscription tiers, retainers, usage-based, hybrid), current ARR/MRR, and average revenue per account (ARPA)
- **Retention data** — gross and net revenue retention rates, churn rate by cohort or ICA segment if available, average customer lifetime in months
- **Expansion motion** — how do existing customers grow? (upsell tiers, cross-sell products, seat expansion, usage growth, price escalations)
- **Referral and earned growth** — do customers generate new customers? (formal referral programme, organic word-of-mouth, case study pipeline, partner channel)
- **ICA segments** — which customer segments are they serving, and which segments they believe compound fastest?
- **Known leaks** — where do they suspect revenue is decaying, stalling, or failing to compound? (e.g., high churn in a segment, flat expansion, zero referral activity)

If FutureProof context contains prior session data on their ICA, pricing, or revenue metrics, pre-populate and confirm rather than re-asking.

## Step 3: Do the Work — Revenue Compounding Layer Analysis

Analyse the business across **six compounding layers**, treating each as an independent growth rate that stacks multiplicatively over time:

### Layer 1: Base Retention Compounding
- Calculate the **revenue half-life** — at current gross retention rate, how many months until a cohort's revenue halves?
- Segment retention by ICA tier — identify which segments retain at >95% (compounding) vs. <85% (decaying)
- Model the **retention drag coefficient**: the annual revenue destroyed by churn that must be replaced before net growth begins

### Layer 2: Expansion Revenue Velocity
- Map all expansion pathways (upsell, cross-sell, seat expansion, usage growth, contractual price escalation)
- Calculate **net revenue retention (NRR)** and decompose it: what percentage of NRR above 100% comes from each expansion pathway?
- Identify the **expansion trigger map** — the specific customer milestones, usage thresholds, or time-based events that predict expansion
- Flag **dormant expansion pathways**: expansion motions that exist structurally but are not being activated (e.g., a premium tier nobody upgrades to)

### Layer 3: Pricing Leverage Compounding
- Assess whether pricing architecture compounds value capture over time (usage-based scaling, annual escalators, value-metric alignment) or remains flat
- Calculate the **price compounding rate**: the annualised rate at which ARPA grows for a customer who neither upgrades nor downgrades, purely through pricing mechanics
- Identify pricing structure leaks — unlimited plans that cap revenue, grandfathered pricing, missing value metrics

### Layer 4: Referral Flywheel Dynamics
- Map the **referral coefficient (k-factor)**: average number of new customers generated per existing customer per year
- Classify referral quality — do referred customers retain and expand at higher, equal, or lower rates than direct-acquisition customers?
- Assess referral **structural readiness**: is the referral pathway engineered (programmatic, incentivised, systematised) or accidental (organic, unmeasured)?
- Calculate **referral-attributed revenue** as a percentage of new ARR

### Layer 5: Cohort Compounding Behaviour
- Model revenue behaviour by acquisition cohort over 12, 24, and 36-month horizons
- Identify **compounding cohorts** (revenue per cohort increases over time) vs. **decaying cohorts** (revenue per cohort decreases despite retention)
- Determine whether newer cohorts compound faster or slower than older cohorts — this reveals whether the business model is improving or degrading

### Layer 6: Compounding Stack Rate (Composite)
- Calculate the **composite compounding rate**: the multiplicative effect of all six layers operating simultaneously
- Formula: `Composite Rate = Base Retention × (1 + Expansion Rate) × (1 + Price Compounding Rate) × (1 + Referral Growth Rate)`
- Model three scenarios over 36 months:
  - **Current trajectory** — all rates unchanged
  - **Leak-sealed trajectory** — fix the top 3 identified leaks
  - **Optimised trajectory** — activate dormant pathways + seal leaks

Apply any user-specific `instructions` from FutureProof context (e.g., preferred ICA focus, strategic priorities, board-reporting format requirements).

## Step 4: Deliver Output

Produce the **Revenue Compounding Map** — a structured strategic deliverable containing:

### 4.1 — Compounding Layer Scorecard

| Compounding Layer | Current Rate | Benchmark (Top Quartile SaaS) | Status | Priority |
|---|---|---|---|---|
| Base Retention | X% GRR | >95% | Compounding / Decaying / Stalled | P1–P3 |
| Expansion Revenue | X% NRR contribution | >120% NRR | Compounding / Decaying / Stalled | P1–P3 |
| Pricing Leverage | X% annual ARPA growth | 3–7% annual | Compounding / Decaying / Stalled | P1–P3 |
| Referral Flywheel | X k-factor | 0.15–0.30 | Active / Dormant / Absent | P1–P3 |
| Cohort Behaviour | Expanding / Flat / Contracting | Expanding | Compounding / Decaying / Stalled | P1–P3 |
| **Composite Stack Rate** | **X% annualised** | **>140% revenue efficiency** | — | — |

### 4.2 — Revenue Compounding Map (Visual Specification)

A structured diagram specification showing:
- Each compounding layer as a loop with its rate and directionality (compounding ↑, leaking ↓, stalled →)
- Interaction points between layers (e.g., expansion increases retention, referrals improve cohort quality)
- Leak points marked in red with estimated annual revenue impact

### 4.3 — Top 5 Compounding Leaks (Ranked by Revenue Impact)

For each leak:
- **Leak description** — precisely what is happening and in which layer
- **Annual revenue impact** — estimated ARR destroyed or forgone over 12 months
- **Root cause** — structural, operational, or strategic
- **Remediation action** — specific, implementable intervention (not generic advice)
- **Expected compounding effect** — how fixing this leak changes the composite rate

### 4.4 — 36-Month Revenue Projection Model

Three-scenario table:
- **Scenario A (Current Trajectory)**: projected ARR at months 12, 24, 36
- **Scenario B (Leaks Sealed)**: projected ARR with top 3 leaks fixed, quantified delta vs. Scenario A
- **Scenario C (Fully Optimised)**: projected ARR with all layers actively compounding, quantified delta vs. Scenario A
- **Compounding gap**: the cumulative revenue difference between Scenario A and Scenario C — this is the cost of inaction

### 4.5 — Compounding Acceleration Roadmap

A sequenced 90-day action plan:
- **Days 1–30**: Seal the highest-impact leak (specific actions, owners where identifiable, success metric)
- **Days 31–60**: Activate the highest-potential dormant compounding pathway
- **Days 61–90**: Instrument measurement for all six layers to enable ongoing compounding tracking

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="revenue-compounding-map", experiment={
  hypothesis: "Activating the dormant expansion trigger (identified in Layer 2) for the highest-ARPA ICA segment will increase net revenue retention by 8–12 points within one quarter",
  variants: ["control: current expansion motion with no proactive trigger", "variant: proactive expansion outreach at identified usage threshold"],
  measurement: "Net revenue retention rate for target ICA segment, measured at 90 days post-implementation",
  expected_impact: "5–12% increase in NRR, translating to estimated $[X] incremental ARR over 12 months through compounding"
})
```

```
FutureProof:save_experiment(skill="revenue-compounding-map", experiment={
  hypothesis: "Introducing a structured referral programme for the highest-retention ICA segment will generate a referral coefficient of 0.10–0.20 within two quarters, producing a self-reinforcing acquisition loop",
  variants: ["control: no formal referral mechanism", "variant: programmatic referral with reciprocal incentive tied to account credit"],
  measurement: "Referral-attributed new ARR and referred-customer 90-day retention rate",
  expected_impact: "10–20% reduction in blended customer acquisition cost and 0.10+ k-factor contribution to composite compounding rate"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="revenue-compounding-map",
  query="Latest benchmarks for SaaS net revenue retention by segment, expansion revenue patterns, and referral coefficient data from 2024 cohort analyses — including emerging pricing models that structurally compound ARPA over time",
  reason="Ensure compounding layer benchmarks and remediation recommendations reflect current market dynamics rather than outdated 2020–2022 growth-at-all-costs norms"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="revenue-compounding-map", session={
  summary: "Built Revenue Compounding Map for [business name/type] across six compounding layers — retention, expansion, pricing leverage, referral flywheel, cohort behaviour, and composite stack rate",
  key_findings: ["Primary compounding leak identified in [layer] with estimated $[X] annual impact", "Dormant compounding pathway in [layer] represents highest-leverage activation opportunity", "Composite compounding rate of [X%] vs. top-quartile benchmark of [Y%] — [Z]pp gap addressable within 90 days"],
  deliverables_produced: ["Compounding Layer Scorecard", "Revenue Compounding Map (visual specification)", "Top 5 Compounding Leaks analysis", "36-Month Revenue Projection Model (3 scenarios)", "90-Day Compounding Acceleration Roadmap"],
  user_feedback: null
})
```