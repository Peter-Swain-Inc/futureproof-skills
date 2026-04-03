---
name: ids-root-cause-solver
description: |
  Guides executive teams through Gino Wickman's Identify-Discuss-Solve (IDS) methodology to drill past symptoms to the true root cause before brainstorming solutions, then drives to concrete action items with owners and deadlines.
  Trigger: when a user presents a recurring business problem, organisational issue, or strategic challenge and needs help finding the real root cause — or when a user says they're stuck solving the same problem repeatedly and want to run IDS on it.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="ids-root-cause-solver")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to:
- Previous IDS sessions (recurring themes signal systemic root causes that span issues)
- Organisational structure, leadership team composition, and accountability chart if available
- Any standing `instructions` about communication style, strategic priorities, or decision-making norms

## Step 2: Get Input

Ask the user:

1. **State the issue in one sentence.** What is the problem, challenge, or opportunity you want to IDS? (Force brevity — if the description exceeds two sentences, ask them to distil further; verbosity at this stage is the first symptom of unclear framing.)
2. **Impact gravity.** What is the tangible cost of leaving this unsolved for another 90 days? (Revenue at risk, churn exposure, team attrition, strategic delay — quantify where possible.)
3. **History.** Has this issue — or a close variant — surfaced before? If so, what was tried and why didn't it hold?
4. **Who is in the room?** List the stakeholders involved or affected. (This shapes the Discuss and Solve phases — solutions must be assignable to real people.)

If the user provides a list of multiple issues, instruct them to **stack-rank by impact** and confirm which single issue to IDS first. IDS is sequential — one issue at a time, fully resolved before moving to the next.

## Step 3: IDENTIFY — Drill to the Root Cause

This is the most critical phase. Executives habitually solve the wrong problem because they anchor on the first framing. The goal is to separate **symptoms** from the **single root cause**.

Apply the following diagnostic protocol:

### 3a. Symptom Stripping

Restate the user's issue, then challenge it:
- "Is this the real problem, or is this a **symptom** of something deeper?"
- Ask **"Why?"** up to five times (Sakichi Toyoda's Five Whys), documenting each layer explicitly:

| Layer | Question | Answer |
|-------|----------|--------|
| L1 | Why is [stated issue] happening? | … |
| L2 | Why is [L1 answer] happening? | … |
| L3 | Why is [L2 answer] happening? | … |
| L4 | Why is [L3 answer] happening? | … |
| L5 | Why is [L4 answer] happening? | … |

Stop when the answer becomes something **directly actionable by someone in the room** — that is the root cause.

### 3b. Root Cause Validation

Before proceeding, pressure-test the identified root cause with three checks:

1. **Upstream test**: If we solved this root cause completely, would the original stated issue disappear? If not, there is a deeper or parallel cause.
2. **Recurrence test**: Does this root cause explain why the issue has resurfaced before (per the user's history in Step 2)?
3. **Scope test**: Is this root cause within the control or influence of the stakeholders in the room? If not, reframe to the highest-leverage factor they *can* control.

Present the validated root cause statement in bold and ask the user to explicitly confirm: **"Is THIS the real issue?"**

Do not proceed to Discuss until confirmation is received.

## Step 4: DISCUSS — Structured Exploration

Once the root cause is confirmed, facilitate a rigorous discussion. The rule: **everyone's input, but no tangents and no solution-jumping yet.**

### 4a. Dimension Mapping

Explore the root cause across six dimensions:

| Dimension | Guiding Question |
|-----------|-----------------|
| **People** | Is this a right-person-right-seat issue? Does someone lack the capacity, capability, or commitment to own this? |
| **Process** | Is there a missing, broken, or undocumented process that allows this root cause to persist? |
| **Data** | Are decisions being made without adequate leading indicators or scorecards? What metric would have flagged this earlier? |
| **Structure** | Does the accountability chart create ambiguity about who owns this outcome? |
| **Priorities** | Is this root cause a consequence of competing or misaligned Rocks (quarterly priorities)? |
| **Culture/Values** | Is there a core value violation or cultural norm enabling this issue to fester unaddressed? |

For each relevant dimension, summarise the key insight in one sentence.

### 4b. Constraint Identification

Surface the top constraints that any solution must respect:
- Budget or resource limits
- Timeline (e.g., must resolve before end of quarter)
- Organisational dependencies or political realities
- ICA impact (will the solution be visible to or felt by the ICA? If so, how must it be managed?)

### 4c. Discussion Summary

Produce a **Discussion Brief** — a concise synthesis of:
- Root cause (confirmed)
- Contributing dimensions (from 4a)
- Binding constraints (from 4b)
- Any areas of disagreement or uncertainty flagged by the user

## Step 5: SOLVE — Drive to Concrete Action

Now — and only now — move to solutions. Apply the following rigorous solve protocol:

### 5a. Solution Generation

Generate 3–5 candidate solutions that **directly address the confirmed root cause** (not the original symptom). For each candidate:

| # | Solution | Addresses Root Cause Because… | Effort (H/M/L) | Impact (H/M/L) | Risk |
|---|----------|-------------------------------|-----------------|-----------------|------|
| 1 | … | … | … | … | … |
| 2 | … | … | … | … | … |
| 3 | … | … | … | … | … |

Prioritise solutions that are **simple, executable within the current quarter, and owned by one person** — per EOS discipline.

### 5b. Solution Selection

Ask the user to select or combine. If they are torn, apply a forced-rank: "If you could only do ONE of these, which moves the needle most?" That is the primary action. Others become contingencies or Phase 2.

### 5c. To-Do Construction

Convert the selected solution into EOS-standard **To-Dos** — each with three mandatory fields:

| To-Do | Owner | Due Date |
|-------|-------|----------|
| [Specific, verb-first action — not vague] | [Single name — shared ownership = no ownership] | [Specific date, not "ASAP"] |
| … | … | … |
| … | … | … |

Apply the **"Who does what by when?"** test to every line. If any field is vague, challenge the user to sharpen it before finalising.

### 5d. Cascading Communication

If the solution requires communication beyond the room, specify:
- **Who** needs to be informed (by name or role)
- **What** message (one-sentence version)
- **By when** and **via what channel**

## Step 6: Deliver Output

Produce the **IDS Resolution Document** — a single, structured artefact the user can paste directly into their Level 10 meeting notes, issue tracker, or EOS tooling:

---

### IDS Resolution Document

**Date**: [Session date]
**Issue (as originally stated)**: [From Step 2]
**Root Cause (validated)**: [From Step 3]

**Five Whys Trace**:
[Table from Step 3a]

**Discussion Summary**:
- Key dimensions: [From Step 4a]
- Binding constraints: [From Step 4b]

**Selected Solution**: [From Step 5b]

**Action Items**:
| To-Do | Owner | Due Date |
|-------|-------|----------|
| … | … | … |

**Cascading Communication**:
| Recipient | Message | Channel | By When |
|-----------|---------|---------|---------|
| … | … | … | … |

**Follow-Up**: This issue is **resolved/moved to the V/TO issue list/carried to next L10** (ask user to confirm status).

---

Ask the user: "Is this issue resolved, or does it need to be carried forward?" Update the status accordingly.

## Step 7: Propose Experiments

```
FutureProof:save_experiment(skill="ids-root-cause-solver", experiment={
  hypothesis: "Applying the Five Whys drill consistently surfaces root causes that differ from the originally stated issue in >70% of sessions, leading to higher solution durability",
  variants: ["control: team solves from original issue framing", "variant: team solves from IDS-validated root cause"],
  measurement: "Issue recurrence rate — does the same issue reappear within 90 days on the L10 issues list?",
  expected_impact: "60% reduction in recurring issues on the L10 list within two quarters"
})
```

## Step 8: Request Research

```
FutureProof:request_research(skill="ids-root-cause-solver",
  query="Advanced root-cause analysis frameworks used alongside EOS IDS — including Kepner-Tregoe, Ishikawa, and current-reality trees — and evidence on which techniques most reduce issue recurrence in leadership teams",
  reason="Strengthen the Identify phase with complementary diagnostic tools; ensure the methodology evolves beyond baseline Five Whys when users bring complex, multi-causal issues"
)
```

## Step 9: Save Session

```
FutureProof:save_session(skill="ids-root-cause-solver", session={
  summary: "IDS session on [root cause summary] — originally presented as [stated issue summary]",
  key_findings: ["Root cause diverged from stated issue: [yes/no]", "Primary dimension: [people/process/data/structure/priorities/culture]", "Number of action items generated: [n]", "Issue status: [resolved/carried forward]"],
  user_feedback: null
})
```