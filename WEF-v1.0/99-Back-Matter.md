# BACK MATTER

*Website Excellence Framework (WEF) v1.0*

---

## GLOSSARY

**AI Build Package** — The consolidated, implementation-ready specification produced at Stage Gate 10 that a developer or AI code-generation model uses to construct the actual website.

**AI Orchestrator** — The human role responsible for managing AI model handoffs, prompt quality, Module context injection, and verification of AI-produced output against Stage Gate standards.

**AI Workflows** — The Core Methodology chapter consolidating the LLM Handoff Protocol, multi-model collaboration patterns, the Prompt Library master index, and AI output verification standards.

**Benchmark Validation** — The Stage Gate 7.5 activity that stress-tests the winning design direction against fixed performance, accessibility, and technical SEO standards before executive approval.

**Blended-Module Engagement** — An engagement where two Industry Modules are active simultaneously, one designated primary and one secondary, per Governance Section 1.5.

**Blueprint** — See *Master Website Blueprint*.

**Compliance/Standards Constraint Log** — The running record, seeded at Stage Gate 1 and expanded through later gates, of all regulatory and professional-standards requirements applicable to the client's content and advertising, drawn from the active Industry Module.

**Component Library** — The firm-wide, cross-industry registry of reusable, already-built UI components (`/Component-Library/`), checked before any component is designed net-new (Design, Sec. 9.5). Distinct from an engagement's own component set, which is that engagement's *instance* of registry entries plus any genuinely novel components built for it.

**Content & Code Access Tier** — The confirmed mechanism (SSH+WP-CLI, REST API, or browser-GUI automation, in descending order of reliability) an engagement uses to push content and code changes to the live site, confirmed at Project Initialization alongside the rest of the Technology Stack (Governance, Sec. 13.4.1).

**Content-as-Files Sync Pipeline** — The required Development-discipline mechanism (Sec. 06, SG10.5-Sync) that treats git-tracked page-content files as the source of truth and the live CMS database as a synced build artifact, giving AI coding agents a reliable file-based workflow instead of relying on browser-GUI automation alone.

**Compliance/Standards Liaison** — The client-side individual responsible for reviewing and approving all claims, disclosures, and regulated content per the active Industry Module. WEF firms and their consultants do not issue compliance sign-off themselves, in any industry.

**AI Agent Services** — The optional, add-on Core Methodology chapter (file 10) covering Chat AI Agent-as-a-Service (Stage Gate 12A, delivered on the website) and Voice AI Agent-as-a-Service (Stage Gate 12B, delivered over telephony, outside the website Stage Gate spine). Only active when named as a Service Add-On Module in the Project Charter (Governance, Sec. 1.7).

**AI Verification Packet** — The compact evidence returned with an AI-assisted change: target, source/input, changed state, validation, fresh independent read-back, reviewer/status, unresolved risks, and rollback/recovery reference (AI Workflows, Sec. 5.4; Reusable Templates, Sec. 12.1).

**Core Methodology** — The industry-agnostic portion of WEF: Governance, Research, SEO & Architecture, UX & Conversion, Design, Development, QA & Optimization, AI Workflows, Reusable Templates, and (optionally, per engagement) AI Agent Services. The first eight apply unchanged to every engagement regardless of vertical; AI Agent Services activates only when named as a Service Add-On Module.

**Design Constraints Package** — The structured, tool-agnostic constraint set (platform target, buildability rules, machine-readable design tokens, accessibility/compliance visual constraints, and the Do-Not-Break List) produced at Stage Gate 7 and required as loaded context for every AI design tool and AI coding agent that touches the site's design or code, at initial build and for the life of the site (Design, Appendix; Governance, Sec. 15.4 RETRO-005).

**Core Web Vitals (CWV)** — Google's user-experience performance metrics: Largest Contentful Paint (LCP), Interaction to Next Paint (INP), and Cumulative Layout Shift (CLS), used throughout this manual as binding performance targets.

**Decision Authority** — The named individual(s), specified in the Project Charter, with final sign-off power at each approval gate.

**Decision Register** — The append-only ledger of every material engagement decision, its rationale, and its alternatives considered (Governance, Sec. 4).

**Design Tournament** — The Stage Gate 7.5 activity in which 2–3 fully realized design directions are scored head-to-head on a fixed rubric rather than a single design being presented for approval or rejection.

**Engagement Lead** — The consultant with overall accountability for engagement outcomes, Industry Module selection, and Decision Register authority.

**Entity SEO** — An SEO approach focused on establishing unambiguous, machine-readable identity for an organization, its people, and its offerings — the foundation of both classic knowledge-panel visibility and AI-mediated search citation.

**Exit Criteria** — The pass/fail conditions that must be met before an engagement can move from one Stage Gate to the next.

**Digital Estate & Access Map** — The secret-free Discovery inventory of domains, DNS, hosting, environments, CMS, repositories/deployments, backups, measurement systems, form/CRM destinations, ownership, access status, and recovery paths (Research, SG1; Reusable Templates, Sec. 16.5).

**Evidence & Source Register** — The cross-gate record preserving each material claim or observation's source class, provenance, date, definition, limitation, confidence, reuse, freshness, and rights status (Research, Evidence Standard; Reusable Templates, Sec. 7.8).

**Capability Ownership Matrix** — The one-writer governance record assigning exactly one production owner, readers, fallback behavior, verification method, data location, and migration path for each generated website capability (Governance, Sec. 13.4.4; Reusable Templates, Sec. 15.3).

**Access & Environment Matrix** — The secret-free record of who owns and operates each system, which environment/property is targeted, whether access was verified, how recovery/export works, and who revokes temporary access (Governance, Sec. 13.4.5; Reusable Templates, Sec. 15.5).

**Content Release & Rollback Record** — The release evidence for a CMS/API/CLI/import change: source artifact, stable identifiers, field map, scope, validation, destination read-back, cache/indexation impact, and bounded recovery path (Development, SG10.5; Reusable Templates, Sec. 15.4).

**Content Freshness Register** — The lifecycle record classifying decision-relevant public content as evergreen, periodic, event-bound, or volatile and assigning its evidence, owner, last verification, next review/expiry trigger, and stale-content disposition (Research, Evidence Standard; Reusable Templates, Sec. 7.9).

**Post-Release Indexing Verification Record** — The sampled release record connecting sitemap membership, final HTTP status, rendered canonical, robots directive, search-engine inspection result, and follow-up across each materially new template, hierarchy, locale, and risk class. Submission or inspection is diagnostic and does not guarantee indexing or ranking (QA & Optimization, SG11.5; Reusable Templates, Sec. 7.10).

**Conversion Measurement & Operational Handoff Contract** — The UX record connecting a meaningful visitor action to its event definition, consent category, no-PII rule, destination/owner, user-facing success/failure state, response expectation, and fallback path (UX & Conversion, SG6; Reusable Templates, Sec. 22.1).

**Localization & Language QA Matrix** — The per-locale verification record for human review, metadata, canonical/hreflang, consent/legal copy, forms, imagery, indexation, and last-verified status (Reusable Templates, Sec. 15.6).

**Third-Party Custom Domain & Access-Control Record** — The request-path, DNS/TLS cutover, identity-enforcement, fallback, callback/cookie/canonical, and alternate-route bypass evidence for an externally hosted application connected to a client hostname (Governance, Sec. 13.4.6; Reusable Templates, Sec. 15.7).

**Search Visibility Operations Plan** — The living SG5/SG11.5 plan connecting search and analytics baselines, query-page opportunities, meaningful events, rank tracking, link-audit triage, change annotations, and review cadence. Plugin scores are diagnostic inputs, not its KPIs.

**Future-Proofing Review** — The Stage Gate 7.5 activity evaluating whether the approved design system will scale cleanly to a defined future growth scenario, informed by the active Industry Module's typical growth pattern.

**GenerateBlocks / GenerateBlocks Pro** — The WordPress page-building plugin used as the default component/pattern-building layer in the WEF technology stack.

**GeneratePress / GeneratePress Premium** — The WordPress theme framework used as the default visual/structural foundation in the WEF technology stack.

**Industry Module** — A vertical-specific plugin to the Core Methodology, supplying personas, regulatory/compliance landscape, competitive patterns, positioning patterns, information architecture patterns, SEO/keyword strategy, trust signal requirements, and content model for one industry. Exactly one (or a documented blend of two) is active per engagement.

**Knowledge Base (KB)** — The persistent, versioned, structured store of every artifact and decision produced during an engagement (Governance, Sec. 5).

**LLM Handoff Protocol** — The five-layer context package (Charter, History, State, Module, Task) used to brief any AI model working on a WEF engagement (AI Workflows, Sec. 2).

**Master Website Blueprint (MWB)** — The single living document representing the current, approved state of the site's architecture, design, and content (Governance, Sec. 6).

**Module Gap** — A situation where a Stage Gate's Module Injection Point cannot be filled because the active Industry Module lacks needed content; escalated per Governance Section 9.5 and fed back into the Module via Change Request.

**Module Injection Point** — The explicit callout in a Core Methodology Stage Gate marking exactly where the active Industry Module's content must be substituted in (Governance, Sec. 9.2).

**MWEF** — *Mortgage Website Excellence Framework*, the original single-industry manual preserved intact at `/MWEF-v1.0/`, superseded in scope (but not deleted) by WEF v1.0's Core + Modules architecture. Its content lives on as the Mortgage Lending Industry Module.

**Positioning Statement** — The single, client-approved sentence defining how the client is distinctly positioned relative to its competitive set (Stage Gate 3).

**Project Charter** — The foundational governance document defining scope, objectives, roles, decision authority, and the active Industry Module(s) for an engagement (Governance, Sec. 3).

**Project Memory** — The rolling summary of current engagement status, distinct from the full Decision Register and the current-state Blueprint (Governance, Sec. 10).

**Rank Math** — The default SEO plugin used in the WEF technology stack for metadata, schema, and technical SEO management.

**Service Add-On Module** — An optional engagement capability, orthogonal to Industry Modules, named in the Project Charter per Governance Sec. 1.7 (e.g., Chat AI Agent-as-a-Service, Voice AI Agent-as-a-Service). Unlike an Industry Module, zero, one, or several may be active, and none is required.

**Stage Gate** — A defined phase of the WEF Core Methodology with fixed inputs, outputs, roles, and exit criteria; the fundamental unit of engagement structure, identical across every Industry Module.

**Topical Cluster Model** — The pillar-page/cluster-page content architecture used to build genuine topical authority (Stage Gate 5).

**Trust Signal Requirements** — The Industry Module section specifying what a vertical's audience needs to see to trust a provider, and where it typically must appear.

**Video-to-Website Deployment Brief** — The optional governed content brief connecting a video to its mapped website page/query, evidence and freshness, claims clearance, locale review, captions/transcript, CTA, embed/supporting content, internal links, metadata/schema, approved revision, ownership, and retirement trigger (Reusable Templates, Sec. 8.3).

**White Space Opportunity Map** — The Stage Gate 2 output identifying audience needs no competitor currently serves well.

---

## REFERENCES

This manual's methodology draws on, and assumes practitioner familiarity with, the following categories of external standards and resources. Consultants should consult current primary sources directly, as regulatory and platform guidance changes over time.

**Cross-Industry Standards**
- Web Content Accessibility Guidelines (WCAG) 2.1, Level AA
- Schema.org vocabulary and structured data guidelines
- Google Search Central documentation (Core Web Vitals, structured data, indexing)
- [Google Search SEO Starter Guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) (people-first usefulness, logical architecture, canonicalization, internal links, titles/descriptions, and measurement expectations)
- [Google Search spam policies](https://developers.google.com/search/docs/essentials/spam-policies) (doorway abuse and scaled-content abuse constraints relevant to locality and keyword-variant page programs)
- [Google Search guidance on page dates](https://developers.google.com/search/blog/2019/03/help-google-search-know-best-date-for) (visible published/modified dates, structured-data consistency, and no artificial freshness)
- [Google Analytics guidance on avoiding PII](https://support.google.com/analytics/answer/6366371) (event, URL, custom-dimension, and campaign-parameter implementation controls)
- [Cloudflare Access web-application guidance](https://developers.cloudflare.com/cloudflare-one/access-controls/applications/http-apps/) and [custom-hostname Access guidance](https://developers.cloudflare.com/cloudflare-for-platforms/cloudflare-for-saas/security/secure-with-access/) (identity-aware proxy placement, public-hostname routing, and custom-hostname prerequisites/limitations)
- [Rank Math PRO activation guidance](https://rankmath.com/kb/how-to-upgrade-to-rank-math-pro/) and [site connection guidance](https://rankmath.com/kb/how-to-connect-or-disconnect-rank-math/) (base/add-on activation, connected account, license selection, and per-site confirmation)
- FTC advertising and substantiation guidance (general, cross-industry)

**Regulatory Frameworks Referenced by Specific Industry Modules**
- Mortgage Lending: TILA/Reg Z, RESPA/Reg X, ECOA/Reg B, SAFE Act/NMLS, Fair Housing Act, CFPB guidance
- Real Estate: state real estate commission rules, Fair Housing Act, MLS/IDX rules, NAR/state association rules
- Law Firm: state bar advertising rules, state Rules of Professional Conduct
- Medical/Healthcare: HIPAA, state medical/dental board rules, FTC health claim substantiation rules
- Home Services: state/municipal contractor licensing, EPA regulations (trade-specific), FTC advertising rules
- Financial Advisor: SEC Marketing Rule (IA Act Rule 206(4)-1), FINRA advertising rules (Rule 2210), state securities regulator rules
- SaaS: GDPR, CCPA/CPRA, ADA Title III accessibility litigation landscape
- Cash Home Buyer / Real Estate Investor: state wholesaling/equitable-interest disclosure laws, state real estate license thresholds, TCPA, state foreclosure-consultant/homeowner bill of rights statutes, Fair Housing Act, FTC and state Attorney General predatory-practice enforcement history
- Distressed Property Advocate: real estate agent/broker licensing, state foreclosure-consultant statutes, unauthorized-practice-of-law boundaries, RESPA, NAR Code of Ethics, Fair Housing Act
- Expired Listing Specialist (Commercial-Weighted): real estate broker/agent licensing, NAR Code of Ethics (non-disparagement), truth-in-advertising/track-record substantiation, Fair Housing Act (residential component only)
- Probate Real Estate Investor: state wholesaling/equitable-interest disclosure laws, probate court-confirmation and overbid procedure, executor/administrator fiduciary duty and surcharge risk, TCPA, Fair Housing Act, FTC/state AG predatory-practice enforcement history
- Real Estate Development: SEC Regulation D (Rule 506(b)/506(c) general solicitation), state blue-sky securities law, Interstate Land Sales Full Disclosure Act, Fair Housing Act (advertising and design-and-construction), ADA Title III, entitlement/environmental review disclosure accuracy
- Commercial Real Estate (Investment Sales, Owner Rep/Leasing & Property Management): real estate broker/property-management licensing and trust accounting, dual-agency/designated-agency disclosure, Fair Housing Act (multifamily), Fair Credit Reporting Act (tenant screening), ADA Title III

Consult the relevant Industry Module for the full citation list applicable to that vertical, and always verify current requirements with the client's own qualified counsel — this manual identifies starting points, not final legal authority.

**Platform Documentation**
- GeneratePress Premium official documentation
- GenerateBlocks Pro official documentation
- Rank Math SEO official documentation
- LiteSpeed Cache official documentation
- Cloudflare documentation (DNS, CDN, WAF, Page Rules)
- Google Analytics 4, Google Search Console, Google Tag Manager official documentation
- Microsoft Clarity official documentation

**Internal Firm Resources**
- Firm Knowledge Base: `/methodology/wef/v1.0/`
- Predecessor manual (preserved, mortgage-only): `/MWEF-v1.0/`
- Methodology Governance Board meeting minutes and Change Request archive

---

## INDEX

*(Selective index; references point to chapter/section rather than fixed page numbers, since this manual is distributed as versioned digital files.)*

- AI Agent Services chapter — Core Methodology file 10
- AI Build Package — Development, SG10
- AI Verification Packet — AI Workflows, Sec. 5.4; Reusable Templates, Sec. 12.1
- AI Workflows chapter — Core Methodology file 08
- Chat AI Agent-as-a-Service — AI Agent Services, SG12A
- Design Constraints Package — Design, Appendix; Governance Sec. 15.4 (RETRO-005)
- Do-Not-Break List — Design, Appendix (Design Constraints Package Specification)
- Engagement Retrospective Register — Governance, Sec. 15
- Benchmark Validation — Design, SG7.5 Sec. 10.2
- Blended-Module engagements — Governance, Sec. 1.5, 9.4
- Blueprint, Master Website — Governance, Sec. 6
- Change Request process — Governance, Sec. 13.2; Reusable Templates, Sec. 3
- Capability Ownership Matrix — Governance, Sec. 13.4.4; Reusable Templates, Sec. 15.3
- Compliance/Standards Constraint Log — Research, SG1 Sec. 4
- Compliance/Standards Liaison role — Governance, Sec. 2.2
- Component Library (registry) — `/Component-Library/`, file 00; Design, Sec. 9.5
- Component Library Check (Design workflow step) — Design, Sec. 9.5, Sec. 10
- Content & Code Access Tier — Governance, Sec. 13.4.1
- Content-as-Files Sync Pipeline — Development, SG10.5-Sync
- Content Freshness Register — Research, Evidence Standard; Reusable Templates, Sec. 7.9
- Conversion Measurement & Operational Handoff Contract — UX & Conversion, SG6; Reusable Templates, Sec. 22.1
- Default technology stack, portability of — Governance, Sec. 13.4.2
- Core Web Vitals targets — SEO & Architecture, SG5 Sec. 11; Design, SG7.5 Sec. 10.2
- Decision Register — Governance, Sec. 4
- Digital Estate & Access Map — Research, SG1; Reusable Templates, Sec. 16.5
- Evidence & Source Register — Research, Evidence Standard; Reusable Templates, Sec. 7.8
- Default technology stack — Governance, Sec. 13.4
- Design Tournament — Design, SG7.5 Sec. 10.1
- Eight-Dimension Quality Standard — Governance, Sec. 12.2
- Future-Proofing Review — Design, SG7.5 Sec. 10.3
- GeneratePress implementation guidance — Design, Appendix
- GenerateBlocks implementation guidance — Design, Appendix
- Cash Home Buyer / Real Estate Investor Module — Industry Modules, Module-Cash-Home-Buyer.md
- Commercial Real Estate Module — Industry Modules, Module-Commercial-Real-Estate.md
- Distressed Property Advocate Module — Industry Modules, Module-Distressed-Property-Advocate.md
- Expired Listing Specialist (Commercial-Weighted) Module — Industry Modules, Module-Expired-Listings-Commercial.md
- Industry Modules (library index) — Industry Modules, file 00
- Probate Real Estate Investor Module — Industry Modules, Module-Probate-Real-Estate-Investor.md
- Real Estate Development Module — Industry Modules, Module-Real-Estate-Development.md
- Knowledge Base structure — Governance, Sec. 5.2
- LLM Handoff Protocol — AI Workflows, Sec. 2
- Module Injection Point convention — Governance, Sec. 9.2
- Module Integration Standard — Governance, Sec. 9
- Module Gap escalation — Governance, Sec. 9.5
- New Module Development Process — Governance, Sec. 13.6
- Positioning Statement — Research, SG3
- Post-Release Indexing Verification Record — QA & Optimization, SG11.5; Reusable Templates, Sec. 7.10
- Project Charter — Governance, Sec. 3
- Risk Register — Governance, Sec. 14
- Schema Markup Plan — SEO & Architecture, SG5 Sec. 13; Reusable Templates, Sec. 10
- Search Visibility Operations Plan — SEO & Architecture, SG5 Sec. 10.1-10.3; QA & Optimization, SG11.5; Reusable Templates, Sec. 7.4-7.7
- Service Add-On Module — Governance, Sec. 1.7
- Sitemap — SEO & Architecture, SG4
- Stage Gate template (19-part) — Research, Chapter Introduction
- Third-Party Custom Domain & Access-Control Record — Governance, Sec. 13.4.6; Reusable Templates, Sec. 15.7
- Topical Cluster Model — SEO & Architecture, SG5 Sec. 10
- Voice AI Agent-as-a-Service — AI Agent Services, SG12B
- Video-to-Website Deployment Brief — Reusable Templates, Sec. 8.3
- Voice & Tone Guide — Development, SG9

---

## APPENDICES

### Appendix A — Stage Gate Master Sequence Reference

| # | Stage Gate | Core Methodology File |
|---|---|---|
| 1 | Discovery & Market Research | 02-Research.md |
| 2 | Competitive Intelligence | 02-Research.md |
| 3 | Strategic Direction | 02-Research.md |
| 4 | Information Architecture | 03-SEO-Architecture.md |
| 5 | SEO Blueprint | 03-SEO-Architecture.md |
| 6 | UX & Conversion | 04-UX-Conversion.md |
| 7 | Visual Design System | 05-Design.md |
| 7.5 | Prototype Validation | 05-Design.md |
| 8 | Content Specification | 06-Development.md |
| 9 | Copywriting | 06-Development.md |
| 10 | AI Build Package | 06-Development.md |
| 10.5 | WordPress Implementation Blueprint | 06-Development.md |
| 11 | Quality Assurance | 07-QA-Optimization.md |
| 11.5 | Post-Launch Growth Program | 07-QA-Optimization.md |
| 12A | Chat AI Agent-as-a-Service *(optional — Service Add-On Module)* | 10-AI-Agent-Services.md |
| 12B | Voice AI Agent-as-a-Service *(optional — Service Add-On Module; not part of the website Stage Gate spine)* | 10-AI-Agent-Services.md |

### Appendix B — Default Technology Stack Quick Reference

See Governance, Section 13.4 for full detail and the Charter override process. Identical across every Industry Module.

### Appendix C — Mandatory Compliance Checkpoints Quick Reference

Compliance/Standards Liaison sign-off is **mandatory and non-waivable, wherever the active Industry Module flags the vertical as regulated,** at: Stage Gate 8 (Compliance Content Checklist), Stage Gate 9 (page-by-page Compliance Clearance Log), and Stage Gate 11 (final site-wide Compliance Sign-Off Record). No Decision Authority, client urgency, or schedule pressure overrides these three checkpoints. Consult the active Industry Module's Regulatory & Compliance Landscape section for which specific checkpoints apply with what intensity — Mortgage Lending, Law Firm, Medical/Healthcare, Financial Advisor, Cash Home Buyer / Real Estate Investor, Distressed Property Advocate, Probate Real Estate Investor, and Real Estate Development carry the highest intensity (several of these distinctively due to consumer-protection/predatory-practice enforcement history, foreclosure-consultant-statute and fiduciary-duty/court-process exposure, or — uniquely for Real Estate Development — federal securities-law general-solicitation exposure under Regulation D, rather than professional licensing alone); Real Estate, Home Services, Expired Listing Specialist, and Commercial Real Estate carry moderate intensity; SaaS carries the lowest baseline intensity but is not exempt.

### Appendix D — Component Library Quick Reference

See `/Component-Library/00-Component-Library-Index.md` for the full registry schema and governance. Current categories and seed entries: **Core** (Button, Icon), **Feedback** (Badge, Tag), **Forms** (Input, Select, Checkbox, Radio, Switch), **Marketing & Trust** (TrustBar, ComplianceFooter, LeadCaptureForm), **Surfaces** (Card, LocationCard, OfferingCard, StaffBioCard). Design, Sec. 9.5 requires checking this registry before any component is designed net-new, on any engagement, in any industry.

### Appendix E — Manual Change Control Summary

To propose a change to the **Core Methodology**, submit a Change Request (Reusable Templates, Sec. 3) to the Methodology Governance Board per Governance, Section 13.2 — reviewed within 10 business days. To propose a change to, or addition of, an **Industry Module**, submit a Change Request scoped to that Module — reviewed within 5 business days given the narrower blast radius. Approved changes are logged in the Front Matter Revision Log (Core changes) or the Module's own Version History (Module changes) and released as a new version per Governance, Section 11.

### Appendix F — Relationship to the Predecessor Manual

*Mortgage Website Excellence Framework (MWEF) v1.0*, the original single-industry manual, remains intact and unmodified at `/MWEF-v1.0/`. It is not a draft or a deprecated artifact — it is a complete, standalone reference that happens to also be the source material for this framework's Mortgage Lending Industry Module. Firms already running engagements under MWEF v1.0 may continue to reference it directly; new engagements, in any industry including mortgage lending, should be run under WEF v1.0's Core Methodology plus the relevant Industry Module.

---

*This concludes the Website Excellence Framework (WEF) v1.0. For questions regarding methodology interpretation or Industry Module development, contact the Methodology Governance Board via the firm's internal Knowledge Base.*
