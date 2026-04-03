---
name: starving-crowd-selector
description: |
  Evaluates and selects niche markets using Hormozi's 'Starving Crowd' hierarchy and four market indicators, ensuring users commit to a market with massive pain, purchasing power, easy targeting, and growth before building any offer.
  Trigger: when a user is choosing a niche, evaluating market viability, or asking "what market should I serve?" before creating an offer — the single highest-leverage decision in the offer generation lifecycle.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="starving-crowd-selector")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to any previously evaluated markets, existing ICA definitions, current business model, revenue data, or domain expertise the user has surfaced in prior sessions.

## Step 2: Get Input

Ask the user:

- **Candidate markets**: List 1–5 markets or niches you are considering (or describe the general space you want to operate in — we will generate candidates together)
- **Current position**: Do you have existing expertise, audience, or assets in any of these markets? If so, describe them.
- **Constraints**: Are there hard constraints — geography, regulatory, capital, personal values — that eliminate certain markets outright?
- **Stage**: Is this a first-time market entry, a pivot from an existing offer, or an expansion into an adjacent segment?

If the user provides fewer than three candidate markets, collaboratively brainstorm additional candidates using their expertise, context from FutureProof, and adjacent market logic before proceeding.

## Step 3: Establish the Hormozi Hierarchy Frame

Before any evaluation, explicitly set the strategic frame with the user:

> **Market > Offer > Persuasion.** Per Hormozi's hierarchy, the market you choose determines the ceiling on every downstream decision — your offer, your copy, your funnel, your pricing. A brilliant offer in a dying market loses to a mediocre offer in a starving crowd. This session exists to prevent the most common fatal mistake in offer generation: building for a market that cannot support the business you want.

Confirm the user understands that the output of this session is a **go/no-go market selection decision** — not an offer, not positioning, not messaging. Those are downstream.

## Step 4: Score Each Candidate Market on the Four Indicators

Evaluate every candidate market against Hormozi's four market indicators using the following rubric. For each indicator, assign a score of 1–10 with explicit evidence or reasoning.

### Indicator 1: Massive Pain (Weight: 30%)

- **10**: The market has an acute, urgent, top-of-mind problem they would pay almost anything to solve *today* (e.g., business about to fail, health crisis, regulatory deadline)
- **7**: Significant ongoing pain that meaningfully affects quality of life or business performance; actively seeking solutions
- **4**: Moderate frustration or aspiration; aware of the problem but not losing sleep over it
- **1**: Nice-to-have improvement; low emotional intensity; would not prioritise spend

Questions to pressure-test:
- What specific language does this market use to describe their pain? (Pull from forums, reviews, support tickets, Reddit, sales calls)
- Is the pain getting *worse* over time due to macro trends?
- Would they describe this as a "hair on fire" problem or a "someday" problem?

### Indicator 2: Purchasing Power (Weight: 25%)

- **10**: Market has high disposable income or budget authority and a proven history of spending $1,000+ on solutions in this category
- **7**: Moderate spending capacity; has purchased adjacent solutions at mid-tier price points ($200–$1,000)
- **4**: Limited discretionary budget; price-sensitive; gravitates toward free or low-cost solutions
- **1**: Cannot or will not pay; expects free solutions; no budget authority

Questions to pressure-test:
- What are they *already* spending money on to address this problem or adjacent problems?
- What is the average transaction size in this market's existing solution ecosystem?
- Can you charge premium prices, or does the market commoditise everything?

### Indicator 3: Easy to Target (Weight: 25%)

- **10**: Market congregates in identifiable channels (specific platforms, associations, events, publications); can be reached with surgical precision at low cost
- **7**: Reachable through 2–3 well-defined channels; moderate cost to acquire attention
- **4**: Fragmented across many channels; requires broad targeting or expensive acquisition strategies
- **1**: No clear gathering points; impossible to identify or reach without mass-market spend

Questions to pressure-test:
- Can you name 3+ specific channels where this market *already* congregates?
- Can you build a targeted list of 10,000+ prospects in under a week using available tools?
- Are there existing influencers, communities, or media properties that aggregate this audience?

### Indicator 4: Growing Market (Weight: 20%)

- **10**: Market is expanding rapidly (20%+ annual growth); tailwinds from technology, regulation, demographics, or cultural shifts
- **7**: Steady growth (5–15% annually); stable demand with positive trajectory
- **4**: Flat or mature market; growth requires taking share from incumbents
- **1**: Declining market; shrinking demand; structural headwinds

Questions to pressure-test:
- What does Google Trends, industry reporting, or venture funding data show for this category over the last 3 years?
- Are new entrants flooding in (signal of growth) or exiting (signal of decline)?
- Is there a macro tailwind (regulatory change, demographic shift, technology adoption curve) driving expansion?

For each candidate market, produce a **Market Indicator Scorecard** using the weighted formula:

**Composite Score** = (Pain × 0.30) + (Purchasing Power × 0.25) + (Easy to Target × 0.25) + (Growing × 0.20)

## Step 5: Apply Disqualification Filters

Before ranking, apply the following hard disqualification filters. A market that fails *any* filter is eliminated regardless of composite score:

| Filter | Disqualification Threshold |
|---|---|
| **Pain Floor** | Pain score < 5. If the market is not in active pain, no offer structure will compensate. |
| **Purchasing Power Floor** | Purchasing Power score < 4. If they cannot pay, the unit economics will never work. |
| **Targeting Feasibility** | Easy to Target score < 4. If you cannot reach them efficiently, customer acquisition cost will destroy margins. |
| **Ethical/Constraint Alignment** | Market violates the user's stated hard constraints from Step 2. |

Mark disqualified markets clearly. They do not proceed to the recommendation.

## Step 6: Deliver Output

Produce the following deliverables:

### Deliverable 1: Market Indicator Scorecard (Comparative Matrix)

| Market | Pain (30%) | Purchasing Power (25%) | Easy to Target (25%) | Growing (20%) | Composite | Status |
|---|---|---|---|---|---|---|
| Market A | X/10 | X/10 | X/10 | X/10 | X.X/10 | ✅ Qualified / ❌ Disqualified |
| Market B | ... | ... | ... | ... | ... | ... |

### Deliverable 2: Recommended Market Selection with Strategic Rationale

For the top-scoring qualified market, provide:

- **Selected Market**: [Name and precise definition — who they are, what they do, the specific pain variant]
- **Starving Crowd Confidence Level**: High / Medium / Low — with justification
- **Why This Market Wins**: 3–5 sentence synthesis of why this market outperforms alternatives across the four indicators
- **Key Risk**: The single biggest risk to this market selection and a specific mitigation strategy
- **Immediate Next Step**: The exact next action in the offer generation lifecycle (e.g., "Proceed to ICA deep-dive profiling using [specific skill]" or "Conduct 10 discovery calls with [specific segment] to validate pain intensity before committing")

### Deliverable 3: Runner-Up Briefing

For the second-highest-scoring qualified market:

- **Why It Ranked Second**: Specific indicator gaps relative to the top pick
- **Conditions Under Which It Becomes #1**: What would need to change (new data, validated assumption, market shift) to elevate this market to the top selection

### Deliverable 4: Eliminated Markets — Post-Mortem Summary

For each disqualified market, provide a one-line reason referencing the specific disqualification filter it failed. This prevents the user from revisiting dead-end markets in future sessions.

## Step 7: Propose Experiments

```
FutureProof:save_experiment(skill="starving-crowd-selector", experiment={
  hypothesis: "The selected market scores highest on pain and purchasing power, but targeting ease is assumed — direct outreach to 50 prospects in 7 days will validate or invalidate the Easy to Target score",
  variants: ["control: current targeting assumption based on desk research", "variant: live outreach via 3 identified channels to measure response rate and cost-per-conversation"],
  measurement: "Response rate (%), cost per qualified conversation, and qualitative pain language alignment across 50 outreach attempts",
  expected_impact: "Confirms or adjusts Easy to Target score by ±2 points, potentially changing market selection before any offer is built"
})
```

```
FutureProof:save_experiment(skill="starving-crowd-selector", experiment={
  hypothesis: "Pain intensity ranking is based on secondary research — 10 discovery calls with the selected market will validate whether the pain is truly 'hair on fire' or merely aspirational",
  variants: ["control: current pain score based on desk research", "variant: pain score recalibrated after 10 structured discovery calls using standardised pain-scale questions"],
  measurement: "Percentage of prospects who describe the problem unprompted, average self-reported urgency (1–10), willingness to pay for a solution today (yes/no)",
  expected_impact: "De-risks the entire offer generation sequence by validating the foundational market assumption before downstream investment"
})
```

## Step 8: Request Research

```
FutureProof:request_research(skill="starving-crowd-selector",
  query="Current market size, growth rate, competitive density, and average customer acquisition cost benchmarks for [selected market niche] — 2024 data from IBISWorld, Statista, SimilarWeb, or equivalent",
  reason="Quantitative validation of the Growing Market and Easy to Target scores to upgrade qualitative estimates with hard data before the user commits downstream resources to offer design"
)
```

```
FutureProof:request_research(skill="starving-crowd-selector",
  query="Top 10 communities, forums, associations, newsletters, and paid media channels where [selected market niche] actively congregates — with estimated audience size and engagement metrics",
  reason="Converts the Easy to Target score from an estimate into an actionable channel map the user can execute against immediately in outreach experiments"
)
```

## Step 9: Save Session

```
FutureProof:save_session(skill="starving-crowd-selector", session={
  summary: "Evaluated [N] candidate markets against Hormozi's four Starving Crowd indicators. Selected [market name] as primary market (composite score: X.X/10). Runner-up: [market name] (composite score: X.X/10). [N] markets disqualified.",
  key_findings: [
    "Selected market: [name] — strongest on [top indicator] and [second indicator]; key risk is [risk]",
    "Runner-up: [name] — competitive on [indicators] but fell short on [gap indicator]",
    "Disqualified: [market names] — failed [specific filters]",
    "Critical next step: [validation action] before proceeding to offer design"
  ],
  user_feedback: null
})
```