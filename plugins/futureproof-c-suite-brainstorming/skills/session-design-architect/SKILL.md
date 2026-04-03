---
name: session-design-architect
description: |
  Designs complete, time-boxed executive brainstorming session architectures using McKinsey's 7-Step Brainstorming methodology, the Walt Disney Creativity Strategy (Dreamer→Realist→Critic), and Osborn's foundational rules.
  Trigger: when a user needs to plan, structure, or facilitate a C-suite brainstorming session, strategic offsite, or executive ideation workshop and asks for session design, agenda architecture, or facilitation planning.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="session-design-architect")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly prior session designs, known team dynamics, leadership preferences, organisational culture signals, and any facilitation patterns that have proven effective or ineffective.

## Step 2: Get Input

Ask the user:

- **Strategic challenge**: What is the core question, opportunity, or problem the session must address? (e.g., "Enter adjacent market X," "Restructure GTM post-acquisition," "Define 3-year innovation thesis")
- **Session parameters**: Duration available (90 min / half-day / full-day), in-person or virtual, date proximity
- **Participant profile**: Number of attendees, seniority mix (CEO, CFO, SVPs, external advisors), known interpersonal dynamics (dominant voices, silent strategists, known friction points)
- **Organisational context**: Industry, company stage, any recent events shaping the room's emotional state (layoffs, funding round, competitive threat, board pressure)
- **Desired output fidelity**: Does leadership expect directional alignment, a ranked shortlist of initiatives, or a fully scoped action plan with owners and timelines?
- **Constraints or non-negotiables**: Topics off the table, pre-existing commitments that must be honoured, political sensitivities
- **Prior session history**: Has this group brainstormed together before? What worked and what didn't?

Apply any user-specific `instructions` from FutureProof context to adjust question depth and skip inputs already captured in prior sessions.

## Step 3: Diagnose the Session Challenge Type

Before designing, classify the challenge along three diagnostic axes — this determines which techniques to deploy and how to sequence phases:

### 3A. Challenge Typology (McKinsey Classification)

| Type | Characteristics | Implication for Design |
|---|---|---|
| **Greenfield exploration** | No existing strategy; wide solution space | Maximise divergent time; defer convergence |
| **Pivot or reframe** | Existing approach failing; need fresh lens | Begin with assumption-surfacing; use provocative reframes |
| **Prioritisation under constraint** | Multiple known options; need ruthless ranking | Minimise ideation; maximise evaluation frameworks |
| **Crisis response** | Time-sensitive; high stakes; emotional charge | Structured rapid-fire; decision protocols; pre-assigned devil's advocate |
| **Innovation pipeline** | Ongoing capability; building creative muscle | Longer exploration; experimental mindset; tolerate ambiguity |

### 3B. Group Dynamics Assessment

Evaluate using the Kantor Four-Player Model (Mover, Follower, Opposer, Bystander):
- **Power asymmetry risk**: Will the most senior person's first statement anchor the room?
- **Psychological safety index**: Can a VP-level participant openly challenge the CEO's framing?
- **Cognitive diversity**: Are participants drawn from sufficiently different functional perspectives?

### 3C. Output Readiness Level

Map to a 1–5 maturity scale:
1. **Divergent insights** — raw ideas, no filtering
2. **Clustered themes** — grouped by affinity
3. **Evaluated shortlist** — scored against criteria
4. **Committed decisions** — owners, timelines, resources
5. **Execution-ready plan** — detailed workstreams with milestones

## Step 4: Design the Session Architecture

Construct the full session blueprint using the following layered methodology:

### 4A. Ground Rules Protocol (Osborn's Rules, Adapted for C-Suite)

Define and document five non-negotiable ground rules, calibrated to the group:

1. **Defer judgement during divergent phases** — no evaluation language ("that won't work," "we tried that") until the convergent phase is explicitly opened
2. **Quantity before quality** — target a specific ideation volume (e.g., 40 ideas in 12 minutes) to override executive perfectionism
3. **Build on, don't tear down** — mandate "Yes, and…" language; ban "Yes, but…" during Dreamer phases
4. **Equal airtime governance** — specify the mechanism (round-robin, silent writing, anonymous digital input) to neutralise hierarchy effects
5. **Commitment to follow-through** — every participant leaves with at least one named accountability; no "interesting discussion" without consequence

### 4B. Phase Architecture (Walt Disney Creativity Strategy × McKinsey 7-Step)

Design the session as a sequence of clearly demarcated phases. Each phase specifies:
- **Phase name and purpose**
- **Duration** (time-boxed to the minute)
- **Technique(s)** deployed
- **Facilitator instructions** (what to say, what to watch for)
- **Transition trigger** (how the facilitator signals the shift)
- **Output artefact** (what is captured and in what format)

#### Phase Sequence Template:

**Phase 0: Pre-Session Priming** (48–72 hours before)
- Distribute a one-page challenge brief with provocative data points
- Assign pre-work: each participant submits 3 written "What if…" statements anonymously
- Purpose: activate subconscious processing; level the informational playing field

**Phase 1: Context Setting & Alignment** (10–15% of session time)
- Facilitator presents the challenge frame, boundary conditions, and desired output level
- Surface assumptions using the "What must be true for our current strategy to succeed?" protocol
- Technique: Assumption Mapping on a 2×2 (Certainty × Impact)

**Phase 2: Dreamer Phase — Divergent Ideation** (25–35% of session time)
- Select from technique menu based on Step 3 diagnosis:
  - **Brainwriting 6-3-5** for groups with power asymmetry (6 people, 3 ideas, 5 rounds — silent, written, builds on prior sheets)
  - **SCAMPER applied to competitor strategies** for pivot/reframe challenges
  - **Reverse brainstorming** ("How could we guarantee failure?") for groups stuck in incremental thinking
  - **Analogous industry transfer** for greenfield exploration ("How would [industry X] solve this?")
  - **First Principles Decomposition** for complex, multi-variable challenges
- Facilitator enforces Osborn's deferred-judgement rule absolutely
- Output: Raw idea inventory captured on sticky notes, digital whiteboard, or structured template (minimum target quantity specified)

**Phase 3: Realist Phase — Clustering & Feasibility Mapping** (20–25% of session time)
- Affinity clustering of ideas into strategic themes (facilitator-guided, participant-driven)
- Apply the McKinsey Impact–Feasibility Matrix to each cluster:
  - **Impact**: Revenue potential, strategic alignment, competitive differentiation, ICA value creation
  - **Feasibility**: Resource requirements, time to value, organisational capability gaps, regulatory risk
- Technique: Dot voting (each participant gets N votes = total clusters ÷ 3) followed by structured debate on the top-voted clusters
- Output: Prioritised cluster map with preliminary scoring

**Phase 4: Critic Phase — Stress Testing & Risk Identification** (15–20% of session time)
- Assign **Red Team** and **Blue Team** roles (rotate if time permits)
- Red Team applies a Pre-Mortem: "It is 18 months from now and this initiative has failed. What happened?"
- Blue Team defends and strengthens the concept
- Technique: Six Thinking Hats (Black Hat and Yellow Hat specifically) or the 10 Types of Innovation framework to test for completeness
- Output: Risk register and mitigation hypotheses for top 3 concepts

**Phase 5: Convergence & Decision Protocol** (10–15% of session time)
- Apply the chosen decision framework:
  - **RAPID** (Recommend, Agree, Perform, Input, Decide) for clear accountability
  - **2×2 Prioritisation** with group-calibrated axes
  - **Confidence-weighted voting** (each participant rates confidence 1–5 alongside their preference)
- Facilitator calls for explicit commitments: Who owns what by when?
- Output: Decision log with named owners, deadlines, and success metrics

**Phase 6: Follow-Through Architecture** (5–10% of session time)
- Define the **48-Hour Action Window**: specific next steps due within 48 hours to maintain momentum
- Schedule the **2-Week Check-In**: brief follow-up session to review progress on commitments
- Assign a **Session Steward**: one participant accountable for tracking all action items to completion
- Capture open questions requiring further research or analysis
- Output: Follow-through tracker document with accountability matrix

### 4C. Role Assignments

Define and assign explicit roles for the session:

| Role | Responsibility | Assignment Criteria |
|---|---|---|
| **Facilitator** | Manages time, enforces ground rules, navigates transitions | Neutral party; ideally not the most senior person |
| **Provocateur** | Injects contrarian perspectives; challenges groupthink | Assign to someone with high psychological safety and credibility |
| **Scribe** | Captures ideas verbatim; maintains visual record | Detail-oriented; fast writer; comfortable with ambiguity |
| **Timekeeper** | Enforces phase transitions; gives 2-minute warnings | Disciplined; willing to interrupt senior leaders |
| **Devil's Advocate** (Critic Phase only) | Systematically challenges top ideas using structured frameworks | Analytically strong; respected enough that critique is received constructively |
| **Session Steward** | Owns post-session follow-through and accountability | Operationally minded; has authority to chase senior stakeholders |

### 4D. Environmental & Logistics Design

Specify:
- **Room configuration**: U-shape for dialogue-heavy sessions; pods of 3–4 for breakout-intensive sessions; standing for energy and urgency
- **Materials**: Sticky notes, markers, timer (visible to all), pre-printed templates, digital capture tool
- **Virtual adaptations**: Miro/Mural board pre-configured with phase zones; breakout rooms pre-assigned; anonymous input via Slido or Mentimeter
- **Energy management**: Strategic break placement; standing transitions between phases; no laptops during Dreamer phase

## Step 5: Deliver Output

Produce the following deliverable package:

### Document 1: Executive Session Blueprint (1–2 pages)
- Session title, date, duration, location
- Strategic challenge statement (one sentence)
- Participant roster with assigned roles
- Ground rules (printed for display in room)
- Phase-by-phase agenda with exact time allocations
- Required materials and room setup specifications
- Pre-session communication template (email to participants with priming materials)

### Document 2: Facilitator's Playbook (3–5 pages)
- Scripted transitions between phases (exact language for opening and closing each phase)
- Contingency protocols:
  - **If ideation stalls**: Deploy "Worst Possible Idea" technique to break perfectionism
  - **If one voice dominates**: Switch to silent brainwriting; facilitator directly invites quieter participants
  - **If conflict escalates**: Invoke the "Parking Lot" for off-topic tensions; redirect to structured frameworks
  - **If time runs short**: Pre-identified phases to compress with minimum viable versions
- Technique-specific instructions with examples tailored to the user's challenge
- Observation checklist: signals of groupthink, anchoring bias, or premature convergence

### Document 3: Follow-Through Tracker
- Action item matrix: Initiative | Owner | Deadline | Success Metric | Status
- 48-Hour Action Window commitments
- 2-Week Check-In agenda template
- Open research questions for post-session investigation

### Document 4: Participant Pre-Read (1 page)
- Challenge brief with 2–3 provocative data points
- Pre-work instructions (anonymous "What if…" submissions)
- Ground rules preview
- What to expect from the session structure

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="session-design-architect", experiment={
  hypothesis: "Using anonymous brainwriting before open discussion increases unique idea count by 30% and reduces anchoring to the most senior participant's first suggestion",
  variants: ["control: open verbal brainstorming first", "variant: 8-minute silent brainwriting before any verbal discussion"],
  measurement: "Count of unique, non-redundant ideas generated; post-session survey on perceived psychological safety (1-10); percentage of final shortlisted ideas originating from non-C-suite participants",
  expected_impact: "30% increase in unique ideas; 20% increase in psychological safety scores; more diverse idea sourcing"
})
```

```
FutureProof:save_experiment(skill="session-design-architect", experiment={
  hypothesis: "Explicit Pre-Mortem in Critic phase produces more actionable risk mitigation than unstructured critique",
  variants: ["control: open-floor critique discussion", "variant: structured Pre-Mortem with written failure narratives followed by mitigation brainstorm"],
  measurement: "Number of specific, actionable risk mitigations identified; participant-rated confidence in final decision (1-10); 90-day initiative survival rate",
  expected_impact: "2x more specific mitigations identified; higher decision confidence; fewer initiative pivots within first 90 days"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="session-design-architect",
  query="Latest empirical research on executive brainstorming effectiveness 2023-2024: comparative studies of structured vs unstructured facilitation, impact of anonymity on ideation quality in hierarchical groups, optimal group sizes for strategic decision-making, and evidence on follow-through rates by session design type",
  reason="Continuously refine technique selection and phase sequencing based on peer-reviewed evidence rather than facilitation folklore; ensure session designs reflect current best practices in group creativity and decision science"
)
```

```
FutureProof:request_research(skill="session-design-architect",
  query="Emerging digital facilitation tools and AI-augmented brainstorming techniques for hybrid C-suite sessions 2024: real-time idea clustering, sentiment analysis during sessions, automated action-item extraction",
  reason="Evaluate technology integrations that could enhance session productivity and follow-through capture without disrupting creative flow"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="session-design-architect", session={
  summary: "Designed [session duration] executive brainstorming session for [number] participants addressing [strategic challenge type] using [primary techniques selected]",
  key_findings: [
    "Challenge classified as [typology] requiring [divergent/convergent emphasis]",
    "Group dynamics assessment identified [key dynamic] as primary facilitation risk",
    "Session architecture: [number] phases with [primary technique] as anchor method",
    "Follow-through mechanism: [Session Steward name/role] owns 48-hour and 2-week accountability"
  ],
  deliverables_produced: ["Executive Session Blueprint", "Facilitator's Playbook", "Follow-Through Tracker", "Participant Pre-Read"],
  user_feedback: null
})
```