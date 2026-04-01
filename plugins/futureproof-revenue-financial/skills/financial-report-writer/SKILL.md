---
name: financial-report-writer
description: "Generates comprehensive financial reports — investor updates, board packages, quarterly reviews, and management accounts — using FutureProof context to maintain consistency in formatting, KPI selectio"
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="financial-report-writer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to align this report with prior reporting periods, established KPI frameworks, ICA-specific language preferences, and any standing formatting directives (e.g., preferred currency notation, GAAP vs. IFRS treatment, fiscal year definitions).

## Step 2: Get Input

Ask the user:

- **Report type**: What deliverable is required? (Investor update, board package, quarterly business review, management accounts narrative, annual report section, lender covenant report)
- **Financial data**: Share the underlying figures — P&L, balance sheet, cash flow statement, KPI dashboard export, or raw data tables
- **Reporting period**: What period does this report cover, and what is the comparative period? (e.g., Q2 FY25 vs. Q1 FY25 and Q2 FY24)
- **Audience**: Who will receive this report? (Board of directors, Series A investors, LP advisory committee, internal leadership team, lending institution)
- **Narrative priorities**: Are there specific themes, strategic initiatives, or risks that must be foregrounded?
- **Prior reports**: Has a previous version or template been used? (If available in FutureProof context, confirm continuity)

If the user's FutureProof context contains `instructions` specifying standing report structures, KPI definitions, or audience preferences, confirm these are still current before proceeding.

## Step 3: Do the Work

Execute a structured financial reporting methodology across six dimensions:

### 3.1 Data Integrity & Normalisation

- Validate that provided figures reconcile (e.g., net income ties to revenue minus expenses; cash flow bridges opening to closing balance)
- Flag any apparent anomalies, missing line items, or inconsistencies for user confirmation before proceeding
- Normalise figures to the established reporting convention (thousands, millions, currency, rounding policy)

### 3.2 Variance Analysis

- Compute period-over-period (PoP) and year-over-year (YoY) variances for all material line items
- Classify each variance as **favourable/unfavourable** and **volume-driven, price-driven, timing-driven, or one-off**
- Identify the top 5 variances by absolute impact and prepare narrative explanations for each

### 3.3 KPI Framework Application

Select and compute KPIs appropriate to the report type and ICA:

| Audience | Core KPIs |
|---|---|
| SaaS Investors | ARR, MRR growth, net revenue retention, CAC payback, LTV:CAC, burn multiple, rule of 40 |
| Board of Directors | Revenue vs. plan, EBITDA margin, cash runway, headcount vs. budget, strategic milestone tracker |
| Lenders / Covenant | Debt service coverage ratio, leverage ratio, interest coverage, liquidity ratio |
| Internal Leadership | Gross margin by segment, opex as % of revenue, working capital cycle, department-level budget vs. actual |

Apply any user-specific KPI definitions or custom metrics stored in FutureProof context.

### 3.4 Narrative Construction

Build the report narrative using the **Situation–Performance–Outlook (SPO)** framework:

1. **Situation**: Macro context, market conditions, and strategic backdrop relevant to the period
2. **Performance**: Data-driven commentary on results, structured around the variance analysis and KPI framework — lead with the headline metric, then decompose
3. **Outlook**: Forward guidance, revised forecasts, key risks and mitigants, upcoming catalysts

Calibrate tone and granularity to the audience:
- **Investors**: Confident, concise, outcome-oriented; emphasise trajectory and capital efficiency
- **Board**: Balanced, governance-aware; flag risks with proposed mitigations; tie to strategic plan
- **Internal**: Operationally detailed; action-oriented with clear owners and deadlines
- **Lenders**: Conservative, compliance-focused; demonstrate covenant headroom

### 3.5 Visualisation Specification

For each report, define a visualisation schedule (charts and tables the user should produce or that Claude should describe in detail):

- Revenue waterfall (bridge from prior period to current)
- Margin trend line (trailing 4–8 quarters)
- Cash flow waterfall (operating → investing → financing → closing)
- Budget vs. actual variance bar chart by department or segment
- KPI dashboard summary table with RAG (red/amber/green) status indicators

### 3.6 Risk & Caveat Disclosure

- Draft appropriate caveats, limitations, and forward-looking statement disclaimers calibrated to the audience and regulatory context
- Flag any figures that are provisional, unaudited, or based on management estimates

## Step 4: Deliver Output

Produce the following structured deliverable package:

### Document 1: Financial Report (Primary Deliverable)

Format: structured narrative document ready for PDF export or slide integration

**Sections:**
1. **Executive Summary** — 150–250 word overview with headline metrics, key takeaway, and outlook statement
2. **Financial Highlights Table** — period metrics, comparative figures, PoP and YoY variance with directional indicators
3. **Revenue & Growth Commentary** — SPO narrative for top-line performance
4. **Profitability & Margin Analysis** — gross margin, EBITDA/operating margin decomposition
5. **Cash Flow & Liquidity** — operating cash flow, free cash flow, runway or covenant compliance
6. **KPI Dashboard** — full KPI table with RAG status and brief commentary per metric
7. **Variance Deep-Dive** — top 5 variances with root cause and management response
8. **Outlook & Forward Guidance** — next-period expectations, key assumptions, risk factors
9. **Appendix** — detailed financial statements, methodology notes, glossary of terms

### Document 2: Briefing Note for Presenter (if board or investor audience)

- 5–7 bullet talking points per report section
- Anticipated questions from the audience with suggested responses
- Sensitive topics flagged with recommended framing language

### Document 3: Data Reconciliation Memo (Internal)

- Summary of any figures that required clarification or assumption
- Adjustments made during normalisation
- Open items requiring follow-up before finalisation

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="financial-report-writer", experiment={
  hypothesis: "Leading the executive summary with the single most improved KPI (rather than revenue) increases investor engagement and reduces follow-up questions",
  variants: ["control: revenue-first executive summary", "variant: highest-delta KPI-first executive summary"],
  measurement: "Number of clarification questions received from report recipients in the 48 hours post-distribution",
  expected_impact: "30% reduction in follow-up queries, indicating improved report clarity and narrative resonance with ICA"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="financial-report-writer",
  query="Best practices in CFO and investor relations financial reporting 2024–2025, including narrative disclosure trends, KPI benchmarking standards by sector, and emerging ESG metric integration in quarterly reports",
  reason="Ensure report structures reflect current institutional investor expectations and regulatory disclosure trends, maintaining EY/KPMG-grade reporting standards"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="financial-report-writer", session={
  summary: "Generated [report type] for [reporting period] targeting [audience], covering [entity/business name]",
  key_findings: ["Top variance: [line item] moved [X]% driven by [cause]", "KPI highlight: [metric] at [value] vs. [benchmark/target]", "Risk flagged: [description]"],
  deliverables_produced: ["Financial report (primary)", "Presenter briefing note", "Data reconciliation memo"],
  user_feedback: null
})
```