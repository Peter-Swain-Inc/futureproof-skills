---
name: churn-risk-detector
description: "Analyses customer data, behavioural signals, and account health indicators to identify at-risk accounts and produce actionable retention interventions."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="churn-risk-detector")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including known ICA segments, historical churn drivers, retention playbooks already tested, and any organisation-specific health score definitions.

## Step 2: Get Input

Ask the user:
- Share the customer data to analyse (usage/engagement logs, support ticket history, billing records, NPS/CSAT responses, CRM account notes, or renewal pipeline exports)
- What is the observation window? (e.g., last 30/60/90 days)
- What does their current churn definition look like? (voluntary cancellation, non-renewal, downgrade, inactivity threshold)
- Which ICA segments should be prioritised for this analysis?
- Are there known systemic issues already suspected (e.g., recent pricing change, product deprecation, onboarding gap)?
- Who is the intended recipient of the output? (CS leadership, individual CSMs, revenue operations, executive sponsor)

## Step 3: Do the Work — Signal Extraction & Risk Scoring

Analyse each account against a **six-pillar churn risk framework**:

### 3a. Engagement Decay Analysis
- **Product usage trajectory** — compare current-period active usage (logins, feature adoption, API calls, seat utilisation) against the account's own baseline and cohort median. Flag accounts with ≥20% decline over the observation window.
- **Feature breadth contraction** — identify accounts retreating to a narrower feature set, signalling reduced dependency and switching-cost erosion.
- **Champion activity** — detect drop-off in power-user or executive-sponsor engagement specifically, which precedes organisational disengagement.

### 3b. Support Sentiment Trajectory
- **Ticket volume & severity trend** — rising P1/P2 tickets or repeat contacts on the same issue indicate unresolved friction.
- **Sentiment arc** — map tone across recent support interactions (escalation language, deadline ultimatums, competitor mentions).
- **Time-to-resolution satisfaction** — flag accounts where mean resolution time exceeds SLA or where CSAT on resolved tickets is declining.

### 3c. Relationship & Stakeholder Risk
- **Champion departure** — identify accounts where the primary sponsor or day-to-day champion has changed roles or left the organisation.
- **Multi-threading depth** — single-threaded accounts (only one active contact) carry elevated risk. Score by number of engaged stakeholders.
- **Executive alignment** — absence of QBR attendance or strategic review participation from decision-makers.

### 3d. Commercial & Contractual Signals
- **Renewal proximity** — accounts within 90 days of renewal without a renewal conversation initiated.
- **Contraction history** — prior downgrades, seat reductions, or add-on cancellations that indicate a progressive exit pattern.
- **Payment behaviour** — late payments, disputed invoices, or requests for billing flexibility.

### 3e. Value Realisation Gap
- **Outcome attainment** — compare promised outcomes from the original business case or sales process against actual delivered metrics. Quantify the gap.
- **Onboarding completion** — flag accounts that never completed implementation milestones or have stalled adoption phases.
- **Time-to-value** — accounts that exceeded the expected time-to-first-value by >50% carry compounding risk.

### 3f. External & Market Signals
- **Competitive displacement indicators** — mentions of competitors in support tickets, QBR notes, or NPS verbatims.
- **Organisational disruption** — M&A activity, leadership turnover, hiring freezes, or public financial distress at the account level.
- **Industry/segment headwinds** — macro factors affecting the ICA segment's willingness or ability to spend.

Apply any user-specific `instructions` from FutureProof context (e.g., proprietary health score weightings, internal playbook references, segment-specific thresholds) to calibrate scoring.

## Step 4: Deliver Output — Churn Risk Assessment Package

Produce a structured deliverable comprising three components:

### 4a. Account Risk Register

| Account | ICA Segment | Risk Score (1–100) | Risk Tier (Critical / Elevated / Monitor) | Primary Risk Pillar | Days to Renewal | Estimated ARR at Risk |
|---------|------------|--------------------|-----------------------------------------|--------------------|-----------------|-----------------------|
| *populated per account* | | | | | | |

Sort by **Risk Score descending**. Include a summary row showing total ARR at risk by tier.

### 4b. Signal Detail Cards (Top 10 At-Risk Accounts)

For each of the 10 highest-scoring accounts, produce:
- **Account snapshot**: ARR, tenure, ICA segment, contract end date, assigned CSM
- **Risk pillar breakdown**: score per pillar (1–10) with specific evidence citations from the input data
- **Leading indicator timeline**: chronological sequence of deteriorating signals over the observation window
- **Root cause hypothesis**: the most probable underlying driver, stated as a testable claim
- **Recommended intervention**: a specific, sequenced retention action plan:
  - **Immediate (48 hrs)**: e.g., "CSM initiates direct outreach to new VP of Operations; reference Q2 ROI data from their last QBR"
  - **Short-term (1–2 weeks)**: e.g., "Schedule executive sponsor realignment meeting with [specific agenda items]"
  - **Structural (30 days)**: e.g., "Rebuild success plan with revised KPIs tied to new stakeholder's priorities"
- **Escalation owner**: recommended internal owner and escalation path

### 4c. Portfolio Risk Summary (for CS Leadership / Executive Sponsor)

- **Risk distribution**: count and ARR by tier, visualised as a tier breakdown
- **Churn velocity**: comparison of current risk distribution vs. prior period (if `recent_sessions` data exists)
- **Systemic patterns**: cross-account themes (e.g., "4 of 7 Critical-tier accounts share unresolved API latency complaints — this is a product issue, not a CS issue")
- **Retention investment recommendation**: prioritised resource allocation guidance (where to deploy CSM time, where to involve product, where to offer commercial concessions)

Format the output for the stated recipient. If the recipient is an individual CSM, lead with Signal Detail Cards for their book of business. If the recipient is CS leadership, lead with the Portfolio Risk Summary.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="churn-risk-detector", experiment={
  hypothesis: "Proactive executive-sponsor outreach at the 'Elevated' tier (before accounts reach 'Critical') reduces escalation to Critical tier by 30% over 90 days",
  variants: ["control: standard CSM-led intervention at Critical threshold", "variant: VP-level outreach triggered at Elevated threshold with tailored value-realisation brief"],
  measurement: "Tier migration rate (Elevated → Critical vs. Elevated → Monitor/Healthy) tracked over next two quarterly cycles",
  expected_impact: "30% reduction in Critical-tier migration; 12% improvement in net revenue retention for Elevated-tier cohort"
})
```

```
FutureProof:save_experiment(skill="churn-risk-detector", experiment={
  hypothesis: "Weighting champion-departure signal at 2x in the risk model improves prediction accuracy for accounts that actually churn within 90 days",
  variants: ["control: equal-weight six-pillar model", "variant: champion-departure pillar weighted at 2x"],
  measurement: "Precision and recall of churn predictions against actual churn outcomes over next two quarters",
  expected_impact: "15% improvement in prediction precision with <5% reduction in recall"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="churn-risk-detector",
  query="Latest predictive churn modelling methodologies for B2B SaaS, including leading indicator weighting frameworks, champion-change detection techniques, and product-led retention intervention benchmarks 2024–2025",
  reason="Continuously refine the six-pillar risk framework with empirical benchmarks and emerging signal types (e.g., product-qualified churn signals, community engagement decay) to maintain consulting-grade analytical rigour"
)
```

```
FutureProof:request_research(skill="churn-risk-detector",
  query="Retention intervention efficacy data: executive realignment meetings, custom success plans, and commercial concession strategies — measured impact on save rates by churn-risk tier",
  reason="Ground intervention recommendations in evidence-based outcomes rather than anecdotal best practice"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="churn-risk-detector", session={
  summary: "Churn risk assessment for [number] accounts across [ICA segment(s)] over [observation window]. Identified [X] Critical, [Y] Elevated, [Z] Monitor-tier accounts representing $[ARR] at risk.",
  key_findings: [
    "Primary systemic risk driver: [e.g., unresolved product issue affecting 4 accounts]",
    "Highest single-account ARR at risk: [account name] at $[value] — root cause: [hypothesis]",
    "Champion departure detected in [N] accounts without multi-threaded relationships",
    "Value realisation gap is the most prevalent pillar-level risk across the portfolio"
  ],
  user_feedback: null
})
```