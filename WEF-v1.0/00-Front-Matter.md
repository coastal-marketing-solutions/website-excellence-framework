# WEBSITE EXCELLENCE FRAMEWORK (WEF)
## Version 1.0

### A Complete AI-Assisted Consulting Methodology for Designing, Building, Optimizing, and Scaling High-Performing Websites Across Regulated and Specialized Industries

---

## TITLE PAGE

**WEBSITE EXCELLENCE FRAMEWORK (WEF) v1.0**

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
**Manual Edition:** v1.1
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

---

## DOCUMENT CONTROL

| Field | Value |
|---|---|
| Document Title | Website Excellence Framework (WEF) |
| Document Version | 1.2 |
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

| Change ID | Date | Section(s) Affected | Description | Approved By |
|---|---|---|---|---|
| CR-001 through CR-004 | 2026-06-18 – 2026-07-20 | Various | See `/MWEF-v1.0/00-Front-Matter.md` for the full pre-re-architecture revision history | Methodology Governance Board |
| CR-005 | 2026-07-23 | Entire framework | Re-architected the single-industry MWEF manual into WEF v1.0: an industry-agnostic Core Methodology (Governance, Research, SEO & Architecture, UX & Conversion, Design, Development, QA & Optimization, AI Workflows, Reusable Templates) plus a pluggable Industry Module library. Rationale: the firm's engagements span mortgage lending and real estate today, with law firm, medical, home services, financial advisor, and SaaS clients anticipated; a monolithic mortgage-specific manual forced re-authoring 80-90% of the methodology for every new vertical. Original MWEF v1.0 preserved unmodified at `/MWEF-v1.0/`. | Methodology Governance Board |
| CR-006 | 2026-07-23 | Industry Modules | Added six new Industry Modules (Real Estate, Law Firm, Medical/Healthcare, Home Services, Financial Advisor, SaaS) and the Mortgage Lending module (carried forward from MWEF), each built to the new fixed Module Template (see Front Matter Section 6.4 below and Industry Modules front matter). | Methodology Governance Board |
| CR-007 | 2026-07-23 | Industry Modules | Added the **Cash Home Buyer / Real Estate Investor Module** via the New Module Development Process (Governance, Sec. 13.6), using the Real Estate Module as the structural starting point. Authored from direct research into Carrot.com's published SEO methodology (the dominant platform vendor in this vertical), the live site structure of bluewavehomebuyers.com, competitor archetypes (national franchise, algorithmic iBuyer, local independent, comparison aggregator), and current state wholesaling/equitable-interest disclosure law, TCPA telemarketing rules, and FTC/state Attorney General predatory-practice enforcement history against this business model. | Methodology Governance Board |
| CR-008 | 2026-07-23 | Industry Modules | Added the **Distressed Property Advocate Module** (licensed agents/brokers representing distressed residential and commercial owners via traditional listing/sale) via the New Module Development Process, using the Real Estate Module as the structural starting point and cross-referencing the Cash Home Buyer Module. Grounded in research on the Chavez Group's dual-site model (keepmyproperty.com education microsite + chavezgroupusa.com full-service brokerage) and state foreclosure-consultant statute/unauthorized-practice-of-law research. | Methodology Governance Board |
| CR-009 | 2026-07-23 | Industry Modules | Added the **Expired Listing Specialist (Commercial-Weighted) Module** via the New Module Development Process, using the Real Estate Module as the structural starting point, re-weighted toward commercial asset classes per user instruction. Grounded in research on the mgrcre.com reference model (diagnostic-first positioning, BOV methodology, LoopNet/Crexi/CoStar channel strategy, property management cross-sell) and NAR Code of Ethics non-disparagement research. | Methodology Governance Board |
| CR-010 | 2026-07-23 | Industry Modules | Added the **Probate Real Estate Investor Module** via the New Module Development Process, using the Cash Home Buyer Module as the structural starting point. Grounded in CPRES body-of-knowledge research and detailed research on probate court-confirmation/overbid mechanics and executor fiduciary-duty/surcharge risk, which materially shape this Module's compliance and trust-signal requirements beyond the general Cash Home Buyer Module's probate persona. | Methodology Governance Board |
| CR-011 | 2026-07-23 | Industry Modules | Added the **Real Estate Development Module** via the New Module Development Process, using the Expired Listing Specialist (Commercial-Weighted) Module as the structural starting point. Intentionally scoped broad, per user instruction, as a foundation for future asset-class-specific niche sub-modules. Grounded in research on investment-manager website-structure patterns, SEC Regulation D Rule 506(b)/506(c) general solicitation requirements, the Interstate Land Sales Full Disclosure Act, Fair Housing Act design-and-construction requirements, and pre-construction rendering disclaimer conventions. | Methodology Governance Board |
| CR-012 | 2026-07-23 | Industry Modules | Added the **Commercial Real Estate (Investment Sales, Owner Representation/Leasing & Property Management) Module** via the New Module Development Process, using the Expired Listing Specialist (Commercial-Weighted) Module as the structural starting point, covering retail, office, multifamily, industrial, and land per user instruction. Grounded in research on property-management broker-licensing/trust-accounting requirements and dual-agency/designated-agency disclosure standards — the latter two with no prior analog anywhere in the library. | Methodology Governance Board |
| CR-013 | 2026-07-23 | Industry Modules | Refined the **Real Estate Development Module** to v1.1 per Governance, Sec. 9.5 (Module Gap / cross-pollination), applying findings from CR-012's research to build-to-hold developers: property-management trust-accounting requirements, sharpened Fair Housing leasing/advertising obligations, CAM reconciliation accuracy, a "dirt to disposition" positioning extension, and BOV/CCIM/SIOR trust signals. No structural/template change. | Methodology Governance Board |
| CR-014 | 2026-07-28 | Governance (new Sec. 15, Sec. 13.4.1), Design (Sec. 18, Sec. 14), Development (Sec. 11), AI Workflows (new Sec. 3.4) | Added the **Engagement Retrospective Register** (Governance, Sec. 15) as a permanent firm-level mechanism for converting single-engagement pitfalls into cross-industry methodology safeguards, seeded with four entries (RETRO-001 through RETRO-004) extracted from the framework's first full engagement (mortgage lending, run substantially before this Core + Modules architecture existed): AI design-tool execution deferred past launch under schedule pressure; Development authorized to begin on a partially-designed sitemap; technology stack drifting from the Charter without a formal amendment; and a structural defect propagating site-wide due to hand-duplicated markup instead of reusable components. Hardened Design's SG7.5 Exit Criteria and Development's SG8 Checklist to require 100% sitemap design coverage before build begins; strengthened Governance Sec. 13.4 into an active, per-layer technology-stack intake confirmation (Sec. 13.4.1) instead of a silent default; and named concrete AI design/build tools (Claude Design, and the SG10 multi-platform roster) explicitly in AI Workflows Sec. 3.4, where previously only generic model *roles* were described. | Methodology Governance Board |

| CR-015 | 2026-07-28 | Governance (Sec. 1.7, Sec. 3.2, Sec. 15.4 RETRO-005), Design (Sec. 4–5, new Appendix — Design Constraints Package Specification), Development (SG10.5 retitled + new Sec. 10.5-Alt, Prompt 10.5.1), AI Workflows (Sec. 3.4), new Core Methodology file 10 (AI Agent Services) | Added the **Design Constraints Package** as a required SG7 deliverable and required loaded-context input for every downstream AI design tool and AI coding agent (Claude Design, OpenAI Design, Figma, Canva, Adobe Express/Firefly on the design side; Claude Code, Codex, Manus, GitHub Copilot on the build side), explicitly stack-agnostic so it works identically whether the confirmed platform is the WordPress/GeneratePress default or a Charter-specified alternative (e.g., custom PHP/HTML) — see Governance RETRO-005. Added **Stage Gate 10.5-Alt** mapping the default-stack WordPress Implementation workflow onto an alternative-stack build step-by-step. Added a new, optional **Service Add-On Module** axis (Governance, Sec. 1.7), orthogonal to Industry Modules, and its first library entry: **AI Agent Services** (Core Methodology, file 10) — Stage Gate 12A (Chat AI Agent-as-a-Service, delivered on the website) and Stage Gate 12B (Voice AI Agent-as-a-Service, delivered over telephony, explicitly outside the website Stage Gate spine given its distinct TCPA/telemarketing-consent regulatory exposure). | Methodology Governance Board |

| CR-016 | 2026-07-28 | New `/Component-Library/` (6 files), Design (Sec. 3–4, new Sec. 9.5, Workflow step 1, Sec. 11 Checklist, Sec. 14 Common Mistakes, Design Constraints Package Appendix), AI Workflows (Sec. 3.4) | Established the **Component Library** as a firm-wide, cross-industry registry of reusable UI components — the direct answer to repeated difficulty getting AI coding agents to translate an AI-designed mockup into an existing WordPress/GeneratePress site cleanly. Seeded with 16 components (Button, Icon, Badge, Tag, Input, Select, Checkbox, Radio, Switch, TrustBar, ComplianceFooter, LeadCaptureForm, Card, LocationCard, OfferingCard, StaffBioCard) generalized from the framework's first full engagement's actual Claude Design export. Design Sec. 9.5 now requires checking this registry before any component is designed net-new; a New Component Promotion Process (Component Library Index) feeds newly-built, genuinely reusable components back into the registry at SG11.5 close-out — the same compounding-value loop as Module Gap Escalation (Governance, Sec. 9.5) applied to UI components instead of vertical knowledge. | Methodology Governance Board |

| CR-017 | 2026-07-28 | Governance (new Sec. 13.4.2, Sec. 13.4.1 extended), Development (new Sec. 10.5-Sync, Prompt 10.5.3, Sec. 11 Checklist), Design (Design Constraints Package Appendix, AI Tool Handoff Instructions), Component Library Index (Platform Implementation Note(s) field), all Component Library category files (field rename) | Two additions responding directly to a recurring AI-assisted-editing failure mode: (1) **Sec. 13.4.2 (Portability)** makes explicit that the default GeneratePress/GenerateBlocks stack is a starting recommendation, not lock-in — the durable asset is the Component Library's token/interface layer, and each entry's Platform Implementation Note field is explicitly designed to hold more than one stack's implementation over time, renamed accordingly across the registry. (2) **Sec. 13.4.1 extended + Development Sec. 10.5-Sync** establish a tiered Content & Code Access confirmation (SSH+WP-CLI preferred, REST API fallback, browser-GUI automation as last resort) and a required **Content-as-Files Sync Pipeline** that treats git-tracked page-content files as the source of truth and the live database as a synced build artifact — directly reversing the database-drift failure mode in Governance RETRO-005, and giving AI coding agents (Claude Code, Codex, Manus, GitHub Copilot) a file-based workflow to work in rather than only browser automation. | Methodology Governance Board |

| CR-018 | 2026-08-04 | Governance (new Sec. 13.4.3) | Added **Sec. 13.4.3 (Maximize a Selected Plugin's Advanced/Licensed Capabilities)**, generalizing a pattern first observed with GeneratePress Premium's advanced modules (Elements, Hooks, Sections) into a standing principle: once a plugin clears the "native functionality preferred" bar and is licensed as part of the confirmed stack, use its advanced/paid-tier capabilities as fully as its goals allow rather than configuring it at the free-tier minimum, and document which advanced features were actually enabled in the Decision Register so the pattern compounds across future engagements — the same reuse discipline Sec. 13.4.2 already applies to the Component Library's token/interface layer, now applied to plugin capability, not just plugin choice. Prompted directly by a live engagement (mortgage lending vertical) discovering Rank Math SEO PRO already licensed and active, with several PRO-tier features (Schema Templates, Content AI, SEO Analyzer, AI Link Genius) not yet being used to configure the site. Does not relax Sec. 13.5's compliance-review gate for anything an advanced feature publishes live. | Methodology Governance Board |

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
