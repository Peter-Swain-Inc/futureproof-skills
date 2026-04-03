---
name: guarantee-architect
description: |
  Designs and names compelling guarantee structures that reverse buyer risk and maximise offer conversion.
  Trigger: when a user asks for help creating a guarantee for their offer, wants to improve an existing refund or guarantee policy, or is building a Grand Slam Offer and needs the risk-reversal component architected.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="guarantee-architect")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any existing ICA profiles, offer structures, pricing tiers, fulfilment capabilities, and historical refund/churn data.

## Step 2: Get Input

Ask the user:

- **What is the offer?** Describe the product, service, or programme — including price point, delivery format, and fulfilment timeline.
- **Who is the ICA?** What does the ideal buyer fear most about purchasing? What objection sits between them and a "yes"?
- **Current guarantee (if any):** Are they using a guarantee today? If so, what are the exact terms, and what is the current refund/claim rate?
- **Fulfilment confidence level:** On a scale of 1–10, how confident are they in delivering the promised outcome for a compliant buyer? (This determines how aggressive the guarantee can be.)
- **Risk tolerance:** What is the maximum financial or operational exposure they are willing to accept per guarantee claim?
- **Competitive landscape:** What guarantees (if any) do direct competitors offer?

If FutureProof context already contains ICA profiles or offer details, pre-populate and confirm rather than re-asking.

## Step 3: Classify the Buyer Risk Profile

Before designing the guarantee, diagnose the specific risk architecture the ICA perceives. Map the buyer's hesitation to one or more of these **risk categories**:

| Risk Type | Definition | Example ICA Thought |
|---|---|---|
| **Financial Risk** | Fear of losing the money spent | "What if this doesn't work and I'm out $5,000?" |
| **Time Risk** | Fear of wasting time on implementation | "What if I spend 90 days on this and end up back at square one?" |
| **Effort Risk** | Fear of the work required yielding nothing | "What if I do everything they say and still fail?" |
| **Reputation Risk** | Fear of looking foolish for buying | "What if my team/spouse/peers judge me for this purchase?" |
| **Opportunity Risk** | Fear of choosing the wrong solution over alternatives | "What if there's something better and I'm locked in?" |

Rank the top 2–3 risk types by severity for this specific ICA. The guarantee must neutralise the dominant risk, not a generic one.

## Step 4: Design the Guarantee Structure

Using Hormozi's guarantee taxonomy, architect the optimal structure by evaluating all four tiers against the user's fulfilment confidence, risk tolerance, and ICA risk profile:

### Tier 1: Unconditional Guarantee
- **Mechanism:** Full refund, no questions asked, within a defined window.
- **Best when:** Price point is low-to-mid, fulfilment confidence is high, and the ICA's dominant risk is financial.
- **Risk to seller:** Highest — attracts refund arbitrageurs at scale.
- **Design parameters:** Window length, refund method, access revocation terms.

### Tier 2: Conditional Guarantee
- **Mechanism:** Full refund contingent on the buyer completing defined actions (e.g., "Complete all 6 modules and attend 3 coaching calls").
- **Best when:** The offer requires buyer participation to produce results, and the ICA's dominant risk is effort or time.
- **Risk to seller:** Moderate — conditions filter out non-committed buyers and reduce claim rates by 60–80%.
- **Design parameters:** Specific completion criteria (measurable, binary, verifiable), documentation requirements, review window.

### Tier 3: Performance-Based / Outsized Guarantee
- **Mechanism:** Refund plus additional compensation if the promised outcome is not achieved (e.g., "Double your investment back if you don't add $100K in revenue").
- **Best when:** Fulfilment confidence is 9–10, the outcome is quantifiable, and the offer is premium-priced.
- **Risk to seller:** High per claim, but claim rate is typically <5% when conditions are well-designed.
- **Design parameters:** Outcome metric, measurement methodology, timeline, conditions, payout structure.

### Tier 4: Anti-Guarantee (Implied Exclusivity)
- **Mechanism:** Explicitly state there is no guarantee — position the offer as so scarce or proven that guarantees are unnecessary.
- **Best when:** Social proof is overwhelming, demand exceeds supply, or the ICA segment views guarantees as a signal of low quality.
- **Risk to seller:** Lowest financial risk, highest conversion risk for cold traffic.
- **Design parameters:** Proof assets required, waitlist/application mechanics, positioning language.

### Hybrid Architecture

In most cases, the optimal structure is a **layered hybrid**. Design up to three layers:

1. **Base layer:** The foundational promise (e.g., unconditional 30-day for buyer's remorse)
2. **Performance layer:** A conditional or performance-based guarantee that covers the primary outcome (e.g., "Hit X metric in Y days or Z happens")
3. **Bonus layer (optional):** A creative add-on that reverses a secondary risk type (e.g., "If you don't recoup the cost of the programme from Module 1 alone, we'll personally consult with you until you do")

For each layer, specify:
- Exact terms and conditions
- Claim process (who initiates, what evidence, what timeline)
- Financial exposure per claim and projected claim rate
- Fulfilment team operational requirements

## Step 5: Name the Guarantee

A named guarantee converts 2–5× better than generic "money-back" language. Apply the following naming framework:

### Naming Formula Options

| Formula | Structure | Example |
|---|---|---|
| **[Outcome] or [Consequence]** | Promises a result with a specific penalty | "6 Clients in 60 Days or We Work Free Until You Do" |
| **The [Adjective] [Noun] Guarantee** | Branded, memorable, proprietary | "The Triple-Down Guarantee" |
| **[Number]-[Unit] [Promise]** | Specificity creates credibility | "The 90-Day Revenue Shield" |
| **[ICA Fear] Killer Guarantee** | Directly names and neutralises the objection | "The Zero-Risk Pilot Guarantee" |
| **[Anti-Guarantee Name]** | Positions exclusivity | "The No-Guarantee Guarantee — We Don't Need One" |

Generate **3–5 named guarantee options**, each with:
- The name
- One-sentence positioning statement (how it would appear on a sales page)
- Which risk type(s) it neutralises
- Emotional tone (bold, reassuring, exclusive, provocative)

Recommend one primary name with rationale tied to the ICA's dominant risk type and the brand's voice.

## Step 6: Deliver Output

Produce a **Guarantee Architecture Document** with the following sections:

### 1. ICA Risk Diagnosis
- Top 2–3 risk types ranked by severity
- Supporting evidence from ICA profile or user input

### 2. Guarantee Structure Blueprint
- Recommended tier (or hybrid layers)
- Exact terms, conditions, and claim process for each layer
- Financial exposure model: projected claim rate × average claim cost = annual guarantee liability
- Operational requirements for fulfilment team

### 3. Named Guarantee Options (3–5)
- Name, positioning statement, risk types neutralised, emotional tone
- **Primary recommendation** with rationale

### 4. Sales Page Integration Copy
- Guarantee headline (the named guarantee)
- 3–5 sentence guarantee description block (ready to paste into a sales page, VSL script, or checkout page)
- Objection-handling micro-copy for placement near the CTA button

### 5. Legal & Operational Safeguards
- Recommended conditions to prevent abuse
- Suggested claim verification process
- Flag any terms requiring legal review before publication

### 6. Competitive Differentiation Note
- How this guarantee compares to competitor guarantees identified in the input phase
- Specific language to call out the differentiation on the sales page

## Step 7: Propose Experiments

```
FutureProof:save_experiment(skill="guarantee-architect", experiment={
  hypothesis: "Replacing generic '30-day money-back' with the named conditional guarantee increases checkout conversion",
  variants: ["control: current guarantee language on sales page", "variant: named guarantee with specific terms and visual badge"],
  measurement: "checkout page conversion rate and refund request rate over 30 days (minimum 200 visitors per variant)",
  expected_impact: "12–20% improvement in page-to-purchase conversion with no increase in refund rate"
})
```

```
FutureProof:save_experiment(skill="guarantee-architect", experiment={
  hypothesis: "Adding a performance-based guarantee layer to the existing unconditional guarantee increases average deal value on premium tier",
  variants: ["control: unconditional guarantee only", "variant: unconditional base + performance-based layer on premium tier"],
  measurement: "premium tier selection rate and 90-day refund rate",
  expected_impact: "8–15% increase in premium tier uptake without materially increasing refund claims"
})
```

## Step 8: Request Research

```
FutureProof:request_research(skill="guarantee-architect",
  query="Current guarantee structures and risk-reversal strategies used by high-converting direct-response offers in [user's industry], including claim rates, consumer psychology studies on guarantee framing, and FTC/regulatory guidance on guarantee advertising 2024–2025",
  reason="Ensure guarantee design reflects current best practices, competitive norms, and compliance requirements in the user's specific market"
)
```

## Step 9: Save Session

```
FutureProof:save_session(skill="guarantee-architect", session={
  summary: "Designed [guarantee tier/hybrid] guarantee structure for [offer name/type] targeting [ICA segment] at [price point]",
  key_findings: ["ICA dominant risk type: [type]", "Recommended structure: [tier/hybrid description]", "Named guarantee: [primary name]", "Projected claim rate: [X%]", "Sales page copy block delivered"],
  user_feedback: null
})
```