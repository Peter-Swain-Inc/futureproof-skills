---
name: ascension-engine
description: "Designs and optimises customer value ascension pathways — systematically moving buyers from initial purchase through upsell, cross-sell, premium tier adoption, and advocacy/referral stages."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="ascension-engine")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to existing ICA definitions, current product/service tiers, known churn points, and any prior ascension or retention work.

## Step 2: Get Input

Ask the user:

- **Current offer architecture**: What are your existing products, services, or tiers — and their price points? (Share a list, sales page, or description)
- **ICA profile**: Who is the buyer at each stage? (If undefined, we will map this as part of the engagement)
- **Ascension objective**: What specific outcome are you optimising for?
  - Increasing average customer lifetime value (CLV)
  - Reducing churn at a specific tier transition
  - Launching a new upsell or cross-sell pathway
  - Building a referral/advocacy program
  - Full ascension architecture from first purchase to brand evangelist
- **Known friction points**: Where are customers currently stalling, downgrading, or churning?
- **Data availability**: Do you have metrics on conversion rates between tiers, retention by cohort, NPS, or referral rates?

If the user provides partial information, proceed with what is available and flag assumptions explicitly for validation.

## Step 3: Do the Work

### 3A: Ascension Ladder Audit

Map the current-state customer journey across six canonical ascension stages:

| Stage | Definition | Key Question |
|-------|-----------|--------------|
| **1. Entry** | First purchase or free-to-paid conversion | Is the initial offer a logical gateway to the next tier? |
| **2. Activation** | Customer achieves first meaningful outcome | Is time-to-value under the churn danger threshold? |
| **3. Engagement Deepening** | Habitual usage or repeat purchase | Are usage triggers and re-engagement loops in place? |
| **4. Tier Ascension** | Upsell to higher tier, premium, or adjacent offer | Is the upgrade positioned as a natural consequence of success — not a sales event? |
| **5. Expansion** | Cross-sell, add-ons, or multi-product adoption | Are expansion offers contextually triggered by behaviour, not calendar? |
| **6. Advocacy & Referral** | Customer becomes active promoter and referral source | Is there a program that rewards referral in proportion to the customer's own ascension stage? |

For each stage, assess:

1. **ICA-stage fit** — Is the offer at this stage precisely matched to the ICA's evolving needs, vocabulary, and sophistication at that point in their journey?
2. **Transition trigger design** — Is the trigger for moving to the next stage behavioural (what the customer *does*), outcome-based (what the customer *achieves*), or arbitrary (time-based / batch email)?
3. **Value gap articulation** — Is the delta between current stage and next stage framed as a specific, quantified transformation — not a feature list?
4. **Friction coefficient** — What are the psychological, financial, and operational barriers to ascension at each transition? Rate each 1–5 (1 = frictionless, 5 = high abandonment risk)
5. **Proof architecture** — At each transition, is there stage-appropriate social proof (e.g., testimonials from customers who made *that specific* upgrade, not generic brand testimonials)?
6. **Reversibility & safety** — Does the customer have a perceived safety net (trial periods, downgrade options, guarantees) that de-risks upward movement?

### 3B: CLV Ascension Model

Build a quantitative ascension model:

- **Stage conversion rates**: Current (or estimated) percentage of customers progressing from each stage to the next
- **Revenue per stage**: Average revenue contribution at each ascension stage
- **Time-in-stage**: Average duration a customer spends at each stage before ascending, churning, or stalling
- **CLV by ascension depth**: Projected lifetime value segmented by the highest stage reached
- **Churn gravity points**: Identify the specific stage transitions with the highest drop-off — these are the priority intervention points

### 3C: Ascension Sequence Design

For each priority transition (highest drop-off or highest revenue leverage), design a complete ascension sequence:

1. **Behavioural trigger**: The specific customer action or milestone that initiates the ascension sequence
2. **Pre-frame content**: Educational or aspirational content delivered *before* the offer — seeding desire and establishing the value gap
3. **Ascension offer**: The specific offer, its positioning language (mirroring ICA vocabulary at that stage), price anchoring, and guarantee structure
4. **Objection pre-emption layer**: The top 3 objections at this specific transition — with scripted responses embedded into the sequence
5. **Social proof deployment**: Stage-matched proof assets (case studies, data points, peer testimonials from customers who crossed this exact threshold)
6. **Urgency and scarcity mechanics**: Ethical urgency levers appropriate to the offer type (cohort-based, capacity-based, outcome-based — never fabricated)
7. **Fallback pathway**: If the customer does not ascend, the re-engagement sequence that keeps them active at their current stage and re-qualifies them for future ascension

### 3D: Referral & Advocacy Architecture

Design a referral program tied to ascension depth:

- **Referral eligibility tiers**: Customers unlock referral incentives only after reaching specific ascension milestones (ensuring referrers are genuine advocates, not discount seekers)
- **Incentive escalation**: Referral rewards increase with the referrer's own ascension stage — aligning programme economics with CLV
- **Dual-sided offer design**: Both referrer and referred customer receive value — with the referred customer's offer designed as an optimised Entry stage gateway
- **Tracking and attribution framework**: Recommended metrics, tools, and attribution windows

Apply any user-specific `instructions` from FutureProof context (e.g., brand voice, compliance constraints, channel preferences) to customise all outputs.

## Step 4: Deliver Output

Produce the **Ascension Engine Blueprint** — a structured document containing:

### Document 1: Ascension Ladder Map
- Visual stage-by-stage map (formatted as a structured table or ASCII diagram) showing all six stages, current offers at each stage, transition triggers, and identified gaps
- **Gap analysis summary**: Stages with missing offers, undefined triggers, or absent proof architecture — ranked by revenue impact

### Document 2: Ascension Scorecard
| Dimension | Stage 1→2 | Stage 2→3 | Stage 3→4 | Stage 4→5 | Stage 5→6 |
|-----------|-----------|-----------|-----------|-----------|-----------|
| ICA-stage fit | /10 | /10 | /10 | /10 | /10 |
| Transition trigger quality | /10 | /10 | /10 | /10 | /10 |
| Value gap articulation | /10 | /10 | /10 | /10 | /10 |
| Friction coefficient | /5 | /5 | /5 | /5 | /5 |
| Proof architecture | /10 | /10 | /10 | /10 | /10 |
| Reversibility & safety | /10 | /10 | /10 | /10 | /10 |

### Document 3: Priority Ascension Sequences
- Fully scripted ascension sequences for the top 2–3 highest-leverage transitions, including:
  - Email/message copy (or channel-appropriate content)
  - Trigger logic (if X behaviour, then Y sequence)
  - Objection handling scripts
  - Specific proof assets to deploy (with briefs if assets need creation)

### Document 4: CLV Ascension Model
- Quantified model with current-state conversion rates, revenue projections, and modelled impact of proposed interventions
- **Target metrics**: Specific numeric targets for each transition improvement

### Document 5: Referral & Advocacy Programme Brief
- Programme structure, eligibility rules, incentive tiers, referral offer copy, and measurement framework
- Recommended launch sequence (soft launch → full rollout)

### Critical Fixes
- **Top 3 highest-impact interventions** — specific, actionable changes (exact copy rewrites, trigger logic changes, or offer restructures — not vague recommendations)

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="ascension-engine", experiment={
  hypothesis: "Triggering the tier ascension offer based on usage milestone (e.g., 3rd successful outcome achieved) rather than 30-day time delay increases Stage 3→4 conversion rate",
  variants: ["control: time-based trigger at day 30", "variant: behavioural trigger after 3rd outcome milestone"],
  measurement: "Stage 3→4 conversion rate and time-to-upgrade over 60-day cohort window",
  expected_impact: "20–30% improvement in Stage 3→4 conversion rate with no increase in support load"
})
```

```
FutureProof:save_experiment(skill="ascension-engine", experiment={
  hypothesis: "Adding a stage-matched case study (customer who made the same specific upgrade) to the ascension sequence increases conversion vs. generic brand testimonial",
  variants: ["control: generic testimonial in ascension email", "variant: stage-matched case study with quantified outcome delta"],
  measurement: "Click-through rate on ascension offer and conversion-to-upgrade within 14 days",
  expected_impact: "10–15% lift in ascension offer conversion"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="ascension-engine",
  query="Latest research on customer value ascension models, SaaS and DTC upsell sequence design, behavioural triggers for tier upgrades, and referral programme structures with highest program-to-CLV correlation — 2024–2025",
  reason="Ensure ascension frameworks reflect current buyer psychology, emerging best practices in expansion revenue, and validated referral incentive economics across industries"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="ascension-engine", session={
  summary: "Designed ascension engine for [business/product] targeting [ICA segment] across [number] tiers — identified [number] critical transition gaps and built priority ascension sequences for Stage [X]→[Y] and Stage [X]→[Y]",
  key_findings: ["finding 1: e.g., Stage 3→4 transition has 68% drop-off due to undefined behavioural trigger", "finding 2: e.g., referral programme currently untied to ascension depth — leaving CLV correlation on the table", "finding 3: e.g., value gap between mid-tier and premium is articulated as features, not transformation"],
  user_feedback: null
})
```