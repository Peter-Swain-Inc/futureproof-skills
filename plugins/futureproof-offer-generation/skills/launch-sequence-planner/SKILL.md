---
name: launch-sequence-planner
description: |
  Plans and sequences offer launches using Jeff Walker's Product Launch Formula and Brunson's Hook-Story-Offer framework, drawing on accumulated FutureProof context to personalise every phase.
  Trigger: when a user says "plan my launch," "I need a launch sequence," "how do I launch this offer," or shares a completed offer and asks what the go-to-market plan should be.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="launch-sequence-planner")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to:
- Existing ICA profiles, offer stack definitions, and pricing from prior sessions
- Any previous launch results or conversion benchmarks stored in `experiments`
- User-specific `instructions` (e.g., preferred launch cadence, list size constraints, platform preferences)

## Step 2: Get Input

Ask the user to provide or confirm the following — pre-populate from FutureProof context where available:

1. **The Offer**: What is the offer being launched? (Link to a prior offer-generation session or describe the core offer, price point, and transformation promise.)
2. **Launch Type**: Which launch model fits their situation?
   - **Seed Launch** — small list (<500), validating a new offer for the first time
   - **Internal Launch** — existing list/audience, launching to people who already know them
   - **JV Launch** — leveraging partner audiences for scale
   - **Evergreen Launch** — automated, perpetual funnel after a proven live launch
3. **ICA Snapshot**: Who is the primary ICA? (Pull from FutureProof context or ask for demographics, psychographics, current pain state, desired future state.)
4. **Audience Size & Warmth**: Current list size, engagement rate, and how recently the audience has been nurtured.
5. **Launch Window**: Target cart-open date and any hard deadlines (event dates, seasonal relevance, cohort start dates).
6. **Available Assets**: What does the user already have? (Email list, social following, podcast, blog, ad budget, JV partners, testimonials, case studies.)
7. **Constraints**: Budget ceiling, team capacity, tech stack limitations.

## Step 3: Do the Work — Launch Architecture

### 3A: Define the Sideways Sales Letter Structure

Map the entire launch sequence as a **Sideways Sales Letter** (Walker's PLF framework) — the sales argument is delivered horizontally across multiple content pieces rather than vertically in one long page:

| Sequence Phase | Purpose | Duration |
|---|---|---|
| **Pre-Pre-Launch** | Seed curiosity, surface the opportunity/problem, begin identity shift | 7–14 days before PLC1 |
| **PLC 1 — The Opportunity** | Establish the transformational opportunity; position the ICA's problem as solvable | Day 0 of pre-launch |
| **PLC 2 — The Transformation** | Teach a micro-win; demonstrate authority; deliver proof of concept | Day 3–5 |
| **PLC 3 — The Ownership Experience** | Collapse objections; show what life looks like post-purchase; intensify desire | Day 6–8 |
| **Cart Open** | Present the offer with full stack, bonuses, and urgency/scarcity triggers | Day 9 |
| **Cart Open Window** | Conversion-driving email/content sequence with social proof escalation | Days 9–14 (typically 5–7 days) |
| **Cart Close** | Final urgency sequence — last-chance messaging, FAQ, objection handling | Final 48 hours |
| **Post-Close** | Waitlist capture, buyer onboarding, debrief & data collection | Day 15+ |

For each phase, specify:
- **Content format** (video, email, live stream, social post, webinar)
- **Core narrative beat** (the single argument that phase must win)
- **Proof asset** (testimonial, case study, data point, demonstration) to deploy
- **Engagement mechanic** (comment prompt, quiz, reply trigger, share incentive)

### 3B: Apply Hook-Story-Offer to Every Touchpoint

For each major content piece and email in the sequence, articulate the **Brunson HSO triad**:

- **Hook**: The pattern-interrupt or curiosity mechanism that earns attention in the first 3 seconds / subject line / headline. Must be ICA-specific — reference the exact language, frustrations, or aspirations surfaced in the ICA profile.
- **Story**: The narrative vehicle — an Epiphany Bridge story, case study, or analogy — that creates emotional resonance and belief shift. Each PLC uses a different story archetype:
  - PLC 1 → Origin Story (how the creator discovered the opportunity)
  - PLC 2 → Transformation Story (a client/student result that proves the method)
  - PLC 3 → Ownership Story (what daily life looks like inside the programme/product)
- **Offer**: The micro- or macro-call-to-action appropriate to the phase (early phases: opt in, comment, share; cart-open phases: purchase with specific stack and urgency).

### 3C: Engineer Urgency & Scarcity Architecture

Define the specific, *ethical* urgency and scarcity levers for the launch:

1. **Deadline scarcity**: Cart close date/time (with rationale — cohort start, onboarding capacity, seasonal relevance)
2. **Bonus scarcity**: Time-limited bonuses that expire at defined milestones (e.g., fast-action bonus for first 48 hours)
3. **Quantity scarcity**: Enrolment caps tied to genuine delivery constraints (coaching bandwidth, community quality)
4. **Price scarcity**: Launch pricing vs. future pricing, with specific numbers and escalation timeline

For each lever, document the **justification** (why it is real, not manufactured) and **messaging language**.

### 3D: Build the Email Sequence Calendar

Produce a day-by-day email calendar covering the full launch window. Each email entry includes:

- **Day & Date** (relative to cart open)
- **Email Name** (descriptive internal label, e.g., "PLC2-Transformation-Story")
- **Subject Line** (draft — Hook-first)
- **Primary CTA**
- **Segmentation Logic** (e.g., "send to non-openers of PLC1 invite," "send only to cart-abandoners")
- **Emotional Temperature** (curiosity → excitement → urgency → FOMO → resolution)

Minimum email count benchmarks by launch type:
- Seed Launch: 8–12 emails
- Internal Launch: 14–20 emails
- JV Launch: 18–25 emails (including partner swipe copy)
- Evergreen Launch: 12–16 emails in the automated sequence

### 3E: Launch-Type-Specific Adjustments

Apply modifications based on the selected launch type:

- **Seed Launch**: Emphasise co-creation framing ("help me build this"), beta pricing, feedback loops, and founding-member identity. Reduce production polish; increase authenticity and personal access.
- **Internal Launch**: Full PLF sequence. Maximise segmentation. Include re-engagement sequence for dormant subscribers 14 days before pre-launch.
- **JV Launch**: Produce a **Partner Recruitment Kit** containing: partner invite email, sample swipe copy (3 emails minimum), affiliate link setup instructions, commission structure summary, promotional calendar with blackout dates, leaderboard/incentive tiers.
- **Evergreen Launch**: Define the **trigger event** that starts the sequence (opt-in, quiz completion, webinar registration). Map deadline logic (rolling deadlines using tools like Deadline Funnel). Specify the ongoing traffic strategy feeding the top of the evergreen funnel.

## Step 4: Deliver Output

Produce the following named deliverables:

### Deliverable 1: Launch Sequence Blueprint
A single-page visual timeline (described in structured table format) showing every phase, content piece, and email mapped across the full launch window with dates, owners (if team exists), and dependencies.

### Deliverable 2: Hook-Story-Offer Messaging Matrix
A table with one row per content piece / email, columns for Hook (headline/subject line), Story (narrative archetype and key beats), and Offer (CTA and stack element featured). Ready for the user or copywriter to draft from.

### Deliverable 3: Email Sequence Calendar
The day-by-day email plan from Step 3D, formatted as a table the user can import into their ESP or project management tool.

### Deliverable 4: Urgency & Scarcity Playbook
A concise reference document listing each scarcity/urgency lever, its justification, activation timing, and exact messaging language.

### Deliverable 5: Launch-Type Addendum
Specific to the chosen launch type — for JV launches, this is the Partner Recruitment Kit; for Evergreen, the Automation Logic Map; for Seed, the Feedback Loop Plan; for Internal, the Segmentation & Re-engagement Strategy.

### Deliverable 6: Launch KPI Dashboard Template
Define the key metrics to track across each phase:
- **Pre-launch**: opt-in rate, PLC view-through rate, engagement rate (comments, replies), list growth
- **Cart open**: sales page conversion rate, cart abandonment rate, revenue per email sent, average order value
- **Cart close**: final conversion rate, refund rate (30-day), revenue vs. target, cost per acquisition
- **Post-close**: waitlist sign-up rate, testimonial collection rate, NPS / buyer satisfaction

Include target benchmarks calibrated to the user's audience size and launch type.

Apply any user-specific `instructions` from FutureProof context to adjust tone, format, or emphasis across all deliverables.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="launch-sequence-planner", experiment={
  hypothesis: "Leading PLC1 with a contrarian hook that challenges the ICA's current belief about [core problem] increases PLC1 view-through rate compared to a benefit-led hook",
  variants: ["control: benefit-led PLC1 hook", "variant: contrarian/myth-busting PLC1 hook"],
  measurement: "PLC1 video/page view-through rate and PLC1-to-PLC2 progression rate",
  expected_impact: "20% increase in PLC1 completion, 10% lift in PLC2 opt-in"
})
```

```
FutureProof:save_experiment(skill="launch-sequence-planner", experiment={
  hypothesis: "Adding a 24-hour fast-action bonus at cart open increases first-day purchase rate without cannibalising later-window sales",
  variants: ["control: standard cart-open sequence without time-limited bonus", "variant: cart-open with 24-hour exclusive bonus"],
  measurement: "Day-1 purchase rate as percentage of total launch revenue; total launch revenue comparison",
  expected_impact: "30% of total revenue captured in first 24 hours vs. typical 20%, with no decrease in total revenue"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="launch-sequence-planner",
  query="Latest conversion benchmarks for PLF-style launches segmented by list size, price point, and niche (2023–2025). Include emerging trends in launch fatigue mitigation and interactive pre-launch content formats (quizzes, challenges, AI-personalised sequences).",
  reason="Calibrate KPI targets to current market conditions and incorporate new pre-launch engagement mechanics that counteract audience desensitisation to traditional launch sequences"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="launch-sequence-planner", session={
  summary: "Built [launch type] sequence for [offer name] targeting [ICA segment] with cart-open on [date]. Produced Launch Sequence Blueprint, HSO Messaging Matrix, Email Calendar ([X] emails), Urgency Playbook, Launch-Type Addendum, and KPI Dashboard.",
  key_findings: ["finding 1: e.g., list warmth is low — added 14-day re-engagement pre-sequence", "finding 2: e.g., strongest scarcity lever is cohort-start deadline, not price discount", "finding 3: e.g., ICA language audit revealed mismatch between current copy tone and ICA vocabulary"],
  user_feedback: null
})
```