# VOLUME II — RESEARCH & STRATEGY

*Mortgage Website Excellence Framework (MWEF) v1.0*

---

## Volume Introduction

Volume II covers the first three Stage Gates of every MWEF engagement: Discovery & Market Research, Competitive Intelligence, and Strategic Direction. Together these gates convert a signed Project Charter into an evidence-based strategic foundation that every subsequent Volume builds on. No architecture, design, or content decision in Volumes III–V should be traceable to anything other than a finding, decision, or objective established here.

### The Fixed Stage Gate Template

Every Stage Gate in this manual (Volumes II–V) follows the same 19-part structure. It is defined once here and applied without restatement in every subsequent gate:

1. **Purpose** — Why this gate exists
2. **Business Objectives** — What business outcome this gate serves
3. **Inputs** — What must exist before this gate can start
4. **Outputs** — What this gate produces
5. **Required Documents** — Specific Knowledge Base artifacts produced
6. **Responsible Roles** — Who does the work (Volume I Sec. 2)
7. **Required Specialists** — Who must be consulted or must sign off
8. **Decision Authority** — Who has final approval
9. **Workflow** — Step-by-step process
10. **Checklist** — Pass/fail completion checklist
11. **Prompt(s)** — Ready-to-use AI prompt templates for this gate
12. **Examples** — Illustrative sample output
13. **Common Mistakes** — Documented failure patterns
14. **Best Practices** — Documented success patterns
15. **Review Process** — How the deliverable is checked before sign-off
16. **Quality Assurance** — Which of the Eight Dimensions (Vol. I Sec. 12.2) apply and how
17. **Exit Criteria** — The pass/fail gate itself
18. **Knowledge Base / Blueprint / Decision Register Updates** — What must be written where
19. **Future Enhancements** — Where this gate's output will be revisited later in the engagement

---

# STAGE GATE 1 — DISCOVERY & MARKET RESEARCH

## 1. Purpose

Establish a factual, evidence-based understanding of the client lender's business, borrower audience, market footprint, and current digital position before any strategic or design decision is made.

## 2. Business Objectives

- Identify the client's actual (not assumed) target borrower segments and their decision drivers.
- Establish the client's licensed states, loan products, and any niche specialization (e.g., VA, jumbo, non-QM, first-time buyer programs).
- Baseline the client's current website's performance, traffic, and conversion behavior, if one exists.
- Surface compliance constraints early (state licensing disclosures, NMLS requirements, advertising restrictions).

## 3. Inputs

- Signed Project Charter
- Client intake questionnaire (Volume VI — Client Intake Templates)
- Access (read-only where possible) to client's current website, GA4/analytics, and Search Console, if available
- List of loan officers, branches, and licensed states from client

## 4. Outputs

- Discovery Report
- Borrower Persona Set (minimum 2, typically 3–5)
- Current-State Digital Audit (if a prior website exists)
- Compliance Constraint Log (seed version, expanded in later gates)

## 5. Required Documents

`/01-research/discovery-report-v1.md`, `/01-research/borrower-personas-v1.md`, `/01-research/current-state-audit-v1.md`, `/01-research/compliance-constraints-v1.md`

## 6. Responsible Roles

Research Consultant (lead), Engagement Lead (review), AI Orchestrator (supporting research synthesis)

## 7. Required Specialists

SEO Specialist (for current-state technical audit input), Compliance Liaison (to validate licensing/product list)

## 8. Decision Authority

Engagement Lead approves the Discovery Report as sufficient to proceed; no client sign-off is required at this gate, but the report is shared with the client for factual correction.

## 9. Workflow

```
[1] Client Intake Questionnaire returned
        │
        ▼
[2] Stakeholder interviews (loan officers, marketing lead, compliance contact)
        │
        ▼
[3] Current-state digital audit (if applicable): traffic, rankings, Core Web
    Vitals, conversion funnel review
        │
        ▼
[4] Borrower persona synthesis from interviews + audit + market data
        │
        ▼
[5] Compliance constraint pass: licensed states, product-specific disclosure
    requirements, advertising restrictions
        │
        ▼
[6] Discovery Report drafted (AI-assisted synthesis, human-reviewed)
        │
        ▼
[7] Internal review → Exit Criteria check → Stage Gate 2 scheduled
```

## 10. Checklist

- [ ] Minimum 3 stakeholder interviews completed (marketing lead, at least one loan officer, compliance contact)
- [ ] Current-state audit completed if a legacy site exists (traffic, rankings, CWV, conversion funnel)
- [ ] Borrower personas drafted with named decision drivers and objections, not generic demographics only
- [ ] Licensed states and products confirmed against NMLS record, not assumed from client marketing material
- [ ] Compliance Constraint Log seeded with at least: required disclosures, licensed-state list, advertising restrictions applicable to the client's channel mix
- [ ] Discovery Report reviewed by Engagement Lead

## 11. Prompt(s)

**Prompt 1.1 — Borrower Persona Synthesis**

```
You are the Research Consultant on a mortgage lending website engagement.
Using the attached stakeholder interview notes, current-state digital audit,
and client intake questionnaire, synthesize 3-5 borrower personas.

For each persona, provide:
- Name and one-line archetype (e.g., "First-Time Buyer, Credit-Anxious")
- Primary loan product interest
- Top 3 decision drivers (what makes them choose a lender)
- Top 3 objections/anxieties about the mortgage process
- Preferred information format (calculators, guides, direct contact, live chat)
- A representative search query this persona would type

Do not invent statistics. Where you infer rather than cite a source from the
provided materials, label the line "[inference]" explicitly. Ground every
persona in at least one specific quote or data point from the source material.
```

**Prompt 1.2 — Current-State Digital Audit Synthesis**

```
You are auditing the current website for [Client Name], a mortgage lender.
Given the attached GA4 export, Search Console export, and PageSpeed/Core Web
Vitals report, produce a Current-State Digital Audit covering:
1. Traffic overview (organic vs. paid vs. direct, trend over trailing 12 months)
2. Top 10 landing pages by organic sessions and their current keyword rankings
3. Core Web Vitals summary (LCP, INP, CLS) for mobile and desktop
4. Conversion funnel as currently instrumented (or note if not instrumented)
5. Three most significant technical or content gaps observed

Flag any metric you cannot verify from the provided exports rather than
estimating it.
```

## 12. Examples

*Sample persona excerpt:*

> **Persona: "Maria, First-Time Buyer, Credit-Anxious"** — Primary interest: FHA/first-time buyer programs. Decision drivers: perceived approval likelihood, clear step-by-step guidance, low down payment options. Objections: fear of rejection, confusion about required documents, distrust of "too good to be true" rate advertising. Preferred format: plain-language guides, a pre-qualification calculator with no hard credit pull, direct chat access to a loan officer. Representative query: "first time home buyer loans bad credit how much down payment."

## 13. Common Mistakes

- Building personas from marketing assumptions instead of actual stakeholder interviews and analytics.
- Skipping the current-state audit because "the client is starting a new site anyway" — historical performance data is often the best available signal of what borrower segments already convert.
- Treating the Compliance Constraint Log as a Stage Gate 8 concern instead of seeding it here, which causes late-stage rework.

## 14. Best Practices

- Interview at least one loan officer directly — marketing leads routinely misjudge what borrowers actually ask on the phone.
- Pull the client's actual licensed-state list from NMLS Consumer Access, not from the client's own website footer, which is frequently out of date.
- Where no current site exists (new lender, or full replatform with no analytics history), substitute a competitor-proxy audit using Stage Gate 2 data pulled forward.

## 15. Review Process

Engagement Lead reviews the Discovery Report against the Checklist (Section 10) and confirms every persona is traceable to source material before approving progression to Stage Gate 2.

## 16. Quality Assurance

Primary Eight-Dimension focus: **SEO** (current-state audit accuracy) and **Conversion** (persona objection accuracy). Compliance accuracy is verified against the Compliance Liaison's direct input, not inferred.

## 17. Exit Criteria

- [ ] Discovery Report approved by Engagement Lead
- [ ] Borrower personas finalized (minimum 2)
- [ ] Compliance Constraint Log seeded and reviewed by Compliance Liaison
- [ ] No open P0 backlog items blocking Stage Gate 2

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents (Section 5) saved as v1.0
- Blueprint: "Business Context" section populated with objectives and audience segments
- Decision Register: log any decision about persona prioritization (e.g., "Primary persona for homepage messaging: Maria") as `DEC-SG1-00x`

## 19. Future Enhancements

Personas are revisited and refined at Stage Gate 3 (Strategic Direction) and again informed by real behavioral data at Stage Gate 11.5 (Post-Launch Growth Program).

---

# STAGE GATE 2 — COMPETITIVE INTELLIGENCE

## 1. Purpose

Build a rigorous, evidence-based picture of how the client's direct competitors present themselves online, where they are strong or weak, and what white space exists for the client to win distinctly rather than imitate.

## 2. Business Objectives

- Identify 5–8 true competitors (direct lenders competing for the same borrower segments in the same markets), not generic "big bank" comparisons.
- Quantify competitor content, SEO, UX, and design strengths/weaknesses on a consistent rubric.
- Identify specific white-space opportunities the client can credibly own.

## 3. Inputs

- Discovery Report and Borrower Personas (Stage Gate 1)
- Client-nominated competitor list (from intake questionnaire)
- Access to SEO research tooling (rank tracking, backlink/topical data) where available

## 4. Outputs

- Competitive Intelligence Report
- Competitor Scoring Matrix
- White Space Opportunity Map

## 5. Required Documents

`/02-competitive/competitive-intelligence-report-v1.md`, `/02-competitive/competitor-scoring-matrix-v1.md`, `/02-competitive/white-space-map-v1.md`

## 6. Responsible Roles

Research Consultant (lead), SEO Specialist (rankings/topical data), Strategy Consultant (white space synthesis)

## 7. Required Specialists

None mandatory beyond Responsible Roles; Visual Designer may be consulted for early design-pattern observation feeding Stage Gate 7.

## 8. Decision Authority

Engagement Lead approves the report; competitor list itself should be confirmed with the client before deep analysis begins to avoid analyzing the wrong set.

## 9. Workflow

```
[1] Confirm competitor list (client-nominated + Research Consultant additions
    based on SERP presence for target keywords from personas)
        │
        ▼
[2] Score each competitor on the Competitor Scoring Matrix (Sec. 12) across
    Content, SEO, UX, Design, Trust Signals, Conversion Mechanics
        │
        ▼
[3] Identify recurring patterns (what everyone does — table stakes) vs.
    differentiators (what only 1-2 do well)
        │
        ▼
[4] Synthesize White Space Opportunity Map: gaps no competitor fills well
        │
        ▼
[5] Draft Competitive Intelligence Report
        │
        ▼
[6] Review → Exit Criteria → Stage Gate 3 scheduled
```

## 10. Checklist

- [ ] 5–8 true competitors identified and confirmed with client
- [ ] Every competitor scored on the full rubric, not a subset
- [ ] At least 3 white-space opportunities identified with supporting evidence
- [ ] Screenshots or captured references archived in Knowledge Base for each competitor (design/UX evidence, not just written description)

## 11. Prompt(s)

**Prompt 2.1 — Competitor Scoring**

```
You are conducting competitive intelligence for [Client Name], a mortgage
lender. For the competitor [Competitor Name] at [URL], evaluate and score
1-5 (5 = best-in-class) on each dimension, with a one-sentence justification
citing something specifically observed on the site:

1. Content depth & topical authority (does it read as genuinely expert?)
2. Technical SEO signals (structured data, page speed indicators, mobile UX)
3. UX/conversion mechanics (calculator quality, application flow friction,
   number of steps to a rate quote)
4. Visual design quality and modernity
5. Trust signal presence (licensing disclosures, reviews, loan officer bios,
   security signals)
6. Local/state-specific relevance (does it address the specific markets
   the client competes in?)

Do not guess at anything you cannot observe directly on the site; mark
"not observable" rather than inferring.
```

**Prompt 2.2 — White Space Synthesis**

```
Given the attached Competitor Scoring Matrix for [Client Name]'s competitive
set, identify white-space opportunities: things borrowers in the target
personas [attach personas] clearly need, that no competitor scored above a 3
on. For each opportunity, state: (1) the gap, (2) which persona it serves,
(3) a rough feasibility note (content-only fix vs. requires new UX/tooling),
(4) why competitors are likely missing it.
```

## 12. Examples

*Sample Competitor Scoring Matrix row:*

| Competitor | Content Depth | Technical SEO | UX/Conversion | Design | Trust Signals | Local Relevance | Notes |
|---|---|---|---|---|---|---|---|
| Competitor A | 4 | 3 | 2 | 4 | 3 | 2 | Strong blog content but 7-step application form; no state-specific pages despite multi-state licensing |

## 13. Common Mistakes

- Comparing against national megabrand lenders instead of the client's actual local/regional competitive set — this produces strategy the client cannot realistically execute against.
- Scoring competitors on impression rather than the specific rubric, producing unusable, non-comparable results.
- Failing to archive visual evidence, which weakens Stage Gate 7 design differentiation work later.

## 14. Best Practices

- Include at least one competitor who is clearly winning on SEO (organic visibility) even if their design is dated — the goal is pattern extraction, not aesthetic imitation.
- Capture competitor calculator and application flows step-by-step (screenshot each step) — friction points are usually invisible from the homepage alone.

## 15. Review Process

Engagement Lead and SEO Specialist jointly review the scoring matrix for consistency (same rubric applied evenly) before the White Space Map is finalized.

## 16. Quality Assurance

Primary Eight-Dimension focus: **SEO**, **Conversion**, **Brand** (differentiation clarity).

## 17. Exit Criteria

- [ ] Competitive Intelligence Report and Scoring Matrix approved by Engagement Lead
- [ ] White Space Opportunity Map contains at least 3 actionable, evidence-backed opportunities
- [ ] Findings shared with client for factual pushback window (5 business days) before Stage Gate 3 strategy work locks them in

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all three Required Documents saved v1.0
- Blueprint: no direct update yet (competitive findings feed Blueprint indirectly via Stage Gate 3 strategic decisions)
- Decision Register: log final competitor set selection as `DEC-SG2-001`

## 19. Future Enhancements

The Competitor Scoring Matrix is re-run in abbreviated form during Stage Gate 11.5 (Post-Launch Growth Program) to measure relative competitive movement post-launch.

---

# STAGE GATE 3 — STRATEGIC DIRECTION

## 1. Purpose

Convert Discovery and Competitive Intelligence findings into a single, decided strategic direction: positioning, core messaging pillars, and prioritized business objectives that will govern every architecture, design, and content decision from Stage Gate 4 forward.

## 2. Business Objectives

- Produce one clear, client-approved positioning statement.
- Prioritize which borrower personas and loan products the site architecture will be optimized around.
- Resolve any tension between competing business objectives (e.g., broad topical authority vs. narrow niche specialization) explicitly, rather than leaving it implicit.

## 3. Inputs

Discovery Report, Borrower Personas, Competitive Intelligence Report, White Space Opportunity Map, Project Charter business objectives

## 4. Outputs

- Strategic Direction Brief
- Positioning Statement
- Prioritized Persona & Product Matrix
- Messaging Pillars (3–5)

## 5. Required Documents

`/03-strategy/strategic-direction-brief-v1.md`, `/03-strategy/positioning-statement-v1.md`, `/03-strategy/messaging-pillars-v1.md`

## 6. Responsible Roles

Strategy Consultant (lead), Research Consultant (support), Engagement Lead (client negotiation)

## 7. Required Specialists

None mandatory; SEO Specialist consulted to sanity-check that the positioning is compatible with realistic topical authority building (Stage Gate 5).

## 8. Decision Authority

**Client sign-off required.** This is the first hard client approval gate in the engagement — every subsequent Volume assumes this direction is locked. The named Decision Authority from the Project Charter (Volume I, Sec. 3.4) must approve in writing.

## 9. Workflow

```
[1] Draft 2-3 candidate positioning statements from Discovery + Competitive
    findings
        │
        ▼
[2] Working session with client to pressure-test candidates against real
    business constraints (pricing position, service model, growth goals)
        │
        ▼
[3] Select and refine one positioning statement
        │
        ▼
[4] Prioritize personas/products into primary, secondary, tertiary tiers
        │
        ▼
[5] Draft 3-5 messaging pillars that operationalize the positioning
        │
        ▼
[6] Client approval (formal sign-off, Decision Authority)
        │
        ▼
[7] Stage Gate 4 scheduled
```

## 10. Checklist

- [ ] At least 2 positioning candidates were presented, not just one default option
- [ ] Positioning statement is falsifiable/specific — not generic ("we care about our customers") but differentiated and defensible against the White Space Map
- [ ] Personas ranked into explicit priority tiers with rationale
- [ ] Messaging pillars each map to at least one specific persona objection or decision driver
- [ ] Formal written client approval obtained from the named Decision Authority

## 11. Prompt(s)

**Prompt 3.1 — Positioning Candidate Generation**

```
You are the Strategy Consultant for [Client Name], a mortgage lender.
Using the attached Discovery Report, Borrower Personas, and White Space
Opportunity Map, draft 3 distinct candidate positioning statements. Each
must:
- Be one sentence, specific enough to be falsifiable (not generic trust
  language)
- Directly address at least one White Space opportunity
- Be credible given the client's actual licensing, service model, and team
  size (do not propose positioning the client cannot operationally deliver)
- Include a one-paragraph rationale citing specific Discovery/Competitive
  findings

Present the 3 candidates with a comparison table showing which persona
objections each one addresses and which competitors it differentiates
against.
```

**Prompt 3.2 — Messaging Pillar Development**

```
Given the approved positioning statement "[insert]" for [Client Name],
develop 3-5 messaging pillars. Each pillar needs: a short name, a one-
sentence definition, the specific persona objection or decision driver it
answers (cite from the Borrower Personas document), and 2-3 proof points
the client can credibly claim (ask for these if not yet confirmed — do not
invent credentials, awards, or statistics).
```

## 12. Examples

*Sample positioning statement:* "For first-time and credit-rebuilding buyers in [state], [Client Name] is the mortgage lender that replaces rate-shopping anxiety with a transparent, step-by-step path to approval — without the hard credit pull most lenders require just to get a real number."

## 13. Common Mistakes

- Allowing the client to select generic positioning ("we're the trusted local lender") because it feels safe — generic positioning produces generic architecture and content later, and fails to convert the SG2 White Space findings into anything actionable.
- Skipping formal written sign-off because the working session "felt" like agreement — verbal alignment in a meeting is not a Decision Register entry and is not binding.
- Locking positioning before compliance has confirmed any claims used in messaging pillars are substantiable (e.g., "fastest closing" claims require support).

## 14. Best Practices

- Present positioning candidates as a genuine choice with trade-offs, not a single recommendation dressed as three options — clients engage more honestly with real alternatives.
- Have the Compliance Liaison scan messaging pillars for advertising-claim risk (e.g., superlative or guarantee language) before client sign-off, not after.

## 15. Review Process

Engagement Lead facilitates the client approval session; SEO Specialist confirms positioning is compatible with a realistic topical authority strategy before the session; Compliance Liaison scans messaging pillars for claim risk.

## 16. Quality Assurance

Primary Eight-Dimension focus: **Brand**, **Conversion**, and early **SEO** compatibility check.

## 17. Exit Criteria

- [ ] Positioning statement formally approved in writing by named Decision Authority
- [ ] Messaging pillars finalized and compliance-scanned
- [ ] Persona/product priority tiers confirmed
- [ ] Decision Register entry logged for the approved positioning, including rejected alternatives and why

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all Required Documents saved v1.0 (this becomes the reference version for the rest of the engagement — treat as high-durability)
- Blueprint: "Business Context" section finalized with positioning, messaging pillars, and priority tiers
- Decision Register: `DEC-SG3-001` (positioning approval) logged as **Irreversible** reversibility rating — changing positioning after Stage Gate 4 begins is a major-version, Change-Request-triggering event

## 19. Future Enhancements

Positioning is stress-tested again in Stage Gate 7.5's Future-Proofing Review, and formally revisited only if Stage Gate 11.5 post-launch data reveals a persona/product mismatch requiring a strategic pivot.

---

*End of Volume II. Continue to Volume III — Website Architecture.*
