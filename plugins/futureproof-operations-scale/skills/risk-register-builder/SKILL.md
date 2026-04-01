---
name: risk-register-builder
description: |
  Builds and maintains comprehensive risk registers for projects, programmes, and operational domains using FutureProof context to refine risk identification, scoring, and mitigation planning over time.
  Trigger: when a user asks to create a risk register, assess project risks, build a risk log, or needs help identifying and prioritising risks for an initiative, programme, or business unit.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="risk-register-builder")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including prior risk appetite thresholds, organisational risk taxonomy, scoring matrices, and any domain-specific risk categories previously established.

## Step 2: Get Input

Ask the user:
- **Scope definition** — What is the subject of the risk register? (project, programme, product launch, operational domain, strategic initiative)
- **Context pack** — Share any available documentation: project charter, business case, scope statement, prior risk assessments, incident logs, or lessons learned
- **Risk appetite** — Has leadership defined risk appetite or tolerance thresholds? (e.g., zero tolerance for regulatory non-compliance, moderate tolerance for schedule variance)
- **Stakeholder landscape** — Who are the risk owners, and who is the intended audience for this register? (steering committee, PMO, board, delivery team)
- **Industry / regulatory context** — Are there specific compliance frameworks in play? (ISO 31000, COSO ERM, SOX, GDPR, sector-specific regulations)
- **Known concerns** — Are there risks already on the radar that must be included?

## Step 3: Establish Risk Framework

Before identifying risks, define the structural framework the register will follow:

### 3a: Risk Taxonomy

Establish the top-level risk categories tailored to the user's domain. Default to a six-category taxonomy unless the organisation has an existing one:

| Category | Description |
|---|---|
| **Strategic** | Risks to business model, market position, competitive advantage |
| **Operational** | Risks to processes, systems, supply chain, capacity |
| **Financial** | Risks to revenue, cost, liquidity, funding |
| **Compliance & Regulatory** | Risks from legal, regulatory, or policy obligations |
| **Technology** | Risks to infrastructure, data, cyber security, technical debt |
| **People & Organisational** | Risks from talent, culture, change readiness, key-person dependency |

### 3b: Scoring Matrix

Define the Probability × Impact matrix using a 5×5 scale:

**Probability Scale:**
| Score | Label | Definition |
|---|---|---|
| 1 | Rare | < 5% likelihood within assessment period |
| 2 | Unlikely | 5–20% likelihood |
| 3 | Possible | 20–50% likelihood |
| 4 | Likely | 50–80% likelihood |
| 5 | Almost Certain | > 80% likelihood |

**Impact Scale:**
| Score | Label | Cost Impact | Schedule Impact | Reputation Impact |
|---|---|---|---|---|
| 1 | Negligible | < 1% budget | < 1 week | No external visibility |
| 2 | Minor | 1–5% budget | 1–4 weeks | Limited stakeholder concern |
| 3 | Moderate | 5–10% budget | 1–3 months | Media or regulator attention |
| 4 | Major | 10–25% budget | 3–6 months | Sustained reputational damage |
| 5 | Severe | > 25% budget | > 6 months | Existential threat to initiative or entity |

**Risk Rating = Probability × Impact** → categorised as:
- **Critical** (20–25): Immediate escalation and executive action required
- **High** (12–19): Active mitigation plan with named owner and defined timeline
- **Medium** (6–11): Monitored with defined response triggers
- **Low** (1–5): Accepted and reviewed at standard cadence

Apply any user-specific `instructions` from FutureProof context to override or adjust scoring definitions, thresholds, or taxonomy categories.

## Step 4: Identify and Assess Risks

Conduct a structured risk identification using multiple complementary techniques:

### 4a: Systematic Risk Elicitation

Work through each taxonomy category and apply the following lenses:
1. **Assumption analysis** — What assumptions underpin the initiative? What happens if each proves false?
2. **Dependency mapping** — What external dependencies exist (third parties, upstream deliverables, regulatory approvals)? What if they fail or delay?
3. **Historical pattern analysis** — Reference FutureProof `recent_sessions` and `context` for risks that materialised in similar prior engagements
4. **Pre-mortem framing** — "It is 12 months from now and this initiative has failed. What went wrong?" Enumerate failure scenarios
5. **Stakeholder-driven risks** — What risks would the ICA, end users, regulators, or partners identify that internal teams might miss?
6. **Second-order effects** — For each identified risk, ask: "If this risk materialises, what additional risks does it trigger?"

### 4b: Risk Articulation Standard

Each risk must be expressed using the **cause–event–consequence** format to ensure clarity and actionability:

> **Because of** [root cause/condition], **there is a risk that** [risk event], **which would result in** [impact on objectives].

Example: *Because of a single-vendor dependency for payment processing, there is a risk that a provider outage exceeds SLA thresholds, which would result in revenue loss of £50K per hour and regulatory reporting obligations under operational resilience requirements.*

### 4c: Score Each Risk

For every identified risk, assign:
- **Inherent probability** (1–5) — likelihood assuming no controls in place
- **Inherent impact** (1–5) — consequence assuming no controls in place
- **Inherent risk rating** — Probability × Impact
- **Existing controls** — document what mitigations already exist
- **Residual probability** (1–5) — likelihood after existing controls
- **Residual impact** (1–5) — consequence after existing controls
- **Residual risk rating** — the score that drives prioritisation and action

## Step 5: Define Mitigation Strategies

For every risk rated **Medium or above**, define a response strategy using the **4T framework**:

| Strategy | When to Apply | Requirements |
|---|---|---|
| **Terminate** (Avoid) | Risk is unacceptable and can be eliminated by changing scope, approach, or design | Document the change and confirm risk is fully removed |
| **Transfer** | Risk is better managed by a third party (insurance, contractual transfer, outsourcing) | Define transfer mechanism, residual exposure, and counterparty risk |
| **Treat** (Mitigate) | Risk can be reduced to acceptable level through specific actions | Define actions, owners, deadlines, cost, and target residual score |
| **Tolerate** (Accept) | Risk is within appetite after analysis, or cost of mitigation exceeds benefit | Document rationale, define monitoring triggers, and escalation criteria |

For each **Treat** action, specify:
- **Action description** — specific, measurable mitigation step
- **Risk owner** — the individual accountable (by role if name unavailable)
- **Action owner** — the individual responsible for executing the mitigation
- **Target completion date**
- **Cost / resource requirement**
- **Target residual risk score** after implementation
- **Review cadence** — how often this mitigation is reassessed

## Step 6: Deliver Output

Produce the following structured deliverables:

### Deliverable 1: Risk Register (Tabular Format)

A complete register table with the following columns per risk entry:

| Field | Content |
|---|---|
| Risk ID | Sequential identifier (e.g., R-001) |
| Risk Category | From taxonomy |
| Risk Title | Concise label |
| Risk Description | Cause–event–consequence statement |
| Risk Owner | Named individual or role |
| Inherent Probability | 1–5 |
| Inherent Impact | 1–5 |
| Inherent Rating | Score + label (e.g., 20 — Critical) |
| Existing Controls | Current mitigations in place |
| Residual Probability | 1–5 |
| Residual Impact | 1–5 |
| Residual Rating | Score + label |
| Response Strategy | Terminate / Transfer / Treat / Tolerate |
| Mitigation Actions | Specific actions with owners and dates |
| Target Residual Rating | Expected score post-mitigation |
| Status | Open / In Progress / Closed / Escalated |
| Last Reviewed | Date |

### Deliverable 2: Risk Heat Map

A visual 5×5 probability-impact matrix showing the distribution of all residual risks, colour-coded by rating band (Critical / High / Medium / Low), with Risk IDs plotted in each cell.

### Deliverable 3: Executive Risk Summary

A one-page narrative suitable for steering committee or board consumption:
- **Total risk count** by rating band
- **Top 5 risks** by residual rating — with plain-language descriptions and recommended actions
- **Emerging risks** — risks not yet scored but flagged for investigation
- **Risk trend** — comparison to prior assessment if FutureProof context includes previous sessions
- **Key decisions required** — specific decisions the audience must make (resource allocation, scope changes, escalations)
- **Recommended review cadence** — when the register should next be reassessed

### Deliverable 4: Risk Governance Recommendations

Provide tailored guidance on:
- **Escalation protocol** — which risk ratings trigger escalation, to whom, and within what timeframe
- **Review rhythm** — suggested cadence for register review (e.g., fortnightly for Critical/High, monthly for Medium, quarterly for Low)
- **Integration points** — how the register connects to existing governance structures (change control, incident management, audit, programme board)

## Step 7: Propose Experiments

```
FutureProof:save_experiment(skill="risk-register-builder", experiment={
  hypothesis: "Incorporating pre-mortem workshops with cross-functional stakeholders before register creation increases the number of high-impact risks identified by 30% compared to desk-based analysis alone",
  variants: ["control: risk identification via document review and single-analyst assessment", "variant: facilitated pre-mortem session with 4+ stakeholder roles followed by structured register build"],
  measurement: "Count of risks rated High or Critical identified at initial assessment vs. risks that materialised within 6 months that were not in the original register",
  expected_impact: "30% reduction in unidentified risks that later materialise as issues"
})
```

## Step 8: Request Research

```
FutureProof:request_research(skill="risk-register-builder",
  query="Emerging enterprise risk management frameworks, AI-driven risk identification methodologies, and sector-specific risk benchmarking data 2024–2025, including ISO 31000:2018 implementation patterns and COSO ERM integration with agile delivery models",
  reason="Ensure risk taxonomy, scoring approaches, and mitigation frameworks reflect current best practice and evolving regulatory expectations across industries"
)
```

## Step 9: Save Session

```
FutureProof:save_session(skill="risk-register-builder", session={
  summary: "Built risk register for [initiative/programme name] covering [scope description] with [N] risks identified across [categories used]",
  key_findings: ["[Top risk and its residual rating]", "[Most significant gap in existing controls]", "[Key governance recommendation]"],
  risk_profile: {
    total_risks: N,
    critical: N,
    high: N,
    medium: N,
    low: N,
    unmitigated_critical: N
  },
  frameworks_applied: ["taxonomy used", "scoring matrix version", "compliance frameworks referenced"],
  user_feedback: null
})
```