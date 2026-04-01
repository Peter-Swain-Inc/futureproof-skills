---
name: facebook-post-writer
description: |
  Crafts high-performing Facebook posts using FutureProof context, audience intelligence, and platform-specific best practices.
  Trigger: when a user asks to write, draft, or improve a Facebook post, or when they need content for their Facebook page, group, or profile to drive engagement, leads, or brand awareness.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="facebook-post-writer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including ICA definitions, brand voice guidelines, prior post performance data, and any winning formats identified in previous experiments.

## Step 2: Get Input

Ask the user:
- **Objective**: What is the primary goal of this post? (engagement/comments, lead generation, traffic to URL, community building, social proof, launch announcement)
- **ICA context**: Who is this post speaking to? (If not already defined in FutureProof context, ask for ICA demographics, psychographics, and current awareness stage)
- **Placement**: Where will this post appear? (personal profile, business page, Facebook group, paid ad creative)
- **Topic or hook**: What is the core message, offer, story, or insight to communicate?
- **Assets available**: Are there images, videos, carousels, or links to incorporate?
- **Constraints**: Character limits for ad copy, compliance requirements, prohibited claims, or brand-specific language rules?

If FutureProof context already contains ICA profiles, brand voice, or prior high-performing post structures, confirm these with the user rather than re-asking.

## Step 3: Do the Work

### 3A: Audience–Platform Alignment Analysis

Map the ICA's Facebook behaviour profile:
1. **Scroll context** — when and why does this ICA encounter Facebook? (morning commute, work procrastination, evening wind-down) This determines emotional register and cognitive load tolerance
2. **Feed competition** — what other content types dominate their feed? (peer updates, news, memes, group discussions) This defines the pattern-interrupt threshold
3. **Engagement disposition** — what motivates this ICA to stop, read, react, comment, or share on Facebook specifically vs. other platforms?

### 3B: Post Architecture Design

Construct the post using the **HSCA Framework** (Hook → Story → CTA → Amplifier):

1. **Hook (Lines 1–2)** — The first 125 characters before the "See more" truncation are the highest-leverage real estate. Apply one of six proven hook architectures:
   - **Pattern interrupt**: Contradicts a belief the ICA holds ("Stop posting motivational quotes. Your audience hates them.")
   - **Specificity magnet**: Uses an unusually precise data point or outcome ("This 11-word subject line generated $42,300 in 6 hours")
   - **Identity callout**: Names the ICA directly ("If you're a service-based business owner doing $10K–$30K/mo, read this")
   - **Open loop**: Creates an information gap that demands resolution ("I almost deleted this post. Then I checked the results.")
   - **Vulnerability lead**: Opens with admission of failure or struggle to disarm the ICA's ad filter
   - **Polarising stance**: Takes a clear position on an industry debate to force a reaction

2. **Story / Body** — Expand using the structure that matches the objective:
   - **Engagement posts**: Use the PSR model (Problem → Struggle → Resolution) with an open-ended question at the end that invites the ICA to share their own experience
   - **Lead generation posts**: Use the VGO model (Value demonstration → Gap identification → Offer bridge) ending with a clear mechanism to capture the lead (comment keyword, DM prompt, link)
   - **Authority posts**: Use the FCL model (Framework → Case study → Lesson) to establish thought leadership while delivering genuine utility
   - **Community posts**: Use the SPI model (Shared experience → Poll/Question → Invitation to contribute) to maximise comment velocity

3. **Call to Action** — Design a single, frictionless CTA calibrated to platform norms:
   - Favour comment-based CTAs over link clicks (Facebook's algorithm deprioritises link posts by 30–50% in organic reach)
   - Use the "micro-commitment ladder": easiest action first ("Drop a 🔥 if you agree"), then escalate in replies
   - For lead generation, use comment-trigger automations ("Comment READY and I'll send you the guide") rather than raw URLs where possible

4. **Amplifier** — Add a structural element that boosts algorithmic distribution:
   - **Formatting**: Strategic line breaks every 1–2 sentences, white space to increase dwell time, emoji as bullet markers (not decoration)
   - **Engagement bait removal**: Ensure the post does not trigger Facebook's engagement bait classifier (avoid explicit "tag a friend", "share this post", or reaction-gating)
   - **Comment seeding**: Draft 2–3 first-comment options the user can post immediately to prime the engagement loop
   - **Hashtag strategy**: 3–5 targeted hashtags for group/discovery contexts; zero hashtags for personal profile organic reach

### 3C: Voice and Compliance Check

- Align every sentence to the brand voice profile stored in FutureProof context (or established in Step 2)
- Flag any claims requiring substantiation (income claims, health outcomes, client results) and suggest compliant phrasing alternatives
- Verify the post reads as native to Facebook's conversational, personal tone — not as repurposed LinkedIn or Twitter content

### 3D: Variant Development

Produce **two distinct variants** of the post:
- **Variant A**: Optimised for maximum comment engagement (prioritises open loops, questions, and polarisation)
- **Variant B**: Optimised for primary objective stated by user (lead gen, traffic, awareness — with architecture adjusted accordingly)

This enables the user to A/B test or select based on current priorities.

## Step 4: Deliver Output

Produce a structured **Facebook Post Brief** containing:

### Post Variant A — Engagement Optimised
- **Hook type used**: [named architecture from 3B.1]
- **Full post copy**: complete, formatted, ready to paste into Facebook
- **First comment**: pre-written comment for the author to post immediately
- **Predicted engagement lever**: the specific psychological trigger driving interaction
- **Recommended posting time**: based on ICA scroll-context analysis from 3A

### Post Variant B — Objective Optimised
- **Hook type used**: [named architecture from 3B.1]
- **Full post copy**: complete, formatted, ready to paste into Facebook
- **CTA mechanism**: exact instructions for the comment-trigger, link, or DM flow
- **First comment**: pre-written comment for the author to post immediately
- **Recommended posting time**: based on ICA scroll-context analysis from 3A

### Supporting Elements
- **Image/visual direction**: specific guidance on what visual to pair (subject, text overlay copy if applicable, dimensions for placement type)
- **Comment response templates**: 3 pre-written replies to likely first comments to maintain engagement velocity in the critical first 60 minutes
- **Compliance notes**: any flagged claims with suggested compliant alternatives

### Performance Tracking Checklist
- Metric to track per variant (reach, comments, link clicks, DM/keyword triggers)
- When to evaluate (24h for engagement, 72h for lead generation)
- Decision rule: which metric delta justifies adopting Variant A vs. B going forward

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="facebook-post-writer", experiment={
  hypothesis: "Using a pattern-interrupt hook with a specific number in the first line increases 'See more' click-through rate compared to a vulnerability lead hook",
  variants: ["Variant A: vulnerability lead hook", "Variant B: pattern-interrupt hook with specific metric"],
  measurement: "Compare reach, comment count, and CTA conversion rate across both variants over next 5 posts",
  expected_impact: "20–35% increase in engagement rate and 15% improvement in CTA action rate for the winning hook type"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="facebook-post-writer",
  query="Facebook algorithm ranking signals Q3-Q4 2024, organic reach benchmarks by post type, and high-performing post formats for service-based businesses on Facebook pages and groups",
  reason="Ensure post architecture and CTA strategies align with the latest algorithm weighting, particularly any shifts in link-post suppression, comment velocity thresholds, and reels/text-post prioritisation changes"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="facebook-post-writer", session={
  summary: "Wrote Facebook post variants for [ICA segment] with objective [primary goal] — placement: [page/profile/group]",
  key_findings: ["Hook architecture selected and rationale", "CTA mechanism chosen based on placement and objective", "Compliance flags if any"],
  deliverables: ["Post Variant A (engagement-optimised)", "Post Variant B (objective-optimised)", "Comment response templates", "Visual direction brief"],
  user_feedback: null
})
```