---
name: proposal-writer
description: "Crafts high-conversion business proposals using FutureProof context, ICA intelligence, and proven persuasion architecture."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="proposal-writer")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly ICA definitions, past proposal win/loss data, pricing structures, brand voice guidelines, and any saved case studies or proof assets.

## Step 2: Get Input

Ask the user:
- **Proposal type**: New business proposal, RFP response, SOW, partnership pitch, or renewal proposal?
- **Recipient**: Who is the decision-maker and what organisation are they in? (Title, seniority, industry, company size)
- **Opportunity context**: What problem does the recipient need solved? Share any briefing documents, RFP requirements, discovery call notes, or email threads.
- **Scope & deliverables**: What are you proposing to deliver? Timeline, phases, and any known constraints.
- **Commercial parameters**: Budget range, pricing model preference (fixed, retainer, value-based, milestone), and any competitive dynamics (incumbent, competing bids).
- **Proof assets available**: Case studies, testimonials, certifications, team bios, or performance data they can reference.

## Step 3: Analyse the Opportunity

Before drafting, conduct a structured opportunity assessment:

1. **ICA fit scoring** — Rate alignment (1–10) between the recipient and the user's ICA across: budget authority, problem urgency, solution fit, and long-term value potential. Flag misalignment risks.
2. **Decision architecture mapping** — Identify the likely approval chain: economic buyer, technical evaluator, end user, and any gatekeepers. Note which sections of the proposal must speak to each.
3. **Competitive positioning analysis** — Based on context, determine the user's primary differentiator (speed, expertise, methodology, price, relationship, niche specialisation) and the most likely alternative the recipient is considering (competitor, in-house, do nothing).
4. **Win theme extraction** — Distil 2–3 win themes that thread through the entire proposal. A win theme connects a specific recipient pain point → the user's unique capability → a measurable outcome.
5. **Risk register** — Identify the top 3 objections or concerns the recipient is likely to raise and prepare pre-emptive responses to embed in the proposal body.

Present this assessment to the user for validation before proceeding to draft.

## Step 4: Draft the Proposal

Build the proposal using the following architecture, adapting section depth to proposal type:

### Section 1: Executive Summary (1 page maximum)
- Opening hook: Mirror the recipient's own language describing their challenge (drawn from discovery notes or RFP language)
- Situation–Complication–Resolution structure: current state → cost of inaction → proposed transformation
- Three win themes stated as outcome promises
- Single sentence on why the user is uniquely positioned to deliver
- Clear next step with specific date

### Section 2: Understanding of Requirements
- Restate the recipient's objectives in their own terminology — demonstrate deep listening
- Map stated requirements to unstated underlying goals (e.g., "migrate CRM" → "reduce sales cycle length by giving reps better pipeline visibility")
- Explicitly address any RFP evaluation criteria, matching the recipient's numbering and terminology

### Section 3: Proposed Approach & Methodology
- Phase-gated delivery plan with named phases, activities, milestones, and durations
- For each phase: objective, key activities, deliverables, recipient responsibilities, and decision gates
- Methodology rationale — why this approach over alternatives, with reference to similar engagements
- Risk mitigation: embed pre-emptive responses to the top 3 objections identified in Step 3

### Section 4: Proof & Credibility
- 2–3 case studies structured as: Challenge → Approach → Result (quantified)
- Select case studies by ICA proximity — closest industry, problem type, or company stage to the recipient
- Team bios for key delivery personnel, emphasising relevant credentials
- Relevant certifications, partnerships, or proprietary frameworks

### Section 5: Commercial Framework
- Investment summary table: deliverable, price, payment trigger
- Pricing model rationale tied to recipient value (not cost justification)
- ROI projection: conservative, expected, and optimistic scenarios with stated assumptions
- Payment terms and conditions

### Section 6: Next Steps & Call to Action
- Specific proposed action with a named date (e.g., "30-minute alignment call on [date]")
- What the user will provide upon agreement (kickoff pack, access requirements, team introductions)
- Validity period for the proposal

Apply any user-specific `instructions` from FutureProof context — brand voice, formatting standards, preferred document structure, or compliance requirements.

## Step 5: Deliver Output

Produce the following deliverables:

- **Proposal document** — Full draft following the architecture above, formatted with clear section headers, executive summary on page 1, and professional tone throughout. Ready for export to PDF or Google Docs.
- **Proposal scorecard** — Self-assessment rating (1–10) across:
  - ICA resonance (language mirrors recipient's world)
  - Win theme clarity (themes are specific, differentiated, and threaded throughout)
  - Proof density (every major claim backed by evidence)
  - Objection pre-emption (top 3 concerns addressed before they surface)
  - Commercial confidence (pricing positioned as investment, ROI made tangible)
  - Call-to-action friction (next step is specific, low-effort, and time-bound)
- **Strength/risk summary** — Top 3 strongest elements and top 3 areas where the proposal is vulnerable, with specific recommendations to shore up weaknesses
- **Submission checklist** — Compliance matrix confirming all RFP requirements addressed (if applicable), recommended reviewers, and suggested send time

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="proposal-writer", experiment={
  hypothesis: "Leading the executive summary with a quantified cost-of-inaction statement increases proposal-to-meeting conversion",
  variants: ["control: current executive summary opening with capability statement", "variant: open with recipient-specific cost-of-inaction figure derived from discovery data"],
  measurement: "Proposal-to-next-step conversion rate across next 10 proposals",
  expected_impact: "20% improvement in proposal-to-meeting conversion rate"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="proposal-writer",
  query="High-converting B2B proposal structures, executive summary frameworks, and pricing presentation strategies with win-rate data 2024–2025",
  reason="Continuously refine proposal architecture based on evolving buyer decision patterns and procurement psychology"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="proposal-writer", session={
  summary: "Drafted [proposal type] for [recipient name/org] targeting [primary objective]",
  key_findings: ["Win themes identified: [theme 1], [theme 2]", "Primary competitive risk: [risk]", "Proposal scorecard average: [X]/10"],
  user_feedback: null
})
```