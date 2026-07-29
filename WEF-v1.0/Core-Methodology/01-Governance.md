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

---

## 5. Knowledge Base

### 5.1 Purpose

The Knowledge Base (KB) is the single persistent store of every artifact, research finding, deliverable, and decision produced during the engagement. It is what makes WEF engagements AI-collaborable and cross-industry-reusable: any model can be given a defined KB path plus the active Industry Module and immediately have full context for the current state of the engagement.

### 5.2 Standard Folder Structure

```
/clients/{client-name}/wef/
├── 00-charter/
│   ├── project-charter.md            (names active Industry Module(s))
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

Note that this per-client structure is unchanged from a single-industry framework — the industry-specific knowledge lives in the framework-level `/Industry-Modules/` library, referenced from the Charter, not duplicated into every client's KB folder.

### 5.3 Knowledge Base Governance Rules

1. Every Stage Gate deliverable is saved to its numbered folder — never to a personal drive, chat log, or email attachment only.
2. File naming follows the Documentation Standard (Section 8.3).
3. The Knowledge Base is read-access for the full team and client sponsor; write-access is role-gated per the RACI in Section 2.3.
4. No deliverable is considered final until it exists in the Knowledge Base in its approved form — a Slack message or verbal approval is not sufficient.

### 5.4 AI Access Pattern

When briefing an AI model for a Stage Gate task, the standard context package is: (1) Project Charter, (2) Decision Register (filtered to relevant Stage Gates), (3) Master Website Blueprint (current state), (4) the specific Core Methodology Stage Gate chapter, (5) the relevant section(s) of the **active Industry Module**, (6) any Stage Gate inputs listed in that chapter. This is formalized in the LLM Handoff Protocol (AI Workflows chapter).

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

### 13.5 Compliance & Professional Standards Governance

WEF consultants and AI models never issue final compliance, legal, medical, or financial sign-off in any industry. Every piece of content touching claims, disclosures, licensing statements, or advertising language subject to the active Industry Module's Regulatory & Compliance Landscape must pass through the client's named Compliance/Standards Liaison before publication, formalized as a mandatory review step in Development (Stage Gates 8–9) and QA & Optimization (Stage Gate 11).

### 13.6 New Module Development Process

When an engagement requires an industry not yet covered by an existing Industry Module:

1. Engagement Lead identifies the closest existing module as a structural starting point.
2. A draft module is authored to the fixed Module Template (Industry Modules front matter) — Persona Library, Regulatory & Compliance Landscape, Competitive Landscape Notes, Positioning & Messaging Patterns, Information Architecture Patterns, SEO & Keyword Strategy, Trust Signal Requirements, Content Model & Page Types, Stage Gate Injection Map, Module-Specific Prompt Library Additions.
3. The draft is used on the current engagement in parallel with active development, clearly marked "Draft — v0.x" in the Knowledge Base and Decision Register.
4. At engagement close, the module is finalized, submitted to the Methodology Governance Board as a Change Request, and — once approved — added to the permanent Industry Modules library at v1.0 for reuse on future engagements in that vertical.

### 13.7 Module Currency Review

Because regulatory and professional-standards requirements change over time (and faster in some industries — e.g., mortgage lending, medical/healthcare, financial advisory — than others), every Industry Module's Regulatory & Compliance Landscape section is reviewed at minimum annually, and immediately upon any team member flagging a known regulatory change, regardless of the semiannual Core Methodology review cycle.

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

### 15.5 Filing New Entries

Any team member may propose a new Retrospective entry at any point in an engagement, not only at SG11.5 close-out. Proposed entries are reviewed by the Methodology Governance Board on the same cadence as Change Requests (Sec. 13.2) and, once adopted, are cited by ID in whichever Core Methodology or Industry Module section they informed.

---

*End of Governance. Continue to Core Methodology — Research.*
