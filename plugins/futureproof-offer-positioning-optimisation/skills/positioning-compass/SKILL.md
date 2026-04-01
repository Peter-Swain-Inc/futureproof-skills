---
name: positioning-compass
description: "Diagnoses and recalibrates offer positioning to maximise ICA resonance, competitive differentiation, and perceived value."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="positioning-compass")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to previously defined ICA profiles, existing offer architecture, brand voice guidelines, and any prior positioning experiments and their outcomes.

## Step 2: Get Input

Ask the user to provide the following (accept partial input and probe for gaps):

1. **The offer** — What specifically is being positioned? (service, programme, product, tier) Share any existing sales page, one-liner, or pitch deck.
2. **The ICA** — Who is this for? Provide demographics, psychographics, stage of awareness, and the language they use to describe their problem. If an ICA profile exists in FutureProof context, confirm or update it.
3. **The competitive landscape** — Name 3–5 direct alternatives the ICA is evaluating (competitors, DIY, status quo, adjacent solutions).
4. **Current positioning assets** — Any taglines, headlines, value propositions, or brand narratives currently in use.
5. **The friction point** — What's not working? (e.g., "prospects say they need to think about it," "we keep competing on price," "nobody understands what we actually do")

If the user cannot articulate competitors, flag this as a diagnostic signal — the ICA may not perceive the offer as occupying a defined category, which is itself a positioning problem.

## Step 3: Conduct Positioning Diagnostic

Perform a structured diagnostic across six positioning dimensions. Score each 1–10 with evidence-based justification:

### 3.1 Category Design Clarity
- Does the offer occupy a clearly defined category in the ICA's mind?
- Is the user creating a new category, entering an existing one, or straddling multiple categories (a common failure mode)?
- Apply the **"If not this, then what?"** test — what does the ICA default to in the absence of this offer?

### 3.2 ICA Problem–Language Fit
- Does the positioning articulate the problem in the exact vocabulary the ICA uses internally (not industry jargon or the user's preferred framing)?
- Evaluate stage-of-awareness alignment: is the messaging calibrated for unaware, problem-aware, solution-aware, product-aware, or most-aware ICAs?
- Flag any curse-of-knowledge gaps where the user describes outcomes the ICA doesn't yet know to want.

### 3.3 Differentiation Integrity
- Map the current positioning against each named competitor on a **value dimension matrix** (speed, depth, access, methodology, specificity, proof, identity alignment).
- Identify whether differentiation is structural (hard to copy) or cosmetic (easily replicated).
- Apply the **"cross out the logo" test** — if you replaced the brand name with a competitor's, would the positioning still make sense? If yes, differentiation has failed.

### 3.4 Value Articulation Precision
- Is the transformation (before state → after state) explicit and concrete?
- Are outcomes expressed in the ICA's value currency (revenue, time, status, certainty, pain removal) rather than abstract benefits?
- Evaluate the **specificity gradient**: vague ("grow your business") → directional ("get more clients") → precise ("add 5 qualified discovery calls per week within 60 days").

### 3.5 Proof Architecture
- Audit the density and quality of proof assets: case studies, testimonials, data points, credentials, methodology lineage, media mentions.
- Assess proof-to-claim ratio — every major claim should have a corresponding proof element within two scroll-lengths or two sentences.
- Identify the **single strongest proof asset** and evaluate whether it is prominently deployed or buried.

### 3.6 Strategic Coherence
- Does the positioning align with the user's broader offer ecosystem, pricing architecture, and delivery model?
- Is there a positioning–pricing contradiction? (e.g., premium positioning with discount-driven acquisition)
- Does the positioning support the intended buyer journey or create friction at the point of conversion?

Apply any user-specific `instructions` from FutureProof context to weight dimensions differently based on business model, maturity stage, or stated priorities.

## Step 4: Build the Competitive Positioning Map

Construct a **2×2 Positioning Map** using the two value dimensions most contested in the user's competitive landscape.

Format:

```
POSITIONING MAP: [Offer Name]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Axis X: [Value Dimension A] (Low → High)
Axis Y: [Value Dimension B] (Low → High)

Quadrant Placement:
• [Competitor 1]: Low A / High B — "the [archetype]"
• [Competitor 2]: High A / Low B — "the [archetype]"
• [Competitor 3]: Low A / Low B — "the [archetype]"
• [User's Offer - CURRENT]: [placement] — "the [archetype]"
• [User's Offer - RECOMMENDED]: [placement] — "the [archetype]"

White Space Identified: [description of underserved quadrant or axis position]
```

Explain the strategic rationale for the recommended repositioning and the specific messaging shifts required to claim the target position credibly.

## Step 5: Deliver the Positioning Compass Output

Produce a **Positioning Compass Brief** — a structured, implementation-ready document containing:

### A. Diagnostic Scorecard

| Dimension | Score (1–10) | Critical Issue |
|---|---|---|
| Category Design Clarity | X | [one-line finding] |
| ICA Problem–Language Fit | X | [one-line finding] |
| Differentiation Integrity | X | [one-line finding] |
| Value Articulation Precision | X | [one-line finding] |
| Proof Architecture | X | [one-line finding] |
| Strategic Coherence | X | [one-line finding] |
| **Composite Positioning Score** | **X/60** | |

### B. Repositioned Core Narrative

Deliver a complete **Positioning Stack** in this exact format:

1. **Category Statement**: "We are the [category] for [ICA segment]."
2. **Problem Statement** (in ICA language): "[Specific pain] is costing you [specific consequence], and [why existing alternatives fail]."
3. **Differentiator**: "Unlike [primary alternative], we [structural difference] which means [outcome the ICA values]."
4. **Proof Anchor**: "[Single most compelling proof point — specific, quantified, verifiable]."
5. **Transformation Statement**: "You go from [vivid before state] to [vivid after state] in [timeframe/mechanism]."
6. **One-Liner** (≤15 words): A deploy-ready positioning statement for headlines, bios, and introductions.

### C. Critical Fixes (Top 3)

For each fix, provide:
- **The problem**: What is broken and the revenue/conversion impact
- **The fix**: Specific language, structural change, or strategic shift (not vague direction)
- **Implementation copy**: Rewritten headline, tagline, or paragraph ready for deployment

### D. Messaging Do / Don't Guide

A concise reference table of 5–7 rules:

| Instead of (current) | Use (repositioned) | Rationale |
|---|---|---|
| [current phrase] | [repositioned phrase] | [why this resonates with ICA] |

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="positioning-compass", experiment={
  hypothesis: "Leading with the repositioned problem statement increases ICA engagement compared to the current benefit-led opening",
  variants: [
    "control: current headline and opening value proposition",
    "variant A: problem-first positioning stack opening",
    "variant B: differentiator-led opening against primary competitor"
  ],
  measurement: "Sales page scroll depth, time on page, and discovery call booking rate over 30 days",
  expected_impact: "20–35% improvement in page-to-booking conversion based on improved problem–language fit"
})
```

Propose a second experiment if the diagnostic revealed a category design or proof architecture issue:

```
FutureProof:save_experiment(skill="positioning-compass", experiment={
  hypothesis: "[Context-specific hypothesis based on lowest-scoring dimension]",
  variants: ["control: [current approach]", "variant: [specific repositioning tactic]"],
  measurement: "[Specific metric and timeframe]",
  expected_impact: "[Quantified expected improvement with reasoning]"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="positioning-compass",
  query="Current positioning frameworks and differentiation strategies in [user's industry/niche] with emphasis on ICA perception studies, category creation patterns, and high-converting value proposition structures 2024–2025",
  reason="Ensure positioning recommendations reflect current market dynamics, emerging competitor narratives, and evolving ICA language patterns in the user's specific vertical"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="positioning-compass", session={
  summary: "Positioning diagnostic and repositioning for [offer name] targeting [ICA segment] against [number] competitors",
  key_findings: [
    "Composite positioning score: [X/60] — [overall assessment]",
    "Primary positioning failure: [lowest-scoring dimension and one-line diagnosis]",
    "Recommended repositioning: [one-line summary of strategic shift]",
    "Deployed positioning stack with one-liner: '[the one-liner]'",
    "Experiments proposed: [number] — focused on [brief description]"
  ],
  user_feedback: null
})
```