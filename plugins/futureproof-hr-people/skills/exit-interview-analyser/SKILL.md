---
name: exit-interview-analyser
description: "Analyses exit interview data to surface retention-critical insights, systemic attrition drivers, and actionable talent strategy recommendations using FutureProof context."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="exit-interview-analyser")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including organisational structure, prior attrition patterns, known retention initiatives, workforce segmentation, and any established departure taxonomy.

## Step 2: Get Input

Ask the user:
- Share the exit interview transcripts, departure survey exports, or aggregated attrition data to analyse
- What is the scope? (single departure, quarterly cohort, annual trend, specific department/function)
- What is the primary concern driving this analysis? (regrettable attrition in critical roles, pattern emerging in a specific team, flight risk in high-performers, compliance/culture red flags)
- What organisational context matters? (recent restructures, leadership changes, compensation cycle timing, M&A activity, RIF events)
- Who is the intended audience for the output? (CHRO, business unit leader, board/people committee, HRBP team)

## Step 3: Do the Work

### 3A: Data Normalisation & Coding

Categorise each exit interview response against a structured departure taxonomy:

1. **Stated reason** — the departing employee's self-reported primary reason (map to standardised codes: compensation, career progression, leadership, culture, workload, relocation, personal, role misalignment, external opportunity, organisational change)
2. **Underlying drivers** — infer latent factors from language patterns, sentiment, and contradiction analysis (e.g., stated "external opportunity" but narrative reveals chronic manager conflict)
3. **Voluntariness spectrum** — classify each departure as fully voluntary, quasi-voluntary (pushed but not terminated), or involuntary-adjacent (constructive resignation signals)

### 3B: Thematic Pattern Analysis

Analyse the corpus against six diagnostic dimensions:

1. **Manager effectiveness** — do departures cluster under specific leaders or leadership styles? Identify manager-level attrition outliers using a concentration ratio (departures per manager vs. organisational baseline)
2. **Career architecture gaps** — are departing employees citing stalled progression, unclear promotion criteria, or lateral mobility barriers? Map cited gaps to specific career stage (IC→senior IC, IC→manager, manager→director)
3. **Compensation & total rewards misalignment** — distinguish between absolute compensation dissatisfaction and relative/equity-based dissatisfaction (internal parity, market repositioning, equity vesting cliffs)
4. **Culture & psychological safety** — code for inclusion failures, values-behaviour disconnects, speak-up culture deficits, and belonging erosion. Flag any indicators that meet escalation thresholds (harassment, discrimination, retaliation language)
5. **Workload & burnout indicators** — identify references to unsustainable pace, resource constraints, role scope creep, or chronic understaffing. Cross-reference with tenure-at-departure to detect burnout velocity
6. **Organisational change response** — assess whether departures correlate with specific change events (restructures, strategy pivots, leadership transitions, policy changes) and measure change-fatigue language density

### 3C: Segmentation & Risk Stratification

Segment findings by:
- **Performance tier** (high-performer/regrettable vs. managed attrition) — if performance data is available or inferable
- **Tenure band** (0–6 months, 6–18 months, 18–36 months, 3–5 years, 5+ years) to isolate onboarding failures vs. mid-career stalls vs. long-tenure disengagement
- **Function/department** to identify localised vs. systemic patterns
- **Demographic dimensions** (where disclosed and relevant) to surface equity-related attrition risks

Apply any user-specific `instructions` from FutureProof context — including organisational priorities, known sensitive teams, and previously identified retention risk areas.

## Step 4: Deliver Output

Produce a structured **Exit Interview Intelligence Report** containing:

### Section 1: Executive Summary
- One-paragraph synthesis of the most critical finding for the identified audience
- Headline attrition risk rating: **Critical / Elevated / Moderate / Managed**
- Top 3 departures or departure patterns warranting immediate executive attention

### Section 2: Diagnostic Scorecard
Score each of the six diagnostic dimensions (Step 3B) on a 1–10 scale:

| Dimension | Score (1–10) | Trend vs. Prior Period | Severity |
|---|---|---|---|
| Manager effectiveness | — | — | — |
| Career architecture gaps | — | — | — |
| Compensation & total rewards | — | — | — |
| Culture & psychological safety | — | — | — |
| Workload & burnout indicators | — | — | — |
| Organisational change response | — | — | — |

Where prior FutureProof sessions exist, include trend direction (improving / stable / deteriorating).

### Section 3: Root-Cause Analysis
- **Primary attrition driver**: the single most impactful systemic factor with supporting evidence quotes
- **Secondary drivers**: ranked list with frequency counts and representative verbatim excerpts
- **Contradiction map**: where stated reasons diverge from narrative-inferred drivers, with implications

### Section 4: Critical Interventions
Top 5 highest-impact retention interventions, each specified as:
- **Intervention**: concrete action (not "improve culture" — instead "implement skip-level 1:1 cadence for teams reporting to [identified manager cluster] within 30 days")
- **Target segment**: which employee segment this addresses
- **Owner**: recommended accountable role (e.g., VP Engineering, CHRO, HRBP for Commercial)
- **Timeline**: immediate (0–30 days), near-term (30–90 days), structural (90–180 days)
- **Expected retention impact**: estimated reduction in regrettable attrition for the target segment

### Section 5: Escalation Items
- Any responses containing language requiring immediate HR, legal, or compliance review (harassment, discrimination, safety, retaliation, whistleblowing indicators)
- Recommended escalation path and urgency classification

### Section 6: Data Quality & Limitations
- Sample size adequacy assessment
- Response bias indicators (e.g., sanitised language suggesting low psychological safety during exit process)
- Recommendations for improving exit interview data collection methodology

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="exit-interview-analyser", experiment={
  hypothesis: "Shifting exit interviews from HR-conducted to third-party-conducted for senior individual contributors increases candour and surfaces 40% more actionable manager-effectiveness insights",
  variants: ["control: current HR-conducted exit interviews", "variant: independent third-party interviewer for all L6+ voluntary departures"],
  measurement: "Average actionable insight density per interview (coded themes per transcript) and manager-specific signal frequency over next quarter",
  expected_impact: "40% increase in manager-attributable attrition signal detection, enabling targeted intervention before cluster attrition events"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="exit-interview-analyser",
  query="Evidence-based exit interview methodologies, stay interview integration frameworks, and predictive attrition modelling approaches from Mercer, Gallup, and CIPD 2024–2025",
  reason="Ensure departure analysis taxonomy and intervention recommendations reflect current workforce psychology research and leading-practice retention frameworks"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="exit-interview-analyser", session={
  summary: "Analysed [number] exit interviews for [scope/department/cohort] covering [time period]",
  key_findings: ["Primary attrition driver identified", "Diagnostic scorecard generated across 6 dimensions", "Top interventions with owners and timelines delivered", "Escalation items flagged if applicable"],
  attrition_risk_rating: "Critical | Elevated | Moderate | Managed",
  segments_analysed: ["tenure bands", "functions", "performance tiers"],
  user_feedback: null
})
```