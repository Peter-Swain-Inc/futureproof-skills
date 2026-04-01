---
name: ad-creative-brief-generator
description: |
  Generates comprehensive ad creative briefs using FutureProof context, audience intelligence, and campaign strategy inputs.
  Trigger: when a user needs to produce a creative brief for a paid media campaign, or when they say "write a creative brief" or "I need ad creative direction for [platform/campaign]."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="ad-creative-brief-generator")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any previously defined ICA segments, brand voice guidelines, historical campaign performance data, and winning creative patterns.

## Step 2: Get Input

Ask the user to provide the following (pre-fill from FutureProof context where available):

- **Campaign objective**: What is the primary business outcome? (e.g., lead generation, product launch awareness, retargeting for conversion, event registration)
- **ICA segment**: Who is this ad targeting? Demographic, psychographic, and behavioural descriptors. What stage of awareness are they in — unaware, problem-aware, solution-aware, product-aware, or most-aware?
- **Platform(s)**: Where will this run? (Meta, Google, LinkedIn, TikTok, YouTube, programmatic display, etc.)
- **Offer / CTA**: What specific action should the audience take, and what is the value exchange?
- **Brand / product context**: Share any existing brand guidelines, product one-pagers, landing pages, or prior creative assets
- **Constraints**: Budget tier (affects production complexity), mandatory compliance or legal copy, format requirements (static, video, carousel, UGC-style), character/duration limits
- **Performance benchmarks**: Any historical CTR, CPA, ROAS, or hook-rate data from prior campaigns targeting this ICA segment

## Step 3: Do the Work

### 3A: ICA Insight Synthesis

Build an **ICA Creative Profile** that maps:

1. **Core desire**: The single transformation the ICA is seeking — articulated in their own language, not marketing jargon
2. **Primary pain catalyst**: The specific trigger event or escalating frustration that moves them from passive to active search
3. **Objection architecture**: The top 3 beliefs or fears that prevent them from clicking, engaging, or converting — ranked by friction intensity
4. **Attention environment**: How, when, and in what mindset they encounter ads on the specified platform (e.g., LinkedIn = professional identity mode; TikTok = entertainment-first scroll; Meta = social comparison context)
5. **Proof hierarchy**: Which forms of evidence this ICA segment trusts most — peer testimonials, data/statistics, authority endorsements, demonstration, or social volume

### 3B: Message Strategy Framework

Define the creative's strategic backbone using the **4C Message Architecture**:

| Layer | Definition | Output |
|-------|-----------|--------|
| **Claim** | The single most compelling promise this ad makes | One sentence, ≤15 words |
| **Conflict** | The enemy, obstacle, or status-quo tension the ad surfaces | Specific antagonist or friction point |
| **Credibility** | The proof mechanism that makes the claim believable | Named proof asset (case study, metric, endorsement) |
| **Catalyst** | The urgency or scarcity lever that compresses the decision timeline | Time-bound, quantity-bound, or consequence-bound trigger |

### 3C: Creative Execution Direction

For each requested format, specify:

1. **Hook strategy** (first 3 seconds / first visual scan):
   - Primary hook type: question, pattern interrupt, identity callout, shocking stat, or empathy mirror
   - Exact hook copy or visual direction — written out in full, not described abstractly

2. **Body narrative arc**:
   - For video: scene-by-scene breakdown with timing, on-screen text, voiceover/dialogue, and visual direction
   - For static/carousel: frame-by-frame layout with headline hierarchy, body copy, visual focal point, and information sequencing

3. **CTA construction**:
   - Button/end-card copy (primary and fallback variant)
   - Post-click expectation alignment — what the landing page must echo to maintain scent

4. **Visual and tonal direction**:
   - Colour palette rationale tied to emotional intent
   - Typography weight and style (e.g., bold sans-serif for urgency; editorial serif for authority)
   - Imagery style: photography vs. illustration vs. UGC vs. motion graphics — with specific reference direction
   - Talent direction (if applicable): demographic match to ICA, energy level, setting, wardrobe cues

### 3D: Variant Strategy

Produce a minimum of **3 creative variants** structured as an intentional test matrix:

| Variant | Variable Isolated | Hypothesis |
|---------|-------------------|-----------|
| A (Control) | Baseline creative aligned to strongest historical performer or best-practice benchmark | — |
| B | Alternate hook strategy | Tests whether [hook type] outperforms control for this ICA segment at [awareness stage] |
| C | Alternate proof mechanism or emotional angle | Tests whether [credibility/conflict shift] changes conversion behaviour |

Each variant must differ on **exactly one strategic variable** to ensure clean attribution of performance differences.

Apply any user-specific `instructions` from FutureProof context — including brand voice rules, compliance requirements, prior winning patterns, or ICA language banks.

## Step 4: Deliver Output

Produce the **Ad Creative Brief Document** with the following named sections:

### Document: Ad Creative Brief — [Campaign Name] — [Date]

1. **Brief Summary**: Campaign objective, ICA segment, platform(s), and offer — in ≤75 words
2. **ICA Creative Profile**: Full output from Step 3A
3. **Message Strategy (4C Architecture)**: Table from Step 3B
4. **Creative Executions**: Detailed direction per format from Step 3C, including:
   - Exact headline and body copy (not placeholders — production-ready draft copy)
   - Visual/scene direction detailed enough for a designer or video editor to execute without a follow-up call
5. **Variant Test Matrix**: Table and variant briefs from Step 3D
6. **Platform-Specific Specs**: Dimensions, aspect ratios, file requirements, character limits, and safe-zone guidance for each placement
7. **Compliance & Approval Checklist**: Legal/regulatory copy requirements, brand guideline adherence notes, and approval routing (if specified by user)
8. **Measurement Framework**: Primary KPI, secondary KPIs, and the specific metric thresholds that define a winning variant (e.g., "Variant wins if CTR exceeds control by ≥15% at 95% confidence after 5,000 impressions per variant")

Format: Structured markdown, ready to export to PDF or paste into a project management tool. Flag any sections requiring client/stakeholder input before production begins.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="ad-creative-brief-generator", experiment={
  hypothesis: "Leading with ICA pain catalyst in the hook (problem-agitation) outperforms aspiration-first hooks for [ICA segment] at [awareness stage] on [platform]",
  variants: ["control: aspiration-first hook emphasising desired outcome", "variant: pain-catalyst hook surfacing primary frustration before presenting solution"],
  measurement: "hook rate (3-second view rate for video; CTR for static) and downstream CPA across minimum 5,000 impressions per variant",
  expected_impact: "20% improvement in hook rate and 10% reduction in CPA for this ICA segment"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="ad-creative-brief-generator",
  query="Top-performing ad creative patterns and hook strategies on [platform] for [industry/ICA segment] in 2024–2025, including emerging format adoption rates and platform algorithm preferences",
  reason="Ensure creative direction reflects current platform dynamics, audience behaviour shifts, and competitive creative landscape rather than outdated best practices"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="ad-creative-brief-generator", session={
  summary: "Generated ad creative brief for [campaign name] targeting [ICA segment] on [platform(s)] with [number] format executions and [number] test variants",
  key_findings: ["ICA creative profile insight — e.g., primary pain catalyst identified as [X]", "Message strategy anchored on [claim/conflict]", "Variant test matrix isolating [variable] for performance validation"],
  user_feedback: null
})
```