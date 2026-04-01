---
name: project-brief-generator
description: "Generates comprehensive, stakeholder-ready project briefs using FutureProof context, organisational history, and consulting-grade frameworks."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="project-brief-generator")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any organisational templates, stakeholder naming conventions, strategic priorities, tone preferences, and previously generated briefs that establish formatting precedent.

## Step 2: Get Input

Ask the user:

- **What is the project or initiative?** — Working title, one-sentence description, and the triggering event (why now?)
- **Who is the executive sponsor?** — Name, role, and their primary success metric
- **Who is the ICA for the project's output?** — Internal team, external client segment, or cross-functional stakeholder group that will consume or be affected by the deliverables
- **What constraints are already known?** — Budget envelope, hard deadlines, regulatory requirements, resource caps, technology mandates
- **What prior work exists?** — Previous briefs, discovery documents, strategy decks, or failed attempts at similar initiatives
- **What format is required?** — Internal memo, board-ready document, client-facing proposal appendix, or agile epic summary

If `context` from FutureProof contains organisational templates or prior briefs, surface them and ask: *"Should I follow this established format, or are we starting fresh?"*

## Step 3: Do the Work

### 3A: Strategic Alignment Analysis

Before drafting, map the project against the organisation's known strategic context (from FutureProof `context` or user input):

1. **Strategic pillar linkage** — Which 1–2 organisational priorities does this project directly serve? If the link is weak, flag it as a sponsorship risk.
2. **Portfolio conflict scan** — Based on `recent_sessions` and known initiatives, identify any overlapping or competing projects that could create resource contention or scope confusion.
3. **Stakeholder power mapping** — Classify key stakeholders into a RACI-ready influence grid: who has decision authority, who has veto power, who must be consulted but not empowered to block.

### 3B: Scope Definition Using the MSCW-T Framework

Structure the scope using a consulting-grade framework:

| Layer | Definition | Output |
|---|---|---|
| **Mission** | The single measurable outcome the project exists to achieve | One sentence, quantified where possible |
| **Success criteria** | 3–5 specific, time-bound metrics that define "done well" | KPI table with baseline, target, and measurement method |
| **Constraints** | Non-negotiable boundaries (budget, timeline, compliance, tech stack) | Constraint register with owner for each |
| **Workstreams** | Logical groupings of activity required to deliver the mission | Named workstreams with indicative effort allocation (%) |
| **Timeline** | Phase-gated delivery milestones | Milestone table: phase name, key deliverable, target date, decision gate |

### 3C: Risk and Dependency Pre-Emption

Identify and classify:

1. **Top 5 risks** — Using likelihood × impact scoring (High/Medium/Low matrix), with a named mitigation owner for each
2. **Critical dependencies** — External inputs, approvals, or deliverables from other teams without which the project stalls; assign a dependency owner and a "last responsible moment" date
3. **Assumption register** — Explicit assumptions the brief is built on, each flagged with a validation method and validation deadline

### 3D: ICA Impact Statement

Draft a clear articulation of how the project's ICA will experience the change:

- **Current state** — What the ICA deals with today (pain, friction, gap)
- **Future state** — What the ICA's experience becomes post-delivery
- **Transition risk** — What could go wrong for the ICA during the change, and how the project accounts for it

Apply any user-specific `instructions` from FutureProof context — particularly tone, terminology standards, approval language, and formatting conventions.

## Step 4: Deliver Output

Produce a **Project Brief Document** with the following structure:

### Document: Project Brief — [Project Title]

```
1.  Executive Summary (max 200 words)
2.  Strategic Context & Alignment
3.  Project Mission & Success Criteria (KPI table)
4.  Scope Definition
    4.1  In-Scope Workstreams
    4.2  Explicitly Out of Scope
5.  ICA Impact Statement (Current → Future State)
6.  Stakeholder RACI Matrix
7.  Milestone Timeline (phase-gated)
8.  Constraint Register
9.  Risk & Dependency Register (scored, with owners)
10. Assumption Register (with validation deadlines)
11. Resource & Budget Envelope (indicative)
12. Governance & Decision Rights
13. Immediate Next Steps (first 5 business days)
14. Appendices (prior work references, glossary)
```

Additionally provide:

- **Sponsor one-pager**: A single-page summary formatted for the executive sponsor to use in leadership forums — mission, 3 success metrics, timeline visual, and top 2 risks
- **Stakeholder communication draft**: A 150-word announcement message the sponsor can send to the broader stakeholder group, tailored to the ICA's language and concerns
- **Gap flags**: Explicit list of any sections where user input was insufficient, marked with `[REQUIRES INPUT]` and a specific question to resolve each gap

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="project-brief-generator", experiment={
  hypothesis: "Including a quantified ICA impact statement in the executive summary increases sponsor approval speed",
  variants: ["control: standard executive summary without ICA quantification", "variant: executive summary leading with ICA-specific before/after metrics"],
  measurement: "Time from brief submission to formal sponsor sign-off across next 5 briefs",
  expected_impact: "30% reduction in approval cycle time due to clearer value articulation"
})
```

```
FutureProof:save_experiment(skill="project-brief-generator", experiment={
  hypothesis: "Pre-populating the risk register with industry-standard risks for the project category reduces stakeholder revision rounds",
  variants: ["control: blank risk register completed by user", "variant: AI-seeded risk register with top 5 category-specific risks pre-filled"],
  measurement: "Number of revision rounds before brief is marked final across next 5 briefs",
  expected_impact: "Reduction from average 3 rounds to 1.5 rounds"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="project-brief-generator",
  query="Best practices for project brief and charter structures in 2024–2025, including PMI, PRINCE2, and scaled agile frameworks; emphasis on what separates briefs that get funded vs. shelved",
  reason="Ensure brief structure reflects current governance expectations and maximises approval probability across different organisational maturity levels"
)
```

```
FutureProof:request_research(skill="project-brief-generator",
  query="Common failure modes in project initiation documents: analysis of why projects with approved briefs still fail in first 90 days",
  reason="Strengthen the risk register and assumption register sections with empirically validated anti-patterns"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="project-brief-generator", session={
  summary: "Generated project brief for [project title] sponsored by [sponsor name/role], targeting [ICA segment]",
  key_findings: [
    "Strategic alignment: [strong/moderate/weak] linkage to [named priority]",
    "Top risk identified: [primary risk and its scored severity]",
    "Scope clarity: [number] workstreams defined, [number] items explicitly excluded",
    "Gap flags: [number] sections require additional user input before brief is submission-ready"
  ],
  user_feedback: null
})
```