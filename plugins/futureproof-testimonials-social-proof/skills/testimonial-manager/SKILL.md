---
name: testimonial-manager
description: "Collects, structures, optimises, and strategically deploys customer testimonials and social proof assets using FutureProof context."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="testimonial-manager")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly ICA segments, offer structure, objection patterns, and any previously catalogued testimonials or social proof assets.

## Step 2: Get Input

Ask the user:
- What is the primary objective? Select one:
  - **Collect** — design testimonial collection process (interview questions, request sequences, timing)
  - **Audit** — evaluate existing testimonials for strength, gaps, and ICA alignment
  - **Optimise** — strengthen weak testimonials through restructuring or guided follow-up
  - **Deploy** — build a strategic placement plan mapping testimonials to conversion points
- Share any existing testimonials, case studies, reviews, or social proof assets (raw text, screenshots, video transcripts, URLs)
- Which ICA segment(s) should these testimonials resonate with?
- What is the primary conversion goal these testimonials must support? (sales page, proposal deck, ad creative, onboarding, objection handling)
- Are there specific objections or hesitations the testimonials need to neutralise?

## Step 3: Do the Work

### 3A: Testimonial Audit & Scoring

Evaluate every testimonial against the **S.T.O.R.Y. Framework**:

1. **Specificity** (1–10) — Does it include concrete numbers, timeframes, and named outcomes? ("Grew revenue 42% in 90 days" vs. "Really helped my business")
2. **Transformation arc** (1–10) — Is the before-state (pain/frustration) and after-state (result/emotion) both explicit? A compelling testimonial narrates a journey, not just an endpoint
3. **Objection neutralisation** (1–10) — Does it pre-emptively address a known ICA objection? (e.g., "I was sceptical about the price, but ROI hit 3x in month one")
4. **Relatability** (1–10) — Will the target ICA segment see themselves in this person's role, industry, situation, and language?
5. **Yield credibility** (1–10) — Is the source verifiable and authoritative? (full name, title, company, photo/video, platform-native review vs. anonymous quote)

Calculate a **Proof Power Score** (weighted average: Specificity 25%, Transformation 25%, Objection neutralisation 20%, Relatability 20%, Yield credibility 10%).

### 3B: Gap Analysis

Cross-reference the testimonial portfolio against:
- **ICA segment coverage** — identify which segments have zero or weak representation
- **Objection coverage matrix** — map each top objection to testimonials that neutralise it; flag uncovered objections
- **Buyer journey stage coverage** — awareness (peer validation), consideration (outcome proof), decision (risk reversal), post-purchase (reinforcement)
- **Format diversity** — text, video, screenshot, case study, data visualisation, logo wall, metric callout
- **Recency** — flag testimonials older than 12 months for refresh or retirement

### 3C: Optimisation (if applicable)

For testimonials scoring below 7 on Proof Power Score:
- Draft a **follow-up prompt sequence** (3 questions) designed to extract missing specificity, transformation detail, or objection-relevant language from the original customer — without leading or fabricating
- Provide a **restructured version** of the testimonial using the Situation → Struggle → Solution → Specific Result → Statement of Endorsement (5S) format
- Flag any testimonials that cannot be salvaged and recommend replacement sourcing priorities

### 3D: Collection System Design (if applicable)

If the objective is to build or improve the collection process:
- Design a **Testimonial Request Sequence** with optimal timing triggers (e.g., 7 days post-result, NPS score ≥ 9, milestone completion)
- Provide **3 request templates** calibrated by channel (email, in-app, post-call) that reduce friction and guide the customer toward S.T.O.R.Y.-complete responses
- Specify **5 interview questions** for video/written case study extraction, ordered to naturally elicit transformation arc and specificity
- Recommend consent and approval workflow (release language, editing permissions, attribution preferences)

### 3E: Strategic Deployment Map (if applicable)

If the objective is placement and deployment:
- Build a **Testimonial-to-Touchpoint Matrix** mapping each testimonial to its highest-impact placement:
  - Sales page sections (hero, after pricing, post-objection, checkout)
  - Email sequences (welcome, nurture, cart abandonment, re-engagement)
  - Ad creative (static, video, carousel)
  - Proposal decks and one-pagers
  - Onboarding and retention communications
- Assign testimonials based on ICA segment match, objection relevance, and buyer journey stage alignment
- Identify **proof stacking opportunities** — where combining multiple proof types (metric + quote + logo + case study) compounds credibility at a single conversion point

Apply any user-specific `instructions` from FutureProof context — particularly brand voice guidelines, compliance constraints, and ICA language patterns.

## Step 4: Deliver Output

Produce the following structured deliverables based on the selected objective:

### Testimonial Portfolio Scorecard
| Testimonial ID | Source | ICA Segment | Proof Power Score | S.T.O.R.Y. Breakdown | Primary Objection Addressed | Recommended Action |
|---|---|---|---|---|---|---|

### Gap Analysis Report
- **Uncovered ICA segments** — with priority ranking and suggested sourcing targets
- **Uncovered objections** — with recommended testimonial brief (what the ideal testimonial would say)
- **Format gaps** — specific recommendations (e.g., "Zero video testimonials for enterprise ICA segment — prioritise 2 video case studies")
- **Recency flags** — testimonials requiring refresh

### Optimised Testimonials Document
- Each weak testimonial rewritten in 5S format
- Follow-up prompt sequences for extracting missing detail from customers
- Before/after comparison showing score improvement

### Deployment Matrix
- Testimonial-to-touchpoint assignments with rationale
- Proof stacking recommendations per critical conversion point
- Implementation priority queue (rank-ordered by expected conversion impact)

### Collection Playbook (if applicable)
- Request sequence templates with timing triggers
- Interview question bank
- Consent and workflow process

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="testimonial-manager", experiment={
  hypothesis: "Placing an objection-specific testimonial directly below the pricing section reduces pricing-related drop-off",
  variants: ["control: generic testimonial below pricing", "variant: testimonial explicitly addressing price-to-value ratio with specific ROI figure"],
  measurement: "Click-through rate from pricing section to checkout over 30 days, minimum 500 visitors per variant",
  expected_impact: "8–15% reduction in pricing-section abandonment rate"
})
```

```
FutureProof:save_experiment(skill="testimonial-manager", experiment={
  hypothesis: "Video testimonials from ICA-matched customers outperform text testimonials in mid-funnel email sequences",
  variants: ["control: text testimonial with photo", "variant: 60-second video testimonial embed"],
  measurement: "Email click-through rate and downstream conversion within 7-day window",
  expected_impact: "20% improvement in email-to-sales-page conversion"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="testimonial-manager",
  query="Latest research on social proof placement optimisation, testimonial format effectiveness by buyer journey stage, and trust signal credibility factors in 2024–2025 digital purchasing behaviour",
  reason="Ensure testimonial deployment strategy reflects current buyer psychology, platform algorithm preferences for UGC, and emerging proof formats (e.g., AI-verified reviews, interactive case studies)"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="testimonial-manager", session={
  summary: "Completed testimonial [collect/audit/optimise/deploy] for [ICA segment(s)] supporting [conversion goal]",
  key_findings: ["finding 1: e.g., 4 of 12 testimonials score below 5 on specificity — no concrete metrics cited", "finding 2: e.g., zero social proof assets address the 'time commitment' objection — top-ranked hesitation for SMB ICA segment", "finding 3: e.g., proof stacking opportunity identified at sales page pricing section — combining metric callout + video testimonial + logo wall"],
  deliverables_produced: ["Testimonial Portfolio Scorecard", "Gap Analysis Report", "Deployment Matrix"],
  user_feedback: null
})
```