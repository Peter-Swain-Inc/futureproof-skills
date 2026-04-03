---
name: offer-stack-builder
description: |
  Builds strategically sequenced bonus stacks that create an overwhelming perceived-value-to-price gap, using Hormozi's Trimming & Stacking method and Brunson's offer stacking framework from Expert Secrets.
  Trigger: when a user asks to build a bonus stack, create an offer stack, increase perceived value of an offer, or wants to engineer a value gap between what they deliver and what they charge.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="offer-stack-builder")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to previously defined ICA profiles, existing offers, price points, known objections, and any past offer-stack experiments and their results.

## Step 2: Get Input

Ask the user to provide the following (adapt based on what FutureProof context already supplies):

1. **Core offer definition** — What is the primary offer being sold? What transformation does it deliver? What is the current or intended price point?
2. **ICA profile** — Who is the ideal customer? What is their current painful state (Problem → Frustration → Emotion) and desired dream outcome?
3. **Known objections** — What are the top reasons qualified prospects say no or hesitate? (If unknown, state that — we will derive them.)
4. **Existing bonuses** — Are there any bonuses already in use? If so, list them with any assigned values.
5. **Delivery constraints** — What formats are viable? (digital courses, templates, software tools, live sessions, physical items, access/community, done-for-you services)
6. **Competitive landscape** — What do competing offers include at a similar or higher price point?

If the user cannot supply objections, proceed to Step 3a to derive them before building the stack.

## Step 3: Audit & Derive the Objection Map

### Step 3a: Objection Derivation (Hormozi's Four Value Drivers)

Using the ICA profile and core offer, systematically identify objections across the four perceived-value levers:

| Value Driver | Core Question the ICA Asks | Objection Category |
|---|---|---|
| **Dream Outcome** | "Will this actually get me the result?" | Scepticism about the promised transformation |
| **Perceived Likelihood of Achievement** | "Will it work for someone like *me*?" | Self-doubt, uniqueness bias, lack of proof |
| **Time Delay** | "How long until I see results?" | Impatience, opportunity cost, delayed gratification |
| **Effort & Sacrifice** | "How hard is this going to be?" | Complexity, overwhelm, lifestyle disruption |

For each driver, generate 2–4 specific, verbatim-style objections the ICA would voice. Rank them by frequency and deal-killing severity (Critical / High / Medium).

### Step 3b: Existing Bonus Audit (Trim Before You Stack)

If the user has existing bonuses, evaluate each against the **Strategic Purpose Test**. Every bonus must satisfy at least one of the following roles:

- **Objection Neutraliser** — Directly eliminates a specific, named objection from the map
- **Quick-Win Accelerator** — Delivers a tangible, visible result within 24–72 hours of purchase to cement buyer confidence
- **Perceived-Value Inflator** — Has a credible standalone market value that widens the value gap (e.g., a tool, template, or resource the ICA would otherwise pay for separately)
- **Adjacent Problem Solver** — Resolves a problem one step upstream or downstream of the core offer, making the core transformation more achievable

Bonuses that fail all four criteria are flagged as **filler** and recommended for removal. Bonuses that overlap in purpose are flagged as **redundant** and recommended for consolidation.

## Step 4: Engineer the Bonus Stack

### Step 4a: Strategic Bonus Design

For each Critical and High-severity objection remaining unaddressed after the audit, design a purpose-built bonus using the following specification:

**Bonus Design Card:**

| Field | Detail |
|---|---|
| **Bonus Name** | A benefit-driven, standalone-worthy name (e.g., "The 48-Hour Quick Start Launchpad" not "Getting Started Guide") |
| **Strategic Role** | Objection Neutraliser / Quick-Win Accelerator / Perceived-Value Inflator / Adjacent Problem Solver |
| **Target Objection** | The exact objection from the map this bonus neutralises (verbatim) |
| **What It Is** | Concrete deliverable description (format, length, contents) |
| **Why It Matters to the ICA** | One sentence connecting the bonus to the ICA's emotional state or dream outcome |
| **Standalone Value Justification** | How the assigned dollar value is anchored — market comparables, cost-to-create, or replacement cost the ICA would otherwise pay |
| **Assigned Value** | Dollar amount with anchoring rationale |
| **Delivery Timing** | Immediate / Day 1 / Week 1 / Ongoing |

### Step 4b: Stack Sequencing (Brunson's Offer Stack Architecture)

Arrange the complete stack in presentation order following Brunson's escalation framework:

1. **Core Offer** — Restate the primary transformation and its value
2. **Quick-Win Bonus** — The fastest-result bonus goes first to collapse time-delay objections and trigger immediate buyer momentum
3. **Objection-Neutralising Bonuses** — Ordered from most critical to least critical objection addressed
4. **Perceived-Value Inflators** — High-dollar-value items that widen the gap dramatically
5. **Adjacent Problem Solvers** — "We thought of everything" bonuses that demonstrate thoroughness
6. **Scarcity/Urgency Bonus** — (If applicable) A time-limited or quantity-limited bonus positioned last to drive decision compression

### Step 4c: Value Gap Calculation

Produce the **Value Gap Summary Table**:

| Stack Element | Assigned Value | Strategic Role |
|---|---|---|
| Core Offer | $X,XXX | Primary transformation |
| Bonus 1: [Name] | $X,XXX | [Role] → neutralises "[objection]" |
| Bonus 2: [Name] | $X,XXX | [Role] → neutralises "[objection]" |
| ... | ... | ... |
| **Total Perceived Value** | **$XX,XXX** | |
| **Price** | **$X,XXX** | |
| **Value Gap Ratio** | **X:1** | Target: 10:1 minimum |

If the value gap ratio falls below 10:1, recommend specific additions or value-reassignments to reach the threshold.

## Step 5: Deliver Output

Produce the following structured deliverables:

### Deliverable 1: Objection Map
A prioritised table of ICA objections across all four value drivers, ranked by severity, with current coverage status (addressed / unaddressed).

### Deliverable 2: Bonus Stack Blueprint
The complete set of Bonus Design Cards (from Step 4a) in presentation sequence (from Step 4b), ready for use in sales pages, webinar slides, or VSL scripts.

### Deliverable 3: Value Gap Summary
The Value Gap Summary Table with total perceived value, price, ratio, and a confidence assessment (Conservative / Moderate / Aggressive) on the value anchoring.

### Deliverable 4: Stack Presentation Script
A ready-to-use narration script for verbally presenting the stack in a webinar, sales call, or VSL — following Brunson's "But wait, that's not all..." escalation cadence. Each bonus introduction includes:
- The objection it handles (framed as an ICA concern)
- What the bonus is and its standalone value
- A transition line to the next bonus

### Deliverable 5: Trim Report (if existing bonuses were audited)
A list of removed or consolidated bonuses with rationale for each decision.

Apply any user-specific `instructions` from FutureProof context (e.g., brand voice, ICA segment nuances, preferred pricing psychology) to all deliverables.

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="offer-stack-builder", experiment={
  hypothesis: "Reordering the bonus stack to lead with the Quick-Win Accelerator bonus before Objection Neutralisers will increase conversion by reducing early-stage time-delay anxiety",
  variants: [
    "control: current stack presentation order",
    "variant A: Quick-Win Accelerator positioned as Bonus #1 with explicit '48-hour result' language",
    "variant B: Quick-Win Accelerator positioned as Bonus #1 with added social proof screenshot of fast result"
  ],
  measurement: "Sales page or webinar conversion rate over next 500 qualified impressions",
  expected_impact: "8–15% improvement in offer-to-purchase conversion rate"
})
```

```
FutureProof:save_experiment(skill="offer-stack-builder", experiment={
  hypothesis: "Removing the lowest-performing filler bonus and replacing it with a targeted Objection Neutraliser for the #1 deal-killing objection will improve close rate without increasing fulfilment cost",
  variants: [
    "control: current stack with existing bonus lineup",
    "variant: trimmed stack with new purpose-built Objection Neutraliser"
  ],
  measurement: "Close rate and post-purchase refund rate over 30 days",
  expected_impact: "5–10% close rate increase with stable or improved refund rate"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="offer-stack-builder",
  query="Current high-converting bonus stack structures in [user's niche/industry], including standalone bonus value benchmarks, most effective bonus formats (templates vs. tools vs. access vs. done-for-you), and emerging buyer objection patterns 2024–2025",
  reason="Ensure bonus design, value anchoring, and objection mapping reflect current market expectations and competitive stacking norms for the user's ICA segment"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="offer-stack-builder", session={
  summary: "Built bonus stack for [core offer name] targeting [ICA segment] at [$price point]. Achieved [X:1] value gap ratio with [N] strategically purposed bonuses.",
  key_findings: [
    "Top deal-killing objection identified: [objection]",
    "Value gap ratio achieved: [X:1] — [above/below] 10:1 threshold",
    "Bonuses trimmed as filler: [N]",
    "Recommended lead bonus for stack presentation: [Bonus Name]"
  ],
  artifacts: [
    "Objection Map",
    "Bonus Stack Blueprint ([N] Bonus Design Cards)",
    "Value Gap Summary Table",
    "Stack Presentation Script",
    "Trim Report"
  ],
  user_feedback: null
})
```