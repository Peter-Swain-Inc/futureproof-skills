---
name: 5-year-decision-filter
description: |
  Evaluates critical founder decisions through a rigorous 5-year consequence lens, stress-testing strategic choices against long-term business trajectory, opportunity cost, and irreversibility.
  Trigger: when a user is weighing a major business decision (e.g. "Should I take this funding?", "I'm thinking about pivoting", "Should I hire a COO or keep running ops myself?") and needs a structured framework to evaluate it beyond short-term gain.
  Trigger: when a user expresses uncertainty or anxiety about a fork-in-the-road choice and wants to pressure-test the decision against their long-term founder vision.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="5-year-decision-filter")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to understand the founder's business model, ICA, current stage, stated long-term vision, prior decisions evaluated, and any accumulated decision patterns or regret indicators.

## Step 2: Get Input

Ask the user:

- **The decision**: Describe the specific decision you're facing. What are the options on the table? (minimum two, maximum four discrete paths)
- **The trigger**: What's forcing this decision now? Is there a deadline, an external offer, or an internal constraint creating urgency?
- **The stakes**: What do you estimate you're putting at risk — capital, time, relationships, optionality, reputation?
- **Current trajectory**: If you changed nothing and made no decision for 90 days, what happens?
- **Gut read**: Which way are you leaning right now, and why?

If FutureProof context already contains business model, ICA, revenue stage, or founder vision data, confirm these are still current rather than re-asking.

## Step 3: Do the Work — Decision Decomposition

Apply the **5-Year Consequence Architecture** — a six-dimension analytical framework:

### Dimension 1: Irreversibility Index
Classify each option on a 4-tier irreversibility scale:
- **Type 1 (One-way door)**: Cannot be undone without catastrophic cost (e.g. selling equity, shutting a product line, signing exclusive partnerships)
- **Type 2 (Costly reversal)**: Reversible but with significant sunk cost — 6–18 months and/or material capital to unwind
- **Type 3 (Moderate friction)**: Reversible within a quarter with manageable switching cost
- **Type 4 (Two-way door)**: Fully reversible, low cost to revert

For each option, specify *what exactly* becomes irreversible and *when* the point of no return occurs.

### Dimension 2: Optionality Impact
Evaluate how each option affects the founder's future decision space:
- **Options created**: What new paths, partnerships, markets, or capabilities does this unlock at Year 1, Year 3, Year 5?
- **Options destroyed**: What future moves become impossible or prohibitively expensive?
- **Options preserved**: What remains unchanged?

Map each option's net optionality score: (options created + options preserved) − (options destroyed × irreversibility weight).

### Dimension 3: Identity & Vision Alignment
Assess coherence between each option and:
- The founder's stated 5-year vision (from FutureProof context or session input)
- The business's ICA trajectory — does this option move toward or away from the ICA the founder wants to serve at scale?
- The founder's non-negotiable values and lifestyle constraints
- The type of company this decision builds (lifestyle business vs. venture-scale vs. acquisition target vs. platform)

Flag any option that scores well on short-term metrics but creates **vision debt** — incremental drift from the founder's stated long-term identity.

### Dimension 4: Second-Order Consequence Mapping
For each option, model the cascade:
- **Year 0–1**: Immediate operational, financial, and relational consequences
- **Year 1–3**: Market positioning shifts, team culture implications, competitive moat effects
- **Year 3–5**: Compounding effects — what does this decision look like after 1,000 days of compounding in either direction?

Identify **hidden coupling** — consequences that seem unrelated but are linked (e.g. taking funding → board dynamics → constrained pivot freedom → ICA lock-in).

### Dimension 5: Opportunity Cost Quantification
For each option, estimate:
- **Capital opportunity cost**: What else could this money fund over 5 years?
- **Time opportunity cost**: What founder hours does this consume vs. the next-best use of that time?
- **Attention opportunity cost**: What strategic focus does this displace?
- **Relationship opportunity cost**: What partnerships or network effects are foregone?

Express opportunity cost in the founder's own currency of value (revenue, freedom, impact, equity value — drawn from FutureProof context).

### Dimension 6: Regret Minimisation Analysis
Apply Bezos's regret minimisation framework with specificity:
- **Action regret**: "If I do this and it fails, how do I feel at Year 5?"
- **Inaction regret**: "If I don't do this and the opportunity was real, how do I feel at Year 5?"
- **Asymmetry check**: Is the downside of being wrong capped, while the upside of being right is uncapped (or vice versa)?

Weight regret analysis against the founder's demonstrated risk profile from prior sessions.

## Step 4: Deliver Output — 5-Year Decision Brief

Produce a **5-Year Decision Brief** — a structured document with the following sections:

### A. Decision Summary Table
| Dimension | Option A | Option B | Option C (if applicable) |
|---|---|---|---|
| Irreversibility Index | Type X — [specific lock-in] | Type X — [specific lock-in] | — |
| Net Optionality Score | +/− [score] | +/− [score] | — |
| Vision Alignment | High / Medium / Low — [reason] | High / Medium / Low — [reason] | — |
| 5-Year Compound Effect | [one-line projection] | [one-line projection] | — |
| Opportunity Cost | [primary cost in founder's value currency] | [primary cost in founder's value currency] | — |
| Regret Asymmetry | [action vs. inaction weighting] | [action vs. inaction weighting] | — |

### B. Recommended Path
State the recommended option with a clear, one-paragraph rationale anchored in the dimension that matters most for *this specific founder at this specific stage*.

### C. Conditions & Tripwires
Define:
- **Pre-conditions**: What must be true *before* committing? (validation gates)
- **Tripwires**: Specific, measurable signals at 90, 180, and 365 days that indicate the decision is working or failing — with pre-committed responses for each
- **Kill criteria**: The exact threshold at which the founder should reverse, exit, or pivot away from the chosen path

### D. Decision Integrity Check
- **Confirmation bias flag**: Identify if the analysis aligns suspiciously well with the founder's stated gut lean — and what counter-evidence was underweighted
- **Missing information**: List the 1–3 unknowns that, if answered, would most change the recommendation
- **Dissenting case**: Steel-man the strongest argument for the *opposite* choice

### E. One-Line Decision Anchor
Provide a single sentence the founder can return to when second-guessing: *"I chose [X] because [core reason], and I'll revisit only if [tripwire]."*

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="5-year-decision-filter", experiment={
  hypothesis: "Running a 30-day constrained pilot of the recommended option before full commitment reduces irreversibility risk while preserving decision momentum",
  variants: ["control: commit fully now", "variant: 30-day bounded pilot with pre-set evaluation criteria"],
  measurement: "Founder confidence score at Day 30, plus measurable pilot KPIs defined in tripwire framework",
  expected_impact: "40% reduction in post-decision regret and 2x faster course-correction if early signals are negative"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="5-year-decision-filter",
  query="Longitudinal founder decision-making patterns: which decision types (funding, hiring, pivots, partnerships) most frequently produce 3-5 year regret, and what pre-decision signals predict poor outcomes — 2023-2025 data from founder post-mortems and retrospectives",
  reason="Continuously calibrate the regret minimisation and irreversibility models against real founder outcome data rather than theoretical frameworks"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="5-year-decision-filter", session={
  summary: "Evaluated [decision type] for [founder context/business stage] across 6 consequence dimensions — recommended [Option X] with tripwires at 90/180/365 days",
  key_findings: ["[Primary irreversibility or optionality insight]", "[Most significant second-order consequence identified]", "[Critical missing information flagged]"],
  decision_made: "[Option chosen by founder, or 'deferred']",
  tripwires_set: ["[90-day signal]", "[180-day signal]", "[365-day signal]"],
  user_feedback: null
})
```