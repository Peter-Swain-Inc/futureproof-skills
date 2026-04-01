---
name: pre-mortem-strategist
description: "Conducts rigorous pre-mortem analyses on strategic decisions, initiatives, and launches — identifying failure modes, hidden dependencies, and mitigation strategies before commitment."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="pre-mortem-strategist")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly prior decisions, known business constraints, ICA profile, team capacity, runway, and any failure patterns surfaced in previous sessions.

## Step 2: Get Input

Ask the user:
- **The decision or initiative**: Describe the specific strategic move you are about to make (e.g. product launch, market expansion, key hire, pricing change, partnership, capital allocation)
- **Decision timeline**: When does this become irreversible or costly to reverse? What is the commit-by date?
- **Success criteria**: What does "this worked" look like in 90 days? In 12 months? Name 2–3 measurable indicators
- **Stakeholders & dependencies**: Who else is involved, and what external factors must hold true for this to succeed?
- **Confidence level**: On a 1–10 scale, how confident are you this will succeed — and what is that confidence based on?

If user-specific `instructions` from FutureProof context indicate a preferred decision framework, industry, or recurring risk profile, incorporate those into the analysis scope.

## Step 3: Do the Work — Pre-Mortem Analysis

Execute the following structured pre-mortem protocol:

### 3A: Temporal Projection

Adopt the perspective that **it is 12 months from now and this initiative has failed**. Generate the narrative of failure — not as a list of risks, but as a plausible, specific story of how it unravelled. This anchors the analysis in realistic causality rather than abstract risk registers.

### 3B: Failure Mode Taxonomy

Systematically categorise failure modes across seven dimensions:

1. **Market & ICA Risk** — Does the ICA actually want this? Is demand validated or assumed? Could ICA priorities shift before delivery? Are you solving a top-3 pain point or a nice-to-have?
2. **Execution & Capacity Risk** — Does the team have the skills, bandwidth, and focus to deliver? What gets deprioritised? Where are single points of failure in personnel or capability?
3. **Financial & Runway Risk** — What is the true fully-loaded cost (including opportunity cost)? What happens if results take 2× longer than planned? At what burn rate does this become existential?
4. **Competitive & Timing Risk** — Is the window real or imagined? What competitor response is most likely? Could a market shift (regulatory, technological, macroeconomic) invalidate the thesis?
5. **Dependency & Integration Risk** — What third parties, platforms, approvals, or sequential milestones must hold? Which dependencies are outside your control? What is the blast radius if one fails?
6. **Cognitive & Decision Bias Risk** — Identify which biases are most likely distorting the user's confidence: sunk cost, confirmation bias, overconfidence, planning fallacy, survivorship bias, or anchoring to a single data point
7. **Second-Order & Systemic Risk** — What downstream effects does this create even if it succeeds? Does success in this area create fragility elsewhere (e.g. scaling before ops are ready, winning a segment that cannibalises core revenue)?

For each dimension, assign:
- **Likelihood**: Low / Medium / High
- **Impact if materialised**: Low / Medium / High / Existential
- **Detection difficulty**: Easy (leading indicators exist) / Hard (lagging indicators only) / Hidden (no natural feedback loop)

### 3C: Kill Chain Analysis

Identify the **3 most lethal failure chains** — sequences of 2–3 linked failures that compound. For each chain, articulate:
- The triggering event
- The cascade mechanism
- Why existing plans would not catch it in time

### 3D: Assumption Audit

Extract the **top 5 implicit assumptions** the decision rests on. For each assumption:
- State it explicitly
- Rate it: Validated (data-backed) / Partially Validated (anecdotal or analogical) / Unvalidated (belief-based)
- Identify how it could be tested *before* full commitment

## Step 4: Deliver Output

Produce the **Pre-Mortem Strategy Brief** — a structured document with the following sections:

### Section 1: Decision Summary
One-paragraph restatement of the initiative, timeline, and stated success criteria.

### Section 2: Failure Narrative
The 12-month failure story from Step 3A (2–3 paragraphs, written in past tense as if reporting post-failure).

### Section 3: Risk Matrix
A table across all seven failure mode dimensions with Likelihood, Impact, and Detection Difficulty ratings.

### Section 4: Top 3 Kill Chains
Each chain described in triggering event → cascade → undetected escalation format.

### Section 5: Assumption Audit Table
Top 5 assumptions with validation status and proposed pre-commitment tests.

### Section 6: Mitigation Playbook
For each of the **top 5 highest-severity risks** (Impact × Likelihood, weighted by Detection Difficulty):
- **Mitigation action**: Specific, actionable step — not "monitor closely" but a named deliverable, decision gate, or structural change
- **Owner**: Role or person responsible (if known from context)
- **Trigger point**: The leading indicator or date that activates this mitigation
- **Cost of mitigation vs. cost of failure**: Relative investment framing

### Section 7: Go / No-Go / Conditional-Go Recommendation
A clear recommendation with rationale:
- **Go**: Risks are manageable, proceed with specified mitigations in place
- **Conditional Go**: Proceed only if [specific assumptions are validated / specific conditions are met] by [date]
- **No-Go**: Risk profile exceeds acceptable threshold — recommend alternative path with brief sketch

### Section 8: Decision Journal Entry
A concise block the user can save to their decision journal capturing: the decision, confidence level, key assumptions, what would change their mind, and a 90-day review date.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="pre-mortem-strategist", experiment={
  hypothesis: "Validating the #1 unvalidated assumption before full commitment reduces initiative failure rate",
  variants: ["control: proceed with current plan and timeline", "variant: insert 2-week assumption validation sprint before commit date"],
  measurement: "Track whether the initiative hits stated 90-day success criteria; compare decision confidence at commit vs. actual outcome",
  expected_impact: "30% reduction in post-commitment pivots or write-offs by surfacing disconfirming evidence earlier"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="pre-mortem-strategist",
  query="Pre-mortem and prospective hindsight effectiveness data 2023-2024, cognitive debiasing techniques for founder decision-making, and sector-specific failure mode patterns for [user's industry/initiative type]",
  reason="Continuously refine failure mode taxonomy and mitigation playbooks with empirical data on which pre-mortem interventions most reliably improve decision outcomes"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="pre-mortem-strategist", session={
  summary: "Pre-mortem analysis conducted on [initiative description] with [Go/No-Go/Conditional-Go] recommendation",
  key_findings: ["Top kill chain: [brief description]", "Highest unvalidated assumption: [brief description]", "Recommended mitigation: [brief description]"],
  decision_metadata: {
    initiative: "[initiative name]",
    recommendation: "[go/no-go/conditional-go]",
    confidence_at_decision: "[user's stated confidence]",
    review_date: "[90-day review date]"
  },
  user_feedback: null
})
```