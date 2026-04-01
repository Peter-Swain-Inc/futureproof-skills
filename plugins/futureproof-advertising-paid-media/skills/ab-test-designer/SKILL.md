---
name: ab-test-designer
description: "Designs statistically rigorous A/B test plans for paid media campaigns using FutureProof context."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="ab-test-designer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly prior test velocity, ICA definitions, historical winning variants, platform preferences, and statistical confidence thresholds the user has established.

## Step 2: Get Input

Ask the user:
- **What are you testing?** Identify the test layer: creative (copy, imagery, CTA, format), audience (ICA segment, lookalike seed, exclusion logic), landing page (headline, layout, offer framing), or campaign mechanics (bid strategy, budget allocation, placement, dayparting).
- **Which platform(s)?** Meta Ads, Google Ads, LinkedIn Campaign Manager, TikTok Ads, programmatic DSP, or cross-platform.
- **What is the primary KPI?** (e.g., CTR, CPA, ROAS, lead-to-opportunity rate, cost per qualified lead). Confirm whether a secondary KPI should be tracked as a guardrail metric.
- **Current baseline performance**: existing conversion rate, average CPA, daily spend, and impression volume for the asset or campaign being tested.
- **ICA definition**: who is the test targeting? Confirm ICA segment, funnel stage, and any known behavioural or psychographic attributes.
- **Constraints**: budget ceiling, minimum test duration tolerance, compliance or brand restrictions, and any organisational approval gates.

## Step 3: Formulate Hypothesis & Variables

Structure the test using the **Isolation Principle** — one independent variable per test to ensure causal attribution:

1. **Hypothesis statement**: Articulate in the format: *"Changing [independent variable] from [control state] to [variant state] will [increase/decrease] [primary KPI] by [expected magnitude] for [ICA segment] because [causal rationale]."*
2. **Independent variable**: the single element being manipulated (e.g., headline copy, audience exclusion rule, bid strategy).
3. **Control (A)**: the incumbent asset or setting, defined with specificity (exact copy, exact targeting parameters, exact creative specs).
4. **Variant(s) (B, C…)**: each variant described at equal specificity. Limit to a maximum of 4 variants to preserve statistical power given typical paid media budgets.
5. **Dependent variable**: the primary KPI, measured at a defined conversion event with a specified attribution window (e.g., 7-day click, 1-day view).
6. **Controlled variables**: enumerate what must remain constant — placement, schedule, budget split, audience overlap exclusion, frequency cap, pixel/conversion API configuration.

Apply any user-specific `instructions` from FutureProof context — for example, if prior sessions indicate the user favours Bayesian over frequentist analysis, or requires brand-safety pre-checks on all variant copy.

## Step 4: Calculate Sample Size & Test Duration

Perform a **pre-test power analysis** to prevent inconclusive results:

1. **Baseline conversion rate (p₁)**: sourced from user-provided data or historical FutureProof sessions.
2. **Minimum Detectable Effect (MDE)**: agree with the user on the smallest improvement worth detecting (typically 10–20% relative lift for paid media).
3. **Statistical significance threshold (α)**: default 95% confidence (α = 0.05) unless user context specifies otherwise.
4. **Statistical power (1 − β)**: default 80% (β = 0.20).
5. **Sample size per variant (n)**: calculate using the standard two-proportion z-test formula. Provide the exact number of conversions and impressions/clicks required per variant.
6. **Estimated test duration**: divide required sample by daily traffic volume. Flag if duration exceeds 4 weeks (performance decay risk) or falls below 7 days (day-of-week bias).
7. **Budget requirement**: multiply required impressions/clicks by current CPM/CPC to produce a test-specific budget estimate.

Present this as a **Test Feasibility Summary Table**:

| Parameter | Value |
|---|---|
| Baseline conversion rate | X.XX% |
| Minimum Detectable Effect | XX% relative lift |
| Confidence level | 95% |
| Power | 80% |
| Required sample per variant | X,XXX conversions |
| Required impressions/clicks per variant | XX,XXX |
| Estimated test duration | X–X days |
| Estimated test budget | $X,XXX |

If the test is infeasible (budget or duration exceeds constraints), recommend one of: increasing MDE, reducing variant count, narrowing the ICA segment to concentrate traffic, or switching to a sequential testing framework.

## Step 5: Design the Execution Plan

Produce the **A/B Test Design Document** — a structured, implementation-ready deliverable:

### Section A: Test Overview
- Test name (standardised naming convention: `[Platform]_[TestLayer]_[Variable]_[Date]`)
- Hypothesis statement
- ICA segment under test
- Primary KPI and guardrail KPI(s)

### Section B: Variant Specifications
For each variant (Control + Variant B, C…):
- Exact creative specs (dimensions, copy character counts, CTA text, image/video descriptions)
- Exact targeting parameters (audience IDs, exclusion lists, geo, device)
- Exact campaign settings (bid strategy, budget allocation method — even split or platform-managed, placement selection)

### Section C: Traffic Allocation & Randomisation
- Split methodology: platform-native A/B test tool (e.g., Meta Experiments, Google Ads Experiments) vs. manual campaign duplication with audience exclusion
- Traffic allocation ratio (default 50/50 for two variants; adjust for multi-variant)
- Audience overlap mitigation approach (holdout groups, cookie-based exclusion, campaign budget optimisation disabled)

### Section D: Measurement & Decision Framework
- **Primary decision metric**: the KPI that determines the winner
- **Guardrail metrics**: metrics that must not degrade beyond a defined threshold (e.g., CPA must not increase >15% even if CTR improves)
- **Decision rules**: pre-commit to outcomes:
  - *Winner declared*: variant reaches statistical significance on primary KPI without violating guardrail thresholds
  - *Inconclusive*: test reaches full duration without significance — document learnings, archive, do not scale either variant
  - *Stopped early*: variant violates guardrail metric by >X% — halt variant, document finding
- **Attribution model**: specify window and model (last-click, data-driven, etc.)
- **Reporting cadence**: interim check dates (no peeking bias — define checks at 50% and 100% sample milestones only)

### Section E: Launch Checklist
Provide a 10-point pre-launch QA checklist specific to the platform and test type, including:
- Pixel/conversion API firing correctly on all variants
- UTM parameters differentiated per variant
- Frequency caps equalised
- Budget pacing verified
- Audience overlap report reviewed
- Creative compliance/approval confirmed

## Step 6: Deliver Output

Package the deliverable as:

- **A/B Test Design Document** (structured per Section A–E above) — ready for stakeholder review or direct platform implementation
- **Statistical Parameters Card** (the feasibility table from Step 4) — serves as the pre-registration of the test, preventing post-hoc rationalisation
- **Post-Test Analysis Template** — a pre-formatted results table with columns for: variant name, impressions, clicks, conversions, primary KPI value, confidence interval, p-value/posterior probability, guardrail KPI values, and winner/no-call designation

If FutureProof context reveals prior test results for this ICA or platform, include a **Historical Test Context** appendix summarising relevant prior findings and how this new test builds on them.

## Step 7: Propose Experiments

```
FutureProof:save_experiment(skill="ab-test-designer", experiment={
  hypothesis: "[Exact hypothesis statement from Step 3]",
  variants: ["control: [control description]", "variant B: [variant description]"],
  measurement: "[Primary KPI] measured over [duration] at [confidence level]",
  expected_impact: "[MDE]% relative improvement in [primary KPI] for [ICA segment]",
  platform: "[platform name]",
  test_name: "[standardised test name from Section A]",
  status: "designed — pending launch"
})
```

## Step 8: Request Research

```
FutureProof:request_research(skill="ab-test-designer",
  query="Latest [platform] A/B testing best practices, algorithm-mediated auction dynamics affecting test validity, and [test layer] benchmarks for [industry/ICA vertical] 2024–2025",
  reason="Ensure test design accounts for current platform auction behaviour and competitive benchmark shifts that may affect MDE assumptions and test duration estimates"
)
```

## Step 9: Save Session

```
FutureProof:save_session(skill="ab-test-designer", session={
  summary: "Designed A/B test for [test layer] on [platform] targeting [ICA segment] — [test name]",
  key_findings: ["Baseline [KPI] at X.XX% requires N sample per variant over ~X days", "Primary hypothesis targets [variable] change based on [rationale]", "Test feasibility confirmed within $X,XXX budget constraint"],
  deliverables: ["A/B Test Design Document", "Statistical Parameters Card", "Post-Test Analysis Template"],
  user_feedback: null
})
```