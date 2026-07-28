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

**Compliance/Standards Liaison** — The client-side individual responsible for reviewing and approving all claims, disclosures, and regulated content per the active Industry Module. WEF firms and their consultants do not issue compliance sign-off themselves, in any industry.

**Core Methodology** — The industry-agnostic portion of WEF: Governance, Research, SEO & Architecture, UX & Conversion, Design, Development, QA & Optimization, AI Workflows, and Reusable Templates. Applies unchanged to every engagement regardless of vertical.

**Core Web Vitals (CWV)** — Google's user-experience performance metrics: Largest Contentful Paint (LCP), Interaction to Next Paint (INP), and Cumulative Layout Shift (CLS), used throughout this manual as binding performance targets.

**Decision Authority** — The named individual(s), specified in the Project Charter, with final sign-off power at each approval gate.

**Decision Register** — The append-only ledger of every material engagement decision, its rationale, and its alternatives considered (Governance, Sec. 4).

**Design Tournament** — The Stage Gate 7.5 activity in which 2–3 fully realized design directions are scored head-to-head on a fixed rubric rather than a single design being presented for approval or rejection.

**Engagement Lead** — The consultant with overall accountability for engagement outcomes, Industry Module selection, and Decision Register authority.

**Entity SEO** — An SEO approach focused on establishing unambiguous, machine-readable identity for an organization, its people, and its offerings — the foundation of both classic knowledge-panel visibility and AI-mediated search citation.

**Exit Criteria** — The pass/fail conditions that must be met before an engagement can move from one Stage Gate to the next.

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

**Stage Gate** — A defined phase of the WEF Core Methodology with fixed inputs, outputs, roles, and exit criteria; the fundamental unit of engagement structure, identical across every Industry Module.

**Topical Cluster Model** — The pillar-page/cluster-page content architecture used to build genuine topical authority (Stage Gate 5).

**Trust Signal Requirements** — The Industry Module section specifying what a vertical's audience needs to see to trust a provider, and where it typically must appear.

**White Space Opportunity Map** — The Stage Gate 2 output identifying audience needs no competitor currently serves well.

---

## REFERENCES

This manual's methodology draws on, and assumes practitioner familiarity with, the following categories of external standards and resources. Consultants should consult current primary sources directly, as regulatory and platform guidance changes over time.

**Cross-Industry Standards**
- Web Content Accessibility Guidelines (WCAG) 2.1, Level AA
- Schema.org vocabulary and structured data guidelines
- Google Search Central documentation (Core Web Vitals, structured data, indexing)
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

- AI Build Package — Development, SG10
- AI Workflows chapter — Core Methodology file 08
- Benchmark Validation — Design, SG7.5 Sec. 10.2
- Blended-Module engagements — Governance, Sec. 1.5, 9.4
- Blueprint, Master Website — Governance, Sec. 6
- Change Request process — Governance, Sec. 13.2; Reusable Templates, Sec. 3
- Compliance/Standards Constraint Log — Research, SG1 Sec. 4
- Compliance/Standards Liaison role — Governance, Sec. 2.2
- Core Web Vitals targets — SEO & Architecture, SG5 Sec. 11; Design, SG7.5 Sec. 10.2
- Decision Register — Governance, Sec. 4
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
- Project Charter — Governance, Sec. 3
- Risk Register — Governance, Sec. 14
- Schema Markup Plan — SEO & Architecture, SG5 Sec. 13; Reusable Templates, Sec. 10
- Sitemap — SEO & Architecture, SG4
- Stage Gate template (19-part) — Research, Chapter Introduction
- Topical Cluster Model — SEO & Architecture, SG5 Sec. 10
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

### Appendix B — Default Technology Stack Quick Reference

See Governance, Section 13.4 for full detail and the Charter override process. Identical across every Industry Module.

### Appendix C — Mandatory Compliance Checkpoints Quick Reference

Compliance/Standards Liaison sign-off is **mandatory and non-waivable, wherever the active Industry Module flags the vertical as regulated,** at: Stage Gate 8 (Compliance Content Checklist), Stage Gate 9 (page-by-page Compliance Clearance Log), and Stage Gate 11 (final site-wide Compliance Sign-Off Record). No Decision Authority, client urgency, or schedule pressure overrides these three checkpoints. Consult the active Industry Module's Regulatory & Compliance Landscape section for which specific checkpoints apply with what intensity — Mortgage Lending, Law Firm, Medical/Healthcare, Financial Advisor, Cash Home Buyer / Real Estate Investor, Distressed Property Advocate, Probate Real Estate Investor, and Real Estate Development carry the highest intensity (several of these distinctively due to consumer-protection/predatory-practice enforcement history, foreclosure-consultant-statute and fiduciary-duty/court-process exposure, or — uniquely for Real Estate Development — federal securities-law general-solicitation exposure under Regulation D, rather than professional licensing alone); Real Estate, Home Services, Expired Listing Specialist, and Commercial Real Estate carry moderate intensity; SaaS carries the lowest baseline intensity but is not exempt.

### Appendix D — Manual Change Control Summary

To propose a change to the **Core Methodology**, submit a Change Request (Reusable Templates, Sec. 3) to the Methodology Governance Board per Governance, Section 13.2 — reviewed within 10 business days. To propose a change to, or addition of, an **Industry Module**, submit a Change Request scoped to that Module — reviewed within 5 business days given the narrower blast radius. Approved changes are logged in the Front Matter Revision Log (Core changes) or the Module's own Version History (Module changes) and released as a new version per Governance, Section 11.

### Appendix E — Relationship to the Predecessor Manual

*Mortgage Website Excellence Framework (MWEF) v1.0*, the original single-industry manual, remains intact and unmodified at `/MWEF-v1.0/`. It is not a draft or a deprecated artifact — it is a complete, standalone reference that happens to also be the source material for this framework's Mortgage Lending Industry Module. Firms already running engagements under MWEF v1.0 may continue to reference it directly; new engagements, in any industry including mortgage lending, should be run under WEF v1.0's Core Methodology plus the relevant Industry Module.

---

*This concludes the Website Excellence Framework (WEF) v1.0. For questions regarding methodology interpretation or Industry Module development, contact the Methodology Governance Board via the firm's internal Knowledge Base.*
