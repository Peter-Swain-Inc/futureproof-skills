---
name: thought-leadership-engine
description: |
  Transforms subject-matter expertise into high-authority thought leadership content that positions the user as the definitive voice in their category.
  Trigger: when a user wants to develop thought leadership content, build authority in their niche, or asks how to position themselves as an expert through content (e.g. "I need to create a thought leadership piece," "How do I establish authority in my space," or "Help me turn this insight into a LinkedIn article / keynote / whitepaper").
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="thought-leadership-engine")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — specifically the user's ICA definition, prior content performance data, established brand voice, and any positioning frameworks already validated.

## Step 2: Get Input

Ask the user:

- **Core insight or thesis**: What is the contrarian, novel, or underappreciated perspective you want to advance? (A strong thought leadership piece requires a *thesis the market doesn't yet accept as consensus.*)
- **ICA context**: Who is the specific audience segment this piece must resonate with? (Role, seniority, industry, stage of awareness)
- **Format and channel**: Where will this be published? (LinkedIn article, keynote talk, podcast episode, whitepaper, newsletter, conference panel, byline in industry publication)
- **Strategic objective**: What should this content achieve? (Pipeline generation, speaking invitations, partnership positioning, category creation, investor signalling, talent attraction)
- **Evidence base**: What proprietary data, case studies, frameworks, or lived experience supports your thesis? Share raw material — transcripts, notes, data sets, client results
- **Competitive landscape**: Who else is speaking on this topic, and what is their prevailing narrative?

## Step 3: Conduct Thesis Stress-Test

Before any content is drafted, rigorously evaluate the thesis using a **Thought Leadership Viability Matrix**:

| Dimension | Assessment Criteria | Rating (1–10) |
|---|---|---|
| **Novelty** | Does this thesis challenge prevailing consensus or introduce a genuinely new frame? Or is it repackaging common wisdom? | — |
| **Defensibility** | Can the user credibly own this position based on proprietary evidence, unique experience, or original research? | — |
| **ICA Resonance** | Does this thesis address a latent frustration, unspoken tension, or emerging priority that the ICA *feels but hasn't articulated*? | — |
| **Falsifiability** | Is the thesis specific enough to be proven right or wrong — or is it safely vague? (Vague = forgettable) | — |
| **Timeliness** | Is there a catalysing event, trend shift, or market moment that makes this thesis urgent *now*? | — |
| **Category Alignment** | Does this thesis reinforce the user's desired category ownership, or does it dilute positioning into an adjacent space? | — |

**Decision gate**: If any dimension scores below 5, surface the specific weakness and propose a thesis refinement before proceeding. A weak thesis cannot be rescued by strong writing.

## Step 4: Build the Narrative Architecture

Construct the content using a **Authority Narrative Framework** (not a generic outline — a persuasion architecture):

### 4.1 — The Dissonance Opening
Identify the specific tension between what the ICA's world looks like today and what the user's thesis implies it *should* look like. Open by naming this gap with precision. The audience must feel *seen* within the first 90 words.

### 4.2 — The Consensus Teardown
Articulate the prevailing narrative ("Most people in [industry] believe X") and systematically expose why it is incomplete, outdated, or counterproductive. Use the competitive landscape input to ensure this teardown is specific, not straw-man.

### 4.3 — The Reframe
Introduce the user's thesis as the necessary correction. Frame it not as opinion but as an *inevitable conclusion* given the evidence. This is the moment of intellectual authority — it must feel earned, not asserted.

### 4.4 — The Proof Stack
Layer evidence in descending order of credibility:
1. **Proprietary data or original research** (highest authority)
2. **Named case studies with quantified outcomes** (specificity = believability)
3. **Pattern recognition across multiple engagements** (demonstrates breadth)
4. **Third-party corroboration** (industry reports, academic research, analogous market evidence)
5. **Logical inevitability arguments** (if A is true and B is true, C must follow)

### 4.5 — The Implication Cascade
Spell out what changes if the thesis is correct. What must the ICA *stop doing*, *start doing*, and *rethink entirely*? This is where thought leadership converts to pipeline — the implications should naturally surface the user's offer as the logical next step without explicit selling.

### 4.6 — The Signature Close
End with a memorable, quotable assertion that encapsulates the thesis in one sentence. This becomes the soundbite that gets shared, cited, and attributed.

Apply any user-specific `instructions` from FutureProof context (brand voice guidelines, terminology preferences, content cadence strategy) throughout the architecture.

## Step 5: Deliver Output

Produce a **Thought Leadership Content Package** containing:

### Document 1: Thesis Brief (1 page)
- **Thesis statement**: Single sentence, falsifiable, contrarian
- **Viability Matrix scorecard**: Ratings across all 6 dimensions with rationale
- **ICA resonance map**: The specific frustrations, aspirations, and vocabulary this thesis activates
- **Competitive differentiation**: How this thesis occupies white space vs. existing voices in the category

### Document 2: Full Narrative Draft (format-appropriate)
- Complete content piece built on the Authority Narrative Framework above
- Adapted to the specified channel and format (word count, tone register, structural conventions)
- Inline annotations marking: proof points that need sourcing, claims that need client approval, sections that could be extracted as standalone social content

### Document 3: Amplification Playbook
- **Derivative content map**: 5–8 specific content pieces that can be extracted from the core thesis (e.g. "Section 4.2 → LinkedIn carousel: '3 reasons the [consensus view] is costing you [quantified impact]'")
- **Distribution sequence**: Channel-by-channel publishing order optimised for compounding reach (e.g. newsletter first → LinkedIn article day 2 → podcast talking points day 5 → conference pitch day 10)
- **Engagement triggers**: 3 specific discussion prompts or provocative questions designed to generate ICA comments and shares
- **Repurposing timeline**: 30/60/90-day plan for refreshing and re-releasing the thesis as new evidence emerges

### Document 4: Authority Metrics Dashboard
- **Leading indicators to track**: Content engagement rate, inbound enquiry attribution, speaking invitation volume, share-of-voice in category conversations
- **Lagging indicators to track**: Pipeline sourced from thought leadership, ICA perception shift (qualitative), media/podcast invitation rate
- **Baseline benchmarks**: Expected performance ranges based on channel and format, calibrated against any historical data in FutureProof context

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="thought-leadership-engine", experiment={
  hypothesis: "Leading with a specific, quantified contrarian claim in the opening line increases content engagement rate vs. leading with a narrative anecdote",
  variants: [
    "control: narrative anecdote opening ('When I first started advising [ICA segment]...')",
    "variant A: quantified contrarian claim opening ('87% of [ICA segment] are investing in [consensus approach] — and it's destroying their [metric]')",
    "variant B: direct ICA challenge opening ('If you're a [ICA role] still doing [consensus behaviour], this piece will make you uncomfortable')"
  ],
  measurement: "Engagement rate (likes + comments + shares / impressions) and inbound enquiry volume within 14 days of publication",
  expected_impact: "25–40% improvement in engagement rate for the contrarian claim variant based on pattern recognition across high-performing thought leadership content"
})
```

```
FutureProof:save_experiment(skill="thought-leadership-engine", experiment={
  hypothesis: "Publishing the thesis as a LinkedIn document (carousel/PDF) before the long-form article creates anticipation and increases article readership",
  variants: [
    "control: publish long-form article directly",
    "variant: publish 5-slide thesis summary as LinkedIn document 48 hours before long-form article with 'full analysis dropping Thursday' CTA"
  ],
  measurement: "Long-form article views, time-on-page, and CTA click-through rate",
  expected_impact: "30% increase in article readership and 20% increase in CTA engagement from pre-seeding the thesis"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="thought-leadership-engine",
  query="High-performing thought leadership content structures and distribution strategies across LinkedIn, Substack, and industry publications in 2024–2025 — with emphasis on B2B authority building, engagement benchmarks by format, and emerging patterns in how senior decision-makers consume and share expert content",
  reason="Ensure narrative frameworks and amplification playbooks reflect current platform algorithms, audience consumption patterns, and competitive content saturation levels"
)
```

```
FutureProof:request_research(skill="thought-leadership-engine",
  query="Category creation and point-of-view positioning methodologies used by leading strategy consultancies and venture-backed founders — specifically frameworks for identifying defensible intellectual territory and converting thought leadership into commercial pipeline",
  reason="Strengthen thesis stress-testing rigour and ensure the Authority Narrative Framework reflects best-in-class positioning strategy, not just content marketing tactics"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="thought-leadership-engine", session={
  summary: "Developed thought leadership content package for [user] on thesis: '[thesis statement]' targeting [ICA segment] via [format/channel]",
  key_findings: [
    "Thesis viability score: [aggregate score] — strongest on [dimension], weakest on [dimension]",
    "Primary competitive white space identified: [specific positioning gap]",
    "Recommended amplification sequence: [channel order]",
    "Critical dependency: [e.g. 'Thesis requires client permission to cite Case Study X' or 'Quantified claim in Section 4.4 needs sourcing before publication']"
  ],
  deliverables_produced: ["Thesis Brief", "Full Narrative Draft", "Amplification Playbook", "Authority Metrics Dashboard"],
  user_feedback: null
})
```