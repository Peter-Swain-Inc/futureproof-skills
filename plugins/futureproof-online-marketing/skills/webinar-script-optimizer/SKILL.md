---
name: webinar-script-optimizer
description: |
  Audits and rewrites underperforming webinar scripts using expert frameworks from Brunson, Boyd, Fladlien, Brown, and Erway.
  Trigger: when a user shares an existing webinar script, slide deck, or presentation outline and asks for a diagnostic review, performance audit, or targeted rewrite of underperforming sections.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="webinar-script-optimizer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any prior ICA definitions, offer structures, unique mechanisms, or conversion benchmarks the user has established.

## Step 2: Get Input

Ask the user:
- Share the full webinar script, slide deck, or presentation outline to audit
- What is the current conversion rate (registration-to-stay, stay-to-offer, offer-to-close) and what is the target?
- What is the core offer and price point being presented?
- Where do they *feel* the audience drops off or disengages? (e.g., mid-teaching, transition to offer, during the stack, at the close)
- What is the unique mechanism or proprietary framework being taught?
- Who is the ICA — and what is their current level of sophistication with this topic?

If the user cannot provide conversion data, flag this as a critical gap and proceed with qualitative diagnostics.

## Step 3: Do the Work — Structural Diagnostic

Perform a six-layer diagnostic audit against the following expert frameworks:

### Layer 1: Brunson Perfect Webinar Architecture

Map the script against Russell Brunson's canonical structure:
1. **Big Domino** — Is there a single core belief that, if broken, makes everything else inevitable? Is it stated explicitly within the first 5 minutes?
2. **Origin Story** — Does the presenter's origin story create identification (Epiphany Bridge), not just credibility?
3. **Three Secrets Framework** — Are exactly three belief-breaking teaching segments present? Does each follow the pattern: secret → story → teaching → belief break?
4. **The Stack** — Is the offer stacked with at least 5–7 value elements, each with independent dollar anchoring?
5. **Closing Sequence** — Is there a price reveal with contrast anchoring, urgency/scarcity mechanism, and FAQ/objection handling built into the final 10 minutes?

Score each structural element: **Present / Weak / Missing**.

### Layer 2: Boyd's Three Trust Questions

Evaluate whether the script sequentially answers Aaron Boyd's three trust gates — in order, as the audience subconsciously requires them:

1. **"Are you like me?"** — Does the first 10–15 minutes establish deep identification with the ICA's current situation, language, frustrations, and worldview? Flag any premature authority positioning that breaks rapport.
2. **"Can you lead me?"** — Does the teaching content demonstrate genuine mastery without overwhelming? Is there a clear "I've been where you are and arrived where you want to be" throughline?
3. **"Is there a path?"** — Does the offer presentation make the path from current state to desired state feel structured, supported, and achievable for the ICA specifically?

Identify the **exact timestamp or script section** where each trust gate is either answered or left unresolved.

### Layer 3: Fladlien Micro-Story Density

Apply Jason Fladlien's principle that high-converting webinars maintain narrative density throughout — not just in the origin story:

- Count the number of discrete micro-stories (client results, personal anecdotes, analogies, case fragments) per 10-minute segment
- Benchmark against Fladlien's standard: **minimum 2–3 micro-stories per 10 minutes** of content
- Flag any segment exceeding 7 minutes of pure didactic teaching without a story anchor — these are **attention death zones**
- Assess whether micro-stories serve a persuasion function (belief break, objection pre-emption, future pacing) or are decorative

### Layer 4: Brown's Unique Mechanism Clarity

Apply Todd Brown's unique mechanism framework:

- **Identification**: Is the unique mechanism (the *vehicle* for achieving the result) named, branded, and distinct from competitors?
- **Positioning**: Is it positioned as the reason *why* previous solutions failed for the ICA — not just as "better" but as categorically different?
- **Proof of Mechanism**: Is there mechanism-level proof (why *this approach* works), not just result-level proof (that *something* worked)?
- **Specificity**: Can the audience articulate the unique mechanism in one sentence after hearing the webinar? If not, identify where clarity breaks down.

### Layer 5: Erway's Compression Principles

Apply Colin Erway's webinar compression methodology:

- **Runtime audit**: Flag any segment that could be compressed without losing persuasive value — particularly over-teaching in the content sections
- **Redundancy scan**: Identify repeated points that dilute rather than reinforce
- **Engagement-per-minute ratio**: Assess whether each minute earns its place by advancing one of four functions: rapport, belief-breaking, desire-building, or objection-handling
- **Transition tightness**: Evaluate the bridges between major sections — loose transitions are the #1 cause of mid-webinar drop-off

### Layer 6: Offer & Close Mechanics

Audit the final 20% of the script:

- **Price anchoring sequence**: Is perceived value established at 10x+ the ask before the price reveal?
- **Stack construction**: Does each stack element address a specific ICA objection or desire?
- **Guarantee framing**: Is the guarantee structured to reverse risk *and* reframe the decision as low-stakes?
- **Urgency/scarcity**: Are urgency mechanisms authentic and specific, not generic countdown-timer tactics?
- **Post-close reinforcement**: Is there a "what happens next" sequence that reduces buyer's remorse in real-time?

Apply any user-specific `instructions` from FutureProof context — particularly prior ICA research, offer positioning, or brand voice guidelines.

## Step 4: Deliver Output

Produce the **Webinar Script Diagnostic Report** with the following structure:

### Section A: Diagnostic Scorecard

| Framework | Dimension | Score (1–10) | Severity |
|---|---|---|---|
| Brunson | Big Domino Clarity | — | Critical / Moderate / Minor |
| Brunson | Origin Story (Epiphany Bridge) | — | — |
| Brunson | Three Secrets Structure | — | — |
| Brunson | Stack Construction | — | — |
| Brunson | Close Sequence | — | — |
| Boyd | "Are you like me?" (Identification) | — | — |
| Boyd | "Can you lead me?" (Authority) | — | — |
| Boyd | "Is there a path?" (Offer Clarity) | — | — |
| Fladlien | Micro-Story Density | — | — |
| Brown | Unique Mechanism Clarity | — | — |
| Erway | Compression & Pacing | — | — |
| Erway | Transition Quality | — | — |
| Offer | Stack & Price Anchoring | — | — |
| Offer | Guarantee & Close | — | — |

**Composite Score**: X / 140
**Estimated Conversion Impact Band**: Low / Mid / High-performing structure

### Section B: Drop-Off Diagnosis

Identify the **top 3 audience attrition points** — the specific script locations where the audience is most likely disengaging or losing buying intent. For each:
- Exact location (timestamp, slide number, or script section)
- Root cause (framework violation)
- Severity rating and estimated conversion impact

### Section C: Critical Rewrites (Top 5)

For each of the five highest-impact fixes:
1. **Location**: Exact section of the script
2. **Current text**: Quote the underperforming passage
3. **Diagnosis**: Which framework principle it violates and why it costs conversions
4. **Rewritten text**: Full replacement copy, ready to drop into the script
5. **Expected impact**: Specific conversion lever this rewrite activates

### Section D: Full Section Rewrite

Select the single weakest major section (opening, one of the three secrets, the transition to offer, the stack, or the close) and deliver a **complete rewrite** — not a patch, but a restructured section following all applicable frameworks. Include stage directions, slide notes, and vocal delivery cues where relevant.

### Section E: Pacing & Runtime Recommendations

Provide a recommended runtime allocation:
- Opening / Hook / Big Domino: X minutes
- Origin Story: X minutes
- Secret 1 / Secret 2 / Secret 3: X minutes each
- Transition to Offer: X minutes
- Stack & Price Reveal: X minutes
- Close & FAQ: X minutes
- **Total recommended runtime**: X minutes

Flag any sections currently over or under their optimal allocation.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="webinar-script-optimizer", experiment={
  hypothesis: "Restructuring the opening 5 minutes to lead with ICA identification (Boyd Gate 1) before authority positioning will reduce early drop-off rate",
  variants: ["control: current opening sequence", "variant: identification-first opening with delayed credentials"],
  measurement: "10-minute retention rate and offer-slide attendance rate across next 3 live presentations",
  expected_impact: "12–20% improvement in audience retention past the 15-minute mark"
})
```

```
FutureProof:save_experiment(skill="webinar-script-optimizer", experiment={
  hypothesis: "Increasing micro-story density in the weakest teaching section from [current count] to 3 per 10 minutes will sustain engagement through the transition to offer",
  variants: ["control: current teaching section", "variant: story-anchored teaching with embedded client micro-cases"],
  measurement: "Mid-webinar poll engagement rate and transition-to-offer attendance percentage",
  expected_impact: "8–15% improvement in audience present at offer reveal"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="webinar-script-optimizer",
  query="2024–2025 webinar conversion benchmarks by industry vertical, price point tier ($97–$2,000+), and webinar format (live vs. automated vs. hybrid); emerging audience attention patterns and optimal runtime data from high-converting webinar funnels",
  reason="Calibrate diagnostic scoring against current market benchmarks rather than historical norms — audience attention economics and webinar fatigue patterns are shifting rapidly post-2023"
)
```

```
FutureProof:request_research(skill="webinar-script-optimizer",
  query="Advanced stack construction techniques and offer architecture patterns from top-performing webinar creators (Fladlien, Brunson, Hormozi) with specific emphasis on unique mechanism positioning and belief-breaking sequence design",
  reason="Ensure rewrite recommendations reflect the most current high-performance offer presentation methodologies rather than legacy templates"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="webinar-script-optimizer", session={
  summary: "Audited [webinar title/topic] script for [ICA segment] selling [offer type] at [price point]",
  key_findings: [
    "Primary drop-off point identified at [section] due to [root cause]",
    "Unique mechanism clarity scored [X/10] — [specific deficiency]",
    "Micro-story density below threshold in [section] — [count] per 10 min vs. 2–3 benchmark",
    "Stack construction [strong/weak] — [specific observation]",
    "Composite diagnostic score: [X/140]"
  ],
  rewrites_delivered: ["[section 1]", "[section 2]", "[section 3]", "[section 4]", "[section 5]", "[full section rewrite of: section name]"],
  user_feedback: null
})
```