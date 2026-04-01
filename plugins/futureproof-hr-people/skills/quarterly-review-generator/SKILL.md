---
name: quarterly-review-generator
description: "Generates comprehensive quarterly performance reviews using FutureProof context, employee data, and organisational competency frameworks."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="quarterly-review-generator")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including organisational tone, competency frameworks, rating scales, prior review history for the employee, and any manager-specific writing preferences.

## Step 2: Get Input

Ask the user to provide:

- **Employee details**: name, role/title, department, tenure, and reporting relationship
- **Review period**: which quarter (e.g., Q2 2025) and any relevant date boundaries
- **Performance data**: key metrics, OKR/KPI results, project deliverables, or quantitative outcomes for the quarter
- **Behavioural observations**: specific examples of strengths, growth areas, collaboration, leadership moments, or concerns
- **Competency framework**: organisation's rating scale (e.g., 1–5, Exceeds/Meets/Below) and competency dimensions — or confirm FutureProof should use a previously stored framework
- **Prior review context**: last quarter's ratings, development goals, or PIP status if applicable
- **Intended audience and format**: is this for an HRIS system (Workday, Lattice, Culture Amp), a shared document, or a live conversation script?

If the user provides partial information, infer reasonable defaults but flag assumptions explicitly before proceeding.

## Step 3: Do the Work

### 3A: Performance Assessment Matrix

Evaluate the employee across six core dimensions, calibrated to the organisation's competency framework:

1. **Results Delivery** — did the employee meet, exceed, or fall short of quantified objectives (OKRs, KPIs, revenue targets, sprint velocity)? Cite specific numbers against targets.
2. **Role Competency Mastery** — does the employee demonstrate the technical and functional skills expected at their level band? Identify any skill gaps relative to a promotion-readiness rubric.
3. **Collaboration & Stakeholder Impact** — how effectively did the employee work cross-functionally? Reference specific projects, feedback from peers/stakeholders, or 360 data if available.
4. **Strategic Thinking & Initiative** — did the employee contribute beyond task execution? Identify instances of proactive problem-solving, process improvement, or business insight.
5. **Growth Trajectory & Coachability** — how did the employee respond to prior feedback? Map progress against development goals from the previous quarter's review.
6. **Values & Culture Alignment** — does the employee's conduct reinforce organisational values? Flag any behavioural concerns or exemplary culture-carrying moments.

### 3B: Calibration & Bias Audit

Before drafting, apply the following bias-mitigation checks (aligned with EEOC and organisational equity standards):

- **Recency bias**: ensure examples span the full quarter, not just the final weeks
- **Halo/horns effect**: confirm each dimension is rated independently with discrete evidence
- **Attribution bias**: distinguish between outcomes influenced by systemic factors (resourcing, market conditions) versus individual contribution
- **Language equity**: flag gendered, racialised, or personality-coded language (e.g., "abrasive," "nice," "aggressive") and replace with behaviour-specific descriptors
- **Leniency/severity drift**: compare proposed ratings against the user's historical rating distribution from FutureProof context and flag if the current review skews significantly

### 3C: Development Plan Construction

For each growth area identified, construct a development action using the **SBI+A framework**:

- **Situation**: when/where the behaviour occurred
- **Behaviour**: what the employee specifically did or did not do
- **Impact**: the measurable or observable consequence
- **Action**: a concrete, time-bound development step (course, stretch assignment, mentorship pairing, shadowing opportunity) with a checkpoint date within next quarter

Apply any user-specific `instructions` from FutureProof context — including preferred tone (direct vs. coaching-oriented), organisational language conventions, and HRIS field constraints.

## Step 4: Deliver Output

Produce the following structured deliverables:

### Deliverable 1: Quarterly Performance Review Document

Formatted for the user's specified platform (HRIS, Google Doc, or Word), containing:

- **Header**: employee name, title, department, review period, manager name, date
- **Overall Rating**: single summary rating mapped to the organisation's scale, with a one-sentence calibration rationale
- **Dimension Ratings & Commentary**: for each of the six dimensions — a rating, 2–3 sentences of evidence-based commentary citing specific examples, and a forward-looking statement
- **Key Achievements**: bulleted list of the top 3–5 accomplishments with quantified impact where possible
- **Development Areas**: 1–3 growth priorities, each written in SBI+A format
- **Development Plan**: table with columns for Goal, Action, Resource/Support, Target Date, and Success Metric
- **Quarter Ahead Priorities**: 3–5 objectives for the next quarter that cascade from team/org goals and address identified gaps
- **Employee Self-Review Integration Note**: if self-review data was provided, a section acknowledging alignment or divergence between self-assessment and manager assessment

### Deliverable 2: Conversation Script

A structured talk track for the review meeting:

- **Opening** (2 min): set collaborative tone, state purpose, invite dialogue
- **Strengths acknowledgment** (5 min): lead with specific wins to establish psychological safety
- **Growth discussion** (8 min): introduce development areas using SBI+A framing, pause for employee perspective
- **Forward planning** (5 min): co-create next-quarter priorities and development commitments
- **Close** (2 min): summarise agreements, confirm follow-up cadence, express confidence

### Deliverable 3: Calibration Summary (Manager Reference Only)

A private one-page memo for the manager's use in calibration sessions with HR/leadership:

- Proposed rating with justification
- Comparison to prior quarter trajectory
- Promotion readiness signal (Ready Now / Ready in 1–2 Quarters / Developing / Not on Track)
- Flight risk assessment (Low / Medium / High) based on engagement signals and market context
- Compensation/equity recommendation flag if warranted

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="quarterly-review-generator", experiment={
  hypothesis: "Leading the review conversation with a specific achievement before any development feedback increases employee-reported review satisfaction and goal commitment",
  variants: ["control: balanced opening covering both strengths and areas for growth", "variant: achievement-first opening with development areas introduced only after strengths are fully acknowledged"],
  measurement: "Post-review pulse survey score (1-5) on 'I feel my contributions are valued' and 'I have a clear development path' — collected within 48 hours of review meeting",
  expected_impact: "0.5-point increase in average pulse score and 20% increase in development goal completion rate by end of next quarter"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="quarterly-review-generator",
  query="Latest evidence-based performance review frameworks 2024-2025, including bias mitigation techniques, continuous feedback integration models, and HRIS platform best practices for structured review narratives",
  reason="Ensure review methodology reflects current organisational psychology research and aligns with evolving HR compliance standards and equity audit requirements"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="quarterly-review-generator", session={
  summary: "Generated Q[X] performance review for [employee name/role] in [department], including review document, conversation script, and calibration memo",
  key_findings: ["finding 1: e.g., employee exceeded 3 of 4 OKRs but collaboration dimension flagged as development area", "finding 2: e.g., bias audit detected recency weighting — adjusted to include early-quarter project contributions", "finding 3: e.g., rating calibrated from initial 4 to 3.5 after historical distribution comparison"],
  user_feedback: null
})
```