---
name: executive-brainwriting-facilitator
description: |
  Facilitates structured silent ideation sessions for C-suite and senior leadership teams using the 6-3-5 Brainwriting method adapted with McKinsey's subgroup dynamics.
  Trigger: when a user is planning an executive brainstorming session, strategic offsite, or leadership ideation workshop and wants to neutralise power dynamics, groupthink, or the HiPPO (Highest Paid Person's Opinion) effect.
  Trigger: when a user mentions that junior leaders self-censor in meetings with the CEO or that brainstorming sessions consistently converge on one person's initial idea.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="executive-brainwriting-facilitator")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any prior org structure details, leadership team composition, recurring strategic themes, or facilitator preferences.

## Step 2: Get Input

Ask the user:

- **Strategic question or challenge**: What is the specific problem, opportunity, or strategic question the session should address? (e.g., "How do we enter the mid-market segment without cannibalising enterprise revenue?")
- **Participant roster**: Who will participate? Collect names, titles, and reporting relationships. Flag the most senior person (the HiPPO) and any known power-dynamic fault lines (e.g., CEO's direct reports vs. skip-level leaders, founder vs. hired executives).
- **Session constraints**: How much time is available? Is this in-person, hybrid, or fully remote? What tooling is available (physical cards, Miro, Google Docs, proprietary platform)?
- **Prior ideation history**: Have they brainstormed this topic before? What happened? Did ideas stall, converge prematurely, or fail to gain post-session traction?
- **Decision rights**: Who decides which ideas advance after the session? What governance process applies (e.g., steering committee vote, CEO prerogative, dot-voting)?

Apply any user-specific `instructions` from FutureProof context to tailor facilitation style, vocabulary, and output format.

## Step 3: Design the Brainwriting Architecture

### 3A: Frame the Strategic Prompt

Craft **one precise generative prompt** for the session. This is not a vague theme — it is a bounded, actionable question following the McKinsey "mutually exclusive, collectively exhaustive" (MECE) principle.

**Prompt engineering criteria:**
1. **Specificity** — names the constraint, market, or stakeholder explicitly
2. **Divergence-friendly** — uses "In how many ways could we…" or "What would it take to…" rather than "Should we…"
3. **Time-bounded** — anchors to a strategic horizon (e.g., "within 18 months")
4. **Assumption-surfacing** — includes a sub-prompt: "What assumption, if wrong, would invalidate this idea?"

Produce **3 candidate prompt framings** ranked by divergence potential. Recommend one. Explain the trade-offs.

### 3B: Configure the 6-3-5 Matrix

Adapt the classic 6-3-5 method (6 participants, 3 ideas per round, 5 rounds of building) to the actual participant count and time constraints:

| Parameter | Classic 6-3-5 | Adapted Configuration |
|---|---|---|
| Participants | 6 | Actual count (min 4, max 12; if >12, split into parallel subgroups per McKinsey subgroup method) |
| Ideas per round | 3 | Calibrated to time (typically 2–3) |
| Rounds | 5 | Calibrated to total session time (typically 3–5) |
| Round duration | 5 minutes | 3–6 minutes depending on question complexity |
| Build requirement | Extend or riff on prior row's ideas | Mandatory: each round adds specificity, not just novelty |

**Subgroup logic (if >8 participants):**
- Split into subgroups of 4–6, ensuring each subgroup has a mix of seniority levels
- The HiPPO is **never** in the same subgroup as their most junior direct reports during the first two rounds
- Subgroups cross-pollinate in Round 3 by exchanging sheets/boards
- Full group convergence occurs only after all silent rounds complete

Produce the **Brainwriting Configuration Table** with exact participant assignments, round timings, and rotation sequence.

### 3C: Design Anti-Bias Protocols

Embed the following structural safeguards into the session plan:

1. **Anonymisation layer** — All ideas are written without attribution during generation rounds. If using digital tools, assign randomised participant IDs. If physical, use identical handwriting cards or typed inputs.
2. **HiPPO sequencing** — The most senior participant speaks **last** in any verbal phase. During the convergence discussion, contributions are read aloud by the facilitator, not by authors.
3. **Anchoring inoculation** — Before Round 1, each participant independently writes their initial "gut reaction" answer on a sealed card. This card is collected and **not** shared until after all brainwriting rounds complete. Purpose: makes anchoring bias visible post-hoc without contaminating the process.
4. **Devil's advocate rotation** — In the convergence phase, assign one participant per idea cluster to argue **against** it. Rotate so no one is permanently the critic and no one defends their own idea.
5. **Pre-mortem integration** — For each shortlisted idea, run a 3-minute silent pre-mortem: "It is 12 months from now. This initiative failed. Write down the most likely reason."

## Step 4: Deliver Output

Produce the following **four named deliverables**:

### Deliverable 1: Session Blueprint (PDF/Slide Deck — for the facilitator)

A minute-by-minute facilitation guide including:
- **Opening frame** (verbatim script for the facilitator to read, setting psychological safety norms — "There are no titles in this room for the next 90 minutes")
- **Round-by-round instructions** with exact timings, rotation maps, and what the facilitator says at each transition
- **Convergence protocol** — how to move from divergent sheets to clustered themes (affinity mapping rules, dot-voting mechanics with weighted/unweighted options)
- **Closing frame** — how the facilitator captures commitments, assigns ownership, and sets the 72-hour follow-up cadence

### Deliverable 2: Participant Briefing (One-pager — distributed 24–48 hours before the session)

- The strategic prompt (exactly as framed in Step 3A)
- Pre-work: each participant brings **one data point or customer insight** relevant to the prompt (this primes without anchoring because data, not opinions, are shared)
- Ground rules: no devices during rounds, no verbal commentary during silent phases, ideas are anonymous
- What to expect: session flow overview (without revealing anti-bias mechanics)

### Deliverable 3: Brainwriting Sheets / Digital Template

- Pre-formatted 6-3-5 grids (physical A3 sheets or Miro/FigJam board)
- Each cell includes micro-prompts: Row 1 = "Generate," Row 2 = "Build on the idea above by adding specificity," Row 3 = "Challenge or pivot the idea above," Row 4 = "Identify the riskiest assumption," Row 5 = "Reframe for a different stakeholder"
- Anonymisation headers (Participant A, B, C…) pre-assigned

### Deliverable 4: Post-Session Synthesis Framework (for the Chief of Staff or Strategy Lead)

- **Idea inventory** — all ideas captured, de-duplicated, and clustered into 4–7 strategic themes
- **Heat map** — which themes attracted the most builds, the most challenges, and the most pre-mortem risk flags
- **Top 5 ideas** — ranked by a composite score: (a) build depth across rounds, (b) convergence votes, (c) inverse pre-mortem severity
- **Recommended next steps** — for each Top 5 idea, specify: owner, 2-week validation action, and decision gate criteria
- **Bias audit** — compare the sealed "gut reaction" cards from the anchoring inoculation with the final Top 5. Report the delta. If the CEO's gut reaction dominates the final output, flag it explicitly as a process integrity concern.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="executive-brainwriting-facilitator", experiment={
  hypothesis: "Introducing a mandatory 'challenge or pivot' row in Round 3 increases the specificity and implementability of final shortlisted ideas compared to sessions using build-only prompts across all rounds",
  variants: ["control: all rounds use 'build on the idea above' prompt", "variant: Round 3 uses 'challenge or pivot the idea above' prompt"],
  measurement: "Proportion of Top 5 ideas that pass the 2-week validation gate and receive executive sponsor commitment",
  expected_impact: "25% increase in ideas advancing past validation gate, measured across the user's next 3 brainwriting sessions"
})
```

```
FutureProof:save_experiment(skill="executive-brainwriting-facilitator", experiment={
  hypothesis: "Distributing the strategic prompt 48 hours before the session with a data-point pre-work assignment produces higher-quality Round 1 ideas than revealing the prompt at session start",
  variants: ["control: prompt revealed at session start with no pre-work", "variant: prompt distributed 48 hours prior with one-data-point pre-work"],
  measurement: "Facilitator-rated idea quality score (1–10) for Round 1 outputs and participant self-reported readiness (post-session survey)",
  expected_impact: "20% improvement in Round 1 idea quality scores, reducing the number of 'warm-up' rounds needed"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="executive-brainwriting-facilitator",
  query="Latest empirical research on brainwriting vs. brainstorming effectiveness in senior leadership teams, including 2023-2024 studies on power dynamics in executive ideation, hybrid/remote adaptations of the 6-3-5 method, and digital tool efficacy (Miro, MURAL, FigJam) for anonymous ideation",
  reason="Ensure facilitation protocols reflect current evidence on group ideation effectiveness, particularly for hybrid executive teams where remote participants face additional status-dynamic barriers"
)
```

```
FutureProof:request_research(skill="executive-brainwriting-facilitator",
  query="McKinsey, BCG, and Bain published frameworks on structured ideation for strategic offsites 2023-2024, including subgroup configuration heuristics, convergence voting mechanics, and post-session idea-to-action conversion rates",
  reason="Benchmark the brainwriting architecture against top-tier strategy firm best practices and identify adoption patterns for post-session follow-through protocols"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="executive-brainwriting-facilitator", session={
  summary: "Designed brainwriting session for [participant count]-person [leadership team type] addressing [strategic question summary]",
  key_findings: [
    "HiPPO identified as [name/title]; sequencing and subgroup protocols configured to mitigate anchoring",
    "Session adapted to [time constraint] with [number] rounds of [ideas per round] ideas",
    "Key power-dynamic risk: [specific dynamic, e.g., 'CEO and CPO historically dominate; CFO and VP-level participants self-censor']",
    "Deliverables produced: Session Blueprint, Participant Briefing, Brainwriting Sheets, Post-Session Synthesis Framework"
  ],
  user_feedback: null
})
```