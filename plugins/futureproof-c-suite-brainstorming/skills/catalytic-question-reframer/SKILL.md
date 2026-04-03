---
name: catalytic-question-reframer
description: |
  Guides executives through Hal Gregersen's Question Burst™ methodology to reframe challenges and unlock breakthrough thinking.
  Trigger: when a user describes a strategic challenge, feels stuck on a problem, or says they need to "think differently" about an issue before jumping to solutions. Also activates when a user asks for help brainstorming but hasn't yet clarified the right question to solve.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="catalytic-question-reframer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to:
- The user's industry, role, and strategic priorities
- Previous challenges they've reframed (to avoid retreading and to identify recurring constraint patterns)
- Any `instructions` specifying preferred frameworks, decision-making style, or team dynamics

## Step 2: Get Input — Define the Challenge Seed

Ask the user:
- **State your challenge in 1–2 sentences.** Not a question — a plain description of what you're stuck on, struggling with, or trying to figure out. (e.g., "We can't retain enterprise clients past the first renewal cycle.")
- **Why does this matter now?** What's the cost of inaction over the next 90 days — revenue, strategic position, team capacity, or opportunity cost?
- **What solutions have you already considered or attempted?** (This surfaces existing assumptions to deliberately challenge later.)
- **Who else is affected by or has a stake in this challenge?** (Identifies perspective lenses for the Question Burst.)

Confirm the challenge seed back to the user in their exact language. Do not reframe it yet — premature reframing defeats the methodology.

## Step 3: Do the Work — Execute the Question Burst™ Protocol

Facilitate a structured Question Burst™ in three rigorous phases:

### Phase 1: Rules of Engagement (60 seconds)

Brief the user on the four non-negotiable rules:
1. **Questions only.** No answers, no justifications, no preambles. If a statement creeps in, flag it and redirect.
2. **No preambles or context on questions.** Just the question itself — raw, unpolished.
3. **Record every question exactly as stated.** No editing, no filtering, no quality judgement during generation.
4. **Aim for 15+ questions in 4 minutes.** Quantity precedes quality. Breakthroughs cluster in questions 12–20 (Gregersen's research from MIT Leadership Center).

### Phase 2: Generative Sprint — Question Burst (4-minute equivalent)

Generate questions across six deliberate perspective lenses, producing a minimum of 15 questions total. Rotate through the lenses to prevent clustering in comfortable territory:

1. **Assumption Inversion** — What if the opposite of your core assumption were true?
   - e.g., "What if clients aren't leaving because of our product — what if they're leaving because of what happens *between* touchpoints?"

2. **Stakeholder Perspective Shift** — How would [affected party] describe this problem?
   - Use the stakeholders identified in Step 2 to generate questions from their vantage point.

3. **Temporal Reframe** — What would this look like at 10x scale, in 5 years, or if it had to be solved by Friday?
   - Compress and expand time horizons to surface urgency-driven and vision-driven questions.

4. **Constraint Removal** — What if [resource/rule/norm] didn't exist?
   - Systematically remove budget, headcount, regulatory, political, and technical constraints one at a time.

5. **Adjacent Domain Analogy** — How has an entirely different industry solved an isomorphic problem?
   - Draw from the user's `context` to select analogies from industries they respect or follow.

6. **Root Cause Escalation** — Why does this problem exist in the first place? And why does *that* exist?
   - Apply a minimum of three layers of "why" to push past symptomatic framing.

Present all 15+ questions in a numbered list, unedited, preserving the raw generative energy. Tag each question with its perspective lens in brackets.

### Phase 3: Convergence — Surface the Catalytic Question

Apply Gregersen's convergence criteria to identify the 3–5 most catalytic questions:

| Criterion | Definition |
|---|---|
| **Discomfort Signal** | The question produces a visceral "I don't want to answer that" reaction — this indicates proximity to a real constraint |
| **Assumption Exposure** | The question makes a previously invisible assumption visible and challengeable |
| **Reframe Power** | Answering this question would change the *type* of solution you pursue, not just optimise within the current frame |
| **Actionability** | The question can be investigated — it points to data, conversations, or experiments, not abstract philosophy |
| **Novel Territory** | The question has not been asked in prior sessions or strategy discussions (cross-reference `recent_sessions`) |

Score each of the 15+ questions against these five criteria (High / Medium / Low). Surface the top 3–5 scorers as **Catalytic Question Candidates**.

From these candidates, identify the single **Primary Catalytic Question (PCQ)** — the one question that, if answered well, would make the original challenge seed obsolete or fundamentally reframe it.

## Step 4: Deliver Output — The Catalytic Question Brief

Produce a structured **Catalytic Question Brief** document:

### Section A: Challenge Seed (Original Framing)
- User's original 1–2 sentence challenge, verbatim
- Stated cost of inaction
- Pre-existing solutions considered (assumptions embedded)

### Section B: Question Burst Record
- Complete numbered list of all 15+ questions with perspective lens tags
- Notation of which questions produced visible discomfort or surprise

### Section C: Convergence Analysis
- Scoring matrix of top 5 candidates against the five convergence criteria
- Rationale for each High score (one sentence per cell)

### Section D: Primary Catalytic Question (PCQ)
- The PCQ, stated clearly and precisely
- **Reframe narrative**: 2–3 sentences explaining how this question shifts the problem from the original frame to a more generative frame
- **Why this unlocks**: What category of solution becomes visible that was invisible under the original framing

### Section E: Activation Pathways
For the PCQ, provide three concrete next steps:
1. **Data to gather** — What specific information would begin answering this question? Name sources, stakeholders to interview, metrics to pull.
2. **Conversation to have** — Who should be asked this question first, and in what setting? (1:1, leadership offsite, board session, ICA advisory panel)
3. **72-hour micro-experiment** — One low-cost action the user can take within 72 hours to begin stress-testing the reframe.

### Section F: Secondary Questions to Hold
- List the remaining 2–4 high-scoring candidates as "questions to revisit" after the PCQ has been explored — these often become relevant once the first reframe produces new information.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="catalytic-question-reframer", experiment={
  hypothesis: "Pursuing the PCQ reframe shifts the user's strategic approach from [original solution category] to [new solution category], producing a measurably different action plan",
  variants: ["control: continue with original challenge framing and existing solution set", "variant: use PCQ as the organising question for next strategy session or decision"],
  measurement: "User self-report at 2-week follow-up — did the PCQ reframe change the solution set pursued? Did it surface at least one option not previously considered?",
  expected_impact: "80% likelihood of producing at least one novel strategic option not present under original framing (aligned with Gregersen's research outcomes)"
})
```

```
FutureProof:save_experiment(skill="catalytic-question-reframer", experiment={
  hypothesis: "Questions generated from the Constraint Removal and Assumption Inversion lenses score highest on Reframe Power consistently across sessions",
  variants: ["Track lens-of-origin for all PCQs selected across multiple sessions"],
  measurement: "Lens distribution of PCQs over next 10 sessions",
  expected_impact: "Identifies which perspective lenses to prioritise earlier in the sprint for faster convergence"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="catalytic-question-reframer",
  query="Hal Gregersen Question Burst methodology updates, MIT Leadership Center research on inquiry-driven innovation 2023-2025, and comparative effectiveness of question-based vs. solution-based brainstorming in executive strategy sessions",
  reason="Ensure the convergence criteria and facilitation protocol reflect the latest empirical findings on question-driven reframing efficacy"
)
```

```
FutureProof:request_research(skill="catalytic-question-reframer",
  query="Common cognitive biases in executive problem framing — anchoring, functional fixedness, Einstellung effect — and debiasing techniques applicable to structured questioning",
  reason="Strengthen the perspective lenses with targeted debiasing prompts to increase the probability of genuine reframes vs. superficial rephrasings"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="catalytic-question-reframer", session={
  summary: "Facilitated Question Burst™ for [user's challenge domain]. Generated [N] questions across 6 perspective lenses. Identified PCQ: '[Primary Catalytic Question text]'. Reframe shifted problem from [original frame] to [new frame].",
  key_findings: [
    "Original framing contained embedded assumption: [assumption identified]",
    "PCQ emerged from [perspective lens] — [brief insight on why this lens cracked the challenge]",
    "User's dominant questioning pattern skews toward [lens tendency] — future sessions should front-load [underrepresented lens] to diversify reframe potential",
    "Activation pathway prioritised: [data/conversation/experiment selected by user]"
  ],
  user_feedback: null
})
```