# CORE METHODOLOGY — SEO & ARCHITECTURE

*Website Excellence Framework (WEF) v1.0*

---

## Chapter Introduction

This chapter covers Stage Gates 4 and 5: Information Architecture and SEO Blueprint. They are grouped together because, in practice, a site's structure and its search-visibility strategy are inseparable — the sitemap a client approves *is* the topical architecture the SEO Blueprint builds authority around. Both gates follow the fixed 19-part Stage Gate template defined in the Research chapter's introduction. Decisions made here are foundational — reversing an approved sitemap or keyword architecture after Design begins is a costly, major-version change requiring a formal Change Request.

---

# STAGE GATE 4 — INFORMATION ARCHITECTURE

## 1. Purpose

Design the complete page hierarchy, navigation structure, URL scheme, and content taxonomy for the website, translating the approved positioning and persona priorities into a structure a visitor can navigate intuitively and a search engine can crawl and understand cleanly.

## 2. Business Objectives

- Ensure every priority persona and offering has a clear, discoverable path from entry to conversion.
- Build a taxonomy that supports topical authority (Stage Gate 5) rather than a flat, disconnected page list.
- Set a URL structure that is stable, semantic, and scalable to the site's projected 3–5 year page count.

## 3. Inputs

Strategic Direction Brief, Positioning Statement, Persona/Offering Priority Matrix, White Space Opportunity Map, Compliance/Standards Constraint Log, active Industry Module's Information Architecture Patterns

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

UX Designer (early consult on navigation usability), Compliance/Standards Liaison (confirm required disclosure/credential pages per the active Industry Module)

## 8. Decision Authority

Engagement Lead approves; client review recommended but not mandatory sign-off (mandatory sign-off resumes at UX & Conversion exit and Design's Prototype Validation gate).

## 9. Module Injection Point(s)

> **Module Injection Point:** Load the active Industry Module's **Information Architecture Patterns** (typical sitemap structures and page types for this vertical) before drafting the sitemap, and its **Regulatory & Compliance Landscape** to confirm every required disclosure/credential/licensing page is present.

## 10. Workflow

```
[1] List all required page types using the Module's Information
    Architecture Patterns as a starting checklist: core (home, about,
    contact), offering pages, persona-path hubs, location/service-area
    pages if applicable, resource (blog/guides), compliance/credential
    pages
        │
        ▼
[2] Group pages into a hierarchy reflecting topical clusters (see Stage
    Gate 5 pillar/cluster model) rather than a flat list
        │
        ▼
[3] Draft URL Structure Standard (see Sec. 13 example pattern)
        │
        ▼
[4] Design primary navigation (max depth and item count per usability
    best practice — see Sec. 15) and footer/utility navigation
        │
        ▼
[5] Define content taxonomy: categories, tags, and entity relationships
        │
        ▼
[6] Internal review → Exit Criteria → Stage Gate 5 scheduled
```

## 11. Checklist

- [ ] Active Industry Module's Information Architecture Patterns reviewed before drafting
- [ ] Every priority persona (Stage Gate 3) has a clear top-level path in the sitemap
- [ ] Every offering in scope has a dedicated page or hub
- [ ] All Module-flagged compliance/credential pages are present (licensing/registration page, required regulatory links, disclosure pages, accessibility statement)
- [ ] URL Structure Standard is documented and consistent (no mixed patterns)
- [ ] Primary navigation tested against a "3-click rule" — any priority page reachable within 3 clicks from homepage
- [ ] Taxonomy supports topical clustering for Stage Gate 5 (no orphaned pages with no cluster relationship)

## 12. Prompt(s)

**Prompt 4.1 — Sitemap Generation**

```
You are the Information Architect for [Client Name] in the [Industry
Module name] vertical, operating in [service area/jurisdiction(s)]. Using
the attached Strategic Direction Brief, Persona Priority Matrix,
Compliance/Standards Constraint Log, and the [Industry Module]'s
Information Architecture Patterns, produce a complete hierarchical
sitemap.

Requirements:
- Organize around topical clusters (pillar pages + supporting cluster
  pages), not a flat list
- Include a dedicated hub page for each priority persona identified
- Include a dedicated page for each offering in scope
- Include all compliance/credential pages flagged by the Module:
  licensing/registration page, jurisdiction-specific disclosure pages,
  privacy policy, accessibility statement, and any vertical-specific
  required statement
- Note page depth (how many clicks from home) for each entry
- Flag any page you believe is required for compliance but did not appear
  in the Compliance/Standards Constraint Log, for review by the
  Compliance/Standards Liaison
```

**Prompt 4.2 — URL Structure Standard**

```
Given the sitemap above, propose a URL structure standard for [Client
Name]'s WordPress/GeneratePress site. Rules: lowercase, hyphenated, no
stop-word bloat, reflect the topical hierarchy, stable under future page
additions. Provide the full URL for every page in the sitemap and flag
any URL over 60 characters for review.
```

## 13. Examples

*Generic URL Structure Standard pattern (adapt page-type names per the active Industry Module's Content Model):*

| Page Type | Pattern | Example |
|---|---|---|
| Offering pillar | `/{offering-category}/{offering}/` | `/services/{offering}/` |
| Offering + location cluster | `/{offering-category}/{offering}/{location}/` | `/services/{offering}/{location}/` |
| Persona hub | `/{persona-path}/` | `/{persona-path}/` |
| Resource/guide | `/guides/{slug}/` | `/guides/{slug}/` |
| Compliance/credential | `/legal/{slug}/` | `/legal/licensing-disclosures/` |

See each Industry Module's Information Architecture Patterns for fully worked, vertical-specific sitemap examples.

## 14. Common Mistakes

- Building navigation around internal company structure (departments, teams) instead of the audience's mental model.
- Flat sitemaps with no pillar/cluster relationship, which undermines the entire Stage Gate 5 SEO strategy.
- Forgetting jurisdiction-specific or credential-specific disclosure pages the active Industry Module flags as required.
- URL structures mixing patterns inconsistently.
- Ignoring the Module's Information Architecture Patterns and rebuilding a generic sitemap that misses vertical-standard page types (e.g., forgetting a "meet the team/practitioners" hub in a professional-services vertical).

## 15. Best Practices

- Apply a 7±2 item limit to primary navigation; push depth into mega-menus or hub pages rather than a flat wide navbar.
- Design the taxonomy before the sitemap is finalized — taxonomy-first prevents orphaned pages.
- Validate the "3-click rule" explicitly for every persona's priority conversion path, not just structurally for all pages.

## 16. Review Process

Engagement Lead and SEO Specialist jointly review the sitemap against the Checklist; Compliance/Standards Liaison independently confirms all Module-required compliance pages are present before sign-off.

## 17. Quality Assurance

Primary Eight-Dimension focus: **SEO**, **Scalability**, **Maintainability**. Secondary: **Conversion** (path clarity).

## 18. Exit Criteria

- [ ] Sitemap, URL Structure Standard, Navigation Model, and Content Taxonomy approved by Engagement Lead
- [ ] Compliance/Standards Liaison has confirmed all Module-required compliance pages present
- [ ] No orphaned pages in the taxonomy

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents saved v1.0
- Blueprint: "Sitemap & IA" section populated in full
- Decision Register: log final navigation model choice and any rejected alternatives as `DEC-SG4-00x`

The sitemap is extended (not restructured) in Stage Gate 5 as topical clusters are fully mapped to keywords, and again in Post-Launch Growth Program as new content is added under the same taxonomy rules.

---

# STAGE GATE 5 — SEO BLUEPRINT

## 1. Purpose

Build the complete search visibility architecture for the site: keyword-to-page mapping, topical cluster strategy, technical SEO requirements, schema markup plan, and AI-search (LLM-citation) optimization approach.

## 2. Business Objectives

- Ensure every page in the Stage Gate 4 sitemap has a defined keyword and search-intent purpose — no page exists without a search rationale.
- Build genuine topical authority in the client's specific offering and geographic niches, rather than shallow coverage across too many topics.
- Position content to be citable by AI-mediated search (ChatGPT, Google AI Overviews, Perplexity, etc.), not only classic 10-blue-links SEO.

## 3. Inputs

Sitemap & Content Taxonomy (Stage Gate 4), Competitive Intelligence Report (Stage Gate 2), Positioning & Messaging Pillars (Stage Gate 3), active Industry Module's SEO & Keyword Strategy section

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

Developer (early consult — confirm Rank Math + GeneratePress technical constraints), Compliance/Standards Liaison (confirm no keyword targeting implies unsubstantiated claims per the active Industry Module)

## 8. Decision Authority

Engagement Lead approves; this Blueprint becomes binding input to Development (Content Specification) and cannot be materially altered afterward without a Change Request.

## 9. Module Injection Point(s)

> **Module Injection Point:** Load the active Industry Module's **SEO & Keyword Strategy** section for known high-value topical clusters, typical schema types, and known claim-risk keyword patterns for this vertical before building the keyword map and schema plan.

## 10. Workflow

```
[1] Keyword research per persona/offering/location combination from the
    sitemap, informed by the Module's SEO & Keyword Strategy
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
[5] Define Schema Markup Plan per page type (see Sec. 13), using the
    Module's recommended schema types as a starting checklist
        │
        ▼
[6] Draft Entity SEO & AI Search Optimization Brief: how the site
    establishes clear entity identity (organization, people, offerings)
    for both classic and AI-mediated search
        │
        ▼
[7] Internal review → Exit Criteria → Stage Gate 6 scheduled
```

## 11. Checklist

- [ ] Active Industry Module's SEO & Keyword Strategy reviewed before keyword research began
- [ ] Every sitemap page has a mapped primary keyword and defined search intent
- [ ] Topical Cluster Model shows explicit pillar → cluster → internal link relationships
- [ ] Technical SEO Requirements Spec includes Core Web Vitals targets (LCP < 2.5s, INP < 200ms, CLS < 0.1) as binding requirements for Development
- [ ] Schema Markup Plan covers all schema types the Module recommends for this vertical, plus Organization, FAQPage, and BreadcrumbList as universal baseline
- [ ] Entity SEO Brief addresses how credentials/licensing/registration establish machine-readable trust signals per the Module's Trust Signal Requirements
- [ ] No keyword target implies a claim requiring compliance substantiation without a flag for Development (Copywriting) review

## 12. Prompt(s)

**Prompt 5.1 — Keyword-to-Page Mapping**

```
You are the SEO Specialist for [Client Name] in the [Industry Module name]
vertical. Using the attached sitemap, Competitive Intelligence Report, and
the [Industry Module]'s SEO & Keyword Strategy, produce a keyword-to-page
map. For each page, provide: primary keyword, 3-5 secondary keywords,
search intent (informational/commercial/transactional/navigational),
estimated competitiveness (low/medium/high based on competitor content
depth observed in Stage Gate 2), and a one-sentence content angle that
differentiates from what competitors currently rank with.

Do not fabricate search volume figures; if volume data is not provided,
label estimates as "[unverified estimate]" or omit them.
```

**Prompt 5.2 — Topical Cluster Model**

```
Using the keyword-to-page map above, group pages into topical clusters:
identify pillar pages (broad, high-value pages meant to rank for head
terms and link out to supporting content) and cluster pages (specific,
long-tail pages that link back to their pillar). Produce a cluster
diagram (text/ASCII acceptable) showing pillar-to-cluster and cluster-to-
cluster internal linking relationships for at least the top 3 clusters by
business priority.
```

**Prompt 5.3 — Schema Markup Plan**

```
Produce a schema.org markup plan for [Client Name]'s website in the
[Industry Module name] vertical, using the [Industry Module]'s recommended
schema types as your starting checklist. Cover, at minimum: Organization
schema for the homepage, LocalBusiness schema for each location/service
area, Person schema for practitioner/staff profile pages (include any
Module-specified professional identifier property), FAQPage schema for
guide/FAQ content, BreadcrumbList for all deep pages, and Article schema
for blog/guide content. For each schema type, list the required and
recommended properties and note any properties requiring data the client
has not yet provided.
```

## 13. Examples

*Generic Schema Markup Plan pattern:*

| Page Type | Schema Type | Key Properties | Notes |
|---|---|---|---|
| Practitioner/Staff Profile | Person + [industry service schema] (employee of) | name, jobTitle, telephone, identifier (per Module), worksFor | Any Module-required professional ID must be displayed as visible text per compliance, in addition to schema |
| Location/Service-Area Page | Service + LocalBusiness (areaServed) | areaServed, provider, serviceType | Pair with FAQPage schema for location-specific Q&A |

See each Industry Module's SEO & Keyword Strategy section for fully worked, vertical-specific schema plans (e.g., FinancialService + Person/NMLS for mortgage lending; MedicalOrganization + Physician for healthcare; Attorney + LegalService for law firms).

## 14. Common Mistakes

- Targeting high-volume, high-competition head terms that a client with limited domain authority cannot realistically compete for, at the expense of winnable long-tail/local terms.
- Treating schema markup as a technical afterthought for Development rather than specifying it here, where it should influence content structure decisions at the Content Specification gate.
- Omitting the Entity SEO Brief, leaving the site with no deliberate strategy for AI-mediated search visibility.
- Ignoring the active Industry Module's SEO & Keyword Strategy and re-deriving vertical keyword patterns the firm has already validated on prior engagements.

## 15. Best Practices

- Prioritize topical depth in the client's specific service area and specialty offerings over broad national keyword coverage the client cannot substantiate operationally.
- Build the Entity SEO Brief around making the organization, its credentials, and its practitioners unambiguously machine-readable — this is what allows AI search systems to cite the site confidently as a source.
- Cross-check every keyword target against the Compliance/Standards Constraint Log and the Module's flagged claim-risk patterns before finalizing.

## 16. Review Process

SEO Specialist and Information Architect jointly review the cluster model for structural consistency with the Stage Gate 4 sitemap; Developer reviews Technical SEO Requirements for GeneratePress/Rank Math feasibility; Compliance/Standards Liaison scans keyword targets for claim risk.

## 17. Quality Assurance

Primary Eight-Dimension focus: **SEO** (this gate's core output), **Scalability**, **AI Implementation Readiness** (schema/technical spec must be precise enough for Development's build gates).

## 18. Exit Criteria

- [ ] All five Required Documents approved by Engagement Lead
- [ ] Compliance/Standards Liaison has cleared keyword targets for claim risk
- [ ] Developer has confirmed Technical SEO Requirements are buildable on the default stack (or alternative per Charter)

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all five Required Documents saved v1.0
- Blueprint: "SEO Architecture" section populated in full
- Decision Register: log cluster prioritization decisions (which clusters are Phase 1 vs. Phase 2) as `DEC-SG5-00x`

The Keyword-to-Page Map and Schema Plan are directly consumed by Development (Content Specification and WordPress Implementation Blueprint). Cluster performance is measured and the model is extended in Post-Launch Growth Program.

---

*End of SEO & Architecture. Continue to Core Methodology — UX & Conversion.*
