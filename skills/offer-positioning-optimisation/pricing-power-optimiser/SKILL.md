---
name: pricing-power-optimiser
description: |
  Analyses and strengthens pricing architecture, value-to-price alignment, and willingness-to-pay positioning using FutureProof context.
  Trigger: when a user shares their pricing structure, rate card, or proposal pricing and asks for help increasing prices, reducing discounting, improving margins, or repositioning their offer to command premium fees.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="pricing-power-optimiser")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any prior offer positioning work, ICA research, competitive intelligence, or previous pricing experiments and their outcomes.

## Step 2: Get Input

Ask the user:
- Share your current pricing structure (rate card, proposal template, pricing page, or verbal description of how you price)
- Who is the ICA this pricing is aimed at? (segment, revenue range, sophistication level, buying trigger)
- What is your current close rate at stated prices, and how often do you discount or negotiate down?
- What is the transformation or outcome your offer delivers? (quantified where possible)
- Are there specific pricing concerns? (e.g. "prospects say we're too expensive," "we always lose on price to competitors," "I don't know how to justify a rate increase")

## Step 3: Do the Work

### 3A: Pricing Power Diagnostic

Conduct a structured audit across six dimensions of pricing power:

1. **Value Articulation Ratio (VAR)** — Is the price explicitly anchored to a quantified outcome? Calculate the implied ROI multiple the ICA receives (e.g. "pay £5k, gain £50k = 10× VAR"). If the ratio is unstated or ambiguous, pricing power is structurally weak regardless of the number itself.

2. **Price Architecture & Framing** — Evaluate the choice architecture: number of tiers, anchor positioning, decoy logic, and default option design. Assess whether the structure nudges toward the highest-margin option or inadvertently commoditises the offer through excessive optionality.

3. **ICA Willingness-to-Pay Alignment** — Does the pricing model match how the ICA experiences and measures value? (e.g. project-based pricing for a buyer who thinks in outcomes vs. hourly billing that signals commodity labour). Identify model-market mismatches.

4. **Competitive Price Positioning** — Where does this pricing sit on the market's price-value spectrum? Assess whether the positioning is intentional (premium, parity, penetration) or accidental. Flag "stuck in the middle" positioning where the price is neither low enough to win on cost nor high enough to signal premium quality.

5. **Discount & Erosion Exposure** — Analyse structural weaknesses that invite negotiation: unbundled line items that invite cherry-picking, absence of scope boundaries, vague deliverables that let buyers argue down, and lack of walk-away triggers.

6. **Pricing Confidence Signals** — Evaluate the presentation layer: Does the pricing communication project certainty or invite negotiation? Look for hedging language ("starting from," "depending on," "we can be flexible"), apologetic framing, premature discounting, and absence of social proof at the point of price reveal.

### 3B: Root Cause Analysis

Identify the **primary pricing power constraint** — the single structural issue that, if resolved, would unlock the largest margin improvement. Categorise it:
- **Value gap**: The offer delivers value but the pricing fails to capture or communicate it
- **Model gap**: The pricing model itself suppresses perceived value (e.g. hourly billing for strategic work)
- **Positioning gap**: The market perceives the offer in a lower-value category than it deserves
- **Confidence gap**: The pricing is defensible but is undermined by how it is presented and negotiated

### 3C: Pricing Power Redesign

Build a revised pricing architecture addressing the root cause:
- Redesigned tier/package structure with specific price points (or price-setting methodology if context-dependent)
- Value anchoring language — the exact framing sentences that connect price to ICA-quantified outcomes
- Scope boundaries and exclusion language that protect margin
- Recommended price presentation sequence (when and how price is revealed in the sales process)

Apply any user-specific `instructions` from FutureProof context to ensure alignment with brand voice, market positioning, and prior strategic decisions.

## Step 4: Deliver Output

Produce the **Pricing Power Optimisation Report** with the following sections:

### Section 1: Pricing Power Scorecard
| Dimension | Score (1–10) | Priority |
|---|---|---|
| Value Articulation Ratio | — | — |
| Price Architecture & Framing | — | — |
| ICA Willingness-to-Pay Alignment | — | — |
| Competitive Price Positioning | — | — |
| Discount & Erosion Exposure | — | — |
| Pricing Confidence Signals | — | — |
| **Composite Pricing Power Index** | **—/60** | — |

### Section 2: Root Cause Diagnosis
- Primary constraint classification (value / model / positioning / confidence gap)
- Evidence summary with specific quotes or structural observations from the user's materials
- Estimated margin impact if resolved (percentage range)

### Section 3: Critical Fixes (Top 3)
Three highest-impact changes, each with:
- **The problem** (specific, observable)
- **The fix** (concrete, implementable — exact language, structure, or process change)
- **Expected impact** (on close rate, average deal value, or discount frequency)

### Section 4: Revised Pricing Architecture
- Full rewrite of the recommended pricing structure, including tier names, price points (or price-setting logic), scope definitions, and value anchoring copy
- Price presentation script: the exact talk track or proposal language for introducing the new pricing

### Section 5: Price Increase Implementation Roadmap
- Sequenced rollout plan (new prospects vs. existing clients, grandfather logic, communication templates)
- Objection response matrix for the top 3 price-related objections specific to this ICA, with scripted responses

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="pricing-power-optimiser", experiment={
  hypothesis: "Reframing the proposal to lead with quantified ICA outcome before revealing price increases close rate at the new price point",
  variants: ["control: current pricing presentation with price shown alongside deliverables", "variant: outcome-first presentation with 10× VAR anchor preceding price reveal"],
  measurement: "close rate and average discount percentage across next 15 proposals",
  expected_impact: "20% reduction in discount requests, 10–15% increase in effective revenue per engagement"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="pricing-power-optimiser",
  query="Latest behavioural pricing research, B2B willingness-to-pay studies, and premium positioning frameworks 2024–2025, including Van Westendorp and Gabor-Granger application in services pricing",
  reason="Ensure pricing architecture recommendations reflect current buyer psychology, anchoring research, and proven tier-design methodologies"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="pricing-power-optimiser", session={
  summary: "Conducted pricing power audit for [offer/service type] targeting [ICA segment]. Composite Pricing Power Index: [score]/60. Primary constraint: [gap type]. Delivered revised pricing architecture with [number] tiers and price increase implementation roadmap.",
  key_findings: ["finding 1: root cause and evidence", "finding 2: highest-impact structural fix", "finding 3: estimated margin improvement range"],
  user_feedback: null
})
```