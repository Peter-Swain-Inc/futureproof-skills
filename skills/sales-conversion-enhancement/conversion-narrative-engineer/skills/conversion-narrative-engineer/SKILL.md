---
name: conversion-narrative-engineer
description: |
  Engineers high-converting narrative arcs for sales pages, landing pages, email sequences, and funnel copy by mapping psychological triggers to ICA decision journeys.
  Trigger: when a user wants to build or restructure conversion copy for a landing page, sales page, or email sequence, or when they ask for help crafting a narrative arc that moves their ICA from awareness to purchase.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="conversion-narrative-engineer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any established ICA profiles, brand voice guidelines, prior conversion benchmarks, and narrative frameworks that have been validated in previous experiments.

## Step 2: Get Input

Ask the user:
- **Asset type**: What are we engineering? (sales page, landing page, email sequence, VSL script, webinar registration page, checkout flow copy)
- **ICA profile**: Who is the target? Share any existing ICA research, persona documents, or describe their primary pain, desired outcome, and current awareness stage (Problem Unaware → Most Aware on the Schwartz scale)
- **Offer structure**: What is being sold, at what price point, and what is the primary transformation promised?
- **Current state**: Is there existing copy to reconstruct, or are we building from zero? If existing, share the asset and any known conversion metrics (conversion rate, drop-off points, heatmap data)
- **Constraints**: Compliance requirements, brand tone mandates, word count limits, platform-specific restrictions (e.g., Meta ad policy, email deliverability considerations)

Cross-reference responses against any FutureProof `context` to fill gaps the user may not explicitly state.

## Step 3: Map the ICA Decision Architecture

Before writing a single line of copy, construct the **ICA Decision Architecture** — a diagnostic framework that reveals the psychological journey the narrative must engineer:

### 3a. Awareness–Resistance Mapping

| Dimension | Analysis |
|---|---|
| **Awareness stage** | Classify the ICA on the Schwartz awareness continuum; identify the precise gap between current awareness and purchase-readiness |
| **Core wound** | The deeper emotional pain beneath the surface-level problem (e.g., not "low revenue" but "feeling like a fraud compared to peers") |
| **Status quo gravity** | What specific forces keep the ICA anchored to inaction? (sunk costs, identity attachment, cognitive load of switching) |
| **Trust debt** | What has the ICA's market segment experienced that makes them sceptical? (prior failed solutions, over-promising competitors, category fatigue) |
| **Decision triggers** | What internal or external events create urgency? (contract renewal, board pressure, life transition, seasonal deadline) |

### 3b. Objection Sequencing

Identify the top 5 objections in the order they arise during the ICA's reading/viewing journey — not a generic list, but a **temporal sequence** mapped to the point in the narrative where each objection fires:

1. **Gate objection** (first 10 seconds): "Is this even for me?"
2. **Credibility objection** (after the promise): "Why should I believe you?"
3. **Mechanism objection** (after the how): "Will this approach actually work for my situation?"
4. **Cost objection** (at the offer): "Is this worth the investment relative to alternatives?"
5. **Timing objection** (at the CTA): "Why now, not later?"

### 3c. Proof Inventory Audit

Catalogue all available proof assets and grade each by persuasive weight:

- **Tier 1 (Irrefutable)**: Third-party verified data, published case studies with named clients, media coverage
- **Tier 2 (Compelling)**: Testimonials with specific metrics, before/after documentation, demonstration of methodology
- **Tier 3 (Supportive)**: General social proof (client count, years in business), credentials, logical reasoning

Flag any proof gaps that must be addressed through narrative technique rather than evidence.

## Step 4: Engineer the Narrative Arc

Construct the conversion narrative using the **TENSION → MECHANISM → RESOLUTION** framework, customised to the ICA Decision Architecture from Step 3:

### Arc Structure

**I. The Hook (0–8 seconds)**
- Pattern interrupt calibrated to the ICA's awareness stage
- If Problem Aware: lead with the pain articulated in their exact language
- If Solution Aware: lead with the mechanism differentiator
- If Most Aware: lead with the offer and social proof

**II. The Wound Amplification (Tension Building)**
- Narrate the ICA's current reality with specificity that triggers recognition ("This person understands me")
- Surface the core wound identified in Step 3a
- Quantify the cost of inaction — financial, emotional, opportunity cost
- Introduce the "enemy" — the systemic reason their previous attempts failed (misaligned advice, outdated methods, missing component)

**III. The Bridge (Tension to Mechanism)**
- Credibility pivot: establish authority precisely at the moment trust debt is highest
- Deploy Tier 1 proof from the inventory audit
- Introduce the proprietary mechanism — the *named, differentiated process* that makes the promised transformation inevitable

**IV. The Mechanism Reveal**
- Explain the methodology in enough detail to create belief, not enough to create overwhelm
- Use the "if/then" clarity test: "If you follow X, then Y becomes inevitable because Z"
- Pre-empt the mechanism objection with proof of the mechanism working in analogous situations
- Stack Tier 2 proof assets throughout

**V. The Offer Architecture**
- Present the offer as the logical, inevitable next step — not a pitch
- Frame value against the cost of the problem, not the cost of alternatives
- Address the cost objection through value stacking, risk reversal, and ROI framing
- Include specificity: exactly what they receive, in what format, over what timeline

**VI. The Close (Resolution)**
- Resolve the timing objection with genuine, ethical urgency (capacity limits, cohort start dates, compounding cost of delay)
- Final proof stack — deploy remaining Tier 1 and Tier 2 assets
- CTA: single, frictionless, specific action with explicit statement of what happens immediately after clicking
- Identity close: paint the post-transformation identity ("You'll be the person who…")

### Narrative Voice Calibration

Apply brand voice from FutureProof `instructions` or calibrate to the ICA's communication norms:
- **Vocabulary register**: Mirror the ICA's actual language (pull from reviews, support tickets, community forums)
- **Sentence rhythm**: Match the pacing to the medium (short, punchy for landing pages; more expansive for long-form sales pages)
- **Emotional register**: Calibrate empathy-to-authority ratio based on ICA segment

## Step 5: Deliver Output

Produce a structured deliverable package:

### Document 1: ICA Decision Architecture Brief
- One-page diagnostic from Step 3 (Awareness–Resistance Map, Objection Sequence, Proof Inventory with gap analysis)
- Format: structured brief suitable for sharing with copywriters, marketing teams, or creative agencies

### Document 2: Conversion Narrative Blueprint
- Full annotated narrative arc from Step 4, with:
  - Section-by-section purpose annotations (why each block exists and which psychological lever it activates)
  - Proof asset placement markers (where each testimonial, case study, or data point deploys)
  - Objection neutralisation callouts (where each of the 5 sequenced objections is pre-empted)

### Document 3: Ready-to-Deploy Copy
- Complete, production-ready copy for the specified asset type
- Headline and sub-headline variants (minimum 3 options, ranked by recommended strength)
- CTA copy variants (minimum 2, with rationale for each)
- Section transitions written in full — no "[insert testimonial here]" placeholders unless proof assets are unavailable

### Document 4: Conversion Risk Register
- Top 5 narrative vulnerabilities ranked by severity (e.g., "Mechanism section relies on Tier 3 proof only — high risk of credibility drop-off at paragraph 12")
- Specific mitigation for each risk
- Recommended proof assets to source or create

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="conversion-narrative-engineer", experiment={
  hypothesis: "Leading with core wound articulation before problem statement increases time-on-page and scroll depth for [ICA segment]",
  variants: ["control: problem-first opening", "variant: wound-first opening with identity language"],
  measurement: "scroll depth percentage, time on page, and click-through rate on primary CTA across minimum 500 sessions",
  expected_impact: "20% improvement in CTA click-through rate based on increased emotional resonance in opening section"
})
```

```
FutureProof:save_experiment(skill="conversion-narrative-engineer", experiment={
  hypothesis: "Deploying the strongest testimonial immediately after the mechanism reveal (rather than in a dedicated social proof section) reduces the belief gap at the critical decision point",
  variants: ["control: testimonials grouped in dedicated section", "variant: anchor testimonial positioned directly after mechanism explanation"],
  measurement: "conversion rate and heatmap engagement at mechanism section across minimum 300 sessions",
  expected_impact: "12% reduction in drop-off at mechanism-to-offer transition"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="conversion-narrative-engineer",
  query="Latest high-converting narrative structures and psychological trigger sequencing for [asset type] in [ICA industry/segment] 2024-2025, including emerging buyer resistance patterns and attention threshold data for digital sales environments",
  reason="Ensure narrative arc construction reflects current buyer psychology, platform algorithm behaviour, and attention economy dynamics rather than legacy copywriting frameworks"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="conversion-narrative-engineer", session={
  summary: "Engineered conversion narrative for [asset type] targeting [ICA segment] at [awareness stage] awareness level for [offer/product name]",
  key_findings: ["ICA decision architecture revealed [key insight about primary objection or awareness gap]", "Proof inventory audit identified [critical gap or strength]", "Narrative arc optimised for [specific psychological lever] based on ICA resistance profile"],
  deliverables: ["ICA Decision Architecture Brief", "Conversion Narrative Blueprint", "Ready-to-Deploy Copy for [asset type]", "Conversion Risk Register"],
  user_feedback: null
})
```