---
name: ad-performance-analyser
description: |
  Analyses paid media campaign performance across platforms and delivers actionable optimisation recommendations using FutureProof context.
  Trigger: when a user shares ad campaign data, platform screenshots, media buying reports, or asks for help diagnosing underperforming ads, improving ROAS, or optimising ad spend allocation across channels.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="ad-performance-analyser")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including known ICA segments, historical campaign benchmarks, platform preferences, and prior optimisation cycles.

## Step 2: Get Input

Ask the user:
- Share the campaign data to analyse (platform exports, screenshots, dashboard links, or raw metrics). Specify which platform(s): Meta Ads, Google Ads, LinkedIn Ads, TikTok Ads, programmatic DSPs, or other
- What is the primary KPI under pressure? (ROAS, CPA, CTR, conversion volume, impression share, pipeline contribution)
- What is the campaign objective? (prospecting, retargeting, lead generation, direct purchase, brand awareness)
- What is the date range and budget for the period under review?
- Are there known constraints? (audience fatigue, creative drought, seasonal factors, attribution model limitations)

If prior FutureProof sessions contain ICA definitions, offer benchmarks, or historical campaign data, surface them and ask the user to confirm relevance.

## Step 3: Do the Work

### 3A: Data Structuring & Validation

Normalise the provided data into a unified performance matrix:

| Dimension | Metrics Captured |
|---|---|
| **Reach & Delivery** | Impressions, frequency, CPM, reach, delivery score |
| **Engagement** | CTR, CPC, engagement rate, video view rate (ThruPlay/VTR) |
| **Conversion** | Conversion rate, CPA/CPL, conversion volume, assisted conversions |
| **Revenue & Efficiency** | ROAS, revenue attributed, AOV, LTV:CAC ratio (if data available) |
| **Quality & Relevance** | Quality/relevance score, ad rank, audience saturation index |

Flag any data gaps or attribution blind spots (e.g., iOS 14+ signal loss, cross-device attribution, view-through vs. click-through windows).

### 3B: Diagnostic Analysis (Six-Lever Framework)

Evaluate campaign performance across six interdependent levers:

1. **ICA–Audience Alignment** — Does the targeting architecture (custom audiences, lookalikes, interest stacks, keyword themes) map precisely to the defined ICA segments? Identify audience bleed, overlap between ad sets, or wasted spend on non-ICA impressions. Calculate ICA precision ratio where data permits.

2. **Creative Effectiveness** — Assess ad creative against the ICA's stage of awareness (unaware, problem-aware, solution-aware, product-aware, most aware). Evaluate hook strength (first 3 seconds for video, headline for static), message–market match, proof density, and visual scroll-stopping power. Identify creative fatigue signals (rising frequency + declining CTR).

3. **Offer–Funnel Congruence** — Does the advertised offer match the audience temperature? Is there friction between the ad promise and the landing page experience? Evaluate offer specificity, urgency mechanics, and risk-reversal elements against ICA objection patterns.

4. **Bid & Budget Architecture** — Analyse budget allocation efficiency across campaigns, ad sets, and platforms. Identify budget-constrained winners (high ROAS but capped spend), over-funded losers, and bid strategy mismatches (e.g., using lowest-cost bidding when cost-cap would stabilise CPA).

5. **Platform & Placement Optimisation** — Break down performance by placement (feed, stories, reels, search, display, audience network, inbox). Identify placement-level CPA variance and whether Advantage+/Performance Max broad targeting is outperforming or obscuring manual controls.

6. **Attribution & Measurement Integrity** — Assess whether the reported metrics reflect true business impact. Flag discrepancies between platform-reported conversions and backend/CRM data. Evaluate attribution window settings, conversion API implementation status, and incrementality signals.

Apply any user-specific `instructions` from FutureProof context (e.g., preferred attribution model, internal ROAS thresholds, ICA definitions, brand voice constraints on creative recommendations).

### 3C: Benchmarking

Compare performance against:
- **Historical performance**: prior FutureProof sessions and saved benchmarks for this account
- **Industry benchmarks**: platform-published and third-party benchmarks for the relevant vertical and campaign objective
- **Efficiency frontier**: identify the theoretical optimum given current spend levels and conversion rates

## Step 4: Deliver Output

Produce a structured **Ad Performance Diagnostic Report** with the following sections:

### 4.1 Executive Summary
- One-paragraph performance verdict with overall health rating (Critical / Underperforming / On Track / Outperforming)
- Primary bottleneck identified (the single lever with greatest drag on KPI performance)
- Estimated recoverable spend or revenue opportunity

### 4.2 Six-Lever Scorecard

| Lever | Score (1–10) | Status | Priority |
|---|---|---|---|
| ICA–Audience Alignment | — | 🔴🟡🟢 | P1/P2/P3 |
| Creative Effectiveness | — | 🔴🟡🟢 | P1/P2/P3 |
| Offer–Funnel Congruence | — | 🔴🟡🟢 | P1/P2/P3 |
| Bid & Budget Architecture | — | 🔴🟡🟢 | P1/P2/P3 |
| Platform & Placement Optimisation | — | 🔴🟡🟢 | P1/P2/P3 |
| Attribution & Measurement Integrity | — | 🔴🟡🟢 | P1/P2/P3 |

### 4.3 Critical Fixes (Top 5 Highest-Impact Actions)

Each fix must include:
- **What to change**: specific, implementable instruction (not vague guidance)
- **Where to change it**: exact campaign/ad set/ad level and platform location
- **Why it matters**: quantified impact hypothesis tied to the primary KPI
- **Implementation effort**: Low / Medium / High
- **Expected timeline to measurable impact**: hours / days / weeks

### 4.4 Budget Reallocation Matrix

A specific recommended reallocation table showing:
- Current spend by campaign/ad set/channel
- Recommended spend adjustment (increase, decrease, pause, or maintain)
- Rationale for each adjustment

### 4.5 Creative Brief (if creative is the bottleneck)

Provide a production-ready creative brief for the next round of ads:
- Hook variants (3 options) tailored to ICA pain points
- Body copy direction aligned to awareness stage
- CTA specification
- Format and placement recommendations

### 4.6 90-Day Optimisation Roadmap

A phased plan:
- **Week 1–2**: Emergency fixes (stop bleeding)
- **Week 3–4**: Structural improvements (audience, bid, budget)
- **Week 5–8**: Creative refresh and testing cadence
- **Week 9–12**: Scale what works, sunset what doesn't, measure incrementality

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="ad-performance-analyser", experiment={
  hypothesis: "Restructuring ad sets to isolate ICA segments by awareness stage will reduce CPA by enabling stage-appropriate creative and bidding",
  variants: ["control: current broad ad set structure", "variant: segmented ad sets by ICA awareness stage with tailored creative"],
  measurement: "CPA and conversion volume comparison across segmented vs. broad ad sets over 14-day window with minimum 100 conversions per variant",
  expected_impact: "20–30% CPA reduction on prospecting campaigns with maintained or improved conversion volume"
})
```

```
FutureProof:save_experiment(skill="ad-performance-analyser", experiment={
  hypothesis: "Replacing benefit-led hooks with ICA-specific pain-point hooks in the first 3 seconds of video ads will increase ThruPlay rate and downstream conversion rate",
  variants: ["control: current benefit-led hook", "variant: pain-point hook mirroring ICA's exact language from reviews/calls"],
  measurement: "ThruPlay rate, CTR, and CPA across minimum 5,000 impressions per variant",
  expected_impact: "25% improvement in ThruPlay rate, 10–15% improvement in CTR"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="ad-performance-analyser",
  query="Current CPM and CPA benchmarks by platform and vertical for Q-current, emerging ad format performance data (Meta Advantage+ Shopping, Google Demand Gen, TikTok Smart+), and post-iOS signal recovery strategies including Conversions API and server-side tracking best practices 2024–2025",
  reason="Ensure optimisation recommendations reflect current auction dynamics, new platform features, and evolving measurement landscape rather than outdated heuristics"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="ad-performance-analyser", session={
  summary: "Analysed [platform(s)] ad performance for [ICA segment/campaign objective] over [date range] with [budget amount] in spend",
  key_findings: ["Primary bottleneck: [lever name] scoring [X/10]", "Top fix: [specific action] with estimated [X%] impact on [KPI]", "Budget reallocation opportunity: [amount] from underperforming [campaign/channel] to [high-performing campaign/channel]", "Creative fatigue detected on [X] ad sets with frequency above [threshold]"],
  benchmarks_captured: { cpa: "value", roas: "value", ctr: "value", cpm: "value" },
  user_feedback: null
})
```