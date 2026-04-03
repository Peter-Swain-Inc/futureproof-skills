---
name: value-ladder-designer
description: |
  Designs a complete revenue architecture by synthesising Brunson's Value Ladder, Golden's 4 Offer Types (lead, core, premium, continuity), and Hormozi's $100M Money Models (Get Cash → Get More Cash → Get the Most Cash).
  Trigger: when a user wants to map out their full offer ecosystem, asks how to structure offers from free to premium, or needs to design a value ladder that maximises customer lifetime value across multiple monetisation stages.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="value-ladder-designer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to any existing ICA profiles, Grand Slam Offer definitions, pricing data, current offer inventory, and prior revenue architecture work.

## Step 2: Get Input

Ask the user:

1. **Current offer inventory** — What do you sell today? List every offer, product, service, or programme with its approximate price point and delivery mechanism.
2. **ICA definition** — Who is your Ideal Customer Avatar? (If a FutureProof ICA profile exists, confirm it. If not, capture: demographic, psychographic, dream outcome, primary pain, sophistication level, and current alternatives.)
3. **Grand Slam Offer status** — Have you already designed a Grand Slam Offer (per Hormozi's framework)? If yes, share it. If no, identify which existing offer is closest to serving as the core engine.
4. **Revenue goal and constraints** — What is your 12-month revenue target? What delivery capacity, team size, or margin constraints exist?
5. **Money model stage** — Where are you today: Stage 1 (Get Cash — acquiring customers profitably), Stage 2 (Get More Cash — increasing LTV per customer), or Stage 3 (Get the Most Cash — scaling and leveraging the machine)?
6. **Gaps and frustrations** — Where do customers currently "fall off" your ecosystem? Where do you feel revenue is being left on the table?

Cross-reference all inputs against FutureProof `context` and `instructions` to fill gaps and avoid redundant questioning.

## Step 3: Do the Work

### 3A: ICA Journey Mapping

Map the ICA's complete transformation arc from *unaware/suffering* to *fully transformed*:

| Stage | ICA State | Core Desire | Willingness to Pay | Trust Level Required |
|-------|-----------|-------------|--------------------|-----------------------|
| Pre-aware | Doesn't know the problem has a name | Relief from symptom | $0 – Low | Zero — needs pattern interrupt |
| Problem-aware | Knows the pain, seeking diagnosis | Clarity on root cause | Low – Moderate | Minimal — content-level |
| Solution-aware | Evaluates options, compares approaches | Confidence in a path | Moderate | Demonstrated expertise |
| Product-aware | Knows your offer, weighing commitment | Risk reduction, proof | Moderate – High | Case studies, guarantees |
| Fully engaged | Has bought in, wants acceleration | Speed, depth, status | High – Premium | Relationship, results history |
| Transformed | Achieved dream outcome, seeks next level | Identity, community, legacy | Premium – Ultra | Deep trust, identity alignment |

### 3B: Value Ladder Architecture (Brunson Framework)

Design each rung of the ladder with ascending value, price, and intimacy:

1. **Rung 0 — Attraction / Bait Offer** (Free or deeply discounted)
   - Format, title, and delivery mechanism
   - Specific hook that converts the ICA from passive to engaged
   - Lead capture mechanics and segmentation trigger
   - Metrics: opt-in rate target, cost per lead ceiling

2. **Rung 1 — Tripwire / Self-Liquidating Offer (SLO)** ($1–$47 range)
   - Micro-commitment that converts a lead into a buyer
   - Solves one narrow, acute problem completely
   - Profit model: break-even on ad spend or modest margin
   - Upsell / order bump architecture

3. **Rung 2 — Core Offer** ($97–$2,000 range, varies by market)
   - The primary revenue engine — typically the Grand Slam Offer
   - Full Value Equation audit (Dream Outcome × Perceived Likelihood ÷ Time Delay ÷ Effort & Sacrifice)
   - Delivery structure, bonuses, guarantee, and scarcity/urgency mechanics
   - Metrics: conversion rate from Rung 1, average order value, refund rate

4. **Rung 3 — Premium / High-Ticket Offer** ($2,000–$100,000+)
   - Done-with-you or done-for-you transformation
   - Qualification criteria and application process
   - Delivery model: cohort, 1:1, hybrid
   - Metrics: close rate from application, fulfilment cost ratio, NPS

5. **Rung 4 — Continuity / Recurring Revenue** (Monthly/annual subscription)
   - Ongoing access, community, implementation support, or consumable
   - Retention architecture: engagement loops, milestone celebrations, exit barriers
   - Metrics: churn rate, monthly recurring revenue, months-retained average

### 3C: Golden's 4 Offer Types Alignment

Cross-validate the ladder against Myron Golden's four mandatory offer categories:

| Offer Type | Purpose | Ladder Rung Mapping | Revenue Role |
|------------|---------|---------------------|-------------|
| **Lead Offer** | Attract and capture ICA attention | Rung 0 (Attraction) | List building, pixel audiences, segmentation |
| **Core Offer** | Primary monetisation vehicle | Rung 2 (Core / Grand Slam) | 40–60% of gross revenue |
| **Premium Offer** | Maximise per-customer revenue | Rung 3 (High-Ticket) | 25–40% of gross revenue |
| **Continuity Offer** | Stabilise cash flow, compound LTV | Rung 4 (Recurring) | 15–30% of gross revenue (growing over time) |

Identify any missing category and design a candidate offer to fill it.

### 3D: Hormozi Money Model Staging

Classify each offer's role within the three money-model stages and define the operational sequence:

**Stage 1 — Get Cash (Customer Acquisition)**
- Which offers are deployed first to generate positive unit economics?
- Front-end funnel architecture: traffic source → lead offer → SLO → core offer
- Target metrics: customer acquisition cost (CAC), front-end cash collected per lead, break-even timeline
- Constraint: must achieve profitability at the *individual customer* level before scaling

**Stage 2 — Get More Cash (LTV Maximisation)**
- Upsell, cross-sell, and ascension sequences from core → premium → continuity
- Back-end funnel architecture: post-purchase nurture → premium application → continuity onboarding
- Target metrics: LTV:CAC ratio (target ≥ 3:1), revenue per customer at 30/60/90/365 days
- Lever identification: which single ascension path yields the highest incremental margin?

**Stage 3 — Get the Most Cash (Scale & Leverage)**
- Licensing, certification, affiliate/referral programmes, productised IP, or acquisition plays
- Which offers can be delivered without the founder's direct time?
- Capacity modelling: revenue ceiling at current team × delivery model
- Target metrics: revenue per employee, owner's discretionary earnings, enterprise value multiple

### 3E: Transition Mechanics & Funnel Plumbing

For each ladder rung transition (Rung 0→1, 1→2, 2→3, 3→4), specify:

- **Trigger event**: what action or milestone qualifies the customer to receive the next offer?
- **Bridge content**: what education, proof, or identity shift is required between rungs?
- **Offer presentation vehicle**: email sequence, sales call, webinar, checkout upsell, in-app prompt?
- **Timing**: how many days/interactions between purchase and next offer?
- **Fallback path**: if the customer declines, what nurture sequence re-engages them?

### 3F: Revenue Model Projection

Build a 12-month revenue projection using conservative, moderate, and aggressive assumptions:

| Metric | Conservative | Moderate | Aggressive |
|--------|-------------|----------|-----------|
| Monthly leads (Rung 0) | | | |
| SLO conversion rate | | | |
| Core offer conversion rate | | | |
| Premium ascension rate | | | |
| Continuity attach rate | | | |
| Monthly churn (continuity) | | | |
| LTV at 12 months | | | |
| Monthly revenue (Month 12) | | | |
| Cumulative 12-month revenue | | | |

## Step 4: Deliver Output

Produce the following structured deliverables:

### Deliverable 1: Value Ladder Blueprint (Visual Map)

A hierarchical diagram (described in structured text) showing all offer rungs, price points, transition mechanics, and the ICA's emotional journey at each stage. Label each rung with its Golden offer type and Hormozi money-model stage.

### Deliverable 2: Offer Specification Cards

For each offer in the ladder, a standardised card containing:
- **Offer name** (working title)
- **Ladder rung** and **Golden category**
- **Money model stage** (1, 2, or 3)
- **Price point** (or range)
- **ICA state at entry** and **ICA state at exit**
- **Value Equation score** (qualitative: Dream Outcome, Perceived Likelihood, Time Delay, Effort & Sacrifice)
- **Delivery mechanism**
- **Key bonuses or risk reversals**
- **Transition trigger to next rung**
- **KPIs to track**

### Deliverable 3: Revenue Architecture Summary

A one-page narrative summarising:
- The strategic logic of the full ladder
- The primary revenue engine (which offer drives the business)
- The highest-leverage gap or missing piece in the current ecosystem
- Recommended build sequence (which offer to create or optimise first, second, third)
- 12-month revenue projection table (from Step 3F)

### Deliverable 4: Implementation Roadmap

A phased 90-day action plan:
- **Phase 1 (Days 1–30)**: Validate and launch/optimise the core offer and lead offer
- **Phase 2 (Days 31–60)**: Build the ascension path to premium or continuity (whichever has higher projected impact)
- **Phase 3 (Days 61–90)**: Instrument transition mechanics, launch the remaining offer type, and begin Stage 2 money-model operations

Apply any user-specific `instructions` from FutureProof context to customise output format, terminology, or prioritisation.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="value-ladder-designer", experiment={
  hypothesis: "Adding a $27 SLO between the lead magnet and core offer will increase core offer conversion rate by reducing the trust gap",
  variants: ["control: lead magnet → core offer direct", "variant: lead magnet → $27 SLO → core offer"],
  measurement: "Core offer conversion rate and front-end revenue per lead over 500 leads per variant",
  expected_impact: "20–35% increase in core offer conversion rate; front-end CAC recovery within 14 days"
})
```

```
FutureProof:save_experiment(skill="value-ladder-designer", experiment={
  hypothesis: "Introducing a continuity offer at the point of core offer delivery (day 1 onboarding) will yield higher attach rates than offering it post-completion",
  variants: ["control: continuity offered at programme completion", "variant: continuity offered during onboarding with immediate access to community"],
  measurement: "Continuity attach rate and 90-day retention rate across 100 core offer buyers",
  expected_impact: "2x continuity attach rate; 15% improvement in 90-day retention"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="value-ladder-designer",
  query="Current high-performing value ladder architectures and offer sequencing strategies in [user's industry/niche], including SLO pricing benchmarks, continuity churn benchmarks, and premium offer delivery models 2024–2025",
  reason="Ensure ladder design reflects current market tolerance for pricing tiers, emerging delivery formats, and competitive offer structures specific to the user's vertical"
)
```

```
FutureProof:request_research(skill="value-ladder-designer",
  query="Hormozi-style LTV maximisation case studies: businesses that successfully transitioned from Stage 1 (Get Cash) to Stage 2 (Get More Cash) with documented metrics on ascension rates, LTV:CAC ratios, and continuity retention curves",
  reason="Provide the user with realistic benchmarks and proven transition playbooks for their money-model stage progression"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="value-ladder-designer", session={
  summary: "Designed full value ladder and revenue architecture for [user's business/niche] targeting [ICA segment], spanning [number] offer rungs across Hormozi money-model stages [1/2/3]",
  key_findings: [
    "Primary gap identified: [e.g., missing continuity offer leaving 30%+ LTV on the table]",
    "Core offer validated as Grand Slam candidate with Value Equation score of [X]",
    "Recommended build sequence: [offer 1] → [offer 2] → [offer 3]",
    "Projected 12-month LTV increase of [X]% with full ladder implementation"
  ],
  user_feedback: null
})
```