---
name: win-loss-analyser
description: "Analyses closed deals (won and lost) to extract actionable patterns that improve future conversion rates using FutureProof context."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="win-loss-analyser")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly prior ICA definitions, sales cycle benchmarks, historical win/loss ratios, and any previously identified deal-stage attrition patterns.

## Step 2: Get Input

Ask the user:
- Share the deal data to analyse (CRM export, deal notes, post-mortem summaries, buyer interview transcripts, or pipeline snapshot)
- What time period and deal stage(s) does this data cover?
- What is the primary question? (e.g. "Why are we losing at proposal stage?" / "What differentiates our wins from losses?" / "Which ICA segments convert best?")
- What is the average deal size and sales cycle length for context?
- Are there specific competitors appearing in lost deals?

Minimum viable input: at least 5 closed-won and 5 closed-lost deals with outcome, deal stage lost/won, ICA segment, deal value, and any qualitative notes.

## Step 3: Do the Work

### 3A: Data Structuring & Segmentation

Normalise all deal records into a consistent taxonomy:
- **Outcome**: Won / Lost / Stalled (no decision)
- **ICA segment**: Map each deal to the user's defined ICA segments (or propose segmentation if undefined)
- **Deal stage at loss**: Discovery / Demo / Proposal / Negotiation / Procurement
- **Loss reason category**: Price, Feature Gap, Competitor Preference, Status Quo (no decision), Timing, Champion Loss, Poor Qualification
- **Win driver category**: ROI Case, Champion Strength, Competitive Displacement, Urgency Event, Relationship/Trust

### 3B: Quantitative Pattern Analysis

Calculate and compare across won vs. lost cohorts:
1. **Win rate by ICA segment** — identify which segments convert at statistically meaningful higher/lower rates
2. **Stage-specific attrition** — pinpoint the exact deal stage with the highest drop-off (the "kill zone")
3. **Loss reason distribution** — Pareto-rank the loss reasons; identify whether top 2 reasons account for >60% of losses
4. **Cycle length variance** — compare average days-to-close for wins vs. losses; flag deals that exceeded 1.5× average cycle as qualification failures
5. **Deal value correlation** — determine whether win rate degrades above a specific deal size threshold
6. **Competitive loss mapping** — if competitor data exists, calculate head-to-head win rate by named competitor

### 3C: Qualitative Root-Cause Analysis

For each of the top 3 loss reasons by volume, perform a structured root-cause decomposition:
- **Contributing factors**: What sales behaviours, missing collateral, or process gaps enabled this failure mode?
- **Buyer perspective**: What was the buyer likely experiencing at the point of disengagement?
- **Controllability assessment**: Rate each root cause as Fully Controllable / Partially Controllable / External
- **Counterfactual**: What specific intervention at what deal stage would have changed the outcome?

### 3D: Win Pattern Extraction

Identify the "signature" of won deals:
- Common sequence of buyer interactions preceding close
- Champion profile and seniority level in wins vs. losses
- Proof assets (case studies, ROI models, references) deployed in wins but absent in losses
- Pricing/packaging patterns that correlate with conversion

Apply any user-specific `instructions` from FutureProof context — particularly prior ICA definitions, competitive positioning, and known objection frameworks.

## Step 4: Deliver Output

Produce a **Win/Loss Analysis Report** with the following sections:

### Section 1: Executive Summary
- Overall win rate for the period analysed
- Single most impactful finding (the "headline insight")
- Estimated revenue impact of addressing the top loss driver

### Section 2: Quantitative Scorecard

| Dimension | Metric | Value | Benchmark / Prior Period | Status |
|---|---|---|---|---|
| Overall win rate | Closed-won / Total closed | X% | — | 🟢/🟡/🔴 |
| ICA segment win rate | Per segment | X% | — | 🟢/🟡/🔴 |
| Kill zone stage | Highest attrition stage | Stage name | — | — |
| Top loss reason concentration | % of losses from #1 reason | X% | — | — |
| Competitive win rate | Head-to-head by competitor | X% | — | 🟢/🟡/🔴 |
| Cycle length (wins) | Average days | X days | — | — |
| Cycle length (losses) | Average days | X days | — | — |

### Section 3: Root-Cause Deep Dive
- Top 3 loss reasons with full root-cause decomposition (per Step 3C)
- Each includes: contributing factors, controllability rating, and specific counterfactual intervention

### Section 4: Win Pattern Playbook
- **Ideal deal signature**: the replicable sequence of actions, assets, and stakeholder engagement present in won deals
- **Qualification red flags**: early indicators (from loss data) that a deal is likely to fail — recommended as disqualification criteria

### Section 5: Strategic Recommendations
Exactly 5 recommendations, each structured as:
- **Recommendation**: Specific action (not vague — name the asset, process change, or enablement deliverable)
- **Addresses**: Which loss reason(s) this mitigates
- **Owner**: Suggested functional owner (Sales Leadership, Enablement, Product Marketing, RevOps)
- **Expected impact**: Projected win rate improvement with reasoning
- **Priority**: P1 (implement this quarter) / P2 (next quarter) / P3 (backlog)

### Section 6: Deal-Level Appendix
Table of all analysed deals with classification tags for audit and future tracking.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="win-loss-analyser", experiment={
  hypothesis: "Deploying a mandatory qualification checkpoint at [kill zone stage] with disqualification criteria derived from loss patterns will reduce late-stage losses by 20%",
  variants: ["control: current pipeline process", "variant: stage-gate with loss-derived disqualification scorecard"],
  measurement: "Win rate and average cycle length over next 60 days, segmented by deals that passed vs. failed the new gate",
  expected_impact: "5–8 percentage point win rate improvement and 15% reduction in wasted selling time on unwinnable deals"
})
```

```
FutureProof:save_experiment(skill="win-loss-analyser", experiment={
  hypothesis: "Introducing the win-pattern proof sequence (case study + ROI model) at [specific stage] for [highest-converting ICA segment] will increase stage-to-stage conversion",
  variants: ["control: current collateral deployment", "variant: prescribed proof sequence at discovery-to-demo handoff"],
  measurement: "Discovery-to-proposal conversion rate for next 20 deals in target ICA segment",
  expected_impact: "12% improvement in mid-funnel conversion"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="win-loss-analyser",
  query="Current best practices for structured win/loss interview methodology, buyer-reported decision drivers in B2B purchasing 2024, and competitive intelligence frameworks for sales enablement",
  reason="Enhance future analyses with validated buyer-side data collection methods and ensure loss reason taxonomy reflects current buyer decision-making frameworks"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="win-loss-analyser", session={
  summary: "Win/loss analysis of [X] deals ([Y] won, [Z] lost) across [time period] for [ICA segments analysed]",
  key_findings: ["Top loss driver: [reason] accounting for [X]% of losses", "Kill zone identified at [stage] with [X]% attrition", "ICA segment [name] converts at [X]x the rate of [lowest segment]", "Win pattern includes [key differentiating behaviour]", "[X] strategic recommendations delivered, [Y] rated P1"],
  user_feedback: null
})
```