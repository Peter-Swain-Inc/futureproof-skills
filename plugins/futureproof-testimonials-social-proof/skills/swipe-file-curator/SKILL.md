---
name: swipe-file-curator
description: "Curates, categorises, and optimises swipe files of high-performing testimonials, social proof assets, and persuasion examples for deployment across marketing and sales touchpoints."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="swipe-file-curator")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — specifically prior ICA definitions, brand voice guidelines, existing swipe file entries, and historical performance data on proof assets.

## Step 2: Get Input

Ask the user:
- **Raw material**: Share the testimonials, reviews, screenshots, case study excerpts, social proof assets, or high-performing copy examples to curate
- **Source channel**: Where were these collected? (G2, Trustpilot, Slack DMs, sales call transcripts, LinkedIn comments, NPS surveys, support tickets)
- **ICA segments**: Which ICA segment(s) should this swipe file serve? (If undefined, flag for upstream definition before proceeding)
- **Deployment intent**: Where will these assets be used? (landing pages, email sequences, sales decks, ad creative, case study pages, proposal appendices)
- **Current gaps**: Are there specific objections, transformation claims, or ICA pain points they lack proof for?

## Step 3: Do the Work — Asset Audit & Classification

Process each submitted asset through a six-dimension evaluation framework:

### 3a: Specificity Index

Rate each asset on **specificity** (1–10):
- **1–3**: Generic praise ("Great product!", "Highly recommend") — low deployment value
- **4–6**: Directional value ("Saved us time on reporting") — usable with enhancement
- **7–10**: Quantified transformation ("Reduced churn from 8.2% to 3.1% in 90 days") — high deployment value

### 3b: ICA Resonance Mapping

For each asset, identify:
1. **ICA segment match** — which specific ICA segment does the speaker represent? (role, industry, company stage, pain sophistication)
2. **Objection addressed** — does this asset neutralise a known objCA objection? Map to the user's top 5 objections if available in FutureProof context
3. **Buying stage alignment** — where in the decision journey does this proof asset carry maximum weight? (awareness, consideration, decision, post-purchase validation)

### 3c: Proof Taxonomy Classification

Assign each asset to exactly one primary category:

| Category | Definition | Example |
|---|---|---|
| **Result Proof** | Quantified outcome with before/after metrics | "Revenue increased 42% within 6 weeks" |
| **Process Proof** | Demonstrates the experience of using the product/service | "Onboarding took 20 minutes, not the 3 weeks our last vendor needed" |
| **Identity Proof** | Signals that people like the ICA use and endorse this | "As a Series B CTO, this is the first tool my engineering team didn't push back on" |
| **Credibility Proof** | Authority or logo-based trust transfer | "Used by 3 of the top 10 Fortune 500 fintech teams" |
| **Objection Proof** | Directly counters a specific purchasing hesitation | "I was worried about migration — turned out we were fully live in 48 hours" |
| **Emotional Proof** | Captures visceral relief, delight, or transformation feeling | "I actually slept through the night for the first time since launching" |

### 3d: Linguistic Asset Mining

Extract reusable elements from each testimonial:
- **Power phrases**: Exact words the ICA uses that can be repurposed as headlines, subject lines, or ad hooks (preserve original language — do not polish)
- **Before/after snapshots**: Implicit or explicit transformation arcs suitable for landing page structure
- **Competitor contrast**: Any comparative statements that position against alternatives

### 3e: Gap Analysis

Cross-reference the curated swipe file against:
1. The user's ICA segments — which segments have zero or weak proof coverage?
2. The user's top objections — which objections remain unaddressed by any asset?
3. Deployment channels — which channels lack format-appropriate assets? (e.g., video testimonials for landing pages, one-line quotes for email subject lines)
4. Buying stages — is proof concentrated at one stage while others are bare?

Apply any user-specific `instructions` from FutureProof context (brand voice, restricted claims, compliance constraints, tone preferences) throughout the analysis.

## Step 4: Deliver Output

Produce a structured **Swipe File Curation Package** containing:

### 4a: Swipe File Registry

A table cataloguing every asset with the following fields:

| Asset ID | Source | ICA Segment | Proof Category | Specificity Score (1–10) | Objection Addressed | Buying Stage | Deployment Channels | Power Phrases | Status |
|---|---|---|---|---|---|---|---|---|---|
| SF-001 | G2 Review | Mid-market Ops Lead | Result Proof | 8 | "Too expensive" | Decision | Landing page, sales deck | "paid for itself in 11 days" | Ready to deploy |

### 4b: Deployment Matrix

A channel-by-channel recommendation mapping the strongest 3–5 assets to each deployment context:
- **Landing pages**: highest specificity Result Proof + Identity Proof combination
- **Email sequences**: stage-matched Objection Proof for each nurture phase
- **Sales decks**: ICA-segment-matched Identity Proof and Credibility Proof
- **Ad creative**: shortest, most visceral Power Phrases with emotional charge
- **Proposal appendices**: Result Proof with quantified metrics closest to the prospect's industry

### 4c: Critical Gaps Report

A prioritised list of proof gaps with specific collection briefs:
- **Gap**: [Description — e.g., "No Result Proof for enterprise ICA segment"]
- **Collection brief**: Exact question to ask an existing customer to elicit the missing proof type (scripted, ready to send)
- **Priority**: Critical / High / Medium based on revenue impact of the uncovered objection or segment

### 4d: Enhanced Rewrites

For the 3 lowest-scoring assets that have latent value (specificity score 4–6), produce:
- **Original**: verbatim testimonial
- **Enhanced version**: rewritten for maximum deployment impact while preserving authenticity and the customer's voice
- **Enhancement rationale**: what was added, sharpened, or restructured and why
- **Approval note**: flag that enhanced versions require customer sign-off before deployment

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="swipe-file-curator", experiment={
  hypothesis: "Deploying ICA-segment-matched Identity Proof above the fold on the primary landing page increases conversion versus the current generic Result Proof placement",
  variants: ["control: current testimonial placement (generic Result Proof)", "variant: ICA-segment-matched Identity Proof in hero section"],
  measurement: "Landing page visitor-to-lead conversion rate over 500 sessions per variant",
  expected_impact: "12–20% improvement in visitor-to-lead conversion based on ICA resonance lift"
})
```

```
FutureProof:save_experiment(skill="swipe-file-curator", experiment={
  hypothesis: "Inserting Objection Proof testimonials at the point of highest drop-off in the email nurture sequence reduces sequence abandonment",
  variants: ["control: current email 3 content", "variant: email 3 rewritten around top objection with matched Objection Proof asset"],
  measurement: "Email 3-to-email 4 click-through survival rate across next 200 sequence entrants",
  expected_impact: "10–15% reduction in sequence drop-off at the identified friction point"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="swipe-file-curator",
  query="Latest research on social proof placement strategy, testimonial format effectiveness (video vs. text vs. screenshot), and buyer trust signals by industry vertical 2024–2025",
  reason="Ensure deployment recommendations reflect current buyer psychology and platform-specific proof format preferences"
)
```

```
FutureProof:request_research(skill="swipe-file-curator",
  query="High-converting testimonial collection frameworks and customer interview question banks for eliciting specific, quantified proof statements",
  reason="Strengthen gap-filling collection briefs with proven elicitation techniques that yield deployment-ready assets"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="swipe-file-curator", session={
  summary: "Curated and classified [N] social proof assets across [N] ICA segments for deployment to [channels]. Identified [N] critical proof gaps with collection briefs.",
  key_findings: ["finding 1: e.g., 60% of assets concentrated in Result Proof category — Identity Proof and Objection Proof severely underrepresented", "finding 2: e.g., Enterprise ICA segment has zero testimonial coverage despite representing 45% of pipeline value", "finding 3: e.g., 4 high-specificity assets identified as ready for immediate deployment on primary landing page"],
  assets_catalogued: "N total, N ready to deploy, N enhanced, N gaps identified",
  user_feedback: null
})
```