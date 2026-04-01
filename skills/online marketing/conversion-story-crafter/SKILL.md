---
name: conversion-story-crafter
description: |
  Crafts high-converting signature stories using Brunson's Epiphany Bridge technique, Colin Boyd's Conversion Story Formula, and Fladlien's micro-story close methodology.
  Trigger: when a user wants to create, refine, or script an origin story, epiphany bridge, or conversion story for a webinar, sales page, or live presentation. Also triggers when a user says they need a story that sells or asks how to make their offer feel inevitable through narrative.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="conversion-story-crafter")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay special attention to the user's ICA profiles, existing offer language, prior story assets, and any tested narrative angles from previous sessions.

## Step 2: Get Input

Ask the user:

1. **Story purpose** — Where will this story be deployed? (webinar, sales page, VSL, stage presentation, email sequence, micro-story close within a pitch)
2. **Offer context** — What is the offer the story must bridge to? Provide the core transformation promise (before state → after state) and price point if known.
3. **Story raw material** — Share any of the following:
   - A personal experience, turning point, or "aha moment" related to the offer
   - A client/customer result or testimonial
   - A backstory, failure, or struggle that preceded discovery of the method/product
   - Existing draft narrative or bullet-point outline
4. **ICA profile** — Who is the ideal audience hearing this story? What do they currently believe, fear, or desire? What false beliefs does the offer need to dismantle?
5. **Story type requested** — Which archetype(s) are they building?
   - **Origin Story** (how you discovered the method/framework)
   - **Epiphany Bridge** (the moment of realisation that reframes a false belief)
   - **Conversion Story** (a structured narrative that moves the listener from scepticism to purchase readiness)
   - **Micro-story close** (a compact proof-and-pivot story used mid-pitch to neutralise a specific objection)
   - **Not sure** — help me choose

Apply any user-specific `instructions` from FutureProof context to adjust story tone, vocabulary, or structural preferences.

## Step 3: Diagnose the Narrative Gap

Before writing, perform a **Story-Offer Alignment Diagnostic**:

### 3A: False Belief Mapping

Identify the 3 core false beliefs the ICA holds that prevent them from purchasing:

| # | False Belief | Emotional Weight (1–10) | Story Type Best Suited to Dismantle |
|---|---|---|---|
| 1 | _e.g. "I need more traffic before I need a funnel"_ | | |
| 2 | | | |
| 3 | | | |

### 3B: Emotional Arc Assessment

Map the required emotional journey using the **Brunson Epiphany Bridge Framework**:

1. **Backstory** — Where were you (or the character) before the epiphany? What was the external situation and internal emotional state?
2. **Wall / Conflict** — What event, failure, or frustration created the breaking point?
3. **Epiphany** — What was the single insight, moment, or realisation that changed everything? (This must be visceral and specific — not abstract.)
4. **Framework Birth** — How did the epiphany crystallise into the method, system, or offer being sold?
5. **Achievement** — What tangible result followed? (Specificity is mandatory: numbers, timelines, named outcomes.)
6. **Bridge to Offer** — How does the listener access the same transformation without needing the same painful journey?

### 3C: Boyd Conversion Story Structure Check

Validate that the raw material supports Colin Boyd's five-part Conversion Story Formula:

1. **Relatable Setup** — Does the opening mirror the ICA's current situation closely enough to trigger self-identification within 15 seconds?
2. **Unexpected Twist** — Is there a genuine plot turn that disrupts the predictable trajectory?
3. **Lesson / Framework Reveal** — Does the story naturally surface a proprietary principle or method?
4. **Proof of Concept** — Is there embedded evidence (results, data, third-party validation) within the narrative?
5. **Seamless Offer Transition** — Does the story's conclusion create a logical, non-jarring bridge to the offer?

Flag any gaps as **Critical** (story will fail without it), **Important** (story will underperform), or **Optional** (polish-level enhancement).

## Step 4: Craft the Story

Build the complete story asset(s) as specified below, based on the story type(s) selected in Step 2.

### Deliverable A: Story Architecture Document

A structured outline containing:

- **Story title** (internal working name)
- **Story type** (Origin / Epiphany Bridge / Conversion Story / Micro-Story Close)
- **Target false belief** being dismantled
- **Emotional arc** mapped to Brunson's six stages (from Step 3B)
- **Key sensory anchors** — 3–5 specific, vivid details (settings, dialogue snippets, physical sensations) that make the story feel lived-in rather than conceptual
- **Transition line** — the exact sentence that bridges from story conclusion to offer introduction

### Deliverable B: Full Story Script

A presentation-ready script with the following specifications:

- **Word count guidance**: Origin Story (800–1,200 words), Epiphany Bridge (500–900 words), Conversion Story (1,000–1,500 words), Micro-Story Close (150–300 words)
- **Stage directions** in brackets — pauses, vocal emphasis, slide cues where applicable
- **Dialogue reconstructions** written as natural speech, not reported speech (e.g., "She looked at me and said, 'That's never going to work'" — not "She told me it wouldn't work")
- **The Epiphany Moment** formatted as a standalone paragraph, preceded by a deliberate pause cue, using present-tense language to heighten immediacy
- **Offer bridge** scripted as a complete paragraph — not left as a placeholder

### Deliverable C: Micro-Story Variant Bank (if applicable)

If the user is building a webinar or long-form pitch, provide 3 micro-story closes (Fladlien method) derived from the primary narrative:

| Micro-Story # | Objection It Neutralises | Setup (1–2 sentences) | Pivot Line | Close Line |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

Each micro-story must be deployable as a standalone 60–90 second insertion at any point in a pitch.

### Deliverable D: Story Score Card

Rate the crafted story on these dimensions (1–10):

| Dimension | Score | Rationale |
|---|---|---|
| **ICA Self-Identification Speed** — Does the listener think "that's me" within 15 seconds? | | |
| **Emotional Specificity** — Are feelings shown through detail, not told through labels? | | |
| **Epiphany Clarity** — Is the single insight unmistakably clear and memorable? | | |
| **False Belief Disruption** — Does the story make the old belief untenable? | | |
| **Offer Inevitability** — Does the offer feel like the only logical next step? | | |
| **Proof Embedding** — Are results woven into narrative rather than appended as claims? | | |
| **Fladlien Micro-Close Potential** — Can fragments of this story be extracted for mid-pitch objection handling? | | |

Include **top 3 amplification recommendations** — specific, actionable edits (not general advice) with exact replacement language.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="conversion-story-crafter", experiment={
  hypothesis: "Leading with the Wall/Conflict moment before the Backstory (in medias res opening) increases audience retention through the first 2 minutes of the story",
  variants: ["control: chronological Backstory → Wall → Epiphany sequence", "variant: Wall → Backstory → Epiphany (in medias res)"],
  measurement: "Audience retention rate at 2-minute mark (webinar) or scroll depth past story section (sales page), plus downstream conversion rate",
  expected_impact: "20% improvement in story completion rate leading to 8–12% lift in offer click-through"
})
```

```
FutureProof:save_experiment(skill="conversion-story-crafter", experiment={
  hypothesis: "Adding a second character's dialogue in the Epiphany moment (external validation voice) increases perceived credibility of the realisation",
  variants: ["control: internal monologue epiphany", "variant: epiphany triggered or confirmed by a mentor/peer dialogue line"],
  measurement: "Post-webinar survey on 'How believable was the presenter's story?' (1–10) and offer conversion rate",
  expected_impact: "0.5–1.0 point increase in believability score; 5% conversion lift"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="conversion-story-crafter",
  query="Latest data on narrative transportation theory applied to sales contexts 2024 — specifically Epiphany Bridge completion rates across webinar, VSL, and written sales page formats, plus Fladlien's micro-story close effectiveness benchmarks",
  reason="Ensure story structures are calibrated to current audience attention patterns and that recommended story lengths and placement align with empirical performance data across delivery formats"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="conversion-story-crafter", session={
  summary: "Crafted [story type(s)] for [offer name/description] targeting [ICA segment] — dismantling false belief: [primary false belief addressed]",
  key_findings: ["finding 1: e.g. user's raw material strongest in Backstory but lacked a specific Epiphany moment — fabricated sensory anchor to crystallise it", "finding 2: e.g. Offer bridge required reframe from feature-language to transformation-language to maintain emotional continuity", "finding 3: e.g. Generated 3 Fladlien micro-story closes covering price, timing, and trust objections"],
  assets_created: ["Story Architecture Document", "Full Story Script ([word count] words)", "Micro-Story Variant Bank (3 variants)", "Story Score Card"],
  user_feedback: null
})
```