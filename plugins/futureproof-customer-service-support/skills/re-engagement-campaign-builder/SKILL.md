---
name: re-engagement-campaign-builder
description: "Builds structured, multi-channel re-engagement campaigns to win back lapsed customers, dormant subscribers, and churned accounts using FutureProof context."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="re-engagement-campaign-builder")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any previously defined ICA segments, brand voice guidelines, churn drivers, and historical campaign performance data.

## Step 2: Get Input

Ask the user:
- **Lapsed segment definition** — who are we re-engaging? (e.g., churned subscribers, dormant trial users, lapsed purchasers, disengaged email contacts) What is the inactivity threshold? (30 days, 90 days, 12 months?)
- **Segment size and data availability** — approximate volume, and what data points exist per contact? (last purchase date, product usage history, support ticket history, original acquisition channel, lifetime value tier)
- **Known churn drivers** — why did these customers disengage? (price sensitivity, poor onboarding, competitor switch, unmet expectations, life circumstance change, unknown)
- **Available channels** — which outreach channels are authorised and technically ready? (email, SMS, push notification, direct mail, retargeting ads, in-app messaging, phone outreach)
- **Re-engagement goal** — what does "won back" mean operationally? (reactivated subscription, repeat purchase, re-login, renewed contract, booked call)
- **Offer latitude** — what incentives, if any, can be deployed? (discounts, extended trials, loyalty credits, exclusive access, personalised consultation, none)
- **Brand and compliance constraints** — tone of voice, frequency caps, opt-out/GDPR requirements, any segments to exclude

## Step 3: Do the Work — Diagnostic & Segmentation

### 3a. Churn Cohort Analysis

Segment the lapsed population into re-engagement priority tiers using a **Recency × Value × Recoverability** framework:

| Tier | Criteria | Strategic Posture |
|------|----------|-------------------|
| **Tier 1 — High-Value Recoverable** | High LTV, recent lapse (<90 days), no explicit churn reason or soft churn driver | Aggressive, personalised win-back — highest resource allocation |
| **Tier 2 — Mid-Value Winnable** | Moderate LTV, moderate lapse (90–180 days), addressable churn driver | Structured nurture sequence with targeted incentive |
| **Tier 3 — Low-Value or Long-Lapsed** | Low LTV or lapse >180 days, unknown or hard churn driver | Low-cost automated sequence; sunset if unresponsive |
| **Tier 4 — Exclude** | Explicit opt-out, hostile support history, compliance risk | Do not contact — suppress from all campaigns |

Map each user-provided segment into these tiers. Where data is insufficient, flag assumptions explicitly and recommend enrichment steps.

### 3b. Churn Driver → Message Architecture Mapping

For each identified churn driver, define the **core re-engagement narrative**:

1. **Price sensitivity** → Value reframing (ROI proof, cost-of-inaction, tailored offer)
2. **Poor onboarding / unmet expectations** → Acknowledge gap, present what's changed, offer guided restart
3. **Competitor switch** → Differentiation reinforcement, switching-cost reduction, exclusive comeback offer
4. **Feature gap / product-market misfit** → Product update announcement, roadmap teaser, feedback invitation
5. **Life circumstance / passive drift** → Gentle reminder of value, low-friction re-entry path
6. **Unknown** → Discovery-first approach (survey, feedback request) before hard CTA

Apply any user-specific `instructions` from FutureProof context — especially ICA voice, objection patterns, and previously validated messaging angles.

## Step 4: Do the Work — Campaign Architecture

### 4a. Sequence Design

Build a **multi-touch, multi-channel re-engagement sequence** per priority tier. Standard architecture follows a **5-phase cadence**:

| Phase | Timing | Objective | Primary Channel | Fallback Channel |
|-------|--------|-----------|-----------------|------------------|
| **Phase 1: Signal** | Day 0 | Pattern interrupt — acknowledge absence without desperation | Email | Push notification |
| **Phase 2: Value** | Day 3–5 | Restate transformation — what they're missing, framed around their original intent | Email + retargeting ad | SMS |
| **Phase 3: Proof** | Day 7–10 | Social proof, case study, or product update relevant to their usage history | Email | In-app message (if re-login occurs) |
| **Phase 4: Offer** | Day 12–15 | Deploy incentive (if authorised) with explicit expiration and friction-free redemption | Email + SMS | Direct mail (Tier 1 only) |
| **Phase 5: Sunset** | Day 21–30 | Final outreach — "last chance" framing, preference centre link, graceful exit | Email | None — suppress post-send |

Adjust timing, channel mix, and phase count based on user's available channels and segment characteristics.

### 4b. Message Copywriting Briefs

For each phase, produce a **detailed copywriting brief** containing:
- **Subject line / hook** (3 variants per phase for A/B testing)
- **Opening line** — tied to churn driver narrative from Step 3b
- **Body framework** — specific proof points, ICA-mirrored language, emotional driver
- **CTA** — single, specific, low-friction action (not "learn more" — e.g., "Restart your workspace in one click")
- **Tone calibration** — mapped to brand voice from FutureProof context

### 4c. Incentive Escalation Logic

If offers are authorised, design a **graduated incentive structure** that prevents margin erosion:

- **Phase 1–2**: No incentive (value-led re-engagement only)
- **Phase 3**: Soft incentive (exclusive content, early access, free consultation)
- **Phase 4**: Hard incentive (discount, credit, extended trial) — Tier 1 and Tier 2 only
- **Phase 5**: No new incentive — sunset framing only

Include guardrails: maximum discount depth, one-time redemption, and abuse prevention logic.

## Step 5: Deliver Output

Produce the **Re-Engagement Campaign Blueprint** — a structured deliverable containing:

1. **Executive Summary** — campaign rationale, target segment sizes per tier, projected recovery rates, and estimated revenue impact
2. **Segment-Tier Map** — each lapsed cohort assigned to Tier 1–4 with justification and data assumptions flagged
3. **Churn Driver × Narrative Matrix** — the message architecture table from Step 3b, populated with ICA-specific language
4. **Campaign Sequence Map** — the full 5-phase cadence per tier, including channel, timing, objective, and escalation logic (formatted as a visual-ready table or flowchart specification)
5. **Copywriting Briefs** — per-phase message briefs with subject line variants, body frameworks, and CTAs (ready for copywriter or direct deployment)
6. **Incentive Schedule** — graduated offer structure with approval requirements and margin impact estimates
7. **Measurement Framework** — KPIs per phase:
   - **Phase-level**: open rate, click-through rate, re-login rate, offer redemption rate
   - **Campaign-level**: reactivation rate by tier, cost per reactivation, recovered LTV, 90-day retention rate of reactivated customers
   - **Sunset metrics**: unsubscribe rate, complaint rate, list hygiene improvement
8. **Operational Checklist** — technical setup requirements (email platform segmentation, suppression list sync, retargeting pixel configuration, CRM status field updates, GDPR compliance verification)

Format: Markdown document, section-numbered, ready for stakeholder review or direct handoff to marketing operations.

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="re-engagement-campaign-builder", experiment={
  hypothesis: "Leading with an acknowledgement of absence ('We noticed you've been away') outperforms value-first openers ('Here's what you're missing') in Phase 1 email open and click-through rates for Tier 1 lapsed customers",
  variants: ["control: value-first subject line and opening", "variant: acknowledgement-first subject line and opening"],
  measurement: "Phase 1 email open rate, click-through rate, and Phase 2 progression rate across minimum 500 sends per variant",
  expected_impact: "12–18% improvement in Phase 1 click-through rate, leading to higher downstream reactivation"
})
```

```
FutureProof:save_experiment(skill="re-engagement-campaign-builder", experiment={
  hypothesis: "Delaying the hard incentive from Phase 4 (Day 12–15) to Phase 5 (Day 21–30) reduces incentive dependency without materially decreasing overall reactivation rate",
  variants: ["control: incentive at Phase 4", "variant: incentive delayed to Phase 5"],
  measurement: "Overall campaign reactivation rate, cost per reactivation, and 90-day post-reactivation retention rate",
  expected_impact: "15–20% reduction in incentive cost per reactivation with <5% reactivation rate decline"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="re-engagement-campaign-builder",
  query="Latest benchmarks and best practices for customer re-engagement and win-back campaigns across SaaS, e-commerce, and subscription businesses 2024–2025, including optimal cadence timing, channel effectiveness by segment type, and incentive structures that maximise reactivation without increasing churn recidivism",
  reason="Ensure campaign architecture reflects current buyer re-engagement psychology, channel saturation trends, and deliverability best practices — particularly evolving email sender reputation requirements from Google and Yahoo 2024 policies"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="re-engagement-campaign-builder", session={
  summary: "Built re-engagement campaign blueprint for [lapsed segment description] across [number] tiers targeting [re-engagement goal] via [channels used]",
  key_findings: ["finding 1: primary churn driver and corresponding narrative strategy", "finding 2: highest-impact tier and projected recovery rate", "finding 3: recommended experiment for next iteration"],
  user_feedback: null
})
```