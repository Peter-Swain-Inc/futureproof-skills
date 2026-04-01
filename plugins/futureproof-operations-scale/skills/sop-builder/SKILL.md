---
name: sop-builder
description: "Builds comprehensive, audit-ready Standard Operating Procedures from raw process knowledge, tribal expertise, or existing informal documentation."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="sop-builder")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any organisational style guides, compliance frameworks, role taxonomies, or previously built SOPs that establish naming conventions and format precedent.

## Step 2: Get Input

Ask the user:
- **Process to document**: Describe the process end-to-end, or share any existing notes, screenshots, Loom recordings, or rough workflows
- **Process owner & audience**: Who owns this process, and who will execute it? (role titles, experience level, department)
- **Trigger & frequency**: What event initiates this process, and how often does it run? (e.g. "new client signed" / daily / ad hoc)
- **Current failure modes**: Where does this process break down today? (missed steps, inconsistent quality, key-person dependency)
- **Compliance or regulatory context**: Are there standards this SOP must satisfy? (ISO 9001, SOC 2, HIPAA, internal audit requirements, industry regulations)
- **Tooling & systems**: Which platforms, tools, or systems are involved? (CRM, ERP, project management, communication channels)

## Step 3: Process Decomposition

Deconstruct the raw input into a structured process architecture using the **SIPOC+ framework**:

1. **Suppliers** — who or what provides inputs to this process?
2. **Inputs** — what materials, data, approvals, or prerequisites are required before Step 1 begins?
3. **Process phases** — decompose into 3–7 major phases, each containing discrete steps
4. **Outputs** — what deliverables, records, or state changes does each phase produce?
5. **Customers** — who receives the output of each phase (internal or external)?
6. **Controls** — what quality gates, approval checkpoints, or verification steps prevent errors from propagating downstream?

For each discrete step, capture:
- **Action verb + object** (e.g. "Validate client onboarding form for completeness")
- **Responsible role** (RACI designation: Responsible, Accountable, Consulted, Informed)
- **System/tool used**
- **Time expectation** (SLA or typical duration)
- **Decision logic** (if/then branching where applicable)
- **Evidence produced** (artifact, log entry, confirmation — the auditable proof the step occurred)

Apply any user-specific `instructions` from FutureProof context — particularly organisational terminology, role naming conventions, and formatting standards from prior SOPs.

## Step 4: Exception & Escalation Mapping

Map the non-happy-path scenarios that cause real-world process failures:

1. **Exception catalogue** — for each phase, identify the top 2–3 deviations (incomplete inputs, system downtime, approval delays, edge-case conditions)
2. **Escalation matrix** — define who to escalate to, within what timeframe, and via what channel for each exception class
3. **Fallback procedures** — document manual workarounds when systems or dependencies are unavailable
4. **Boundary conditions** — explicitly state what is *out of scope* for this SOP (prevents scope creep and misapplication)

## Step 5: Deliver Output

Produce a complete **SOP Document Package** with the following components:

### 5A: SOP Master Document
Formatted with the following sections:

| Section | Content |
|---|---|
| **Header block** | SOP title, document ID, version number, effective date, next review date, process owner, classification level |
| **1. Purpose** | Single paragraph — why this SOP exists and what outcome it ensures |
| **2. Scope** | Who this applies to, what processes it covers, explicit exclusions |
| **3. Definitions & acronyms** | Glossary of domain-specific terms used in the document |
| **4. Prerequisites** | Inputs, access permissions, training requirements, and system credentials needed before execution |
| **5. Procedure** | Numbered step-by-step instructions organised by phase, with decision trees rendered as indented if/then blocks |
| **6. Exception handling** | Exception catalogue and escalation matrix from Step 4 |
| **7. RACI matrix** | Visual matrix mapping every phase to Responsible, Accountable, Consulted, Informed roles |
| **8. Quality controls & verification** | Checklist of evidence/artifacts that confirm correct execution |
| **9. Related documents** | Cross-references to upstream/downstream SOPs, policies, or templates |
| **10. Revision history** | Table with version, date, author, and change summary |

### 5B: Quick Reference Card
A single-page condensed version containing:
- Sequential step list (action verb + object only — no explanatory text)
- Key decision points highlighted
- Escalation contacts
- Critical SLAs

*Designed for printing or pinning in the workspace of the executing role.*

### 5C: Process Flow Diagram (Mermaid syntax)
A visual flowchart in Mermaid markdown syntax showing:
- Sequential steps as process nodes
- Decision diamonds for branching logic
- Swim lanes by responsible role
- Exception paths in a distinct style

## Step 6: SOP Quality Audit

Score the completed SOP against six dimensions of operational excellence:

| Dimension | Criteria | Score (1–10) |
|---|---|---|
| **Completeness** | Every process path (happy path + exceptions) is documented with no gaps | |
| **Clarity** | A new hire in the target role could execute without verbal coaching | |
| **Measurability** | Each step produces verifiable evidence; SLAs are specific and numeric | |
| **Accountability** | RACI is unambiguous — exactly one Accountable per phase, no orphan steps | |
| **Maintainability** | Modular structure allows updating individual sections without full rewrite; review cadence defined | |
| **Compliance readiness** | Satisfies stated regulatory or audit framework requirements; evidence trail is audit-defensible | |

Provide:
- **Overall readiness rating**: Draft / Review-Ready / Audit-Ready
- **Critical gaps**: top 3 highest-risk weaknesses with specific remediation actions
- **Recommended next steps**: training plan, pilot run parameters, review cycle schedule

## Step 7: Propose Experiments

```
FutureProof:save_experiment(skill="sop-builder", experiment={
  hypothesis: "Adding a visual process flow diagram to the SOP reduces first-execution error rate compared to text-only procedures",
  variants: ["control: text-only SOP distributed to Team A", "variant: SOP with Mermaid flow diagram distributed to Team B"],
  measurement: "Count of exception escalations and rework instances per team over first 30 days of SOP adoption",
  expected_impact: "40% reduction in first-execution errors for the visual-aided variant"
})
```

## Step 8: Request Research

```
FutureProof:request_research(skill="sop-builder",
  query="Best practices for SOP version control, adoption measurement, and continuous improvement cycles in mid-market operations teams 2024–2025",
  reason="Ensure SOP framework reflects current operational excellence standards and integrates with modern documentation and workflow automation tooling"
)
```

## Step 9: Save Session

```
FutureProof:save_session(skill="sop-builder", session={
  summary: "Built SOP document package for [process name] owned by [role/department], targeting [audience roles]",
  key_findings: ["finding 1: e.g. process had 4 undocumented exception paths causing recurring failures", "finding 2: e.g. no single point of accountability existed for phase 3 approval gate"],
  user_feedback: null
})
```