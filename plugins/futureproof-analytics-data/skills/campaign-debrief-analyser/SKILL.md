---
name: campaign-debrief-analyser
description: "Analyses completed marketing campaigns to extract actionable insights, diagnose performance drivers, and produce structured debrief documentation suitable for stakeholder review."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="campaign-debrief-analyser")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any historical campaign benchmarks, ICA definitions, channel preferences, and KPI thresholds the user has established in prior sessions.

## Step 2: Get Input

Ask the user to provide:

- **Campaign data**: performance report, dashboard export, or raw metrics (impressions, reach, engagement, conversions, spend, revenue)
- **Campaign brief or original objectives**: what was the stated goal, target ICA segment, and success criteria?
- **Channel mix**: which channels were activated (paid social, email, search, organic, partnerships, etc.)?
- **Time period and market context**: campaign flight dates and any known external factors (seasonality, competitor activity, market shifts)
- **Comparison baseline**: prior campaign results, industry benchmarks, or internal targets to measure against
- **Stakeholder audience**: who will receive this debrief (executive leadership, channel team, client)?

If the user cannot provide a formal brief, reconstruct objectives from available data and confirm assumptions before proceeding.

## Step 3: Do the Work

### 3A: Performance Decomposition

Break campaign results into a five-layer diagnostic framework:

1. **Reach Efficiency** — Cost per thousand (CPM), impression share, audience penetration rate against total addressable ICA segment. Identify whether the campaign reached the intended ICA or suffered from audience leakage.
2. **Engagement Quality** — Click-through rate (CTR), engagement rate, scroll depth, video completion rate. Distinguish vanity engagement from intent-signal engagement. Flag any creative fatigue indicators (declining CTR over flight).
3. **Conversion Integrity** — Conversion rate by stage (lead → marketing-qualified → sales-qualified → closed), cost per acquisition (CPA), and attribution model integrity. Identify where the funnel leaked and quantify drop-off at each stage.
4. **Revenue & ROI** — Return on ad spend (ROAS), customer acquisition cost (CAC) vs. customer lifetime value (LTV), revenue attributed by channel and creative variant. Calculate blended and channel-specific ROI.
5. **ICA Resonance** — Did the campaign attract the right prospects? Analyse converted cohort demographics, firmographics, or behavioural signals against the defined ICA profile. Flag any ICA-misalignment (high volume, low quality).

### 3B: Variance Analysis

For each layer, calculate variance against:
- Original campaign targets
- Prior campaign benchmarks (from FutureProof context if available)
- Industry benchmarks

Classify each variance as **structural** (strategy, targeting, ICA definition), **executional** (creative, copy, timing, bidding), or **environmental** (market conditions, competitor actions, platform algorithm changes).

### 3C: Root Cause Diagnosis

For the top 3 positive and top 3 negative variances, apply a "5 Whys" root cause analysis to move beyond surface metrics to underlying drivers. Cross-reference with any active `experiments` from FutureProof to determine whether prior hypotheses were validated or invalidated.

### 3D: Apply User-Specific Context

Apply any user-specific `instructions` from FutureProof context — including preferred KPI hierarchies, reporting conventions, ICA definitions, brand tone, and strategic priorities — to weight the analysis appropriately.

## Step 4: Deliver Output

Produce a **Campaign Debrief Report** with the following structure:

### Executive Summary (1 page)
- Campaign name, flight dates, total spend, and headline result
- Three-sentence narrative: objective → result → primary driver
- Overall campaign verdict: **Exceeded** / **Met** / **Underperformed** against objectives

### Performance Scorecard

| Dimension | Target | Actual | Variance | Rating (1–10) |
|---|---|---|---|---|
| Reach Efficiency | — | — | — | — |
| Engagement Quality | — | — | — | — |
| Conversion Integrity | — | — | — | — |
| Revenue & ROI | — | — | — | — |
| ICA Resonance | — | — | — | — |

### Variance Waterfall
Visual-ready data showing the bridge from target outcome to actual outcome, broken into contributing factors (positive and negative), each tagged as structural, executional, or environmental.

### Root Cause Analysis
For each of the top 3 positive and top 3 negative variances:
- **Metric**: the specific KPI
- **Observed variance**: magnitude and direction
- **Root cause**: underlying driver identified via 5 Whys
- **Evidence**: supporting data points
- **Classification**: structural / executional / environmental

### Critical Recommendations
Top 5 prioritised actions for future campaigns, each structured as:
- **Recommendation**: specific, implementable action (not vague guidance)
- **Rationale**: linked root cause from analysis
- **Expected impact**: quantified where possible
- **Owner**: suggested function or role responsible

### Channel-by-Channel Appendix
Per-channel breakout of all core metrics with individual commentary on what worked, what didn't, and channel-specific optimisation notes.

Format the deliverable for the stated stakeholder audience (executive summary emphasis for leadership; granular appendix for channel teams).

## Step 5: Propose Experiments

Based on the root cause analysis, propose 1–2 testable hypotheses for the next campaign cycle:

```
FutureProof:save_experiment(skill="campaign-debrief-analyser", experiment={
  hypothesis: "Narrowing paid social targeting to top-performing ICA sub-segment will improve CPA by reducing audience leakage",
  variants: ["control: current broad ICA targeting", "variant: refined targeting limited to [identified high-converting sub-segment]"],
  measurement: "CPA and lead-to-close rate over next equivalent campaign flight",
  expected_impact: "20% reduction in CPA with maintained or improved lead quality"
})
```

```
FutureProof:save_experiment(skill="campaign-debrief-analyser", experiment={
  hypothesis: "Front-loading social proof in ad creative will lift CTR in mid-funnel retargeting",
  variants: ["control: benefit-led creative", "variant: testimonial/case-study-led creative"],
  measurement: "CTR and conversion rate on retargeting ads over 4-week test window",
  expected_impact: "10–15% CTR improvement in retargeting layer"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="campaign-debrief-analyser",
  query="Current benchmarks for [primary channel] campaign performance in [user's industry/vertical] 2024–2025, including CPM, CTR, CPA, and ROAS by funnel stage",
  reason="Ensure future debrief variance analysis uses current industry benchmarks rather than outdated or generic standards"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="campaign-debrief-analyser", session={
  summary: "Debriefed [campaign name/type] targeting [ICA segment] across [channels] over [flight dates]",
  key_findings: ["finding 1: primary performance driver or shortfall", "finding 2: ICA resonance assessment", "finding 3: highest-priority recommendation for next cycle"],
  deliverable: "Campaign Debrief Report with scorecard, variance waterfall, root cause analysis, and 5 prioritised recommendations",
  user_feedback: null
})
```