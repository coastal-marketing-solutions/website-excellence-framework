# WEBSITE EXCELLENCE FRAMEWORK (WEF)
## Version 1.4 (Working Draft)

### A Complete AI-Assisted Consulting Methodology for Designing, Building, Optimizing, and Scaling High-Performing Websites Across Regulated and Specialized Industries

---

## TITLE PAGE

**WEBSITE EXCELLENCE FRAMEWORK (WEF) v1.4 — Working Draft**

*A Complete AI-Assisted Consulting Methodology for Designing, Building, Optimizing, and Scaling High-Performing Websites Across Regulated and Specialized Industries*

Published by: WEF Methodology Group
Edition: First Edition
Format: Enterprise Consulting Operations Manual
Classification: Internal Use — Licensed Consulting Practice Methodology

---

## COPYRIGHT PAGE

© 2026 WEF Methodology Group. Licensed under Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0).

This manual is published openly to invite review, critique, and contribution from working practitioners across the industries it covers. You are free to share, copy, redistribute, and adapt this material in any medium or format, and to build upon it, **provided that**: (1) you give appropriate credit to the WEF Methodology Group, link to the license, and indicate if changes were made; and (2) you do not use the material, or any adaptation of it, for commercial purposes (including but not limited to selling it, repackaging it as a paid product, or using it to deliver paid consulting engagements) without the publisher's prior written permission. Full license text: https://creativecommons.org/licenses/by-nc/4.0/

This manual is a methodology and operations framework intended for use by consulting practices, internal digital strategy teams, and independent practitioners in the design, construction, and optimization of professional and commercial websites across multiple industries. Trademarks, product names, and platform names referenced in this manual (including but not limited to WordPress, GeneratePress, GenerateBlocks, Rank Math, LiteSpeed Cache, Cloudflare, Google Analytics, Google Search Console, Google Tag Manager, and Microsoft Clarity) are the property of their respective owners. Reference to these products does not imply endorsement by, or affiliation with, their owners.

This document does not constitute legal, financial, medical, or regulatory compliance advice for any industry. Several of the verticals addressed by this framework's Industry Modules — including mortgage lending, real estate, law, medicine, and financial advisory services — are subject to significant federal, state, and professional-licensing regulation. Each Industry Module identifies the regulatory frameworks typically applicable to that vertical (e.g., TILA/RESPA/ECOA/SAFE Act for mortgage lending; HIPAA for medical/healthcare; state bar advertising rules for law firms; state real estate commission rules for real estate; SEC/FINRA/state securities rules for financial advisors and real estate development capital-raising), but this identification is a starting orientation for the consulting team, not a substitute for the client's own qualified legal and compliance counsel. All content, calculators, disclosures, and advertising language produced under this methodology must be reviewed and approved by the client's qualified compliance function prior to publication, per the Governance discipline (Core Methodology, Governance) and each applicable Industry Module.

**Document Classification:** Public — Open Methodology, Contributions Welcome
**Manual Edition:** v1.4 (Working Draft)
**Publication Date:** 2026-07-23
**Repository:** See the repository README for how to propose corrections, flag Module Gaps, or suggest new Industry Modules.

---

## VERSION HISTORY

| Version | Date | Author/Owner | Summary of Changes |
|---|---|---|---|
| 0.1 (Draft) | 2026-05-02 | WEF Methodology Group | Initial outline drafted as a single-industry (mortgage lending) framework |
| 0.9 (Release Candidate) | 2026-07-05 | WEF Methodology Group | Full mortgage-specific draft assembled; internal review pass completed |
| 1.0 (Mortgage-Only Release) | 2026-07-23 (AM) | WEF Methodology Group | Published as *Mortgage Website Excellence Framework (MWEF) v1.0* — a single-industry manual. Preserved unmodified at `/MWEF-v1.0/` as a standalone historical reference and as the source material for the Mortgage Lending Industry Module below. |
| 1.0 (Core + Modules Architecture) | 2026-07-23 (PM) | WEF Methodology Group | **Re-architected same-day** into the current structure: an industry-agnostic Core Methodology plus a library of pluggable Industry Modules. This is a structural change per the Governance discipline's versioning rules (a "major" change), but is designated v1.0 of the newly renamed *Website Excellence Framework* product line rather than v2.0 of MWEF, since the deliverable itself — a reusable, multi-industry consulting framework — did not exist in this form before. Six new industry modules added (Real Estate, Law Firm, Medical/Healthcare, Home Services, Financial Advisor, SaaS) alongside the carried-forward Mortgage Lending module. |
| 1.1 | 2026-07-30 | WEF Methodology Group (Change Proposal, Governance Sec. 13.2) | Adopted the ICM ("context management") methodology's context-navigation-layer concepts, first applied to a live engagement KB before being proposed back into the framework (Governance Sec. 9.5's Module-refinement pattern, applied here to the Core Methodology itself). Additive, minor-version change: (1) Governance Sec. 5.2 Knowledge Base folder structure gained an explicit CLAUDE.md/CONTEXT.md navigation layer and a `_config`/`_references` consolidation of engagement-wide governance documents (new Sec. 5.2.1); (2) AI Workflows gained a Context Window Loading Discipline subsection (Sec. 2.5) governing *when* the existing Five-Layer Context Package's layers load, plus two new Common Mistakes entries (Sec. 3.3); (3) Reusable Templates gained a new Context Navigation Templates section (Sec. 21) with CLAUDE.md, CONTEXT.md, stage-contract, naming-convention, and multi-client practice-root templates. Does not alter any Stage Gate's exit criteria, persona library, compliance landscape, or prior engagement approvals — no re-approval of completed Stage Gate work is required. |
| 1.2 | 2026-08-04 | WEF Methodology Group (Change Proposal, Governance Sec. 13.2) | Added Governance Sec. 13.4.3 (see CR-018): once a Default Technology Stack plugin (or Charter-approved alternative) is licensed, use its advanced/paid-tier capabilities fully rather than at the free-tier minimum, and log which advanced features were enabled in the Decision Register — extending Sec. 13.4.2's reuse discipline from "which plugin" to "how much of the plugin." Additive, minor-version change; does not alter any Stage Gate's exit criteria, prior engagement approvals, or the Default Technology Stack table itself. |
| 1.3 | 2026-08-13 | WEF Methodology Group (Change Proposal, Governance Sec. 13.2) | Added three Engagement Retrospective Register entries (see CR-019) extracted from a live engagement's production-outage-and-recovery incident: RETRO-006 (a git deploy-target misconfiguration wiped an entire live site twice, undetected until the first deploy fired), RETRO-007 (a browser-based virtualized code editor silently duplicated a large full-file push, and the same-technique DOM-text verification failed to catch it), and RETRO-008 (analytics tags were QA-signed-off as "firing correctly" without verifying they were consent-gated, running unconsented tracking in production for days). Hardened Development Sec. 10.5 with a mandatory pre-first-push deploy-target verification checklist item and a hardened Sec. 10.5-Sync Tier 3 sub-rule against paste-simulation into virtualized editors (preferring an editor's native state API or a platform's file-upload path, with exact-length/marker-occurrence verification only); added a Best Practices entry on not compounding mistakes mid-incident (don't re-run a failed automated repair tool, never restore an unverified backup). Hardened QA & Optimization Sec. 11 Checklist and Sec. 14 Common Mistakes to require tags be verified consent-gated, not merely firing. Additive, minor-version change; does not alter any Stage Gate's exit criteria or prior engagement approvals. |
| 1.4 (Working Draft) | 2026-08-13 | WEF Methodology Group (Change Proposal, Governance Sec. 13.2) | Cross-industry operating-discipline expansion informed by live mortgage and real-estate engagements. Research adds evidence provenance/freshness, freshness classes, and a Digital Estate & Access Map; Governance adds capability ownership, collision prevention, portability, access/environment boundaries, scoped/version-bound approval, separate paid-entitlement/site-assignment verification, and third-party custom-domain/origin controls; SEO adds evidence-led query-page prioritization, selected-page/local-landing quality gates, contextual internal linking, link-audit classification, recurring visibility operations, and representative post-release indexing verification; UX adds conversion measurement and operational handoff; Development adds rendered-output ownership checks, all-post-type content sync, deterministic publication/import/rollback safety, an authoring-source/verified-mirror distinction for GUI-only work, environment-qualified hierarchy preflight, proportional WordPress maintenance, and custom-domain cutover testing; QA adds meaningful-event, real destination-receipt, fresh-read, consent, entitlement, freshness, alternate-route, geographic-data integrity, and post-release monitoring; AI Workflows adds verification packets; Reusable Templates makes every control executable and adds an optional Video-to-Website Deployment Brief; the Component Library strengthens LocationCard interaction/accessibility; the Real Estate Module adds a governed school-information boundary. Plugin scores are explicitly diagnostic rather than ranking/business KPIs, capability ownership overrides indiscriminate feature activation, and vertical facts remain in Industry Modules. **Working draft — pending formal Governance Board approval before release as an adopted minor version.** |

---

## DOCUMENT CONTROL

| Field | Value |
|---|---|
| Document Title | Website Excellence Framework (WEF) |
| Document Version | 1.4 (Working Draft) |
| Document Owner | Head of Methodology / Managing Partner |
| Review Cycle | Semiannual (January / July), upon material platform change, or upon addition of a new Industry Module |
| Approval Authority | Methodology Governance Board (see Core Methodology, Governance, Section 13) |
| Distribution | Engagement Leads, Consultants, Designers, Developers, SEO Specialists, Copywriters, QA Leads, Project Managers |
| Storage Location of Record | Firm Knowledge Base — `/methodology/wef/v1.0/` |
| Companion Files | Core Methodology (10 files), Industry Modules (13 files, extensible), Component Library (6 files, extensible), Front/Back Matter |
| Predecessor | *Mortgage Website Excellence Framework (MWEF) v1.0*, preserved intact at `/MWEF-v1.0/` |
| Relationship to Predecessor | MWEF v1.0 is not superseded or deleted. It remains a complete, standalone, mortgage-specific manual and is the canonical source for the Mortgage Lending Industry Module's content. WEF v1.0 is architecturally distinct: it separates what MWEF bundled together into a reusable Core plus a swappable Module. |

---

## REVISION LOG (Change Control)

This Revision Log is a thin index. Each row's full "what changed and why" prose lives in
`_change-requests/CR-0NN.md` (see `_change-requests/CONTEXT.md` for the frontmatter schema and
the rule that the next free CR number is `max(id) + 1` read from those files). Module-scoped
changes are also logged in the affected Module's own front matter.

| Change ID | Date | Section(s) Affected | One-line summary | Status | Link |
|---|---|---|---|---|---|
| CR-001 – CR-004 | 2026-06-18 – 2026-07-20 | Various | Pre-re-architecture revision history — see `/MWEF-v1.0/00-Front-Matter.md` | Adopted | — |
| CR-005 | 2026-07-23 | Entire framework | Re-architected single-industry MWEF into WEF v1.0 — industry-agnostic Core + pluggable Industry Modules | Adopted | [CR-005](_change-requests/CR-005.md) |
| CR-006 | 2026-07-23 | Industry Modules | Seeded the Module library — six new Modules + Mortgage Lending carried forward, all to the fixed Module Template | Adopted | [CR-006](_change-requests/CR-006.md) |
| CR-007 | 2026-07-23 | Industry Modules | Added the Cash Home Buyer / Real Estate Investor Module | Adopted | [CR-007](_change-requests/CR-007.md) |
| CR-008 | 2026-07-23 | Industry Modules | Added the Distressed Property Advocate Module | Adopted | [CR-008](_change-requests/CR-008.md) |
| CR-009 | 2026-07-23 | Industry Modules | Added the Expired Listing Specialist (Commercial-Weighted) Module | Adopted | [CR-009](_change-requests/CR-009.md) |
| CR-010 | 2026-07-23 | Industry Modules | Added the Probate Real Estate Investor Module | Adopted | [CR-010](_change-requests/CR-010.md) |
| CR-011 | 2026-07-23 | Industry Modules | Added the Real Estate Development Module | Adopted | [CR-011](_change-requests/CR-011.md) |
| CR-012 | 2026-07-23 | Industry Modules | Added the Commercial Real Estate Module (investment sales, owner rep/leasing, property management) | Adopted | [CR-012](_change-requests/CR-012.md) |
| CR-013 | 2026-07-23 | Industry Modules | Refined the Real Estate Development Module to v1.1 (cross-pollination from CR-012) | Adopted | [CR-013](_change-requests/CR-013.md) |
| CR-014 | 2026-07-28 | Governance, Design, Development, AI Workflows | Added the Engagement Retrospective Register (Sec. 15), seeded RETRO-001–004; 100% sitemap-coverage gates | Adopted | [CR-014](_change-requests/CR-014.md) |
| CR-015 | 2026-07-28 | Governance, Design, Development, AI Workflows, new file 10 | Design Constraints Package as required SG7 deliverable; Service Add-On axis + AI Agent Services (SG12A/12B) | Adopted | [CR-015](_change-requests/CR-015.md) |
| CR-016 | 2026-07-28 | Component Library (new), Design, AI Workflows | Established the Component Library — cross-industry registry of reusable UI components, seeded with 16 | Adopted | [CR-016](_change-requests/CR-016.md) |
| CR-017 | 2026-07-28 | Governance, Development, Design, Component Library | Stack portability (token/interface layer is the durable asset) + Content-as-Files Sync Pipeline | Adopted | [CR-017](_change-requests/CR-017.md) |
| CR-018 | 2026-08-04 | Governance (Sec. 13.4.3) | Maximize a licensed plugin's advanced/paid-tier capabilities; log enabled features in the Decision Register | Adopted | [CR-018](_change-requests/CR-018.md) |
| CR-019 | 2026-08-13 | Governance, Development, QA & Optimization | RETRO-006/007/008 from a production-outage incident — deploy-target preflight, virtualized-editor guidance, consent-gating QA | Adopted | [CR-019](_change-requests/CR-019.md) |
| CR-020 | 2026-08-13 | Governance, Research, SEO, UX, Development, QA, AI Workflows, Reusable Templates, Component Library, RE Module, Back Matter | Cross-industry operating-discipline expansion; RETRO-009–012 | Working Draft — pending Board | [CR-020](_change-requests/CR-020.md) |
| CR-021 | 2026-08-14 | Governance, SEO & Architecture, Development | RETRO-013–016 — enumerated page counts, sitemap-category coverage checks, two-approval fact/publish rule | Adopted | [CR-021](_change-requests/CR-021.md) |
| CR-022 | 2026-08-14 | Governance (Sec. 15.6), Reusable Templates, `new-engagement` + `wef-sync` skills | Cross-Engagement Contribution Pipeline; RETRO-017 | Adopted | [CR-022](_change-requests/CR-022.md) |
| CR-023 | 2026-08-15 | Governance, Design | RETRO-018 — rendered mockup required as a standalone SG7/SG7.5 checklist line | Working Draft — pending Board | [CR-023](_change-requests/CR-023.md) |
| CR-024 | 2026-08-20 | Governance, Development | WPConsent as a standing default-stack layer; RETRO-019/020 (plugin state-store + batch-score reliability) | Adopted | [CR-024](_change-requests/CR-024.md) |
| CR-025 | 2026-08-20 | SEO & Architecture, Reusable Templates | Master Content Workbook (Sec. 8.4); SG4/SG5 file-naming reconciled to `Title-Case-No-Version.md` in `output/` | Adopted | [CR-025](_change-requests/CR-025.md) |
| CR-026 | 2026-08-20 | Governance, Development | Design Fidelity Reviewer standing role with remediation authority; RETRO-021 | Adopted | [CR-026](_change-requests/CR-026.md) |
| CR-027 | 2026-09-07 | Governance, Research, UX, Design, Development, QA, AI Agent Services, Reusable Templates, skills, repo-root `AGENTS.md` | Systematised client intake (`intake` skill); ICM alignment F-1–F-7; file-naming sweep | Adopted | [CR-027](_change-requests/CR-027.md) |
| CR-028 | 2026-09-07 | Front Matter, new `_change-requests/`, Governance Sec. 15.6, `wef-sync`, Multi-Context Protocol, `AGENTS.md` | Migrated CR bodies to `_change-requests/CR-0NN.md`; thinned this log to an index (F-4) | Adopted | [CR-028](_change-requests/CR-028.md) |
| CR-029 | 2026-09-07 | `01-Governance.md` → `01-governance/` (15 section files + `CONTEXT.md` router); stub kept; `README.md`, `AGENTS.md`, skills | Split the Governance chapter for selective loading (F-8, Board Option C); reference sweep deferred | Working Draft — pending Board | [CR-029](_change-requests/CR-029.md) |

All future changes to this manual must be logged in this table and versioned per the Governance discipline's Change Control policy.

---

## TABLE OF CONTENTS

**FRONT MATTER**
Title Page · Copyright Page · Version History · Document Control · Revision Log · Table of Contents

**INTRODUCTION**
1. Executive Summary
2. Purpose of This Manual
3. Intended Audience
4. Methodology Architecture (Core + Modules)
5. Consulting Philosophy
6. How to Use This Manual
7. Governing Principles

**CORE METHODOLOGY** (`/Core-Methodology/`) — industry-agnostic; applies to every engagement regardless of vertical

1. Governance — project initialization, organization, charter, decision register, knowledge base, blueprint, backlog, documentation standards, project memory, version control, firm-level QA, governance policies, risk management, **Module Integration Standard**
2. Research — Stage Gates 1–3: Discovery & Market Research, Competitive Intelligence, Strategic Direction
3. SEO & Architecture — Stage Gates 4–5: Information Architecture, SEO Blueprint
4. UX & Conversion — Stage Gate 6: UX & Conversion Design
5. Design — Stage Gates 7–7.5: Visual Design System, Prototype Validation (Design Tournament, Benchmark Validation, Future-Proofing Review, Executive Approval)
6. Development — Stage Gates 8–10.5: Content Specification, Copywriting, AI Build Package, WordPress Implementation Blueprint
7. QA & Optimization — Stage Gates 11–11.5: Quality Assurance, Post-Launch Growth Program
8. AI Workflows — LLM Handoff Protocol, multi-model collaboration patterns, prompt library index, AI output verification standards
9. Reusable Templates — the fillable template library referenced throughout the Core Methodology
10. AI Agent Services — Stage Gates 12A–12B: Chat AI Agent-as-a-Service, Voice AI Agent-as-a-Service (**optional add-on discipline** — only active when named in the Project Charter, Governance Sec. 1.7; not part of the mandatory Stage Gate spine)

**INDUSTRY MODULES** (`/Industry-Modules/`) — vertical-specific; exactly one is selected per engagement in the Project Charter, with the option to blend two where a client spans categories

- Mortgage Lending Module
- Real Estate Module
- Law Firm Module
- Medical / Healthcare Module
- Home Services Module
- Financial Advisor Module
- SaaS Module
- Cash Home Buyer / Real Estate Investor Module
- Distressed Property Advocate Module
- Expired Listing Specialist (Commercial-Weighted) Module
- Probate Real Estate Investor Module
- Real Estate Development Module
- Commercial Real Estate (Investment Sales, Owner Representation/Leasing & Property Management) Module
- *(extensible — see Governance, Section 13.6, for the New Module Development Process)*

**COMPONENT LIBRARY** (`/Component-Library/`) — cross-industry registry of reusable, already-built UI components; checked before any component is designed net-new (Design, Sec. 9.5)

- 00 — Index & Governance (registry schema, reuse-first rule, New Component Promotion Process)
- Category: Core (Button, Icon)
- Category: Feedback (Badge, Tag)
- Category: Forms (Input, Select, Checkbox, Radio, Switch)
- Category: Marketing & Trust (TrustBar, ComplianceFooter, LeadCaptureForm)
- Category: Surfaces (Card, LocationCard, OfferingCard, StaffBioCard)
- *(extensible — see Component Library Index, "New Component Promotion Process")*

**BACK MATTER**
Glossary · References · Index · Appendices

---

## INTRODUCTION

### 1. Executive Summary

Every regulated or reputation-sensitive industry — mortgage lending, real estate, law, medicine, home services, financial advisory, and increasingly B2B SaaS — is undergoing the same structural shift in how prospective customers discover, evaluate, and select a provider. Search behavior has moved from keyword lookup toward conversational, AI-mediated discovery; trust signals have shifted from brand recognition toward transparency, demonstrated expertise, and genuine user experience; and Google's ranking systems increasingly reward topical authority and entity clarity over keyword density and link volume alone.

Most professional-services and regulated-industry websites in production today were built to satisfy a marketing checklist rather than to win in this new environment. Worse, most consulting methodologies for building these sites are re-invented from scratch for every new client vertical — a mortgage lending engagement and a law firm engagement end up sharing almost no reusable process, even though 80–90% of what makes a website excellent (governance discipline, research rigor, information architecture, SEO structure, UX conversion mechanics, design system quality, build discipline, QA rigor, and AI-assisted production workflow) is identical across industries. Only the specifics — who the audience is, what regulations apply, what keywords and content model matter, what trust signals a buyer needs to see — actually change.

The **Website Excellence Framework (WEF)** is built on that insight. It separates a single, rigorous **Core Methodology** — the eleven-plus Stage Gates, governance system, and AI collaboration protocol that apply to any engagement — from a growing library of **Industry Modules**, each of which supplies exactly the vertical-specific inputs (personas, compliance landscape, keyword and content strategy, trust signals, page/content model) that the Core Methodology's Stage Gates consume at defined injection points. A consulting team runs the same eleven Stage Gates whether the client is a mortgage lender, a real estate brokerage, a personal injury law firm, or a SaaS company — they simply load a different Industry Module at engagement initialization.

### 2. Purpose of This Manual

This manual is the single source of truth for how WEF engagements are run, across any supported industry. Its purpose is to:

- Provide a **stage-gated Core Methodology** that is identical across every engagement, eliminating the need to reinvent process for each new vertical.
- Provide a **pluggable Industry Module system** so that vertical-specific expertise (compliance, personas, content model, trust signals) is captured once, reused across every future engagement in that vertical, and improved cumulatively over time.
- Define **roles and responsibilities** so any consultant, designer, developer, SEO specialist, copywriter, QA analyst, or project manager can step into an engagement — in any industry — and know exactly what is expected of them.
- Establish a **governance and documentation system** that keeps every engagement auditable and reusable, and that makes explicit, at every Stage Gate, exactly where industry-specific knowledge must be substituted in.
- Codify an **LLM Handoff Protocol** so multiple AI models can collaborate on a single engagement — carrying both the Core Methodology's structure and the active Industry Module's specifics — without losing context or introducing contradictions.
- Provide a **template and prompt library** extensive enough that most deliverables can be produced by following the manual directly.
- Set a **quality bar** — performance, accessibility, SEO, conversion, brand, scalability, maintainability, platform compatibility, and AI implementation readiness — that applies universally, regardless of industry.

### 3. Intended Audience

| Audience | How This Manual Serves Them |
|---|---|
| Engagement Leads / Managing Consultants | Full Core Methodology, governance, Stage Gate sequencing, Module selection and blending, client management |
| Human Consultants | Stage Gate playbooks (Core) plus the active engagement's Industry Module |
| AI Models (Research, Design, Build, QA) | Structured prompts, handoff protocol, Knowledge Base schema, Module-specific context injection |
| Designers | Core Design discipline, scoring matrices, GeneratePress/GenerateBlocks guidance, plus Module trust-signal/visual-convention notes |
| Developers | Core Development discipline, WordPress Implementation Blueprint, plus Module-specific integration notes |
| SEO Specialists | Core SEO & Architecture discipline plus Module keyword/schema strategy |
| Copywriters | Core Development (Copywriting) discipline, voice/tone standards, plus Module compliance guardrails and content model |
| QA Teams | Core QA & Optimization discipline plus Module-specific compliance QA checklist |
| Project Managers | Core Governance discipline, backlog, risk management, meeting templates |
| Future Engagement Teams, Any Industry | The Core Methodology (reused unchanged) plus whichever Industry Module — existing or newly authored — matches the client |

### 4. Methodology Architecture (Core + Modules)

```
                    WEBSITE EXCELLENCE FRAMEWORK (WEF) v1.0
                                     │
                ┌────────────────────┴────────────────────┐
                │                                            │
        CORE METHODOLOGY                          INDUSTRY MODULES
        (industry-agnostic;                       (vertical-specific;
         reused on every engagement)                exactly one selected
                │                                    per engagement,
                │                                    or two blended)
   ┌────────────┼─────────────┐                              │
   │            │             │                ┌─────────────┼──────────────┐
Governance   Research   SEO & Architecture      │             │              │
   │            │             │            Mortgage      Real Estate     Law Firm
   UX &       Design    Development         Lending        Module         Module
Conversion       │             │              Module           │              │
   │        QA & Optimization  │                │          Medical /     Home Services
AI Workflows     │        Reusable            Financial    Healthcare       Module
                 │        Templates           Advisor        Module
                 │                             Module           │
                 └─────────────┬───────────────────┴──────────SaaS
                                │                              Module
                     Every Stage Gate in Core
                     has defined MODULE INJECTION
                     POINTS where the active
                     Industry Module's personas,
                     compliance landscape, keyword
                     strategy, trust signals, and
                     content model are substituted in.
```

The Core Methodology defines **what happens and in what order** (the Stage Gates, their roles, their exit criteria, their quality standard). The active Industry Module defines **who the audience is, what rules apply, what they need to see, and what the site must contain**. An engagement is fully specified only when both are combined: Core Methodology + one (or a documented blend of two) Industry Module(s), named explicitly in the Project Charter.

This is the same architectural principle used inside modern software: a stable core with a plugin interface. Each Stage Gate chapter in the Core Methodology explicitly marks its **Module Injection Points** — the exact places where the module's content must be pulled in — so that a consultant or AI model never has to guess where general methodology ends and vertical specifics begin.

### 5. Consulting Philosophy

WEF is built on five non-negotiable principles, unchanged from the framework's mortgage-lending origin because they are true regardless of industry:

1. **Evidence before opinion.** Every strategic recommendation traces back to a documented research finding, competitive data point, or performance metric — never to house style alone.
2. **Customer trust is the product.** Nearly every industry this framework serves sells something the buyer cannot easily verify themselves in advance — a loan, a legal outcome, a medical relationship, a home repair, a financial plan, a piece of software they haven't yet used. Every design, content, and technical decision is evaluated against whether it increases or decreases that trust.
3. **Compliance and professional standards are a design constraint, not an afterthought.** Whatever the applicable regulatory or professional-conduct framework — set by the active Industry Module — it is treated as a first-class architectural requirement from Stage Gate 1 onward, not a Stage Gate 11 cleanup pass.
4. **Speed and structure are ranking factors and conversion factors simultaneously.** Performance-first and SEO-first are not competing priorities in this methodology — they are the same priority.
5. **Documentation is deliverable.** An engagement that produces a beautiful website but no reusable knowledge base — and no refinement to its Industry Module — has failed the methodology, even if the client is satisfied. Cross-engagement, cross-industry reusability is a core success metric.

### 6. How to Use This Manual

- **New engagement teams** should read this Introduction and the entire Core Methodology (all 10 files) before touching an Industry Module. Governance and the Module Integration Standard are not optional scaffolding — they are the mechanism that makes a single methodology work across every industry this firm serves. AI Agent Services (file 10) is the exception to "applies to every engagement" — read it, but it only activates when a Service Add-On is named in the Charter (Governance, Sec. 1.7).
- **Consultants entering an engagement mid-stream** should read the Project Charter (which names the active Industry Module) and Decision Register, then jump directly to the current Stage Gate chapter in the Core Methodology, with the named Industry Module open alongside it.
- **AI models** should be provided the relevant Core Stage Gate chapter, the active Industry Module, the current Master Website Blueprint, and the LLM Handoff Protocol (Core Methodology, AI Workflows) as context before being prompted to produce deliverables.
- **Specialists** (designers, developers, SEO, copywriters, QA) should treat their respective Core Methodology discipline as their primary desk reference, the active Industry Module as their vertical reference, and Reusable Templates as their template source.
- Every Stage Gate chapter follows the same fixed structure (see the Research chapter's introduction for the full 19-part template plus the Module Injection Point convention), so once a reader is oriented to one Stage Gate, all others follow the same pattern — in any industry.
- **To onboard a new industry not yet covered** (e.g., dentistry, veterinary services, insurance brokerage), do not modify the Core Methodology. Instead, author a new Industry Module using the fixed Module Template (Industry Modules front matter) and the New Module Development Process (Governance, Section 13.6).

### 7. Governing Principles for Manual Maintenance

This manual is itself governed by the policies described in the Governance discipline. In brief: changes to the **Core Methodology** are proposed via Change Request, reviewed by the Methodology Governance Board, versioned, and logged in the Revision Log above; a **Core** change requires a higher approval bar than adding or refining an **Industry Module**, since Core changes affect every engagement in every industry simultaneously, while a Module change affects only that vertical. No individual consultant may unilaterally alter Core Stage Gate exit criteria, quality standards, or the default technology stack without Governance Board approval; Industry Module refinements based on engagement learnings are expected and encouraged, subject to the same Change Request discipline at the Module level.

---

*Continue to Core Methodology — Governance.*
