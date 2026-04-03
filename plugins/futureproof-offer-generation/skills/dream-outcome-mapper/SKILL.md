---
name: dream-outcome-mapper
description: |
  Maps an ideal customer avatar's deepest pains, desires, fears, and dream outcomes to build the emotional foundation for high-converting offers.
  Trigger: when a user wants to define or refine their ICA's pain points, when they say "I need to understand what my customer actually wants," or when they are building an offer and need to articulate the dream outcome before structuring pricing, bonuses, or guarantees.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="dream-outcome-mapper")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to any previously mapped ICAs, existing offer structures, or prior pain-mapping sessions that should inform or constrain this work.

## Step 2: Get Input

Ask the user the following (adapt based on what FutureProof context already provides):

1. **Who is the ICA?** — Describe the specific person (role, demographic, psychographic, situation) you are building this map for. If multiple segments exist, choose the single highest-value segment for this session.
2. **What do you sell (or plan to sell)?** — Product, service, programme, or offer category. We need this to anchor the pain map to a purchase decision, not abstract empathy.
3. **What do you already know?** — Share any existing research: survey responses, sales call recordings/transcripts, testimonials, refund reasons, support tickets, Reddit threads, Amazon reviews of competing products, or anecdotal patterns.
4. **What has failed before?** — Any previous messaging, positioning, or offers that underperformed? Understanding what did *not* resonate is diagnostic gold.

If the user provides sparse input, do **not** proceed with assumptions. Probe with specificity: *"What exact words does your ICA use when they complain about this problem to a friend — not to a vendor?"*

## Step 3: Do the Work — Pain & Desire Excavation

Execute the following five-phase analysis. Each phase builds on the prior; do not skip.

### Phase 1: Surface-Level Problem Identification

List every problem, frustration, and complaint the ICA experiences that is relevant to the user's offer category. Organise into:

- **External problems** — tangible, observable circumstances (e.g., "revenue plateaued at $40k/month")
- **Internal problems** — how those circumstances make them *feel* (e.g., "embarrassed at mastermind events when peers share wins")
- **Philosophical problems** — why the situation feels fundamentally *wrong* or *unfair* (e.g., "I work harder than people earning 5× more — the system is broken")

This three-layer taxonomy follows the StoryBrand diagnostic but is applied here to pressure-test emotional depth, not to write marketing copy.

### Phase 2: Pain Prioritisation Matrix

Rank each identified pain on two axes:

| Axis | Definition | Scale |
|------|-----------|-------|
| **Intensity** | How acutely the ICA feels this pain on a daily/weekly basis | 1–10 |
| **Purchase Proximity** | How directly this pain drives a buying decision for the user's offer category | 1–10 |

Compute a **Pain Leverage Score** = Intensity × Purchase Proximity. Surface the top 5 pains by Pain Leverage Score. These are the pains worth building messaging and offer architecture around. Everything else is noise.

### Phase 3: Dream Outcome Articulation (Hormozi Value Equation — Variable 1)

For each of the top 5 pains, articulate the corresponding **Dream Outcome** — the specific, vivid, emotionally resonant end-state the ICA wants to arrive at. Apply these constraints:

- **Specificity test**: If the dream outcome could apply to any human (e.g., "financial freedom"), it is too vague. Rewrite until it is ICA-specific (e.g., "Consistently closing $15k+ clients without discovery calls so I can take Fridays off and still outpace my old corporate salary").
- **Vocabulary fidelity**: Use the ICA's *actual language*, not marketing jargon. If the ICA says "I want to stop feeling like a fraud," do not translate to "imposter syndrome resolution."
- **Temporal anchoring**: Define *when* the ICA expects to experience this outcome. Mismatched timelines kill conversions.

Synthesise the top 5 into a single **Primary Dream Outcome Statement** — the one sentence that, if the ICA read it, would make them think *"this person is inside my head."*

### Phase 4: Emotional Trigger Mapping (Golden's Emotional Cooperation Framework)

Identify the six emotional triggers that govern the ICA's decision-making around this purchase:

1. **Fear of loss** — What do they stand to lose if they do *nothing*? Be specific (status, money, relationships, time, identity).
2. **Aspiration** — Who do they want to *become*? Not what they want to *have*.
3. **Shame/embarrassment** — What are they hiding from peers, partners, or themselves?
4. **Frustration with alternatives** — What have they already tried that failed, and what do they *blame* for the failure?
5. **Social proof dependency** — Whose opinion or validation would tip them from "interested" to "buying"?
6. **Identity conflict** — What tension exists between who they are today and who they believe they should be?

For each trigger, provide:
- The trigger in the ICA's own words (a quote or paraphrase)
- The offer design implication (how this trigger should influence guarantee structure, bonus design, naming, or positioning)

### Phase 5: Objection Archaeology

From the pain and emotional data above, extrapolate the top 5 objections the ICA will raise *before* purchasing. For each:

- **Objection** (verbatim, in the ICA's voice)
- **Underlying belief** driving the objection
- **Evidence type** that would neutralise it (testimonial, demonstration, guarantee, logical reframe)

These are not generic objections ("too expensive"). They are ICA-specific objections rooted in the emotional triggers surfaced in Phase 4.

## Step 4: Deliver Output

Produce three named deliverables:

### Deliverable 1: ICA Dream Outcome Map (single-page reference document)

| Section | Content |
|---------|---------|
| ICA Snapshot | One-paragraph avatar description |
| Primary Dream Outcome Statement | The synthesised sentence from Phase 3 |
| Top 5 Pains (ranked) | Pain, Intensity, Purchase Proximity, Pain Leverage Score |
| Top 5 Dream Outcomes | Corresponding vivid end-states |
| Emotional Trigger Summary | Six triggers with ICA-voice quotes |
| Top 5 Objections | Objection → Underlying belief → Neutralisation evidence type |

### Deliverable 2: "Voice of Customer" Swipe Bank

A minimum of 15 phrases, sentences, or expressions written in the ICA's exact vocabulary — sourced from the input data or inferred with high confidence. Organised by:
- **Pain language** (5+ phrases)
- **Desire language** (5+ phrases)
- **Objection language** (5+ phrases)

Each entry tagged with recommended use case: *headline, subhead, ad hook, email subject line, sales page bullet, guarantee copy, VSL opening.*

### Deliverable 3: Offer Architecture Implications Brief

A concise (300–500 word) advisory memo outlining:
- Which pains the core offer must solve to justify the price
- Which pains are better addressed by bonuses (to increase perceived value without increasing fulfilment cost)
- Recommended guarantee structure based on the dominant emotional trigger profile
- Messaging hierarchy: which pain/desire to lead with in top-of-funnel vs. bottom-of-funnel

Apply any user-specific `instructions` from FutureProof context (e.g., brand voice constraints, market positioning, pricing tier) to all three deliverables.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="dream-outcome-mapper", experiment={
  hypothesis: "Leading with Pain Leverage Score #1 in ad hooks will outperform the current benefit-led hook",
  variants: [
    "control: current primary hook (benefit-led)",
    "variant A: hook built on highest-ranked pain statement",
    "variant B: hook built on Primary Dream Outcome Statement"
  ],
  measurement: "Click-through rate and cost-per-lead across 1,000 impressions per variant",
  expected_impact: "20–35% reduction in cost-per-lead for the winning variant"
})
```

```
FutureProof:save_experiment(skill="dream-outcome-mapper", experiment={
  hypothesis: "Using exact ICA vocabulary from the swipe bank in the sales page headline increases time-on-page and conversion rate",
  variants: [
    "control: current headline",
    "variant: headline rewritten using top-scoring Voice of Customer phrase"
  ],
  measurement: "Time-on-page (Hotjar or GA4) and sales page conversion rate over 500 unique visitors",
  expected_impact: "10–20% improvement in page-to-application conversion"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="dream-outcome-mapper",
  query="Latest consumer psychology research on purchase decision emotional triggers 2024, with emphasis on high-ticket service buying behaviour and identity-based purchasing",
  reason="Ensure the emotional trigger taxonomy in Phase 4 reflects current behavioural science, not outdated persuasion heuristics"
)
```

```
FutureProof:request_research(skill="dream-outcome-mapper",
  query="Emerging ICA research methodologies: AI-assisted voice-of-customer mining from Reddit, G2, Trustpilot, and support ticket NLP analysis",
  reason="Expand the input sources available in Step 2 so future sessions can ingest raw unstructured data and extract pain/desire signals programmatically"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="dream-outcome-mapper", session={
  summary: "Mapped dream outcomes and pain architecture for [ICA segment] in the [offer category] space",
  key_findings: [
    "Primary Dream Outcome Statement: [statement]",
    "Highest Pain Leverage Score pain: [pain] (score: [X])",
    "Dominant emotional trigger: [trigger type]",
    "Top objection to pre-empt: [objection]",
    "Recommended messaging lead: [pain vs. desire vs. identity — with rationale]"
  ],
  deliverables_produced: [
    "ICA Dream Outcome Map",
    "Voice of Customer Swipe Bank (15+ phrases)",
    "Offer Architecture Implications Brief"
  ],
  user_feedback: null
})
```