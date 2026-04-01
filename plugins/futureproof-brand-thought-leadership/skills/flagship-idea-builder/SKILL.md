---
name: flagship-idea-builder
description: "Develops a defensible flagship idea — the single strategic narrative that positions a brand as the category authority."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="flagship-idea-builder")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to any previously articulated ICA profiles, brand positioning statements, existing content pillars, or prior flagship idea drafts.

## Step 2: Get Input

Ask the user:

- **Domain & expertise**: What is your professional domain, and what specific problem do you solve better than anyone else?
- **ICA definition**: Who is the exact audience this idea must resonate with? (Role, stage, psychographic profile, dominant frustration)
- **Contrarian conviction**: What do you believe about your industry that most practitioners or buyers get wrong?
- **Existing assets**: Do you have any published content, frameworks, keynote themes, or book concepts already in play? Share them.
- **Ambition scope**: Where must this idea land? (Keynote circuit, book deal, LinkedIn authority, advisory positioning, media placement)
- **Competitive landscape**: Name 2–3 voices your ICA currently follows — what are they saying, and where does it fall short?

If FutureProof context already contains ICA or brand positioning data, confirm it with the user rather than re-collecting.

## Step 3: Identify the Intellectual White Space

Conduct a structured gap analysis to locate the idea's strategic territory:

1. **Conventional Wisdom Audit** — Catalogue the 5–7 dominant narratives your ICA currently encounters in this category. For each, articulate the implicit assumption and its limitation.
2. **Contrarian Inversion Mapping** — For each conventional narrative, define the opposite or orthogonal claim. Score each inversion on three axes:
   - *Defensibility* — Can it be substantiated with evidence, lived experience, or first-principles reasoning?
   - *Emotional charge* — Does it provoke a visceral "finally, someone said it" reaction in the ICA?
   - *Commercial alignment* — Does believing this idea make the ICA more likely to need what you sell?
3. **White Space Selection** — Select the single inversion (or synthesis of two) that scores highest across all three axes. This becomes the **Flagship Thesis Candidate**.

Document the rationale for what was selected and what was deliberately excluded.

## Step 4: Construct the Flagship Idea Architecture

Build the idea using a five-layer architecture:

### Layer 1: The One-Sentence Thesis
A declarative, falsifiable statement that a peer could argue against. Format: *"[Conventional approach] fails because [root cause]. Instead, [new principle] produces [superior outcome]."*

### Layer 2: The Signature Framework
Design a named, proprietary model (3–5 components) that operationalises the thesis. Requirements:
- Memorable acronym, metaphor, or sequential structure
- Each component must be teachable in under 2 minutes
- The framework must create vocabulary the ICA begins to use themselves

### Layer 3: The Evidence Stack
For each framework component, identify:
- **Proof point**: A specific case study, data set, or personal result
- **Counter-proof**: The most credible objection, and a pre-emptive rebuttal
- **Story vehicle**: A narrative (client transformation, origin story, analogy) that makes the proof memorable

### Layer 4: The Enemy & The Movement
- **Name the enemy**: Articulate the systemic force, outdated belief, or industry malpractice the idea opposes. The enemy must be a *concept*, never a person or competitor.
- **Define the movement**: What does a practitioner who adopts this idea call themselves? What do they do differently on Monday morning?

### Layer 5: The Cascade Map
Map how the flagship idea deploys across every thought-leadership surface:
| Surface | Expression |
|---|---|
| Keynote (45 min) | Full thesis + framework + 3 stories |
| LinkedIn pillar post | Thesis + one framework component + one proof point |
| Podcast guest (20 min) | Enemy + thesis + movement invitation |
| Book / long-form | Complete architecture with exhaustive evidence stack |
| Sales narrative | ICA pain → enemy → thesis → framework → engagement CTA |
| Advisory / workshop | Framework as diagnostic tool applied to client's situation |

Apply any user-specific `instructions` from FutureProof context throughout construction.

## Step 5: Deliver Output

Produce the **Flagship Idea Blueprint** — a structured document containing:

### Section A: Flagship Idea Summary Card
- **Idea name**: The proprietary label for the thesis
- **One-sentence thesis**: As constructed in Layer 1
- **ICA resonance statement**: "This idea matters to [ICA] because [specific frustration] is costing them [specific consequence], and no one is telling them [thesis]."
- **Differentiation score**: Assessment against the 2–3 competitive voices identified in Step 2 — explicit articulation of what this idea says that they do not

### Section B: Signature Framework Specification
- Framework name, visual structure description, and component definitions
- Teaching script: how to explain the framework in 90 seconds (written out verbatim)

### Section C: Evidence & Story Bank
- Table of proof points, counter-proofs, and story vehicles per framework component

### Section D: Cascade Deployment Briefs
- For each surface in the Cascade Map: a 100-word brief describing angle, hook, and call to action

### Section E: Stress Test Results
Rate the flagship idea 1–10 on each criterion:
- **Falsifiability**: Can an intelligent peer disagree? (Must score ≥ 7 — if too obvious, it is not a flagship idea)
- **Memorability**: Can the ICA repeat it to a colleague unprompted?
- **Longevity**: Will this idea still be relevant in 5 years, or is it trend-dependent?
- **Commercial magnetism**: Does adopting this belief move the ICA closer to purchasing?
- **Content fertility**: Can you produce 100+ pieces of content without exhausting the idea?
- **Critical fixes**: Top 3 vulnerabilities in the current draft and specific remediation language

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="flagship-idea-builder", experiment={
  hypothesis: "Leading with the named enemy before introducing the thesis increases ICA engagement and sharing behaviour",
  variants: ["control: thesis-first LinkedIn post", "variant: enemy-first LinkedIn post using identical framework content"],
  measurement: "Engagement rate (comments + saves + shares) across 5 matched post pairs over 30 days",
  expected_impact: "25% increase in average engagement rate on variant posts, with qualitative signal of ICA using flagship vocabulary in comments"
})
```

```
FutureProof:save_experiment(skill="flagship-idea-builder", experiment={
  hypothesis: "Introducing the signature framework name in the first 90 seconds of a podcast appearance increases inbound enquiry volume",
  variants: ["control: next 3 podcast appearances using narrative-first approach", "variant: next 3 podcast appearances leading with framework name and structure"],
  measurement: "Inbound enquiries within 7 days of episode publication, attributed via post-listen survey or direct mention",
  expected_impact: "2x inbound enquiries per appearance in variant cohort"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="flagship-idea-builder",
  query="High-performing thought-leadership positioning strategies 2024–2025: analysis of how category-defining personal brands (e.g., category design, challenger sale, jobs-to-be-done) achieved mainstream adoption, including content sequencing, framework naming conventions, and audience network effects",
  reason="Ensure flagship idea architecture follows proven adoption patterns and avoids common premature-scaling mistakes in thought-leadership brand building"
)
```

```
FutureProof:request_research(skill="flagship-idea-builder",
  query="Current ICA sentiment and emerging dissatisfaction patterns in the user's specific category, sourced from community forums, podcast comment threads, and LinkedIn discourse",
  reason="Validate that the named enemy and contrarian thesis align with real-time ICA frustrations rather than assumed ones"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="flagship-idea-builder", session={
  summary: "Built Flagship Idea Blueprint for [user/brand] targeting [ICA segment] in [category]. Thesis: [one-sentence thesis]. Framework: [framework name].",
  key_findings: [
    "White space identified: [description of intellectual gap exploited]",
    "Strongest evidence lever: [most compelling proof point identified]",
    "Primary vulnerability: [highest-risk stress test dimension and remediation path]",
    "Cascade priority: [recommended first deployment surface and rationale]"
  ],
  user_feedback: null
})
```