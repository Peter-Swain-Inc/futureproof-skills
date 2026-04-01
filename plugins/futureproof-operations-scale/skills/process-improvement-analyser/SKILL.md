---
name: process-improvement-analyser
description: "Analyses business processes for inefficiencies, bottlenecks, and waste using structured improvement methodologies (Lean Six Sigma, TOC, BPR) enriched by FutureProof context."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="process-improvement-analyser")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including any prior process analyses, known organisational constraints, ICA segment characteristics, and previously identified systemic bottlenecks.

## Step 2: Get Input

Ask the user:
- **Process under review**: Share the process map, SOP, workflow description, or operational narrative. If no formal documentation exists, walk through the process step-by-step verbally.
- **Scope boundaries**: Where does this process start and end? What upstream inputs and downstream handoffs are in play?
- **Pain signal**: What triggered this review? (e.g., cycle time complaints, cost overruns, error rates, customer churn at a specific stage, scaling failure)
- **Current metrics** (if available): Throughput, cycle time, defect/error rate, cost per transaction, headcount involved, rework frequency.
- **Constraints**: Non-negotiable elements — regulatory requirements, platform/tooling lock-ins, union agreements, budget ceilings.
- **Improvement objective**: What does success look like? (e.g., reduce cycle time by 40%, cut cost per unit by 25%, eliminate manual handoffs, support 3× volume without headcount increase)

## Step 3: Do the Work

### 3A: Process Decomposition & Current-State Mapping

Break the process into discrete stages. For each stage, capture:
- **Activity type**: Value-adding (VA), Business-necessary non-value-adding (BNVA), or Non-value-adding waste (NVA) — per Lean classification
- **Responsible party**: Role or system performing the activity
- **Cycle time**: Active working time per unit
- **Wait time**: Elapsed time between this activity completing and the next beginning
- **Error/rework rate**: Frequency of defects or loops at this stage
- **Dependencies**: Upstream inputs, approvals, or system integrations required

Render a **Current-State Value Stream Summary Table** from this decomposition.

### 3B: Bottleneck & Constraint Identification (Theory of Constraints)

Identify the single binding constraint — the stage where throughput is most restricted. Validate by checking:
1. Does work-in-progress (WIP) accumulate immediately before this stage?
2. Does every downstream stage have idle/wait capacity?
3. Would doubling this stage's capacity increase total process throughput?

Flag secondary constraints that would become binding if the primary constraint were relieved.

### 3C: Waste Classification (8 Wastes of Lean)

Categorise all identified NVA activities across the eight waste types:
1. **Defects** — errors requiring rework or correction
2. **Overproduction** — producing outputs before they are needed downstream
3. **Waiting** — idle time between stages, approval queues, batch accumulation
4. **Non-utilised talent** — skilled personnel performing tasks below their capability
5. **Transportation** — unnecessary movement of information or materials between systems/teams
6. **Inventory** — WIP buildup, backlog accumulation, excess data staging
7. **Motion** — redundant steps, excessive clicks, toggling between systems
8. **Extra processing** — over-engineering, unnecessary approvals, gold-plating

Rank wastes by estimated impact (time cost × frequency) to prioritise intervention.

### 3D: Root Cause Analysis

For the top 3 waste sources and the binding constraint, perform a **5 Whys analysis** to surface root causes. Distinguish between:
- **Structural causes** (process design, system architecture)
- **Behavioural causes** (workarounds, tribal knowledge, incentive misalignment)
- **Environmental causes** (tooling limitations, policy constraints, volume variability)

### 3E: Future-State Design

Design an improved process that:
1. **Exploits the constraint** — maximises throughput at the bottleneck with zero additional investment
2. **Subordinates other stages** — aligns non-constraint stages to feed the bottleneck at its exact capacity (no faster, no slower)
3. **Eliminates NVA activities** — removes or automates pure waste steps
4. **Converts BNVA to automated** — applies automation, templates, or system integration to business-necessary overhead
5. **Introduces error-proofing (poka-yoke)** — builds validation, defaults, and constraints that prevent defects at source

Apply any user-specific `instructions` from FutureProof context — such as preferred tooling, organisational change appetite, ICA-facing SLA requirements, or prior experiment results — to calibrate recommendations.

## Step 4: Deliver Output

Produce a **Process Improvement Analysis Report** with the following sections:

### 4.1 — Executive Summary
Two-paragraph narrative: current-state diagnosis, recommended future state, and projected impact on the user's stated objective.

### 4.2 — Current-State Value Stream Summary Table

| Stage | Activity Type (VA/BNVA/NVA) | Owner | Cycle Time | Wait Time | Error Rate | Waste Type |
|-------|------------------------------|-------|------------|-----------|------------|------------|
| ...   | ...                          | ...   | ...        | ...       | ...        | ...        |

### 4.3 — Bottleneck Analysis
Identification of the binding constraint with supporting evidence and secondary constraint forecast.

### 4.4 — Waste Heat Map
Ranked list of waste instances by estimated annualised impact (hours or cost), with waste type classification.

### 4.5 — Root Cause Summary
5 Whys output for top 3 issues — structured as cause chains terminating in actionable root causes.

### 4.6 — Improvement Recommendations (Prioritised)
For each recommendation:
- **Change description**: Specific, implementable action (not directional advice)
- **Waste/constraint addressed**: Direct link to diagnosis
- **Implementation complexity**: Low / Medium / High
- **Expected impact**: Quantified where data permits (e.g., "Eliminates ~12 hours/week of manual reconciliation")
- **Prerequisites**: Dependencies, tooling, or approvals required

Recommendations ordered by **impact-to-effort ratio** (highest first).

### 4.7 — Future-State Process Summary
Revised stage-by-stage flow reflecting all recommended changes, with projected cycle time, wait time, and error rate per stage.

### 4.8 — Implementation Roadmap
Three-horizon phasing:
- **Quick wins** (0–2 weeks): Zero-cost or low-cost changes executable immediately
- **Structural improvements** (2–8 weeks): System changes, automation builds, role redesigns
- **Systemic transformation** (8+ weeks): Cross-functional redesigns, tooling migrations, culture/incentive shifts

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="process-improvement-analyser", experiment={
  hypothesis: "Eliminating the [identified NVA stage] and routing directly to [downstream stage] reduces end-to-end cycle time without increasing error rate",
  variants: ["control: current process with manual handoff intact", "variant: direct routing with automated validation gate"],
  measurement: "Cycle time (end-to-end) and defect rate tracked over 30-day window across both variants",
  expected_impact: "20–35% reduction in cycle time with error rate held constant or improved"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="process-improvement-analyser",
  query="Latest automation and process orchestration patterns for [user's industry/process domain] — including AI-assisted workflow tools, RPA benchmarks, and Lean Six Sigma case studies from 2024",
  reason="Ensure recommendations reflect current best-in-class tooling and methodology, and identify proven intervention patterns for similar process archetypes"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="process-improvement-analyser", session={
  summary: "Analysed [process name] for [user's team/business unit] — identified [binding constraint] as primary bottleneck and [top waste type] as highest-impact waste category",
  key_findings: ["Binding constraint at [stage] creating [X hours/week] of downstream wait time", "[NVA activity] accounts for [Y%] of total cycle time with zero value contribution", "Root cause traced to [structural/behavioural/environmental factor]"],
  recommendations_count: "[N] recommendations delivered, [M] classified as quick wins",
  user_feedback: null
})
```