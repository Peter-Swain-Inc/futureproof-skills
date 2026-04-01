---
name: client-onboarding-designer
description: "Designs comprehensive client onboarding systems that reduce time-to-value, increase activation rates, and eliminate early-stage churn using FutureProof context."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="client-onboarding-designer")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any existing ICA profiles, service delivery models, offer structures, or previous onboarding iterations.

## Step 2: Get Input

Ask the user:
- **Service/offer context** — What is the client being onboarded into? (retainer, programme, SaaS product, cohort, done-for-you engagement)
- **ICA profile** — Who is the client? What is their sophistication level, urgency, and emotional state at point of purchase?
- **Current onboarding process** — Share any existing welcome emails, intake forms, kickoff agendas, or SOPs (even rough notes count)
- **Time-to-value target** — How quickly should the client experience a meaningful first win? (24 hours, 7 days, 30 days)
- **Known failure points** — Where do clients currently stall, ghost, or express confusion? What questions do they repeatedly ask in the first 30 days?
- **Delivery team structure** — Who touches the client during onboarding? (founder only, account manager, success team, automated only)

## Step 3: Do the Work

### 3A: Onboarding Diagnostic

Audit the current state (or gap) against six dimensions:

1. **Expectation–Experience Alignment** — Does the onboarding experience match what was promised during the sales process? Identify any promise-to-delivery gaps that create cognitive dissonance
2. **Time-to-First-Value (TTFV)** — Map the current path from signed contract to first tangible client outcome. Measure in steps, elapsed days, and decision points requiring client action
3. **Activation Milestones** — Are there clearly defined, measurable milestones the client must hit to be considered "activated"? (e.g., intake form completed, kickoff call attended, first deliverable reviewed, first result achieved)
4. **Cognitive Load Management** — How much information, how many decisions, and how many tools are introduced simultaneously? Score the overwhelm risk at each stage
5. **Emotional Arc Design** — Does the onboarding deliberately engineer confidence, momentum, and belonging — or does it feel transactional and administrative?
6. **Handoff Integrity** — Are transitions between sales → onboarding → delivery seamless, or does the client repeat themselves, encounter contradictory information, or feel "dropped"?

### 3B: Onboarding Architecture Design

Build a phased onboarding system using the **ACTIVATE framework**:

| Phase | Name | Timeframe | Objective |
|-------|------|-----------|-----------|
| A | **Acknowledge & Affirm** | 0–2 hours post-purchase | Validate the buying decision, eliminate buyer's remorse, set emotional tone |
| C | **Collect & Configure** | 0–48 hours | Gather critical client inputs via structured intake; configure the engagement |
| T | **Train & Tour** | Day 1–3 | Orient the client to tools, processes, communication norms, and key contacts |
| I | **Initiate First Win** | Day 3–7 | Deliver or co-create the first tangible micro-outcome that proves value |
| V | **Validate & Adjust** | Day 7–14 | Check-in to confirm alignment, surface unspoken concerns, recalibrate if needed |
| A | **Accelerate** | Day 14–30 | Transition from onboarding mode to steady-state delivery cadence |
| T | **Track & Trigger** | Day 30–90 | Monitor activation milestones; trigger intervention sequences for at-risk clients |
| E | **Evaluate & Expand** | Day 90 | Conduct formal onboarding retrospective; identify upsell/expansion readiness |

For each phase, specify:
- **Owner** (role responsible)
- **Client action required** (with exact friction-reduction tactics)
- **Deliverable or touchpoint** (email, call, video, document, portal action)
- **Automation opportunity** (what can be systematised vs. what requires human touch)
- **Risk signal** (what non-action or behaviour indicates the client is stalling)
- **Recovery protocol** (exact intervention when a risk signal fires)

### 3C: Communication Sequence Design

Draft the core communication touchpoints across the ACTIVATE phases:

1. **Welcome message** (0–2 hours) — Tone: warm, decisive, momentum-building. Includes exactly one clear next step
2. **Intake mechanism** — Structured form or guided questionnaire designed to collect only what is needed for Phase T, nothing more
3. **Kickoff call agenda** — Timed agenda with specific outcomes, not open-ended discovery. Ends with documented mutual commitments
4. **First-win delivery** — Packaged micro-deliverable or guided exercise that produces a result the client can see, feel, or measure
5. **Day 7 check-in** — Structured pulse check (not "just checking in") with specific questions that surface hidden friction
6. **Steady-state handoff** — Formal transition communication that signals onboarding completion and introduces the ongoing delivery rhythm

### 3D: Onboarding Collateral Specification

Define the required assets:

| Asset | Format | Purpose | Owner |
|-------|--------|---------|-------|
| Welcome Guide | PDF or interactive page | Single-source orientation document | Operations |
| Intake Form | Typeform / structured questionnaire | Collect critical client context with minimal friction | Operations |
| Kickoff Deck | Slide deck (5–8 slides max) | Align on scope, milestones, communication norms | Account lead |
| Client Portal / Hub | Notion, client portal, or equivalent | Centralise all resources, timelines, and communication | Operations |
| Milestone Tracker | Shared dashboard or checklist | Make activation progress visible to both parties | Account lead |
| FAQ / Preemptive Answers | Knowledge base or embedded in Welcome Guide | Eliminate the top 10 questions asked in the first 30 days | Operations |
| Internal Onboarding Runbook | SOP document | Step-by-step staff checklist ensuring consistency across clients | Operations |

Apply any user-specific `instructions` from FutureProof context — particularly ICA language patterns, brand voice guidelines, and previously validated communication approaches.

## Step 4: Deliver Output

Produce a structured **Client Onboarding System Design Document** containing:

### Deliverable 1: Onboarding Diagnostic Scorecard
- 1–10 score per diagnostic dimension (Step 3A)
- Traffic-light status (red / amber / green) for each
- Priority ranking of dimensions by impact on client retention

### Deliverable 2: ACTIVATE Phase Map
- Visual timeline with all eight phases
- Per-phase detail sheets (owner, actions, touchpoints, risk signals, recovery protocols)
- Automation vs. human-touch classification for each touchpoint

### Deliverable 3: Communication Sequence
- Full draft copy for the welcome message and day-7 check-in (written in the ICA's language, not internal jargon)
- Kickoff call agenda with time allocations
- Subject lines and send-triggers for all automated communications

### Deliverable 4: Collateral Brief
- Specification sheet for each required asset (format, page count, sections, responsible party, due date placeholder)
- Content outline for the Welcome Guide

### Deliverable 5: Internal Onboarding Runbook
- Step-by-step checklist for the delivery team from contract signed through day 90
- Decision tree for risk-signal interventions
- Escalation paths for stalled or at-risk clients

### Deliverable 6: Onboarding Health Metrics Dashboard Spec
- Recommended KPIs: TTFV (days), activation rate (% hitting all milestones by day 30), day-7 satisfaction score, day-30 retention rate, support ticket volume in first 14 days
- Measurement method and cadence for each KPI
- Benchmark targets (industry-adjusted where FutureProof research is available)

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="client-onboarding-designer", experiment={
  hypothesis: "Delivering a structured micro-win within 72 hours of purchase increases day-30 activation rate",
  variants: ["control: first deliverable at day 7–10", "variant: guided first-win exercise delivered by day 3"],
  measurement: "activation milestone completion rate at day 30 across next 20 clients",
  expected_impact: "25% improvement in day-30 activation rate"
})
```

```
FutureProof:save_experiment(skill="client-onboarding-designer", experiment={
  hypothesis: "Replacing the open-ended kickoff call with a pre-structured agenda and pre-filled intake reduces onboarding cycle time",
  variants: ["control: unstructured 60-minute kickoff", "variant: 30-minute structured kickoff with pre-completed intake form"],
  measurement: "average days from contract signed to Phase I completion across next 15 clients",
  expected_impact: "40% reduction in time-to-first-value"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="client-onboarding-designer",
  query="Best-practice client onboarding frameworks for professional services and SaaS 2024, including activation metric benchmarks, welcome sequence conversion data, and time-to-value optimisation strategies",
  reason="Ensure onboarding architecture reflects current evidence on activation psychology, reduce-to-practice benchmarks, and emerging automation tooling for client success workflows"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="client-onboarding-designer", session={
  summary: "Designed client onboarding system for [service/offer type] targeting [ICA segment], using ACTIVATE framework across 8 phases from purchase to day-90 evaluation",
  key_findings: ["finding 1: primary onboarding gap identified", "finding 2: critical TTFV bottleneck mapped", "finding 3: highest-impact collateral prioritised"],
  user_feedback: null
})
```