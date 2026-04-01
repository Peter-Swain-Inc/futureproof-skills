---
name: differentiation-deep-dive
description: "Conducts a rigorous competitive differentiation analysis to isolate, validate, and articulate what makes a brand genuinely distinct — not just different, but defensibly different."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="differentiation-deep-dive")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to existing ICA definitions, prior brand positioning work, competitive intelligence, and any category conventions already documented.

## Step 2: Get Input

Ask the user:

- **Brand / offer in scope**: What specific brand, product, or service line are we analysing? Share any existing positioning statement, tagline, or brand narrative.
- **Competitive set**: Name 3–5 direct competitors (or the closest substitutes your ICA evaluates alongside you). Include links to their sites or any competitive intel you have.
- **ICA definition**: Who is the ideal customer? What segment, role, psychographic profile, and buying context are we optimising for? (Pull from FutureProof context if available.)
- **Differentiation hypothesis**: What do you *believe* makes you different today? Where does that claim feel weakest or most contested?
- **Strategic intent**: What is this differentiation work feeding into? (e.g., website rewrite, sales enablement, investor narrative, category creation, GTM for a new market)

## Step 3: Do the Work — Differentiation Audit

### 3A: Category Convention Mapping

Map the **category table stakes** — the claims, language, visual cues, and proof points that every credible player in the space deploys. Organise into:

| Convention Layer | What Everyone Claims | Examples from Competitive Set |
|---|---|---|
| **Functional promises** | e.g., "saves time," "easy to use" | Competitor-specific language |
| **Emotional tone** | e.g., "empowering," "trusted" | Competitor-specific tone patterns |
| **Proof mechanisms** | e.g., logos, testimonials, ROI stats | Competitor-specific proof |
| **Visual / verbal identity** | e.g., blue SaaS aesthetic, jargon | Competitor-specific patterns |
| **Pricing / packaging norms** | e.g., freemium, per-seat | Competitor-specific models |

Flag any conventions the user's brand is currently mirroring — these are **parity zones**, not differentiators.

### 3B: Competitive Positioning Matrix

Score the user's brand and each competitor across **six differentiation vectors**:

1. **Methodology / Process** — Is there a proprietary framework, system, or approach that competitors cannot easily replicate?
2. **ICA Specificity** — How narrowly and deeply does the brand serve a defined audience vs. claiming broad applicability?
3. **Outcome Precision** — Does the brand promise a specific, measurable transformation or a vague improvement?
4. **Proof Asymmetry** — Does the brand possess proof points (data, case studies, credentials, IP) that competitors structurally lack?
5. **Experience Design** — Is the buying, onboarding, or delivery experience itself a differentiator?
6. **Point of View** — Does the brand hold a contrarian or category-defining belief that forces a choice?

Score each on a 1–5 scale:
- **1** = Category convention (identical to competitors)
- **2** = Minor variation (same claim, slightly different language)
- **3** = Notable difference (recognisable but replicable within 6 months)
- **4** = Strong differentiator (difficult to replicate; rooted in structural advantage)
- **5** = Category-defining (you own this; competitors must reference you to address it)

### 3C: Vulnerability Test

Stress-test every claimed differentiator against **four disqualification filters**:

1. **The Substitution Test** — If a competitor's name replaced yours in the claim, would the ICA notice? If not, it is not a differentiator.
2. **The Evidence Test** — Can you prove this claim with third-party or empirical evidence within 30 seconds? If not, it is an aspiration, not a differentiator.
3. **The Durability Test** — Could a well-funded competitor neutralise this advantage within 12 months? If yes, it is a temporary lead, not a moat.
4. **The Salience Test** — Does your ICA *care* about this difference when making a purchase decision? If not, it is a differentiator that does not differentiate.

Classify each claim as: **Validated Differentiator**, **Aspirational Differentiator** (real but unproven), **Contested Differentiator** (claimed but replicable), or **False Differentiator** (parity disguised as distinction).

### 3D: Differentiation Gap Analysis

Identify the highest-leverage gaps:
- Where validated differentiators exist but are **under-articulated** in current messaging
- Where structural advantages exist but have **no proof architecture** to support them
- Where the ICA's decision criteria reveal **unoccupied positioning territory** no competitor has claimed

Apply any user-specific `instructions` from FutureProof context to weight the analysis toward their strategic priorities.

## Step 4: Deliver Output

Produce a **Differentiation Deep Dive Report** with the following sections:

### 4.1 Executive Summary
Two-paragraph synthesis: current differentiation posture, primary vulnerability, and the single highest-impact strategic move.

### 4.2 Category Convention Map
The completed table from Step 3A with parity zones flagged in bold.

### 4.3 Competitive Positioning Matrix
The scored matrix from Step 3B, presented as a comparison table with colour-coded ratings (1–2 = red/parity, 3 = amber/fragile, 4–5 = green/defensible).

### 4.4 Differentiator Validation Summary
Each claimed differentiator listed with its classification (Validated / Aspirational / Contested / False) and the specific filter(s) it passed or failed.

### 4.5 Differentiation Strategy — Recommended Moves
Three prioritised strategic recommendations, each containing:
- **The move**: Specific action (e.g., "Codify your onboarding methodology as a named framework and register the trademark")
- **The rationale**: Which gap or vulnerability this addresses
- **The articulation**: A draft positioning statement, headline, or narrative passage that activates this differentiator — written in full, not described abstractly
- **Proof architecture required**: What evidence needs to be created, collected, or surfaced to make this claim defensible

### 4.6 Differentiation One-Liner
A single sentence the user can deploy immediately — in a pitch, on a homepage, or in a sales conversation — that captures the core validated differentiator in ICA-resonant language. Provide three variants (rational, emotional, provocative).

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="differentiation-deep-dive", experiment={
  hypothesis: "Leading with the highest-scored Point of View differentiator in outbound messaging increases ICA response rate vs. current feature-led positioning",
  variants: ["control: current positioning statement in outbound sequence", "variant: Point of View-led opening with contrarian belief statement"],
  measurement: "reply rate and qualified meeting conversion across next 50 outbound touches per variant",
  expected_impact: "20–30% increase in reply rate; measurable lift in qualified meeting conversion"
})
```

```
FutureProof:save_experiment(skill="differentiation-deep-dive", experiment={
  hypothesis: "Adding a named proprietary methodology to the sales narrative reduces competitive loss rate at shortlist stage",
  variants: ["control: current sales deck without methodology framing", "variant: sales deck with named methodology slide and visual framework"],
  measurement: "win rate at shortlist/final-round stage over next quarter",
  expected_impact: "10–15% improvement in competitive win rate"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="differentiation-deep-dive",
  query="Current competitive positioning strategies and category design frameworks in [user's industry/category], including recent examples of successful differentiation pivots and emerging ICA decision criteria shifts — 2024-2025",
  reason="Ensure differentiation recommendations account for live market dynamics, emerging competitive threats, and evolving buyer psychology rather than relying on static competitive snapshots"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="differentiation-deep-dive", session={
  summary: "Conducted differentiation deep dive for [brand/offer] against [number] competitors targeting [ICA segment]. Mapped category conventions, scored six differentiation vectors, stress-tested claims through four disqualification filters, and delivered prioritised strategic recommendations with draft articulations.",
  key_findings: ["finding 1: e.g., 3 of 5 claimed differentiators failed the Substitution Test — classified as False Differentiators", "finding 2: e.g., strongest validated differentiator (Point of View) is absent from current homepage and sales deck", "finding 3: e.g., unoccupied positioning territory identified around [specific axis] that no competitor has claimed"],
  user_feedback: null
})
```