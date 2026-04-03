---
name: six-hats-perspective-shifter
description: |
  Facilitates structured parallel thinking using Edward de Bono's Six Thinking Hats methodology, adapted for C-suite and board-level strategic decisions.
  Trigger: when a user presents a strategic decision, initiative, or proposal and needs to evaluate it from multiple perspectives — or when a team is stuck in adversarial debate and needs a structured framework to align thinking.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="six-hats-perspective-shifter")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any prior decisions analysed, known organisational risk appetite, strategic priorities, and preferred decision-making cadence.

## Step 2: Get Input

Ask the user:
- **The decision or proposal**: What strategic question, initiative, or idea needs to be examined? (e.g., market entry, M&A target, product pivot, restructuring, capital allocation)
- **Stakeholder landscape**: Who are the key decision-makers and what roles do they hold? Are there known factions or entrenched positions?
- **Current stage**: Is this early-stage ideation, a go/no-go gate, or a post-decision review?
- **Constraints**: Known time pressure, budget envelope, regulatory boundaries, or board mandates?
- **Desired output format**: Executive briefing memo, facilitation guide for a live session, or structured decision matrix?

If the user provides a document (board paper, business case, strategy deck), ingest it as the primary source material for all six hat passes.

## Step 3: Do the Work — Six Hats Sequential Analysis

Conduct a rigorous, sequential pass through all six thinking modes. Each hat produces a discrete, documented output section. Explicitly label transitions between hats to maintain parallel thinking discipline — no hat bleeds into another.

### 🔵 Blue Hat — Process & Framing (Facilitator Pass)

Establish the session architecture before substantive analysis begins:
1. **Decision statement**: Restate the decision as a precise, falsifiable proposition (e.g., "We should acquire Company X at a valuation of £Y by Q3 2025")
2. **Scope boundaries**: What is in-scope and explicitly out-of-scope for this analysis
3. **Success criteria**: What would a good decision look like in 12, 24, and 36 months?
4. **Hat sequencing rationale**: Confirm the sequence order (default: Blue → White → Red → Yellow → Black → Green → Blue close) and adapt if user context or FutureProof `instructions` suggest a different order (e.g., leading with Red Hat when emotional resistance is the known blocker)

### ⚪ White Hat — Facts, Data & Information Gaps

Neutral, objective examination of what is known and unknown:
1. **Verified facts**: Extract and list all data points, metrics, and evidence from the provided context — sourced and dated
2. **Assumptions register**: Identify every assumption embedded in the proposal, classify each as *tested*, *testable*, or *untested*
3. **Information gaps**: Catalogue missing data that would materially change the analysis — assign each a criticality rating (Must-Have / Should-Have / Nice-to-Have)
4. **Data quality flags**: Note where figures are estimates, projections, or single-source dependent

Apply any organisation-specific data standards or KPIs from FutureProof `context`.

### 🔴 Red Hat — Intuition, Emotions & Gut Reactions

Surface the unspoken emotional and political dynamics:
1. **Instinctive reactions**: What is the immediate gut response to this proposal? Name it plainly (excitement, dread, suspicion, fatigue)
2. **Stakeholder sentiment map**: For each key stakeholder identified in Step 2, hypothesise their likely emotional posture — enthusiasm, anxiety, territorial defensiveness, indifference
3. **Cultural and political undercurrents**: What organisational history, prior failures, interpersonal dynamics, or power structures might silently shape this decision?
4. **ICA/market sentiment**: How would the organisation's ICA likely *feel* about this move if they learned of it?

No justification required — Red Hat captures feelings without demanding rationale.

### 🟡 Yellow Hat — Benefits, Opportunities & Value

Constructive, optimistic exploration of upside:
1. **Direct value drivers**: Enumerate the tangible benefits — revenue impact, cost reduction, margin expansion, market share gain — with estimated magnitudes where possible
2. **Strategic optionality**: What future doors does this decision open? Second-order opportunities and platform effects
3. **Competitive advantage**: How does this strengthen differentiation, moat, or positioning relative to named competitors?
4. **Stakeholder value**: Benefits to ICA segments, employees, investors, and partners respectively
5. **Best-case scenario**: Describe the realistic upside case with conditions required to achieve it

### ⬛ Black Hat — Risks, Cautions & Critical Judgement

Rigorous, disciplined risk examination — not cynicism, but protective thinking:
1. **Risk register**: Identify strategic, operational, financial, regulatory, reputational, and execution risks — each with likelihood (High/Medium/Low) and impact severity
2. **Failure modes**: What are the three most probable ways this initiative fails? Describe the causal chain for each
3. **Assumption stress-test**: Take the top 5 assumptions from the White Hat pass and invert them — what happens if each is wrong?
4. **Opportunity cost**: What is *not* being done if resources are committed here? Name the specific alternatives foregone
5. **Worst-case scenario**: Describe the realistic downside case and its second-order consequences
6. **Historical analogues**: Reference comparable decisions (internal from FutureProof `recent_sessions` or external industry precedent) that resulted in negative outcomes

### 🟢 Green Hat — Creative Alternatives & Lateral Thinking

Generative, unconstrained ideation:
1. **Alternative framings**: Restate the core problem in at least three fundamentally different ways — challenge the premise itself
2. **Option expansion**: Generate a minimum of 5 alternative approaches, including at least one that is deliberately unconventional or contrarian
3. **Hybrid solutions**: Propose at least 2 combinations that blend elements from the Yellow and Black Hat findings to capture upside while mitigating key risks
4. **Staging and sequencing**: Could this be de-risked through phasing, pilots, partnerships, or reversible first steps?
5. **Provocation**: Apply a de Bono–style provocation (PO) — deliberately introduce an illogical statement to unlock lateral paths (e.g., "PO: What if we gave this product away free to our largest competitor's clients?")

## Step 4: Deliver Output

Produce a structured **Six Hats Decision Brief** containing:

### A. Executive Summary (1 page)
- Decision statement
- Net assessment across all six hats in 3–4 sentences
- Recommended action with confidence level (High / Moderate / Low)

### B. Hat-by-Hat Analysis (detailed)
- Full output from each hat pass as documented in Step 3
- Cross-referenced where findings in one hat directly tension or reinforce another

### C. Decision Matrix
| Dimension | Key Finding | Implication | Action Required |
|-----------|------------|-------------|-----------------|
| Facts (White) | ... | ... | ... |
| Emotions (Red) | ... | ... | ... |
| Benefits (Yellow) | ... | ... | ... |
| Risks (Black) | ... | ... | ... |
| Alternatives (Green) | ... | ... | ... |
| Process (Blue) | ... | ... | ... |

### D. Facilitation Guide (if requested)
- Timed agenda for a 90-minute live Six Hats session with the executive team
- Hat-specific prompting questions tailored to this decision
- Ground rules for parallel thinking discipline (no cross-hat argumentation)
- Suggested hat assignments if running a role-play variant

### E. Recommended Next Steps
- Top 3 actions ranked by impact and urgency
- Information gaps to close before final decision (from White Hat)
- Proposed decision deadline and escalation path

Format the brief for the user's specified audience. Default: C-suite executive memo, PDF-ready, with an appendix containing the full hat-by-hat detail.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="six-hats-perspective-shifter", experiment={
  hypothesis: "Leading with Red Hat before White Hat surfaces hidden blockers earlier and reduces downstream rework in the decision process",
  variants: ["control: standard sequence (White → Red)", "variant: inverted sequence (Red → White)"],
  measurement: "User-reported decision confidence score and number of late-stage objections in next 5 sessions",
  expected_impact: "20% reduction in decision revisits and stakeholder escalations post-session"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="six-hats-perspective-shifter",
  query="Latest applications of de Bono's Six Thinking Hats in corporate governance and board decision-making, including integration with pre-mortem analysis and cognitive bias mitigation frameworks 2023-2025",
  reason="Ensure hat-specific prompts reflect current best practice in structured deliberation and address newly documented cognitive biases in executive decision-making"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="six-hats-perspective-shifter", session={
  summary: "Six Hats analysis of [decision/proposal] for [stakeholder group/organisation]",
  key_findings: ["White Hat: [top information gap]", "Red Hat: [dominant emotional dynamic]", "Black Hat: [highest-severity risk]", "Yellow Hat: [primary value driver]", "Green Hat: [most promising alternative or hybrid]", "Blue Hat: [recommended sequence adjustment for future sessions]"],
  decision_statement: "[precise proposition analysed]",
  recommended_action: "[action and confidence level]",
  user_feedback: null
})
```