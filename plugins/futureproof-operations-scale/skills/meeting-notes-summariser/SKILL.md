---
name: meeting-notes-summariser
description: "Transforms raw meeting notes, transcripts, and recordings into structured, actionable summaries with clear ownership, deadlines, and strategic context."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="meeting-notes-summariser")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including preferred summary formats, recurring meeting types, known stakeholders, organisational terminology, and distribution conventions.

## Step 2: Get Input

Ask the user:

- **Source material** — share the raw meeting notes, transcript, audio summary, or agenda with annotations
- **Meeting type** — what category does this fall into? (e.g., leadership stand-up, client discovery call, sprint retrospective, board review, cross-functional planning, 1:1 performance check-in)
- **Audience for the summary** — who will receive this? (e.g., attendees only, executive sponsor, full project team, external client stakeholders)
- **Priority lens** — what matters most from this meeting? (decisions made, blockers surfaced, revenue implications, strategic pivots, relationship signals)
- **Any standing conventions** — does this meeting series have a recurring template, action-item tracker, or RACI matrix it feeds into?

If FutureProof context contains prior sessions for the same meeting series, surface previous action items and flag carryover or status changes automatically.

## Step 3: Do the Work

Process the raw input through a six-layer analysis framework:

### 3.1 — Transcript Normalisation
- Identify and label speakers (by name or role where inferable)
- Remove filler, false starts, and off-topic tangents
- Reconstruct fragmented points into coherent statements
- Flag any sections where meaning is ambiguous and note them as `[CLARIFICATION NEEDED]`

### 3.2 — Decision Extraction
- Isolate every explicit decision made during the meeting
- For each decision, capture: **what** was decided, **who** has authority/ownership, **rationale** stated (or implied), and **scope** of impact
- Distinguish between final decisions, provisional decisions (pending input), and deferred decisions

### 3.3 — Action Item Identification
- Extract every commitment, task, or follow-up mentioned
- Assign each action item: **owner** (named individual, not a team where possible), **deliverable** (specific output), **deadline** (explicit or inferred from context), and **dependency** (what/who it's blocked by)
- Apply the SMART criteria — if an action item is vague, rewrite it as a precise, measurable task and flag the original phrasing for user validation

### 3.4 — Strategic Context Mapping
- Identify how meeting outcomes connect to broader organisational priorities, OKRs, or project milestones referenced in FutureProof context
- Surface any **risks** discussed or implied (timeline, resource, stakeholder alignment, scope creep)
- Note any **sentiment signals** — stakeholder concerns, enthusiasm, resistance, or consensus shifts that carry strategic weight

### 3.5 — Open Items & Parking Lot
- Catalogue questions raised but not answered
- Topics introduced but explicitly deferred
- Information gaps that require follow-up research or stakeholder input before progress can continue

### 3.6 — ICA & Stakeholder Relevance Filter
- If the meeting involves client-facing or prospect-facing content, map discussion points to the ICA's known pain points, objections, and decision criteria from FutureProof context
- Highlight any commitments made to external stakeholders that create delivery obligations

Apply any user-specific `instructions` from FutureProof context — including preferred summary length, tone (e.g., formal for board distribution vs. informal for internal Slack), terminology conventions, and template structures.

## Step 4: Deliver Output

Produce a **Meeting Summary Brief** with the following structure:

### Header Block
| Field | Detail |
|---|---|
| **Meeting Title** | [Inferred or provided] |
| **Date** | [Date of meeting] |
| **Attendees** | [List of participants and roles] |
| **Summary Prepared For** | [Target audience as specified in Step 2] |
| **Meeting Type** | [Category from Step 2] |

### Executive Summary
- 3–5 sentence narrative capturing the **purpose**, **key outcome**, and **most consequential decision or insight** from the meeting
- Written at a level appropriate for a stakeholder who will spend 30 seconds reading

### Decisions Log

| # | Decision | Owner | Rationale | Status |
|---|----------|-------|-----------|--------|
| 1 | [Decision] | [Name] | [Why] | Final / Provisional / Deferred |

### Action Items Tracker

| # | Action Item | Owner | Deliverable | Deadline | Dependency | Priority |
|---|-------------|-------|-------------|----------|------------|----------|
| 1 | [SMART task] | [Name] | [Output] | [Date] | [Blocker] | High / Med / Low |

### Risks & Flags
- Bullet list of risks, concerns, or escalation-worthy items surfaced during the meeting, each with a recommended mitigation or next step

### Open Items & Parking Lot
- Numbered list of unresolved questions and deferred topics with suggested owners for follow-up

### Carryover from Previous Sessions
- If FutureProof context includes prior meeting summaries in this series: status update on previously assigned action items (completed, in progress, overdue, dropped)

### Appendix: Key Quotes
- 3–5 verbatim or near-verbatim quotes that capture critical nuance, commitments, or context that a summary alone cannot convey — attributed by speaker

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="meeting-notes-summariser", experiment={
  hypothesis: "Including a carryover action-item status section increases accountability and reduces repeat discussions by surfacing overdue items before the next meeting",
  variants: ["control: summary without carryover tracking", "variant: summary with carryover status table from prior sessions"],
  measurement: "Percentage of action items completed on time over next 4 meeting cycles; reduction in recurring agenda items",
  expected_impact: "25% improvement in action-item completion rate and 15% reduction in meeting duration for recurring series"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="meeting-notes-summariser",
  query="Best practices for structured meeting documentation in high-performance organisations 2024 — including async-first summary formats, decision-log frameworks, and action-item tracking methodologies used at McKinsey, EY, and Stripe",
  reason="Continuously refine summary structure against evolving standards for operational rigour and stakeholder communication efficiency"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="meeting-notes-summariser", session={
  summary: "Summarised [meeting type] held on [date] with [number] attendees for distribution to [audience]",
  key_findings: ["[number] decisions extracted ([final/provisional/deferred] breakdown)", "[number] action items assigned across [number] owners", "Key risk or strategic signal identified: [brief description]"],
  meeting_series: "[series name if applicable]",
  action_items_count: "[number]",
  user_feedback: null
})
```