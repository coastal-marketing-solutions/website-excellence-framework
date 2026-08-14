# CORE METHODOLOGY — RESEARCH

*Website Excellence Framework (WEF) v1.0*

---

## Chapter Introduction

Research covers the first three Stage Gates of every WEF engagement, in any industry: Discovery & Market Research, Competitive Intelligence, and Strategic Direction. Together these gates convert a signed Project Charter into an evidence-based strategic foundation that every subsequent discipline builds on. No architecture, design, or content decision made later in the engagement should be traceable to anything other than a finding, decision, or objective established here — and, at each step, to the active Industry Module's Persona Library, Competitive Landscape Notes, or Positioning & Messaging Patterns.

### The Fixed Stage Gate Template

Every Stage Gate in the Core Methodology follows the same 19-part structure, defined once here and applied without restatement in every subsequent gate across every discipline chapter:

1. **Purpose** — Why this gate exists
2. **Business Objectives** — What business outcome this gate serves
3. **Inputs** — What must exist before this gate can start
4. **Outputs** — What this gate produces
5. **Required Documents** — Specific Knowledge Base artifacts produced
6. **Responsible Roles** — Who does the work (Governance, Sec. 2)
7. **Required Specialists** — Who must be consulted or must sign off
8. **Decision Authority** — Who has final approval
9. **Module Injection Point(s)** — Exactly which Industry Module section(s) this gate consumes (see Governance, Sec. 9)
10. **Workflow** — Step-by-step process
11. **Checklist** — Pass/fail completion checklist
12. **Prompt(s)** — Ready-to-use AI prompt templates for this gate, written generically with explicit placeholders for Industry Module content
13. **Examples** — Illustrative sample output (industry-neutral; see each Industry Module for vertical-specific worked examples)
14. **Common Mistakes** — Documented failure patterns
15. **Best Practices** — Documented success patterns
16. **Review Process** — How the deliverable is checked before sign-off
17. **Quality Assurance** — Which of the Eight Dimensions (Governance, Sec. 12.2) apply and how
18. **Exit Criteria** — The pass/fail gate itself
19. **Knowledge Base / Blueprint / Decision Register Updates** — What must be written where

Each Stage Gate additionally names any **Future Enhancements** — where its output is revisited later in the engagement — inline in its Workflow or Exit Criteria discussion rather than as a rigid 20th section, since this varies more naturally by gate.

### Research Evidence, Provenance, and Freshness Standard

Research is reusable only when a later consultant can tell **what was observed, when it was observed, and how much confidence to place in it**. For every material external fact, statistic, competitor observation, regulatory reference, market statement, or recommendation, preserve an Evidence & Source Register entry with:

- source title, publisher/owner, URL or file path, and source class (`authoritative/regulatory`, `client/first-party`, `neutral secondary`, `competitor`, or `inference`);
- publication date, access/extraction date, geography, population or sample definition, metric definition, and any stated limitations;
- the exact claim or observation used, whether it is a quotation, paraphrase, calculation, or inference, and the deliverables that consume it;
- confidence/status (`verified`, `client-confirmed`, `needs human verification`, `stale`, or `superseded`), a review/expiry date for time-sensitive material, and the responsible owner; and
- licensing or permitted-use notes for screenshots, datasets, photographs, maps, or third-party copy.

Use the strongest practical source for the decision. Prefer a regulator, official registry, professional association, client-owned record, or neutral public dataset for facts; use competitors for observable architecture and UX patterns, not as proof of the client's claims. Date market and platform information. If a source blocks automated access, returns an error, or exposes an ambiguous definition, do not silently substitute an estimate: mark the item as unverified, seek a second method or source, and record the limitation.

The Evidence & Source Register is a cross-gate working record. It does not replace a Stage Gate deliverable, a compliance sign-off, or client fact confirmation. A source that was adequate at discovery can become stale before launch; later gates must re-check any fact that appears in public copy, schema, pricing, licensing, availability, or comparison content.

Assign every public artifact containing decision-relevant facts a freshness class in the Content Freshness Register:

- **Evergreen:** principles unlikely to change; review on material business, legal, or product change.
- **Periodic:** statistics, rankings, staff, pricing, inventory, or service details; review on a fixed cadence.
- **Event-bound:** grants, programs, promotions, application windows, events, temporary rules, or campaigns; review at the named event/date and expire or qualify automatically when it passes.
- **Volatile:** rates, availability, emergency guidance, regulatory status, live inventory, or other facts capable of changing rapidly; show an “as of” date where useful and assign a short review interval or authoritative live source.

Each entry names the factual dependency, source, owner, last-verified date, next review or expiry trigger, and the disposition if it is no longer current: refresh, qualify, archive, redirect, consolidate, or noindex. A page does not become evergreen merely because its URL has no year in it.

---

# STAGE GATE 1 — DISCOVERY & MARKET RESEARCH

## 1. Purpose

Establish a factual, evidence-based understanding of the client organization's business, target audience, market footprint, and current digital position before any strategic or design decision is made.

## 2. Business Objectives

- Identify the client's actual (not assumed) target audience segments and their decision drivers.
- Establish the client's service area, offerings, and any niche specialization.
- Baseline the client's current website's performance, traffic, and conversion behavior, if one exists.
- Surface regulatory or professional-standards constraints early, using the active Industry Module as the starting checklist.

## 3. Inputs

- Signed Project Charter (naming the active Industry Module)
- Client intake questionnaire (Reusable Templates — Client Intake Templates)
- Access (read-only where possible) to client's current website, GA4/analytics, and Search Console, if available
- Active Industry Module's Persona Library and Regulatory & Compliance Landscape (seed version)

## 4. Outputs

- Discovery Report
- Client-Specific Persona Set (adapted from the Industry Module's Persona Library, minimum 2, typically 3–5)
- Current-State Digital Audit (if a prior website exists)
- Digital Estate & Access Map (domains, DNS, hosting, CMS, repositories/deployments, environments, backups, analytics/search properties, forms/CRM, ownership, and access status; never secret values)
- Compliance/Standards Constraint Log (seed version, expanded in later gates)

## 5. Required Documents

`/01-research/discovery-report-v1.md`, `/01-research/client-personas-v1.md`, `/01-research/current-state-audit-v1.md`, `/01-research/digital-estate-map-v1.md`, `/01-research/compliance-constraints-v1.md`

## 6. Responsible Roles

Research Consultant (lead), Engagement Lead (review), AI Orchestrator (supporting research synthesis)

## 7. Required Specialists

SEO Specialist (for current-state technical audit input), Compliance/Standards Liaison (to validate the client's specific regulatory/professional footprint against the Industry Module)

## 8. Decision Authority

Engagement Lead approves the Discovery Report as sufficient to proceed; no client sign-off is required at this gate, but the report is shared with the client for factual correction.

## 9. Module Injection Point(s)

> **Module Injection Point:** Load the active Industry Module's **Persona Library** before conducting stakeholder interviews — use it as the starting archetype set to validate or refine against real client input, not as a substitute for the interviews themselves. Load the **Regulatory & Compliance Landscape** section to seed the Compliance/Standards Constraint Log with the correct starting checklist for this vertical.

## 10. Workflow

```
[1] Client Intake Questionnaire returned
        │
        ▼
[2] Load active Industry Module's Persona Library and Regulatory
    Landscape as starting reference
        │
        ▼
[3] Stakeholder interviews (practitioners/staff, marketing lead,
    compliance contact)
        │
        ▼
[4] Current-state digital audit (if applicable): traffic, rankings,
    Core Web Vitals, conversion funnel review
        │
        ▼
[5] Persona synthesis: validate/refine Module archetypes against
    interviews + audit + market data into client-specific personas
        │
        ▼
[6] Compliance/standards constraint pass: confirm the client's specific
    licensing/jurisdiction/accreditation footprint against the Module's
    Regulatory Landscape checklist
        │
        ▼
[7] Discovery Report drafted (AI-assisted synthesis, human-reviewed)
        │
        ▼
[8] Internal review → Exit Criteria check → Stage Gate 2 scheduled
```

## 11. Checklist

- [ ] Active Industry Module's Persona Library and Regulatory Landscape loaded before interviews began
- [ ] Minimum 3 stakeholder interviews completed (marketing lead, at least one practitioner/frontline staff member, compliance contact if applicable)
- [ ] Current-state audit completed if a legacy site exists (traffic, rankings, CWV, conversion funnel)
- [ ] Digital Estate & Access Map identifies the registrar, authoritative DNS, hosting account and document root, production/staging URLs, custom domains and their external origins, CMS, source repository and deploy target, backup schedule and restore-test status, analytics/search properties, form/CRM destinations, named business owner, operational custodian, and access status for each system
- [ ] No passwords, API secrets, recovery codes, private keys, or full credentials copied into the Knowledge Base; the map points to the approved credential manager and records only ownership/access status
- [ ] Legacy-site preservation plan records the authoritative URL inventory, search/analytics baseline, content/media export, redirect requirements, and shutdown authority before migration work begins
- [ ] Client-specific personas drafted with named decision drivers and objections, not generic demographics only, and explicitly reconciled against the Module's starting archetypes
- [ ] Client's regulatory/licensing footprint confirmed against an authoritative source (not assumed from the client's own marketing material) and checked against the Module's Regulatory Landscape
- [ ] Material facts and external research are recorded in an Evidence & Source Register with source class, access date, definitions/limitations, confidence, and review date where time-sensitive
- [ ] Public artifacts with time-sensitive claims are entered in the Content Freshness Register with a class, owner, last-verified date, next review/expiry trigger, and stale-content disposition
- [ ] Compliance/Standards Constraint Log seeded
- [ ] Discovery Report reviewed by Engagement Lead

## 12. Prompt(s)

**Prompt 1.1 — Persona Synthesis**

```
You are the Research Consultant on a website engagement for [Client Name],
operating in the [Industry Module name] vertical. Using the attached
stakeholder interview notes, current-state digital audit, client intake
questionnaire, and the [Industry Module]'s Persona Library as your starting
reference, synthesize 3-5 client-specific personas.

For each persona, provide:
- Name and one-line archetype (drawing on the Module's archetype set where
  it fits, but adapted to what this specific client's interviews actually
  revealed)
- Primary need/service interest
- Top 3 decision drivers (what makes them choose this provider)
- Top 3 objections/hesitations
- Preferred information format (calculators/tools, guides, direct contact,
  live chat)
- A representative search query this persona would type

Do not invent statistics. Where you infer rather than cite a source from
the provided materials, label the line "[inference]" explicitly. Ground
every persona in at least one specific quote or data point from the source
material.
```

**Prompt 1.2 — Current-State Digital Audit Synthesis**

```
You are auditing the current website for [Client Name] in the [Industry
Module name] vertical. Given the attached GA4 export, Search Console
export, and PageSpeed/Core Web Vitals report, produce a Current-State
Digital Audit covering:
1. Traffic overview (organic vs. paid vs. direct, trend over trailing 12
   months)
2. Top 10 landing pages by organic sessions and their current keyword
   rankings
3. Core Web Vitals summary (LCP, INP, CLS) for mobile and desktop
4. Conversion funnel as currently instrumented (or note if not
   instrumented)
5. Three most significant technical or content gaps observed

Flag any metric you cannot verify from the provided exports rather than
estimating it.
```

**Prompt 1.3 — Digital Estate & Access Map**

```text
Create a Digital Estate & Access Map for [Client Name]. Inventory, without
recording secret values: domain registrar and renewal owner; authoritative
DNS and current records; hosting account, environment, document root, and
backup/restore status; CMS and administrative owner; source repository,
branch, deployment integration, and exact deploy target; production and
staging URLs; analytics, search, tag-management, consent, form, CRM, email,
CDN/security, and translation systems; and each system's business owner,
operational custodian, access status, and recovery path.

Mark every item Verified / Client-reported / Unknown. Flag split ownership,
personal accounts, cross-client connected properties, unknown billing or
renewal authority, absent tested backups, and any system where the live
state has no documented source of truth. Never include a password, token,
private key, recovery code, or other secret in the output.
```

## 13. Examples

See each Industry Module's front matter for a fully worked persona example in that vertical (e.g., the Mortgage Lending Module's "credit-anxious first-time buyer" persona, or the Law Firm Module's "post-accident, insurance-wary" persona). This chapter intentionally does not repeat vertical-specific examples, since the same Stage Gate 1 process produces structurally identical but substantively different output depending on the active Module.

## 14. Common Mistakes

- Building personas purely from marketing assumptions instead of actual stakeholder interviews and analytics.
- Ignoring the active Industry Module's Persona Library entirely and starting from a blank page, re-deriving archetypes the firm has already validated on prior engagements in that vertical.
- Treating the Module's Persona Library as final and skipping client-specific validation — the Module is a starting hypothesis, not a substitute for discovery.
- Skipping the current-state audit because "the client is starting a new site anyway" — historical performance data is often the best available signal of what audience segments already convert.
- Treating the Compliance/Standards Constraint Log as a later-stage concern instead of seeding it here, which causes late-stage rework.

## 15. Best Practices

- Interview at least one frontline practitioner or staff member directly — marketing leads routinely misjudge what customers actually ask when engaging directly.
- Pull the client's actual regulatory/licensing footprint from the authoritative registry named in the active Industry Module's Regulatory Landscape section, not from the client's own website footer, which is frequently out of date.
- Where no current site exists (new business, or full replatform with no analytics history), substitute a competitor-proxy audit using Stage Gate 2 data pulled forward.

## 16. Review Process

Engagement Lead reviews the Discovery Report against the Checklist (Section 11) and confirms every persona is traceable to source material and reconciled against the Module's Persona Library before approving progression to Stage Gate 2.

## 17. Quality Assurance

Primary Eight-Dimension focus: **SEO** (current-state audit accuracy) and **Conversion** (persona objection accuracy). Regulatory/compliance accuracy is verified against the Compliance/Standards Liaison's direct input, not inferred.

## 18. Exit Criteria

- [ ] Discovery Report approved by Engagement Lead
- [ ] Client-specific personas finalized (minimum 2), reconciled against the active Industry Module
- [ ] Compliance/Standards Constraint Log seeded and reviewed by the Compliance/Standards Liaison (where applicable)
- [ ] No open P0 backlog items blocking Stage Gate 2

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents (Section 5) saved as v1.0
- Blueprint: "Business Context" section populated with objectives and audience segments
- Decision Register: log any decision about persona prioritization as `DEC-SG1-00x`; log any deviation from the Module's default Persona Library as a candidate refinement to propose back to the Module (Governance, Sec. 9.5)

Personas are revisited and refined at Stage Gate 3 (Strategic Direction) and again informed by real behavioral data at Stage Gate 11.5 (Post-Launch Growth Program).

---

# STAGE GATE 2 — COMPETITIVE INTELLIGENCE

## 1. Purpose

Build a rigorous, evidence-based picture of how the client's direct competitors present themselves online, where they are strong or weak, and what white space exists for the client to win distinctly rather than imitate.

## 2. Business Objectives

- Identify 5–8 true competitors (organizations competing for the same audience segments in the same market), not generic "big brand" comparisons.
- Quantify competitor content, SEO, UX, and design strengths/weaknesses on a consistent rubric.
- Identify specific white-space opportunities the client can credibly own.

## 3. Inputs

- Discovery Report and Client Personas (Stage Gate 1)
- Client-nominated competitor list (from intake questionnaire)
- Active Industry Module's Competitive Landscape Notes (typical competitor archetypes for the vertical)
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

None mandatory beyond Responsible Roles; Visual Designer may be consulted for early design-pattern observation feeding the Design discipline.

## 8. Decision Authority

Engagement Lead approves the report; competitor list itself should be confirmed with the client before deep analysis begins to avoid analyzing the wrong set.

## 9. Module Injection Point(s)

> **Module Injection Point:** Load the active Industry Module's **Competitive Landscape Notes** to understand the typical competitor archetypes, common strengths/weaknesses patterns, and known table-stakes vs. differentiator features for this vertical before scoring the client's actual named competitors — this accelerates scoring and prevents mis-rating a competitor against the wrong baseline expectation.

## 10. Workflow

```
[1] Confirm competitor list (client-nominated + Research Consultant
    additions based on SERP presence for target queries from personas),
    informed by the Module's Competitive Landscape Notes
        │
        ▼
[2] Score each competitor on the Competitor Scoring Matrix (Sec. 12)
    across Content, SEO, UX, Design, Trust Signals, Conversion Mechanics
        │
        ▼
[3] Identify recurring patterns (what everyone does — table stakes) vs.
    differentiators (what only 1-2 do well), cross-checked against the
    Module's known vertical patterns
        │
        ▼
[4] Synthesize White Space Opportunity Map: gaps no competitor fills
    well
        │
        ▼
[5] Draft Competitive Intelligence Report
        │
        ▼
[6] Review → Exit Criteria → Stage Gate 3 scheduled
```

## 11. Checklist

- [ ] Active Industry Module's Competitive Landscape Notes reviewed before scoring began
- [ ] 5–8 true competitors identified and confirmed with client
- [ ] Every competitor scored on the full rubric, not a subset
- [ ] At least 3 white-space opportunities identified with supporting evidence
- [ ] Screenshots or captured references archived in Knowledge Base for each competitor (design/UX evidence, not just written description)
- [ ] Competitor observations are separated from claims about the client, and every material observation has a URL/file reference and capture/access date

## 12. Prompt(s)

**Prompt 2.1 — Competitor Scoring**

```
You are conducting competitive intelligence for [Client Name] in the
[Industry Module name] vertical. Using the [Industry Module]'s Competitive
Landscape Notes as background on typical patterns in this vertical,
evaluate and score the competitor [Competitor Name] at [URL] 1-5 (5 = best-
in-class) on each dimension, with a one-sentence justification citing
something specifically observed on the site:

1. Content depth & topical authority (does it read as genuinely expert?)
2. Technical SEO signals (structured data, page speed indicators, mobile
   UX)
3. UX/conversion mechanics (tool/calculator quality if applicable,
   engagement flow friction, number of steps to a qualified action)
4. Visual design quality and modernity
5. Trust signal presence (per the Module's Trust Signal Requirements —
   licensing/credential disclosures, reviews, practitioner bios, security
   signals)
6. Local/service-area relevance (does it address the specific markets the
   client competes in?)

Do not guess at anything you cannot observe directly on the site; mark
"not observable" rather than inferring.
```

**Prompt 2.2 — White Space Synthesis**

```
Given the attached Competitor Scoring Matrix for [Client Name]'s
competitive set and the [Industry Module]'s known vertical patterns,
identify white-space opportunities: things prospective customers in the
target personas [attach personas] clearly need, that no competitor scored
above a 3 on. For each opportunity, state: (1) the gap, (2) which persona
it serves, (3) a rough feasibility note (content-only fix vs. requires new
UX/tooling), (4) why competitors are likely missing it.
```

## 13. Examples

See each Industry Module's Competitive Landscape Notes for vertical-specific worked examples of common competitor patterns (e.g., what a typical mortgage lender's site gets wrong, vs. what a typical law firm's site gets wrong).

## 14. Common Mistakes

- Comparing against national megabrands instead of the client's actual local/regional competitive set — this produces strategy the client cannot realistically execute against.
- Scoring competitors on impression rather than the specific rubric, producing unusable, non-comparable results.
- Ignoring the active Industry Module's Competitive Landscape Notes and re-discovering well-known vertical patterns from scratch each engagement.
- Failing to archive visual evidence, which weakens Design-discipline differentiation work later.

## 15. Best Practices

- Include at least one competitor who is clearly winning on SEO (organic visibility) even if their design is dated — the goal is pattern extraction, not aesthetic imitation.
- Capture competitor conversion flows (calculators, forms, booking tools) step-by-step (screenshot each step) — friction points are usually invisible from the homepage alone.
- Preserve the source and access date for every market or platform fact, and record whether a source is authoritative, first-party, neutral secondary, competitor, or inference. This prevents a dated third-party metric from becoming an undated site claim.

## 16. Review Process

Engagement Lead and SEO Specialist jointly review the scoring matrix for consistency (same rubric applied evenly) before the White Space Map is finalized.

## 17. Quality Assurance

Primary Eight-Dimension focus: **SEO**, **Conversion**, **Brand** (differentiation clarity).

## 18. Exit Criteria

- [ ] Competitive Intelligence Report and Scoring Matrix approved by Engagement Lead
- [ ] White Space Opportunity Map contains at least 3 actionable, evidence-backed opportunities
- [ ] Findings shared with client for factual pushback window (5 business days) before Stage Gate 3 strategy work locks them in

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all three Required Documents saved v1.0
- Blueprint: no direct update yet (competitive findings feed Blueprint indirectly via Stage Gate 3 strategic decisions)
- Decision Register: log final competitor set selection as `DEC-SG2-001`

The Competitor Scoring Matrix is re-run in abbreviated form during Stage Gate 11.5 (Post-Launch Growth Program) to measure relative competitive movement post-launch.

---

# STAGE GATE 3 — STRATEGIC DIRECTION

## 1. Purpose

Convert Discovery and Competitive Intelligence findings into a single, decided strategic direction: positioning, core messaging pillars, and prioritized business objectives that will govern every architecture, design, and content decision from Information Architecture forward.

## 2. Business Objectives

- Produce one clear, client-approved positioning statement.
- Prioritize which client personas and offerings the site architecture will be optimized around.
- Resolve any tension between competing business objectives explicitly, rather than leaving it implicit.

## 3. Inputs

Discovery Report, Client Personas, Competitive Intelligence Report, White Space Opportunity Map, Project Charter business objectives, active Industry Module's Positioning & Messaging Patterns

## 4. Outputs

- Strategic Direction Brief
- Positioning Statement
- Prioritized Persona & Offering Matrix
- Messaging Pillars (3–5)

## 5. Required Documents

`/03-strategy/strategic-direction-brief-v1.md`, `/03-strategy/positioning-statement-v1.md`, `/03-strategy/messaging-pillars-v1.md`

## 6. Responsible Roles

Strategy Consultant (lead), Research Consultant (support), Engagement Lead (client negotiation)

## 7. Required Specialists

None mandatory; SEO Specialist consulted to sanity-check that the positioning is compatible with realistic topical authority building (SEO & Architecture discipline).

## 8. Decision Authority

**Client sign-off required.** This is the first hard client approval gate in the engagement — every subsequent discipline assumes this direction is locked. The named Decision Authority from the Project Charter must approve in writing.

## 9. Module Injection Point(s)

> **Module Injection Point:** Load the active Industry Module's **Positioning & Messaging Patterns** section for common, proven positioning angles and known claim-risk language specific to this vertical, before drafting candidate positioning statements. Have the Compliance/Standards Liaison cross-check messaging pillars against the Module's Regulatory & Compliance Landscape before client sign-off.

## 10. Workflow

```
[1] Draft 2-3 candidate positioning statements from Discovery +
    Competitive findings + the Module's Positioning & Messaging Patterns
        │
        ▼
[2] Working session with client to pressure-test candidates against real
    business constraints (pricing position, service model, growth goals)
        │
        ▼
[3] Select and refine one positioning statement
        │
        ▼
[4] Prioritize personas/offerings into primary, secondary, tertiary tiers
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

## 11. Checklist

- [ ] Active Industry Module's Positioning & Messaging Patterns reviewed before drafting candidates
- [ ] At least 2 positioning candidates were presented, not just one default option
- [ ] Positioning statement is falsifiable/specific — not generic ("we care about our customers") but differentiated and defensible against the White Space Map
- [ ] Personas ranked into explicit priority tiers with rationale
- [ ] Messaging pillars each map to at least one specific persona objection or decision driver
- [ ] Formal written client approval obtained from the named Decision Authority

## 12. Prompt(s)

**Prompt 3.1 — Positioning Candidate Generation**

```
You are the Strategy Consultant for [Client Name] in the [Industry Module
name] vertical. Using the attached Discovery Report, Client Personas,
White Space Opportunity Map, and the [Industry Module]'s Positioning &
Messaging Patterns, draft 3 distinct candidate positioning statements.
Each must:
- Be one sentence, specific enough to be falsifiable (not generic trust
  language)
- Directly address at least one White Space opportunity
- Be credible given the client's actual credentials, service model, and
  team size (do not propose positioning the client cannot operationally
  deliver)
- Avoid any claim pattern the Module's Positioning & Messaging Patterns
  flags as high compliance risk for this vertical
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
answers (cite from the Client Personas document), and 2-3 proof points the
client can credibly claim (ask for these if not yet confirmed — do not
invent credentials, awards, or statistics). Flag any pillar language that
the [Industry Module]'s Regulatory & Compliance Landscape suggests may
need Compliance/Standards Liaison review.
```

## 13. Examples

See each Industry Module's Positioning & Messaging Patterns for vertical-specific worked positioning examples.

## 14. Common Mistakes

- Allowing the client to select generic positioning ("we're the trusted local provider") because it feels safe — generic positioning produces generic architecture and content later, and fails to convert the Stage Gate 2 White Space findings into anything actionable.
- Skipping formal written sign-off because the working session "felt" like agreement — verbal alignment in a meeting is not a Decision Register entry and is not binding.
- Locking positioning before the Compliance/Standards Liaison has confirmed any claims used in messaging pillars are substantiable and compliant with the active Industry Module's requirements.

## 15. Best Practices

- Present positioning candidates as a genuine choice with trade-offs, not a single recommendation dressed as three options — clients engage more honestly with real alternatives.
- Have the Compliance/Standards Liaison scan messaging pillars for claim risk (per the Module's flagged language patterns) before client sign-off, not after.

## 16. Review Process

Engagement Lead facilitates the client approval session; SEO Specialist confirms positioning is compatible with a realistic topical authority strategy before the session; Compliance/Standards Liaison scans messaging pillars for claim risk against the active Industry Module.

## 17. Quality Assurance

Primary Eight-Dimension focus: **Brand**, **Conversion**, and early **SEO** compatibility check.

## 18. Exit Criteria

- [ ] Positioning statement formally approved in writing by named Decision Authority
- [ ] Messaging pillars finalized and compliance-scanned against the active Industry Module
- [ ] Persona/offering priority tiers confirmed
- [ ] Decision Register entry logged for the approved positioning, including rejected alternatives and why

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all Required Documents saved v1.0 (this becomes the reference version for the rest of the engagement — treat as high-durability)
- Blueprint: "Business Context" section finalized with positioning, messaging pillars, and priority tiers
- Decision Register: `DEC-SG3-001` (positioning approval) logged as **Irreversible** reversibility rating — changing positioning after Information Architecture begins is a major-version, Change-Request-triggering event

Positioning is stress-tested again in the Design discipline's Prototype Validation gate, and formally revisited only if Post-Launch Growth Program data reveals a persona/offering mismatch requiring a strategic pivot.

---

*End of Research. Continue to Core Methodology — SEO & Architecture.*
