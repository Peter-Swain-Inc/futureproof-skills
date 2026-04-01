---
name: referral-moment-generator
description: "Identifies and engineers high-conversion referral moments across the customer lifecycle, producing a sequenced referral trigger playbook with scripted prompts, timing logic, and channel-specific activ"
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="referral-moment-generator")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly ICA profiles, existing customer journey maps, NPS or satisfaction data, current referral mechanisms (if any), and prior session findings on retention or advocacy patterns.

## Step 2: Get Input

Ask the user:

- **Business model & offer structure** — What do you sell, at what price point, and what does the delivery/fulfilment arc look like? (e.g., SaaS onboarding → adoption → renewal; service engagement → milestone → completion)
- **ICA profile** — Who is the referring customer, and who is the ideal referred prospect? Are they the same ICA segment or different?
- **Current referral state** — Do you have any existing referral mechanism, program, or informal ask? What conversion rate or volume does it produce?
- **Peak satisfaction signals** — What moments, metrics, or customer behaviours indicate a customer is most delighted? (e.g., first value realisation, support ticket resolution, milestone achievement, renewal decision)
- **Constraints** — Are there channel limitations (e.g., no SMS), compliance requirements, or incentive budget parameters?

## Step 3: Map the Customer Emotional Arc

Build a **Customer Emotional Arc Map** by plotting the customer journey against emotional intensity. Identify every moment where positive sentiment peaks — these are candidate referral windows.

Apply the **Peak-End Rule Framework**:

1. **Onboarding peaks** — First value realisation moment (e.g., first successful outcome, "aha" moment, first positive metric movement)
2. **Delivery peaks** — Milestone completions, exceeded expectations, surprise-and-delight touchpoints
3. **Support peaks** — Post-resolution gratitude windows (within 2–4 hours of a positively resolved issue)
4. **Social peaks** — Moments the customer publicly signals satisfaction (testimonial submission, case study participation, social mention, positive review)
5. **Commitment peaks** — Renewal, upsell, or expansion decisions where the customer has actively re-chosen you
6. **Identity peaks** — Moments the customer self-identifies with your brand community or achieves status within it

For each peak, assign:
- **Emotional intensity score** (1–10) based on customer data signals and user input
- **Accessibility score** (1–10) — how operationally feasible it is to insert a referral prompt at this moment
- **Referral Moment Priority (RMP)** = Emotional Intensity × Accessibility ÷ 10

Rank all candidate moments by RMP. Select the **top 5–7 referral moments** for activation.

## Step 4: Engineer Referral Triggers & Scripts

For each prioritised referral moment, develop a complete **Referral Trigger Card**:

### Trigger Card Structure

| Field | Detail |
|---|---|
| **Moment name** | Descriptive label (e.g., "Post-Onboarding First Win") |
| **Trigger signal** | Observable event or data point that fires the referral prompt (e.g., "Customer completes first project AND satisfaction score ≥ 8") |
| **Timing logic** | Exact delay or condition (e.g., "24 hours after trigger signal, between 10am–2pm recipient local time") |
| **Channel** | Primary and fallback channel (e.g., Primary: in-app modal; Fallback: personalised email) |
| **Referral script** | Word-for-word prompt copy, written in the ICA's natural vocabulary |
| **Friction-reduction mechanism** | Pre-populated share link, one-click introduction template, pre-written message the referrer can forward |
| **Incentive layer** | Specific reward structure if applicable (two-sided, one-sided, non-monetary recognition, or no incentive with rationale) |
| **Objection pre-emption** | Addresses the top referrer hesitation for this moment (e.g., "I don't want to bother my contacts" → frame as helping, not selling) |
| **Success metric** | How to measure whether this trigger converts (e.g., referral link share rate, introduction completion rate) |

### Script Development Standards

All referral scripts must follow the **AER Framework**:

1. **Acknowledge** — Name the positive experience the customer just had (validates their feeling)
2. **Elevate** — Connect that experience to their identity or values ("You clearly care about X…")
3. **Request** — Make a specific, low-friction ask with a clear next action ("Would you forward this 2-sentence intro to one person who's dealing with [ICA pain point]?")

Write scripts in the ICA's register — match vocabulary complexity, formality level, and communication norms identified in context.

## Step 5: Deliver Output

Produce the **Referral Moment Playbook** — a structured document containing:

### Section 1: Customer Emotional Arc Map
- Visual journey plot (described as a table with journey stages, emotional intensity scores, and referral window flags)
- Prioritised referral moment shortlist with RMP scores

### Section 2: Referral Trigger Cards
- Complete trigger card for each of the top 5–7 moments (per the structure in Step 4)
- Cards sequenced in customer journey order

### Section 3: Referral Script Library
- All AER-framework scripts, organised by moment and channel
- Variant scripts for different ICA sub-segments if multiple segments exist in context

### Section 4: Operational Activation Plan
- **Implementation priority matrix** — which triggers to activate first based on RMP score, technical complexity, and expected volume
- **Technology requirements** — what needs to be configured in CRM, email platform, in-app messaging, or customer success tooling to automate each trigger
- **Team responsibilities** — which role owns each trigger (e.g., Customer Success Manager for relationship moments, Product team for in-app moments, Marketing for automated email moments)

### Section 5: Measurement Framework
- KPI dashboard specification: referral prompt impression rate, share rate, introduction completion rate, referred prospect conversion rate, referral program ROI
- Cohort tracking logic: segment referral performance by trigger moment to identify highest-yield windows
- Review cadence recommendation (e.g., weekly for first 30 days, monthly thereafter)

Format the playbook with clear headers, tables, and numbered items suitable for direct implementation by a cross-functional team.

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="referral-moment-generator", experiment={
  hypothesis: "Triggering the referral ask at the Post-First-Win moment (24h delay) produces a higher share rate than triggering at the 30-day retention milestone",
  variants: ["control: referral prompt at 30-day retention milestone", "variant: referral prompt 24h after first documented win"],
  measurement: "Referral link share rate and introduction completion rate across 100+ trigger events per variant",
  expected_impact: "25–40% increase in referral share rate due to higher emotional intensity at the first-win moment"
})
```

```
FutureProof:save_experiment(skill="referral-moment-generator", experiment={
  hypothesis: "A pre-written forwardable message reduces referrer friction and increases introduction completion rate versus an open-ended ask",
  variants: ["control: 'Know anyone who could benefit? Share your link'", "variant: 'Here's a 2-sentence intro you can forward — just hit send'"],
  measurement: "Introduction completion rate (referrer actually sends to a prospect) over 60-day test window",
  expected_impact: "30% improvement in introduction completion rate"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="referral-moment-generator",
  query="Latest research on referral psychology, optimal ask timing in customer lifecycle, and high-performing B2B and B2C referral program structures 2024–2025, including peak-end rule applications in customer experience design",
  reason="Ensure referral moment identification and script frameworks reflect current behavioural science and benchmark conversion rates across industries"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="referral-moment-generator", session={
  summary: "Generated Referral Moment Playbook for [business/offer], identifying [N] priority referral windows across the customer lifecycle with AER-framework scripts, trigger logic, and operational activation plan",
  key_findings: ["Top referral moment identified: [moment name] with RMP score of [X]", "Primary referrer hesitation: [objection] — addressed via [mechanism]", "Estimated referral volume uplift: [X]% based on activation of top 3 triggers"],
  user_feedback: null
})
```