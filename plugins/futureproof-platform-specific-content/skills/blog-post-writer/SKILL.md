---
name: blog-post-writer
description: |
  Crafts high-performing blog posts using FutureProof context, ICA research, and proven content frameworks.
  Trigger: when a user asks to write, draft, or outline a blog post, article, or long-form content piece for their website or content marketing strategy.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="blog-post-writer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including brand voice, ICA profiles, past content performance data, editorial guidelines, and any standing instructions on tone, structure, or SEO approach.

## Step 2: Get Input

Ask the user:
- **Topic or brief**: What is the blog post about? Share any working title, keyword targets, or content brief.
- **ICA segment**: Who is the intended reader? (If FutureProof context already contains ICA profiles, confirm which segment this post targets.)
- **Strategic intent**: What should this post accomplish? (organic traffic acquisition, thought leadership positioning, lead nurture, product education, link-building asset)
- **Funnel stage**: Is this top-of-funnel (awareness), mid-funnel (consideration), or bottom-of-funnel (decision) content?
- **Format preference**: Standard editorial, listicle, how-to guide, data-driven analysis, opinion/POV piece, comparison post, or pillar page?
- **Target word count**: Any length requirements or constraints?
- **Internal assets**: Are there case studies, proprietary data, product features, or existing content to reference or link to?

## Step 3: Conduct Pre-Write Analysis

Before drafting, perform a structured content strategy audit:

### 3a. ICA-Intent Mapping
- Define the **specific question or problem** the ICA is searching for that this post answers
- Identify the ICA's **awareness level** (unaware, problem-aware, solution-aware, product-aware) and calibrate sophistication of language accordingly
- Map the ICA's **emotional state** at the point of search — frustration, curiosity, urgency, comparison fatigue — and plan the opening hook to meet that state

### 3b. Keyword & Search Intent Architecture
- Confirm the **primary keyword** and 3–5 **semantic supporting keywords**
- Classify search intent: informational, navigational, commercial investigation, or transactional
- Define the **content angle** that differentiates this post from the current top 5 ranking results (proprietary data, contrarian POV, deeper specificity, fresher recency, superior structure)

### 3c. Competitive Content Gap Assessment
- Based on available context and user input, identify what existing top-ranking content **fails to cover** or covers poorly
- Define 2–3 **content gap opportunities** this post will exploit (missing subtopics, outdated statistics, lack of actionable frameworks, no real-world examples)

### 3d. Structural Framework Selection
Choose and declare the structural framework best suited to the intent and format:
- **PAS (Problem–Agitation–Solution)** — for pain-driven informational content
- **AIDA (Attention–Interest–Desire–Action)** — for commercial/conversion content
- **Inverted Pyramid** — for news-style or data-driven pieces
- **Hub & Spoke** — for pillar pages covering broad topics
- **StoryBridge (Situation–Complication–Resolution)** — for thought leadership and narrative-driven posts

Apply any user-specific `instructions` from FutureProof context (brand voice guidelines, editorial standards, compliance requirements, preferred frameworks) to override or refine selections.

## Step 4: Produce the Blog Post

Deliver the complete blog post as a **publish-ready document** with the following components:

### 4a. Metadata Block
| Field | Value |
|---|---|
| **Working Title** | Primary title (60 characters max, front-loaded keyword) |
| **SEO Title Tag** | Optimised for CTR and keyword placement |
| **Meta Description** | 150–155 characters, includes primary keyword and clear value proposition |
| **URL Slug** | Lowercase, hyphenated, keyword-focused |
| **Primary Keyword** | As confirmed in Step 3 |
| **Secondary Keywords** | 3–5 supporting terms |
| **Target Word Count** | Actual word count of draft |
| **Funnel Stage** | As confirmed in Step 2 |
| **ICA Segment** | As confirmed in Step 2 |

### 4b. Full Draft
Write the complete blog post adhering to these standards:

1. **Opening hook (first 100 words)** — Must accomplish three things: (a) validate the ICA's current emotional state or situation, (b) establish a credibility marker or pattern interrupt, (c) create a clear forward-reading contract (the reader knows what they will gain by continuing)
2. **Subheaded sections** — Every 200–350 words, a new H2 or H3. Each subheading must be specific and benefit-oriented, not generic labels
3. **ICA language mirroring** — Use the vocabulary, idioms, and framing the ICA uses to describe their own problems (drawn from FutureProof ICA context where available)
4. **Proof density standard** — Every major claim must be supported by at least one of: specific data point, named case study, direct quote, logical first-principles argument, or cited source. No unsupported assertions
5. **Actionable specificity** — Any advice or recommendation must pass the "Monday morning test" — could the reader act on it immediately without further research?
6. **Transition engineering** — Each section's final sentence must create a logical bridge to the next section, maintaining reading momentum
7. **Strategic internal links** — Suggest 2–4 placement points for internal links to the user's existing content or product pages (marked as `[INTERNAL LINK: suggested anchor text → target page]`)
8. **Call to action** — Conclude with a CTA aligned to the declared strategic intent. The CTA must be specific, low-friction, and logically connected to the content (not bolted on)

### 4c. Enhancement Recommendations
Provide a brief addendum:
- **Visual content suggestions**: 2–3 specific images, diagrams, charts, or embedded media that would increase engagement and dwell time (describe what each should depict)
- **Pull quotes**: 2 high-impact sentences from the draft suitable for social sharing or visual callout formatting
- **Content upgrade opportunity**: One lead magnet concept that naturally extends the post's value (e.g., checklist, template, calculator, swipe file) for email capture

## Step 5: Quality Scorecard

Rate the completed draft against these dimensions (1–10 scale):

| Dimension | Score | Rationale |
|---|---|---|
| **ICA resonance** | — | Does the language, depth, and framing match the target reader? |
| **Search intent fulfilment** | — | Does the post fully satisfy what the searcher wanted? |
| **Proof density** | — | Are claims substantiated with data, examples, or logic? |
| **Structural clarity** | — | Is the post scannable, logically sequenced, and well-paced? |
| **Differentiation** | — | Does this offer a meaningfully different angle from competing content? |
| **Actionability** | — | Can the reader implement advice without further research? |
| **CTA alignment** | — | Does the closing action logically follow from the content? |

Flag any dimension scoring below 7 with a **specific remediation note**.

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="blog-post-writer", experiment={
  hypothesis: "Leading with a contrarian statistic in the opening line increases average time-on-page compared to empathy-first openings",
  variants: ["control: empathy-led opening validating ICA pain point", "variant: data-led opening with surprising statistic that challenges assumptions"],
  measurement: "average time-on-page and scroll depth for next 5 blog posts using each approach",
  expected_impact: "20% increase in average time-on-page for data-led variant"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="blog-post-writer",
  query="High-performing blog post structures and engagement patterns by industry vertical 2024–2025, including optimal word count, heading density, and CTA placement benchmarks",
  reason="Continuously refine structural frameworks and scoring benchmarks against current content performance data across ICA segments"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="blog-post-writer", session={
  summary: "Drafted [format type] blog post on [topic] targeting [ICA segment] at [funnel stage] stage, optimised for [primary keyword]",
  key_findings: ["finding 1: e.g., ICA segment responds to X framing based on context data", "finding 2: e.g., competitive gap identified in Y subtopic", "finding 3: e.g., content upgrade opportunity for Z lead magnet"],
  deliverables: ["publish-ready blog post draft", "metadata block", "quality scorecard", "enhancement recommendations"],
  user_feedback: null
})
```