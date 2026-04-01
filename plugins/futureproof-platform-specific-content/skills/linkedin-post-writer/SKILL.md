---
name: linkedin-post-writer
description: "Crafts high-performing LinkedIn posts using FutureProof context, audience intelligence, and platform-native best practices."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="linkedin-post-writer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly the user's ICA definition, brand voice, past post performance data, and any winning formats identified through prior experiments.

## Step 2: Get Input

Ask the user:
- **Core topic or raw material** — What is the post about? (an idea, a personal story, a hot take, a lesson learned, an article to riff on, a promotion, etc.)
- **Strategic objective** — What should this post accomplish? (authority building, lead generation, community engagement, newsletter/funnel sign-ups, hiring visibility, event promotion)
- **ICA targeting** — Who specifically must this post resonate with? (If not stated, pull from FutureProof context; confirm with the user)
- **Format preference** — Do they have a preferred format? (story-driven, contrarian take, listicle, carousel concept, poll, before/after transformation, "I was wrong about X")
- **Constraints** — Any mandatory inclusions (links, tags, hashtags, CTAs) or exclusions (no emojis, no hashtags, avoid certain language)?

If FutureProof context contains established brand voice guidelines or prior top-performing post patterns, surface these and confirm they still apply.

## Step 3: Do the Work

### 3A: Strategic Framing

Before writing a single word, define the post's architecture:

1. **ICA Pain/Desire Mapping** — Identify the specific tension this post addresses in the ICA's professional life. Map the topic to one of: an unspoken frustration, an aspiration they publicly signal, or a knowledge gap they'd be embarrassed to admit.
2. **Scroll-Stop Thesis** — Distil the post into a single provocative, specific, or counterintuitive claim that earns the first 3 seconds of attention.
3. **Platform-Native Format Selection** — Choose the optimal LinkedIn post structure based on objective and topic:
   - **Narrative Arc** — personal story with professional takeaway (highest engagement ceiling)
   - **Contrarian Reframe** — challenge conventional wisdom with evidence (authority positioning)
   - **Tactical Breakdown** — step-by-step framework or process (save-worthy, high share)
   - **Observation + Insight** — pattern recognition from the user's domain (thought leadership)
   - **Before/After Transformation** — concrete results with context (proof-driven lead generation)
   - **Curated List** — "X things I learned about Y" (accessible, high completion rate)

### 3B: Drafting — The LinkedIn Engagement Architecture

Write the post applying all six layers of the engagement architecture:

1. **Hook (Lines 1–2)** — Must pass the "thumb-stop test." Use one of the following proven hook patterns:
   - Bold declaration: "Most [ICA role] get [topic] completely wrong."
   - Specific result: "This one change added [specific metric] in [timeframe]."
   - Pattern interrupt: "I got fired. It was the best thing that happened to my career."
   - Curiosity gap: "The highest-performing [ICA role] I know all do this. Almost nobody talks about it."
   - Direct address: "If you're a [ICA role] struggling with [pain point], read this."

2. **Tension/Context (Lines 3–6)** — Establish stakes. Why should the reader care *now*? Ground the post in a recognisable situation, a surprising data point, or an emotional moment. Write at a 7th-grade reading level. One idea per sentence.

3. **Substance/Body (Lines 7–18)** — Deliver on the hook's promise with specificity. No filler. Every line must either teach, prove, or reframe. Use:
   - White space aggressively (one sentence per line for key points)
   - Concrete numbers over vague claims
   - "You" language to maintain direct address
   - Parallel structure for lists and frameworks
   - Strategic line breaks before the "See more" fold (lines 3–4) to maximise expand rate

4. **Proof Layer** — Embed at least one credibility signal: a personal result, a client outcome (anonymised if needed), a cited statistic, or a named authority reference.

5. **Memorable Close (Lines 19–21)** — End with one of:
   - A single-sentence reframe that recontextualises the entire post
   - A vulnerable admission that humanises the advice
   - A punchy, quotable one-liner

6. **Call to Action (Final lines)** — Engineer the CTA to match the strategic objective:
   - **Engagement**: Ask a specific, low-friction question ("What's one thing you'd add to this list?")
   - **Lead generation**: Offer a resource with a clear access mechanism ("I wrote a deeper breakdown of this framework — comment 'FRAMEWORK' and I'll send it over")
   - **Authority**: Invite disagreement ("Tell me where I'm wrong — I'll engage with every comment")
   - **Funnel**: Soft link to newsletter/profile with value framing, never naked URLs in body text

### 3C: Technical Optimisation

Apply LinkedIn algorithm and readability best practices:
- **Character count**: Target 1,200–1,800 characters (the engagement sweet spot for text-only posts; adjust for carousel or image posts)
- **"See more" optimisation**: Ensure the first 210 characters (approximately 3 lines on mobile) create an irresistible reason to expand
- **Hashtag strategy**: 3–5 hashtags maximum, placed at the end, mixing 1 broad (500K+ followers), 2 mid-tier (10K–100K), and 1–2 niche tags relevant to the ICA's world
- **Formatting**: Use line breaks, not dense paragraphs. Employ → bullets, numbered lists, or em-dashes for scannability. Avoid walls of text.
- **Tagging**: Only tag individuals or companies if genuinely relevant and likely to engage (tag sparingly — over-tagging suppresses reach)
- **Link placement**: If a link is required, place in comments (not body text) to avoid algorithmic suppression, unless the user explicitly overrides

### 3D: Voice Calibration

Cross-reference the draft against:
- FutureProof `instructions` for brand voice (tone, vocabulary, phrases to use/avoid)
- The user's prior top-performing posts (if available in `recent_sessions`) — mirror the cadence and structural patterns that drove results
- ICA vocabulary — ensure the post speaks *their* language, not industry jargon they wouldn't naturally use

## Step 4: Deliver Output

Produce a structured deliverable with three components:

### **LinkedIn Post — Final Draft**
The complete, copy-paste-ready post with all formatting, line breaks, hashtags, and CTA in place.

### **Post Strategy Brief**
| Element | Detail |
|---|---|
| **Hook Type** | [Pattern used and why] |
| **Format** | [Structure selected and rationale] |
| **ICA Resonance Point** | [Specific pain/desire this post targets] |
| **Scroll-Stop Score** | 1–10 rating of the hook's interrupt strength |
| **Substance Density** | 1–10 rating of value-per-line in the body |
| **Proof Layer** | 1–10 rating of credibility signals embedded |
| **CTA Friction Score** | 1–10 (10 = zero friction, effortless to act on) |
| **Algorithm Alignment** | 1–10 (formatting, length, link handling, hashtag strategy) |
| **Voice Consistency** | 1–10 match to user's established brand voice |

### **Posting Guidance**
- **Recommended posting window**: Based on ICA's likely active hours (default: Tuesday–Thursday, 7:30–9:00 AM in the ICA's primary timezone)
- **First 60 minutes plan**: Suggest 2–3 engagement actions to boost initial distribution (e.g., reply to every comment within the first hour, share to relevant LinkedIn groups, notify tagged individuals)
- **Comment-section prompt**: A pre-written first comment the user can post (to seed conversation or place a link)

If the user requested multiple post variants, deliver each as a separate numbered draft with a brief rationale for when to use each.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="linkedin-post-writer", experiment={
  hypothesis: "Story-driven hooks with a specific emotional moment outperform declarative/statistic hooks for this user's ICA segment",
  variants: ["control: declarative hook ('Most founders get pricing wrong')", "variant: narrative hook ('I lost my biggest client over a $50/month price increase')"],
  measurement: "Impressions, engagement rate (reactions + comments / impressions), and profile visits within 48 hours of posting",
  expected_impact: "25% increase in engagement rate and 15% increase in profile visits"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="linkedin-post-writer",
  query="LinkedIn algorithm ranking factors and high-engagement post patterns Q3-Q4 2024, including impact of dwell time, comment velocity, and format-specific reach benchmarks",
  reason="Platform algorithm and user behaviour evolve rapidly; maintain evidence-based formatting and structural recommendations"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="linkedin-post-writer", session={
  summary: "Drafted LinkedIn post on [topic] targeting [ICA segment] with [format type] structure, optimised for [strategic objective]",
  key_findings: ["[Hook pattern selected and rationale]", "[ICA resonance point identified]", "[Brand voice calibration notes]"],
  artifacts: ["linkedin-post-final-draft", "post-strategy-brief", "posting-guidance"],
  user_feedback: null
})
```