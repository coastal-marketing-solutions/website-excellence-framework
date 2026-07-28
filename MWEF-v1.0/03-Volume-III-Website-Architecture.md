# VOLUME III — WEBSITE ARCHITECTURE

*Mortgage Website Excellence Framework (MWEF) v1.0*

---

## Volume Introduction

Volume III converts the approved Strategic Direction (Stage Gate 3) into the structural backbone of the website: its information architecture, its SEO blueprint, and its UX/conversion flows. Every Stage Gate in this Volume follows the fixed 19-part template defined in Volume II's introduction. Decisions made here are foundational — reversing an approved sitemap or keyword architecture after Stage Gate 7 begins is a costly, major-version change requiring a formal Change Request.

---

# STAGE GATE 4 — INFORMATION ARCHITECTURE

## 1. Purpose

Design the complete page hierarchy, navigation structure, URL scheme, and content taxonomy for the website, translating the approved positioning and persona priorities into a structure a borrower can navigate intuitively and a search engine can crawl and understand cleanly.

## 2. Business Objectives

- Ensure every priority persona and loan product has a clear, discoverable path from entry to conversion.
- Build a taxonomy that supports topical authority (Stage Gate 5) rather than a flat, disconnected page list.
- Set a URL structure that is stable, semantic, and scalable to the site's projected 3–5 year page count.

## 3. Inputs

Strategic Direction Brief, Positioning Statement, Persona/Product Priority Matrix, White Space Opportunity Map, Compliance Constraint Log

## 4. Outputs

- Full Sitemap (hierarchical)
- URL Structure Standard
- Navigation Model (primary, footer, utility nav)
- Content Taxonomy (categories, tags, entity relationships)

## 5. Required Documents

`/04-architecture/sitemap-v1.md`, `/04-architecture/url-structure-standard-v1.md`, `/04-architecture/navigation-model-v1.md`, `/04-architecture/content-taxonomy-v1.md`

## 6. Responsible Roles

Information Architect (lead), SEO Specialist (taxonomy/URL structure co-owner), Strategy Consultant (persona-path validation)

## 7. Required Specialists

UX Designer (early consult on navigation usability), Compliance Liaison (confirm required disclosure pages: licensing page, NMLS Consumer Access link, state-specific disclosures, privacy/accessibility policy pages)

## 8. Decision Authority

Engagement Lead approves; client review recommended but not mandatory sign-off (mandatory sign-off resumes at Stage Gate 6 exit and Stage Gate 7.5).

## 9. Workflow

```
[1] List all required page types: core (home, about, contact), product
    (loan program pages), persona-path (first-time buyer hub, refinance hub),
    location (state/market pages if multi-state), resource (blog/guides),
    compliance (licensing, disclosures, privacy, accessibility)
        │
        ▼
[2] Group pages into a hierarchy reflecting topical clusters (see Stage
    Gate 5 pillar/cluster model) rather than a flat list
        │
        ▼
[3] Draft URL Structure Standard (see Sec. 12 example pattern)
        │
        ▼
[4] Design primary navigation (max depth and item count per usability
    best practice — see Sec. 14) and footer/utility navigation
        │
        ▼
[5] Define content taxonomy: categories, tags, and entity relationships
    (e.g., "FHA Loans" entity relates to "First-Time Buyer" persona hub
    and "[State] FHA Loan Limits" location page)
        │
        ▼
[6] Internal review → Exit Criteria → Stage Gate 5 scheduled
```

## 10. Checklist

- [ ] Every priority persona (Stage Gate 3) has a clear top-level path in the sitemap
- [ ] Every loan product in scope has a dedicated page or hub
- [ ] All compliance-required pages are present (licensing, NMLS link, state disclosures, privacy policy, accessibility statement, equal housing lending statement)
- [ ] URL Structure Standard is documented and consistent (no mixed patterns)
- [ ] Primary navigation tested against a "3-click rule" — any priority page reachable within 3 clicks from homepage
- [ ] Taxonomy supports topical clustering for Stage Gate 5 (no orphaned pages with no cluster relationship)

## 11. Prompt(s)

**Prompt 4.1 — Sitemap Generation**

```
You are the Information Architect for [Client Name], a mortgage lender
licensed in [states]. Using the attached Strategic Direction Brief, Persona
Priority Matrix, and Compliance Constraint Log, produce a complete
hierarchical sitemap.

Requirements:
- Organize around topical clusters (pillar pages + supporting cluster pages),
  not a flat list
- Include a dedicated hub page for each priority persona identified
- Include a dedicated page for each loan product in scope
- Include all compliance-required pages: NMLS/licensing page, state-specific
  disclosure pages for each licensed state, privacy policy, accessibility
  statement, equal housing lender statement
- Note page depth (how many clicks from home) for each entry
- Flag any page you believe is required for compliance but did not appear
  in the Compliance Constraint Log, for review by the Compliance Liaison
```

**Prompt 4.2 — URL Structure Standard**

```
Given the sitemap above, propose a URL structure standard for [Client
Name]'s WordPress/GeneratePress site. Rules: lowercase, hyphenated, no
stop-word bloat, reflect the topical hierarchy (e.g.,
/loans/fha-loans/[state]/ pattern for location-nested product pages),
stable under future page additions. Provide the full URL for every page
in the sitemap and flag any URL over 60 characters for review.
```

## 12. Examples

*Sample URL Structure Standard excerpt:*

| Page Type | Pattern | Example |
|---|---|---|
| Loan product pillar | `/loans/{product}/` | `/loans/fha-loans/` |
| Product + state cluster | `/loans/{product}/{state}/` | `/loans/fha-loans/texas/` |
| Persona hub | `/{persona-path}/` | `/first-time-home-buyer/` |
| Resource/guide | `/guides/{slug}/` | `/guides/how-much-down-payment-fha/` |
| Compliance | `/legal/{slug}/` | `/legal/licensing-disclosures/` |

## 13. Common Mistakes

- Building navigation around internal company structure (departments, loan officer teams) instead of borrower mental models.
- Flat sitemaps with no pillar/cluster relationship, which undermines the entire Stage Gate 5 SEO strategy.
- Forgetting state-specific disclosure pages for every licensed state, not just the client's headquarters state.
- URL structures mixing patterns (`/fha-loan/` vs `/loans/va/`) inconsistently.

## 14. Best Practices

- Apply a 7±2 item limit to primary navigation; push depth into mega-menus or hub pages rather than a flat wide navbar.
- Design the taxonomy before the sitemap is finalized — taxonomy-first prevents orphaned pages.
- Validate the "3-click rule" explicitly for every persona's priority conversion path, not just structurally for all pages.

## 15. Review Process

Engagement Lead and SEO Specialist jointly review the sitemap against the Checklist; Compliance Liaison independently confirms all required compliance pages are present before sign-off.

## 16. Quality Assurance

Primary Eight-Dimension focus: **SEO**, **Scalability**, **Maintainability**. Secondary: **Conversion** (path clarity).

## 17. Exit Criteria

- [ ] Sitemap, URL Structure Standard, Navigation Model, and Content Taxonomy approved by Engagement Lead
- [ ] Compliance Liaison has confirmed all required compliance pages present
- [ ] No orphaned pages in the taxonomy

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents saved v1.0
- Blueprint: "Sitemap & IA" section populated in full
- Decision Register: log final navigation model choice and any rejected alternatives as `DEC-SG4-00x`

## 19. Future Enhancements

The sitemap is extended (not restructured) in Stage Gate 5 as topical clusters are fully mapped to keywords, and again in Stage Gate 11.5 as new content is added post-launch under the same taxonomy rules.

---

# STAGE GATE 5 — SEO BLUEPRINT

## 1. Purpose

Build the complete search visibility architecture for the site: keyword-to-page mapping, topical cluster strategy, technical SEO requirements, schema markup plan, and AI-search (LLM-citation) optimization approach.

## 2. Business Objectives

- Ensure every page in the Stage Gate 4 sitemap has a defined keyword and search-intent purpose — no page exists without a search rationale.
- Build genuine topical authority in the client's specific loan product and geographic niches, rather than shallow coverage across too many topics.
- Position content to be citable by AI-mediated search (ChatGPT, Google AI Overviews, Perplexity, etc.), not only classic 10-blue-links SEO.

## 3. Inputs

Sitemap & Content Taxonomy (Stage Gate 4), Competitive Intelligence Report (Stage Gate 2), Positioning & Messaging Pillars (Stage Gate 3)

## 4. Outputs

- Keyword-to-Page Map
- Topical Cluster Model (pillar/cluster diagram)
- Technical SEO Requirements Spec
- Schema Markup Plan
- Entity SEO & AI Search Optimization Brief

## 5. Required Documents

`/05-seo-blueprint/keyword-map-v1.md`, `/05-seo-blueprint/topical-cluster-model-v1.md`, `/05-seo-blueprint/technical-seo-spec-v1.md`, `/05-seo-blueprint/schema-plan-v1.md`, `/05-seo-blueprint/entity-ai-search-brief-v1.md`

## 6. Responsible Roles

SEO Specialist (lead), Information Architect (cluster/sitemap alignment), Research Consultant (keyword research support)

## 7. Required Specialists

Developer (early consult — confirm Rank Math + GeneratePress technical constraints), Compliance Liaison (confirm no keyword targeting implies rate guarantees or unsubstantiated claims)

## 8. Decision Authority

Engagement Lead approves; this Blueprint becomes binding input to Stage Gate 8 (Content Specification) and cannot be materially altered afterward without a Change Request.

## 9. Workflow

```
[1] Keyword research per persona/product/location combination from the
    sitemap
        │
        ▼
[2] Map every sitemap page to a primary keyword + 3-5 secondary
    keywords + defined search intent
        │
        ▼
[3] Build the Topical Cluster Model: identify pillar pages and their
    supporting cluster pages, with internal linking relationships
        │
        ▼
[4] Define Technical SEO Requirements: crawlability, indexation rules,
    canonicalization, mobile-first requirements, Core Web Vitals targets
        │
        ▼
[5] Define Schema Markup Plan per page type (see Sec. 12)
        │
        ▼
[6] Draft Entity SEO & AI Search Optimization Brief: how the site
    establishes clear entity identity (organization, people, products) for
    both classic and AI-mediated search
        │
        ▼
[7] Internal review → Exit Criteria → Stage Gate 6 scheduled
```

## 10. Checklist

- [ ] Every sitemap page has a mapped primary keyword and defined search intent
- [ ] Topical Cluster Model shows explicit pillar → cluster → internal link relationships
- [ ] Technical SEO Requirements Spec includes Core Web Vitals targets (LCP < 2.5s, INP < 200ms, CLS < 0.1) as binding requirements for Stage Gate 10
- [ ] Schema Markup Plan covers Organization, LocalBusiness (per licensed location), FAQPage, Person (loan officers), BreadcrumbList, and Article/WebPage as applicable
- [ ] Entity SEO Brief addresses how NMLS ID, licensing entities, and loan officer credentials establish machine-readable trust signals
- [ ] No keyword target implies a claim requiring compliance substantiation without a flag for Stage Gate 9 content review

## 11. Prompt(s)

**Prompt 5.1 — Keyword-to-Page Mapping**

```
You are the SEO Specialist for [Client Name], a mortgage lender licensed in
[states]. Using the attached sitemap and Competitive Intelligence Report,
produce a keyword-to-page map. For each page, provide: primary keyword,
3-5 secondary keywords, search intent (informational/commercial/
transactional/navigational), estimated competitiveness (low/medium/high
based on competitor content depth observed in Stage Gate 2), and a one-
sentence content angle that differentiates from what competitors currently
rank with.

Do not fabricate search volume figures; if volume data is not provided,
label estimates as "[unverified estimate]" or omit them.
```

**Prompt 5.2 — Topical Cluster Model**

```
Using the keyword-to-page map above, group pages into topical clusters:
identify pillar pages (broad, high-value pages meant to rank for head
terms and link out to supporting content) and cluster pages (specific,
long-tail pages that link back to their pillar). Produce a cluster diagram
(text/ASCII acceptable) showing pillar-to-cluster and cluster-to-cluster
internal linking relationships for at least the top 3 clusters by business
priority.
```

**Prompt 5.3 — Schema Markup Plan**

```
Produce a schema.org markup plan for [Client Name]'s mortgage website
covering: Organization/FinancialService schema for the homepage,
LocalBusiness schema for each licensed branch/state, Person schema for
loan officer profile pages (include NMLS ID as an identifier property),
FAQPage schema for guide/FAQ content, BreadcrumbList for all deep pages,
and Article schema for blog/guide content. For each schema type, list the
required and recommended properties and note any properties requiring
data the client has not yet provided.
```

## 12. Examples

*Sample Schema Markup Plan row:*

| Page Type | Schema Type | Key Properties | Notes |
|---|---|---|---|
| Loan Officer Profile | Person + FinancialService (employee of) | name, jobTitle, telephone, identifier (NMLS ID), worksFor | NMLS ID must be displayed as visible text per compliance, in addition to schema |
| State Loan Product Page | Service + LocalBusiness (areaServed) | areaServed (state), provider, serviceType | Pair with FAQPage schema for state-specific loan limit Q&A |

## 13. Common Mistakes

- Targeting high-volume, high-competition head terms (e.g., "mortgage rates") that a client with limited domain authority cannot realistically compete for, at the expense of winnable long-tail/local terms.
- Treating schema markup as a technical afterthought for Stage Gate 10 rather than specifying it here, where it should influence content structure decisions in Stage Gate 8.
- Omitting the Entity SEO Brief, leaving the site with no deliberate strategy for AI-mediated search visibility.

## 14. Best Practices

- Prioritize topical depth in the client's specific licensed states and specialty products over broad national keyword coverage the client cannot substantiate operationally.
- Build the Entity SEO Brief around making the organization, its licensing, and its loan officers unambiguously machine-readable — this is what allows AI search systems to cite the site confidently as a source.
- Cross-check every keyword target against the Compliance Constraint Log before finalizing — "no closing cost" or "guaranteed approval" style keyword targets are compliance risks, not just content risks.

## 15. Review Process

SEO Specialist and Information Architect jointly review the cluster model for structural consistency with the Stage Gate 4 sitemap; Developer reviews Technical SEO Requirements for GeneratePress/Rank Math feasibility; Compliance Liaison scans keyword targets for claim risk.

## 16. Quality Assurance

Primary Eight-Dimension focus: **SEO** (this gate's core output), **Scalability**, **AI Implementation Readiness** (schema/technical spec must be precise enough for Stage Gate 10 build).

## 17. Exit Criteria

- [ ] All five Required Documents approved by Engagement Lead
- [ ] Compliance Liaison has cleared keyword targets for claim risk
- [ ] Developer has confirmed Technical SEO Requirements are buildable on the default stack (or alternative per Charter)

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all five Required Documents saved v1.0
- Blueprint: "SEO Architecture" section populated in full
- Decision Register: log cluster prioritization decisions (which clusters are Phase 1 vs. Phase 2) as `DEC-SG5-00x`

## 19. Future Enhancements

The Keyword-to-Page Map and Schema Plan are directly consumed by Stage Gate 8 (Content Specification) and Stage Gate 10.5 (WordPress Implementation Blueprint). Cluster performance is measured and the model is extended in Stage Gate 11.5.

---

# STAGE GATE 6 — UX & CONVERSION

## 1. Purpose

Design the borrower-facing user experience: primary conversion flows (rate quote, pre-qualification, application start, contact/schedule), page-level UX patterns, and the friction-reduction mechanics that convert anonymous traffic into qualified leads.

## 2. Business Objectives

- Minimize friction in the path from landing page to qualified lead action for each priority persona.
- Define calculator and interactive tool specifications that serve genuine borrower decision-making (not just lead-capture bait).
- Establish trust-building UX patterns appropriate to a regulated financial product.

## 3. Inputs

Sitemap & Navigation Model (Stage Gate 4), Keyword-to-Page Map (Stage Gate 5), Borrower Personas (Stage Gate 1), Positioning & Messaging Pillars (Stage Gate 3)

## 4. Outputs

- Primary Conversion Flow Diagrams (one per priority persona/product combination)
- Calculator & Interactive Tool Specifications
- Page-Level UX Pattern Library (wireframe-level, pre-visual-design)
- Trust Signal Placement Plan

## 5. Required Documents

`/06-ux-conversion/conversion-flows-v1.md`, `/06-ux-conversion/calculator-specs-v1.md`, `/06-ux-conversion/ux-pattern-library-v1.md`, `/06-ux-conversion/trust-signal-plan-v1.md`

## 6. Responsible Roles

UX Designer (lead), Strategy Consultant (persona alignment), Information Architect (structural consistency)

## 7. Required Specialists

Developer (feasibility check on calculator logic and any LOS/CRM integration points), Compliance Liaison (mandatory review of calculator outputs and any language implying pre-approval or rate commitment)

## 8. Decision Authority

**Client sign-off required** on Primary Conversion Flow Diagrams before Stage Gate 7 (Visual Design) begins — UX flows are expensive to change once visual design work starts.

## 9. Workflow

```
[1] Map each priority persona's ideal conversion path from entry point to
    qualified lead action, in wireframe-level detail (no visual design yet)
        │
        ▼
[2] Specify calculator/interactive tool logic: inputs, outputs, disclaimer
    requirements, and what happens to the output (lead capture trigger?
    informational only?)
        │
        ▼
[3] Define page-level UX patterns reused across the site (hero patterns,
    CTA patterns, form patterns, FAQ patterns, trust-signal patterns)
        │
        ▼
[4] Define Trust Signal Placement Plan: where licensing info, NMLS ID,
    security badges, reviews, and loan officer credentials appear across
    templates
        │
        ▼
[5] Compliance review of calculator outputs and flow copy
        │
        ▼
[6] Client review and sign-off on conversion flows
        │
        ▼
[7] Exit Criteria → Stage Gate 7 scheduled
```

## 10. Checklist

- [ ] A conversion flow diagram exists for every priority persona/product combination identified in Stage Gate 3
- [ ] Every calculator has a fully specified input/output/disclaimer set, reviewed by Compliance Liaison
- [ ] UX Pattern Library covers, at minimum: hero, primary CTA, lead capture form, FAQ accordion, loan officer bio card, trust signal bar, comparison/rate table
- [ ] Trust Signal Placement Plan specifies exact template locations, not just "include trust signals somewhere"
- [ ] Client has formally signed off on conversion flows

## 11. Prompt(s)

**Prompt 6.1 — Conversion Flow Design**

```
You are the UX Designer for [Client Name], a mortgage lender. For the
persona "[Persona Name]" seeking "[Loan Product]", design a wireframe-level
conversion flow from first landing-page view to qualified lead action.
Specify each screen/step, the single primary action available at each step,
what friction-reduction technique is used (e.g., progressive disclosure,
soft credit pull avoidance, save-and-resume), and where in the flow trust
signals (licensing, security, reviews) should appear. Do not specify visual
design — this is structure and content of steps only.
```

**Prompt 6.2 — Calculator Specification**

```
Specify a [calculator type, e.g., "FHA affordability calculator"] for
[Client Name]'s site. Define: required inputs, optional inputs, the
calculation logic in plain language (not code), the output presentation,
required disclaimer language placement (flag for Compliance Liaison
review — do not draft final disclaimer legal text yourself), and whether
the output triggers a lead capture prompt or remains purely informational.
State any assumption that needs compliance confirmation explicitly.
```

## 12. Examples

*Sample conversion flow (condensed):*

```
Landing Page (FHA Loans hub, organic entry)
   → Primary CTA: "Check My FHA Affordability" (calculator, no email
     required to see result)
   → Calculator Result Screen: estimated affordability range + soft CTA
     "Get a personalized rate quote" (email + phone required)
   → Rate Quote Request Form (3 fields, progress-saved)
   → Confirmation Screen: "A loan officer will contact you within
     [X hours]" + trust signal (loan officer photo/bio preview)
```

## 13. Common Mistakes

- Requiring contact information before any value (a calculator result) is delivered, which increases bounce on cost-sensitive, anxious personas.
- Designing calculators that function as disguised lead-gen forms with no genuine calculation value — borrowers detect this and it damages trust.
- Skipping compliance review of calculator disclaimer placement, creating rework at Stage Gate 11.

## 14. Best Practices

- Give genuine value (a real estimate) before asking for contact information wherever compliance and business model allow it — this is consistently one of the highest-leverage trust and conversion levers available on lending sites.
- Reuse a small number of well-designed UX patterns across many pages rather than one-off page designs — this both improves usability consistency and reduces Stage Gate 10 build complexity.
- Design save-and-resume for any multi-step application flow; mortgage decisions are rarely completed in a single session.

## 15. Review Process

UX Designer presents flows to Engagement Lead and Compliance Liaison jointly; Developer confirms technical feasibility of calculator logic and any integration points before client presentation.

## 16. Quality Assurance

Primary Eight-Dimension focus: **Conversion**, **Accessibility** (flow must be fully keyboard/screen-reader navigable), **Brand** (flow tone consistent with positioning).

## 17. Exit Criteria

- [ ] All four Required Documents approved
- [ ] Compliance Liaison has signed off on calculator logic and disclaimer placement
- [ ] Client has formally approved Primary Conversion Flow Diagrams

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents saved v1.0
- Blueprint: "UX Flows" section populated with flow references and pattern library
- Decision Register: log client-approved conversion flow decisions as `DEC-SG6-00x` (rated Costly to Reverse — changes after Stage Gate 7 begins trigger a Change Request)

## 19. Future Enhancements

UX flows are translated into visual form in Stage Gate 7, stress-tested in Stage Gate 7.5's Prototype Validation, and measured against real conversion data in Stage Gate 11.5, where flow adjustments are proposed as data-driven experiments rather than opinion-driven redesigns.

---

*End of Volume III. Continue to Volume IV — Design.*
