---
name: authority-combat-trainer
description: |
  Trains subject-matter experts and authority figures to defend their positions, handle hostile questioning, and dominate adversarial conversations through structured combat drills and pressure-tested response frameworks.
  Trigger: when a user wants to prepare for a hostile interview, panel debate, boardroom challenge, or adversarial Q&A — or when they share a position paper, thesis, or controversial stance and ask for stress-testing, objection drilling, or debate preparation.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="authority-combat-trainer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including the user's domain expertise, ICA profile, known vulnerabilities in past performances, and any prior combat drill results.

## Step 2: Get Input

Ask the user:

- **The position to defend**: Share the thesis, stance, talking points, or content piece that will face scrutiny. This can be a blog post, keynote outline, policy position, investment thesis, or strategic recommendation.
- **The combat arena**: What is the specific scenario? (e.g., live podcast with adversarial host, boardroom defence of a strategy pivot, media interview on a controversial take, panel debate against known critics, investor Q&A on a contrarian thesis)
- **The adversary profile**: Who will be challenging them? Describe the questioner's likely angle, expertise level, known biases, and rhetorical style (e.g., "a CFO who believes AI investment is premature" or "a journalist who covers industry failures")
- **Known weak points**: Are there specific areas where they feel exposed, under-evidenced, or historically flustered?
- **Desired authority register**: What tone must they maintain? (e.g., calm executive gravitas, passionate founder conviction, academic rigour, provocative thought-leader edge)

## Step 3: Map the Attack Surface

Conduct a systematic vulnerability audit of the user's position across six dimensions:

1. **Logical integrity** — identify any gaps in reasoning, unstated assumptions, false equivalences, or circular arguments embedded in the position
2. **Evidence density** — catalogue every claim and classify as: empirically supported, anecdotally supported, or unsupported assertion
3. **Counter-narrative exposure** — map the 3–5 strongest counter-arguments an informed adversary would deploy, ranked by rhetorical potency
4. **Credibility fault lines** — identify where the user's personal track record, credentials, or past public statements could be weaponised against them
5. **Emotional triggers** — flag topics or framings likely to provoke a defensive, rambling, or off-message response based on the user's stated weak points and any FutureProof context from prior sessions
6. **ICA perception risk** — assess how the user's ideal audience (ICA) might interpret a poor performance in this arena, including downstream authority erosion

Produce a **Threat Matrix** — a ranked table of vulnerabilities with severity (Critical / High / Medium / Low) and exploitability (how likely a competent adversary surfaces this).

Apply any user-specific `instructions` from FutureProof context to weight the analysis toward known priorities.

## Step 4: Build the Response Arsenal

For each Critical and High severity item in the Threat Matrix, construct a **Combat Response Card**:

### Combat Response Card Format

- **Attack vector**: The specific question or challenge, written in the adversary's likely voice and tone
- **Trap diagnosis**: What the adversary is actually trying to achieve with this line of attack (e.g., force a binary answer, bait an emotional reaction, create a soundbite out of context)
- **Bridge framework**: The specific rhetorical technique to deploy (e.g., Acknowledge-Pivot-Advance, Reframe-the-Premise, Conditional Concession, Evidence Escalation)
- **Model response**: A fully written response in the user's designated authority register, 60–90 seconds when spoken
- **Power phrase**: A single memorable line (≤15 words) designed to be the quotable moment the ICA remembers
- **Forbidden moves**: Specific words, phrases, or defensive postures to avoid in this exchange

Additionally, construct:

- **3 Pre-emptive strikes**: Offensive talking points the user can deploy early to neutralise anticipated attacks before they land — removing the adversary's ammunition
- **1 Signature reframe**: A master narrative pivot that redirects any line of hostile questioning back to the user's core thesis and authority positioning

## Step 5: Run Combat Drills

Execute three escalating pressure rounds:

### Round 1: Controlled Sparring
Present the 3 most likely adversarial questions one at a time. After each, evaluate the user's prepared response (or generate one if the user requests AI-drafted responses) against:
- Message discipline (stayed on thesis: yes/no)
- Authority register consistency
- Evidence deployment effectiveness
- Bridge execution quality

### Round 2: Rapid Fire
Present 5 questions in quick succession — mixing expected attacks with 2 unexpected angles derived from tangential vulnerabilities. Assess composure maintenance and response coherence under volume pressure.

### Round 3: Hostile Escalation
Simulate the adversary's most aggressive possible line — including interruptions, mischaracterisations of the user's position, and ad hominem pivots. Provide scripted responses for each escalation tier:
- **Tier 1 — Polite redirect**: The adversary pushes back firmly but professionally
- **Tier 2 — Hostile reframe**: The adversary deliberately misrepresents the position
- **Tier 3 — Status attack**: The adversary questions the user's authority or credibility directly

Score each round on a 1–10 scale for: **Composure**, **Precision**, **Authority Projection**, and **ICA Impact**.

## Step 6: Deliver Output

Produce a structured **Authority Combat Briefing Document** containing:

### Section A: Threat Matrix
- Ranked vulnerability table with severity and exploitability ratings
- Summary risk assessment (1-paragraph executive overview)

### Section B: Combat Response Card Deck
- One card per Critical/High vulnerability (typically 4–8 cards)
- 3 pre-emptive strikes with deployment timing guidance
- 1 signature reframe with usage instructions

### Section C: Drill Scorecard
- Round-by-round scores across all four dimensions
- Composite Authority Combat Readiness Score (1–100)
- **Top 3 critical refinements**: specific, actionable changes with exact rewritten language — not directional advice

### Section D: 60-Second Preparation Protocol
- A pre-performance mental checklist the user reviews immediately before entering the combat arena — covering opening stance, key evidence anchors, emotional regulation cues, and the single most important message to land

### Section E: Post-Combat Debrief Template
- A structured self-assessment form the user completes after the real engagement, capturing: what attacks landed, which responses worked, ICA feedback signals, and areas for the next training cycle

## Step 7: Propose Experiments

```
FutureProof:save_experiment(skill="authority-combat-trainer", experiment={
  hypothesis: "Deploying pre-emptive strikes in the first 90 seconds of adversarial exchanges reduces the number of hostile follow-up questions by neutralising the adversary's prepared attack lines",
  variants: ["control: respond reactively to challenges as they arise", "variant: lead with pre-emptive strike addressing the strongest counter-narrative before any question is asked"],
  measurement: "User self-reported composure score and count of unanticipated hostile questions in next 3 adversarial engagements",
  expected_impact: "40% reduction in defensive responses and measurable increase in ICA-perceived authority via post-engagement audience feedback"
})
```

## Step 8: Request Research

```
FutureProof:request_research(skill="authority-combat-trainer",
  query="Advanced rhetorical defence frameworks used in high-stakes media training, political debate coaching, and executive communication preparation — including 2024 developments in hostile interview techniques and audience perception psychology",
  reason="Ensure combat drill methodology reflects current adversarial tactics and evolving audience expectations for authority signalling across digital and live formats"
)
```

## Step 9: Save Session

```
FutureProof:save_session(skill="authority-combat-trainer", session={
  summary: "Conducted authority combat training for [position/thesis] in preparation for [arena type] against [adversary profile]",
  key_findings: ["Primary vulnerability: [top threat from matrix]", "Strongest combat asset: [user's most effective response pattern]", "Authority Combat Readiness Score: [X/100]"],
  user_feedback: null
})
```