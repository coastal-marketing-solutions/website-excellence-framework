# VOLUME I — GOVERNANCE & OPERATING SYSTEM

*Mortgage Website Excellence Framework (MWEF) v1.0*

---

## Volume Introduction

Volume I is the operating system on which every other Volume runs. It defines how an engagement starts, who does what, how decisions and knowledge persist across a multi-week (or multi-month) engagement, and — critically for this methodology — how multiple AI models can collaborate on the same engagement without contradicting each other or losing context. Read this Volume in full before beginning any client work.

---

## 1. Project Initialization

### 1.1 Purpose

Project Initialization converts a signed Statement of Work (SOW) into a running engagement with an assigned team, a provisioned Knowledge Base, and a scheduled first Stage Gate. It exists to prevent the single most common cause of engagement failure: starting substantive work before the team agrees on scope, roles, and success criteria.

### 1.2 Initialization Workflow

```
 SOW Signed
     │
     ▼
 [1] Engagement Lead assigned ──────► Engagement Lead confirms scope vs. SOW
     │
     ▼
 [2] Core team staffed (see Sec. 2) ─► Roles assigned; specialists booked
     │
     ▼
 [3] Knowledge Base provisioned ─────► Folder structure created (Sec. 5)
     │
     ▼
 [4] Project Charter drafted ────────► See Sec. 3; signed by client + Engagement Lead
     │
     ▼
 [5] Kickoff Meeting held ───────────► Template: Volume VI, Meeting Templates
     │
     ▼
 [6] Master Website Blueprint seeded ► Skeleton document created (Sec. 6)
     │
     ▼
 [7] Stage Gate 1 scheduled ─────────► Engagement formally begins
```

### 1.3 Initialization Checklist

- [ ] SOW reviewed by Engagement Lead against MWEF standard scope boundaries
- [ ] Client primary contact and decision authority (Section 3.4) confirmed in writing
- [ ] Core team assigned and calendars blocked for Stage Gates 1–3 at minimum
- [ ] Knowledge Base workspace created at `/clients/{client-name}/mwef/`
- [ ] Project Charter drafted and routed for signature
- [ ] Kickoff meeting scheduled within 5 business days of SOW signature
- [ ] Compliance contact identified (client-side legal/compliance officer of record)
- [ ] Technology stack confirmed or default stack (Volume I Sec. 13.4) accepted
- [ ] Billing/scope guardrails communicated to full team

### 1.4 Common Mistakes

- Starting Discovery interviews (Stage Gate 1) before the Project Charter is signed, resulting in scope disputes later.
- Failing to identify a compliance contact at initialization — this routinely causes rework in Stage Gate 9 (Copywriting) and Stage Gate 11 (QA).
- Assigning a single generalist to cover both SEO and Copywriting roles on engagements where the client has aggressive topical authority goals; this understaffing shows up as schedule slippage at Stage Gate 5.

---

## 2. Consulting Organization

### 2.1 Purpose

Defines the standing roles used across every MWEF engagement, their responsibilities, and their decision rights. Not every engagement staffs every role as a distinct human — smaller engagements may consolidate roles — but every responsibility below must be explicitly assigned to someone (human or AI-with-human-reviewer) before Stage Gate 1 begins.

### 2.2 Role Definitions

| Role | Primary Responsibility | Typical Stage Gate Ownership |
|---|---|---|
| **Engagement Lead** | Overall accountability for engagement outcomes, client relationship, Decision Register authority | All gates (approval) |
| **Project Manager** | Schedule, backlog, risk register, meeting cadence, cross-role coordination | All gates (operations) |
| **Research Consultant** | Market research, discovery synthesis, competitive intelligence | SG1, SG2, SG3 |
| **Strategy Consultant** | Positioning, strategic direction, business objective alignment | SG3, SG6 |
| **Information Architect** | Sitemap, content hierarchy, navigation, taxonomy | SG4 |
| **SEO Specialist** | Keyword architecture, topical maps, technical SEO, schema strategy | SG5, SG8, SG10.5, SG11.5 |
| **UX Designer** | User flows, conversion paths, wireframes | SG6, SG7 |
| **Visual Designer** | Design system, visual identity, GeneratePress/GenerateBlocks design specification | SG7, SG7.5 |
| **Copywriter** | On-page copy, calculators' microcopy, disclosures coordination | SG9 |
| **Developer / WordPress Implementer** | GeneratePress/GenerateBlocks build, performance, integrations | SG10, SG10.5 |
| **QA Analyst** | Functional, performance, accessibility, SEO, and compliance QA | SG11 |
| **Compliance Liaison (client-side)** | Reviews all rate, disclosure, and licensing content | SG8, SG9, SG11 (mandatory) |
| **AI Orchestrator (human)** | Manages LLM Handoff Protocol, prompt quality, output verification | All gates |

### 2.3 RACI Summary (Engagement-Level)

| Activity | Engagement Lead | Project Manager | Specialists | Client |
|---|---|---|---|---|
| Project Charter approval | A | R | C | A |
| Stage Gate exit sign-off | A | R | R | I (or A for SG3, SG7.5, SG11) |
| Decision Register entries | A | R | R | I |
| Compliance sign-off | I | I | C | A |
| Go-live authorization | A | R | C | A |

*(R = Responsible, A = Accountable, C = Consulted, I = Informed)*

### 2.4 Best Practices

- Never let the Visual Designer also serve as final QA Analyst on the same engagement — independent review of design fidelity requires separation of duties.
- The Compliance Liaison must be client-side, not a firm consultant role-playing compliance; MWEF firms do not issue legal opinions.
- On engagements under a certain size (to be defined in the Project Charter), the AI Orchestrator role may be held by the Engagement Lead directly, but must still be explicitly named.

---

## 3. Project Charter

### 3.1 Purpose

The Project Charter is the foundational governance document of the engagement. It is signed before Stage Gate 1 begins and is the reference document the Decision Register, Knowledge Base, and every Stage Gate cite back to when questions of scope arise.

### 3.2 Required Contents

| Section | Contents |
|---|---|
| Engagement Overview | Client name, lender type (retail, wholesale/broker, credit union, correspondent), states licensed, target markets |
| Business Objectives | Quantified goals (e.g., "increase qualified rate-quote submissions by 35% within 6 months of launch") |
| Scope Boundaries | In-scope pages/features; explicitly out-of-scope items (e.g., loan origination system integration, CRM build) |
| Technology Stack | Default MWEF stack (Sec. 13.4) or client-specified alternative, with rationale if alternative |
| Compliance Framework | Applicable regulations (TILA, RESPA, ECOA, SAFE Act, state licensing), NMLS ID, compliance contact |
| Roles & Staffing | Named individuals/AI roles per Section 2 |
| Timeline | Target dates for each Stage Gate |
| Decision Authority | Named individual(s) with final sign-off authority at each approval gate |
| Success Metrics | KPIs to be tracked post-launch (Stage Gate 11.5) |
| Assumptions & Dependencies | E.g., "client will provide loan officer bios within 5 business days of request" |
| Change Control Process | Reference to Volume VI Change Request template |

### 3.3 Project Charter Template

See **Volume VI — Client Intake Templates** for the fillable Project Charter template. All fields marked "Required" must be completed before Charter signature; fields marked "Confirm at SG3" may be finalized after Strategic Direction is set.

### 3.4 Decision Authority Standard

Every Project Charter must name exactly one client-side individual as final Decision Authority for each of the following gates: Strategic Direction (SG3), Visual Design System (SG7.5 Executive Approval), and Go-Live (post SG11). Ambiguity here — "the marketing team will decide" — is a Charter defect and must be corrected before signature.

### 3.5 Common Mistakes

- Leaving Decision Authority as a committee rather than a named person, which stalls SG7.5 executive approval indefinitely.
- Failing to capture state licensing footprint accurately, which causes rework in SG5 (SEO Blueprint — local/state landing pages) and SG9 (state-specific disclosures).

---

## 4. Decision Register

### 4.1 Purpose

The Decision Register is the append-only ledger of every material decision made during the engagement: what was decided, why, by whom, on what evidence, and what alternatives were rejected. It is the mechanism that lets a consultant (or AI model) joining the engagement at Stage Gate 8 understand why the sitemap looks the way it does without re-reading every Stage Gate 4 working session.

### 4.2 Decision Register Schema

| Field | Description |
|---|---|
| Decision ID | Sequential, format `DEC-{stage gate}-{sequence}`, e.g., `DEC-SG4-003` |
| Date | Date decided |
| Decision Summary | One-sentence statement of what was decided |
| Rationale | Evidence/reasoning supporting the decision |
| Alternatives Considered | What else was on the table, and why it was rejected |
| Decided By | Named individual(s) |
| Stage Gate | Which Stage Gate this decision belongs to |
| Impacts | Which Blueprint sections, backlog items, or downstream gates this affects |
| Reversibility | Reversible / Costly to Reverse / Irreversible |
| Status | Active / Superseded (with link to superseding Decision ID) |

### 4.3 Governance Rule

Decisions are never deleted, only superseded. If a Stage Gate 7 design decision is later reversed at Stage Gate 7.5, a new Decision Register entry is created referencing and superseding the original — preserving full engagement history for audit and reuse.

### 4.4 When to Log a Decision

Log a Decision Register entry any time: a strategic direction is chosen among alternatives; a scope boundary is set or changed; a compliance interpretation is applied; a design or architecture pattern is selected over competing options; or an AI model's recommendation is accepted, modified, or rejected by a human reviewer.

---

## 5. Knowledge Base

### 5.1 Purpose

The Knowledge Base (KB) is the single persistent store of every artifact, research finding, deliverable, and decision produced during the engagement. It is what makes MWEF engagements AI-collaborable: any model can be given a defined KB path and immediately have full context for the current state of the engagement.

### 5.2 Standard Folder Structure

```
/clients/{client-name}/mwef/
├── 00-charter/
│   ├── project-charter.md
│   └── decision-register.md
├── 01-research/                  (Stage Gate 1)
├── 02-competitive/               (Stage Gate 2)
├── 03-strategy/                  (Stage Gate 3)
├── 04-architecture/              (Stage Gate 4)
├── 05-seo-blueprint/             (Stage Gate 5)
├── 06-ux-conversion/             (Stage Gate 6)
├── 07-design-system/             (Stage Gate 7)
├── 07.5-prototype-validation/    (Stage Gate 7.5)
├── 08-content-spec/              (Stage Gate 8)
├── 09-copywriting/               (Stage Gate 9)
├── 10-ai-build-package/          (Stage Gate 10)
├── 10.5-wp-implementation/       (Stage Gate 10.5)
├── 11-qa/                        (Stage Gate 11)
├── 11.5-post-launch/             (Stage Gate 11.5)
├── blueprint/
│   └── master-website-blueprint.md
├── backlog/
│   └── project-backlog.md
└── memory/
    └── project-memory.md
```

### 5.3 Knowledge Base Governance Rules

1. Every Stage Gate deliverable is saved to its numbered folder — never to a personal drive, chat log, or email attachment only.
2. File naming follows the Documentation Standard (Section 8.3).
3. The Knowledge Base is read-access for the full team and client sponsor; write-access is role-gated per the RACI in Section 2.3.
4. No deliverable is considered final until it exists in the Knowledge Base in its approved form — a Slack message or verbal approval is not sufficient.

### 5.4 AI Access Pattern

When briefing an AI model for a Stage Gate task, the standard context package is: (1) Project Charter, (2) Decision Register (filtered to relevant Stage Gates), (3) Master Website Blueprint (current state), (4) the specific Stage Gate chapter of this manual, (5) any Stage Gate inputs listed in that chapter. This is formalized in the LLM Handoff Protocol (Section 9).

---

## 6. Master Website Blueprint

### 6.1 Purpose

The Master Website Blueprint (MWB) is the single living document that aggregates the *current, approved state* of every architectural, design, and content decision about the website — as distinct from the Decision Register, which is a historical log. If the Decision Register is the "why," the Blueprint is the "what, right now."

### 6.2 Blueprint Sections

| Section | Populated At | Contents |
|---|---|---|
| Business Context | SG1–SG3 | Objectives, audience segments, positioning |
| Sitemap & IA | SG4 | Full page hierarchy, URL structure |
| SEO Architecture | SG5 | Keyword map, topical clusters, schema plan |
| UX Flows | SG6 | Primary conversion paths, wireframe references |
| Design System | SG7–SG7.5 | Approved visual system, component library |
| Content Inventory | SG8–SG9 | Page-by-page content specs and approved copy |
| Technical Build Spec | SG10–SG10.5 | GeneratePress/GenerateBlocks implementation record |
| QA Status | SG11 | Outstanding issues, sign-off record |
| Growth Program | SG11.5 | KPIs, experiment log, optimization roadmap |

### 6.3 Blueprint Update Discipline

Every Stage Gate chapter in Volumes II–V ends with a "Blueprint Updates" subsection specifying exactly what must be written into the MWB before the gate can close. The Blueprint is never updated informally — updates happen only as part of a Stage Gate exit.

### 6.4 Blueprint as AI Context Anchor

The current MWB is the primary grounding document for any AI model asked to produce work on the engagement. A model prompted without the current MWB in context is operating blind and its output must be treated as draft-only pending reconciliation.

---

## 7. Project Backlog

### 7.1 Purpose

The Project Backlog tracks discrete units of work below the Stage Gate level — tasks, open questions, content items pending, dependencies on the client — so that the Project Manager has a single place to assess engagement health at any moment.

### 7.2 Backlog Item Schema

| Field | Description |
|---|---|
| Item ID | Format `BL-{sequence}` |
| Title | Short description |
| Stage Gate | Associated gate |
| Owner | Assigned role/person |
| Status | Not Started / In Progress / Blocked / Client-Dependent / Done |
| Priority | P0 (blocks gate exit) / P1 / P2 |
| Dependency | What this item is blocked by, if anything |
| Due Date | Target completion |

### 7.3 Backlog Cadence

Reviewed at minimum weekly by the Project Manager; P0 items are reviewed daily until cleared. Client-Dependent items exceeding their due date by more than 5 business days are escalated to the Engagement Lead and logged as a Risk (Section 14).

---

## 8. Documentation Standards

### 8.1 Purpose

Consistent documentation is what allows deliverables to move between human consultants and AI models without translation loss. All MWEF deliverables follow the standards below.

### 8.2 Formatting Standards

- Markdown as the canonical authoring format for all strategy, research, and specification documents.
- Headings follow strict hierarchy (H1 document title, H2 major section, H3 subsection); no skipped levels.
- Tables used for any structured comparison, rubric, or schema — never prose paragraphs describing tabular data.
- Every deliverable begins with a metadata block: Client, Stage Gate, Author (human or AI model + reviewer), Date, Version, Status.

### 8.3 File Naming Convention

`{stage-gate-number}-{deliverable-short-name}-v{version}.md`

Example: `05-seo-topical-map-v1.md`, `07-design-system-spec-v2.md`

### 8.4 Versioning Within Documents

Draft versions are tracked as v0.x; the first client- or Engagement-Lead-approved version becomes v1.0; subsequent approved revisions increment the minor or major version per Section 11.

### 8.5 Common Mistakes

- Producing deliverables as unstructured chat transcripts instead of formatted Knowledge Base documents.
- Mixing draft and approved content in the same file without a status marker, causing downstream gates to build on unapproved assumptions.

---

## 9. LLM Handoff Protocol

### 9.1 Purpose

MWEF engagements assume that different Stage Gates may be executed with the assistance of different AI models — for example, a research-oriented model for Stage Gates 1–3, a design-oriented model for Stage Gates 7–7.5, and a code-generation-oriented model for Stage Gate 10. The LLM Handoff Protocol ensures that context, decisions, and constraints survive the transition between models without a human having to manually re-explain the entire engagement.

### 9.2 The Four-Layer Context Package

Every AI model handoff must include, in this order:

1. **Charter Layer** — Project Charter (Section 3) in full. Establishes non-negotiable business objectives, compliance constraints, and decision authority.
2. **History Layer** — Decision Register entries (Section 4) relevant to the task at hand, filtered by Stage Gate tag. Establishes what has already been decided and why, so the model does not re-litigate settled questions.
3. **State Layer** — Current Master Website Blueprint (Section 6). Establishes the present factual state of the site's architecture, design, and content.
4. **Task Layer** — The specific Stage Gate chapter from this manual (Volumes II–V), including its Prompt(s) subsection, plus any specific human instruction for the current task.

### 9.3 Handoff Checklist

- [ ] Charter Layer attached and current (no unresolved Charter Change Requests pending)
- [ ] History Layer filtered to relevant Decision Register entries — not the entire register, to preserve context window budget, but never omitted
- [ ] State Layer confirmed as the latest approved Blueprint version
- [ ] Task Layer includes exact Stage Gate chapter and explicit deliverable expected
- [ ] Human AI Orchestrator reviews model output against the Stage Gate's Quality Assurance criteria before it is logged as a deliverable
- [ ] Any AI-proposed deviation from a prior Decision Register entry is flagged explicitly to the human Engagement Lead, not silently applied

### 9.4 Model-to-Model Consistency Rule

When a second AI model picks up work from a first (e.g., a build-oriented model implementing a design-oriented model's Stage Gate 7 output), the receiving model must be given the *producing* model's actual output as State Layer — never a human's paraphrase of it. Paraphrasing across handoffs is the single largest source of specification drift observed in MWEF pilot engagements.

### 9.5 Human-in-the-Loop Requirement

No AI-produced deliverable exits a Stage Gate without human review against that gate's exit criteria. The LLM Handoff Protocol accelerates production; it does not remove the human quality gate defined in each Stage Gate's "Review Process" subsection.

### 9.6 Common Mistakes

- Re-prompting a fresh model instance mid-engagement without the History Layer, causing it to silently contradict earlier decisions.
- Treating AI output as final without the human review step required in every Stage Gate chapter.
- Allowing context window pressure to justify dropping the Charter Layer — compliance and scope constraints must never be summarized away.

---

## 10. Project Memory

### 10.1 Purpose

Project Memory is a rolling, human-and-AI-readable summary of engagement state, distinct from both the Decision Register (full history) and the Blueprint (current architectural state). It exists to answer the question "what is the current status and what should I know before I do anything today?" in under two minutes of reading.

### 10.2 Project Memory Contents

- Current Stage Gate and its status (not started / in progress / pending exit review / complete)
- Last 5 Decision Register entries
- Open P0 backlog items
- Open risks (Section 14)
- Any pending client dependencies
- Next scheduled milestone/meeting

### 10.3 Update Cadence

Updated by the Project Manager at the close of every working session and at every Stage Gate transition. Project Memory is the first document any team member or AI model should read when resuming work on an engagement after any gap.

---

## 11. Version Control

### 11.1 Purpose

Ensures that every deliverable, the Blueprint, and this manual itself can be traced to a specific, unambiguous version at any point in time.

### 11.2 Versioning Scheme

MWEF uses semantic-style versioning for engagement deliverables:

- **Major version** (v1 → v2): Structural or strategic change requiring re-approval (e.g., a sitemap restructure after SG4 was already approved).
- **Minor version** (v1.0 → v1.1): Material content or design refinement within an approved structure.
- **Patch** (v1.1 → v1.1.1): Copy edits, typo fixes, non-substantive corrections.

### 11.3 Approval Gate for Version Increments

Any major version increment requires a new Decision Register entry explaining why the previously approved version is being revised, and re-triggers the relevant Stage Gate's Review Process before the new version can be marked "Approved."

### 11.4 This Manual's Own Versioning

Governed identically — see Front Matter Version History and Volume I Section 13 (Governance Policies) for how changes to MWEF itself are proposed, reviewed, and released.

---

## 12. Quality Assurance (Firm-Level)

### 12.1 Purpose

Distinct from Stage Gate 11 (project-level QA of the website itself), Firm-Level QA governs the quality of the *engagement's methodology execution* — are Stage Gates being run correctly, are deliverables meeting the manual's standards, is documentation discipline being maintained.

### 12.2 The Eight-Dimension Quality Standard

Every recommendation or deliverable produced anywhere in an MWEF engagement must be evaluated against all eight dimensions before it is considered complete:

| Dimension | Guiding Question |
|---|---|
| Performance | Does this decision help the site load fast and respond instantly? |
| Accessibility | Can a borrower using assistive technology use this without friction? |
| SEO | Does this strengthen topical authority, entity clarity, and technical crawlability? |
| Conversion | Does this reduce borrower anxiety and friction toward a qualified lead? |
| Brand | Is this consistent with the client's approved positioning and visual identity? |
| Scalability | Will this still work cleanly when the site grows to 5x its current page count? |
| Maintainability | Can the client's own team (or a future consultant) maintain this without the original author? |
| WordPress/GeneratePress/GenerateBlocks Compatibility & AI Implementation Readiness | Can this be built cleanly on the default stack, and is the spec precise enough for an AI build model to implement without guessing? |

### 12.3 Firm-Level QA Cadence

- Spot audit of one active engagement's Knowledge Base per month by someone outside the engagement team.
- Full methodology compliance audit at engagement close, feeding the Post-Launch Growth Program retrospective (Stage Gate 11.5) and, in aggregate, this manual's semiannual review (Front Matter, Document Control).

---

## 13. Governance Policies

### 13.1 Methodology Governance Board

A standing body (minimum 3 senior consultants) responsible for approving changes to this manual, adjudicating disputes about Stage Gate exit criteria, and maintaining the default technology stack decision.

### 13.2 Change Proposal Process

1. Any team member may submit a Change Request (Volume VI template) against this manual.
2. The Governance Board reviews within 10 business days.
3. Approved changes are logged in the Revision Log (Front Matter) and released as a new manual version per Section 11.4.
4. Rejected changes are logged with rationale for future reference.

### 13.3 Engagement-Level Governance

Within a single engagement, the Engagement Lead holds equivalent authority to the Governance Board for engagement-specific interpretation questions, but may not override this manual's Stage Gate exit criteria, quality standards, or compliance requirements without Governance Board sign-off logged as a Decision Register entry tagged `GOVERNANCE-EXCEPTION`.

### 13.4 Default Technology Stack Policy

Unless the Project Charter specifies an alternative:

| Layer | Default |
|---|---|
| Hosting | Hostinger VPS |
| CMS | WordPress |
| Theme Framework | GeneratePress Premium |
| Page Building | GenerateBlocks Pro |
| Asset/Cloud Layer | GenerateCloud |
| SEO Plugin | Rank Math SEO |
| Caching | LiteSpeed Cache |
| CDN / Edge Security | Cloudflare |
| Analytics | Google Analytics 4 |
| Search Monitoring | Google Search Console |
| Tag Management | Google Tag Manager |
| Behavioral Analytics | Microsoft Clarity |

Any deviation must be documented in the Project Charter with rationale and logged as a Decision Register entry at initialization.

### 13.5 Compliance Governance

MWEF consultants and AI models never issue final compliance sign-off. Every piece of content touching rates, APR examples, disclosures, licensing statements, or advertising claims must pass through the client's named Compliance Liaison (Section 2.2) before publication, formalized as a mandatory review step in Stage Gates 8, 9, and 11.

---

## 14. Risk Management

### 14.1 Purpose

Provides a standard mechanism for identifying, tracking, and mitigating risks to engagement success — schedule, compliance, technical, or client-relationship risks — before they become issues.

### 14.2 Risk Register Schema

| Field | Description |
|---|---|
| Risk ID | Format `RISK-{sequence}` |
| Description | What could go wrong |
| Category | Schedule / Compliance / Technical / Client Relationship / Scope |
| Likelihood | Low / Medium / High |
| Impact | Low / Medium / High |
| Mitigation Plan | Specific action(s) to reduce likelihood or impact |
| Owner | Who is responsible for monitoring/mitigating |
| Status | Open / Mitigated / Realized (became an Issue) / Closed |

### 14.3 Standard MWEF Risk Categories to Screen For

- **Compliance drift**: content or design implying rate guarantees, pre-approval, or terms without required qualifying language.
- **Scope creep at Stage Gate 4/6**: information architecture growing beyond Charter-approved page counts without a Change Request.
- **Client bottleneck risk**: dependency on a single client stakeholder (e.g., for loan officer bios, compliance review) with no backup path.
- **Platform lock-in risk**: build decisions in Stage Gate 10 that would be costly to reverse if the client later leaves the default stack.
- **AI hallucination risk**: AI-produced statistics, competitor claims, or regulatory statements presented as fact without a verifiable source — screened for explicitly at every Stage Gate's Review Process.

### 14.4 Escalation Policy

Any risk rated High/High is escalated to the Engagement Lead within 24 hours of identification and reviewed at the next standing engagement meeting regardless of normal cadence.

---

*End of Volume I. Continue to Volume II — Research & Strategy.*
