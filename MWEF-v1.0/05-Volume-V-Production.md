# VOLUME V — PRODUCTION

*Mortgage Website Excellence Framework (MWEF) v1.0*

---

## Volume Introduction

Volume V is where the engagement moves from approved specification to a live, measured website. It comprises six Stage Gates: Content Specification, Copywriting, AI Build Package, WordPress Implementation Blueprint, Quality Assurance, and Post-Launch Growth Program. All follow the fixed 19-part template from Volume II. This Volume carries the highest compliance exposure in the methodology — Stage Gates 8, 9, and 11 each carry a mandatory Compliance Liaison review step that cannot be waived.

---

# STAGE GATE 8 — CONTENT SPECIFICATION

## 1. Purpose

Produce a complete, page-by-page content specification for the entire sitemap: what content each page needs, its structural outline, its SEO requirements, and its compliance requirements — the brief that Stage Gate 9 copywriting will execute against.

## 2. Business Objectives

- Ensure no page reaches copywriting without a clear content brief, eliminating rework and inconsistent depth across the site.
- Operationalize the Stage Gate 5 keyword map and Stage Gate 6 UX flows into concrete content requirements per page.
- Front-load compliance requirements so Stage Gate 9 copy is written correctly the first time.

## 3. Inputs

Sitemap (SG4), Keyword-to-Page Map & Schema Plan (SG5), UX Pattern Library & Calculator Specs (SG6), approved Design System & Page Templates (SG7.5), Compliance Constraint Log (SG1, expanded through SG5/6)

## 4. Outputs

- Page-by-Page Content Specification (one brief per sitemap page)
- Content Depth Standard (minimum word count/structural requirements by page type)
- Compliance Content Checklist (per page type)

## 5. Required Documents

`/08-content-spec/content-specifications-v1.md`, `/08-content-spec/content-depth-standard-v1.md`, `/08-content-spec/compliance-content-checklist-v1.md`

## 6. Responsible Roles

SEO Specialist (lead — content briefs must satisfy Stage Gate 5 architecture), Information Architect (structural consistency), Strategy Consultant (messaging pillar consistency)

## 7. Required Specialists

Copywriter (early consult — confirm briefs are actionable), Compliance Liaison (mandatory — confirm compliance content checklist is complete before Stage Gate 9 begins)

## 8. Decision Authority

Engagement Lead approves; no client sign-off required at this gate (client sees content at Stage Gate 9 review), but Compliance Liaison sign-off on the Compliance Content Checklist is mandatory.

## 9. Workflow

```
[1] For each sitemap page, draft a content brief: H1/heading outline,
    target keyword and intent (from SG5), required sections, internal
    linking targets (per SG5 cluster model), calculator/tool embed
    references (from SG6), and compliance requirements (from Compliance
    Constraint Log)
        │
        ▼
[2] Define Content Depth Standard by page type (pillar page vs. cluster
    page vs. location page vs. compliance page)
        │
        ▼
[3] Build Compliance Content Checklist per page type: required
    disclosures, NMLS display requirements, equal housing lending
    statement placement, state-specific licensing language
        │
        ▼
[4] Compliance Liaison review and sign-off
        │
        ▼
[5] Internal review → Exit Criteria → Stage Gate 9 scheduled
```

## 10. Checklist

- [ ] Every sitemap page has a completed content brief
- [ ] Every brief references its Stage Gate 5 primary keyword and search intent
- [ ] Every brief specifies internal linking targets consistent with the topical cluster model
- [ ] Content Depth Standard defined and applied consistently by page type
- [ ] Compliance Content Checklist completed and signed off by Compliance Liaison

## 11. Prompt(s)

**Prompt 8.1 — Page Content Brief Generation**

```
You are producing content briefs for [Client Name]'s mortgage website.
Using the attached sitemap, Keyword-to-Page Map, and UX Pattern Library,
produce a content brief for the page "[Page Name/URL]". Include:
- H1 and full heading outline (H2/H3)
- Primary keyword and search intent (from Keyword-to-Page Map)
- Required sections with a one-sentence purpose for each
- Internal linking targets (which pillar/cluster pages this should link
  to/from)
- Any calculator or interactive tool to embed (reference Stage Gate 6 spec)
- Compliance content requirements applicable to this page type (flag for
  Compliance Liaison confirmation rather than asserting final legal
  language yourself)
- Target word count range per the Content Depth Standard for this page type
```

**Prompt 8.2 — Compliance Content Checklist**

```
Using the Compliance Constraint Log accumulated through Stage Gates 1-6
for [Client Name], produce a Compliance Content Checklist organized by
page type (homepage, product page, location/state page, loan officer
profile, blog/guide, application/contact). For each page type, list every
disclosure, licensing statement, or required legal element that must
appear, and note whether placement is header/footer/inline. Flag any
item where you are inferring a requirement rather than citing it directly
from the Compliance Constraint Log, for Compliance Liaison confirmation.
```

## 12. Examples

*Sample content brief excerpt (state loan product page):*

> **Page:** `/loans/fha-loans/texas/` — **Primary keyword:** "FHA loans Texas" — **Intent:** Commercial. **Sections:** (1) H1 + intro answering "what is an FHA loan in Texas," (2) Texas-specific FHA loan limits table (by county, if applicable), (3) eligibility requirements, (4) down payment/credit score guidance, (5) embedded FHA affordability calculator (per SG6 spec), (6) FAQ block (schema-tagged per SG5 plan), (7) loan officer CTA card (Texas-licensed officer). **Compliance:** Texas-specific licensing statement in footer per Compliance Content Checklist; NMLS ID visible; equal housing lending logo/statement.

## 13. Common Mistakes

- Writing content briefs generically ("write about FHA loans") without page-specific differentiation, producing thin, duplicate-feeling content across similar pages (e.g., FHA loans across multiple states).
- Deferring compliance requirements to Stage Gate 9 or 11, which causes expensive copy rewrites after the fact.
- Ignoring the Content Depth Standard and allowing inconsistent depth across a topical cluster, weakening the cluster's collective SEO authority.

## 14. Best Practices

- Write each state/location page brief with at least one genuinely state-specific data point (loan limits, state housing programs, state-specific closing cost norms) — this is what prevents locational content from reading as templated.
- Have the Compliance Liaison review the Compliance Content Checklist against the actual current CFPB/state regulator guidance, not just prior-engagement templates, since requirements change.

## 15. Review Process

SEO Specialist and Copywriter jointly review briefs for actionability before Compliance Liaison sign-off; Engagement Lead approves the full specification.

## 16. Quality Assurance

Primary Eight-Dimension focus: **SEO**, **Scalability** (consistent brief quality across a growing page set).

## 17. Exit Criteria

- [ ] All Required Documents approved
- [ ] Compliance Liaison has signed off on the Compliance Content Checklist
- [ ] Copywriter confirms briefs are actionable without further clarification

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all three Required Documents saved v1.0
- Blueprint: "Content Inventory" section seeded with brief references (full content added at SG9)
- Decision Register: log Content Depth Standard thresholds as `DEC-SG8-001`

## 19. Future Enhancements

Briefs are executed in Stage Gate 9; the Content Depth Standard is reapplied to all new content proposed in Stage Gate 11.5.

---

# STAGE GATE 9 — COPYWRITING

## 1. Purpose

Produce final, approved on-page copy for every page in the sitemap, written to the Stage Gate 8 briefs, in the client's approved voice, cleared by compliance.

## 2. Business Objectives

- Deliver copy that converts anxious borrowers into qualified leads without overpromising or misleading.
- Maintain consistent voice and messaging pillar alignment across the full site.
- Achieve 100% compliance clearance before any copy is handed to Stage Gate 10 build.

## 3. Inputs

Page-by-Page Content Specifications (SG8), Positioning & Messaging Pillars (SG3), Compliance Content Checklist (SG8), Borrower Personas (SG1)

## 4. Outputs

- Final Approved Copy (per page, in Knowledge Base)
- Voice & Tone Guide
- Compliance Clearance Log (per page)

## 5. Required Documents

`/09-copywriting/final-copy/{page-slug}.md` (one file per page), `/09-copywriting/voice-tone-guide-v1.md`, `/09-copywriting/compliance-clearance-log-v1.md`

## 6. Responsible Roles

Copywriter (lead), Strategy Consultant (voice/pillar consistency review)

## 7. Required Specialists

SEO Specialist (on-page optimization review against SG5 keyword targets), Compliance Liaison (**mandatory, page-by-page sign-off** — no page copy is final without an entry in the Compliance Clearance Log)

## 8. Decision Authority

Client review of copy is recommended (particularly homepage, product pillar pages, and any page containing rate/APR examples) but not mandatory for every page; Compliance Liaison sign-off is mandatory for every page without exception.

## 9. Workflow

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
[4] Compliance Liaison review: page-by-page sign-off logged in
    Compliance Clearance Log
        │
        ▼
[5] Client review (recommended for key pages)
        │
        ▼
[6] Final copy locked → Exit Criteria → Stage Gate 10 scheduled
```

## 10. Checklist

- [ ] Voice & Tone Guide documented and applied consistently
- [ ] Every page has final copy matching its Stage Gate 8 brief structure
- [ ] Every page has an SEO Specialist on-page review completed (meta title/description, heading/keyword usage, internal links executed)
- [ ] Every page has a Compliance Clearance Log entry — no exceptions, including low-traffic or "boilerplate" pages
- [ ] No superlative, guarantee, or unsubstantiated claim language remains without compliance-approved qualifying language

## 11. Prompt(s)

**Prompt 9.1 — Page Copywriting**

```
You are the Copywriter for [Client Name], a mortgage lender. Using the
content brief for "[Page Name]" and the Voice & Tone Guide, write final
on-page copy. Requirements: address the persona's specific objection(s)
named in the brief; use the messaging pillars as the emotional/value
throughline, not as literal repeated phrases; write all headings per the
brief's heading outline; embed calls-to-action per the Stage Gate 6
conversion flow for this page; flag any statement about rates, approval
odds, timelines, or savings with "[COMPLIANCE REVIEW NEEDED]" rather than
asserting it as fact. Do not fabricate testimonials, statistics, or awards.
```

**Prompt 9.2 — Meta Title/Description Generation**

```
For the page "[Page Name/URL]" with primary keyword "[keyword]" and search
intent "[intent]", write 3 meta title options (50-60 characters) and 3
meta description options (140-155 characters) that include the primary
keyword naturally, reflect the positioning statement's value proposition,
and avoid any claim requiring compliance substantiation (no "lowest rates,"
"guaranteed approval," or similar language).
```

## 12. Examples

*Sample compliance-flagged copy line before clearance:*

> Draft: "Get approved in as little as 24 hours." → `[COMPLIANCE REVIEW NEEDED: timeline claim]` → Cleared version (per Compliance Liaison): "Many borrowers receive an initial decision within 1 business day after submitting a complete application.\*" with footnote disclosure per Compliance Liaison-approved language.

## 13. Common Mistakes

- Publishing AI-drafted copy without running it through the Compliance Liaison because it "reads fine" — compliance risk in mortgage advertising is a legal, not stylistic, judgment.
- Copy drifting from the approved Voice & Tone Guide as multiple contributors (human and AI) write different pages, without a Strategy Consultant consistency pass.
- Treating meta titles/descriptions as an afterthought rather than a Stage Gate 9 deliverable with the same compliance scrutiny as body copy.

## 14. Best Practices

- Run every AI-drafted page through a compliance-risk-flagging pass (Prompt 9.1's flagging instruction) before it ever reaches a human compliance reviewer — this makes the Compliance Liaison's job faster and more thorough.
- Maintain the Compliance Clearance Log as a page-by-page ledger, not a single "content approved" blanket statement, so any future compliance question about a specific page can be traced to exactly what was reviewed and when.

## 15. Review Process

SEO Specialist reviews for on-page optimization; Compliance Liaison reviews every page without exception; Strategy Consultant spot-checks a sample for voice consistency; client reviews key pages by invitation.

## 16. Quality Assurance

Primary Eight-Dimension focus: **Conversion**, **Brand**, **SEO**. Compliance is treated as a gating requirement layered on top of, not substituting for, the Eight-Dimension standard.

## 17. Exit Criteria

- [ ] All pages have final copy with Compliance Clearance Log entries
- [ ] Voice & Tone consistency confirmed
- [ ] SEO on-page review complete for all pages

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: final copy files saved v1.0 per page; Voice & Tone Guide and Compliance Clearance Log saved v1.0
- Blueprint: "Content Inventory" section finalized with approved copy references
- Decision Register: log any compliance-driven claim modifications as `DEC-SG9-00x` for future reference (protects against re-litigating the same claim question in future content additions)

## 19. Future Enhancements

Voice & Tone Guide and Compliance Clearance Log processes are reused unchanged for all Stage Gate 11.5 post-launch content additions.

---

# STAGE GATE 10 — AI BUILD PACKAGE

## 1. Purpose

Assemble the complete, unambiguous specification package that a developer or AI build model uses to construct the actual WordPress/GeneratePress/GenerateBlocks site — translating every prior Volume's approved output into implementation-ready instructions.

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
- Integration Requirements Spec (forms, calculators, CRM/LOS if applicable, analytics)

## 5. Required Documents

`/10-ai-build-package/build-package-v1.md`, `/10-ai-build-package/build-manifest-v1.md`, `/10-ai-build-package/component-pattern-mapping-v1.md`, `/10-ai-build-package/integration-requirements-v1.md`

## 6. Responsible Roles

Developer (lead), Visual Designer (design fidelity reference), SEO Specialist (technical SEO requirements carry-forward)

## 7. Required Specialists

AI Orchestrator (structuring the package for AI build-model consumption per the LLM Handoff Protocol, Volume I Sec. 9)

## 8. Decision Authority

Engagement Lead approves the package as complete and unambiguous before build begins; no client sign-off required at this gate (client already approved design at SG7.5 and copy at SG9).

## 9. Workflow

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
    tags (GA4, GTM, Clarity), any third-party integrations
        │
        ▼
[5] Internal completeness review → Exit Criteria → Stage Gate 10.5
    scheduled
```

## 10. Checklist

- [ ] Every sitemap page appears in the Build Manifest with its template, copy, schema, and URL
- [ ] Every component in the Stage Gate 7 library has a corresponding entry in the Component-to-Pattern Mapping
- [ ] Integration Requirements Spec covers all calculators, forms, analytics, and any LOS/CRM touchpoints in scope
- [ ] Package is structured so an AI build model, given this document plus the LLM Handoff Protocol context package, could implement a page correctly without additional clarification

## 11. Prompt(s)

**Prompt 10.1 — Build Manifest Generation**

```
You are assembling the AI Build Package for [Client Name]'s mortgage
website. Using the approved sitemap, final copy files, schema plan, and
component library, produce a Page-by-Page Build Manifest as a table with
columns: Page URL, Template Type (reference Stage Gate 7 template names),
Copy File Reference, Schema Types Required, Primary Components Used,
Internal Links Required (from Stage Gate 5 cluster model). Flag any page
where required inputs are incomplete rather than guessing at placeholder
content.
```

**Prompt 10.2 — Component-to-Pattern Mapping**

```
For each component in the Stage Gate 7 Component Library, specify its
GenerateBlocks implementation: block type composition (Container/Grid/
Button/Query Loop/etc.), required CSS classes tied to Global Style tokens,
responsive behavior at each breakpoint, and any dynamic data source
(e.g., loan officer directory via Query Loop against a custom post type).
This mapping will be handed to a developer or AI build model as the
authoritative implementation reference — be exact, not descriptive.
```

## 12. Examples

*Sample Build Manifest row:*

| Page URL | Template | Copy Ref | Schema | Components | Internal Links |
|---|---|---|---|---|---|
| `/loans/fha-loans/texas/` | State Product Page | `09-copywriting/final-copy/fha-loans-texas.md` | Service, LocalBusiness, FAQPage, BreadcrumbList | Hero, Calculator Module, FAQ Accordion, Loan Officer CTA Card | → `/loans/fha-loans/` (pillar), → `/first-time-home-buyer/` (persona hub) |

## 13. Common Mistakes

- Handing a build model the design and copy separately without a consolidated manifest, forcing it to infer relationships that should have been made explicit.
- Omitting analytics/tag requirements from the Integration Requirements Spec, resulting in a launched site with no measurement instrumentation (directly undermining Stage Gate 11.5).
- Failing to flag incomplete inputs (e.g., a missing loan officer bio) and instead allowing an AI build model to fabricate placeholder content that accidentally ships to production.

## 14. Best Practices

- Structure the Build Package explicitly for the LLM Handoff Protocol (Volume I Sec. 9) — include the Charter, History (relevant Decision Register entries), State (current Blueprint), and Task layers together rather than assuming the build model has separate access to them.
- Version the Build Manifest so that any mid-build scope addition is a tracked, deliberate change rather than an informal request.

## 15. Review Process

Engagement Lead and Developer jointly review the package for completeness against the Checklist before build begins.

## 16. Quality Assurance

Primary Eight-Dimension focus: **AI Implementation Readiness**, **Maintainability**, **WordPress/GeneratePress/GenerateBlocks Compatibility**.

## 17. Exit Criteria

- [ ] All Required Documents complete and internally reviewed
- [ ] No incomplete inputs remain unflagged
- [ ] Developer confirms the package is sufficient to begin build without further clarification requests

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents saved v1.0
- Blueprint: "Technical Build Spec" section seeded (finalized at SG10.5)
- Decision Register: log any build-sequencing decisions (e.g., phased launch order) as `DEC-SG10-00x`

## 19. Future Enhancements

The Build Package is the direct input to Stage Gate 10.5, where it is executed into an actual WordPress/GeneratePress/GenerateBlocks build.

---

# STAGE GATE 10.5 — WORDPRESS IMPLEMENTATION BLUEPRINT

## 1. Purpose

Execute the AI Build Package into an actual, functioning WordPress/GeneratePress Premium/GenerateBlocks Pro site on the default (or Charter-specified) technology stack, with performance, caching, and security layers correctly configured.

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

Engagement Lead approves staging build as ready for Stage Gate 11 QA; no client sign-off at this specific gate (client sees the site formally at QA/launch).

## 9. Workflow

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
[9] Internal smoke test → Exit Criteria → Stage Gate 11 scheduled
```

## 10. Checklist

- [ ] WordPress + GeneratePress Premium + GenerateBlocks Pro + GenerateCloud provisioned and licensed correctly
- [ ] Global Styles match Design System Specification exactly (spot-check color/type tokens)
- [ ] Every page in the Build Manifest exists on staging with correct copy, schema, and internal links
- [ ] Rank Math configuration matches Schema Markup Plan (spot-check structured data via a validator)
- [ ] LiteSpeed Cache configured; Core Web Vitals targets tested on staging
- [ ] Cloudflare DNS, CDN, and security rules configured
- [ ] GA4, Search Console, GTM, and Clarity all verified firing correctly on staging
- [ ] Staging environment access provided to QA Analyst

## 11. Prompt(s)

**Prompt 10.5.1 — Build Execution (Code-Generation Model)**

```
You are implementing a WordPress page using GenerateBlocks Pro for
[Client Name]'s mortgage website. Using the Build Manifest entry for
"[Page URL]" and the Component-to-Pattern Mapping, generate the
GenerateBlocks pattern structure (as block markup/JSON per GenerateBlocks'
format) for this page. Use only Global Style token references (no
hardcoded hex colors or font sizes). Insert the approved copy from
"[copy file reference]" exactly as written — do not paraphrase or
regenerate copy that has already cleared compliance review.
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

## 12. Examples

*Sample Performance Configuration Record excerpt:*

| Setting | Value | Rationale |
|---|---|---|
| LiteSpeed Cache — Image Optimization | WebP conversion enabled, lazy load below fold | Reduces LCP on image-heavy homepage hero |
| LiteSpeed Cache — CSS/JS | Combine + minify, critical CSS generation enabled | Reduces render-blocking resources |
| Cloudflare — Caching Level | Standard, with Page Rules caching static assets aggressively | Reduces server load, improves TTFB |
| Cloudflare — Rocket Loader | Disabled | Conflicted with GenerateBlocks interactive calculator scripts in testing; documented as a known incompatibility |

## 13. Common Mistakes

- Enabling aggressive caching/minification defaults without testing calculator and form functionality, which can silently break interactive tools.
- Deploying without verifying Rank Math schema output against a structured data validator, shipping malformed schema that fails to earn rich results.
- Skipping GA4/GTM/Clarity verification, discovering at Stage Gate 11.5 that months of traffic went unmeasured.

## 14. Best Practices

- Always test LiteSpeed Cache and Cloudflare optimization settings against every interactive element (calculators, multi-step forms) before finalizing — performance settings and JavaScript-dependent UX are a common conflict point.
- Document every non-default configuration decision (like the Rocket Loader example above) in the Performance Configuration Record so a future maintainer understands why a setting deviates from platform defaults.
- Use GenerateCloud to sync the Global Styles and pattern library, so future multi-site or template reuse across engagements is possible.

## 15. Review Process

Developer self-tests against the Checklist; SEO Specialist independently validates schema output; Engagement Lead confirms staging is ready for formal QA.

## 16. Quality Assurance

Primary Eight-Dimension focus: **Performance**, **WordPress/GeneratePress/GenerateBlocks Compatibility**, **Maintainability**.

## 17. Exit Criteria

- [ ] All Required Documents complete
- [ ] Staging site passes internal smoke test (all pages load, all forms/calculators function, analytics fire)
- [ ] SEO Specialist has validated schema implementation

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all Required Documents saved v1.0; staging URL logged in Project Memory
- Blueprint: "Technical Build Spec" section finalized with actual configuration record
- Decision Register: log any deviation from default stack configuration (e.g., the Rocket Loader example) as `DEC-SG10.5-00x`

## 19. Future Enhancements

This build is the subject of Stage Gate 11 formal QA and becomes the production site upon successful launch. Configuration records are referenced again during Stage Gate 11.5 growth-program technical changes.

---

# STAGE GATE 11 — QUALITY ASSURANCE

## 1. Purpose

Formally validate the staged website against every standard set across the engagement — functional, performance, accessibility, SEO, compliance, and brand fidelity — before go-live authorization.

## 2. Business Objectives

- Catch and remediate defects before they reach borrowers or search engines index a flawed site.
- Provide the client with an evidence-based go-live recommendation, not a subjective "looks ready" assessment.
- Establish the compliance sign-off record required before any regulated financial services site goes live.

## 3. Inputs

Staging site (SG10.5), all prior Stage Gate approved specifications (used as the QA reference standard), Compliance Clearance Log (SG9)

## 4. Outputs

- QA Test Report (functional, performance, accessibility, SEO)
- Compliance Sign-Off Record (final, site-wide)
- Issue Log (defects found, severity, remediation status)
- Go-Live Recommendation

## 5. Required Documents

`/11-qa/qa-test-report-v1.md`, `/11-qa/compliance-signoff-record-v1.md`, `/11-qa/issue-log-v1.md`, `/11-qa/go-live-recommendation-v1.md`

## 6. Responsible Roles

QA Analyst (lead), Developer (remediation), SEO Specialist (SEO QA), Visual Designer (design fidelity QA)

## 7. Required Specialists

Compliance Liaison (**mandatory final sign-off** — this is the last compliance gate before launch)

## 8. Decision Authority

**Client sign-off required for go-live.** The named Decision Authority approves the Go-Live Recommendation; Compliance Liaison sign-off on the Compliance Sign-Off Record is a hard prerequisite that cannot be waived regardless of client urgency.

## 9. Workflow

```
[1] Functional QA: every form, calculator, navigation path, and
    integration tested against the Build Manifest and Conversion Flows
        │
        ▼
[2] Performance QA: Core Web Vitals tested on production-equivalent
    staging across representative templates (mobile + desktop)
        │
        ▼
[3] Accessibility QA: automated scan + manual keyboard/screen-reader
    testing against WCAG 2.1 AA
        │
        ▼
[4] SEO QA: schema validation, meta tag audit, internal linking audit,
    XML sitemap/robots.txt verification, indexation settings check
        │
        ▼
[5] Design Fidelity QA: staging compared page-by-page against Stage
    Gate 7.5 approved design system
        │
        ▼
[6] Compliance QA: final site-wide review against Compliance Clearance
    Log and Compliance Content Checklist
        │
        ▼
[7] Issue Log compiled, severity-rated, remediated, re-tested
        │
        ▼
[8] Go-Live Recommendation drafted → client review → sign-off
```

## 10. Checklist

- [ ] Every form and calculator tested for correct function, validation, and error states
- [ ] Core Web Vitals pass targets on representative templates, mobile and desktop
- [ ] Automated accessibility scan shows no critical/serious WCAG 2.1 AA violations; manual keyboard navigation confirmed functional site-wide
- [ ] Schema markup validated (no errors) via structured data testing tool
- [ ] XML sitemap submitted-ready, robots.txt correct, no unintended noindex tags
- [ ] Design fidelity spot-checked against approved templates for every page type
- [ ] Compliance Liaison has completed final site-wide Compliance Sign-Off Record
- [ ] All P0/P1 Issue Log items remediated and re-tested; any open P2 items documented with client-accepted risk

## 11. Prompt(s)

**Prompt 11.1 — QA Test Plan Generation**

```
You are the QA Analyst for [Client Name]'s mortgage website launch.
Using the Build Manifest and Conversion Flow diagrams, generate a
functional test plan covering every form, calculator, and primary
navigation path. For each test case, specify: the action taken, the
expected result, and the pass/fail criteria. Include edge cases (invalid
input handling, required field validation, mobile viewport behavior) for
every calculator and lead capture form.
```

**Prompt 11.2 — Issue Log Triage**

```
Given the attached raw QA findings for [Client Name]'s site, organize them
into an Issue Log with columns: Issue ID, Description, Page/Location,
Category (Functional/Performance/Accessibility/SEO/Compliance/Design),
Severity (P0 = blocks launch, P1 = fix before launch if feasible,
P2 = post-launch acceptable), and a recommended remediation. Flag any
compliance-category issue as automatically P0 regardless of apparent
severity.
```

## 12. Examples

*Sample Issue Log entry:*

| Issue ID | Description | Page | Category | Severity | Remediation |
|---|---|---|---|---|---|
| ISS-014 | NMLS ID not visible in footer on mobile viewport (hidden behind collapsed menu) | Site-wide (mobile) | Compliance | P0 | Move NMLS ID display outside collapsible footer menu; re-test on 3 device widths |

## 13. Common Mistakes

- Treating compliance issues as negotiable severity based on launch timeline pressure — compliance issues are categorically P0 in this methodology.
- Testing only on desktop, missing mobile-specific defects (a majority of mortgage research traffic is mobile).
- Allowing "it looks done" to substitute for the structured test plan — undocumented QA is not defensible if a defect surfaces post-launch.

## 14. Best Practices

- Run accessibility and compliance QA as dedicated passes, not folded into general functional testing, since they require different expertise and a different failure tolerance (zero for compliance).
- Re-test every remediated P0/P1 issue explicitly rather than assuming a fix worked — regression risk is real, especially with caching layers involved.
- Present the Go-Live Recommendation with the full Issue Log attached, including any client-accepted P2 risk, so the launch decision is fully informed and documented.

## 15. Review Process

QA Analyst compiles findings; Engagement Lead reviews Issue Log severity ratings; Compliance Liaison independently completes final sign-off; client reviews Go-Live Recommendation for final approval.

## 16. Quality Assurance

This gate formally re-verifies all Eight Dimensions (Volume I Sec. 12.2) site-wide — it is the methodology's final comprehensive checkpoint.

## 17. Exit Criteria

- [ ] All Required Documents complete
- [ ] Compliance Sign-Off Record completed and signed
- [ ] All P0 issues remediated and re-tested; no open P0 items
- [ ] Client has approved Go-Live Recommendation

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents saved v1.0
- Blueprint: "QA Status" section finalized with sign-off record
- Decision Register: log go-live approval as `DEC-SG11-001`; log any client-accepted open P2 risk explicitly as `DEC-SG11-002`

## 19. Future Enhancements

Post-launch, the QA test plan is reused for regression testing after any Stage Gate 11.5 growth-program change.

---

# STAGE GATE 11.5 — POST-LAUNCH GROWTH PROGRAM

## 1. Purpose

Establish the structured, data-driven optimization program for the first 90 days (and ongoing) after launch — closing the loop from strategic hypothesis (Volume II) through measured real-world performance.

## 2. Business Objectives

- Validate or invalidate the personas, positioning, and conversion assumptions made in Volumes II–IV against real behavioral data.
- Establish a KPI dashboard and experiment cadence so improvement is continuous rather than one-time.
- Feed validated learnings back into the Knowledge Base for reuse in future MWEF engagements.

## 3. Inputs

Live production site, GA4/Search Console/Clarity data (accumulating from launch), Success Metrics defined in Project Charter, Master Website Blueprint (full, as of launch)

## 4. Outputs

- 90-Day Growth Program Plan
- KPI Dashboard Specification
- Experiment Log (A/B or sequential test tracking)
- Engagement Retrospective & Methodology Learnings Memo

## 5. Required Documents

`/11.5-post-launch/growth-program-plan-v1.md`, `/11.5-post-launch/kpi-dashboard-spec-v1.md`, `/11.5-post-launch/experiment-log-v1.md`, `/11.5-post-launch/retrospective-learnings-v1.md`

## 6. Responsible Roles

Strategy Consultant (lead — reconnects growth work to original strategic hypotheses), SEO Specialist (ranking/traffic monitoring), UX Designer (conversion experiment design)

## 7. Required Specialists

Developer (implement experiment variants), Compliance Liaison (review any new content/experiment copy per the same standard as Stage Gate 9)

## 8. Decision Authority

Engagement Lead approves the Growth Program Plan; ongoing experiment decisions follow the same Decision Register discipline as the rest of the engagement, with client informed per the cadence set in the Project Charter.

## 9. Workflow

```
[1] Confirm KPI Dashboard is correctly capturing Success Metrics from
    the Project Charter (traffic, conversion rate, ranking positions,
    Core Web Vitals in production)
        │
        ▼
[2] Baseline first 2-4 weeks of production data
        │
        ▼
[3] Compare actual borrower behavior against Stage Gate 1 personas and
    Stage Gate 3 positioning assumptions; note confirmations and
    surprises
        │
        ▼
[4] Prioritize a 90-day experiment roadmap (content additions, UX
    refinements, new topical cluster expansion) using the same Content
    Depth Standard (SG8) and Design System (SG7.5) discipline —
    no ad hoc changes outside the governed system
        │
        ▼
[5] Execute experiments; log each in the Experiment Log with hypothesis,
    result, and decision
        │
        ▼
[6] At 90 days (or Charter-defined interval), produce the Engagement
    Retrospective & Methodology Learnings Memo
```

## 10. Checklist

- [ ] KPI Dashboard verified accurate against Project Charter Success Metrics
- [ ] Baseline production data captured before first experiment begins
- [ ] Every experiment logged with a clear hypothesis and success criterion before it starts, not just a result after the fact
- [ ] Any new content follows Stage Gate 8/9 discipline (brief → compliance-cleared copy), not ad hoc publishing
- [ ] Retrospective Memo completed and submitted to the firm's Knowledge Base for cross-engagement reuse

## 11. Prompt(s)

**Prompt 11.5.1 — Growth Program Prioritization**

```
Using production KPI data from [Client Name]'s first 30 days live, the
original Borrower Personas (Stage Gate 1), and the Keyword-to-Page Map
(Stage Gate 5), identify: (1) which personas' behavior matched
predictions and which diverged, citing specific metrics; (2) which
topical clusters are underperforming their keyword targets and why
(ranking, content depth, or technical issue); (3) 3-5 prioritized
experiment or content-expansion recommendations with a stated hypothesis
and success metric for each. Do not recommend a full redesign or
repositioning without explicit evidence of a fundamental strategic
mismatch — prefer incremental, testable changes.
```

**Prompt 11.5.2 — Retrospective & Methodology Learnings**

```
Produce an Engagement Retrospective for [Client Name]'s MWEF engagement.
Cover: what strategic assumptions from Stage Gate 3 were validated or
invalidated by post-launch data; which Stage Gates ran smoothly vs. which
caused rework, and why; any methodology improvement recommendation for
future MWEF engagements (to be submitted as a Change Request per Volume I
Section 13.2, not applied unilaterally to this manual).
```

## 12. Examples

*Sample Experiment Log entry:*

| Experiment ID | Hypothesis | Change | Success Metric | Result | Decision |
|---|---|---|---|---|---|
| EXP-003 | Removing the phone-number-required field from the FHA calculator's first step will reduce abandonment | A/B test: calculator with email-only first step vs. control (email+phone) | Calculator completion rate | Variant: +18% completion, lead quality unchanged per loan officer follow-up | Ship variant site-wide; log as `DEC-SG11.5-004` |

## 13. Common Mistakes

- Making design or content changes directly on production without following the same brief/compliance discipline used pre-launch, quietly eroding the governance system the whole engagement was built on.
- Running experiments without a predefined success metric, leading to post-hoc rationalization of whatever happened.
- Treating the Retrospective Memo as optional paperwork rather than the mechanism that makes the next MWEF engagement better than this one.

## 14. Best Practices

- Treat every post-launch content addition as a miniature Stage Gate 8→9 cycle — brief, compliance clearance, then publish — never skip steps because the site is already live.
- Feed every validated learning (both confirmations and surprises) back to the firm's cross-engagement Knowledge Base, tagged by lender type and market, so future Stage Gate 1 Discovery work starts from a stronger evidence base.

## 15. Review Process

Strategy Consultant and Engagement Lead review the Growth Program Plan and Experiment Log at each Charter-defined reporting interval; Compliance Liaison reviews any new content or experiment copy exactly as in Stage Gate 9.

## 16. Quality Assurance

All Eight Dimensions remain in force for any new work produced during this gate; performance and SEO dimensions are additionally now measured against real data rather than projections.

## 17. Exit Criteria

This gate does not "close" in the same sense as prior gates — it establishes an ongoing program. Its formal completion checkpoint (typically at 90 days or the Charter-defined interval) requires:

- [ ] KPI Dashboard operating and reviewed at agreed cadence
- [ ] At minimum 3 experiments logged with documented results
- [ ] Retrospective & Methodology Learnings Memo submitted

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents maintained as living documents, versioned per Volume I Section 11
- Blueprint: "Growth Program" section populated and continuously updated
- Decision Register: every shipped experiment logged as a standard Decision Register entry

## 19. Future Enhancements

The Retrospective Memo feeds the firm's Change Request process (Volume I Sec. 13.2) for this manual itself, and the accumulated cross-engagement learnings inform future Stage Gate 1 and Stage Gate 2 research more efficiently over time — this is the mechanism by which MWEF becomes more valuable with every engagement run.

---

*End of Volume V. Continue to Volume VI — Reusable Templates.*
