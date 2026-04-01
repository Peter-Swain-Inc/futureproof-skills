---
name: synthetic-focus-group
description: "Simulates a multi-persona focus group using AI-generated panellists grounded in the user's ICA profiles, market context, and FutureProof research history."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="synthetic-focus-group")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to populate panellist archetypes, calibrate sentiment baselines from prior sessions, and apply any user-specific moderation preferences.

## Step 2: Get Input

Ask the user:

- **Stimulus material** — share the asset to be tested (product concept, landing page copy, pricing table, ad creative, packaging design description, feature set, positioning statement, or campaign theme)
- **ICA definition** — who is the intended audience? Request demographic, psychographic, and behavioural descriptors. If FutureProof context already contains ICA profiles, confirm or refine them
- **Panel composition request** — how many panellists (default: 6), any specific segments to over-index (e.g., power users vs. first-time buyers, budget-conscious vs. premium-oriented), and whether to include a deliberate contrarian/hostile panellist
- **Research objective** — what decision does this focus group inform? (go/no-go on launch, A vs. B creative selection, pricing tier validation, messaging hierarchy ranking)
- **Sensitivity flags** — any topics, competitor names, or language the user wants panellists to specifically probe or avoid

## Step 3: Construct the Panel

Build each synthetic panellist as a **Panellist Dossier** containing:

1. **Persona name and archetype label** — e.g., "Dana — The Sceptical Mid-Market Ops Lead"
2. **Demographic snapshot** — age range, role/title, company size, geography, income bracket
3. **Psychographic profile** — core motivations, decision-making style (analytical, impulsive, consensus-seeking), media diet, brand affinities
4. **Behavioural context** — current tools/solutions used, switching triggers, deal-breakers, budget authority level
5. **Attitude seed** — a 1-sentence internal monologue that anchors this panellist's default disposition toward the stimulus category (e.g., "I've been burned by tools that promise automation but create more admin work")
6. **Voice calibration** — vocabulary register (technical jargon vs. plain language), communication style (direct, diplomatic, verbose), emotional expressiveness level

Validate panel composition against the stated ICA to ensure coverage across:
- Enthusiasm spectrum (advocate → neutral → hostile)
- Decision-making authority (end-user → influencer → budget holder)
- Adoption curve position (early adopter → mainstream → laggard)

Present the panel roster to the user for approval before proceeding.

## Step 4: Run the Focus Group Simulation

Execute a structured **three-round moderation protocol**:

### Round 1 — First Impressions (Unprimed Reaction)
Present the stimulus to each panellist without framing. Capture per-panellist:
- **Gut reaction** — one-sentence instinctive response
- **Comprehension check** — what do they believe this is/does, in their own words
- **Emotional valence** — positive, negative, mixed, or indifferent, with a stated reason
- **First question** — the single thing they would ask if they could

### Round 2 — Structured Probing
Moderate a guided discussion across five diagnostic dimensions:

1. **Relevance** — "Does this solve a problem you actually have, or a problem someone imagines you have?"
2. **Credibility** — "Do you believe the claims being made? What proof would you need?"
3. **Differentiation** — "How is this different from what you use/see today? Could you explain the difference to a colleague?"
4. **Value perception** — "What would you expect to pay? What would make this feel expensive vs. cheap?"
5. **Friction mapping** — "What would stop you from saying yes right now? What would need to be true for you to act?"

Each panellist responds in character. Surface disagreements and inter-panellist debate where perspectives naturally conflict.

### Round 3 — Comparative & Constructive
- If the user provided multiple variants (A/B creative, tiered pricing), run a **forced-rank exercise** with rationale per panellist
- Ask each panellist to complete: "I would share this with someone if ___" and "I would ignore this if ___"
- Final **recommendation round**: each panellist gives a thumbs-up, thumbs-sideways, or thumbs-down with a one-sentence justification

## Step 5: Deliver Output

Produce a **Synthetic Focus Group Debrief Report** with the following sections:

### 5.1 — Executive Summary
- One-paragraph synthesis of the dominant finding
- Go / Iterate / Pivot recommendation with confidence level (high / moderate / low)

### 5.2 — Panel Roster Reference
- Table of all panellists: Name, Archetype, Segment, Overall Sentiment (positive/mixed/negative)

### 5.3 — Consensus & Divergence Map
- **Points of consensus** — findings where ≥70% of panellists aligned (bulleted, ranked by strategic importance)
- **Points of divergence** — findings where the panel split, with segment-level attribution (e.g., "Budget holders were uniformly negative on Tier 3 pricing; end-users were indifferent to price but concerned about onboarding time")

### 5.4 — Dimension Scorecard
| Dimension | Avg. Score (1–10) | Range | Critical Verbatim |
|---|---|---|---|
| Relevance | | | |
| Credibility | | | |
| Differentiation | | | |
| Value Perception | | | |
| Friction Level (inverted) | | | |

### 5.5 — Top 5 Actionable Insights
Each insight formatted as:
- **Observation** — what the panel revealed
- **Implication** — what it means for the user's decision
- **Recommended action** — specific, implementable next step (copy rewrites, pricing restructures, proof-point additions — not vague advice)

### 5.6 — Verbatim Highlight Reel
8–12 direct quotes from panellists, attributed by name, selected for maximum strategic signal. Flag any quote that contradicts the user's stated assumptions.

### 5.7 — Risk Register
Identify 2–4 audience-side risks the stimulus currently carries (e.g., "Messaging implies enterprise-grade capability, which may create expectation debt for mid-market ICA segments") with severity rating and mitigation suggestion.

### 5.8 — Recommended Stimulus Revision
Rewrite or restructure the single highest-impact element of the original stimulus (e.g., the headline, the pricing anchor, the CTA, the hero section) incorporating panel feedback. Provide before/after with annotation explaining each change.

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="synthetic-focus-group", experiment={
  hypothesis: "Addressing the top friction point surfaced by the hostile panellist segment in the opening line increases stated purchase intent among sceptical ICA profiles",
  variants: ["control: current stimulus as submitted", "variant: revised stimulus with friction-first framing from Section 5.8"],
  measurement: "Re-run synthetic focus group with fresh panel in 2 weeks; compare dimension scores and sentiment distribution. Validate against real-world engagement metrics if stimulus is deployed (CTR, conversion rate, or qualitative sales feedback)",
  expected_impact: "20% improvement in credibility and friction scores among sceptical panellist archetypes; directional lift in real-world conversion if deployed"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="synthetic-focus-group",
  query="Latest qualitative research methodologies for validating synthetic persona accuracy against real consumer panels, including bias correction frameworks and calibration benchmarks 2024–2025",
  reason="Continuously improve panellist fidelity by grounding synthetic archetypes in validated behavioural science and emerging ICA modelling techniques"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="synthetic-focus-group", session={
  summary: "Ran synthetic focus group with [N] panellists testing [stimulus type] for [ICA segment]. Primary objective: [research objective].",
  key_findings: ["finding 1: dominant consensus or divergence point", "finding 2: highest-impact actionable insight", "finding 3: unexpected risk or opportunity surfaced"],
  panel_composition: ["archetype 1", "archetype 2", "..."],
  stimulus_tested: "[brief description of stimulus]",
  recommendation: "go / iterate / pivot",
  user_feedback: null
})
```