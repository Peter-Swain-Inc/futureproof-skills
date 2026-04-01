---
name: customer-survey-designer
description: "Designs high-performance customer surveys that generate actionable insights, using FutureProof context to align question design with known ICA segments, business objectives, and prior feedback data."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="customer-survey-designer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any known ICA segments, previous survey response rates, identified pain points, and preferred survey distribution channels.

## Step 2: Get Input

Ask the user:

- **Survey objective**: What decision will this survey inform? (e.g., product improvement, churn reduction, service quality benchmarking, onboarding optimisation, renewal forecasting)
- **Target audience**: Which ICA segment(s) will receive this survey? What is their relationship stage? (new customer, active, at-risk, churned, post-support interaction)
- **Distribution method**: How will the survey reach respondents? (in-app, email, SMS, post-call IVR, embedded in support ticket closure)
- **Constraint parameters**: Maximum acceptable survey length, any regulatory or compliance requirements (e.g., GDPR consent language, accessibility standards), brand voice guidelines
- **Existing materials**: Any prior surveys, known response rate benchmarks, or specific questions they want included or avoided
- **Measurement framework**: Are they tracking against an established metric (NPS, CSAT, CES) or building a custom measurement model?

## Step 3: Do the Work

### 3A: Survey Architecture Design

Define the survey blueprint using a **Goal → Construct → Item** hierarchy:

1. **Business goal mapping** — trace each survey section back to a specific business decision or action trigger (e.g., "If score < 3 on Q7, route to retention team within 24 hours")
2. **Construct definition** — identify the latent constructs being measured (e.g., perceived value, effort friction, emotional loyalty, service competence) and ensure each construct has a minimum of 2 items for internal reliability
3. **Respondent journey flow** — sequence sections to mirror natural cognitive recall: experience recency first, evaluative judgements second, demographic/classification items last

### 3B: Question Engineering

Apply rigorous survey methodology to each item:

1. **Question type selection** — match each construct to the optimal measurement format:
   - Likert scales (agreement/frequency) for attitudinal constructs
   - Semantic differentials for brand perception
   - Single-select forced choice for behavioural classification
   - Open-text fields (maximum 2 per survey) positioned after their quantitative anchor question
   - Matrix grids only when attribute evaluation requires direct comparison (limit to 5 rows maximum to prevent satisficing)

2. **Bias mitigation audit** — review every item against the following threat checklist:
   - **Leading language**: remove directional phrasing ("How much did you enjoy…")
   - **Double-barrelled items**: split compound questions into discrete items
   - **Acquiescence bias**: include at least one reverse-coded item per construct
   - **Social desirability**: use indirect phrasing for sensitive topics (effort, dissatisfaction)
   - **Order effects**: randomise item presentation within sections where methodologically appropriate
   - **Scale anchoring**: ensure all scale endpoints are symmetrically labelled with concrete behavioural descriptors, not abstract intensifiers

3. **ICA language calibration** — rewrite all question stems and response options to match the vocabulary, reading level, and communication style of the target ICA segment (informed by FutureProof context on known ICA profiles)

4. **Response rate optimisation** — apply completion probability modelling:
   - Target total completion time under 3 minutes for transactional surveys, under 7 minutes for relational surveys
   - Front-load the single highest-value question (the "golden question") within the first 30 seconds
   - Implement smart branching logic to eliminate irrelevant paths and reduce perceived length
   - Design progress indicators that reflect cognitive effort, not just page count

### 3C: Actionability Framework

For each question, define:
- **Decision rule**: the specific threshold or pattern that triggers a business action
- **Owner**: the team or role responsible for acting on the signal
- **Response SLA**: the expected timeframe from signal detection to action

Apply any user-specific `instructions` from FutureProof context to override defaults (e.g., preferred scale formats, mandatory compliance language, banned question types).

## Step 4: Deliver Output

Produce the **Customer Survey Design Package** containing:

### 4A: Survey Specification Document

| Element | Detail |
|---|---|
| Survey title | Descriptive internal title and respondent-facing title |
| Objective statement | Single sentence linking survey to business decision |
| Target ICA segment(s) | With estimated population size and expected response rate |
| Distribution channel | With send timing recommendation |
| Estimated completion time | Based on item count and question complexity |

### 4B: Complete Question Bank

For each item, provide:
- **Item ID** (e.g., CSAT-Q01)
- **Construct measured**
- **Question text** (final, respondent-ready)
- **Response format** with exact scale labels
- **Branching logic** (if applicable)
- **Decision rule** (threshold → action → owner → SLA)

### 4C: Survey Flow Diagram

A structured text-based flowchart showing:
- Section sequence with estimated time per section
- Skip logic and conditional branching paths
- Termination points and thank-you screen variants (customised by response sentiment where applicable)

### 4D: Analysis Plan

- **Scoring methodology**: how raw responses translate to composite scores (weighted or unweighted, with justification)
- **Segmentation cuts**: which ICA attributes to cross-tabulate against
- **Statistical thresholds**: minimum sample sizes for significance, margin of error targets
- **Reporting cadence**: recommended frequency and dashboard metrics
- **Verbatim coding framework**: preliminary theme categories for open-text analysis

### 4E: Implementation Checklist

- Pre-launch: pilot test protocol (sample size, feedback loop, revision criteria)
- Launch: distribution timing, reminder cadence (recommended: Day 0, Day 3, Day 6)
- Post-launch: response rate monitoring triggers, non-response bias assessment method

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="customer-survey-designer", experiment={
  hypothesis: "Placing the golden question (overall satisfaction) as the first item rather than after contextual warm-up questions increases both completion rate and response validity for the target ICA segment",
  variants: ["control: warm-up sequence then golden question at position 4", "variant: golden question at position 1 followed by contextual items"],
  measurement: "Survey completion rate and response distribution variance across both variants over 500 responses per arm",
  expected_impact: "8-12% improvement in completion rate with no degradation in score distribution normality"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="customer-survey-designer",
  query="Latest evidence on optimal survey length, scale format effectiveness, and mobile-first survey design patterns for customer feedback in 2024-2025, including impact of AI-generated survey personalisation on response quality",
  reason="Ensure question design methodology reflects current respondent behaviour patterns, particularly declining attention spans and increasing mobile completion rates"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="customer-survey-designer", session={
  summary: "Designed [survey type] survey targeting [ICA segment] to inform [business decision], comprising [N] items across [N] constructs with [distribution channel] delivery",
  key_findings: ["finding 1: e.g., identified 3 constructs with no current measurement coverage", "finding 2: e.g., recommended branching logic reduces median completion time by 40%", "finding 3: e.g., prior survey contained 4 double-barrelled items requiring decomposition"],
  deliverables: ["Survey Specification Document", "Question Bank with Decision Rules", "Survey Flow Diagram", "Analysis Plan", "Implementation Checklist"],
  user_feedback: null
})
```