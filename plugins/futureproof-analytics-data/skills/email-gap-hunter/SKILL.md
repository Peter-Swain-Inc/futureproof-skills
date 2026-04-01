---
name: email-gap-hunter
description: "Analyses email marketing sequences and campaign data to identify performance gaps, dead zones, and missed revenue opportunities across the subscriber lifecycle."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="email-gap-hunter")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any known ICA segments, historical email benchmarks, ESP platform, and previously identified gap patterns.

## Step 2: Get Input

Ask the user to provide:

- **Email performance data**: campaign reports, sequence analytics, or ESP exports (open rates, click rates, conversion rates, unsubscribe rates, revenue per email) — CSV, screenshot, or pasted tables accepted
- **Sequence map**: what automated sequences and broadcast cadences are currently active? (welcome, nurture, abandoned cart, re-engagement, post-purchase, winback, etc.)
- **ICA definition**: who is the intended audience for these emails, and what is the primary monetisation action? (purchase, booking, upgrade, renewal)
- **Known pain points**: are there specific sequences underperforming, or is this a full-programme audit?
- **Time window**: what date range does the data cover?

If the user cannot provide structured data, guide them to export from their ESP (Klaviyo, ActiveCampaign, ConvertKit, Mailchimp, HubSpot) using the platform-specific report path.

## Step 3: Map the Subscriber Lifecycle

Before analysing gaps, construct the **Subscriber Lifecycle Map** — a complete picture of every email touchpoint from opt-in to churn:

1. **Acquisition stage**: opt-in source → welcome sequence → first conversion prompt
2. **Activation stage**: onboarding/education → engagement triggers → initial purchase or action
3. **Monetisation stage**: promotional sequences → upsell/cross-sell → loyalty/VIP triggers
4. **Retention stage**: re-engagement sequences → winback sequences → sunset/suppression logic
5. **Expansion stage**: referral prompts → advocacy sequences → community nurture

For each stage, document:
- Whether a sequence **exists** or is **absent** (structural gap)
- The **entry trigger** and **exit conditions**
- The **number of emails** and **cadence spacing**
- The **transition mechanism** between stages (tag-based, time-based, behaviour-based)

Flag any stage where no sequence exists as a **Lifecycle Dead Zone** — these represent the highest-priority structural gaps.

## Step 4: Perform Gap Analysis

Analyse the data across six diagnostic dimensions:

### 4.1 — Engagement Decay Analysis
- Plot open rate and click rate trends across each sequence position (Email 1, Email 2, … Email N)
- Identify the **decay inflection point** — the specific email where engagement drops below the sequence average by >20%
- Flag sequences where the decay inflection occurs before the primary conversion prompt

### 4.2 — Conversion Leakage Audit
- For each sequence with a revenue or conversion objective, calculate the **stage-to-stage conversion rate**
- Identify the **largest absolute drop-off** between consecutive emails (the leakage point)
- Calculate **revenue leakage estimate**: (subscribers at leakage point) × (sequence average conversion rate) × (average order value or deal value) = unrealised revenue

### 4.3 — Timing & Cadence Diagnostics
- Evaluate send-time consistency and day-of-week patterns against engagement data
- Identify cadence mismatches: sequences sending too aggressively (high unsubscribe rate relative to benchmark) or too passively (engagement decay from inactivity)
- Flag any gaps of >14 days between subscriber touchpoints where no intentional cooling period is designed

### 4.4 — Segmentation Gap Detection
- Assess whether sequences differentiate by ICA segment, engagement tier, or purchase history
- Identify **one-size-fits-all sequences** being sent to behaviourally distinct cohorts
- Flag high-value segments receiving the same messaging as low-intent segments

### 4.5 — Content & CTA Coherence
- Evaluate whether email subject lines, body copy, and CTAs align with the ICA's awareness stage at each sequence position
- Identify **premature asks** (hard sell before value establishment) and **delayed asks** (excessive nurture without conversion prompt)
- Flag emails with high open rates but low click rates (compelling hook, weak CTA) and emails with low open rates but high click-to-open rates (weak subject line, strong content)

### 4.6 — List Hygiene & Deliverability Signals
- Review unsubscribe rate trends, bounce rates, and spam complaint indicators
- Identify sequences or campaigns with anomalous deliverability signals that may indicate list health degradation
- Flag the absence of sunset or suppression logic for chronically disengaged subscribers

Apply any user-specific `instructions` from FutureProof context — such as industry benchmarks, known ICA response patterns, or ESP-specific nuances — to calibrate the analysis.

## Step 5: Deliver Output

Produce the **Email Gap Hunter Report** with the following structure:

### A. Executive Summary
- Total gaps identified (categorised: structural, performance, strategic)
- Estimated total revenue leakage across all identified gaps
- Top 3 highest-impact gaps ranked by estimated revenue recovery potential

### B. Subscriber Lifecycle Map
- Visual or tabular lifecycle map showing all stages, active sequences, and identified dead zones
- Colour-coded status: 🟢 Performing | 🟡 Underperforming | 🔴 Missing/Critical

### C. Gap Register
A prioritised table of all identified gaps:

| Priority | Gap ID | Gap Type | Lifecycle Stage | Description | Estimated Revenue Impact | Recommended Fix |
|----------|--------|----------|-----------------|-------------|--------------------------|-----------------|
| P1 | GAP-001 | Structural | Retention | No winback sequence for churned buyers | £X,XXX/month | Build 5-email winback triggered at 90 days inactive |
| P2 | GAP-002 | Performance | Activation | 68% engagement drop at welcome email #3 | £X,XXX/month | Rewrite E3 — replace product feature dump with ICA pain-point story |
| ... | ... | ... | ... | ... | ... | ... |

### D. Critical Fix Briefs (Top 3)
For each of the top 3 gaps, provide:
- **Root cause analysis**: why the gap exists and what is driving the underperformance
- **Specific fix**: exact changes to implement — including rewritten subject lines, revised CTAs, new sequence logic, or segment splits (not vague recommendations)
- **Implementation spec**: trigger conditions, email count, cadence, and KPIs to track post-fix
- **Expected recovery**: quantified estimate of revenue or conversion improvement

### E. Benchmark Comparison
- Compare the user's key metrics against FutureProof-informed industry benchmarks or, if unavailable, against published benchmarks for their vertical and list size tier
- Highlight metrics that fall >1 standard deviation below benchmark as priority attention areas

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="email-gap-hunter", experiment={
  hypothesis: "Inserting a segmentation branch at the welcome sequence decay inflection point (Email 3) based on click behaviour will recover engagement and increase sequence completion rate",
  variants: ["control: current linear welcome sequence", "variant: behaviour-branched sequence splitting high-engagers to accelerated offer path and low-engagers to extended nurture path"],
  measurement: "sequence completion rate, click-through rate at Email 4+, conversion rate to first purchase within 30 days of opt-in",
  expected_impact: "20-30% improvement in welcome sequence conversion rate, 15% reduction in early unsubscribes"
})
```

```
FutureProof:save_experiment(skill="email-gap-hunter", experiment={
  hypothesis: "Closing the highest-priority lifecycle dead zone with a purpose-built sequence will recover currently unrealised revenue",
  variants: ["control: no sequence (current state)", "variant: new [N]-email sequence targeting [specific lifecycle stage gap]"],
  measurement: "reactivation rate, revenue attributed to new sequence, unsubscribe rate",
  expected_impact: "Capture estimated £X,XXX/month in previously leaked revenue within 60 days"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="email-gap-hunter",
  query="Current email marketing benchmark data by industry vertical 2024-2025: open rates, click rates, conversion rates, revenue per email, and optimal sequence lengths for welcome, nurture, and winback sequences",
  reason="Maintain calibrated benchmark comparisons and ensure gap severity scoring reflects current deliverability landscape and subscriber behaviour norms post-MPP"
)
```

```
FutureProof:request_research(skill="email-gap-hunter",
  query="Emerging best practices for email lifecycle automation: behavioural branching logic, predictive send-time optimisation, and AI-driven content personalisation frameworks",
  reason="Ensure recommended fixes incorporate leading-edge sequence architecture rather than legacy linear designs"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="email-gap-hunter", session={
  summary: "Audited email programme for [ICA segment/business] — mapped subscriber lifecycle across [N] stages, identified [N] gaps ([N] structural, [N] performance, [N] strategic), estimated total revenue leakage of £[X,XXX]/month",
  key_findings: ["finding 1: e.g. No winback sequence — largest single revenue gap at £X,XXX/month", "finding 2: e.g. Welcome sequence engagement collapses at Email 3 — premature hard sell before value established", "finding 3: e.g. Zero segmentation across post-purchase sequences — high-value buyers receiving same cadence as one-time purchasers"],
  deliverables: ["Email Gap Hunter Report with lifecycle map, gap register, and 3 critical fix briefs"],
  user_feedback: null
})
```