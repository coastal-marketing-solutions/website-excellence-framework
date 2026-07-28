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

# STAGE GATE 10.5 — WORDPRESS IMPLEMENTATION BLUEPRINT

## 1. Purpose

Execute the AI Build Package into an actual, functioning WordPress/GeneratePress Premium/GenerateBlocks Pro site on the default (or Charter-specified) technology stack, with performance, caching, and security layers correctly configured. This gate is identical in process across every industry — it is purely a platform-implementation activity.

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

## 12. Prompt(s)

**Prompt 10.5.1 — Build Execution (Code-Generation Model)**

```
You are implementing a WordPress page using GenerateBlocks Pro for
[Client Name]'s website. Using the Build Manifest entry for "[Page URL]"
and the Component-to-Pattern Mapping, generate the GenerateBlocks pattern
structure (as block markup/JSON per GenerateBlocks' format) for this page.
Use only Global Style token references (no hardcoded hex colors or font
sizes). Insert the approved copy from "[copy file reference]" exactly as
written — do not paraphrase or regenerate copy that has already cleared
compliance review.
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
