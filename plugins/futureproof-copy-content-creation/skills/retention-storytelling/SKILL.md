---
name: retention-storytelling
description: "Crafts narrative-driven retention content that reduces churn and deepens customer commitment using story architecture, behavioural psychology, and ICA-specific emotional triggers."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="retention-storytelling")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any known ICA segments, churn triggers, product milestones, and brand voice guidelines.

## Step 2: Get Input

Ask the user:
- **Retention asset type**: What are you creating? (onboarding sequence, win-back email, renewal narrative, loyalty campaign, milestone celebration, feature adoption story, community nurture content)
- **ICA segment**: Who is this for? Share any persona details, lifecycle stage, and known churn risk factors
- **Churn context**: What behaviour or signal is triggering this need? (drop-off after trial, usage decline at Day 30, upcoming renewal, support ticket escalation, competitor consideration)
- **Transformation proof**: What measurable outcomes have successful retained customers achieved? Share case studies, testimonials, or internal data if available
- **Emotional baseline**: What is the customer likely *feeling* right now? (buyer's remorse, overwhelm, plateau frustration, neglect, curiosity fatigue)
- **Channel and format**: Where will this content appear? (email, in-app message, SMS, direct mail, video script, community post)

## Step 3: Map the Retention Story Architecture

Build the narrative framework using a **six-layer retention story model**:

### 3a. Diagnose the Churn Narrative

Identify the **competing story** the customer is telling themselves that leads to disengagement. This is the story you must displace. Common archetypes:

| Churn Archetype | Internal Customer Narrative | Story Intervention Required |
|---|---|---|
| Buyer's Remorse | "I made a mistake choosing this." | Origin validation — retell why they chose correctly |
| Plateau Effect | "I've gotten everything I can from this." | Horizon expansion — reveal the next level of value |
| Complexity Abandonment | "This is too hard to use properly." | Simplicity reframe — show the smallest next step |
| Invisibility | "They don't care about me." | Recognition — prove they are seen and valued |
| Opportunity Cost | "Something better exists." | Sunk-cost reframe + future-state contrast |
| Drift | "I just forgot about it." | Pattern interrupt — re-anchor to original pain |

Select the dominant churn archetype and one secondary archetype based on user input.

### 3b. Construct the Retention Narrative Arc

Apply the **Identity–Friction–Momentum (IFM) story framework**:

1. **Identity Anchor** — Open by reflecting back who the customer has *become* since starting. Use language that reinforces their self-image as someone who made a smart decision. Reference a specific milestone or behaviour ("You've already [specific action] — that puts you in the top X% of [ICA segment]").

2. **Friction Acknowledgement** — Name the exact feeling or obstacle they are experiencing *before they articulate it*. This builds trust through radical empathy. Do not minimise — validate. ("Around this point, most [ICA role] hit a wall where [specific friction]. That's not failure — it's the threshold before the shift.")

3. **Proof Bridge** — Introduce a specific customer story (real or composite) of someone in their ICA segment who faced the identical friction point and broke through. Structure this micro-story as: *Situation identical to reader → moment of doubt → small specific action taken → measurable outcome achieved*.

4. **Momentum Mechanic** — Prescribe exactly one next action that is low-effort and high-signal. Connect this action directly to the transformation in the proof bridge. Frame it as continuation, not restart.

5. **Future-State Contrast** — Paint two futures: the vivid, specific future where they continue (with sensory and emotional detail) versus the unnamed, vague alternative of stopping. Apply loss aversion — make the cost of leaving concrete.

6. **Belonging Close** — End by placing the customer inside a community or cohort narrative. They are not alone; they are part of a group moving toward something. Include a specific, personal sign-off element.

### 3c. Apply Behavioural Retention Triggers

Layer the following psychological mechanisms into the narrative at specific points:

- **Endowed Progress Effect** (Identity Anchor): Show progress already made — never start from zero
- **Implementation Intention** (Momentum Mechanic): Use "When X happens, you will Y" phrasing
- **Social Proof Specificity** (Proof Bridge): Name cohort size, percentage, or specific individual — never generic "many customers"
- **Peak-End Rule** (Belonging Close): Ensure the final emotional beat is the strongest
- **Commitment Consistency** (throughout): Reference past actions and decisions to reinforce continued engagement

### 3d. Voice Calibration

Using FutureProof context and user input, calibrate the narrative voice across three spectrums:

- **Warmth ↔ Authority** (scale 1–10): Retention content skews warmer than acquisition — default to 7 warmth / 5 authority unless brand voice dictates otherwise
- **Urgency ↔ Patience** (scale 1–10): Match to churn archetype — Drift requires urgency (8); Plateau requires patience (3)
- **Personal ↔ Institutional** (scale 1–10): Earlier lifecycle stages require personal (8); renewal content can be more institutional (5)

Apply any user-specific `instructions` from FutureProof context — particularly brand voice, tone restrictions, compliance language, and banned phrases.

## Step 4: Deliver Output

Produce a **Retention Storytelling Brief** containing:

### A. Strategic Narrative Summary
- **Churn archetype diagnosed** (primary and secondary)
- **Emotional state map**: where the customer is now → where the story takes them
- **Core narrative thesis**: one sentence that captures the story's persuasive logic

### B. Full Retention Narrative Draft
- Complete, publish-ready copy for the specified channel and format
- Annotated with inline notes identifying each IFM framework layer and behavioural trigger
- Word count calibrated to channel (email: 150–350 words; in-app: 40–80 words; video script: 60–90 seconds; SMS: under 160 characters with link)

### C. Subject Line / Hook Variants (if applicable)
- 5 subject lines or opening hooks, each employing a different psychological angle:
  1. Curiosity gap
  2. Identity reinforcement
  3. Loss aversion
  4. Social proof
  5. Pattern interrupt

### D. Sequence Architecture (if multi-touch)
- Recommended cadence with send triggers (time-based and behaviour-based)
- Narrative arc across messages — how the story evolves across touches
- Escalation logic: when to shift from nurture tone to urgency tone

### E. Measurement Framework
- **Leading indicators**: open rate, click-through, feature re-engagement within 48 hours
- **Lagging indicators**: 30-day retention lift, renewal conversion, NPS shift
- **Story-specific metric**: one custom metric tied to the narrative's core action (e.g., "% of recipients who complete the prescribed next step within 7 days")

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="retention-storytelling", experiment={
  hypothesis: "Leading with identity anchor ('You've already achieved X') outperforms leading with pain re-activation ('Remember when you struggled with Y') for [ICA segment] at [lifecycle stage]",
  variants: ["control: pain-first opening per current sequence", "variant: identity-anchor opening with endowed progress framing"],
  measurement: "click-through rate and 14-day retention rate across cohort of 500+ recipients",
  expected_impact: "20% improvement in click-through; 8% improvement in 14-day retention for targeted churn-risk segment"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="retention-storytelling",
  query="Latest behavioural science research on narrative-driven retention interventions, subscription churn psychology, and story-based onboarding effectiveness 2024–2025",
  reason="Update the IFM story framework with emerging evidence on endowed progress, identity-based habit formation, and optimal re-engagement timing across digital channels"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="retention-storytelling", session={
  summary: "Created retention storytelling asset ([asset type]) targeting [ICA segment] at [lifecycle stage] to address [churn archetype]",
  key_findings: ["Primary churn narrative identified as [archetype]", "IFM framework applied with [specific behavioural triggers]", "Recommended [number]-touch sequence with [cadence] timing"],
  user_feedback: null
})
```