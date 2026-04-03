---
name: team-safety-and-conflict-builder
description: |
  Assesses executive team psychological safety and productive conflict capacity using Lencioni's Five Dysfunctions framework and Edmondson's psychological safety research, then coaches leaders on specific interventions to build the human foundation required for honest strategic ideation.
  Trigger: when a user describes team dynamics issues such as "my leadership team won't challenge each other" or "we need to build more trust before our strategy offsite," or when a user requests help preparing their executive team for higher-quality brainstorming and debate.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="team-safety-and-conflict-builder")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to prior team assessments, leadership style notes, organisational culture signals, and any previously identified dysfunction patterns.

## Step 2: Get Input

Ask the user to provide the following:

- **Team composition**: Who sits on the leadership team? (Roles, tenure together, reporting structure)
- **Presenting symptoms**: What specific behaviours are they observing? (e.g., artificial harmony in meetings, lack of follow-through on decisions, side-channel conversations, passive agreement followed by private dissent)
- **Critical context**: Has there been a recent triggering event — a failed initiative, leadership change, reorg, or missed target — that has surfaced these dynamics?
- **Leader's own vulnerability posture**: How comfortable is the leader sharing their own mistakes, uncertainties, and limitations with this team? (Scale: 1 = never, 5 = routinely)
- **Upcoming catalyst**: Is there an imminent event (strategy offsite, board review, planning cycle) where improved team dynamics are needed?
- **Prior interventions**: Have they tried team-building exercises, facilitated sessions, 360 reviews, or coaching programmes before? What happened?

If the user provides partial information, probe specifically on the gaps — an accurate dysfunction diagnosis requires all six inputs.

## Step 3: Diagnose Position on the Five Dysfunctions Pyramid

Map the team's current state against each layer of Lencioni's pyramid, bottom to top:

### Layer 1: Absence of Trust (Foundation)
- **Indicators assessed**: Willingness to admit mistakes, ask for help, acknowledge weaknesses, give benefit of the doubt
- **Diagnostic questions to apply**: Do team members know each other's personal histories and behavioural styles? Do they apologise genuinely? Do they volunteer weaknesses in group settings?
- **Edmondson overlay**: Score the team on the 7-item psychological safety scale (belief that the team is safe for interpersonal risk-taking)

### Layer 2: Fear of Conflict
- **Indicators assessed**: Quality of debate in meetings, presence of "back-channel" discussions, speed to artificial consensus, avoidance of contentious topics
- **Diagnostic questions to apply**: When was the last time two executives openly disagreed in a group setting and resolved it productively? Are meetings described as "boring" or "efficient" (often a euphemism for conflict-avoidant)?

### Layer 3: Lack of Commitment
- **Indicators assessed**: Clarity of decisions made, revisiting of settled issues, hedging language in communications, ambiguity in who owns what
- **Diagnostic questions to apply**: After a decision, can every team member articulate what was decided and why — even if they initially disagreed?

### Layer 4: Avoidance of Accountability
- **Indicators assessed**: Willingness to call out peer underperformance, reliance on the leader as sole accountability mechanism, tolerance of low standards
- **Diagnostic questions to apply**: Do team members address behavioural or performance concerns directly with each other, or does everything route through the CEO/leader?

### Layer 5: Inattention to Results
- **Indicators assessed**: Prioritisation of individual/departmental goals over collective outcomes, status-seeking behaviour, ego-driven decision-making
- **Diagnostic questions to apply**: Does the team have a single, shared scoreboard? When the team wins collectively, does it feel more important than individual wins?

Assign each layer a maturity rating:
- **Red (Dysfunctional)**: Dysfunction is active and visibly degrading team performance
- **Amber (Fragile)**: Some positive behaviours present but inconsistent; reverts under stress
- **Green (Functional)**: Healthy norms established and self-reinforcing

Identify the **primary bottleneck layer** — the lowest Red or Amber layer, since the pyramid is sequential and higher layers cannot stabilise without the foundation beneath them.

## Step 4: Deliver the Team Safety Diagnostic & Leadership Action Plan

Produce the following structured deliverables:

### Deliverable A: Five Dysfunctions Diagnostic Scorecard

| Dysfunction Layer | Maturity Rating | Key Evidence | Impact on Executive Ideation Quality |
|---|---|---|---|
| Absence of Trust | Red / Amber / Green | [Specific observed behaviours] | [How this suppresses honest brainstorming] |
| Fear of Conflict | Red / Amber / Green | [Specific observed behaviours] | [How this produces groupthink] |
| Lack of Commitment | Red / Amber / Green | [Specific observed behaviours] | [How this kills execution of ideas] |
| Avoidance of Accountability | Red / Amber / Green | [Specific observed behaviours] | [How this erodes standards] |
| Inattention to Results | Red / Amber / Green | [Specific observed behaviours] | [How this fragments strategic focus] |

**Primary Bottleneck Layer**: [Identified layer]
**Edmondson Psychological Safety Estimate**: [Low / Moderate / High] with rationale

### Deliverable B: Leadership Intervention Playbook (90-Day Sprint)

Structured as three phases, with specific moves — not platitudes:

**Phase 1: Vulnerability-First Leadership (Weeks 1–3)**
- **The Leader Goes First**: Script 2–3 specific vulnerability disclosures the leader can make at the next team meeting (e.g., "I got the pricing decision wrong last quarter because I was anchored to sunk costs — here's what I've learned"). Tailor to the leader's actual context.
- **Personal History Exercise**: Design a structured 90-minute session agenda where each executive shares formative professional experiences — specific prompts provided, not open-ended
- **Behavioural Profiling Debrief**: Recommend a specific instrument (DISC, Hogan, Enneagram for executive teams) and design the debrief session format

**Phase 2: Mining for Conflict (Weeks 4–7)**
- **Conflict Norming Session**: Draft a team conflict charter — explicit agreements on how the team will disagree (e.g., "We commit to real-time objections rather than post-meeting dissent")
- **Real-Time Mining Techniques**: Provide the leader with 5 specific facilitation phrases to surface buried disagreement during meetings (e.g., "I sense some hesitation — what's the strongest counter-argument to what we just agreed?")
- **Designated Dissenter Protocol**: Design a rotating "red team" role for executive meetings with specific responsibilities and protection norms
- **Topic-Specific Conflict Agenda**: Identify 2–3 "undiscussable" topics the team is avoiding and design a structured debate format for each

**Phase 3: Commitment & Accountability Architecture (Weeks 8–12)**
- **Cascading Communication Protocol**: After each executive decision, require a written "commitment statement" — what was decided, who dissented and why they can still commit, and what each person owns
- **Peer Accountability Pairings**: Design a structured peer check-in format (bi-weekly, 30 minutes) with specific conversation guides
- **Collective Scoreboard**: Design 3–5 team-level (not departmental) metrics that the executive team publicly tracks and discusses weekly

### Deliverable C: Psychological Safety Pre-Check for Brainstorming Sessions

A diagnostic checklist the leader runs before any strategic ideation session to confirm minimum safety conditions are met:

1. [ ] Every participant can name one mistake they've made this quarter without discomfort
2. [ ] At least two genuine disagreements have been resolved productively in the last 30 days
3. [ ] No participant has a known unresolved interpersonal conflict with another participant
4. [ ] The leader has publicly changed their mind based on team input in the last 60 days
5. [ ] Meeting norms explicitly protect dissent and separate idea critique from personal critique

**Verdict**: If fewer than 3 boxes are checked, prioritise team-building interventions before running ideation sessions — the output will be self-censored and unreliable.

Apply any user-specific `instructions` from FutureProof context to adjust language, frameworks, or cultural considerations.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="team-safety-and-conflict-builder", experiment={
  hypothesis: "Leader vulnerability disclosure at the opening of the next 3 executive meetings will increase unprompted dissent and counter-proposals by team members",
  variants: ["control: leader opens with agenda and status updates as usual", "variant: leader opens with a personal vulnerability disclosure or admission of a recent mistake before transitioning to agenda"],
  measurement: "Count of unprompted dissenting viewpoints raised during the meeting, tracked over 3 consecutive sessions per condition",
  expected_impact: "40% increase in productive conflict episodes per meeting within 6 weeks"
})
```

```
FutureProof:save_experiment(skill="team-safety-and-conflict-builder", experiment={
  hypothesis: "Implementing a Designated Dissenter rotation increases decision quality by surfacing risks that would otherwise go unvoiced",
  variants: ["control: standard meeting facilitation", "variant: rotating red-team member with explicit mandate to argue the counter-position on each major decision"],
  measurement: "Post-decision review at 90 days — percentage of decisions that required significant course correction",
  expected_impact: "25% reduction in decision reversals within one quarter"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="team-safety-and-conflict-builder",
  query="Latest empirical research on psychological safety interventions in C-suite and executive teams 2023-2024, including Edmondson's updated frameworks, Lencioni practitioner case studies, and measurable outcomes of vulnerability-based trust programmes in Fortune 500 leadership teams",
  reason="Ensure diagnostic criteria and intervention recommendations reflect current evidence base and avoid outdated or debunked team-building practices; calibrate expected impact timelines based on peer-reviewed longitudinal studies"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="team-safety-and-conflict-builder", session={
  summary: "Diagnosed [team name/company] executive team against Lencioni's Five Dysfunctions pyramid; primary bottleneck identified at [Layer X: dysfunction name]; delivered 90-day Leadership Intervention Playbook and Psychological Safety Pre-Check for upcoming [catalyst event]",
  key_findings: ["Primary dysfunction layer: [layer and rating]", "Leader vulnerability posture: [score/5]", "Critical undiscussable topics identified: [topics]", "Estimated time to minimum brainstorming-ready safety: [weeks]"],
  user_feedback: null
})
```