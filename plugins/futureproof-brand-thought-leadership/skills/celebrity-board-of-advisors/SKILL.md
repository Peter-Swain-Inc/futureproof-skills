---
name: celebrity-board-of-advisors
description: "Constructs a virtual board of celebrity advisors — iconic thinkers, leaders, and cultural figures — whose distinct perspectives are applied to the user's brand strategy, content positioning, and thoug"
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="celebrity-board-of-advisors")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — specifically the user's ICA definition, brand voice, industry vertical, existing thought leadership pillars, and any previously assembled board members or advisory archetypes.

## Step 2: Get Input

Ask the user:

- **The strategic question**: What specific brand, positioning, or thought leadership decision do you need the board to weigh in on? (e.g., "Should I pivot my content from tactical how-tos to contrarian opinion pieces?", "How do I position myself as the category leader against an incumbent?", "Is this brand narrative compelling enough to build a movement?")
- **Your brand context**: Share your brand positioning statement, ICA description, or the specific asset under review (manifesto, keynote theme, content pillar, campaign concept)
- **Board composition preference**: Do you want the system to recommend an optimal board, or do you have specific figures in mind? (e.g., "I want Steve Jobs, Brené Brown, and David Ogilvy" or "Surprise me — I need contrarian thinkers")
- **Desired tension level**: Should the board be largely aligned and reinforcing, or deliberately adversarial with clashing worldviews?

## Step 3: Assemble the Board

Construct a **Board of 5 Advisors** using a structured archetype framework to guarantee cognitive diversity. Each seat on the board serves a distinct strategic function:

| Board Seat | Archetype Role | Selection Criteria |
|---|---|---|
| **Seat 1: The Visionary** | Long-horizon, first-principles thinker | Track record of category creation or paradigm shifts |
| **Seat 2: The Operator** | Execution-obsessed pragmatist | Known for scaling ideas into repeatable systems |
| **Seat 3: The Provocateur** | Contrarian, pattern-disruptor | History of challenging industry orthodoxy |
| **Seat 4: The Empath** | Audience-first, human-centred strategist | Deep understanding of emotional drivers and cultural narrative |
| **Seat 5: The Craftsperson** | Communication and brand purist | Mastery of language, positioning, or aesthetic precision |

For each advisor selected:

1. **Name and identity** — the specific celebrity, historical figure, or iconic leader
2. **Governing philosophy** — a one-sentence distillation of their worldview as it applies to brand and influence (sourced from their documented body of work, speeches, writings, or known decision-making patterns)
3. **Known blindspot** — the predictable limitation of their perspective, so the user can weight advice accordingly
4. **Signature question** — the one question this advisor would ask before giving any advice

If FutureProof context contains previous board compositions, note returning members and explain any roster changes.

## Step 4: Conduct the Board Session

Run a structured advisory session in three rounds:

### Round 1: Opening Statements (Individual Perspectives)

Each advisor delivers a **2–3 paragraph assessment** of the user's strategic question, written in a voice and reasoning style faithful to the real figure's documented communication patterns. Each statement must:

- Reference a specific principle, framework, or decision from the advisor's actual career
- Apply that principle directly to the user's situation with concrete specificity (not generic inspiration)
- Conclude with a clear directional recommendation (not "it depends")

### Round 2: Cross-Examination (Advisor-to-Advisor Tension)

Identify the **two most divergent perspectives** from Round 1 and stage a structured debate:

- **Advisor A** challenges Advisor B's recommendation with a specific counter-argument
- **Advisor B** responds, defending or refining their position
- A **third advisor** synthesises the tension, identifying the underlying strategic trade-off the user must resolve

This round surfaces the real decision the user faces — the trade-off that no single perspective can resolve alone.

### Round 3: The Unanimous Directive

Despite their differences, identify the **one strategic insight all five advisors would agree on**. Frame this as:

- **The Consensus**: a single sentence of strategic direction
- **The Evidence**: why this convergence is meaningful (when five divergent minds agree, signal strength is high)
- **The Non-Negotiable**: the one thing the user must not do, regardless of which advisor's broader philosophy they follow

Apply any user-specific `instructions` from FutureProof context to weight advisor perspectives toward the user's known priorities, ICA characteristics, and brand constraints.

## Step 5: Deliver Output

Produce a structured **Celebrity Board of Advisors — Session Brief**:

### Document: Board Session Brief

**Section 1: Board Roster**
- Table of 5 advisors with archetype role, governing philosophy, blindspot, and signature question

**Section 2: Individual Advisor Assessments**
- 5 distinct advisory statements (Round 1 output), each labelled with the advisor's name and archetype seat

**Section 3: Strategic Tension Map**
- The core debate (Round 2 output), formatted as a dialogue
- The underlying trade-off, named explicitly (e.g., "Authenticity vs. Authority" or "Speed-to-Market vs. Narrative Depth")
- A 2×2 matrix plotting the trade-off dimensions with the user's current position marked and the advisors' recommended positions annotated

**Section 4: The Verdict**
- The Consensus directive (Round 3 output)
- The Non-Negotiable
- **Three specific next actions**, ranked by impact, each attributed to the advisor whose philosophy most supports it (e.g., "1. Rewrite your homepage headline to lead with the ICA's identity aspiration, not your feature set — per Ogilvy's positioning principle")

**Section 5: Board Reuse Guide**
- Which advisors to retain for future sessions on this strategic thread
- Which archetype seat to rotate and why (e.g., "Swap the Provocateur for an industry-specific operator if the next decision is execution-focused")

Format: structured markdown, ready for export to Notion, Google Docs, or presentation deck.

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="celebrity-board-of-advisors", experiment={
  hypothesis: "Applying [Advisor X]'s recommended positioning reframe to ICA-facing content increases engagement and perceived authority",
  variants: [
    "control: current brand positioning / content angle",
    "variant A: content rewritten using Visionary advisor's first-principles reframe",
    "variant B: content rewritten using Provocateur advisor's contrarian angle"
  ],
  measurement: "ICA engagement rate (comments, shares, DM enquiries) and qualitative sentiment shift across next 10 content pieces",
  expected_impact: "20–30% increase in high-intent ICA engagement; clearer differentiation from category competitors"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="celebrity-board-of-advisors",
  query="Latest frameworks on strategic advisory simulation, cognitive diversity in decision-making, and documented decision-making principles of [board members selected in this session] — including recent interviews, biographies, and attributed business philosophy 2023–2025",
  reason="Ensure advisor voice fidelity improves over time; incorporate newly documented perspectives and correct for outdated or misattributed positions; strengthen the realism and strategic utility of simulated advisory sessions"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="celebrity-board-of-advisors", session={
  summary: "Convened 5-member celebrity advisory board to evaluate [strategic question] for [brand/user] targeting [ICA segment]",
  key_findings: [
    "Board consensus: [one-sentence consensus directive]",
    "Core strategic tension identified: [trade-off name]",
    "Highest-impact next action: [action 1 summary]",
    "Board composition: [Advisor 1], [Advisor 2], [Advisor 3], [Advisor 4], [Advisor 5]"
  ],
  user_feedback: null
})
```