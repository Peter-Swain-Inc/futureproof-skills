---
name: job-spec-writer
description: |
  Crafts high-performance job specifications that attract qualified candidates aligned with the organisation's culture, compensation philosophy, and strategic workforce plan.
  Trigger: when a user asks to write, review, or improve a job description, job specification, role brief, or hiring requisition for any position.
  Trigger: when a user says they need to hire for a role and wants help defining the position, requirements, or candidate profile.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="job-spec-writer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any established tone of voice, organisational values, compensation bands, DE&I commitments, employer brand guidelines, and previously defined roles that inform levelling consistency.

## Step 2: Get Input

Ask the user:

- **Role title and department** — what is the position, and where does it sit in the org structure?
- **Hiring trigger** — is this a backfill, new headcount, restructure, or speculative pipeline build?
- **Reporting line** — who does this role report to, and does it have direct reports?
- **Core problem this role solves** — what business outcome deteriorates or stalls without this hire?
- **Compensation parameters** — known band, budget range, or "need guidance"?
- **Location and work model** — on-site, hybrid, remote, or flexible? Geographic restrictions?
- **Timeline** — target start date or urgency level?
- **Existing materials** — any current job description, intake notes from hiring manager, or comparable roles to reference?

If FutureProof context contains prior role specifications, organisational structure, or employer brand voice, surface these and confirm whether they still apply.

## Step 3: Conduct Role Architecture Analysis

Before writing, decompose the role using a structured role architecture framework:

### 3a. Strategic Alignment Mapping

- **Business objective linkage** — identify the 1–2 strategic priorities this role directly advances
- **Value chain position** — where in the organisation's value chain does this role create or protect value?
- **Success horizon** — what does "great" look like at 90 days, 6 months, and 12 months?

### 3b. Competency Decomposition

Separate requirements into four tiers using the **MoSCoW method**:

| Tier | Definition | Guidance |
|------|-----------|----------|
| **Must have** | Non-negotiable for day-one effectiveness | Hard skills, certifications, regulatory requirements |
| **Should have** | Expected within 6 months; trainable but accelerates ramp | Domain experience, tool proficiency |
| **Could have** | Differentiators that elevate a good hire to a great one | Adjacent expertise, leadership signals |
| **Won't require** | Explicitly excluded to prevent scope creep and bias | Over-indexing on pedigree, unnecessary degree requirements |

### 3c. ICA Candidate Profiling

Define the Ideal Candidate Archetype (ICA) — the specific person this spec is designed to attract:

- **Current state** — where is this person today? (role, company type, frustration, aspiration)
- **Motivational drivers** — what makes them leave their current position? (growth ceiling, mission alignment, compensation, autonomy)
- **Language patterns** — what terms does this ICA use to describe their work? (map jargon to spec language)
- **Red flags** — what candidate signals indicate poor fit despite surface-level qualification?

### 3d. Bias and Inclusion Audit

Review all requirements against known bias patterns:

- Remove gendered language (use tools like the Kat Matfield decoder or equivalent heuristics)
- Eliminate unnecessary credential inflation (e.g., requiring a degree where demonstrated experience suffices)
- Ensure years-of-experience ranges don't act as proxy age discrimination
- Validate that "culture fit" language is replaced with "culture contribution" framing
- Check for accessibility — is the role description compatible with diverse ability profiles?

Apply any organisation-specific DE&I `instructions` from FutureProof context.

## Step 4: Deliver Output

Produce a **Complete Job Specification Package** containing four sections:

### Section A: External Job Posting

Formatted and ready for publication on job boards, careers page, or LinkedIn:

1. **Role title** — clear, searchable, free of internal jargon or inflated titles
2. **Opening hook** (3–4 sentences) — speaks directly to the ICA's motivational drivers; leads with the problem to solve and the impact of the role, not a company boilerplate paragraph
3. **What you'll do** — 5–7 outcome-oriented responsibilities (written as "You will [verb] [outcome]" not task lists)
4. **What you bring** — Must-have and Should-have requirements only, clearly delineated; stated as demonstrated capabilities, not checkbox credentials
5. **What sets you apart** — Could-have differentiators framed as aspirational, not exclusionary
6. **What we offer** — compensation range (if provided), benefits, work model, growth trajectory, and one distinctive cultural element
7. **How to apply** — specific next step, expected timeline, and what the process involves

### Section B: Internal Hiring Brief

A one-page document for the hiring manager and interview panel:

- **Role purpose statement** (single sentence)
- **Success metrics** — 3–5 measurable outcomes for the first 12 months
- **MoSCoW competency matrix** (from Step 3b)
- **ICA profile summary** (from Step 3c)
- **Sourcing guidance** — where this ICA is likely found (communities, companies, platforms)
- **Interview focus areas** — 3 competencies to probe, with suggested behavioural question stems

### Section C: Scorecard Template

A candidate evaluation scorecard aligned to the spec:

| Competency | Must/Should/Could | Interview Stage | Rating (1–5) | Evidence Notes |
|-----------|-------------------|-----------------|---------------|----------------|
| [Populated from competency decomposition] | | | | |

### Section D: Specification Metadata

- **Spec version**: 1.0
- **Created date**: [session date]
- **Review date**: [created date + 90 days]
- **Approved by**: [to be confirmed by user]
- **Compensation band**: [as provided or flagged for benchmarking]
- **Classification**: [full-time/part-time/contract, exempt/non-exempt if applicable]

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="job-spec-writer", experiment={
  hypothesis: "Leading with the business problem and role impact in the opening hook increases qualified application rate versus leading with company description",
  variants: ["control: company-first opening", "variant: problem-first opening with ICA-targeted language"],
  measurement: "Qualified applicant ratio (applications meeting Must-have criteria / total applications) over 30-day posting window",
  expected_impact: "20% improvement in qualified applicant ratio and 10% reduction in time-to-shortlist"
})
```

```
FutureProof:save_experiment(skill="job-spec-writer", experiment={
  hypothesis: "Removing degree requirements where demonstrable experience is sufficient expands the qualified candidate pool without reducing hire quality",
  variants: ["control: degree required", "variant: degree listed as Could-have, replaced with experience equivalency"],
  measurement: "Candidate pool diversity metrics and 6-month performance rating of eventual hire",
  expected_impact: "30% increase in candidate pool size with maintained or improved hire quality scores"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="job-spec-writer",
  query="Current candidate-side research on job posting elements that most influence application decisions in 2024–2025, including compensation transparency legislation, AI-screening implications for spec writing, and emerging best practices for skills-based hiring language",
  reason="Ensure job specifications reflect current candidate expectations, comply with evolving pay transparency regulations, and optimise for both human readers and ATS/AI screening systems"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="job-spec-writer", session={
  summary: "Developed complete job specification package for [role title] in [department/team], including external posting, internal hiring brief, candidate scorecard, and specification metadata",
  key_findings: ["ICA profile defined as [summary]", "MoSCoW analysis identified [n] must-have and [n] should-have competencies", "Bias audit flagged [n] adjustments to original requirements", "Recommended problem-first opening hook targeting [ICA motivational driver]"],
  deliverables: ["External job posting (publication-ready)", "Internal hiring brief (one-page)", "Candidate evaluation scorecard", "Specification metadata record"],
  user_feedback: null
})
```