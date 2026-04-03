---
name: value-equation-optimizer
description: |
  Engineers and optimises offers using Alex Hormozi's Value Equation framework from $100M Offers.
  Systematically maximises Dream Outcome × Perceived Likelihood of Achievement while minimising Time Delay × Effort & Sacrifice to produce offers so compelling that prospects feel stupid saying no.
  Trigger: when a user wants to build, redesign, or stress-test a core offer, or when they mention pricing feels commoditised, close rates are low despite strong demand, or they need to increase the perceived value of their deliverables without increasing fulfilment cost.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="value-equation-optimizer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to any previously defined ICA profiles, existing offer structures, pricing benchmarks, and past experiment results related to offer conversion.

## Step 2: Get Input

Ask the user the following in sequence. If FutureProof context already supplies answers, confirm rather than re-ask:

1. **ICA Definition** — Who is the specific person this offer is for? (role, revenue stage, acute pain, psychographic state)
2. **Current Offer State** — Do they have an existing offer to optimise, or are they building from scratch? If existing, request the offer outline, sales page, or pitch deck.
3. **Dream Outcome** — What is the singular, tangible transformation the ICA is paying for? (stated in the ICA's language, not the seller's)
4. **Delivery Mechanism** — How is the outcome currently delivered? (format, timeline, touchpoints)
5. **Competitive Landscape** — What are the 2–3 closest alternatives the ICA is comparing against? (direct competitors, DIY, do nothing)
6. **Pricing Context** — Current or intended price point, and what feels like the ceiling they cannot break through

## Step 3: Map the Value Equation Components

Structure the analysis around Hormozi's four value drivers:

### 3A: Dream Outcome (Numerator — Maximise)

- Articulate the ICA's dream outcome in first-person ICA language ("I want to…")
- Distinguish between the **surface goal** (what they say) and the **deeper goal** (what they actually buy — status, freedom, certainty, identity)
- Rate current offer's Dream Outcome clarity on a 1–10 scale with justification
- Identify gaps where the offer undersells the transformation

### 3B: Perceived Likelihood of Achievement (Numerator — Maximise)

Audit every proof and certainty element across six categories:

| Proof Category | Current Evidence | Strength (1–10) | Gap / Recommendation |
|---|---|---|---|
| Results documentation (case studies, metrics) | | | |
| Social proof (testimonials, logos, volume) | | | |
| Mechanism clarity (why this method works) | | | |
| Credibility markers (credentials, media, associations) | | | |
| Risk reversal (guarantees, trials, clawbacks) | | | |
| Demonstration (free value, audits, samples) | | | |

- Assign a composite Perceived Likelihood score (1–10)
- Identify the single highest-leverage proof element missing

### 3C: Time Delay (Denominator — Minimise)

- Map the current timeline from purchase to first meaningful result
- Identify every phase: onboarding, setup, learning curve, first output, first win, full ROI
- Flag where perceived time exceeds actual time (perception gaps)
- Design **quick wins** — what tangible result can the ICA experience within 24–72 hours of purchase?
- Rate Time Delay perception (1–10, where 10 = feels instant)

### 3D: Effort & Sacrifice (Denominator — Minimise)

Catalogue every form of friction the ICA must endure:

- **Cognitive load** — decisions, learning, complexity
- **Behavioural change** — new habits, disrupted routines
- **Opportunity cost** — what they give up (time, other investments)
- **Social cost** — explaining to partners, team buy-in, reputation risk
- **Technical friction** — integrations, migrations, tool adoption

Rate Effort & Sacrifice (1–10, where 10 = effortless) and identify the top 3 friction points to eliminate or absorb.

## Step 4: Compute the Value Score and Redesign the Offer

### 4A: Value Equation Scorecard

```
VALUE = (Dream Outcome × Perceived Likelihood of Achievement)
        ÷ (Time Delay × Effort & Sacrifice)

Current Score:  (DO: _/10 × PLA: _/10) ÷ (TD: _/10 × ES: _/10) = ___
Target Score:   (DO: _/10 × PLA: _/10) ÷ (TD: _/10 × ES: _/10) = ___
```

*Note: For denominator scores, invert the scale for calculation — a 10 in "feels instant" translates to a 1 in the denominator (minimal drag). Display both the user-friendly rating and the calculation value.*

### 4B: Offer Stack Architecture

Reconstruct the offer as a layered stack. For each component, specify:

| Stack Layer | Deliverable | Value Driver It Serves | Perceived Value ($) | Fulfilment Cost ($) |
|---|---|---|---|---|
| Core outcome vehicle | | | | |
| Quick-win accelerator | | | | |
| Effort reducer / done-for-you layer | | | | |
| Risk reversal mechanism | | | | |
| Scarcity / urgency element | | | | |
| Bonus: objection destroyer #1 | | | | |
| Bonus: objection destroyer #2 | | | | |

- Calculate **Total Perceived Value** vs. **Asking Price** — target a minimum 10:1 value-to-price ratio
- Calculate **Gross Fulfilment Margin** to ensure the offer is operationally viable

### 4C: Critical Fixes — Top 5 Highest-Impact Changes

For each fix, provide:
1. **What to change** — specific, not directional
2. **Why it matters** — which Value Equation variable it moves and by how much
3. **Exact implementation** — copy rewrites, structural changes, or new deliverable specifications
4. **Expected impact on conversion** — quantified estimate with reasoning

### 4D: Naming and Framing

- Propose 3 offer names that encode the Dream Outcome (not the mechanism)
- Write a single-sentence offer statement: *"We help [ICA] achieve [Dream Outcome] in [Timeframe] without [Primary Effort/Sacrifice], guaranteed by [Risk Reversal]."*
- Draft the 60-second verbal pitch for the redesigned offer

## Step 5: Deliver Output

Produce the following structured deliverables:

1. **Value Equation Scorecard** — current vs. redesigned scores across all four variables with delta analysis
2. **Offer Stack Blueprint** — the complete table from Step 4B, ready for sales page or pitch deck integration
3. **Top 5 Critical Fixes Document** — implementation-ready changes ranked by impact-to-effort ratio
4. **Offer One-Liner and 60-Second Pitch** — polished copy for immediate use
5. **Competitive Differentiation Map** — how the redesigned offer creates categorical separation from the 2–3 alternatives identified in Step 2

Apply any user-specific `instructions` from FutureProof context (e.g. brand voice, pricing philosophy, fulfilment constraints) to refine all deliverables.

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="value-equation-optimizer", experiment={
  hypothesis: "Adding a 72-hour quick-win deliverable reduces perceived Time Delay and increases trial-to-paid conversion",
  variants: [
    "control: current onboarding sequence with first result at day 14",
    "variant: restructured onboarding with tangible quick-win asset delivered within 72 hours"
  ],
  measurement: "trial-to-paid conversion rate and post-onboarding NPS score over next 30 days",
  expected_impact: "20% improvement in trial-to-paid conversion by compressing perceived Time Delay"
})
```

```
FutureProof:save_experiment(skill="value-equation-optimizer", experiment={
  hypothesis: "Reframing the guarantee from money-back to performance-based increases Perceived Likelihood of Achievement and close rate",
  variants: [
    "control: 30-day money-back guarantee",
    "variant: outcome-based guarantee tied to specific measurable result"
  ],
  measurement: "close rate on sales calls and refund/guarantee-claim rate over next 60 days",
  expected_impact: "10–15% improvement in close rate with no increase in guarantee claims"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="value-equation-optimizer",
  query="High-converting offer structures and guarantee frameworks in [user's industry/niche] 2024–2025, including emerging risk-reversal models and value-stack patterns from top-performing info-product and service businesses",
  reason="Ensure offer architecture reflects current buyer expectations and competitive offer design standards; identify novel proof and friction-reduction mechanisms the user can adopt"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="value-equation-optimizer", session={
  summary: "Engineered Value Equation offer for [ICA segment] — scored current offer at [X], redesigned to target [Y] across all four value drivers",
  key_findings: [
    "Primary value leak: [specific denominator issue, e.g. perceived Time Delay of 90 days suppressing urgency]",
    "Highest-leverage fix: [specific change, e.g. adding done-for-you onboarding layer reduces Effort & Sacrifice by 3 points]",
    "Offer stack redesigned with [N] components at [value-to-price ratio] perceived value ratio",
    "Competitive differentiation established via [specific mechanism or guarantee structure]"
  ],
  deliverables_produced: [
    "Value Equation Scorecard (current vs. redesigned)",
    "Offer Stack Blueprint",
    "Top 5 Critical Fixes Document",
    "Offer One-Liner and 60-Second Pitch",
    "Competitive Differentiation Map"
  ],
  user_feedback: null
})
```