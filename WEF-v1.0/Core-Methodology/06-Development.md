# CORE METHODOLOGY — DEVELOPMENT

*Website Excellence Framework (WEF) v1.0*

---

## Chapter Introduction

Development covers the four Stage Gates that move an engagement from approved specification to a live, staged build: Content Specification, Copywriting, AI Build Package, and WordPress Implementation Blueprint. All follow the fixed 19-part template defined in the Research chapter's introduction. This discipline carries the highest compliance/professional-standards exposure in the methodology in regulated verticals — Stage Gates 8 and 9 each carry a mandatory Compliance/Standards Liaison review step that cannot be waived wherever the active Industry Module flags the vertical as regulated.

---

# STAGE GATE 8 — CONTENT SPECIFICATION

## 1. Purpose

Produce a complete, page-by-page content specification for the entire sitemap: what content each page needs, its structural outline, its SEO requirements, and its compliance requirements — the brief that Stage Gate 9 copywriting will execute against.

## 2. Business Objectives

- Ensure no page reaches copywriting without a clear content brief, eliminating rework and inconsistent depth across the site.
- Operationalize the SEO & Architecture discipline's keyword map and the UX & Conversion discipline's flows into concrete content requirements per page.
- Front-load compliance/professional-standards requirements so Stage Gate 9 copy is written correctly the first time.

## 3. Inputs

Sitemap (SG4), Keyword-to-Page Map & Schema Plan (SG5), UX Pattern Library & Calculator Specs (SG6), approved Design System & Page Templates (SG7.5), Compliance/Standards Constraint Log (SG1, expanded through SG5/6), active Industry Module's Content Model & Page Types

## 4. Outputs

- Page-by-Page Content Specification (one brief per sitemap page)
- Content Depth Standard (minimum word count/structural requirements by page type)
- Compliance Content Checklist (per page type)

## 5. Required Documents

`/08-content-spec/content-specifications-v1.md`, `/08-content-spec/content-depth-standard-v1.md`, `/08-content-spec/compliance-content-checklist-v1.md`

## 6. Responsible Roles

SEO Specialist (lead — content briefs must satisfy the SEO & Architecture discipline's output), Information Architect (structural consistency), Strategy Consultant (messaging pillar consistency)

## 7. Required Specialists

Copywriter (early consult — confirm briefs are actionable), Compliance/Standards Liaison (mandatory — confirm compliance content checklist is complete before Stage Gate 9 begins, wherever the active Industry Module flags the vertical as regulated)

## 8. Decision Authority

Engagement Lead approves; no client sign-off required at this gate (client sees content at Stage Gate 9 review), but Compliance/Standards Liaison sign-off on the Compliance Content Checklist is mandatory wherever applicable.

## 9. Module Injection Point(s)

> **Module Injection Point:** Load the active Industry Module's **Content Model & Page Types** to determine what each page type must contain (beyond generic SEO/UX requirements), and its full **Regulatory & Compliance Landscape** to build the Compliance Content Checklist per page type.

## 10. Workflow

```
[1] For each sitemap page, draft a content brief: H1/heading outline,
    target keyword and intent (from SG5), required sections (per the
    Module's Content Model & Page Types), internal linking targets (per
    SG5 cluster model), calculator/tool embed references (from SG6), and
    compliance requirements (from Compliance/Standards Constraint Log)
        │
        ▼
[2] Define Content Depth Standard by page type (pillar page vs. cluster
    page vs. location page vs. compliance page)
        │
        ▼
[3] Build Compliance Content Checklist per page type using the Module's
    Regulatory & Compliance Landscape: required disclosures, credential
    display requirements, required statements, jurisdiction-specific
    language
        │
        ▼
[4] Compliance/Standards Liaison review and sign-off
        │
        ▼
[5] Internal review → Exit Criteria → Stage Gate 9 scheduled
```

## 11. Checklist

- [ ] Approved Design System & Page Templates (SG7.5) confirmed to cover 100% of the SG4-approved sitemap before any brief is drafted — if any page lacks an approved design, stop and resolve that gap first rather than drafting its content brief anyway (Governance, Sec. 15.4, RETRO-002; Design, Sec. 18)
- [ ] Active Industry Module's Content Model & Page Types reviewed before drafting briefs
- [ ] Every sitemap page has a completed content brief
- [ ] Every brief references its Stage Gate 5 primary keyword and search intent
- [ ] Every brief specifies internal linking targets consistent with the topical cluster model
- [ ] Content Depth Standard defined and applied consistently by page type
- [ ] Compliance Content Checklist completed and signed off by Compliance/Standards Liaison (where applicable)

## 12. Prompt(s)

**Prompt 8.1 — Page Content Brief Generation**

```
You are producing content briefs for [Client Name]'s website in the
[Industry Module name] vertical. Using the attached sitemap, Keyword-to-
Page Map, UX Pattern Library, and the [Industry Module]'s Content Model &
Page Types, produce a content brief for the page "[Page Name/URL]".
Include:
- H1 and full heading outline (H2/H3)
- Primary keyword and search intent (from Keyword-to-Page Map)
- Required sections with a one-sentence purpose for each (per the Module's
  Content Model for this page type)
- Internal linking targets (which pillar/cluster pages this should link
  to/from)
- Any calculator or interactive tool to embed (reference Stage Gate 6
  spec)
- Compliance content requirements applicable to this page type per the
  [Industry Module] (flag for Compliance/Standards Liaison confirmation
  rather than asserting final legal/professional language yourself)
- Target word count range per the Content Depth Standard for this page
  type
```

**Prompt 8.2 — Compliance Content Checklist**

```
Using the Compliance/Standards Constraint Log accumulated through Stage
Gates 1-6 and the [Industry Module]'s Regulatory & Compliance Landscape
for [Client Name], produce a Compliance Content Checklist organized by
page type. For each page type, list every disclosure, credential
statement, or required element that must appear, and note whether
placement is header/footer/inline. Flag any item where you are inferring
a requirement rather than citing it directly from the Module or the
Compliance/Standards Constraint Log, for Compliance/Standards Liaison
confirmation.
```

## 13. Examples

See each Industry Module's Content Model & Page Types for a fully worked content brief example (e.g., a state-specific loan product page for mortgage lending, a practice-area page for a law firm, a service-area page for home services, a specialty page for a medical practice).

## 14. Common Mistakes

- Writing content briefs generically without page-specific differentiation, producing thin, duplicate-feeling content across similar pages (e.g., the same offering across multiple locations).
- Deferring compliance requirements to Stage Gate 9 or 11, which causes expensive copy rewrites after the fact.
- Ignoring the Content Depth Standard and allowing inconsistent depth across a topical cluster, weakening the cluster's collective SEO authority.
- Skipping the active Industry Module's Content Model & Page Types and inventing page structures ad hoc, missing vertical-standard sections audiences expect to see.

## 15. Best Practices

- Write each location/service-area page brief with at least one genuinely location-specific data point — this is what prevents locational content from reading as templated.
- Have the Compliance/Standards Liaison review the Compliance Content Checklist against current regulatory/professional-standards guidance, not just the Module's last-updated version, since requirements change (Governance, Sec. 13.7).

## 16. Review Process

SEO Specialist and Copywriter jointly review briefs for actionability before Compliance/Standards Liaison sign-off; Engagement Lead approves the full specification.

## 17. Quality Assurance

Primary Eight-Dimension focus: **SEO**, **Scalability** (consistent brief quality across a growing page set).

## 18. Exit Criteria

- [ ] All Required Documents approved
- [ ] Compliance/Standards Liaison has signed off on the Compliance Content Checklist (where applicable)
- [ ] Copywriter confirms briefs are actionable without further clarification

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all three Required Documents saved v1.0
- Blueprint: "Content Inventory" section seeded with brief references (full content added at SG9)
- Decision Register: log Content Depth Standard thresholds as `DEC-SG8-001`

Briefs are executed in Stage Gate 9; the Content Depth Standard is reapplied to all new content proposed in Post-Launch Growth Program.

---

# STAGE GATE 9 — COPYWRITING

## 1. Purpose

Produce final, approved on-page copy for every page in the sitemap, written to the Stage Gate 8 briefs, in the client's approved voice, cleared by compliance where applicable.

## 2. Business Objectives

- Deliver copy that converts hesitant visitors into qualified leads without overpromising or misleading.
- Maintain consistent voice and messaging pillar alignment across the full site.
- Achieve 100% compliance clearance (where the active Industry Module flags the vertical as regulated) before any copy is handed to Development's build gates.

## 3. Inputs

Page-by-Page Content Specifications (SG8), Positioning & Messaging Pillars (SG3), Compliance Content Checklist (SG8), Client Personas (SG1), active Industry Module's Regulatory & Compliance Landscape and known claim-risk language patterns

## 4. Outputs

- Final Approved Copy (per page, in Knowledge Base)
- Voice & Tone Guide
- Compliance Clearance Log (per page)

## 5. Required Documents

`/09-copywriting/final-copy/{page-slug}.md` (one file per page), `/09-copywriting/voice-tone-guide-v1.md`, `/09-copywriting/compliance-clearance-log-v1.md`

## 6. Responsible Roles

Copywriter (lead), Strategy Consultant (voice/pillar consistency review)

## 7. Required Specialists

SEO Specialist (on-page optimization review against SG5 keyword targets), Compliance/Standards Liaison (**mandatory, page-by-page sign-off wherever the active Industry Module flags the vertical as regulated** — no page copy is final without an entry in the Compliance Clearance Log)

## 8. Decision Authority

Client review of copy is recommended (particularly homepage, offering pillar pages, and any page containing outcome, pricing, or result examples) but not mandatory for every page; Compliance/Standards Liaison sign-off is mandatory for every page without exception in regulated verticals.

## 9. Module Injection Point(s)

> **Module Injection Point:** Load the active Industry Module's **Regulatory & Compliance Landscape** and its known claim-risk language patterns before drafting copy for any page touching outcomes, pricing, timelines, guarantees, or credentials — flag every such statement per Prompt 9.1 rather than asserting it as fact.

## 10. Workflow

```
[1] Establish/confirm Voice & Tone Guide from positioning and messaging
    pillars
        │
        ▼
[2] Draft copy per page against its Stage Gate 8 brief (AI-assisted first
    draft, human copywriter refinement)
        │
        ▼
[3] SEO Specialist review: on-page optimization (heading usage, keyword
    integration, internal linking execution, meta title/description)
        │
        ▼
[4] Compliance/Standards Liaison review: page-by-page sign-off logged in
    Compliance Clearance Log (where applicable)
        │
        ▼
[5] Client review (recommended for key pages)
        │
        ▼
[6] Final copy locked → Exit Criteria → Development's build gates
    scheduled
```

## 11. Checklist

- [ ] Voice & Tone Guide documented and applied consistently
- [ ] Every page has final copy matching its Stage Gate 8 brief structure
- [ ] Every page has an SEO Specialist on-page review completed (meta title/description, heading/keyword usage, internal links executed)
- [ ] Every page has a Compliance Clearance Log entry — no exceptions, including low-traffic or "boilerplate" pages, wherever the Module flags the vertical as regulated
- [ ] No superlative, guarantee, or unsubstantiated claim language remains without compliance-approved qualifying language, per the Module's known claim-risk patterns

## 12. Prompt(s)

**Prompt 9.1 — Page Copywriting**

```
You are the Copywriter for [Client Name] in the [Industry Module name]
vertical. Using the content brief for "[Page Name]", the Voice & Tone
Guide, and the [Industry Module]'s known claim-risk language patterns,
write final on-page copy. Requirements: address the persona's specific
objection(s) named in the brief; use the messaging pillars as the
emotional/value throughline, not as literal repeated phrases; write all
headings per the brief's heading outline; embed calls-to-action per the
Stage Gate 6 conversion flow for this page; flag any statement about
outcomes, pricing, timelines, approval/success odds, or savings with
"[COMPLIANCE REVIEW NEEDED]" rather than asserting it as fact. Do not
fabricate testimonials, statistics, or awards.
```

**Prompt 9.2 — Meta Title/Description Generation**

```
For the page "[Page Name/URL]" with primary keyword "[keyword]" and
search intent "[intent]", write 3 meta title options (50-60 characters)
and 3 meta description options (140-155 characters) that include the
primary keyword naturally, reflect the positioning statement's value
proposition, and avoid any claim pattern the [Industry Module] flags as
compliance risk for this vertical.
```

## 13. Examples

*Generic compliance-flagged copy pattern before clearance:*

> Draft: "Get [outcome] in as little as [timeframe]." → `[COMPLIANCE REVIEW NEEDED: timeline/outcome claim]` → Cleared version (per Compliance/Standards Liaison, per the active Industry Module's approved qualifying language pattern).

See each Industry Module's Regulatory & Compliance Landscape for fully worked, vertical-specific before/after claim examples.

## 14. Common Mistakes

- Publishing AI-drafted copy without running it through the Compliance/Standards Liaison because it "reads fine" — compliance risk in regulated-industry advertising is a legal or professional-standards judgment, not a stylistic one.
- Copy drifting from the approved Voice & Tone Guide as multiple contributors (human and AI) write different pages, without a Strategy Consultant consistency pass.
- Treating meta titles/descriptions as an afterthought rather than a Stage Gate 9 deliverable with the same compliance scrutiny as body copy.
- Applying a generic claim-risk sensibility instead of the active Industry Module's specific, documented claim-risk language patterns.

## 15. Best Practices

- Run every AI-drafted page through a compliance-risk-flagging pass (Prompt 9.1's flagging instruction) before it ever reaches a human compliance reviewer — this makes the Compliance/Standards Liaison's job faster and more thorough.
- Maintain the Compliance Clearance Log as a page-by-page ledger, not a single "content approved" blanket statement, so any future compliance question about a specific page can be traced to exactly what was reviewed and when.

**Multilingual/bilingual claims must be explicitly scoped to what's actually offered in that language.** A "we serve Spanish-speaking clients" or "bilingual service" claim must state precisely what that covers — conversation, guidance, and general site content — and must never be implied to extend to legally operative documents (contracts, disclosures, signed agreements) unless the client's actual operational and licensing structure genuinely supports that. A confirmed real-world finding: a client's brokerage only accepted standard English-language forms, making an unscoped bilingual claim a real legal-exposure risk once corrected. Log the scope explicitly as a standing Compliance Constraint Log entry, not just a one-time copy fix, since it will recur any time bilingual content is added later.

**Personal/exclusivity service claims need verification against the actual operational team, not just against outright fabrication.** "One-on-one, same person start to finish" can be *almost* true and still be a real claim-substantiation risk — a confirmed real-world case involved a solo-licensed practitioner supported by an unlicensed or differently-licensed assistant, where the original copy overstated exclusivity beyond what the actual team structure supported. This is a subtler check than the standard no-fabrication rule: verify any claim of personal/solo service delivery against the client's actual team structure as confirmed at Stage Gate 1, not just against whether the claim is technically false.

## 16. Review Process

SEO Specialist reviews for on-page optimization; Compliance/Standards Liaison reviews every page without exception (where applicable); Strategy Consultant spot-checks a sample for voice consistency; client reviews key pages by invitation.

## 17. Quality Assurance

Primary Eight-Dimension focus: **Conversion**, **Brand**, **SEO**. Compliance is treated as a gating requirement layered on top of, not substituting for, the Eight-Dimension standard.

## 18. Exit Criteria

- [ ] All pages have final copy with Compliance Clearance Log entries (where applicable)
- [ ] Voice & Tone consistency confirmed
- [ ] SEO on-page review complete for all pages

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: final copy files saved v1.0 per page; Voice & Tone Guide and Compliance Clearance Log saved v1.0
- Blueprint: "Content Inventory" section finalized with approved copy references
- Decision Register: log any compliance-driven claim modifications as `DEC-SG9-00x` for future reference (protects against re-litigating the same claim question in future content additions, and is a candidate learning to propose back into the active Industry Module)

Voice & Tone Guide and Compliance Clearance Log processes are reused unchanged for all Post-Launch Growth Program content additions.

---

# STAGE GATE 10 — AI BUILD PACKAGE

## 1. Purpose

Assemble the complete, unambiguous specification package that a developer or AI build model uses to construct the actual WordPress/GeneratePress/GenerateBlocks site — translating every prior discipline's approved output into implementation-ready instructions.

## 2. Business Objectives

- Eliminate ambiguity between design intent and build execution.
- Enable an AI code-generation model (or a developer working alongside one) to implement the site correctly on the first pass.
- Preserve full traceability from build decisions back to the Stage Gate that specified them.

## 3. Inputs

Approved Design System & Component Library (SG7.5), Final Copy (SG9), Schema Markup Plan & Technical SEO Spec (SG5), Sitemap & URL Structure (SG4), Calculator Specs (SG6)

## 4. Outputs

- AI Build Package (consolidated implementation spec)
- Page-by-Page Build Manifest
- Component-to-Pattern Mapping
- Integration Requirements Spec (forms, calculators, analytics, and any Module-specific system integrations)

## 5. Required Documents

`/10-ai-build-package/build-package-v1.md`, `/10-ai-build-package/build-manifest-v1.md`, `/10-ai-build-package/component-pattern-mapping-v1.md`, `/10-ai-build-package/integration-requirements-v1.md`

## 6. Responsible Roles

Developer (lead), Visual Designer (design fidelity reference), SEO Specialist (technical SEO requirements carry-forward)

## 7. Required Specialists

AI Orchestrator (structuring the package for AI build-model consumption per the LLM Handoff Protocol — AI Workflows chapter)

## 8. Decision Authority

Engagement Lead approves the package as complete and unambiguous before build begins; no client sign-off required at this gate (client already approved design at SG7.5 and copy at SG9).

## 9. Module Injection Point(s)

> **Module Injection Point:** If the active Industry Module documents any typical third-party system integration pattern (e.g., a loan origination system for mortgage lending, an MLS feed for real estate, a practice-management system for a law or medical practice, a CRM for financial advisors or home services, a billing/subscription system for SaaS), include it explicitly in the Integration Requirements Spec.

## 10. Workflow

```
[1] Consolidate all approved prior-gate outputs into a single Build
    Package document structured for both human developer and AI build
    model consumption
        │
        ▼
[2] Produce Page-by-Page Build Manifest: every page, its template,
    its final copy reference, its schema requirements, its URL
        │
        ▼
[3] Produce Component-to-Pattern Mapping: every design component mapped
    to its specific GenerateBlocks pattern implementation
        │
        ▼
[4] Produce Integration Requirements Spec: forms, calculators, analytics
    tags (GA4, GTM, Clarity), any Module-typical third-party integrations
        │
        ▼
[5] Internal completeness review → Exit Criteria → Stage Gate 10.5
    scheduled
```

## 11. Checklist

- [ ] Every sitemap page appears in the Build Manifest with its template, copy, schema, and URL
- [ ] Every component in the Stage Gate 7 library has a corresponding entry in the Component-to-Pattern Mapping
- [ ] Integration Requirements Spec covers all calculators, forms, analytics, and any Module-flagged third-party touchpoints in scope
- [ ] Package is structured so an AI build model, given this document plus the LLM Handoff Protocol context package, could implement a page correctly without additional clarification

## 12. Prompt(s)

**Prompt 10.1 — Build Manifest Generation**

```
You are assembling the AI Build Package for [Client Name]'s website in
the [Industry Module name] vertical. Using the approved sitemap, final
copy files, schema plan, and component library, produce a Page-by-Page
Build Manifest as a table with columns: Page URL, Template Type
(reference Stage Gate 7 template names), Copy File Reference, Schema
Types Required, Primary Components Used, Internal Links Required (from
Stage Gate 5 cluster model). Flag any page where required inputs are
incomplete rather than guessing at placeholder content.
```

**Prompt 10.2 — Component-to-Pattern Mapping**

```
For each component in the Stage Gate 7 Component Library, specify its
GenerateBlocks implementation: block type composition (Container/Grid/
Button/Query Loop/etc.), required CSS classes tied to Global Style
tokens, responsive behavior at each breakpoint, and any dynamic data
source (e.g., practitioner/staff directory via Query Loop against a
custom post type). This mapping will be handed to a developer or AI build
model as the authoritative implementation reference — be exact, not
descriptive.
```

## 13. Examples

*Generic Build Manifest row pattern:*

| Page URL | Template | Copy Ref | Schema | Components | Internal Links |
|---|---|---|---|---|---|
| `/{offering}/{location}/` | Location Offering Page | `09-copywriting/final-copy/{offering}-{location}.md` | Service, LocalBusiness, FAQPage, BreadcrumbList | Hero, Calculator Module, FAQ Accordion, Staff CTA Card | → `/{offering}/` (pillar), → `/{persona-hub}/` |

## 14. Common Mistakes

- Handing a build model the design and copy separately without a consolidated manifest, forcing it to infer relationships that should have been made explicit.
- Omitting analytics/tag requirements from the Integration Requirements Spec, resulting in a launched site with no measurement instrumentation (directly undermining Post-Launch Growth Program).
- Failing to flag incomplete inputs and instead allowing an AI build model to fabricate placeholder content that accidentally ships to production.

## 15. Best Practices

- Structure the Build Package explicitly for the LLM Handoff Protocol (AI Workflows chapter) — include the Charter, History (relevant Decision Register entries), State (current Blueprint), Module (active Industry Module), and Task layers together rather than assuming the build model has separate access to them.
- Version the Build Manifest so that any mid-build scope addition is a tracked, deliberate change rather than an informal request.

**Read the actual Terms of Service for any third-party API or vendor integration before it goes live, not just before it's selected.** A confirmed real-world gap: a free-tier AVM/valuation API's public-display licensing terms were accepted at vendor-selection time based on marketing language ("flexible licensing") without a direct read of the actual Terms of Use — flagged as a known open item rather than resolved. Any metered or usage-billed third-party integration (an AVM, an IDX feed, an AI/LLM API called from the live site) needs both a Terms of Service review and explicit abuse/bot protection (rate limiting, CAPTCHA/Turnstile, debounce) before go-live, since an unprotected metered endpoint is a direct, uncapped cost-exposure risk — log this as a P0 Backlog item at vendor selection, not an afterthought discovered post-launch.

## 16. Review Process

Engagement Lead and Developer jointly review the package for completeness against the Checklist before build begins.

## 17. Quality Assurance

Primary Eight-Dimension focus: **AI Implementation Readiness**, **Maintainability**, **WordPress/GeneratePress/GenerateBlocks Compatibility**.

## 18. Exit Criteria

- [ ] All Required Documents complete and internally reviewed
- [ ] No incomplete inputs remain unflagged
- [ ] Developer confirms the package is sufficient to begin build without further clarification requests

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents saved v1.0
- Blueprint: "Technical Build Spec" section seeded (finalized at SG10.5)
- Decision Register: log any build-sequencing decisions (e.g., phased launch order) as `DEC-SG10-00x`

The Build Package is the direct input to Stage Gate 10.5, where it is executed into an actual WordPress/GeneratePress/GenerateBlocks build.

---

# STAGE GATE 10.5 — WORDPRESS IMPLEMENTATION BLUEPRINT (OR CHARTER-SPECIFIED ALTERNATIVE STACK)

## 1. Purpose

Execute the AI Build Package into an actual, functioning site on the Charter-confirmed technology stack (Governance, Sec. 13.4.1), with performance, caching, and security layers correctly configured. This gate is identical in process across every industry — it is purely a platform-implementation activity. The workflow, checklist, and prompts below are written against the **default stack** (WordPress/GeneratePress Premium/GenerateBlocks Pro), since that is what most engagements confirm; Sec. 10.5-Alt below maps the same steps onto a Charter-specified alternative (e.g., a custom PHP/HTML build) for engagements that confirm a different stack. No AI coding agent begins work at this gate without the Design Constraints Package (Design, Appendix) loaded as context.

## 2. Business Objectives

- Deliver a functioning, performant, secure WordPress build matching the approved design and content exactly.
- Configure the full default stack (Hostinger VPS, LiteSpeed Cache, Cloudflare, Rank Math, GenerateCloud) correctly and consistently.
- Produce a build that a client's own team, or a future consultant, can maintain without the original developer.

## 3. Inputs

AI Build Package, Build Manifest, Component-to-Pattern Mapping, Integration Requirements Spec (all from Stage Gate 10)

## 4. Outputs

- Functioning WordPress/GeneratePress/GenerateBlocks build (staging environment)
- Server/Hosting Configuration Record
- Plugin & Integration Configuration Record
- Performance Configuration Record (LiteSpeed Cache, Cloudflare settings)

## 5. Required Documents

`/10.5-wp-implementation/server-config-record-v1.md`, `/10.5-wp-implementation/plugin-config-record-v1.md`, `/10.5-wp-implementation/performance-config-record-v1.md`, staging site URL logged in Project Memory

## 6. Responsible Roles

Developer (lead)

## 7. Required Specialists

SEO Specialist (verify Rank Math configuration matches Stage Gate 5 schema plan), AI Orchestrator (verify build output matches Build Manifest, if AI-assisted code generation was used)

## 8. Decision Authority

Engagement Lead approves staging build as ready for QA & Optimization; no client sign-off at this specific gate (client sees the site formally at QA/launch).

## 9. Module Injection Point(s)

None — this gate is purely platform-implementation and does not vary by Industry Module, beyond building whatever Module-specific integrations were already specified in the Stage Gate 10 Integration Requirements Spec.

## 10. Workflow

```
[1] Provision Hostinger VPS environment; install WordPress, GeneratePress
    Premium, GenerateBlocks Pro, GenerateCloud connection
        │
        ▼
[2] Configure Rank Math SEO per Stage Gate 5 Schema Markup Plan and
    Technical SEO Requirements
        │
        ▼
[3] Build Global Styles (typography, color, spacing) per Stage Gate 7.5
    approved Design System Specification
        │
        ▼
[4] Build GenerateBlocks patterns per Component-to-Pattern Mapping
        │
        ▼
[5] Build each page per the Build Manifest, inserting approved copy and
    schema
        │
        ▼
[6] Configure LiteSpeed Cache (page cache, image optimization, CSS/JS
    minification/combination consistent with Core Web Vitals targets)
        │
        ▼
[7] Configure Cloudflare (DNS, CDN, WAF rules, SSL/TLS settings)
        │
        ▼
[8] Configure Google Analytics 4, Google Search Console, Google Tag
    Manager, Microsoft Clarity per Integration Requirements Spec
        │
        ▼
[9] Internal smoke test → Exit Criteria → QA & Optimization scheduled
```

## 11. Checklist

- [ ] WordPress + GeneratePress Premium + GenerateBlocks Pro + GenerateCloud provisioned and licensed correctly
- [ ] Global Styles match Design System Specification exactly (spot-check color/type tokens)
- [ ] Every page in the Build Manifest exists on staging with correct copy, schema, and internal links
- [ ] Rank Math configuration matches Schema Markup Plan (spot-check structured data via a validator)
- [ ] LiteSpeed Cache configured; Core Web Vitals targets tested on staging
- [ ] Cloudflare DNS, CDN, and security rules configured
- [ ] GA4, Search Console, GTM, and Clarity all verified firing correctly on staging
- [ ] Staging environment access provided to QA Analyst
- [ ] Content-as-Files Sync Pipeline (Sec. 10.5-Sync below) set up and tested end-to-end before this gate exits

### 10.5-Alt — Charter-Specified Alternative Stack Mapping

WEF's default recommendation is Hostinger/WordPress/GeneratePress/GenerateBlocks/GitHub, and most engagements are expected to confirm it (Governance, Sec. 13.4.1). Where the Charter confirms a different stack instead — most commonly a **Custom PHP/HTML** build with no CMS — the same Workflow (Sec. 10) and Checklist (Sec. 11) structure still applies; only the platform-specific mechanics change:

| Default-Stack Step | Custom PHP/HTML (or other alternative) Equivalent |
|---|---|
| Provision Hostinger VPS, install WordPress/GeneratePress/GenerateBlocks | Provision the Charter-confirmed host/server; establish the confirmed deploy pipeline (e.g., GitHub Actions or equivalent CI to the confirmed host) |
| Configure Rank Math SEO | Implement the SG5 Schema Markup Plan and meta-tag requirements directly in template/head markup, or via the Charter-confirmed alternative SEO tooling |
| Build Global Styles (GeneratePress Customizer) | Implement the Design Constraints Package's machine-readable design tokens (Design, Appendix) as CSS custom properties or an equivalent token file — the single source of truth either way |
| Build GenerateBlocks patterns | Build reusable template partials/components per the Design Constraints Package's structural constraints (Design, Appendix, Sec. 2) — same reusability discipline, different mechanism |
| Configure LiteSpeed Cache / Cloudflare | Configure the Charter-confirmed caching/CDN layer against the same Core Web Vitals targets (SG5) |
| Configure GA4/GSC/GTM/Clarity | Unchanged — these are platform-independent and apply regardless of the confirmed stack |

The **Design Constraints Package is the deliverable that makes this mapping possible** — because it states platform constraints as an explicit, structured input rather than assuming GeneratePress/GenerateBlocks, any AI coding agent can implement correctly against whichever stack Sec. 1 of that package declares. Log the Platform/Vendor decisions made under this alternative path as Decision Register entries, same as any Sec. 13.4.1 stack confirmation.

### 10.5-Sync — Content-as-Files Sync Pipeline (Required Default)

This is the direct fix for the single most common source of AI-assisted-edit failure this framework has observed (Governance, Sec. 15.4, RETRO-005): a CMS's page content lives in a database, editable only through a browser GUI, while an AI coding agent works natively and reliably in git-tracked files. This pipeline closes that gap by treating **git as the source of truth for page content, and the live database as a build artifact synced from it** — the same relationship code already has to a deployed server, applied to content for the first time.

**Purpose:** Make page-content edits a normal, reviewable git workflow (diff, commit, PR if desired) instead of a browser-automation task, for every engagement where the Content & Code Access Tier (Governance, Sec. 13.4.1) makes it possible.

**Mechanism, by Tier (Governance, Sec. 13.4.1):**

- **Tier 1 (SSH + WP-CLI available):** Export every page's content to a versioned file (one file per page, e.g., `/content-sync/pages/{slug}.html`, containing the raw block markup) via `wp post list --post_type=page --format=json` to enumerate and `wp post get {ID} --field=post_content` per page to export. Edit exported files as normal git-tracked files — this is where an AI coding agent (Claude Code, Codex, Manus, GitHub Copilot) does its actual work. Push changes back with `wp post update {ID} --post_content=- < /content-sync/pages/{slug}.html` (or an equivalent scripted import). Re-export immediately after import and diff against git to confirm the live site matches exactly what was committed — never assume the import succeeded without verifying.
- **Tier 2 (REST API only, no SSH):** Use the platform's REST API with an application-scoped credential (e.g., WordPress Application Passwords) to `GET` and `PATCH`/`POST` page content programmatically from the same git-tracked files — no shell access required, works over HTTPS on nearly any host. Slower and slightly less scriptable than WP-CLI, but preserves the same "files are the source of truth, DB is synced from them" discipline.
- **Tier 3 (GUI only):** Content-as-files still applies as the authoring discipline — draft and review the change as a file in git first — but the actual push is a manual or browser-automated edit through the native editor, with a fresh export/screenshot verification step afterward to confirm the live page matches the committed file. This tier is the least reliable and should trigger a note in the Risk Register (Governance, Sec. 14) if it's the only tier available for an engagement expected to need frequent post-launch content changes.

**Required Documents:** `/10.5-wp-implementation/content-sync/README.md` (documents which Tier is in use and the exact export/import commands or scripts for this engagement's confirmed stack), `/10.5-wp-implementation/content-sync/pages/*.html` (one file per page, the actual source-of-truth content)

**Checklist:**
- [ ] Content & Code Access Tier confirmed at Governance Sec. 13.4.1 intake, before this pipeline is set up
- [ ] Every sitemap page has a corresponding file in `/content-sync/pages/`
- [ ] Import mechanism tested end-to-end at least once (export → edit → import → re-export → diff clean) before being relied on for real changes
- [ ] Every subsequent AI-assisted content change follows this pipeline — a direct, unlogged database or GUI edit that bypasses git is a process defect, not a shortcut, and should be treated the same as any other undocumented Decision Register-worthy change (Governance, Sec. 4.4)

**Common Mistakes:** Treating this pipeline as a one-time migration step instead of the standing workflow for all future content edits, which lets the database silently drift from git again exactly as it did before this pipeline existed. Skipping the post-import re-export/diff verification step and assuming the write succeeded. Building this pipeline once and never documenting which Tier it depends on, so a later session doesn't know why it's failing when host access changes.

## 12. Prompt(s)

**Prompt 10.5.1 — Build Execution (AI Coding Agent)**

```
You are implementing a page for [Client Name]'s website using [Claude
Code / Codex / Manus / GitHub Copilot / equivalent AI coding agent].
Before making any change, load and follow the Design Constraints Package
(Design, Appendix) in full — it declares the confirmed platform target,
the structural/buildability constraints for that platform, the
machine-readable design tokens, and the Do-Not-Break List. Do not assume
GeneratePress/GenerateBlocks if the Design Constraints Package's Platform
Target Declaration says otherwise.

Using the Build Manifest entry for "[Page URL]" and the Component-to-
Pattern Mapping, generate the page structure in the format the confirmed
platform requires (GenerateBlocks pattern markup/JSON for the default
stack; the equivalent template/component format for a Charter-confirmed
alternative stack). Use only the Design Constraints Package's token
references — no hardcoded hex colors, font sizes, or spacing values.
Insert the approved copy from "[copy file reference]" exactly as written
— do not paraphrase or regenerate copy that has already cleared
compliance review. Do not alter anything on the Do-Not-Break List. If
anything in this prompt conflicts with the Design Constraints Package,
stop and flag the conflict rather than guessing which instruction wins.
```

**Prompt 10.5.2 — Performance Configuration Review**

```
Given the current LiteSpeed Cache configuration and Cloudflare settings
for [staging URL], and the Core Web Vitals targets from Stage Gate 5
(LCP < 2.5s, INP < 200ms, CLS < 0.1), identify specific configuration
changes needed to meet these targets on the [homepage/key template]. Be
specific about which LiteSpeed Cache settings (image optimization,
critical CSS, JS delay) or Cloudflare settings (caching level, Rocket
Loader, image resizing) to adjust, rather than giving generic performance
advice.
```

**Prompt 10.5.3 — Content-as-Files Sync (Sec. 10.5-Sync)**

```
You are setting up (or executing a change through) the Content-as-Files
Sync Pipeline for [Client Name]'s site on [confirmed platform, e.g.
WordPress]. The confirmed Content & Code Access Tier for this engagement
is [Tier 1: SSH+WP-CLI / Tier 2: REST API / Tier 3: GUI — see Governance
Sec. 13.4.1]. Using that tier's mechanism:
1. Export the current content of "[Page Name/URL]" into
   /content-sync/pages/[slug].html if it is not already there
2. Make the requested change to that file only — do not edit anything
   through the platform's native editor directly
3. Push the file back via the confirmed tier's import mechanism
4. Re-export the live page and diff it against the file you just pushed;
   report the diff (should be empty) as confirmation, not just "done"
Do not proceed past step 4 without showing the verification diff.
```

## 13. Examples

*Generic Performance Configuration Record pattern:*

| Setting | Value | Rationale |
|---|---|---|
| LiteSpeed Cache — Image Optimization | WebP conversion enabled, lazy load below fold | Reduces LCP on image-heavy homepage hero |
| LiteSpeed Cache — CSS/JS | Combine + minify, critical CSS generation enabled | Reduces render-blocking resources |
| Cloudflare — Caching Level | Standard, with Page Rules caching static assets aggressively | Reduces server load, improves TTFB |
| Cloudflare — Rocket Loader | Disabled | Conflicted with interactive calculator scripts in testing; documented as a known incompatibility |

## 14. Common Mistakes

- Enabling aggressive caching/minification defaults without testing calculator and form functionality, which can silently break interactive tools.
- Deploying without verifying Rank Math schema output against a structured data validator, shipping malformed schema that fails to earn rich results.
- Skipping GA4/GTM/Clarity verification, discovering at Post-Launch Growth Program that months of traffic went unmeasured.

## 15. Best Practices

- Always test LiteSpeed Cache and Cloudflare optimization settings against every interactive element (calculators, multi-step forms) before finalizing — performance settings and JavaScript-dependent UX are a common conflict point.
- Document every non-default configuration decision (like the Rocket Loader example above) in the Performance Configuration Record so a future maintainer understands why a setting deviates from platform defaults.
- Use GenerateCloud to sync the Global Styles and pattern library, so future multi-site or template reuse across engagements — even across different Industry Modules — is possible.

**WordPress's Parent-page picker only searches Published pages — plan nested URLs accordingly if pages stay in Draft pending compliance sign-off.** A confirmed, reproducible finding: if the engagement's compliance strategy holds every page in Draft status until a single bulk pre-launch review (a legitimate strategy — see QA & Optimization Stage Gate 11's Best Practices addendum), any child page built during that window (e.g., a city or persona-hub page meant to nest under a Buy/Sell/Neighborhoods pillar) cannot have its Parent set correctly, because WordPress's admin UI only lists Published pages as parent-picker candidates. The page ships with a flat top-level slug instead of its intended nested URL. This is not a build error — it's a structural consequence of the Draft-until-bulk-review strategy, and must be fixed by re-parenting every affected child page once its intended parent is finally published, immediately before go-live, not discovered as a surprise at that moment.

**Verify every AI-driven CMS/plugin edit via a genuine fresh page reload, not by reading the in-session DOM state.** Two distinct, confirmed failure patterns: (1) a scripted edit (native-setter + dispatched input event, per this chapter's own recommended technique) can *look* successful in the same browser session while silently failing to persist — only a fresh navigation/reload reveals whether it actually saved; (2) some plugin fields carry a deliberate anti-tampering guard against scripted editing altogether (observed with an SEO plugin's title field specifically resisting the standard technique) — when the standard technique doesn't persist after a genuine reload, check whether a different, underlying WordPress-native field feeds the same displayed value via a template token (e.g., editing the post's actual title, which a plugin's "%title%" token then inherits), and edit that instead of continuing to fight the plugin's own UI layer.

**Watch for cross-client tool-connection leakage on any operation managing multiple client sites through shared plugin-level integrations.** A confirmed, serious real-world finding: one client's site was found sending live analytics traffic to a *different* client's Analytics property, traced to an SEO plugin's built-in Analytics module being connected to the wrong Google account — a direct consequence of the same operator configuring the same plugin across multiple client sites via a shared connected account. Any agency or operator managing multiple WordPress sites through shared plugin-level tool connections (an SEO plugin's Analytics integration, a shared API key, a shared connected account) must explicitly re-verify the connected account/property is correct *per site*, not assume the plugin defaulted correctly — add this as an explicit QA checklist item (QA & Optimization Stage Gate 11's Checklist, Sec. 11) for any operator running more than one active client engagement concurrently.

## 16. Review Process

Developer self-tests against the Checklist; SEO Specialist independently validates schema output; Engagement Lead confirms staging is ready for formal QA.

## 17. Quality Assurance

Primary Eight-Dimension focus: **Performance**, **WordPress/GeneratePress/GenerateBlocks Compatibility**, **Maintainability**.

## 18. Exit Criteria

- [ ] All Required Documents complete
- [ ] Staging site passes internal smoke test (all pages load, all forms/calculators function, analytics fire)
- [ ] SEO Specialist has validated schema implementation

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all Required Documents saved v1.0; staging URL logged in Project Memory
- Blueprint: "Technical Build Spec" section finalized with actual configuration record
- Decision Register: log any deviation from default stack configuration (e.g., the Rocket Loader example) as `DEC-SG10.5-00x`

This build is the subject of QA & Optimization's formal QA gate and becomes the production site upon successful launch. Configuration records are referenced again during Post-Launch Growth Program technical changes.

---

*End of Development. Continue to Core Methodology — QA & Optimization.*
