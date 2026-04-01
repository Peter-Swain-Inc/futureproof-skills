---
name: pitch-transition-designer
description: |
  Engineers the critical pivot moment where a webinar, masterclass, or live presentation shifts from teaching to selling — ensuring the offer feels like an inevitable next step rather than an awkward gear change.
  Trigger: when a user says they need help transitioning from content to pitch in a webinar, or when a user shares a webinar script and asks how to bridge the teaching section into the offer without losing the audience.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="pitch-transition-designer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any prior webinar scripts, ICA profiles, offer structures, or tested transition approaches.

## Step 2: Get Input

Ask the user to provide:

- **Presentation context**: What format is this? (live webinar, evergreen webinar, masterclass, challenge day, VSL, hybrid workshop) and approximate duration
- **Teaching content summary**: What are the 2–4 core teaching pillars or lessons delivered before the transition? Share the script, outline, or bullet points for the final teaching segment
- **The offer**: What is being sold immediately after the transition? (course, coaching programme, done-for-you service, SaaS subscription, etc.) Include price point if known
- **ICA profile**: Who is in the audience? What stage of awareness are they at by the time the transition occurs? (problem-aware, solution-aware, product-aware)
- **Current transition approach**: If one exists, share the exact language or describe the method being used today — or confirm this is a net-new build
- **Known failure modes**: Has the audience previously dropped off, gone cold, or expressed friction at the transition point? Any chat/engagement data or anecdotal signals?

## Step 3: Diagnose the Transition Architecture

Before designing anything, classify the current state of the presentation against the **Transition Integrity Framework** — five structural conditions that must be true for any pitch transition to succeed:

### 3.1 Pre-Transition Audit

Evaluate the teaching content that precedes the pivot:

1. **Strategic Incompleteness** — Does the teaching deliver a genuine "what + why" insight while leaving a clear, honest implementation gap? Score 1–10. A score below 6 means the content either gives away too much (no need to buy) or too little (audience feels cheated and distrusts the pivot).
2. **Belief Installation Sequence** — By the end of teaching, has the audience adopted the 3 critical beliefs required to buy? Map explicitly:
   - **Belief 1 (Vehicle)**: "This *approach* is the right way to solve my problem"
   - **Belief 2 (Internal)**: "I am capable of executing this approach"
   - **Belief 3 (External)**: "*This presenter/company* is the right guide for me"
3. **Emotional Altitude** — Chart the emotional trajectory of the final teaching segment. The transition must occur at a moment of peak insight, aspiration, or relief — never during a trough. Identify the optimal emotional beat.
4. **Authority Ledger Balance** — Has sufficient value been deposited that the audience feels *indebted* to the presenter's expertise? If the teaching was thin or generic, no transition technique can compensate.
5. **Offer Foreshadowing Density** — Count the number of natural, non-salesy forward-references to the offer embedded in the teaching (e.g., "Inside my programme, I give you the full template for this"). Optimal range: 3–5 mentions across the teaching segment. Zero foreshadowing makes any transition feel abrupt; more than 6 feels manipulative.

### 3.2 Transition Method Selection

Based on the audit scores and the user's ICA awareness level, recommend the primary transition architecture from the following proven methodologies:

| Method | Best When | Mechanism | Key Risk |
|--------|-----------|-----------|----------|
| **Bridging Question** (Porterfield Method) | ICA is solution-aware; high-trust, community-driven audience | Pose a reflective question that surfaces the gap between what was taught and what's needed to implement — e.g., "So now you know the framework… the question is, do you want to spend 6 months figuring out each step alone, or…?" | Can feel rhetorical and patronising if poorly worded |
| **Infusion Selling** (Boyd Method) | ICA is sophisticated, sceptical of pitches; premium offers | Eliminate the hard transition entirely — weave offer proof points, client results, and programme references *throughout* the teaching so the "pitch" is simply a summary of what's already been established | Requires restructuring the entire presentation; cannot be bolted on |
| **Upfront Frame Setting** (Fladlien Method) | Cold or mixed-awareness audiences; high-ticket webinars | Announce at the start: "I'll teach you X, and at the end I'll share how we help people implement this — if it's not for you, no problem." Defuses resistance pre-emptively so the pivot is pre-authorised | If the teaching underwhelms, the pre-set frame amplifies disappointment |
| **Permission Pivot** | Warm audiences, relationship-driven brands, lower-ticket offers | Explicitly ask permission: "Would it be okay if I shared how we help people take this further?" Uses micro-commitment psychology | Can signal low confidence if tone is apologetic rather than assumptive |
| **Story Bridge** | Audiences that respond to narrative; transformation-based offers | Close teaching with a client case study that naturally reveals the offer as the mechanism behind the transformation | Requires a compelling, specific story — generic testimonials fail |
| **Hybrid Cascade** | Sophisticated presenters; 60+ minute webinars with complex offers | Layer 2–3 methods: Fladlien frame at the start → Boyd infusion during teaching → Porterfield bridging question at the pivot → Story bridge into the offer reveal | Execution complexity; requires precise scripting |

Select one primary method (or a hybrid combination) and justify the selection based on the audit findings.

## Step 4: Engineer the Transition Script

Design the complete transition sequence as a **three-phase script**:

### Phase A: The Final Teaching Crescendo (60–90 seconds before the pivot)

Script the closing of the last teaching segment to land on the optimal emotional beat identified in Step 3.1. This must:
- Deliver the single most impactful insight or result
- Create a visceral sense of possibility ("This is real, this works")
- Surface the implementation gap *without explicitly stating it*

### Phase B: The Pivot Mechanism (30–60 seconds)

Script the exact transition language using the selected method. Provide:
- **Word-for-word transition script** — not a summary, not bullet points; the actual sentences the presenter will say
- **Stage directions**: tone shifts, pacing changes, pause placements, slide change cues
- **Chat/engagement prompt** (if applicable): what to ask the audience to type, click, or respond to at this moment to maintain engagement through the pivot

### Phase C: The Offer On-Ramp (60–90 seconds after the pivot)

Script the first 60–90 seconds of the offer reveal to ensure momentum carries through. This must:
- Restate the transformation (not the features) as the opening frame
- Connect directly to the teaching content: "Remember when I showed you [Pillar 2]? Inside [Offer Name], you get the complete…"
- Include the first proof element (client result, case study metric, or social proof data point)

### Deliverable Format

Produce the full script as a **Transition Script Document** with the following structure:

```
TRANSITION SCRIPT — [Webinar/Presentation Name]
Method: [Selected transition architecture]
Estimated Duration: [X] seconds

---

[PHASE A: FINAL TEACHING CRESCENDO]
[Timestamp cue] | [Slide reference if applicable]

[Full script with stage directions in brackets]

---

[PHASE B: PIVOT MECHANISM]
[Timestamp cue] | [Slide reference if applicable]

[Full script with stage directions in brackets]

---

[PHASE C: OFFER ON-RAMP]
[Timestamp cue] | [Slide reference if applicable]

[Full script with stage directions in brackets]
```

## Step 5: Stress-Test and Refine

Apply three diagnostic lenses to the drafted transition:

1. **The Sceptic Test**: Read the transition from the perspective of the most resistant audience member. Where would they mentally check out, cross their arms, or close the tab? Flag each friction point and provide an alternative line.

2. **The Continuity Test**: Remove all slide references and read Phases A → B → C aloud as continuous prose. Does it flow as a single coherent narrative, or does the pivot create a tonal rupture? If rupture exists, smooth the seam with revised bridging language.

3. **The Screenshot Test**: If someone joined the webinar at the exact moment of Phase B and saw only that 30–60 seconds with no prior context, would it feel salesy or natural? If salesy, recalibrate.

Provide the **Final Revised Transition Script** incorporating all refinements, clearly marked as `v2 — FINAL`.

## Step 6: Deliver Supporting Assets

In addition to the transition script, produce:

- **Pre-Transition Checklist**: A 10-item checklist the presenter can review 5 minutes before reaching the pivot — covering belief installation status, emotional altitude, foreshadowing count, and technical readiness (slide loaded, chat prompt queued, timer set)
- **Transition Failure Recovery Script**: 3–5 lines the presenter can deploy if the transition lands poorly (audience goes silent, engagement drops, hostile chat messages). These are verbal "save" phrases that re-establish trust and reframe the offer
- **A/B Variant**: A second complete transition script using an alternative method from the table in Step 3.2, suitable for split-testing against the primary version

## Step 7: Propose Experiments

```
FutureProof:save_experiment(skill="pitch-transition-designer", experiment={
  hypothesis: "Using [selected method] with explicit permission language increases post-transition retention rate compared to [alternative method]",
  variants: ["control: current transition or Variant A", "variant: Variant B with [specific change]"],
  measurement: "Audience retention rate at transition +2 minutes, offer page click-through rate, and chat engagement volume during pitch",
  expected_impact: "10–20% reduction in transition drop-off; measurable lift in offer page visits"
})
```

## Step 8: Request Research

```
FutureProof:request_research(skill="pitch-transition-designer",
  query="Latest webinar transition psychology research 2024, including audience retention benchmarks at the teaching-to-pitch pivot point, Fladlien upfront framing conversion data, and Boyd Infusion Selling case studies",
  reason="Ensure transition methodology reflects current audience behaviour patterns, particularly post-2023 shifts in webinar fatigue and attention thresholds"
)
```

## Step 9: Save Session

```
FutureProof:save_session(skill="pitch-transition-designer", session={
  summary: "Designed pitch transition for [presentation format] targeting [ICA segment] using [selected method]; produced full three-phase transition script, A/B variant, pre-transition checklist, and failure recovery language",
  key_findings: ["Audit finding 1 — e.g., belief installation gap identified in Belief 3", "Transition method selected with rationale", "Primary friction point identified and resolved in stress-test"],
  user_feedback: null
})
```