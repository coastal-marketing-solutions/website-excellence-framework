# CORE METHODOLOGY — GOVERNANCE

*Website Excellence Framework (WEF) v1.0*

---

## Chapter Introduction

Governance is the operating system on which every other Core Methodology discipline and every Industry Module runs. It is entirely industry-agnostic: the same Project Charter structure, Decision Register, Knowledge Base, and LLM Handoff Protocol apply whether the engagement is a mortgage lender, a law firm, or a SaaS company. What changes between industries is never *how* governance works — only the specific content (personas, compliance requirements, keyword strategy) that flows through it, supplied by the active Industry Module. Read this chapter in full before beginning any engagement work, regardless of vertical.

---

## 1. Project Initialization

### 1.1 Purpose

Project Initialization converts a signed Statement of Work (SOW) into a running engagement with an assigned team, a provisioned Knowledge Base, a **selected Industry Module**, and a scheduled first Stage Gate. It exists to prevent the single most common cause of engagement failure: starting substantive work before the team agrees on scope, roles, module selection, and success criteria.

### 1.2 Initialization Workflow

```
 SOW Signed
     │
     ▼
 [1] Engagement Lead assigned ──────► Engagement Lead confirms scope vs. SOW
     │
     ▼
 [2] Industry Module selected ───────► Confirm against Charter industry
     │                                  classification (Sec. 1.5); note if a
     │                                  blend of two modules is required
     ▼
 [3] Core team staffed (see Sec. 2) ─► Roles assigned; specialists booked
     │
     ▼
 [4] Knowledge Base provisioned ─────► Folder structure created (Sec. 5),
     │                                  Industry Module linked
     ▼
 [5] Project Charter drafted ────────► See Sec. 3; signed by client + Engagement Lead
     │
     ▼
 [6] Kickoff Meeting held ───────────► Template: Reusable Templates, Meeting Templates
     │
     ▼
 [7] Master Website Blueprint seeded ► Skeleton document created (Sec. 6)
     │
     ▼
 [8] Stage Gate 1 scheduled ─────────► Engagement formally begins
```

### 1.3 Initialization Checklist

- [ ] SOW reviewed by Engagement Lead against WEF standard scope boundaries
- [ ] Client industry classified and the corresponding Industry Module selected (or a documented two-module blend agreed — see Sec. 1.5)
- [ ] Client primary contact and decision authority (Section 3.4) confirmed in writing
- [ ] Core team assigned and calendars blocked for Stage Gates 1–3 at minimum
- [ ] Knowledge Base workspace created at `/clients/{client-name}/wef/`
- [ ] Project Charter drafted and routed for signature, naming the active Industry Module(s)
- [ ] Kickoff meeting scheduled within 5 business days of SOW signature
- [ ] Compliance/regulatory contact identified, if the active Industry Module flags the client's vertical as regulated
- [ ] Technology stack confirmed or default stack (Governance, Sec. 13.4) accepted
- [ ] Digital Estate & Access Map identifies the owner, operational custodian, access tier, recovery path, and environment boundary for every production system; no secret values are stored in the Knowledge Base
- [ ] Billing/scope guardrails communicated to full team

### 1.4 Industry Module Selection

At initialization, the Engagement Lead selects the Industry Module that matches the client's business from the current library (Industry Modules front matter). Selection is a Decision Register entry (`DEC-INIT-001`), not an informal choice — it determines which personas, compliance landscape, keyword strategy, trust signals, and content model will be consumed at every downstream Module Injection Point.

**If no existing Industry Module matches the client's vertical**, do not force-fit an adjacent module. Trigger the New Module Development Process (Section 13.6) as a parallel workstream, using the closest existing module as a starting template, and flag the schedule impact to the client.

### 1.5 Blended-Module Engagements

Some clients span two verticals (e.g., a real estate brokerage that also originates mortgages in-house, or a law firm with an embedded financial-planning practice). In these cases:

- Name a **primary** module (governs overall site architecture and positioning) and a **secondary** module (governs a defined sub-section of the site) explicitly in the Project Charter.
- Log the blend decision and its boundary (which pages/sections follow which module) as a Decision Register entry.
- Never silently merge two modules' compliance requirements — apply the stricter of the two wherever they conflict, and flag the conflict to both modules' relevant Compliance Liaison(s) for resolution.

### 1.6 Common Mistakes

- Starting Discovery interviews (Stage Gate 1) before the Project Charter is signed and the Industry Module is confirmed, resulting in scope and persona disputes later.
- Selecting an Industry Module casually or defaulting to whichever module the team last used, rather than verifying it actually matches the client's regulatory and business model.
- Failing to identify a compliance contact at initialization for a regulated vertical — this routinely causes rework in Development (Copywriting) and QA & Optimization.
- Force-fitting a client into the nearest existing module instead of triggering the New Module Development Process when the fit is genuinely poor.

### 1.7 Service Add-On Modules (Optional, Orthogonal to Industry Modules)

An **Industry Module** (Sec. 1.4) selects which vertical's rules apply — exactly one is required per engagement. A **Service Add-On Module** is a different, optional axis entirely: an additional capability the firm delivers on top of the website build, independent of vertical. Zero, one, or several may be active on a single engagement, in any combination, alongside any Industry Module.

The current Service Add-On library lives in AI Agent Services (Core Methodology, file 10):

- **Stage Gate 12A — Chat AI Agent-as-a-Service**: an AI chat agent embedded on the client's website itself.
- **Stage Gate 12B — Voice AI Agent-as-a-Service**: an AI voice agent operating over telephony, delivered independent of the website.

Unlike Industry Modules, Service Add-On Modules do not gate or get gated by the mandatory Stage Gate spine (SG1–SG11.5) — an engagement can complete its website Stage Gates and launch with a Service Add-On still in progress, not yet scoped, or never scoped at all. Name active Service Add-On(s) explicitly in the Project Charter (Sec. 3.2) the same way an Industry Module is named — an add-on delivered without a Charter entry is scope no one formally agreed to.

---

## 2. Consulting Organization

### 2.1 Purpose

Defines the standing roles used across every WEF engagement, their responsibilities, and their decision rights. These roles are identical across industries; only the subject matter they apply expertise to changes. Not every engagement staffs every role as a distinct human — smaller engagements may consolidate roles — but every responsibility below must be explicitly assigned to someone (human or AI-with-human-reviewer) before Stage Gate 1 begins.

### 2.2 Role Definitions

| Role | Primary Responsibility | Typical Stage Gate Ownership |
|---|---|---|
| **Engagement Lead** | Overall accountability for engagement outcomes, client relationship, Decision Register authority, Industry Module selection | All gates (approval) |
| **Project Manager** | Schedule, backlog, risk register, meeting cadence, cross-role coordination | All gates (operations) |
| **Research Consultant** | Market research, discovery synthesis, competitive intelligence | SG1, SG2, SG3 |
| **Strategy Consultant** | Positioning, strategic direction, business objective alignment | SG3, SG6 |
| **Information Architect** | Sitemap, content hierarchy, navigation, taxonomy | SG4 |
| **SEO Specialist** | Keyword architecture, topical maps, technical SEO, schema strategy | SG5, SG8, SG10.5, SG11.5 |
| **UX Designer** | User flows, conversion paths, wireframes | SG6, SG7 |
| **Visual Designer** | Design system, visual identity, GeneratePress/GenerateBlocks design specification | SG7, SG7.5 |
| **Copywriter** | On-page copy, calculator/tool microcopy, disclosures coordination | SG9 |
| **Developer / WordPress Implementer** | GeneratePress/GenerateBlocks build, performance, integrations | SG10, SG10.5 |
| **QA Analyst** | Functional, performance, accessibility, SEO, and compliance QA | SG11 |
| **Compliance/Standards Liaison (client-side)** | Reviews all claims, disclosures, and regulated content per the active Industry Module | SG8, SG9, SG11 (mandatory wherever the Industry Module flags the vertical as regulated) |
| **AI Orchestrator (human)** | Manages LLM Handoff Protocol, prompt quality, output verification, Module context injection | All gates |
| **Knowledge Librarian** *(optional, recommended at engagement scale — added from cross-engagement evidence)* | Files and cross-references every accepted deliverable into the Knowledge Base; audits for duplicate or contradictory entries; **performs no content judgment whatsoever** — cannot resolve a genuine contradiction, only surface it to the Engagement Lead | All gates (filing/audit only, not decision-making) |

**On the Knowledge Librarian role:** this separates *deciding what's accepted* (Engagement Lead/Project Manager, a judgment call) from *filing and auditing it correctly* (Knowledge Librarian, zero judgment authority) — two independent real-world sources converged on this same separation-of-duties pattern without coordinating: a live WEF engagement's own governance system, and an external AI-driven marketing agency's independently designed team roster. On engagements below a size threshold set in the Project Charter, this role may be folded into the Project Manager's Section 2.2 duties, but the *function* (duplicate/contradiction audits, catching e.g. the same Open Question filed twice under different IDs) should not be skipped just because it isn't staffed as a separate person.

### 2.3 RACI Summary (Engagement-Level)

| Activity | Engagement Lead | Project Manager | Specialists | Client |
|---|---|---|---|---|
| Project Charter approval (incl. Module selection) | A | R | C | A |
| Stage Gate exit sign-off | A | R | R | I (or A for SG3, SG7.5, SG11) |
| Decision Register entries | A | R | R | I |
| Compliance/standards sign-off (where applicable) | I | I | C | A |
| Go-live authorization | A | R | C | A |

*(R = Responsible, A = Accountable, C = Consulted, I = Informed)*

### 2.4 Best Practices

- Never let the Visual Designer also serve as final QA Analyst on the same engagement — independent review of design fidelity requires separation of duties.
- The Compliance/Standards Liaison must be client-side, not a firm consultant role-playing compliance; WEF firms do not issue legal, medical, financial, or other professional opinions.
- On engagements under a certain size (defined in the Project Charter), the AI Orchestrator role may be held by the Engagement Lead directly, but must still be explicitly named.

---

## 3. Project Charter

### 3.1 Purpose

The Project Charter is the foundational governance document of the engagement. It is signed before Stage Gate 1 begins and is the reference document the Decision Register, Knowledge Base, and every Stage Gate cite back to when questions of scope arise. **It is also the single document that formally names the active Industry Module(s)** — everything downstream depends on that declaration being correct and unambiguous.

### 3.2 Required Contents

| Section | Contents |
|---|---|
| Engagement Overview | Client name, industry classification, business model, service area/licensing footprint |
| **Active Industry Module(s)** | Named module(s) selected per Section 1.4–1.5; if blended, the boundary between primary and secondary module |
| **Active Service Add-On(s)** (optional) | Named per Section 1.7 (e.g., Chat AI Agent-as-a-Service, Voice AI Agent-as-a-Service), or explicitly "None" — never left blank |
| Business Objectives | Quantified goals (e.g., "increase qualified lead submissions by 35% within 6 months of launch") |
| Scope Boundaries | In-scope pages/features; explicitly out-of-scope items (e.g., CRM/practice-management system integration) |
| Technology Stack | Default WEF stack (Governance, Sec. 13.4) or client-specified alternative, with rationale if alternative |
| Regulatory/Compliance Framework | Pulled from the active Industry Module's Regulatory Landscape section, confirmed with the client's compliance contact |
| Roles & Staffing | Named individuals/AI roles per Section 2 |
| Timeline | Target dates for each Stage Gate |
| Decision Authority | Named individual(s) with final sign-off authority at each approval gate |
| Success Metrics | KPIs to be tracked post-launch (QA & Optimization, Post-Launch Growth Program) |
| Assumptions & Dependencies | E.g., "client will provide practitioner bios within 5 business days of request" |
| Change Control Process | Reference to the Change Request template |

### 3.3 Project Charter Template

See **Reusable Templates — Client Intake Templates** for the fillable Project Charter template. All fields marked "Required" must be completed before Charter signature; fields marked "Confirm at SG3" may be finalized after Strategic Direction is set.

### 3.4 Decision Authority Standard

Every Project Charter must name exactly one client-side individual as final Decision Authority for each of the following gates: Strategic Direction (SG3), Visual Design System (SG7.5 Executive Approval), and Go-Live (post SG11). Ambiguity here — "the marketing team will decide" — is a Charter defect and must be corrected before signature.

### 3.5 Common Mistakes

- Leaving Decision Authority as a committee rather than a named person, which stalls SG7.5 executive approval indefinitely.
- Naming an Industry Module in conversation but not formally in the Charter, leaving the actual module selection undocumented and unauditable.
- Failing to capture the client's true regulatory footprint (licensed states, professional jurisdictions, accreditations) accurately, which causes rework in SEO & Architecture and Development.

---

## 4. Decision Register

### 4.1 Purpose

The Decision Register is the append-only ledger of every material decision made during the engagement: what was decided, why, by whom, on what evidence, and what alternatives were rejected. It is the mechanism that lets a consultant (or AI model) joining the engagement mid-stream understand why the sitemap looks the way it does, without re-reading every prior working session — and it is identical in structure across every industry this framework serves.

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

Decisions are never deleted, only superseded. If a design decision is later reversed, a new Decision Register entry is created referencing and superseding the original — preserving full engagement history for audit and reuse.

### 4.4 When to Log a Decision

Log a Decision Register entry any time: a strategic direction is chosen among alternatives; a scope boundary is set or changed; a compliance or professional-standards interpretation is applied; a design or architecture pattern is selected over competing options; an Industry Module is selected or blended; or an AI model's recommendation is accepted, modified, or rejected by a human reviewer.

### 4.5 Bias-Scan Step for Irreversible Decisions

Any decision logged with **Reversibility: Irreversible** carries a mandatory one-line bias-scan note before it's marked final: does this decision look right because the evidence supports it, or because it's the option that was easiest to reach, confirms an existing assumption, or matches what every prior similar decision on this engagement already concluded? This is not a philosophical exercise — a real, repeated pattern in this framework's own retrospective findings is every self-generated "lessons learned" entry being marked generalizable to other industries, which is itself a plausible artifact of who's doing the generalizing rather than a property of the findings. The AI Orchestrator or Engagement Lead performs this scan; it does not require a separate named role, but it does require a written note, not a mental check.

### 4.6 Named Trigger Condition for Deferred Tradeoffs

Where a decision explicitly accepts a limitation now in exchange for a cheaper/faster path (a free-tier vendor, a launch-only workaround, a deferred feature), log the **specific future condition** that should trigger revisiting it — not just "revisit later." "Upgrade once monthly traffic exceeds the free API tier's call limit" is checkable; "revisit if it becomes a problem" is not. This is what makes a Costly-to-Reverse decision genuinely reversible in practice rather than reversible in theory but never actually reconsidered.

---

## 5. Knowledge Base

### 5.1 Purpose

The Knowledge Base (KB) is the single persistent store of every artifact, research finding, deliverable, and decision produced during the engagement. It is what makes WEF engagements AI-collaborable and cross-industry-reusable: any model can be given a defined KB path plus the active Industry Module and immediately have full context for the current state of the engagement.

### 5.2 Standard Folder Structure

```
/clients/{client-name}/wef/
├── CLAUDE.md                     (L0 — always-loaded orientation, Sec. 5.2.1)
├── CONTEXT.md                    (L1 — full Stage Gate map, Sec. 5.2.1)
├── 01-research/                  (Stage Gate 1)
│   ├── CONTEXT.md                (L2 — stage contract)
│   └── output/                   (L4 — this stage's deliverables)
├── 02-competitive/               (Stage Gate 2)
│   ├── CONTEXT.md
│   └── output/
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
│                                  (each Stage Gate folder above follows the same
│                                   CONTEXT.md + output/ pattern shown for 01/02;
│                                   create a stage's folder only when that stage
│                                   actually begins — do not scaffold ahead, Sec. 5.2.1)
├── _config/                      (L3 — engagement-specific, stable across every stage)
│   ├── project-charter.md            (names active Industry Module(s))
│   ├── decision-register.md
│   ├── compliance-constraints-log.md
│   ├── open-questions.md
│   ├── assumptions-log.md
│   └── project-backlog.md
├── _references/                  (L3 — domain reference, shared across engagements)
│   └── README.md                     (pointers to the WEF framework + active Industry Module(s))
└── blueprint/
    └── master-website-blueprint.md
```

Note that this per-client structure is unchanged in *intent* from a single-industry framework — the industry-specific knowledge lives in the framework-level `/Industry-Modules/` library, referenced from the Charter, not duplicated into every client's KB folder. What changed in this revision (Sec. 5.2.1) is the addition of an explicit navigation layer on top of the folder structure itself, and the consolidation of the engagement's cross-stage governance documents (Charter, Decision Register, and their siblings) into a single `_config/` location instead of a lone `00-charter/`.

### 5.2.1 The Context Navigation Layer (CLAUDE.md / CONTEXT.md)

The folder structure in Sec. 5.2 organizes *where* things live. It does not, on its own, tell an AI model *when* to load them or *what order* to read them in — and a large, multi-stage engagement KB left without that navigation layer tends to be read either exhaustively (wasting context budget on stages that aren't relevant to the current task) or incompletely (a model guesses which files matter and guesses wrong). This subsection formalizes a five-layer navigation discipline, adopted from the ICM ("context management") methodology (external reference material, first applied to a live WEF engagement 2026-07-30; see Change Proposal history, Sec. 13.2) and merged with the WEF-native Five-Layer Context Package already defined in AI Workflows Sec. 2.1, which it does not replace.

| Layer | File(s) | Loads | Answers |
|---|---|---|---|
| L0 | `CLAUDE.md` (KB root) | Always, every session | "Where am I? What is this engagement?" |
| L1 | `CONTEXT.md` (KB root) | On entry to the KB | "Where do I go? What's the full Stage Gate map and current stage?" |
| L2 | `CONTEXT.md` (each stage folder) | Only when working in that stage | "What does this specific Stage Gate do — purpose, inputs, outputs, exit criteria?" |
| L3 | `_config/*`, `_references/*` | Loaded selectively, per task | "What rules/decisions/framework content apply?" |
| L4 | Stage `output/*`, client-supplied source material | Loaded selectively, per task | "What am I actually working with or producing right now?" |

**Rules:**

1. `CLAUDE.md` stays under roughly one screen (WEF Best Practice: under ~800 tokens). If it grows longer, content belongs in `CONTEXT.md` or a stage's own `CONTEXT.md` instead.
2. A stage folder (and its `CONTEXT.md` + `output/`) is created **only when that Stage Gate actually begins** — per Sec. 5.2's inline note. Scaffolding all 14 stage folders in advance defeats the purpose of the layer (nothing to route to yet) and clutters the KB root.
3. `_config/` holds what's stable **across every stage** of this specific engagement (Charter, Decision Register, Compliance Constraints Log, Open Questions, Assumptions Log, Project Backlog). `_references/` holds what's stable **across engagements** (pointers into the framework-level `/Industry-Modules/` and Core Methodology, not copies of them). Do not duplicate framework content into `_references/` — link to it.
4. Every stage's `CONTEXT.md` is a trimmed, engagement-specific instance of that Stage Gate's 19-part Core Methodology template (Research Sec. "The Fixed Stage Gate Template"), not a restatement of the whole chapter — link back to the chapter for full detail rather than copying it.
5. When a stage completes, its `CONTEXT.md` status updates to reflect completion (see the template in Reusable Templates, Sec. 21.3) and the root `CONTEXT.md`'s Stage Map table updates to name the new active stage — this is a Knowledge Base Governance Rule (Sec. 5.3), not optional housekeeping.

**Rationale for adoption:** the same context-window-degradation failure mode this layer prevents — a model given too much undifferentiated context blending reference material with source material, or re-deriving decisions already settled — is exactly what AI Workflows Sec. 5 (Verification Standards) and Sec. 3.3 (Common Mistakes) already warn against from the opposite direction (verifying bad output after the fact, rather than structuring the KB to make bad output less likely in the first place). This is a structural, not incremental, complement to that existing discipline.

### 5.3 Knowledge Base Governance Rules

1. Every Stage Gate deliverable is saved to its stage's `output/` folder — never to a personal drive, chat log, or email attachment only.
2. File naming follows the Documentation Standard (Section 8.3) and the Naming Convention Standard (Reusable Templates, Sec. 21.4).
3. The Knowledge Base is read-access for the full team and client sponsor; write-access is role-gated per the RACI in Section 2.3.
4. No deliverable is considered final until it exists in the Knowledge Base in its approved form — a Slack message or verbal approval is not sufficient.
5. The root `CLAUDE.md` and `CONTEXT.md` are living documents (Sec. 5.2.1) — update them at every Stage Gate transition, not just at KB creation. A navigation layer that describes a stale state is worse than no navigation layer, because it actively misdirects.

### 5.4 AI Access Pattern

When briefing an AI model for a Stage Gate task, the standard context package is: (1) Project Charter, (2) Decision Register (filtered to relevant Stage Gates), (3) Master Website Blueprint (current state), (4) the specific Core Methodology Stage Gate chapter, (5) the relevant section(s) of the **active Industry Module**, (6) any Stage Gate inputs listed in that chapter. This is formalized in the LLM Handoff Protocol (AI Workflows chapter), and — as of Sec. 5.2.1 — routed through the KB's own CLAUDE.md/CONTEXT.md navigation layer rather than assembled from scratch by a human at every handoff.

---

## 6. Master Website Blueprint

### 6.1 Purpose

The Master Website Blueprint (MWB) is the single living document that aggregates the *current, approved state* of every architectural, design, and content decision about the website — as distinct from the Decision Register, which is a historical log. If the Decision Register is the "why," the Blueprint is the "what, right now."

### 6.2 Blueprint Sections

| Section | Populated At | Contents |
|---|---|---|
| Business Context | SG1–SG3 | Objectives, audience segments (from active Industry Module personas), positioning |
| Sitemap & IA | SG4 | Full page hierarchy, URL structure |
| SEO Architecture | SG5 | Keyword map, topical clusters, schema plan |
| UX Flows | SG6 | Primary conversion paths, wireframe references |
| Design System | SG7–SG7.5 | Approved visual system, component library |
| Content Inventory | SG8–SG9 | Page-by-page content specs and approved copy |
| Technical Build Spec | SG10–SG10.5 | GeneratePress/GenerateBlocks implementation record |
| QA Status | SG11 | Outstanding issues, sign-off record |
| Growth Program | SG11.5 | KPIs, experiment log, optimization roadmap |

### 6.3 Blueprint Update Discipline

Every Stage Gate chapter in the Core Methodology ends with a "Blueprint Updates" subsection specifying exactly what must be written into the MWB before the gate can close. The Blueprint is never updated informally — updates happen only as part of a Stage Gate exit.

### 6.4 Blueprint as AI Context Anchor

The current MWB is the primary grounding document for any AI model asked to produce work on the engagement. A model prompted without both the current MWB and the active Industry Module in context is operating blind and its output must be treated as draft-only pending reconciliation.

---

## 7. Project Backlog

### 7.1 Purpose

The Project Backlog tracks discrete units of work below the Stage Gate level — tasks, open questions, content items pending, dependencies on the client — so that the Project Manager has a single place to assess engagement health at any moment. Identical in structure across every industry.

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

Consistent documentation is what allows deliverables to move between human consultants and AI models — and between engagements in entirely different industries — without translation loss. All WEF deliverables follow the standards below.

### 8.2 Formatting Standards

- Markdown as the canonical authoring format for all strategy, research, and specification documents.
- Headings follow strict hierarchy (H1 document title, H2 major section, H3 subsection); no skipped levels.
- Tables used for any structured comparison, rubric, or schema — never prose paragraphs describing tabular data.
- Every deliverable begins with a metadata block: Client, Active Industry Module(s), Stage Gate, Author (human or AI model + reviewer), Date, Version, Status.

### 8.3 File Naming Convention

`{stage-gate-number}-{deliverable-short-name}-v{version}.md`

Example: `05-seo-topical-map-v1.md`, `07-design-system-spec-v2.md`

### 8.4 Versioning Within Documents

Draft versions are tracked as v0.x; the first client- or Engagement-Lead-approved version becomes v1.0; subsequent approved revisions increment the minor or major version per Section 11.

### 8.5 Common Mistakes

- Producing deliverables as unstructured chat transcripts instead of formatted Knowledge Base documents.
- Mixing draft and approved content in the same file without a status marker, causing downstream gates to build on unapproved assumptions.
- Omitting the Active Industry Module field from a deliverable's metadata block, making it ambiguous which module's requirements the document was built against.

---

## 9. Module Integration Standard

### 9.1 Purpose

This section is the mechanism that makes the Core + Modules architecture actually function. It defines, precisely, how an Industry Module's content enters a Core Stage Gate, and the discipline required to keep the boundary between "universal methodology" and "vertical-specific knowledge" clean over time.

### 9.2 The Module Injection Point Convention

Every Stage Gate chapter in the Core Methodology (Research, SEO & Architecture, UX & Conversion, Design, Development, QA & Optimization) contains one or more explicit **Module Injection Point** callouts, in this form:

> **Module Injection Point:** This gate consumes [specific Industry Module section] in place of generic guidance. Load the active Industry Module's [Section Name] before running this gate's workflow.

A Stage Gate is never executed by substituting improvised, ad hoc industry knowledge for a real Module Injection Point. If the active Industry Module does not yet cover something a Stage Gate needs, that gap is logged as a backlog item against the Module (Section 9.5), not silently patched inside the client engagement with no trace.

### 9.3 Standard Module Injection Map

| Core Stage Gate | Module Section(s) Injected |
|---|---|
| SG1 — Discovery & Market Research | Persona Library, Regulatory & Compliance Landscape (seed) |
| SG2 — Competitive Intelligence | Competitive Landscape Notes (typical competitor archetypes for the vertical) |
| SG3 — Strategic Direction | Positioning & Messaging Patterns |
| SG4 — Information Architecture | Information Architecture Patterns (typical sitemap/page types) |
| SG5 — SEO Blueprint | SEO & Keyword Strategy, Schema recommendations |
| SG6 — UX & Conversion | Trust Signal Requirements, industry-typical calculators/tools |
| SG7 / SG7.5 — Design | Trust Signal Requirements (visual treatment), industry visual conventions |
| SG8 / SG9 — Content Spec & Copywriting | Content Model & Page Types, Regulatory & Compliance Landscape (full) |
| SG10 / SG10.5 — Build | Any module-specific integration notes (e.g., practice-management or CRM system patterns) |
| SG11 — QA | Regulatory & Compliance Landscape (final QA checklist) |
| SG11.5 — Post-Launch Growth | Persona Library (validation against real data), Content Model (expansion) |

### 9.4 Handling Blended-Module Engagements

Where two modules are active (Section 1.5), apply both modules' relevant sections at each injection point, using the primary/secondary boundary defined in the Project Charter to determine which module governs which pages/sections. Where the two modules' compliance requirements conflict, the stricter requirement governs by default, with the conflict logged as a Decision Register entry and escalated to both Compliance/Standards Liaisons.

### 9.5 Module Gap Escalation

If a Stage Gate's Module Injection Point cannot be filled because the active Industry Module lacks the needed content, the AI Orchestrator or Engagement Lead logs a Module Gap (using the Issue Log structure in Reusable Templates) against the Module itself, not just the client engagement. Once resolved for the current client, the resolution is proposed back into the Industry Module via Change Request (Section 13.2) so the next engagement in that vertical benefits — this is the mechanism by which the Module library compounds in value over time.

### 9.6 Common Mistakes

- Treating Module Injection Points as optional reading rather than a required input — this is how mortgage-specific assumptions quietly leak into a law firm engagement, or vice versa.
- Resolving a Module Gap for one client and never feeding the learning back into the Module itself, forcing the same gap to be rediscovered on the next engagement in that vertical.
- Blending modules informally without documenting the primary/secondary boundary, leaving later team members unable to determine which rules applied to which pages.

---

## 10. Project Memory

### 10.1 Purpose

Project Memory is a rolling, human-and-AI-readable summary of engagement state, distinct from both the Decision Register (full history) and the Blueprint (current architectural state). It exists to answer the question "what is the current status and what should I know before I do anything today?" in under two minutes of reading.

### 10.2 Project Memory Contents

- Active Industry Module(s) and any blend boundary
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

Ensures that every deliverable, the Blueprint, each Industry Module, and this manual itself can be traced to a specific, unambiguous version at any point in time.

### 11.2 Versioning Scheme

WEF uses semantic-style versioning for engagement deliverables and for Industry Modules alike:

- **Major version** (v1 → v2): Structural or strategic change requiring re-approval (e.g., a sitemap restructure after SG4 was already approved; or, at the Module level, a change to a module's core persona set or compliance landscape).
- **Minor version** (v1.0 → v1.1): Material content or design refinement within an approved structure.
- **Patch** (v1.1 → v1.1.1): Copy edits, typo fixes, non-substantive corrections.

### 11.3 Approval Gate for Version Increments

Any major version increment requires a new Decision Register entry explaining why the previously approved version is being revised, and re-triggers the relevant Stage Gate's Review Process before the new version can be marked "Approved." At the Module level, a major version increment requires Methodology Governance Board approval (Section 13.1).

### 11.4 This Manual's Own Versioning

Governed identically — see Front Matter Version History for how the Core Methodology and Industry Modules are versioned, released, and (in the case of the July 2026 re-architecture) how a structural change was handled without invalidating the prior single-industry manual.

---

## 12. Quality Assurance (Firm-Level)

### 12.1 Purpose

Distinct from Stage Gate 11 (project-level QA of the website itself), Firm-Level QA governs the quality of the *engagement's methodology execution* — are Stage Gates being run correctly, are deliverables meeting the manual's standards, is documentation discipline being maintained, and is the active Industry Module being consumed correctly at every injection point.

### 12.2 The Eight-Dimension Quality Standard

Every recommendation or deliverable produced anywhere in a WEF engagement, in any industry, must be evaluated against all eight dimensions before it is considered complete:

| Dimension | Guiding Question |
|---|---|
| Performance | Does this decision help the site load fast and respond instantly? |
| Accessibility | Can a visitor using assistive technology use this without friction? |
| SEO | Does this strengthen topical authority, entity clarity, and technical crawlability? |
| Conversion | Does this reduce prospective-customer friction and hesitation toward a qualified lead or desired action? |
| Brand | Is this consistent with the client's approved positioning and visual identity? |
| Scalability | Will this still work cleanly when the site grows to 5x its current page count? |
| Maintainability | Can the client's own team (or a future consultant) maintain this without the original author? |
| WordPress/GeneratePress/GenerateBlocks Compatibility & AI Implementation Readiness | Can this be built cleanly on the default stack, and is the spec precise enough for an AI build model to implement without guessing? |

### 12.3 Firm-Level QA Cadence

- Spot audit of one active engagement's Knowledge Base per month by someone outside the engagement team, including a check that Module Injection Points were actually used rather than improvised.
- Full methodology compliance audit at engagement close, feeding both the Post-Launch Growth Program retrospective and, in aggregate, this manual's semiannual review — and specifically feeding any Module Gaps discovered back into the relevant Industry Module.

---

## 13. Governance Policies

### 13.1 Methodology Governance Board

A standing body (minimum 3 senior consultants) responsible for approving changes to the Core Methodology, approving new or revised Industry Modules, adjudicating disputes about Stage Gate exit criteria, and maintaining the default technology stack decision.

### 13.2 Change Proposal Process

1. Any team member may submit a Change Request against the Core Methodology or against a specific Industry Module.
2. The Governance Board reviews within 10 business days (Core changes) or 5 business days (Module changes, given their narrower blast radius).
3. Approved changes are logged in the Revision Log (Front Matter for Core; the Module's own front matter for Module changes) and released as a new version per Section 11.
4. Rejected changes are logged with rationale for future reference.

### 13.3 Engagement-Level Governance

Within a single engagement, the Engagement Lead holds equivalent authority to the Governance Board for engagement-specific interpretation questions, but may not override the Core Methodology's Stage Gate exit criteria, quality standards, default technology stack, or the active Industry Module's compliance requirements without Governance Board sign-off logged as a Decision Register entry tagged `GOVERNANCE-EXCEPTION`.

### 13.4 Default Technology Stack Policy

Unless the Project Charter specifies an alternative, this stack applies regardless of industry:

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

### 13.4.1 Active Intake Confirmation (not a silent default)

This stack is a **starting recommendation**, not an assumption the client is deemed to have accepted by not objecting. At Project Initialization (Sec. 1.2, step 5), the Engagement Lead must walk the client through the stack **layer by layer** and obtain an explicit choice for each — "use the WEF default" is a valid, first-class answer, but it must be *selected*, not defaulted into. Record the confirmed choice for every layer (Hosting, CMS, Theme Framework, Page Building, SEO Plugin, Caching, CDN, Analytics, etc.) in the Charter's Technology Stack section, even where every answer is "WEF default." This closes the gap where a stack choice made mid-engagement (a hosting-tier change, a plugin swap) drifts from what the Charter says without anyone treating it as a decision worth logging (see Retrospective RETRO-003, Sec. 15.4). Any change to a previously confirmed layer, at any point in the engagement, is logged as a Decision Register entry at the moment it happens — not reconstructed later from what actually shipped.

**A second, distinct layer must also be confirmed at intake: Content & Code Access Tier** — *how* AI tools and consultants will actually push changes to this specific site, independent of which CMS/theme was chosen. This determines the mechanism Development (Sec. 06, SG10.5) uses for the Content-as-Files Sync Pipeline:

| Tier | Mechanism | Availability | Use For |
|---|---|---|---|
| **1 — Preferred** | SSH + WP-CLI (or the confirmed stack's CLI equivalent) | Requires the host to provide shell access — confirm per specific hosting plan/tier, never assumed. Not guaranteed on entry-level shared hosting even within the same host brand | Full content-as-files export/import, theme file deploy, cache/plugin management — the most reliable, scriptable, diffable path |
| **2 — Fallback** | Platform REST API with an application-level credential (e.g., WordPress Application Passwords) | Available on nearly every modern WP host over HTTPS alone, no shell required | Pushing page/post content and metadata from git-tracked files when Tier 1 is unavailable |
| **3 — Last Resort** | Browser/GUI automation of the platform's native editor | Always available, but the least reliable — see Governance, Sec. 15.4 (RETRO-005) for why this tier alone caused real drift and rework on this framework's first engagement | Only when Tiers 1–2 are both unavailable, or a change genuinely requires visual/WYSIWYG verification the other tiers can't provide |

Confirm and record the available tier(s) for the confirmed host at Project Initialization, the same as any other stack layer — this is not knowable in the abstract from "we use Hostinger," since access varies by specific plan. Default to the highest tier actually available; never default to Tier 3 by omission just because no one checked whether Tier 1 or 2 was possible.

### 13.4.2 Portability — the Default Stack Does Not Create Lock-In

Recommending GeneratePress/GenerateBlocks as the default (Sec. 13.4) is a starting-point convenience, not a commitment that locks every future engagement to this theme framework. The durable, reusable asset this methodology builds is the **Component Library**'s token system and component interfaces (`/Component-Library/`, Design Sec. 9.5) — colors, spacing, typography scales, and component contracts (props/variants/behavior), all defined independent of any theme. GeneratePress Global Styles and GenerateBlocks patterns are **one implementation of those tokens**, not the tokens themselves. Each Component Library entry's "Platform Implementation Note" field is explicitly designed to hold more than one stack's implementation over time — a GeneratePress note today does not preclude adding a Shopify, Webflow, or custom-PHP/HTML implementation note for the same component later, once an engagement actually builds one. Switching a future engagement to a different theme or stack means writing a new Platform Implementation Note against the existing token/interface spec — it does not mean redesigning the Component Library or the Design Constraints Package's token layer from scratch. This is the same portability discipline Sec. 13.4.1's Content & Code Access Tier and Development's Sec. 10.5-Alt (WordPress Implementation Blueprint) already assume — the default stack is a recommendation with a documented off-ramp, not a dependency.

### 13.4.3 Maximize a Selected Plugin's Advanced/Licensed Capabilities — Once Chosen, Use It Fully

The Default Technology Stack (Sec. 13.4) and the standing "native functionality preferred, plugin dependencies minimized" discipline remain the baseline: don't add a plugin to solve something native WordPress/GeneratePress/GenerateBlocks already does cleanly. But once a plugin has cleared that bar and been licensed as part of the confirmed stack — GeneratePress Premium, GenerateBlocks Pro, Rank Math (SEO Plugin default, Sec. 13.4), or any Charter-approved alternative — the engagement should use that plugin's advanced/paid-tier capabilities as fully as its stated goals allow, not just the minimum feature needed for the immediate task. The licensing cost is already sunk once the plugin is selected; configuring it at half-capacity leaves paid value on the table and produces a shallower implementation than what's actually available.

This mirrors the precedent already set for GeneratePress: engagements are expected to explore GeneratePress Premium's advanced modules (Elements, Hooks, Sections, etc.) rather than hand-building custom equivalents in a child theme when the licensed module already covers it, and to document which specific advanced features were actually exercised so the pattern is reusable on the next GeneratePress engagement rather than re-discovered from scratch each time. The same discipline now applies explicitly to Rank Math and to any future default-stack plugin:

- **Before configuring a plugin's basic settings, check whether a licensed advanced/PRO tier is already active** (Plugins → Installed Plugins shows this directly) and consult its documented feature set before assuming only the free-tier feature set is available — free-tier assumptions made without checking are a real, observed failure mode, not a hypothetical one.
- **Treat installation, activation, subscription entitlement, account connection, and site/property assignment as five separate states.** A premium add-on can be installed and active while the base plugin is connected to a free account or while the paid subscription is assigned to a different site. Verify the subscription in the vendor account, the exact connected account in the site, the site's license badge/assignment in the vendor portal, and the premium update channel. The plugin name or presence of premium menu items is not entitlement evidence.
- **Prefer the plugin's native advanced feature over a custom-code equivalent** when both exist and the plugin's advanced tier is already licensed — e.g., a PRO-tier Schema Templates feature over a hand-rolled JSON-LD block, a plugin's native Search Console/Analytics integration over a separate reporting dashboard, a plugin's built-in content/SEO analyzer over a manual audit pass — once the client has confirmed the feature is wanted and it doesn't route around Sec. 13.5's compliance gate.
- **Document which advanced features were actually turned on and why** in the engagement's Decision Register, the same discipline already required for the base plugin choice — this is what makes the usage pattern reusable across future engagements rather than a one-off. A brief "Advanced Features Enabled" note, cross-referenced from the plugin's stack-selection Decision Register entry, is sufficient; it does not need its own Stage Gate document.
- **This does not relax Sec. 13.5 (Compliance & Professional Standards Governance).** An advanced feature that changes what's published live — AI-generated schema/content suggestions, auto-populated business data, bulk title/description rewrites — still requires the same compliance review any other published content requires before going live.

Applies at Governance Board level to the Default Technology Stack (Sec. 13.4) and at Engagement Lead level to any Charter-approved alternative plugin — the principle is "use what's already been paid for, fully, and record what was used," not a mandate to enable every feature regardless of relevance to the engagement.

**Capability Ownership takes precedence over capability maximization.** “Use it fully” means use all relevant, non-conflicting value—not activate every available writer. A licensed feature may operate in read-only, monitor-only, or reporting mode, or remain disabled, when another approved system owns the production output. The Capability Ownership Matrix (Sec. 13.4.4) records that boundary.

### 13.4.4 Capability Ownership, Collision Prevention, and Tool Portability

Using a selected tool fully does not mean allowing multiple tools to publish the same output. Every engagement must maintain a **Capability Ownership Matrix** in the Plugin & Integration Configuration Record. For each externally visible or data-bearing capability, name exactly one production owner, any monitor-only consumers, the fallback behavior if the owner is disabled, and the export/migration path.

At minimum, assign ownership for: page titles and meta descriptions; canonical URLs; XML sitemaps; robots directives; structured data; redirects; translations and `hreflang`; analytics/tag injection; consent management; forms and lead storage; caching/minification; image optimization; and security/firewall rules. A theme fallback may remain available only when it is programmatically suppressed while the designated plugin is active and has been verified not to emit duplicate output.

The following rules are binding:

- **One writer, many readers.** Reporting tools may read the same Search Console, analytics, or SEO data, but only one configured owner may write each class of metadata, schema, tag, redirect, translation, or optimization output.
- **Rendered output is the truth.** An admin-screen setting is not proof. Verify the public HTML, headers, network requests, cookies, sitemap, and structured-data graph after a fresh uncached load.
- **No overlapping plugins by convenience.** Do not run two SEO, translation, analytics-injection, schema, redirect, consent, cache, or form systems with overlapping production responsibility unless a documented boundary makes their outputs mutually exclusive.
- **Fallbacks require a failure test.** If custom code or a theme supplies a fallback when a plugin is inactive, test both states and confirm there is exactly one output in each state.
- **Portability is documented before dependency.** Record where the tool stores its data, what survives deactivation, how to export it, what licensed features cease to function, and the replacement path. Never let a proprietary score or dashboard become the only record of page strategy.
- **Client/account isolation is explicit.** Connected properties, credentials, API keys, and destination accounts are verified per site; shared agency accounts never justify assuming the current property is correct.

Any collision discovered after launch is treated as a production defect, not a cosmetic configuration preference, and is entered in the Issue Log with the affected URLs and generated outputs.

### 13.4.5 Access, Credential, and Environment Boundary

Every engagement must distinguish **who owns a system**, **who operates it**, and **how a tool is authorized to reach it**. The Digital Estate & Access Map records the provider, property/site identifier, business owner, operational custodian, access status, environment (local, staging, production), recovery path, and next action; it never stores passwords, API tokens, application-password values, recovery codes, private keys, or session cookies.

The following controls apply across every stack and industry:

- Use the least-privileged account that can complete the task. Prefer a named client or service account with a scoped role over a shared administrator login.
- Record whether access is reported, verified, expired, or revoked. “The client said it works” is not the same as a verified connection to the correct property, repository, domain, analytics view, CRM, or production site.
- Separate local/development, staging, and production credentials and destinations. A staging credential must not silently point at production, and a production deploy must not target a broad document root unless that exact scope is approved and backed up.
- Store secrets only in the approved credential manager. Never paste them into chat, prompts, source files, XML/CSV imports, screenshots, issue logs, or commit messages. When a temporary application password or token is used, record its purpose and revocation owner—not its value—and revoke it when the task or engagement requires.
- Before an AI tool or browser session makes a state-changing edit, verify the visible domain/property and the intended environment. After the edit, verify persistence from a fresh read path; an in-session success message or stale DOM is not sufficient.
- Before irreversible or bulk production work, verify a recoverable backup/export, define the rollback trigger, and perform a small reversible smoke test. If the access boundary or destination cannot be verified, stop the state-changing action and escalate it as a P0/P1 risk rather than guessing.

This is an operational control, not a request to expose credentials to the consulting team. The goal is auditable authorization and correct targeting while keeping secrets out of the framework and engagement records.

### 13.4.6 Third-Party Custom Domains, Origin Boundaries, and Access Control

A custom domain connected to a hosted application is a routing layer, not proof that the application is hosted in the DNS provider's account or protected by that provider's directory controls. Before connecting any portal, studio, dashboard, booking app, knowledge base, or other third-party service to a client subdomain, document the full request path: registrar → authoritative DNS → edge/proxy → hosted application/origin → identity provider. Name which layer terminates TLS, which layer enforces authentication, and which URLs can reach the same application.

The following controls are binding:

- **Confirm authoritative DNS and record compatibility before cutover.** A hosting-panel “create subdomain” action may create an A, AAAA, ALIAS, or local document root that conflicts with the CNAME or verification record required by the hosted service. Inventory and resolve conflicts deliberately; do not stack records until one happens to work.
- **Preserve a tested fallback until DNS and TLS are verified.** Keep the provider URL available during cutover unless the security model requires otherwise, record TTL and validation records, and define rollback before changing the public hostname.
- **Apply access control at a layer every route actually traverses.** Host-level directory password protection cannot protect a CNAME that routes directly to an external SaaS origin. Use the application's identity controls or a verified edge/access layer in front of the application.
- **Test alternate-route bypass.** If the provider's original hostname, preview URL, deployment URL, or another custom hostname remains reachable, verify that it enforces equivalent authorization or intentionally document it as public. Protecting only the vanity hostname is not effective access control.
- **Verify cookie, callback, canonical, and redirect behavior on the final hostname.** Authentication callbacks, cross-site cookies, CSP/CORS, canonical URLs, analytics properties, and logout/return URLs must use the intended production domain without loops or leakage to another client property.

Record the cutover and bypass test in the Third-Party Custom Domain & Access-Control Record (Reusable Templates, Sec. 15.7). A DNS “success” badge alone is not acceptance evidence.

### 13.5 Compliance & Professional Standards Governance

WEF consultants and AI models never issue final compliance, legal, medical, or financial sign-off in any industry. Every piece of content touching claims, disclosures, licensing statements, or advertising language subject to the active Industry Module's Regulatory & Compliance Landscape must pass through the client's named Compliance/Standards Liaison before publication, formalized as a mandatory review step in Development (Stage Gates 8–9) and QA & Optimization (Stage Gate 11).

**Approval is bound to a defined artifact and revision, not to a topic, page family, campaign, or website forever.** Every clearance entry must identify the exact page/record, language, version or content hash/date, approval scope, approver, and decision. Later pages, translations, videos, posts, material claim changes, changed disclosures, new data, or substantive revisions do not inherit an earlier blanket approval unless the approver explicitly names that future scope. Define which edits are non-substantive (for example typo correction without meaning change) and which invalidate clearance. When in doubt, return the changed artifact for review; never infer that “the site was approved” clears advertising content created afterward.

**Fact-verification and publish-authorization are two separate, sequentially-required approvals for any sensitive identifying information** (a physical office address, a license-linked location, a practitioner's personal details, or comparable) — confirming that a piece of information is *accurate* is a factual question; deciding whether the client wants it *displayed publicly* is a distinct business/risk decision only the client can make. Log each as its own Decision Register entry. Do not treat a verified fact as cleared for publication until the second, separate approval is logged, and do not needlessly withhold a fact whose accuracy is already confirmed once that second approval is obtained (RETRO-015, Sec. 15.4).

**When an approver's response to a clearance log does not explicitly address items the log itself named as requiring the approver's specific confirmation, ask directly which scope was intended before logging clearance status.** A short, real-world approval reply (e.g., "move forward") is frequently more ambiguous than the log's own itemization, and silently treating it as resolving every previously-named open item risks closing out compliance flags that were never individually checked. The resulting Decision Register entry must record both the approval actually granted and, by name, which specifically-flagged items were not demonstrably individually verified, so a later audit or QA pass does not mistake a granted blanket clearance for itemized confirmation it never received (RETRO-016, Sec. 15.4).

### 13.6 New Module Development Process

When an engagement requires an industry not yet covered by an existing Industry Module:

1. Engagement Lead identifies the closest existing module as a structural starting point.
2. A draft module is authored to the fixed Module Template (Industry Modules front matter) — Persona Library, Regulatory & Compliance Landscape, Competitive Landscape Notes, Positioning & Messaging Patterns, Information Architecture Patterns, SEO & Keyword Strategy, Trust Signal Requirements, Content Model & Page Types, Stage Gate Injection Map, Module-Specific Prompt Library Additions.
3. The draft is used on the current engagement in parallel with active development, clearly marked "Draft — v0.x" in the Knowledge Base and Decision Register.
4. At engagement close, the module is finalized, submitted to the Methodology Governance Board as a Change Request, and — once approved — added to the permanent Industry Modules library at v1.0 for reuse on future engagements in that vertical.

### 13.7 Module Currency Review

Because regulatory and professional-standards requirements change over time (and faster in some industries — e.g., mortgage lending, medical/healthcare, financial advisory — than others), every Industry Module's Regulatory & Compliance Landscape section is reviewed at minimum annually, and immediately upon any team member flagging a known regulatory change, regardless of the semiannual Core Methodology review cycle.

### 13.8 Candidate Structural Extensions — Flagged, Not Adopted

Two structural ideas surfaced from external sources (a live engagement's evolved governance and an independently designed AI-driven agency's own team structure) are documented here deliberately as **candidates requiring a real decision, not silently adopted rules** — consistent with the discipline in Sec. 13.6/9.5 that a genuine structural change gets evaluated on its own merits, not folded in because it appeared somewhere plausible-sounding:

- **Pre-execution doctrine audit.** Every review mechanism currently in this framework (the Stage Gate Review Process, the Four-Question Review Standard referenced from prior engagement evidence, Stage Gate 11 QA) runs *after* a deliverable is produced. A pre-execution check — auditing a plan or draft against the Charter/Design Constraints/Compliance Constraint Log *before* work is executed, not only reviewing the finished output — could catch a doctrine violation before time is spent producing something that fails review anyway. Whether this becomes a formal, separately staffed checkpoint or stays an informal habit of the existing Engagement Lead/AI Orchestrator roles is an open question, not a default answer.
- **A formal "New Role Development Process," parallel to Sec. 13.6's New Module Development Process.** As specialist role-splitting deepens (see the Consulting Organization's optional Knowledge Librarian addition above, and the broader pattern of one generalist role splitting into several deep specialists as an engagement scales), a standing process for proposing, trialing, and promoting a new specialist role — rather than each engagement inventing its own role list ad hoc — has real appeal. It also has a real cost: more named roles means more coordination overhead for a small engagement. Do not adopt a larger role roster than a given engagement's scale actually warrants (Sec. 2.1's existing consolidation guidance still governs) without a specific decision that the added rigor is worth it for that engagement.

---

## 14. Risk Management

### 14.1 Purpose

Provides a standard mechanism for identifying, tracking, and mitigating risks to engagement success — schedule, compliance, technical, or client-relationship risks — before they become issues. Identical in structure across every industry; the specific risk content varies by the active Industry Module.

### 14.2 Risk Register Schema

| Field | Description |
|---|---|
| Risk ID | Format `RISK-{sequence}` |
| Description | What could go wrong |
| Category | Schedule / Compliance / Technical / Client Relationship / Scope / Module Gap |
| Likelihood | Low / Medium / High |
| Impact | Low / Medium / High |
| Mitigation Plan | Specific action(s) to reduce likelihood or impact |
| Owner | Who is responsible for monitoring/mitigating |
| Status | Open / Mitigated / Realized (became an Issue) / Closed |

### 14.3 Standard WEF Risk Categories to Screen For

- **Compliance/professional-standards drift**: content or design implying claims, guarantees, or outcomes without required qualifying language — specifics vary by Industry Module, but the risk category is universal.
- **Scope creep at Information Architecture/UX gates**: site structure growing beyond Charter-approved page counts without a Change Request.
- **Client bottleneck risk**: dependency on a single client stakeholder (e.g., for practitioner bios, compliance review) with no backup path.
- **Platform lock-in risk**: build decisions that would be costly to reverse if the client later leaves the default stack.
- **AI hallucination risk**: AI-produced statistics, competitor claims, or regulatory statements presented as fact without a verifiable source — screened for explicitly at every Stage Gate's Review Process.
- **Module Gap risk**: the active Industry Module lacks coverage for a situation the engagement has encountered, and the gap has not yet been escalated per Section 9.5.

### 14.4 Escalation Policy

Any risk rated High/High is escalated to the Engagement Lead within 24 hours of identification and reviewed at the next standing engagement meeting regardless of normal cadence.

---

## 15. Engagement Retrospective Register

### 15.1 Purpose

Distinct from the Risk Register (forward-looking, engagement-specific) and the per-engagement SG11.5.2 Retrospective & Methodology Learnings prompt (AI Workflows, Sec. 4), the Engagement Retrospective Register is the **firm-level, cross-engagement** ledger of generalized lessons extracted from completed or in-flight engagements. It exists so that a mistake made once, in one industry, becomes a permanent methodology safeguard rather than a private lesson known only to the consultants who lived through it. Entries here are written industry-agnostically even when the triggering engagement was vertical-specific — the whole point is that a lesson learned on a mortgage engagement must protect a law firm or SaaS engagement that comes after it.

### 15.2 Retrospective Register Schema

| Field | Description |
|---|---|
| Retro ID | Format `RETRO-{sequence}` |
| Source Engagement | Which engagement surfaced this (may be anonymized in client-facing copies) |
| What Happened | Factual description of the pitfall, stripped of vertical-specific detail |
| Generalized Risk | Why this is a risk in *any* industry, not just the one it was discovered in |
| Methodology Fix | The specific Core Methodology or Governance change made in response (cite chapter/section) |
| Status | Proposed / Adopted (with Change Request ID) / Rejected (with rationale) |

### 15.3 Governance Rule

A Retrospective entry is not optional documentation — it is the required input to any Change Request that claims to be "informed by engagement experience" (Section 13.2). A Change Request citing a lesson learned without a corresponding Retrospective Register entry is returned to the submitter for that entry to be filed first. This keeps the methodology's evolution evidence-based and auditable rather than anecdotal.

### 15.4 Adopted Retrospective Entries

The following entries were extracted from the framework's first full engagement (mortgage lending vertical, run substantially before this Core + Modules architecture existed) and generalized here so every future engagement — regardless of industry — inherits the fix rather than rediscovering the pitfall.

**RETRO-001 — AI-Assisted Visual Design Deferred Past Launch Under Schedule Pressure**
- **What Happened:** Facing a compressed pre-launch timeline, the team formally deferred the AI design-tool step (the actual rendered mockup pass, as opposed to a written visual spec) to a "Phase 6, post-launch" workstream, reasoning that pre-launch effort should stay focused on QA and cutover. The site shipped on written specs and hand-authored theme code alone; the AI-generated design pass happened days after go-live, against an already-live, already-indexed site.
- **Generalized Risk:** In any industry, treating the AI design-tool pass as a "nice to have" that can slip past launch inverts Stage Gate 7/7.5's entire purpose — design is supposed to *shape* the build, not be reverse-engineered onto one that already shipped. A post-launch design retrofit also has to work around already-live, already-crawled, sometimes already-converting copy and URLs, creating exactly the kind of conflict-resolution overhead ("don't let the redesign overwrite copy that's already been decided") that a pre-build design pass never has to solve.
- **Methodology Fix:** Design (Sec. 05, SG7/SG7.5) and Development (Sec. 06) already sequence design before content spec/copy/build by input dependency. This entry hardens that into an explicit rule: **schedule pressure is resolved by narrowing scope within a Stage Gate (fewer template variants, a smaller tournament), never by reordering Stage Gates.** Deferring SG7/7.5's actual AI-tool execution past SG7.5's Executive Approval is now a `GOVERNANCE-EXCEPTION`-tagged decision (Sec. 13.3), not a routine scope call.
- **Status:** Adopted — CR-014.

**RETRO-002 — Development Authorized to Begin on a Partially-Designed Sitemap**
- **What Happened:** With design complete for only a subset of the approved sitemap, the team authorized the build phase to proceed on the pages that *were* designed, deferring the remainder "until absolutely necessary." The gap was closed later, but only after build had already started — meaning the site was live-in-progress with some templates never having passed a real design gate at all.
- **Generalized Risk:** Any engagement under deadline pressure will be tempted to treat "design most of the site" as good enough to start building. This silently converts a hard Stage Gate into a soft one and is how a client ends up with pages that were never actually design-reviewed, in any industry.
- **Methodology Fix:** Design, SG7.5 Sec. 18 Exit Criteria and Development, SG8 Sec. 3 Inputs now explicitly require that the approved Design System & Page Templates (SG7.5) cover **100% of the SG4-approved sitemap**, not a representative sample, before Stage Gate 8 may begin. A partial-coverage exception requires a `GOVERNANCE-EXCEPTION` Decision Register entry naming exactly which pages are deferred and why.
- **Status:** Adopted — CR-014.

**RETRO-003 — Technology Stack Drifted From the Charter Without a Formal Amendment**
- **What Happened:** The engagement's actual hosting configuration diverged from what the Project Charter originally documented (a plan-tier change made operationally, not as a Charter amendment). The drift was only reconciled later, informally, in the Decision Register — not caught at the time it happened.
- **Generalized Risk:** A Charter's Technology Stack section (Sec. 3.2) is only useful if it reflects reality. In any industry, a stack decision made outside the Charter process (a hosting downgrade, a plugin swap, a theme change) that isn't immediately logged creates a silent gap between what the governing document says and what's actually running — which then has to be discovered and reconciled after the fact, at higher cost than logging it in the moment would have been.
- **Methodology Fix:** Sec. 13.4 (Default Technology Stack Policy) is strengthened below (Sec. 13.4.1) to require the stack be confirmed layer-by-layer as an active intake decision, and any mid-engagement change to any layer — not just the initial choice — triggers an immediate Decision Register entry, not a retroactive one.
- **Status:** Adopted — CR-014.

**RETRO-004 — A Duplicated Structural Defect Recurred Site-Wide Because Templates Weren't Built as Reusable Patterns**
- **What Happened:** A single structural defect (an accessibility-relevant heading-hierarchy error) was introduced once and then propagated across most of the site's pages, because those pages were built from copy-pasted, hand-edited markup rather than a single reusable template/pattern. Fixing it required a page-by-page sweep rather than a one-place correction.
- **Generalized Risk:** This is a direct, real-world confirmation of why Design's "component-based system, not one-off page designs" principle (Sec. 05, Sec. 2) and the Query Loop/Element-hooks guidance (Sec. 05 Appendices) exist. In any industry, hand-duplicated markup means every defect is a site-wide defect waiting to be discovered, and every fix is a full-site sweep instead of a single-source edit.
- **Methodology Fix:** No new rule required — the existing Design chapter guidance already prevents this when followed. This entry is preserved as evidence for *why* that guidance is non-negotiable, referenced from Design Sec. 14 (Common Mistakes).
- **Status:** Adopted — CR-014 (evidentiary entry, no new rule).

**RETRO-005 — Multiple AI Tools Edited the Same Site Without a Shared Constraint Contract**
- **What Happened:** Across the engagement, different AI tools and sessions made design and code changes to the live site without a single, standing document declaring what could and couldn't be changed. This produced repeated drift between what was live and what was tracked in version control, and required ad hoc rules invented mid-engagement (e.g., "don't let a design update overwrite copy that's already been decided") to contain damage after the fact rather than preventing it.
- **Generalized Risk:** In any industry, once more than one AI tool (or more than one session of the same tool) can touch a live site's design or code, the absence of one shared, explicit constraint document is what turns routine AI-assisted edits into drift risk. This is not specific to WordPress or to any one platform — it recurs on any stack where design output and code-generation output come from different tools or sessions.
- **Methodology Fix:** The **Design Constraints Package** (Design, Appendix — Design Constraints Package Specification) is now a required SG7 output and a required loaded-context input for every AI design tool and every AI coding agent used on the engagement, at initial build and for the life of the site post-launch (AI Workflows, Sec. 3.4). It is explicitly built to be stack-agnostic, so the same discipline holds whether the confirmed platform (Governance, Sec. 13.4.1) is the WordPress/GeneratePress default or a Charter-specified alternative such as a custom PHP/HTML build.
- **Status:** Adopted — CR-015.

**RETRO-006 — Git Deploy-Target Misconfiguration Wiped an Entire Live Site, Twice, Because the Deploy Target Was Never Verified Before the First Push**
- **What Happened:** A routine, low-risk CSS-only commit triggered a hosting provider's git auto-deploy integration and took an entire live production site down. Root cause, confirmed directly in the hosting control panel: the git integration's configured deploy target directory was set to the site's actual document root instead of the subdirectory the connected repository was actually meant to contain (a theme folder). Because the hosting provider's deploy mechanism **synced the target directory to exactly match the repository** — deleting anything present on the server but not tracked in the repo — every deploy against this misconfiguration deleted the entire CMS installation (core files, all other themes, all plugins, all media) and replaced it with just the handful of theme files the repo actually contained. This happened twice: once from the triggering push, once from a manual "Redeploy" action taken mid-incident without first fixing the underlying misconfiguration. The deploy target had almost certainly been wrong since the git integration was first connected, weeks earlier — every prior push had simply gotten lucky by not touching a file whose absence would be immediately fatal.
- **Generalized Risk:** In any industry, on any platform where a git-push-to-deploy pipeline is connected to a live site (not just WordPress, not just the framework's default stack), a misconfigured deploy target is a **latent, silent defect** — it produces zero symptoms until a deploy actually fires, at which point the blast radius is the entire site, not just the files intentionally changed. The risk is compounded because the failure mode (a raw server-level error, not an application-level one) does not obviously implicate "deploy configuration" as the cause, sending incident response down slower diagnostic paths first (content bugs, plugin conflicts, code errors) before the actual cause is found.
- **Methodology Fix:** Development, Sec. 10.5 Checklist now requires an explicit, one-time verification step — **confirm the configured deploy target directory directly in the hosting/deploy platform's own control panel, not inferred from the repository's README or from assumption** — performed before the *first* push through any newly connected or newly reconnected git deploy integration, not just at initial setup. This is now also referenced in Sec. 10.5-Sync as a precondition check, since the Content-as-Files Sync Pipeline assumes a correctly-scoped deploy target as a given.
- **Status:** Adopted — CR-019.

**RETRO-007 — A Web-Based Code Editor's Virtualized Document View Silently Duplicated File Content During a Full-File Replacement, Causing a Production Outage That Recurred Across Multiple Recovery Attempts**
- **What Happened:** An AI coding agent needed to push a large (~27KB) full-file replacement through a browser-based code-hosting platform's own in-browser code editor (a virtualized-DOM editor component, in the pattern of CodeMirror 6 or similar). Using a simulated "select all, then type/paste the new content" approach, the resulting commit showed the new content had been *inserted* alongside the old, not used to *replace* it — the editor's on-screen rendering looked correct throughout, because virtualized editors of this kind only render the currently-visible viewport window and do not reflect the true full document in DOM-accessible text at any given moment. The auto-deploying push broke the live site. **Two subsequent recovery attempts, using progressively more careful paste-simulation and DOM-text-slicing verification, both failed for the same underlying reason** — reading `.textContent` (or equivalent) from a virtualized editor's rendered DOM never reflects the true full document once that document exceeds the editor's rendered viewport, so a verification step built on it will report success even when the actual document is corrupted. The failure was only caught by inspecting the file's raw byte size and searching for repeated content markers directly on the server/filesystem (outside the editor entirely) — the file was found to contain four concatenated copies of its own content.
- **Generalized Risk:** In any industry, on any platform, whenever an AI agent (or a human) needs to push a large full-file change through a browser-based code editor built on a virtualizing rendering technique, **the editor's own on-screen state and any DOM-text-read verification performed against it are both unreliable for full-document confirmation** — this is not specific to any one code-hosting platform's editor, since virtualization is a standard technique for any web-based editor handling documents that could be arbitrarily large. Trusting either the visual result or a same-technique verification step creates a false sense of confirmation that is actively dangerous on an auto-deploying pipeline, where the corrupted content ships to production the moment it's committed.
- **Methodology Fix:** Development, Sec. 10.5-Sync's Tier 3 (GUI-only) guidance is hardened with an explicit sub-rule: **large full-file changes must never be pushed by simulating keystrokes/paste into a browser-based virtualized code editor.** Two reliable alternatives, in order of preference: (1) where the target editor exposes a genuine underlying state-management API (e.g., an editor instance's own `getValue()`/`setValue()` methods, as most non-virtualized editors like Ace provide), use that API directly rather than simulating UI interaction; (2) where the platform offers a native file-upload/replace mechanism instead of an inline editor (e.g., a "drag file to replace" upload flow), prefer that over any inline-editor path entirely, since it never routes through a virtualized rendering layer at all. Whichever path is used, verification must be **exact-length and marker-occurrence based, never a visual or partial-text spot-check**: confirm the resulting content's exact character/byte count matches the intended source exactly, and confirm any structurally-unique marker string that should appear exactly once (e.g., a file's own top-of-file declaration) actually occurs exactly once, not more.
- **Status:** Adopted — CR-019.

**RETRO-008 — Analytics/Marketing Tags Fired Unconditionally in Production for Days Before Consent Was Ever Requested, Because QA Verified the Tags Fired Correctly but Never Verified They Were Consent-Gated**
- **What Happened:** A site's analytics/tag-manager integration was verified at QA as "firing correctly" — the tag loaded, and analytics data appeared in the platform's reporting — and this was treated as sufficient. It was not: the tag had been hardcoded to fire unconditionally on every page load, with no cookie-consent mechanism gating it at all, directly contradicting the site's own Privacy Policy (which stated analytics tooling was still "pending" a decision). This ran in production, setting tracking cookies on every visitor with no consent step, for multiple days before a client question ("does this site have any tracking cookies yet?") surfaced it — not the QA process that was specifically supposed to catch it.
- **Generalized Risk:** In any industry, "verified firing correctly" is a materially different (and much weaker) claim than "verified firing only with appropriate consent." A QA checklist item that only confirms a tag *works* will pass even when the tag is a live, undisclosed privacy/compliance defect — and unlike most QA defects, every day this one goes undetected compounds real regulatory exposure (CCPA/CPRA, GDPR, and equivalent frameworks depending on the site's traffic mix) that cannot be retroactively cured for visitors already tracked before the fix ships.
- **Methodology Fix:** QA & Optimization, Sec. 11 Checklist now includes an explicit, separate line item: analytics/marketing/remarketing tags must be verified as **consent-gated**, not merely firing — confirmed by loading the site pre-consent and directly checking that no tracking cookies are set and no analytics network request fires, then confirming both a decline path (tags stay off) and an accept path (tags fire, cookies appear) work correctly. This is a compliance-category check per Sec. 14's existing rule that compliance issues are categorically P0, regardless of how minor the "just add a banner" request that surfaced it may have originally seemed.
- **Status:** Adopted — CR-019.

**RETRO-009 — A Premium Plugin Was Installed and Active While the Site Remained Assigned to the Vendor's Free Tier**
- **What Happened:** Both the base SEO plugin and its premium add-on were installed, active, and exposing premium-looking menus. Repeated attempts to “activate PRO” appeared to succeed, but the site's dashboard still identified the connected account as free. The vendor account had an active paid subscription, yet the site's connected-websites record lacked the paid-plan badge. Disconnecting the site, confirming the paid account and subscription, and explicitly reassigning the exact site to that subscription resolved the mismatch.
- **Generalized Risk:** Installation state, code activation, paid entitlement, connected identity, and per-site assignment are different control planes for many plugins and SaaS integrations. Treating any one of them as proof of the others can leave paid capability unavailable, updates unauthenticated, or the wrong client property connected while the interface looks substantially correct.
- **Methodology Fix:** Governance Sec. 13.4.3 and the Plugin & Integration Configuration Record now require separate evidence for installed/active code, subscription entitlement, connected account, site/property assignment, and premium update channel. QA verifies the vendor-side site record as well as the application-side badge.
- **Status:** Proposed — CR-020 (Working Draft).

**RETRO-010 — Earlier Page Approval Was Mistaken for Clearance of Later Advertising Content**
- **What Happened:** A regulated-industry website received page-by-page approval for a defined batch. New posts and locality pages were produced afterward; an earlier overall approval could easily have been read as permission to publish them, even though the named reviewer had never seen those exact artifacts. The engagement corrected this by keeping later posts in Draft and adding separate clearance-log rows.
- **Generalized Risk:** In any regulated or reputation-sensitive industry, approval language becomes unsafe when it is not bound to a version and scope. “Website approved” can be misapplied to later pages, translations, videos, changed claims, refreshed statistics, or imports that the approver never reviewed.
- **Methodology Fix:** Governance Sec. 13.5 and the Compliance Sign-Off Record now bind approval to an exact artifact/revision/language, define what invalidates clearance, and prohibit inherited or blanket approval unless its future scope is explicit.
- **Status:** Proposed — CR-020 (Working Draft).

**RETRO-011 — A Custom Subdomain Was Treated as Hosting and Access Control Even Though It Only Routed to an External Application**
- **What Happened:** A hosted web application was connected to a branded subdomain. Hosting-panel password protection was considered for that subdomain, but the DNS record routed directly to the external application, bypassing the host's document root entirely. The provider's original application URL also remained reachable, so protection applied only to the branded hostname would have been bypassable.
- **Generalized Risk:** DNS, hosting, TLS, application origin, and identity enforcement are independent layers. Confusing them can create conflicting DNS records, failed certificates, callback loops, or a false sense of privacy while an alternate provider URL remains public.
- **Methodology Fix:** Governance Sec. 13.4.6, Development, QA, and Reusable Templates Sec. 15.7 now require a request-path map, DNS conflict check, fallback/rollback plan, origin-level or edge-level enforcement, and alternate-route bypass testing.
- **Status:** Proposed — CR-020 (Working Draft).

**RETRO-012 — Time-Sensitive Public Guidance Was Accurate at Publication but Had No Built-In Revalidation Trigger**
- **What Happened:** Public-facing guidance relied on program availability, eligibility limits, school data, market figures, association rules, and other facts that can change. Strong pages recorded sources and a reviewed date, but without a framework-level freshness class and owner, the same content could remain indexed after its decision-useful facts expired.
- **Generalized Risk:** Accurate content becomes misleading through age, especially when search traffic continues after programs close, prices change, personnel move, laws update, or vendor terms change. A publication date alone does not assign responsibility or define when the claim must be checked again.
- **Methodology Fix:** Research's Evidence Standard, Development, QA/Post-Launch, and the Content Freshness Register now classify content as evergreen, periodic, event-bound, or volatile; assign an owner and next review/expiry trigger; and define refresh, qualify, archive, redirect, or noindex actions.
- **Status:** Proposed — CR-020 (Working Draft).

**RETRO-013 — A Total Page-Count Figure, Once Stated in Prose, Propagated Uncorrected Across Multiple Stage Gates, and the Eventual Correction Pass Introduced a New Error of the Same Kind**
- **What Happened:** A real estate engagement's sitemap totaled 82 pages across five categories (core, situation/offering, county, city, compliance/legal). An early document stated the total as "70" — apparently a stale or miscounted figure — and every subsequent Stage Gate document (a design coverage-confirmation note, a content specification, a copy-clearance log) simply repeated "70" without anyone recomputing it from the sitemap itself. When the error was finally caught and "corrected" to 81, that correction was itself wrong: the recount missed one page (a situation page that existed in the sitemap and URL standard but had never been carried into the content specification), because the correction was performed as a spot-recount rather than an exhaustive, category-by-category re-enumeration.
- **Generalized Risk:** In any industry, any total that is stated as a bare number in prose — rather than shown as an enumerated sum the reader can independently verify — will drift the moment it is copy-pasted forward into the next document, because nothing forces the next author to recompute it. Worse, a correction pass is not self-verifying: if the correction methodology is "recount and state a new number" rather than "re-enumerate every category and show the arithmetic," the correction is exactly as failure-prone as the error it's fixing, and can create false confidence that the number is now settled when it may still be wrong.
- **Methodology Fix:** Any Core Methodology or Knowledge Base document that states a total page (or comparable) count must show the enumerated breakdown it was derived from (e.g., "10 core + 14 situation + 4 county + 48 city + 6 compliance/legal = 82"), not a bare total — added as a documentation standard to SEO-Architecture Sec. 4 (Sitemap) and Development Sec. 06 (Content Specification, Copywriting, AI Build Package). Any correction to a previously-stated total must restate the full breakdown, not just the new number, so the next reader can verify it independently rather than inheriting a second unverifiable figure.
- **Status:** Adopted — CR-021.

**RETRO-014 — A Stage's Own "100% Sitemap Coverage" Claim Was Silently Wrong Because an Entire Low-Marketing-Priority Page Category Was Absent From the Coverage Check's Own Category List**
- **What Happened:** On the same engagement as RETRO-013, an earlier design stage's page-template coverage confirmation stated that its templates covered "100% of the sitemap" — but that confirmation's own category list (core, situation, county, city) never included the sitemap's 6th category, compliance/legal pages (Privacy Policy, Terms of Use, Fair Housing Statement, etc.). The omission was invisible to the coverage check itself, because the check only verified its templates against its own list, not against the sitemap's actual, complete category set. The gap survived two further Stage Gates undetected before a later stage, assembling a build manifest, discovered that no template existed for an entire class of required pages.
- **Generalized Risk:** In any industry, compliance/legal and other non-revenue-generating page categories are the pages most likely to be treated as an afterthought relative to marketing-priority content — and a coverage-confirmation check that verifies "did we cover everything on our list" rather than "did we cover everything the sitemap actually requires" will pass cleanly even when an entire category has been silently dropped, because the omission never appears as a failed checklist item, only as an absent one.
- **Methodology Fix:** Any "100% sitemap coverage confirmed" claim (Design Sec. 05 SG7.5 Exit Criteria; Development Sec. 06 SG8/SG9/SG10 Inputs and Checklists) must be checked directly against the Sitemap document's own enumerated page-type categories, not against the checking document's internally-maintained list of what it believes those categories to be — the two are allowed to diverge silently otherwise, exactly as they did here.
- **Status:** Adopted — CR-021.

**RETRO-015 — Fact-Verification and Publish-Authorization of Sensitive Identifying Information Were Conflated Into a Single Decision, Rather Than Tracked as Two**
- **What Happened:** A real estate broker's office address was independently verified as accurate against a public regulatory record early in an engagement. That verification was, correctly, not treated as automatic clearance to publish the address on the client's website — a separate Decision Register entry explicitly withheld the address from a compliance/licensing disclosure page pending the client's own, later decision on whether he wanted it displayed publicly. Weeks later, the client did authorize display, and a second, distinct Decision Register entry logged that separate approval. Because the two approvals were tracked as genuinely separate decisions from the start, neither one was skipped, assumed, or retroactively fabricated.
- **Generalized Risk:** In any regulated or reputation-sensitive vertical (a medical practice's location, a financial advisor's CRD-linked address, a therapist's office for client-safety reasons, an attorney's bar-registered address), confirming that a piece of identifying information is *accurate* is a factual question, while deciding whether the client wants it *displayed publicly* is a business/risk decision the client alone can make — conflating the two risks either publishing information the client never actually cleared for public use (because "we verified it" was mistaken for "we're allowed to publish it"), or needlessly withholding information that was already confirmed accurate and just never got a publish decision logged.
- **Methodology Fix:** Governance Sec. 13.5 (Compliance & Professional Standards Governance) now names this pattern explicitly: fact-verification and publish-authorization of any sensitive identifying information are two separate, sequentially-required approvals, each logged as its own Decision Register entry, and a verified fact must not be treated as cleared for publication until the second approval is logged.
- **Status:** Adopted — CR-021.

**RETRO-016 — An Ambiguous Blanket Approval Response Required an Explicit Disambiguating Question Before It Could Be Logged as a Specific Clearance Decision**
- **What Happened:** A Compliance/Standards Liaison was sent a clearance log itemizing 78 pages with several specific, named open items (a source citation needing his direct confirmation, two legal documents needing actual attorney review, a data-confidence flag). His reply was a two-word instruction to proceed. Read literally, that reply is ambiguous between "I have reviewed and am satisfied with everything, including the specific items you flagged" and "proceed with the engagement generally; I have not necessarily addressed each named item." Rather than guessing, the team asked him directly which reading he intended, and logged the answer — plus an explicit note that the itemized sub-flags were not individually demonstrated to have been checked even though the resulting clearance was recorded as formal, per his stated choice — as the actual Decision Register entry.
- **Generalized Risk:** In any industry, a real approver's natural-language reply to a compliance log is frequently shorter and more ambiguous than the log's own itemization, and treating a blanket "move forward" as automatically resolving every previously-named open item (rather than pausing to ask which the approver means) risks silently closing out compliance flags that were never actually individually checked.
- **Methodology Fix:** Governance Sec. 13.5 is strengthened with a companion rule to RETRO-010's artifact/revision binding: when an approver's response to a clearance log does not explicitly address items the log itself named as requiring the approver's specific confirmation, the AI Orchestrator or Engagement Lead must ask the approver directly which scope was intended before logging clearance status, and the resulting Decision Register entry must record both the approval granted and, by name, which specifically-flagged items were not demonstrably individually verified — so a later audit or QA pass does not mistake a granted blanket clearance for itemized confirmation it never received.
- **Status:** Adopted — CR-021.

### 15.5 Filing New Entries

Any team member may propose a new Retrospective entry at any point in an engagement, not only at SG11.5 close-out. Proposed entries are reviewed by the Methodology Governance Board on the same cadence as Change Requests (Sec. 13.2) and, once adopted, are cited by ID in whichever Core Methodology or Industry Module section they informed.

---

*End of Governance. Continue to Core Methodology — Research.*
