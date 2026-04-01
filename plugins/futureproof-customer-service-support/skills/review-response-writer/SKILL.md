---
name: review-response-writer
description: "Crafts professional, brand-aligned responses to customer reviews across platforms (Google, Yelp, Trustpilot, G2, App Store, Amazon, etc.) using FutureProof context to maintain voice consistency, addre"
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="review-response-writer")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — specifically brand voice guidelines, previously approved response templates, ICA segments, known product/service issues, and escalation protocols.

## Step 2: Get Input

Ask the user:
- Share the review(s) to respond to (text, star rating, platform, and reviewer name if visible)
- What is the product, service, or location being reviewed?
- What is the desired outcome? (retention/win-back, reputation management, conversion of review readers, escalation to support)
- Are there any known facts about this customer's situation (order history, prior interactions, resolution status)?
- Any response constraints? (character limits, platform guidelines, legal/compliance boundaries, topics to avoid)

If the user has no prior FutureProof context for brand voice, ask:
- Describe your brand tone (e.g., warm and empathetic, professional and concise, playful and human)
- Are there specific phrases, values, or differentiators that should appear consistently?

## Step 3: Classify the Review

Before drafting, perform a structured review classification:

1. **Sentiment tier**: Positive (4–5 stars), Neutral (3 stars), Negative (1–2 stars), or Mixed (positive content with negative elements)
2. **Intent signal**: Praise, constructive feedback, complaint seeking resolution, venting/emotional, competitive comparison, or suspected fraudulent/spam
3. **Specificity level**: Vague sentiment only, references specific interaction/feature, or contains detailed incident narrative
4. **ICA alignment**: Does this reviewer match the ICA profile? (High-value retention target vs. non-ICA audience)
5. **Visibility risk**: Platform prominence, review recency, and likelihood of being read by prospective buyers (high/medium/low)
6. **Escalation flag**: Does this review reference unresolved issues, legal threats, health/safety concerns, or employee conduct requiring offline resolution?

Document the classification matrix before proceeding.

## Step 4: Do the Work

Draft the response applying the **R.E.S.T.O.R.E. Framework**:

1. **Recognise** — Acknowledge the reviewer by name (if available) and thank them for the specific effort of leaving feedback. Mirror their language to demonstrate the review was read fully, not template-matched.

2. **Empathise** — For negative or mixed reviews, validate the emotional experience without defensiveness. Use first-person accountability language ("We fell short" not "We're sorry you feel that way"). For positive reviews, reflect genuine appreciation tied to a specific detail they mentioned.

3. **Specify** — Reference concrete details from the review to prove attentiveness. Never respond generically to a specific complaint. If the reviewer mentioned a particular interaction, product, or date, echo it back.

4. **Take ownership** — For negative reviews, state clearly what went wrong (if known) or commit to investigating. Avoid deflection, blame-shifting to the customer, or corporate hedging language. For positive reviews, credit the team or process the reviewer praised.

5. **Offer resolution** — For negative/mixed reviews, propose a concrete next step: direct contact channel (name + email/phone), specific remedy, or timeline for follow-up. The offer must be actionable, not vague ("please reach out" without a channel is insufficient). For positive reviews, offer an invitation to deepen the relationship (referral programme, new feature preview, loyalty benefit).

6. **Reinforce value** — Subtly weave in one brand differentiator or value proposition relevant to the review context. This line is written for prospective buyers reading the response, not just the reviewer.

7. **End with warmth** — Close with a forward-looking, human statement. No corporate sign-offs. Match the emotional register of the review — celebratory for positive, earnest for negative.

Apply any user-specific `instructions` from FutureProof context, including:
- Brand voice calibration from prior sessions
- Known product issues and approved messaging
- Legal/compliance language requirements
- Previously tested response patterns and their performance data

### Additional Quality Checks

- **Tone calibration**: Response emotional weight must be proportional to review severity — a 1-star review describing a genuinely harmful experience requires deeper empathy than a 2-star review about slow shipping
- **Length matching**: Response length should be proportional to review length (±30%) — never write a 200-word response to a 15-word review
- **Platform norms**: Adapt formality and structure to platform conventions (Google Business responses trend shorter; G2 responses can be more detailed and technical; Yelp audiences expect personality)
- **SEO awareness**: For Google reviews, naturally incorporate relevant service/product keywords without keyword-stuffing
- **Privacy compliance**: Never reference order details, account information, or personal data in public responses

## Step 5: Deliver Output

Produce the following structured deliverable:

### Review Classification Matrix
| Dimension | Assessment |
|---|---|
| Sentiment Tier | [rating] |
| Intent Signal | [classification] |
| Specificity Level | [level] |
| ICA Alignment | [high/medium/low] |
| Visibility Risk | [high/medium/low] |
| Escalation Flag | [yes/no — with reason if yes] |

### Drafted Response
The complete, ready-to-publish response formatted for the target platform, including appropriate character count notation if platform limits apply.

### Response Strategy Notes
- **Primary objective** of this response (e.g., win-back, social proof amplification, damage containment)
- **Audience beyond the reviewer** — what prospective buyers should take away from reading this exchange
- **Internal action items** — any operational follow-up required (e.g., "Escalate to CS team: order #X requires refund processing before this response is posted")
- **Recommended posting timing** — optimal window based on platform visibility algorithms and urgency of the review

### Batch Mode (if multiple reviews provided)
When processing 3+ reviews, additionally deliver:
- **Sentiment distribution summary** across the batch
- **Recurring theme analysis** — patterns indicating systemic issues or consistent strengths
- **Priority ranking** — which reviews to respond to first based on visibility risk × ICA alignment
- **Response template recommendations** — where similar reviews warrant a templated approach vs. bespoke drafting

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="review-response-writer", experiment={
  hypothesis: "Responses that reference a specific reviewer detail in the opening line generate higher reviewer engagement (edits, follow-up, rating change) than responses opening with a generic thank-you",
  variants: ["control: 'Thank you for your feedback, [Name]'", "variant: '[Name], your point about [specific detail] really resonated with our team'"],
  measurement: "Track reviewer follow-up rate, rating updates, and sentiment shift across next 30 review responses",
  expected_impact: "20% increase in reviewer re-engagement and 10% increase in rating upgrades on negative reviews"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="review-response-writer",
  query="2024-2025 review response best practices by platform, impact of owner responses on conversion rates, and emerging patterns in review authenticity detection algorithms",
  reason="Ensure response strategies align with current platform algorithms, consumer trust signals, and evolving best practices for turning review management into a measurable revenue channel"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="review-response-writer", session={
  summary: "Drafted [number] review response(s) for [platform] — [sentiment tier] review(s) regarding [product/service/location]",
  key_findings: ["finding 1: e.g., recurring complaint theme identified around [topic]", "finding 2: e.g., brand voice calibrated to [tone descriptor] per user preference", "finding 3: e.g., escalation flagged for [issue] requiring offline resolution"],
  user_feedback: null
})
```