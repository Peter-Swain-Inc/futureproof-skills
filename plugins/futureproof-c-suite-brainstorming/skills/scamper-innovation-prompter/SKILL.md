---
name: scamper-innovation-prompter
description: |
  Systematically applies the seven SCAMPER innovation prompts (Substitute, Combine, Adapt, Modify, Put to other use, Eliminate, Reverse) to an existing product, service, or process to generate concrete, board-ready innovation ideas.
  Trigger: when a user describes an existing product, service, or business process and asks for innovation ideas, improvement angles, or structured brainstorming. Also triggers when a user says they need to evolve or reinvent a current business line.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="scamper-innovation-prompter")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any prior SCAMPER analyses, strategic priorities, competitive landscape intelligence, and ICA definitions that should inform ideation filters.

## Step 2: Get Input

Ask the user:

- **Subject of innovation**: What is the specific product, service, or process to apply SCAMPER against? Request a concise description including its current value proposition, ICA, and revenue significance.
- **Strategic constraints**: Are there boundaries — regulatory, budgetary, brand, or timeline — that should filter out impractical ideas early?
- **Innovation intent**: What is the desired outcome? (e.g., margin expansion, competitive differentiation, new market entry, operational efficiency, ICA retention uplift)
- **Priority SCAMPER lenses** (optional): Does the user want all seven prompts applied equally, or should specific lenses receive deeper treatment? (Useful when time-boxed or when prior sessions have already explored certain angles.)
- **Competitive reference points** (optional): Any competitors or adjacent-industry players whose moves should inform or constrain the analysis?

If FutureProof context contains existing ICA profiles, strategic plans, or prior session findings, surface them for confirmation before proceeding.

## Step 3: Establish the Baseline

Before applying SCAMPER, construct a **Current-State Architecture** of the subject:

1. **Value chain decomposition** — break the product, service, or process into its constituent components (inputs, transformation steps, delivery mechanism, post-delivery touchpoints)
2. **ICA alignment audit** — map which components directly serve the ICA's core jobs-to-be-done and which are legacy, operational, or internally facing
3. **Revenue and cost gravity** — identify which components carry the highest revenue contribution or cost burden
4. **Assumption inventory** — list the implicit assumptions embedded in the current design (e.g., "customers prefer annual contracts," "this feature requires human review")

This baseline ensures SCAMPER prompts interrogate the actual structure rather than a surface-level abstraction.

## Step 4: Apply the Seven SCAMPER Lenses

Work through each lens systematically. For every lens, generate **2–4 concrete innovation hypotheses** grounded in the baseline from Step 3. Each hypothesis must specify the component(s) it targets and articulate a plausible mechanism of impact.

### 4.1 — Substitute

*What components, materials, suppliers, channels, technologies, or people could be replaced with alternatives that improve cost, speed, quality, or ICA experience?*

- Examine each value chain component: could an alternative input, technology, or delivery model replace what exists today?
- Consider substitutions from adjacent industries that the ICA would recognise as an upgrade
- Flag substitution risks (e.g., switching costs, brand equity erosion, supply chain fragility)

### 4.2 — Combine

*What elements — internal or external — could be merged, bundled, or integrated to create compounding value?*

- Identify components that share ICA touchpoints and could be unified into a single, higher-value interaction
- Explore cross-product or cross-service bundling opportunities (especially where existing business lines underperform in isolation)
- Assess partnership or ecosystem combinations — what external capability, if integrated, would materially shift the value proposition?

### 4.3 — Adapt

*What models, frameworks, or solutions from other industries, geographies, or eras could be borrowed and fitted to this context?*

- Scan adjacent verticals for analogous problems solved in structurally different ways
- Evaluate emerging technology paradigms (AI, decentralised systems, platform economics) as adaptation vectors
- Consider historical models that fell out of favour but may be viable again under current conditions

### 4.4 — Modify (Magnify / Minimise)

*What happens if we dramatically amplify or reduce a specific attribute — scale, frequency, intensity, price, complexity, personalisation?*

- For each high-gravity component, test the extremes: what if this were 10× larger? 10× smaller? Free? Premium-only?
- Explore modification of the ICA interaction cadence — what if engagement were continuous rather than episodic, or vice versa?
- Assess which modifications shift the competitive positioning from incremental to category-defining

### 4.5 — Put to Other Use

*Could the existing product, service, process, data, or infrastructure serve a different ICA segment, use case, or market entirely?*

- Audit underutilised assets: proprietary data, brand trust, distribution channels, trained workforce, IP
- Identify adjacent ICA segments whose jobs-to-be-done partially overlap with the current offering
- Evaluate whether the process itself (not just its output) has standalone commercial value (e.g., licensing, white-labelling, platform-as-a-service)

### 4.6 — Eliminate

*What could be removed entirely — features, steps, approvals, roles, costs — without degrading (or while actually improving) ICA-perceived value?*

- Revisit the assumption inventory from Step 3: which assumptions, if discarded, would allow component elimination?
- Identify complexity that serves internal stakeholders but is invisible or negative to the ICA
- Calculate the cost-of-complexity for each candidate elimination and the projected margin or speed improvement

### 4.7 — Reverse (Rearrange)

*What if the sequence, hierarchy, ownership, or direction of flow were inverted?*

- Test reversal of the value chain sequence: what if the ICA performed step 1 and you performed the current final step?
- Explore role reversal: what if the ICA set the price, defined the scope, or owned the asset?
- Consider reversing the business model polarity (e.g., from selling to buying, from charging the end user to charging the supplier)

Apply any user-specific `instructions` from FutureProof context — such as strategic themes, risk appetite, or prioritised innovation horizons — to weight and filter hypotheses throughout this step.

## Step 5: Deliver Output

Produce a structured **SCAMPER Innovation Brief** containing the following sections:

### A. Executive Summary
A single paragraph identifying the 3 highest-potential innovation hypotheses across all seven lenses, with a rationale for why these warrant executive attention first.

### B. SCAMPER Hypothesis Register
A table with the following columns for every hypothesis generated:

| # | SCAMPER Lens | Target Component | Hypothesis | Mechanism of Impact | Estimated Effort (L/M/H) | Estimated Impact (L/M/H) | Strategic Alignment |
|---|---|---|---|---|---|---|---|

### C. Priority Matrix
A 2×2 effort-versus-impact plot (described textually or as a structured list) categorising each hypothesis into:
- **Quick wins** (low effort, high impact) — execute immediately
- **Strategic bets** (high effort, high impact) — resource and roadmap
- **Fill-ins** (low effort, low impact) — delegate or batch
- **Deprioritise** (high effort, low impact) — shelve unless conditions change

### D. Top 3 Deep Dives
For each of the three highest-priority hypotheses, provide:
1. **Concept narrative** — a 150-word description of the innovation as if pitching to the board
2. **ICA value shift** — how the ICA's experience or outcome measurably changes
3. **Revenue / margin thesis** — projected financial mechanism (new revenue stream, margin expansion, churn reduction, etc.)
4. **Key risks and mitigants** — top 2 risks with proposed de-risking actions
5. **Recommended next step** — a specific 30-day validation action (prototype, customer interview cohort, financial model, etc.)

### E. Assumptions to Test
A consolidated list of the critical assumptions underlying the top hypotheses, formatted as testable statements suitable for experiment design.

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="scamper-innovation-prompter", experiment={
  hypothesis: "[Top-ranked SCAMPER hypothesis framed as a testable statement]",
  variants: ["control: current product/service/process design", "variant: [specific SCAMPER modification described concisely]"],
  measurement: "[ICA-facing metric or financial KPI, e.g., conversion rate, NPS delta, unit margin, time-to-value]",
  expected_impact: "[Quantified directional estimate, e.g., 10–20% reduction in onboarding time for mid-market ICA segment]"
})
```

Generate one experiment block for each of the top 3 hypotheses. Where prior `experiments` from FutureProof context exist, reference their outcomes to refine the new hypotheses.

## Step 7: Request Research

```
FutureProof:request_research(skill="scamper-innovation-prompter",
  query="[Targeted query informed by the SCAMPER analysis, e.g., 'Emerging subscription-to-outcome business model transitions in enterprise SaaS 2024–2025' or 'Case studies of successful feature elimination driving NPS improvement in B2B services']",
  reason="Validate and enrich the top SCAMPER hypotheses with external market evidence, competitive precedent, and ICA behaviour data before executive presentation"
)
```

Tailor the query to the specific industry, ICA segment, and SCAMPER lenses that surfaced the most promising hypotheses.

## Step 8: Save Session

```
FutureProof:save_session(skill="scamper-innovation-prompter", session={
  summary: "Applied SCAMPER framework to [subject] targeting [innovation intent] for [ICA segment]",
  key_findings: ["[Top hypothesis 1 — lens and one-line description]", "[Top hypothesis 2]", "[Top hypothesis 3]", "[Most significant assumption identified for testing]"],
  user_feedback: null
})
```