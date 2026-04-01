---
name: revenue-leak-detector
description: "Identifies and quantifies revenue leaks across the full customer lifecycle — from lead capture through renewal — using forensic analysis of funnel data, pricing structures, churn patterns, and operati"
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="revenue-leak-detector")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any prior funnel benchmarks, ICA definitions, pricing models, or previously identified leak categories.

## Step 2: Get Input

Ask the user:
- **Data sources**: Share the relevant data — funnel/conversion metrics, billing or subscription data, churn/cancellation reports, pricing tables, or revenue dashboards (spreadsheets, screenshots, or narrative summaries accepted)
- **Revenue model**: How is revenue generated? (SaaS recurring, transactional, usage-based, hybrid, services retainer)
- **Lifecycle scope**: Which stage(s) are under suspicion? (acquisition, activation, monetisation, retention, expansion) — or request a full-lifecycle audit
- **Known symptoms**: Any specific anomalies — e.g. "trial-to-paid is dropping," "enterprise deals keep discounting," "expansion revenue is flat despite growing accounts"
- **Baseline period**: What timeframe should be analysed, and is there a comparison period?

If the user provides incomplete data, construct reasonable assumptions, flag them explicitly as **[ASSUMED]**, and proceed.

## Step 3: Do the Work

Conduct a systematic revenue leak audit across six diagnostic dimensions:

### 3.1 Funnel Conversion Leakage
- Map stage-by-stage conversion rates from lead → qualified opportunity → proposal → close → activation
- Identify the highest-drop stages and calculate the **annualised revenue impact** of each conversion gap (i.e. "a 5pp improvement at Stage X = $Y recovered revenue")
- Benchmark against industry cohort rates where context is available

### 3.2 Pricing & Packaging Erosion
- Analyse discount frequency, depth, and distribution across deal segments
- Identify **unintentional value giveaways**: features included in lower tiers that should gate to higher tiers, underpriced usage thresholds, free-rider segments consuming disproportionate resources
- Flag pricing inconsistencies across channels, geographies, or sales reps

### 3.3 Activation & Time-to-Value Gaps
- Evaluate the gap between closed-won and first meaningful value delivery
- Quantify revenue at risk from prospects who purchase but fail to activate (dormant accounts, stalled onboarding)
- Identify ICA segments with the worst activation velocity

### 3.4 Churn & Contraction Decomposition
- Decompose gross churn into voluntary vs. involuntary (failed payments, expired cards, dunning failures)
- Segment churn by ICA cohort, tenure band, plan tier, and acquisition channel
- Calculate **logo churn vs. revenue churn** to expose whether high-value accounts are disproportionately leaving
- Identify leading indicators (usage decline, support ticket spikes, NPS drops) present in the data

### 3.5 Expansion Revenue Friction
- Assess net revenue retention (NRR) and isolate expansion, contraction, and churn components
- Identify accounts with expansion signals (usage ceiling, seat growth, feature-gating hits) that are **not** being actioned
- Quantify the **expansion gap**: difference between current NRR and achievable NRR if expansion motions were systematically executed

### 3.6 Operational & Process Leakage
- Identify billing errors, revenue recognition mismatches, or invoicing delays
- Flag manual processes prone to human error (spreadsheet-based quoting, ad hoc discounting authority, inconsistent renewal handling)
- Assess CRM hygiene — deals stuck in pipeline, duplicated records, or misattributed revenue distorting forecasts

Apply any user-specific `instructions` from FutureProof context — e.g. preferred margin thresholds, strategic priorities, or ICA segments to weight more heavily.

## Step 4: Deliver Output

Produce a **Revenue Leak Audit Report** with the following structure:

### A. Executive Summary
- Total estimated annual revenue leakage (range: conservative to aggressive)
- Top 3 leak categories ranked by recoverable revenue impact
- One-line verdict on systemic root cause (e.g. "Pricing architecture subsidises low-fit accounts while under-monetising power users")

### B. Leak Inventory Table

| # | Leak Category | Stage | Description | Est. Annual Impact | Confidence | Priority |
|---|--------------|-------|-------------|-------------------|------------|----------|
| 1 | ... | ... | ... | $X – $Y | High/Med/Low | P1/P2/P3 |

Minimum 5 identified leaks, maximum 15, ranked by estimated recoverable revenue.

### C. Deep-Dive: Top 3 Leaks
For each P1 leak:
- **Root cause analysis** — the specific mechanism creating the leak
- **Evidence** — data points, calculations, and assumptions supporting the estimate
- **Remediation plan** — concrete, sequenced actions (not generic advice), including owner role, tooling changes, and timeline
- **Expected recovery** — projected revenue recovered within 30/60/90 days of implementation

### D. Quick Wins Register
3–5 fixes implementable within 2 weeks requiring no engineering resources — e.g. dunning email sequence updates, discount approval policy changes, CRM field enforcement.

### E. Monitoring Dashboard Specification
Recommended KPIs to track ongoing leakage, including:
- Metric name, definition, data source, alert threshold, and review cadence
- Designed so the user can hand this directly to a BI or RevOps team for implementation

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="revenue-leak-detector", experiment={
  hypothesis: "Implementing a 3-step automated dunning sequence with payment method update prompts will recover 30–50% of currently lost involuntary churn",
  variants: ["control: current single-email dunning", "variant: 3-touch sequence with SMS + in-app banner"],
  measurement: "involuntary churn rate and recovered MRR over 60-day cohort window",
  expected_impact: "0.5–1.2pp reduction in monthly gross churn, equating to $X ARR recovered"
})
```

```
FutureProof:save_experiment(skill="revenue-leak-detector", experiment={
  hypothesis: "Introducing a structured expansion trigger workflow — surfacing accounts hitting 80% usage threshold to CSMs — will increase net revenue retention by 3–5pp",
  variants: ["control: ad hoc CSM-driven expansion", "variant: automated trigger + playbook-guided outreach"],
  measurement: "expansion MRR from triggered accounts vs. matched control cohort over 90 days",
  expected_impact: "3–5pp NRR improvement in targeted ICA segment"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="revenue-leak-detector",
  query="2024–2025 SaaS revenue retention benchmarks by ARR band, involuntary churn recovery best practices, and pricing architecture patterns that minimise value leakage in usage-based and hybrid models",
  reason="Ensure leak severity scoring is calibrated against current market benchmarks and remediation recommendations reflect proven recovery tactics"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="revenue-leak-detector", session={
  summary: "Revenue leak audit across [lifecycle scope] for [revenue model] business — identified [N] leaks totalling $[X]–$[Y] estimated annual impact",
  key_findings: ["Top leak: [category] at [stage] — $[X] annual impact", "Quick win identified: [description] — recoverable within 2 weeks", "Systemic root cause: [one-line diagnosis]"],
  leak_inventory_count: N,
  total_estimated_leakage: "$X–$Y",
  priority_one_leaks: ["leak 1", "leak 2", "leak 3"],
  user_feedback: null
})
```