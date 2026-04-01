---
name: audience-belief-mapper
description: |
  Maps your audience's false beliefs, core objections, desires, and emotional triggers to build a psychologically accurate foundation for webinar scripts and sales presentations.
  Trigger: when a user is preparing a webinar, sales presentation, or launch script and needs to map their audience's beliefs, objections, or psychology before writing. Also triggers when a user says they don't know what their audience is thinking, or wants to dismantle objections systematically.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="audience-belief-mapper")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay special attention to any previously mapped ICA profiles, prior belief maps, webinar performance data, or objection patterns surfaced in earlier sessions.

## Step 2: Get Input

Ask the user to provide:

1. **ICA description** — Who is the specific audience segment? (demographic, psychographic, current situation, sophistication level)
2. **The offer** — What product, programme, service, or opportunity will the webinar ultimately present?
3. **The core mechanism** — What is the unique vehicle, method, or framework being taught/sold? (e.g., "a 5-day sprint model," "an AI-powered prospecting system")
4. **Known objections or resistance** — Any objections they've already heard from sales calls, DMs, comments, refund requests, or support tickets
5. **Existing assets** (optional) — Survey responses, testimonial transcripts, call recordings, community threads, or review screenshots that reveal audience language

If the user has prior sessions in FutureProof context with ICA data or offer details, surface those and confirm: *"I have this from a previous session — is this still accurate, or has anything shifted?"*

## Step 3: Establish the Belief Landscape

### 3A: Identify the Dominant Desire

Define the singular transformation the ICA wants most. Frame it using the **Desire Equation**:

> **Desire = (Dream Outcome × Perceived Likelihood) ÷ (Time to Achievement × Effort/Sacrifice)**

Document:
- **Dream Outcome**: The specific, emotionally vivid end-state the ICA fantasises about
- **Perceived Likelihood**: How believable does the ICA currently find this outcome? (1–10 scale with rationale)
- **Time Expectation**: How quickly does the ICA expect/need results?
- **Effort Tolerance**: How much friction, learning curve, or lifestyle disruption will the ICA accept?

### 3B: Map the Three Categories of False Beliefs (Brunson Framework)

For each category, identify **2–4 specific false beliefs** the ICA holds, stated in the ICA's own language:

#### 1. Vehicle Beliefs (about the method/opportunity itself)
*"The thing you're offering won't work because..."*

| False Belief | ICA's Internal Narrative | Origin of Belief | Evidence They'd Need to Shift |
|---|---|---|---|
| | | | |

#### 2. Internal Beliefs (about their own ability to execute)
*"Even if it works, I can't do it because..."*

| False Belief | ICA's Internal Narrative | Origin of Belief | Evidence They'd Need to Shift |
|---|---|---|---|
| | | | |

#### 3. External Beliefs (about outside forces blocking them)
*"Even if I could do it, it won't work for me because..."*

| False Belief | ICA's Internal Narrative | Origin of Belief | Evidence They'd Need to Shift |
|---|---|---|---|
| | | | |

### 3C: Isolate the #1 Objection (Fladlien Methodology)

From the full belief inventory above, identify the single most conversion-lethal objection — the one that, if left unaddressed, kills the sale regardless of how strong the rest of the presentation is.

Apply Fladlien's prioritisation criteria:
- **Frequency**: How often does this objection surface (or silently linger)?
- **Intensity**: How emotionally charged is this objection?
- **Timing**: Does it appear early (prevents engagement) or late (prevents purchase)?
- **Destructiveness**: Does it undermine trust in the entire premise, or just one element?

Document the #1 Objection as a single, precise sentence in the ICA's own words.

## Step 4: Build the Audience Psychology Map (Boyd Framework)

Using the belief data from Step 3, construct a full **Audience Psychology Map™** across six dimensions:

### 1. Current State (Situation & Symptoms)
- What is the ICA's day-to-day reality right now?
- What specific, observable symptoms are they experiencing? (not abstract — tangible, daily friction)
- What language do they use to describe their situation? (exact phrases from surveys, calls, reviews)

### 2. Emotional Undercurrent
- **Surface emotions**: Frustration, overwhelm, confusion, impatience (what they'll openly admit)
- **Deeper emotions**: Shame, fear of irrelevance, jealousy, inadequacy (what they feel but rarely say)
- **Identity threat**: How does their current situation conflict with who they believe they should be?

### 3. Failed Attempts & Scar Tissue
- What has the ICA already tried that didn't work?
- What conclusions did they draw from those failures? (These become the false beliefs above)
- What is their current cynicism level toward new solutions? (1–10 with rationale)

### 4. Decision Filters
- Who or what influences their purchasing decisions? (mentors, peers, spouse, online communities)
- What proof format do they find most credible? (data, testimonials, live demos, case studies, credentials)
- What is their default decision-making style? (analytical, emotional, social-proof-driven, authority-driven)

### 5. Desired Future State
- Describe the ICA's ideal outcome in vivid, sensory language
- What would change in their daily routine, relationships, identity, and status?
- What would they be able to say, do, or stop doing?

### 6. Purchase Anxiety Triggers
- What specific fears activate at the moment of purchase? (wasting money, looking foolish, commitment, past buyer's remorse)
- What post-purchase scenario are they most afraid of?
- What guarantee, reversal, or safety net would neutralise this anxiety?

## Step 5: Deliver Output

Produce the **Audience Belief & Psychology Map** — a single structured document containing:

### Deliverable 1: Belief Map Summary (1-Page Reference)

| Dimension | Key Finding |
|---|---|
| Dominant Desire | [One sentence] |
| #1 Vehicle False Belief | [ICA's words] |
| #1 Internal False Belief | [ICA's words] |
| #1 External False Belief | [ICA's words] |
| #1 Conversion-Killing Objection | [ICA's words] |
| Core Emotional Undercurrent | [Feeling + identity threat] |
| Cynicism Level | [1–10 + rationale] |
| Primary Decision Filter | [Proof format + influence source] |
| Purchase Anxiety Trigger | [Specific fear] |

### Deliverable 2: Full Belief Inventory

The complete tables from Step 3B with all identified false beliefs, narratives, origins, and required evidence — formatted for direct use in webinar script development.

### Deliverable 3: Audience Psychology Map

The complete six-dimension map from Step 4, written in presentation-ready language that can be shared with copywriters, co-presenters, or team members.

### Deliverable 4: Script Architecture Recommendations

Based on the mapped psychology, provide:
- **Recommended Epiphany Bridge stories** — For each of the three belief categories, describe the type of story (protagonist, conflict, resolution) that would most effectively break the false belief
- **Objection destruction sequence** — The optimal order in which to address objections throughout the webinar, with rationale tied to emotional arc
- **Proof stack prescription** — Which specific types of proof (case study, data point, demonstration, testimonial, credential) should appear at which points in the script, matched to decision filters
- **Language bank** — 10–15 exact phrases, words, and metaphors to use throughout the script that mirror the ICA's internal dialogue

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="audience-belief-mapper", experiment={
  hypothesis: "Addressing the #1 objection within the first 8 minutes of the webinar (rather than in the close) reduces early drop-off and increases offer-reveal retention",
  variants: ["control: objection addressed during stack/close", "variant: objection addressed in opening origin story"],
  measurement: "Webinar retention rate at offer reveal and overall conversion rate across next 3 live presentations",
  expected_impact: "20% improvement in attendee retention past minute 15, 10% lift in offer conversion"
})
```

```
FutureProof:save_experiment(skill="audience-belief-mapper", experiment={
  hypothesis: "Using ICA's exact language from the mapped internal beliefs in ad copy and registration pages increases webinar registration rate",
  variants: ["control: current registration page copy", "variant: copy rewritten using belief map language bank"],
  measurement: "Registration page conversion rate over 1,000 visitors",
  expected_impact: "15–25% improvement in registration conversion"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="audience-belief-mapper",
  query="Current objection patterns, false belief structures, and purchase anxiety triggers for [ICA's industry/niche] audiences in 2024–2025, including shifts in buyer sophistication and scepticism toward webinar-based offers",
  reason="Ensure belief map reflects current audience psychology rather than outdated assumptions. Market sophistication shifts rapidly — beliefs mapped 6 months ago may no longer be primary blockers."
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="audience-belief-mapper", session={
  summary: "Mapped audience beliefs and psychology for [ICA segment] in preparation for [webinar/presentation topic] promoting [offer name]",
  key_findings: ["#1 conversion-killing objection: [stated objection]", "Dominant false belief category: [Vehicle/Internal/External]", "Cynicism level: [X/10] driven by [failed attempt pattern]", "Primary decision filter: [filter type]"],
  artifacts: ["Belief Map Summary", "Full Belief Inventory", "Audience Psychology Map", "Script Architecture Recommendations"],
  user_feedback: null
})
```