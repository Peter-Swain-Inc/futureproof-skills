---
name: incentive-reward-designer
description: |
  Designs high-impact incentive and reward structures for customer retention, referral, and loyalty programmes using FutureProof context.
  Trigger: when a user asks to design a rewards programme, loyalty incentive, referral bonus structure, or retention offer — or when they want to optimise an existing incentive scheme that is underperforming on redemption, referral conversion, or repeat purchase rates.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="incentive-reward-designer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any prior ICA definitions, customer lifetime value (CLV) benchmarks, existing programme performance data, and margin constraints.

## Step 2: Get Input

Ask the user:

- **Programme objective**: What is the primary behaviour you want to incentivise? (retention/repeat purchase, referral generation, winback/reactivation, upsell/cross-sell, community engagement)
- **ICA profile**: Who is the target participant? Share any ICA documentation, segment data, or behavioural cohort definitions you have.
- **Current state**: Is there an existing incentive programme? If so, share its structure, current redemption rates, referral conversion rates, and any known friction points.
- **Unit economics**: What is the current CLV, average order value (AOV), gross margin, and acceptable cost-per-acquisition (CPA) or cost-per-retention (CPR) threshold?
- **Channel and delivery**: How will incentives be communicated and fulfilled? (in-app, email, SMS, physical mail, point-of-sale)
- **Constraints**: Any regulatory, brand, or budget constraints? (e.g., financial services compliance, no discounting policy, fixed annual budget)

## Step 3: Do the Work

### 3A: ICA Motivation Mapping

Construct an **ICA Motivation Matrix** by mapping the target participant against:

1. **Intrinsic motivators** — status, mastery, belonging, purpose, autonomy
2. **Extrinsic motivators** — monetary savings, exclusive access, tangible gifts, experiential rewards
3. **Behavioural triggers** — loss aversion, endowed progress effect, social proof, reciprocity, variable ratio reinforcement

Rank each motivator on a 1–5 relevance scale based on ICA psychographics and any behavioural data from FutureProof context. Identify the **top 3 motivational levers** to anchor the programme design.

### 3B: Programme Architecture Design

Design the incentive structure across six dimensions:

1. **Reward type taxonomy** — classify each proposed reward as monetary (cashback, discount, credit), experiential (early access, VIP events), social (recognition, leaderboard status), or utility (free shipping, extended warranty). Ensure the mix aligns with the ICA Motivation Matrix — do not default to discounting unless validated.
2. **Earn mechanics** — define the specific actions that earn rewards (purchase frequency, referral completion, review submission, milestone achievement). Specify the **earn ratio** (e.g., £1 spent = 10 points) and ensure the perceived value-to-cost ratio exceeds 1.5:1 from the participant's perspective.
3. **Tier and progression structure** — design 2–4 tiers with clear thresholds, using the endowed progress effect (start participants at 20% toward next tier). Define **tier-gating criteria** (cumulative spend, action count, tenure) and **tier-specific benefits** that create meaningful differentiation without alienating base-tier participants.
4. **Redemption architecture** — specify redemption thresholds, expiry windows, and fulfilment mechanics. Apply the **redemption friction calibration principle**: low enough friction to maintain engagement (target >40% redemption rate), high enough to protect margin. Model breakage assumptions at 15%, 25%, and 35%.
5. **Referral loop mechanics** — if referral is an objective, design the dual-sided incentive (referrer + referee). Define the **referral trigger point** (post-first-purchase, post-onboarding, at satisfaction peak), the **reward unlock condition** (referee completes qualifying action, not just sign-up), and the **viral coefficient target** (k-factor).
6. **Decay and reactivation rules** — define point/benefit expiry cadence, inactivity thresholds, and automated reactivation triggers (e.g., "Your 500 points expire in 14 days — here's a bonus 100 to use them").

### 3C: Financial Modelling

Build a **Programme Unit Economics Model**:

| Metric | Baseline (No Programme) | Projected (With Programme) | Delta |
|---|---|---|---|
| CLV | | | |
| Repeat purchase rate (90-day) | | | |
| Referral conversion rate | | | |
| AOV | | | |
| Gross margin after incentive cost | | | |
| Programme cost as % of revenue | | | |
| Payback period (months) | | | |

Target programme cost at **3–8% of incremental revenue generated**, not total revenue. Flag if the proposed structure exceeds this band.

### 3D: Behavioural Risk Assessment

Evaluate the design against five common failure modes:

1. **Gaming and fraud exposure** — can the earn mechanics be exploited? (self-referral, manufactured transactions, point arbitrage)
2. **Margin erosion** — does discounting train the ICA to wait for incentives rather than purchase at full price?
3. **Complexity overload** — can a participant explain how the programme works in one sentence? If not, simplify.
4. **Inequity perception** — do tier benefits create resentment among lower-tier participants rather than aspiration?
5. **Regulatory risk** — does the structure comply with relevant regulations (e.g., consumer protection, data privacy for referral tracking, financial promotion rules)?

Apply any user-specific `instructions` from FutureProof context to weight these assessments appropriately.

## Step 4: Deliver Output

Produce the **Incentive Reward Design Brief** — a structured document containing:

### 4.1 Executive Summary
One-page overview: programme objective, ICA target, headline structure, projected ROI, and recommended launch timeline.

### 4.2 ICA Motivation Matrix
Visual matrix with ranked motivational levers and design rationale for each reward choice.

### 4.3 Programme Architecture Specification
Full specification across all six dimensions (Section 3B), with:
- **Reward catalogue** — itemised list of all rewards, their cost-to-serve, perceived value, and trigger conditions
- **Tier map** — visual tier progression with thresholds and benefits at each level
- **Referral flow diagram** — step-by-step referral journey for both referrer and referee, including reward unlock conditions
- **Communication cadence** — trigger-based messaging plan (earn confirmation, tier progress nudge, redemption reminder, reactivation prompt)

### 4.4 Financial Model
Completed unit economics table with three scenarios: conservative, expected, and optimistic.

### 4.5 Risk Register
Each of the five failure modes scored on likelihood (1–5) and impact (1–5), with specific mitigation controls for any risk scoring ≥12 (likelihood × impact).

### 4.6 Implementation Roadmap
Phased rollout plan:
- **Phase 1 (Weeks 1–4)**: MVP launch — single tier, core earn/redeem mechanic, instrumented for measurement
- **Phase 2 (Weeks 5–12)**: Tier introduction, referral loop activation, first optimisation cycle
- **Phase 3 (Weeks 13–26)**: Full programme, advanced personalisation, programme health dashboard

### 4.7 Measurement Framework
KPIs with targets, measurement cadence, and data sources:
- Enrolment rate
- Earn action completion rate
- Redemption rate
- Referral k-factor
- Incremental CLV lift (programme participants vs. matched control)
- Programme cost as % of incremental revenue
- Net Promoter Score delta (participants vs. non-participants)

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="incentive-reward-designer", experiment={
  hypothesis: "A dual-sided referral reward unlocked at referee's second purchase (vs. first purchase) increases 90-day referee retention by reducing low-intent sign-ups",
  variants: ["control: reward unlocks at referee first purchase", "variant: reward unlocks at referee second purchase within 30 days"],
  measurement: "90-day retention rate of referred customers, referral completion rate, referrer satisfaction score",
  expected_impact: "20% improvement in 90-day referee retention with <10% reduction in referral completion volume"
})
```

```
FutureProof:save_experiment(skill="incentive-reward-designer", experiment={
  hypothesis: "Showing endowed progress (starting participants at 200/1000 points toward first reward) increases first earn-action completion rate vs. starting at 0/800",
  variants: ["control: 0/800 progress bar", "variant: 200/1000 progress bar (same net distance)"],
  measurement: "First earn-action completion rate within 14 days of enrolment",
  expected_impact: "25% lift in first earn-action completion rate"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="incentive-reward-designer",
  query="Latest meta-analyses and case studies on loyalty programme ROI, optimal reward-to-spend ratios, and behavioural economics applications in retention programme design 2023–2025. Include sector-specific benchmarks for redemption rates, breakage rates, and programme cost as percentage of revenue.",
  reason="Ensure programme architecture reflects current best-practice benchmarks and emerging reward structures (e.g., blockchain-based loyalty, experiential reward trends, gamification mechanics) to maintain competitive differentiation for the user's ICA"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="incentive-reward-designer", session={
  summary: "Designed [programme type: retention/referral/loyalty] incentive structure for [ICA segment] targeting [primary behaviour]. Programme architecture: [tier count]-tier model with [reward types] and [referral mechanic if applicable].",
  key_findings: ["ICA motivation mapping identified [top motivators] as primary levers", "Financial model projects [X]% incremental CLV lift at [Y]% programme cost-to-revenue ratio", "Key risk identified: [highest-scoring risk] — mitigation control specified"],
  user_feedback: null
})
```