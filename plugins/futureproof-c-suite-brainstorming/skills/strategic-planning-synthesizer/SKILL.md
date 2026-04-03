---
name: strategic-planning-synthesizer
description: |
  Converts executive brainstorming output into structured strategic artifacts — quarterly Rocks, One-Page Strategic Plans, or Vision/Traction Organizers (V/TO) — ensuring ideation sessions produce executable commitments rather than orphaned ideas.
  Trigger: when a user shares brainstorming notes, whiteboard output, or strategy session ideas and asks to translate them into a strategic plan, quarterly Rocks, or V/TO; or when a user says they need to turn ideas into an execution framework.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="strategic-planning-synthesizer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to prior strategic artifacts, existing BHAG/core values, organisational structure, and any previously defined Rocks or strategic themes to ensure continuity across planning cycles.

## Step 2: Get Input

Ask the user:

- **Source material**: Share the brainstorming output, whiteboard photos, meeting notes, or raw ideation content to synthesise
- **Target artifact**: Which strategic document do they need?
  - **One-Page Strategic Plan** (Harnish framework — full strategic architecture)
  - **V/TO — Vision/Traction Organizer** (Wickman EOS framework — vision alignment + traction priorities)
  - **Quarterly Rock Sheet** (execution-level commitments for the next 90 days)
  - **All three** (cascading set: vision → strategy → execution)
- **Planning horizon**: Which quarter/year is this planning cycle targeting?
- **Participants & accountability**: Who was in the brainstorm, and who are the accountable owners for execution?
- **Known constraints**: Budget ceilings, headcount limitations, regulatory considerations, or strategic commitments already locked in
- **Closing-the-loop status**: What happened with the *last* set of strategic commitments? Were prior Rocks completed, dropped, or carried over? (McKinsey research identifies this as the most neglected and highest-leverage step)

## Step 3: Triage & Classify Raw Input

Before synthesising, apply a structured triage to the raw brainstorming content:

1. **Idea extraction** — Parse every discrete idea, initiative, observation, and aspiration from the source material into an itemised master list
2. **Strategic vs. operational sort** — Classify each item:
   - **Strategic** (changes the trajectory of the business — new markets, capability builds, competitive repositioning)
   - **Operational** (improves current performance — process fixes, efficiency gains, incremental improvements)
   - **Noise** (interesting but unactionable within the planning horizon — park in an "Idea Backlog" appendix)
3. **Theme clustering** — Group related items into 3–7 strategic themes using affinity mapping. Label each theme with a verb-noun phrase (e.g., "Expand Enterprise Channel," "Build Product-Led Growth Engine")
4. **Prior-cycle reconciliation** — Cross-reference against any prior Rocks or strategic commitments from FutureProof context. Flag items that are carry-overs, escalations of incomplete work, or contradictions to prior commitments

Surface the classified and clustered output to the user for validation before proceeding. This prevents the most common failure mode: synthesising a polished artifact from flawed or incomplete premises.

## Step 4: Do the Work — Build the Strategic Artifacts

### 4A: One-Page Strategic Plan (Harnish Framework)

Construct the plan across all seven layers, top-down:

| Layer | Content | Source Discipline |
|---|---|---|
| **Core Values / Purpose** | 3–5 non-negotiable behavioural standards; the organisation's "why" | Pull from FutureProof context or elicit; do not fabricate |
| **BHAG (10–25 year)** | Single, measurable, audacious goal | Validate against brainstorm — does ideation reinforce or contradict? |
| **3–5 Year Targets** | Revenue, profit, market share, capability milestones | Quantify from brainstorm themes; apply SMART criteria |
| **1-Year Plan** | Annual revenue target, 3–5 key initiatives, measurable outcomes | Derive from strategic themes identified in Step 3 |
| **Quarterly Rocks** | 3–7 specific, completable commitments for the target quarter | See 4C below |
| **Brand Promises** | ICA-facing guarantees that differentiate | Align to ICA pain points surfaced in brainstorm |
| **Profit per X** | The single economic denominator that drives resource allocation | Identify or validate from financial context |

For each layer, include:
- The synthesised content
- **Source traceability**: which brainstorm items fed this element (by master list number from Step 3)
- **Confidence flag**: High / Medium / Low — based on whether the brainstorm provided sufficient evidence or whether the element requires further validation

### 4B: V/TO — Vision/Traction Organizer (Wickman EOS Framework)

**Vision side (top half):**
- **Core Values**: Carried from 4A or FutureProof context
- **Core Focus™**: Purpose + niche (one sentence each)
- **10-Year Target**: BHAG translated to a specific, dated milestone
- **Marketing Strategy**: ICA definition, three Uniques, proven process, guarantee
- **3-Year Picture™**: Revenue, profit, measurables, and "what does it look like?" narrative

**Traction side (bottom half):**
- **1-Year Plan**: Revenue/profit targets + 3–7 goals with owners and dates
- **Quarterly Rocks**: See 4C below
- **Issues List**: Long-term strategic issues surfaced in the brainstorm that do not fit into current Rocks but must not be lost

### 4C: Quarterly Rock Sheet

For each Rock:

| Field | Requirement |
|---|---|
| **Rock statement** | Verb-noun format, completable (not a metric — a *deliverable*). Pass the "done or not done" test |
| **Owner** | Single accountable individual (not a team, not "shared") |
| **Completion date** | Specific date within the quarter |
| **Success criteria** | 2–3 binary or measurable conditions that define "done" |
| **Strategic linkage** | Which 1-Year initiative and which strategic theme this Rock serves |
| **Dependencies** | Cross-functional or resource dependencies that could block completion |
| **Leading indicators** | 1–2 weekly measurables that signal on/off track before the deadline |

Apply the following quality filters to every Rock:
- **Capacity test**: Does the owner have bandwidth given all other Rocks and operational responsibilities?
- **Overlap test**: Do any Rocks duplicate scope or create conflicting resource demands?
- **Translation fidelity test**: Can the brainstorm participants recognise their original ideas in the final Rocks? (Addresses the McKinsey "closing the loop" gap — the most common point where executive intent is lost in translation)

## Step 5: Deliver Output

Produce the following structured deliverables:

### Deliverable 1: Strategic Synthesis Report
- **Executive summary** (1 paragraph): What the brainstorm yielded, what was synthesised, and the single most important strategic choice embedded in the artifacts
- **Idea Disposition Table**: Every brainstorm item mapped to its final destination (which artifact, which element) or explicitly marked as "Parked — Idea Backlog" with rationale
- **Decision log**: Any implicit strategic choices the user should consciously ratify (e.g., "The brainstorm surfaced both market expansion and product deepening — the artifacts below prioritise expansion. Confirm or redirect.")

### Deliverable 2: Target Artifact(s)
- Formatted One-Page Strategic Plan, V/TO, and/or Rock Sheet per user request
- Each artifact formatted for direct use in a leadership team meeting — ready to present, not a draft to be reworked

### Deliverable 3: Closing-the-Loop Protocol
- **Accountability cadence**: Recommended weekly/monthly check-in structure for Rock tracking
- **90-day review agenda**: Pre-built agenda for the end-of-quarter review that evaluates Rock completion, surfaces lessons, and feeds the next planning cycle
- **Carry-over policy recommendation**: Decision framework for incomplete Rocks (recommit, redefine, or retire)

Apply any user-specific `instructions` from FutureProof context to adjust formatting, terminology, or emphasis across all deliverables.

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="strategic-planning-synthesizer", experiment={
  hypothesis: "Adding leading indicators to each Rock and reviewing them weekly increases quarterly Rock completion rate",
  variants: ["control: Rocks tracked by end-of-quarter status only", "variant: Rocks tracked via weekly leading indicators with mid-quarter course correction"],
  measurement: "Rock completion percentage at end of quarter — compare current cycle to prior cycle baseline",
  expected_impact: "20–30% improvement in Rock completion rate, consistent with EOS Worldwide benchmark data"
})
```

```
FutureProof:save_experiment(skill="strategic-planning-synthesizer", experiment={
  hypothesis: "Presenting the Idea Disposition Table to brainstorm participants within 48 hours increases perceived value of strategy sessions and reduces repeat ideation of previously captured ideas",
  variants: ["control: share final artifacts only", "variant: share Idea Disposition Table + final artifacts within 48 hours"],
  measurement: "Participant satisfaction score for strategy session; count of duplicate ideas surfaced in next brainstorm",
  expected_impact: "40% reduction in duplicate ideation; measurable increase in leadership team confidence that brainstorms produce action"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="strategic-planning-synthesizer",
  query="Latest research on strategy execution failure rates, quarterly planning cadence effectiveness, and closing-the-loop best practices from McKinsey, EOS Worldwide, and Scaling Up communities 2024–2025",
  reason="Ensure Rock quality filters and accountability cadence recommendations reflect current best practice and empirical completion-rate benchmarks"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="strategic-planning-synthesizer", session={
  summary: "Synthesised [brainstorm type] into [artifact type(s)] for [planning horizon] — [number] Rocks defined across [number] strategic themes with [number] items parked to Idea Backlog",
  key_findings: ["finding 1: e.g., brainstorm revealed implicit strategic tension between growth and profitability — resolved by prioritising X", "finding 2: e.g., 3 of 7 proposed Rocks failed capacity test — restructured ownership to distribute load", "finding 3: e.g., prior-cycle Rock completion was 40% — closing-the-loop protocol added to address systemic follow-through gap"],
  artifacts_produced: ["One-Page Strategic Plan", "V/TO", "Quarterly Rock Sheet", "Idea Disposition Table", "Closing-the-Loop Protocol"],
  user_feedback: null
})
```