# CORE METHODOLOGY — REUSABLE TEMPLATES

*Website Excellence Framework (WEF) v1.0*

---

## Chapter Introduction

Reusable Templates is the fillable-template counterpart to the rest of the Core Methodology. Where those chapters explain *why* and *when* each artifact is produced, this chapter provides the *actual blank template* a consultant or AI model fills in. Every template here is referenced by name from a specific Stage Gate; none are decorative, and none are industry-specific — vertical-specific example content lives in the Industry Modules, not here. Copy the relevant template into the Knowledge Base path indicated in the originating Stage Gate's "Required Documents" section and complete it in place — do not rename fields or restructure tables, since downstream automation and cross-engagement comparison depend on structural consistency.

---

## 1. Prompt Library

See AI Workflows, Section 4, for the full Prompt Library master index. Prompt text is authoritative in its originating Stage Gate chapter.

---

## 2. Decision Register Template

```markdown
# Decision Register — [Client Name] — [Active Industry Module(s)]

| Decision ID | Date | Decision Summary | Rationale | Alternatives Considered | Decided By | Stage Gate | Impacts | Reversibility | Status |
|---|---|---|---|---|---|---|---|---|---|
| DEC-SG1-001 | | | | | | | | Reversible/Costly/Irreversible | Active/Superseded |
```
*(Governance, Section 4)*

## 3. Decision Templates — Change Request

```markdown
# Change Request — CR-[###]

**Submitted By:**
**Date:**
**Scope:** Core Methodology / Industry Module: [name] / Engagement-Level
**Section/Artifact Affected:**
**Current State:**
**Proposed Change:**
**Rationale:**
**Impact if Not Approved:**
**Impact on Schedule/Scope/Budget (engagement-level CRs only):**
**Governance Board / Engagement Lead Decision:** Approved / Rejected / Deferred
**Decision Rationale:**
**Date Decided:**
```
*(Governance, Section 13.2)*

---

## 4. Review Templates

### 4.1 Stage Gate Exit Review Template

```markdown
# Stage Gate Exit Review — [Stage Gate Name/Number] — [Client Name]

**Active Industry Module(s):**
**Reviewer(s):**
**Date:**

## Checklist Status
[Paste the Stage Gate's Checklist from the manual; mark each item Pass/Fail/N/A]

## Exit Criteria Status
[Paste Exit Criteria; mark each Met/Not Met]

## Outstanding Items
| Item | Owner | Due Date |
|---|---|---|

## Decision
[ ] Gate approved — proceed to next Stage Gate
[ ] Gate approved with conditions (list below)
[ ] Gate not approved — remediation required before re-review

**Conditions/Remediation Notes:**
**Approved By:**
```

### 4.2 Design Critique Template (internal, pre-tournament)

```markdown
# Internal Design Critique — [Direction Name] — [Client Name]

**Reviewers:**
**Date:**

| Dimension | Score (1-5) | Notes |
|---|---|---|
| Performance | | |
| Accessibility | | |
| SEO | | |
| Conversion | | |
| Brand/Differentiation | | |
| Scalability | | |
| Maintainability | | |
| GP/GB Compatibility | | |

**Overall Recommendation:** Ready for tournament / Needs revision (specify)
```

---

## 5. Scoring Rubrics

### 5.1 Competitor Scoring Matrix (Stage Gate 2)

```markdown
| Competitor | Content Depth (1-5) | Technical SEO (1-5) | UX/Conversion (1-5) | Design (1-5) | Trust Signals (1-5) | Local Relevance (1-5) | Total (/30) | Notes |
|---|---|---|---|---|---|---|---|---|
```

### 5.2 Design Tournament Scoring Matrix (Stage Gate 7.5)

```markdown
| Dimension | Direction A | Direction B | Direction C | Notes |
|---|---|---|---|---|
| Performance | | | | |
| Accessibility | | | | |
| SEO | | | | |
| Conversion | | | | |
| Brand | | | | |
| Scalability | | | | |
| Maintainability | | | | |
| GP/GB Compatibility | | | | |
| Differentiation from Competitors | | | | |
| **Total (of 45)** | | | | |
```

### 5.3 Eight-Dimension Quality Scorecard (Governance Sec. 12.2 — reusable at any gate)

```markdown
| Dimension | Score (1-5) | Evidence/Justification |
|---|---|---|
| Performance | | |
| Accessibility | | |
| SEO | | |
| Conversion | | |
| Brand | | |
| Scalability | | |
| Maintainability | | |
| WordPress/GP/GB Compatibility & AI Readiness | | |
```

---

## 6. Architecture Templates

### 6.1 Sitemap Template

```markdown
# Sitemap — [Client Name] — [Active Industry Module]

| Page | URL | Parent | Depth (clicks from home) | Persona Served | Offering Served | Page Type |
|---|---|---|---|---|---|---|
| Home | / | — | 0 | All | All | Core |
```

### 6.2 URL Structure Standard Template

```markdown
# URL Structure Standard — [Client Name]

| Page Type | Pattern | Example | Notes |
|---|---|---|---|
```

### 6.3 Content Taxonomy Template

```markdown
# Content Taxonomy — [Client Name]

**Categories:**
**Tags:**

| Entity | Related Entities | Related Pages |
|---|---|---|
```

---

## 7. SEO Templates

### 7.1 Keyword-to-Page Map Template

```markdown
| Page URL | Primary Keyword | Secondary Keywords | Search Intent | Competitiveness | Content Angle |
|---|---|---|---|---|---|
```

### 7.2 Topical Cluster Model Template

```markdown
# Topical Cluster Model — [Client Name]

## Cluster: [Cluster Name]
**Pillar Page:** [URL]
**Cluster Pages:**
- [URL] — links to pillar via: [anchor text/context]

**Internal Linking Diagram:**
[ASCII or list-based representation]
```

### 7.3 Technical SEO Requirements Template

```markdown
# Technical SEO Requirements — [Client Name]

| Requirement | Target/Standard | Verification Method |
|---|---|---|
| LCP | < 2.5s | PageSpeed Insights / WebPageTest |
| INP | < 200ms | PageSpeed Insights / CrUX |
| CLS | < 0.1 | PageSpeed Insights |
| Indexation | All priority pages indexable; no unintended noindex | Search Console coverage report |
| Canonicalization | Self-referencing canonical on all pages | Manual/crawler audit |
```

### 7.4 Search Visibility Operations Plan Template

```markdown
# Search Visibility Operations Plan — [Client Name]

## 1. Measurement Sources and Ownership
| Evidence Source | Property/View | Account Owner | Data Window | Decision Use | Last Verified |
|---|---|---|---|---|---|
| First-party search performance | | | | Queries, pages, indexation | |
| Web analytics | | | | Engagement and meaningful actions | |
| Rank tracker | | | | Bounded monitoring portfolio | |
| Technical crawler/link monitor | | | | Crawl and link diagnostics | |
| Performance field/lab data | | | | Template-level performance | |

## 2. Preserved Baseline
- Baseline export location:
- Date range and comparison range:
- Launch/migration/change annotations:
- Known seasonality or campaign effects:
- Data limitations and latency:

## 3. Meaningful-Action Measurement Plan
| Event | Business Meaning | Trigger | Parameters (no PII) | Consent Category | Debug Test | Reporting Owner |
|---|---|---|---|---|---|---|

## 4. Opportunity Prioritization
Score each candidate 0-3 for business value, evidence strength, near-term attainability, page/intent fit, and implementation confidence. Subtract 0-3 each for compliance risk, cannibalization risk, and maintenance burden. Record the evidence; do not use the total as an unexplained black box.

## 5. Rank-Tracking Portfolio
| Bucket | Query | Mapped URL | Intent | Business Reason | Baseline | Owner | Keep/Replace Review |
|---|---|---|---|---|---|---|---|
Buckets: business-critical; near-win; local/segment; brand/entity; discovery/experimental.

## 6. Operating Cadence
- Weekly: anomalies, outages, coverage/indexation changes, conversion-event health, critical 404/5xx changes.
- Monthly: query-page opportunities, CTR, conversions, internal links, content refresh/creation decisions, change-log results.
- Quarterly: portfolio rationalization, cannibalization, technical crawl, schema/metadata ownership, performance, content consolidation, strategy review.

## 7. Reporting Rules
- Separate leading search indicators from meaningful business outcomes.
- Compare consistent windows and note seasonality, campaigns, migrations, and data latency.
- Treat plugin scores as diagnostics, never outcome KPIs.
- Attach the query and URL evidence to every recommendation.
```

### 7.5 SEO Opportunity and Change Log Template

```markdown
| ID | Evidence Window | Query + URL | Observed Problem | Hypothesis | Planned Change | Leading Indicator | Meaningful Outcome | Risk/Review | Owner | Publish Date | Review Date | Result/Decision |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
```

### 7.6 Link Audit Log Template

```markdown
| Source URL(s) | Destination | Internal/External | Purpose (navigation/context/evidence/compliance) | Observed Result | Browser/Second-Method Result | Final URL | Classification | Decision | Owner | Re-test |
|---|---|---|---|---|---|---|---|---|---|---|
```

Classification rules: `2xx healthy`; `3xx update internal / assess external`; `401/403/429 verify before editing`; `404/410 replace, remove, restore, or deliberately leave gone`; `5xx/timeout/DNS/TLS retry and investigate`; `unchecked unknown`. Do not redirect vulnerability-probe noise to the homepage.

### 7.7 Page-Creation Quality Gate Template

```markdown
# Proposed Page — [Topic/Location/Variant]

| Test | Evidence | Pass/Fail |
|---|---|---|
| Genuine service/product/topic coverage | | |
| Distinct user intent or navigation role | | |
| Primary query and non-cannibalizing mapped URL | | |
| Materially unique helpful content/proof available | | |
| Parent hub + contextual inbound/outbound links defined | | |
| Claims and operational capacity substantiated | | |
| Maintenance owner and review trigger assigned | | |
| Useful to visitors even without rankings | | |

**Decision:** Create / strengthen existing page / consolidate / research backlog / reject
**Decision Register ID:**
```

### 7.8 Evidence & Source Register Template

```markdown
| Evidence ID | Claim/Observation Used | Source Title/Publisher | URL/File | Source Class | Geography/Population/Metric Definition | Published Date | Accessed/Extracted | Quotation/Paraphrase/Calculation/Inference | Limitations | Confidence/Status | Review/Expiry | Consuming Deliverables | Owner | Rights/Permitted Use |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
```

Source classes: `authoritative/regulatory`, `client/first-party`, `neutral secondary`, `competitor`, `inference`. Status values: `verified`, `client-confirmed`, `needs human verification`, `stale`, `superseded`. A competitor is evidence of what that competitor publishes or does, not independent proof that its claims are true. Do not publish a time-sensitive fact without its observation date, limitations, and review owner.

### 7.9 Content Freshness Register Template

```markdown
| Artifact/URL | Factual Dependency | Freshness Class (Evergreen/Periodic/Event-Bound/Volatile) | Evidence IDs / Authoritative Source | Public “As Of” Date | Owner | Last Verified | Next Review or Expiry Trigger | Stale Disposition (Refresh/Qualify/Archive/Redirect/Consolidate/Noindex) | Status |
|---|---|---|---|---|---|---|---|---|---|
```

Event-bound entries name the actual event or date, not “review later.” Volatile entries use the shortest practical review interval or point users to an authoritative live source. Closing an entry requires the public artifact and its structured data, metadata, internal links, sitemap/indexation state, and any translations to be handled consistently.

### 7.10 Post-Release Indexing Verification Record

```markdown
| Release/Cluster | Sitemap | Representative URL | Template/Hierarchy/Locale/Risk Class | Final HTTP Status | Rendered Canonical | Robots Directive | Sitemap Membership | Search-Engine Inspection Result | Request Date (if used) | Follow-up Date | Owner |
|---|---|---|---|---|---|---|---|---|---|---|---|
```

Sample each materially new template, hierarchy, locale, and risk class rather than requesting every URL individually. Record alternate/canonical selection and follow-up work. Sitemap submission and URL inspection are discovery/diagnostic actions; neither guarantees indexing or ranking.

## 8. Content Templates

### 8.1 Content Brief Template (Stage Gate 8)

```markdown
# Content Brief — [Page Name/URL]

**Primary Keyword:**
**Secondary Keywords:**
**Search Intent:**
**Persona Served:**

**Heading Outline:**
- H1:
- H2:
  - H3:

**Required Sections (purpose):**
1.

**Internal Linking Targets:**

**Calculator/Tool Embed:**

**Compliance Requirements:**

**Target Word Count:**
```

### 8.2 Content Depth Standard Template

```markdown
| Page Type | Minimum Word Count | Required Structural Elements |
|---|---|---|
| Pillar Page | | |
| Cluster Page | | |
| Location/Service-Area Page | | |
| Compliance Page | | |
```

### 8.3 Video-to-Website Deployment Brief (Optional)

Use when an engagement plans a recurring video series or when a video must function as a governed website, search, localization, accessibility, or compliance asset rather than an isolated social upload.

```markdown
# Video-to-Website Deployment Brief — [Series / Episode]

| Field | Value |
|---|---|
| Episode ID / working title | |
| Audience and question answered | |
| Primary website page / mapped query | |
| Recording format and target duration | |
| Word-for-word script | |
| Presenter bullet version | |
| Local facts/input still required | |
| Evidence IDs and freshness class | |
| Language/locale and human reviewer | |
| Claims/disclosures requiring clearance | |
| On-camera CTA and verified destination | |
| Platform title/description/chapters | |
| Transcript/captions status | |
| Website embed and supporting text/article | |
| Internal links in/out | |
| Thumbnail and descriptive-alt decision | |
| Schema/metadata decision | |
| Exact approval revision | |
| Publication dates and owners | |
| Refresh/retirement trigger | |
```

A translated video is a separate governed artifact and does not inherit source-language clearance. Captions and a useful text equivalent are accessibility and reuse requirements, not SEO padding.

---

## 9. Metadata Templates

```markdown
# Meta Tag Register — [Client Name]

| Page URL | Meta Title (≤60 char) | Meta Description (≤155 char) | Canonical URL | Robots Directive |
|---|---|---|---|---|
```

---

## 10. Schema Templates

```markdown
# Schema Markup Plan — [Client Name] — [Active Industry Module]

| Page Type | Schema Type(s) | Required Properties | Recommended Properties | Data Source/Owner |
|---|---|---|---|---|
| Homepage | Organization + [Module-specific type] | name, url, logo, telephone, address, identifier | sameAs (social profiles) | Marketing |
| Practitioner/Staff Profile | Person | name, jobTitle, telephone, identifier (per Module) | image, sameAs | HR/Compliance |
| Genuine staffed location | LocalBusiness subtype | name, address, geo, telephone | parentOrganization | SEO Specialist / Operations |
| Service area without a staffed office | Service | areaServed, provider, serviceType | | SEO Specialist |
| Guide/article | Article where the page is actually an article/guide | author, datePublished, headline | dateModified | Copywriter |
| Visible FAQ content | FAQPage only when current eligibility and content purpose make it appropriate | mainEntity (visible Q&A pairs) | | Copywriter / SEO Specialist |
```

See each Industry Module's SEO & Keyword Strategy section for the specific recommended schema types for that vertical.

---

## 11. QA Templates

### 11.1 QA Test Plan Template

```markdown
# QA Test Plan — [Client Name]

| Test ID | Feature/Page | Action | Expected Result | Pass/Fail | Notes |
|---|---|---|---|---|---|
```

### 11.2 Issue Log Template

```markdown
# Issue Log — [Client Name]

| Issue ID | Description | Page/Location | Category | Severity (P0/P1/P2) | Owner | Remediation | Status |
|---|---|---|---|---|---|---|---|
```

### 11.3 Compliance Sign-Off Record Template

```markdown
# Compliance Sign-Off Record — [Client Name] — [Active Industry Module]

| Artifact ID / URL | Content Type | Language | Exact Revision (version/hash/date) | Approval Scope | Reviewed By | Date | Status (Cleared/Cleared with Changes/Rejected) | Changes That Invalidate Clearance | Notes / Evidence |
|---|---|---|---|---|---|---|---|---|---|
```

An approval applies only to the exact artifact, revision, language, and scope recorded. New pages, posts, videos, translations, changed claims/data/disclosures, or substantive edits require a new row unless the approver explicitly included them. Define whether typo-only or formatting-only edits remain cleared; never infer future clearance from “site approved” or “batch approved.”

---

## 12. AI Prompt Templates — General-Purpose Frame

Use this frame to construct any Stage-Gate-specific prompt not already in the Prompt Library, ensuring LLM Handoff Protocol compliance (AI Workflows, Section 2):

```markdown
You are the [ROLE] for [Client Name] in the [Industry Module name]
vertical.

Context attached: [Charter Layer excerpt] / [relevant Decision Register
entries] / [current Master Website Blueprint excerpt] / [relevant active
Industry Module section(s)].

Task: [specific deliverable requested, referencing the exact Stage Gate
and Required Document it maps to]

Constraints:
- Do not fabricate statistics, credentials, testimonials, or regulatory
  claims
- Flag any compliance-sensitive statement explicitly rather than
  asserting it as final
- Ground every recommendation in the attached source material; label
  inferences explicitly
- Output format: [specify table/markdown structure expected]
```

### 12.1 AI Verification Packet Template

```markdown
# AI Verification Packet — [Client Name] — [Task/Stage Gate]

| Field | Value |
|---|---|
| Agent/model and date | |
| Target environment/property | |
| Source/commit/input artifact | |
| Files/records/capabilities changed | |
| Validation commands or checks | |
| Fresh independent read-back | |
| Reviewer and status | |
| Unresolved risks/decisions | |
| Rollback/recovery reference | |

**Completion statement:** [State only what the evidence supports. Do not
claim published, synced, verified, or complete from a tool success message
or same-session editor view alone.]
```

---

## 13. GeneratePress Templates

### 13.1 Global Styles Token Record

```markdown
# GeneratePress Global Styles Token Record — [Client Name]

| Token | Value | GeneratePress Location |
|---|---|---|
| Primary Color | | Customizer > Colors > Global Palette |
| Secondary Color | | Customizer > Colors > Global Palette |
| Heading Font | | Customizer > Typography > Headings |
| Body Font | | Customizer > Typography > Body |
| Base Spacing Unit | | Customizer > Layout > Spacing |
```

### 13.2 Element Hooks Record

```markdown
| Element Name | Type (Header/Footer/Hook/Block) | Display Rules | Notes |
|---|---|---|---|
| Trust Signal Bar | Hook (below header) | Site-wide | Per active Industry Module's Trust Signal Requirements |
```

---

## 14. GenerateBlocks Templates

### 14.1 Component-to-Pattern Mapping Template

```markdown
| Component | Block Composition | CSS Classes (token-linked) | Responsive Notes | Dynamic Data Source |
|---|---|---|---|---|
| Staff/Practitioner Card | Container > Grid > Image + Headline + Text + Button | .gb-card--staff-profile | Stack at <768px | Query Loop against Staff CPT |
```

### 14.2 Pattern Library Index Template

```markdown
| Pattern Name | Global/Local | Used On Pages | Last Updated |
|---|---|---|---|
```

---

## 15. WordPress Templates

### 15.1 Server/Hosting Configuration Record

```markdown
# Server Configuration Record — [Client Name]

| Setting | Value | Notes |
|---|---|---|
| Hosting Provider | Hostinger VPS | Plan/tier: |
| PHP Version | | |
| WordPress Version | | |
| SSL/TLS | | Via Cloudflare / Origin cert |
| Backup Schedule | | |
```

### 15.2 Plugin & Integration Configuration Record

```markdown
| Plugin/Integration | Base/Add-on Version | Purpose | Installed & Active | Subscription/Plan + Renewal Owner | Connected Account | Exact Site/Property Assignment | Paid Capability/Badge Verified | Authenticated Update Channel | Configuration Notes |
|---|---|---|---|---|---|---|---|---|---|
| GeneratePress Premium | | Theme framework | | | | | | | |
| GenerateBlocks Pro | | Page building | | | | | | | |
| Rank Math SEO | | SEO/schema | | | | | | | |
| LiteSpeed Cache | | Performance | | | | | | | | |
```

Installation, activation, subscription entitlement, connected identity, and per-site assignment are separate checks. Verify paid state from both the site and vendor account where available; a premium file name, menu item, or installed add-on is not sufficient evidence.

### 15.3 Capability Ownership Matrix

```markdown
| Capability | Production Owner (one writer) | Monitor/Reader(s) | Theme/Code Fallback | Active-State Verification | Disabled-State Verification | Data Location | Export/Migration Path | Account/Property Verified |
|---|---|---|---|---|---|---|---|---|
| Titles/meta descriptions | | | | | | | | |
| Canonicals/robots directives | | | | | | | | |
| XML sitemap | | | | | | | | |
| Structured data | | | | | | | | |
| Redirects/404 monitoring | | | | | | | | |
| Translation/`hreflang` | | | | | | | | |
| Analytics/tag injection | | | | | | | | |
| Consent management | | | | | | | | |
| Forms/lead storage | | | | | | | | |
| Caching/minification/images | | | | | | | | |
| Security/firewall | | | | | | | | |
```

Rendered public output, response headers, cookies, and network requests are the verification source. Admin settings alone are not acceptance evidence.

### 15.4 Content Release & Rollback Record

```markdown
# Content Release & Rollback Record — [Client Name]

## Release
| Field | Value |
|---|---|
| Release ID / timestamp | |
| Environment and destination | |
| Source commit / artifact path | |
| Content type/post type | |
| Operator / reviewer | |
| Intended status | |
| Cache/indexation impact | |

## Scope and Mapping
| Source Record | Stable Identifier | Existing ID/Slug | Action (create/update/status) | Fields Changed | Intended URL/Language | Rollback Artifact |
|---|---|---|---|---|---|---|

## Validation
- Parser/format validation:
- Item count and duplicate check:
- One-record smoke test:
- Pilot batch result:
- Destination type confirmed:
- Fresh public/authenticated read-path result:
- Re-export/source diff:
- Representative links/schema/forms/mobile checks:

## Rollback
- Trigger threshold:
- Rollback owner:
- Exact prior export/backup:
- Recovery steps:
- Re-test and closure evidence:
```

### 15.5 Access & Environment Matrix

```markdown
| System/Property | Environment | Business Owner | Operational Custodian | Account/Role | Access Status | Correct Property Verified | Recovery/Export Path | Last Review | Revocation/Rotation Owner | Secret Location (manager reference only) |
|---|---|---|---|---|---|---|---|---|---|
```

Never write secret values into this matrix. Record a credential-manager reference or ticket ID only. Reconfirm the visible domain/property before state-changing work and record temporary credential revocation when applicable.

### 15.6 Localization & Language QA Matrix

```markdown
| Source URL | Locale URL | Translation Owner/Reviewer | Independent Copy Review | Title/Description | Canonical | Reciprocal hreflang | Consent/Legal Copy | Form/CTA Routing | Images/Alt Text | Indexation Decision | Last Verified |
|---|---|---|---|---|---|---|---|---|---|---|---|
```

Do not treat machine translation as final for regulated, contractual, medical, financial, safety, compensation, consent, or legal language. Every locale must have an explicit indexation decision and a tested user path, not merely translated visible text.

### 15.7 Third-Party Custom Domain & Access-Control Record

```markdown
# Third-Party Custom Domain & Access-Control Record — [Client Name / Application]

## Request Path and Ownership
| Layer | Provider / Identifier | Owner | Verified State | Evidence / Last Checked |
|---|---|---|---|---|
| Registrar | | | | |
| Authoritative DNS | | | | |
| Edge/proxy | | | | |
| TLS termination/certificate | | | | |
| Hosted application/origin | | | | |
| Identity/access-control layer | | | | |

## DNS and Cutover
| Production Hostname | Required Record/Target | Conflicting A/AAAA/ALIAS/CNAME/Local Subdomain Removed | Verification TXT | TTL | Provider Fallback URL | Rollback Trigger/Steps | Status |
|---|---|---|---|---|---|---|---|

## Security and Behavior Tests
| Test | Production Hostname | Provider/Preview/Origin URL | Expected | Result | Evidence |
|---|---|---|---|---|---|
| Anonymous access | | | Denied or intentionally public | | |
| Allowed identity access | | | Authorized | | |
| Disallowed identity access | | | Denied | | |
| Login callback/logout/return URL | | | Final hostname, no loop | | |
| Cookie domain/SameSite/Secure | | | Intended scope | | |
| Canonical/robots/sitemap | | | Intended hostname/indexation | | |
| CSP/CORS/embedded resources | | | No blocked or overbroad origin | | |
| Analytics/client-property isolation | | | Correct property only | | |
```

Do not mark this record complete solely because DNS resolves or the vendor displays “connected.” Access control must be enforced on every reachable route to the same application, or the alternate route must be intentionally documented as public.

---

## 16. Client Intake Templates

### 16.1 Client Intake Worksheet — Purpose and Design Principles

This worksheet is designed to be sent to a prospective or newly-signed client directly — by email, or pasted field-by-field into an online form tool (Google Forms, Typeform, JotForm) so responses arrive ready to save as a `.md`/`.csv` and drop into the engagement's `01-research/` folder. It serves three purposes simultaneously, and every question below is written to satisfy all three at once rather than being asked three separate times:

1. **Populates the Project Charter and Decision Register** directly (Governance, Sec. 3.2) — Industry Module selection, scope, Decision Authority, and the seed facts for `DEC-INIT-001` onward.
2. **Grounds the Stage Gate 5.5 Perplexity Deep Research Brief** (Sec. 16.3 below) in the client's own confirmed facts — service area, licensing, office location, named competitors — so the research pass doesn't drift into inventing or omitting a market the client never confirmed. This is not a hypothetical risk: a real engagement's Perplexity-generated brief omitted the client's own office county from its service-area list and included a neighboring county the client had never actually confirmed serving, both undetected until a later Stage Gate caught them. **This worksheet exists specifically to supply those ground-truth facts before research begins, not after.**
3. **Reduces re-litigation.** Every fact gathered here once should never need to be re-asked in a later Stage Gate — if a later gate needs to confirm something, it confirms *against* what's written here, it doesn't re-derive it from scratch.

**Field-type tags** (`[Short text]`, `[Paragraph]`, `[Multiple choice]`, `[Checkboxes]`, `[Dropdown]`, `[File upload]`) are included so this can be copied directly into a form-building tool without redesigning the field structure. Required fields are marked **(Required)**; everything else may be answered "Not sure yet" or left blank without blocking intake — unanswered fields become Open Questions or Project Backlog items (Governance, Sec. 4.4/7), never guessed.

### 16.2 Client Intake Worksheet — Full Content

```markdown
# New Website Intake Worksheet

Thanks for taking the time to fill this out. The more specific and concrete
your answers — especially factual details like your licensed service area,
credentials, and current online presence — the faster and more accurate your
new website's foundation will be. If you don't know an answer yet, write
"not sure" rather than guessing; we'll follow up on it rather than assume.

---

## Section 1 — About Your Business

1. Business/company name **(Required)** — [Short text]
2. What industry or type of business is this? **(Required)** — [Short text]
   *(e.g., mortgage lending, real estate brokerage, law firm, medical practice,
   home services, financial advisory, SaaS, real estate investing/cash home
   buying, real estate development — if none of these fit, just describe it)*
3. In one or two sentences, what does your business actually do for a
   customer? **(Required)** — [Paragraph]
4. What's your business model? — [Multiple choice: Direct-to-consumer service
   / B2B service / Product sales / Referral or brokerage / Investment or
   acquisition / Other (describe)]
5. What specific offerings, products, programs, or service lines should the
   site cover? **(Required)** — [Paragraph]
6. Do you have a niche specialization or focus that sets you apart within
   your industry? — [Paragraph]

## Section 2 — Service Area & Licensing (the facts we'll research around)

*This section matters more than it might look — everything in Section 6
(competitor and market research) gets built around exactly what you write
here, so please be specific rather than general.*

7. What is your **actual, physical business address** (or the address your
   license/registration is tied to, if different from where you work day to
   day)? **(Required)** — [Short text]
8. What cities, counties, states, or regions do you actually serve?
   **(Required)** — [Paragraph] *(List every one — don't assume "greater
   [metro area]" communicates what you mean. If you serve some areas for one
   service and a wider area for another — e.g., local for one product line,
   nationwide for another — say which is which.)*
9. Are there any nearby areas people might assume you serve that you
   **do not** actually serve? — [Paragraph] *(This prevents us from
   accidentally researching or building content for a market you don't
   actually cover.)*
10. What professional licenses, registrations, or certifications does your
    business or its principals hold? **(Required)** — [Paragraph] *(Include
    license numbers and issuing body/state if you have them handy — e.g., a
    real estate license number and state, an NMLS ID, a bar number, a medical
    board registration. If you're not sure of the exact number right now,
    say "will provide" rather than guessing.)*
11. Is your business a DBA, subsidiary, or otherwise operating under a
    different legal entity name than the brand name customers see? —
    [Short text] *(If yes, name both.)*

## Section 3 — Goals for This Website

12. Is this a brand-new website, a redesign of an existing site, or a full
    rebuild/replatform? **(Required)** — [Multiple choice]
13. What's the single most important outcome you want this website to
    produce? **(Required)** — [Paragraph] *(e.g., more qualified phone
    calls, more form submissions, more listing appointments, more investor
    referrals — be specific about the action, not just "more traffic.")*
14. Do you have any target numbers in mind (e.g., leads per month), or is
    this the first time you'll have a real baseline to measure against? —
    [Paragraph]
15. Is there a deadline or timing consideration we should know about
    (a launch event, a licensing date, a seasonal push)? — [Short text]

## Section 4 — Current Digital Presence

16. Do you currently have a website? — [Multiple choice: Yes / No]
17. If yes, what's the URL? — [Short text]
18. If yes, do you have (or can you get us) access to Google Analytics
    and/or Google Search Console for the current site? — [Multiple choice:
    Yes, I have access / Yes, but I'll need to find/reset it / No / Not
    applicable]
19. What do you like about your current site, if anything? — [Paragraph]
20. What frustrates you about your current site, or what's it missing? —
    [Paragraph]

## Section 5 — Brand & Design

21. Do you have existing brand guidelines, a logo file, or a color
    palette we should use? — [Multiple choice: Yes, I'll upload/send them /
    I have a logo but no formal guidelines / No, we're starting fresh]
22. Logo and brand asset upload (if available) — [File upload]
23. Are there any websites — in your industry or outside it — whose design
    or feel you like? Link them if you can. — [Paragraph]
24. Are there any websites whose design you specifically **don't** want to
    resemble, or any style/tone you want to avoid? — [Paragraph]
25. In a few words, how do you want your site to feel to a visitor? —
    [Short text] *(e.g., "premium and calm," "friendly and approachable,"
    "no-nonsense and fast")*

## Section 6 — Competitors

26. Name at least 2-3 businesses you consider your direct competitors —
    ideally ones you actually compete against for the same customers, not
    just the biggest national names in your industry. **(Required)** —
    [Paragraph, one per line, with a URL if you know it]
27. Is there anything specific you know a competitor does well (or poorly)
    that we should know about? — [Paragraph]

## Section 7 — Team & Decision-Making

28. Who is the main point of contact for this project? **(Required)** —
    [Short text] + email/phone
29. Who has final sign-off authority on the site's strategy and design? —
    [Short text] *(If more than one person, or if a compliance/licensing
    officer holds separate mandatory sign-off on regulated content
    independent of the business-strategy decision-maker, name both roles
    separately — this is common and expected in regulated industries.)*
30. Is there a compliance officer, broker of record, attorney, or other
    professional-standards contact who needs to review site content before
    it's published? — [Short text] *(If yes, name and contact info.)*
31. Are there other staff or practitioners (e.g., agents, loan officers,
    physicians) who should be featured on the site or interviewed for
    content? — [Paragraph]

## Section 8 — Compliance & Advertising Notes

32. Are you aware of any advertising rules, professional-conduct
    restrictions, or required disclosures that apply to your business? —
    [Paragraph] *(You don't need to know the exact legal language — just
    flag anything you're aware of, like "we can't guarantee outcomes" or
    "we have to display our license number.")*
33. Is there any claim, statistic, or statement you've been told NOT to use
    in your marketing, or that a past marketer got wrong? — [Paragraph]

## Section 9 — Technology

*You don't need to know anything technical to answer this section — just
tell us what you already have, if anything.*

34. Do you have an existing hosting provider for your site? — [Multiple
    choice: Yes (please name it) / No / Not sure]
35. Do you already own a domain name, or does one need to be
    purchased/transferred? — [Short text]
36. Do you use any existing business software you'd want the new site to
    connect to (a CRM, a scheduling tool, an application/intake system, an
    IDX/MLS feed, etc.)? — [Paragraph]

*A note on technology, so this section is easy to answer: unless you have a
specific reason to need something different, we build on our standard
technology stack (WordPress, GeneratePress, GenerateBlocks, and the
supporting tools that go with them) — it's what we know best, it keeps your
costs predictable, and it's proven across every site we've built. If you
have an existing hosting provider or software you need to keep, that's
completely fine — just tell us above and we'll work with it. If you'd
prefer a different platform entirely (e.g., a page builder other than ours,
a different CMS) for a specific reason, let us know in Section 10 below —
that's a real option, it's just treated as a custom request with its own
scope and fee rather than our default included approach.*

## Section 10 — Anything Else

37. Is there anything else about your business, your customers, or this
    project that would help us understand what you need? — [Paragraph]
38. Do you have a specific request for a non-standard technology choice
    (see the note above)? If so, what and why? — [Paragraph]
```

### 16.3 Perplexity Deep Research Brief — Prompting Framework

**Purpose.** This is the bridge between the completed Intake Worksheet (Sec. 16.2) and Stage Gate 1 (Discovery & Market Research). Rather than starting Discovery from a blank page, a structured research pass — run in Perplexity or an equivalent deep-research tool — produces a first-draft market/competitor/architecture brief the engagement team reviews, corrects, and formally carries into Stage Gate 1 as a cited input, not as an assumed-correct starting point.

**Where this sits in the sequence, and why.** Generate this prompt only *after* Industry Module selection (New Engagement skill, Step 2) — not before, and not instead of it. The prompt below is deliberately built to inject the *selected* Module's Competitive Landscape Notes and SEO & Keyword Strategy sections as context, so the research pass is scoped by what the framework already knows about this vertical rather than starting from zero. Running this before Module selection produces a generic, unscoped brief; running it after produces one that already speaks the Module's language.

**Why this exists as a formal template.** A real engagement's Perplexity-generated brief both omitted the client's own office county from the recommended service area and included a neighboring county the client had never confirmed — both traceable to the prompt not being explicitly anchored to the Intake Worksheet's confirmed facts. The template below fixes this by structurally requiring every fact in the Worksheet's Section 2 (Service Area & Licensing) to be treated as fixed, non-negotiable input, not a hypothesis for the research tool to revise.

**The Prompt:**

```
You are producing a structured research brief to hand to a website build
team. This brief will be used as a factual, architectural, and competitive
starting point — treat accuracy and sourcing as more important than
breadth or persuasive writing.

## Fixed facts — do not contradict or omit these
[Paste verbatim from the completed Intake Worksheet, Section 2:]
- Business name: [from Worksheet Q1]
- Industry/vertical: [from Worksheet Q2] — operating under the
  [Industry Module name] methodology
- Physical/licensed business address: [from Worksheet Q7]
- Confirmed service area (cities/counties/states): [from Worksheet Q8]
- Explicitly NOT served (if any): [from Worksheet Q9]
- Licenses/registrations held: [from Worksheet Q10]
- Legal entity/DBA structure: [from Worksheet Q11]

Every one of the above facts is confirmed by the client directly. Do not
propose expanding, narrowing, or substituting the service area, and do not
omit the confirmed office location from any geographic recommendation, even
if your own research suggests a neighboring or larger market might be
attractive — if you believe there's a genuine opportunity beyond what's
listed above, note it separately as a suggestion for the team to confirm
with the client, clearly separated from the confirmed facts.

## Business context
[Paste Worksheet Q3, Q5, Q6, Q12-15]

## Named competitors (client-supplied, treat as mandatory research targets)
[Paste Worksheet Q26-27]

## Active Industry Module context
[Paste the selected Industry Module's Competitive Landscape Notes and SEO &
Keyword Strategy sections in full, from the WEF Industry-Modules file]

## What to produce

1. **Objective** — one paragraph restating the business, its confirmed
   service area, and the target outcome (from the Business Objectives
   section above), in your own words, to confirm your own understanding
   before proceeding.
2. **Competitor references** — research each named competitor above, plus
   up to 4 additional real, currently-operating competitors serving the
   *same confirmed geographic area* (not the industry nationally). For each,
   give: URL, what specifically to study (site architecture, content depth,
   local SEO structure, conversion flow, design quality), and cite your
   source for every factual claim about them.
3. **Required site architecture** — propose a pillar-and-cluster sitemap:
   core pages, topic/problem hub pages (informed by the Industry Module's
   typical page types above), location pages for the *confirmed* service
   area only (Section 2's fixed facts), and supporting guide/article topics.
   Every location page proposed must map to a city or county explicitly
   listed in the confirmed service area — flag, don't silently include, any
   location you believe should be added beyond what was confirmed.
4. **SEO content priorities** — a keyword/topic priority model specific to
   this business's actual offerings and confirmed geography, citing the
   reasoning (search intent categories, not just a volume guess).
5. **On-page and content-model guidance** — a reusable outline for each
   major page type identified in #3, and on-page SEO requirements (title/
   meta/schema guidance) consistent with the Industry Module's SEO & Keyword
   Strategy section above.
6. **Trust and conversion requirements** — informed directly by the
   Industry Module's Trust Signal Requirements section above, not generic
   "add testimonials" advice.
7. **Explicit "do not do this" list** — claim risks, design anti-patterns,
   and content mistakes specific to this vertical and this competitive set.

## Sourcing discipline
Cite a source for every competitor fact, market statistic, or claim about
the industry. If you cannot verify something, say so explicitly rather than
presenting an estimate as fact — mark it "[unverified estimate]." Do not
fabricate statistics, review counts, or competitor claims.

## Output format
Return this as a single, well-structured Markdown document, ready to save
as a `.md` file and read directly by the build team — headings, tables, and
bullet lists, not prose paragraphs describing tabular data.
```

**After the research runs.** The returned `.md` file is saved into the engagement's `01-research/` folder as a client-supplied research input — *not* accepted as Stage Gate 1's Discovery Report itself. Per Governance's no-fabrication discipline and the Module Injection Point convention, the Research Consultant (human or AI) reconciles every geographic and factual claim in the returned brief against the Intake Worksheet's Section 2 answers before Stage Gate 1 proceeds — any location, competitor, or claim present in the brief but absent from (or contradicting) the confirmed Worksheet facts is logged as an Open Question or a Decision Register entry requiring client confirmation, never silently carried forward into the Sitemap at Stage Gate 4.

### 16.4 Project Charter Template

*(See Governance, Section 3.2 for required contents; use the following structure)*

```markdown
# Project Charter — [Client Name]

## Engagement Overview
## Active Industry Module(s)
## Business Objectives
## Scope Boundaries (In-Scope / Out-of-Scope)
## Technology Stack
## Regulatory/Compliance Framework
## Roles & Staffing
## Timeline (by Stage Gate)
## Decision Authority (named individuals per gate)
## Success Metrics
## Assumptions & Dependencies
## Change Control Process Reference

**Approved By (Client):**
**Approved By (Engagement Lead):**
**Date:**
```

---

### 16.5 Digital Estate & Access Map Template

```markdown
# Digital Estate & Access Map — [Client Name]

> Record ownership, identifiers, and access status only. Store secrets in the approved credential manager, never in this document.

| System/Asset | Provider/Property/URL | Business Owner | Operational Custodian | Billing/Renewal Owner | Access Status (Verified/Reported/Unknown) | Source of Truth | Recovery/Export Path | Risk/Next Action |
|---|---|---|---|---|---|---|---|---|
| Domain registrar | | | | | | | | |
| Authoritative DNS | | | | | | | | |
| Hosting + exact document root | | | | | | | | |
| Production environment | | | | | | | | |
| Staging environment | | | | | | | | |
| Third-party custom domain(s) + application origin(s) | | | | | | | | |
| CMS | | | | | | | | |
| Source repository + branch | | | | | | | | |
| Deployment integration + exact target | | | | | | | | |
| Backups + last restore test | | | | | | | | |
| Search performance property | | | | | | | | |
| Analytics/tag manager | | | | | | | | |
| Consent manager | | | | | | | | |
| Forms/CRM/email destination | | | | | | | | |
| CDN/security | | | | | | | | |
| Translation/localization | | | | | | | | |

## Legacy Preservation and Cutover
- Authoritative URL inventory/export:
- Content and media export:
- Search/analytics baseline export:
- Redirect map and validation owner:
- DNS TTL/cutover plan:
- Rollback trigger and tested restore point:
- Old-provider shutdown authority and date (never cancel before verified cutover):
```

## 17. Meeting Templates

### 17.1 Kickoff Meeting Agenda

```markdown
# Kickoff Meeting — [Client Name]

1. Introductions & roles (both firm and client sides)
2. Project Charter walkthrough & confirmation, including active Industry
   Module selection
3. Stage Gate 1 discovery interview scheduling
4. Knowledge Base access walkthrough
5. Communication cadence & escalation path
6. Q&A
```

### 17.2 Stage Gate Review Meeting Agenda

```markdown
# Stage Gate [#] Review — [Client Name]

1. Recap of gate objectives and inputs
2. Walkthrough of deliverables
3. Checklist/Exit Criteria review
4. Decisions requiring sign-off
5. Next Stage Gate preview and schedule
```

---

## 18. Risk Registers

```markdown
# Risk Register — [Client Name]

| Risk ID | Description | Category | Likelihood | Impact | Mitigation Plan | Owner | Status |
|---|---|---|---|---|---|---|---|
```
*(Governance, Section 14.2 — see that section for standard WEF risk categories to screen for at initialization)*

---

## 19. Issue Logs

*(See Section 11.2 above — the same Issue Log structure is used at Stage Gate 11 for pre-launch QA and reused for any post-launch defect tracking under Post-Launch Growth Program.)*

---

## 20. Change Requests

*(See Section 3 above for the Change Request template, applicable to Core Methodology changes, Industry Module changes, and engagement-level scope changes alike — the `Scope` field is what distinguishes them.)*

---

## 21. Context Navigation Templates

Templates for the CLAUDE.md/CONTEXT.md navigation layer defined in Governance Sec. 5.2.1. Adopted from the ICM context-management methodology (external reference material; see Governance Sec. 13.2 Change Proposal history for provenance).

### 21.1 Knowledge Base Root — CLAUDE.md Template

Keep this under ~800 tokens (roughly one screen). If it grows longer, move content into `CONTEXT.md` or a stage's own `CONTEXT.md` instead — this file is a map, not a manual.

```markdown
# [Client Name] Website Blueprint

## What This Is
[One to two sentences: who the client is, what this engagement is, which Industry Module(s) govern it.]

## Current State
**Active stage: [NN-stage-name] ([WEF Stage Gate name]).** [One sentence on where things stand.] See `CONTEXT.md` for the full stage map.

## Structure
```
[Client Name] Website Blueprint/
  CLAUDE.md              # You are here.
  CONTEXT.md              # Full WEF Stage Gate map.
  [NN-stage-name]/         # Created only once this stage begins — see CONTEXT.md
    CONTEXT.md
    output/
  _config/                # Charter, Decision Register, and other cross-stage governance docs
  _references/            # Pointers to the WEF framework and active Industry Module(s)
```

## How to Use
1. Read this file first, then `CONTEXT.md` for the full stage map.
2. Go to the active stage's `CONTEXT.md` before touching its `output/`.
3. Read `_config/project-charter.md` and `_config/decision-register.md` before starting any new stage's work.
4. Only create the next stage folder when that stage actually begins.
5. Every new decision goes in `_config/decision-register.md`.

## Layer Annotations (ICM)
- `CLAUDE.md`: L0 (always loaded, orientation)
- `CONTEXT.md`: L1 (stage-gate routing)
- Stage `CONTEXT.md` files: L2 (stage contracts)
- `_config/` files: L3 (engagement-specific reference)
- `_references/` files: L3 (domain reference — the WEF framework itself)
- Stage `output/` and client-supplied source material: L4 (working artifacts)
```

### 21.2 Knowledge Base Root — CONTEXT.md Template

```markdown
# Workflow: [Client Name] Website Blueprint

## Overview
[One to two sentences on which WEF Stage Gates apply and which Industry Module(s) govern them — reference Governance Sec. 1.4/1.5 for module selection/blend, if applicable.]

## Stage Map

| Folder | WEF Stage Gate | Purpose | Status |
|---|---|---|---|
| 01-research | SG1 — Discovery & Market Research | Personas, regulatory footprint, current-state audit | [Not started / Active / Complete] |
| 02-competitive | SG2 — Competitive Intelligence | Competitor scoring, White Space map | ... |
| 03-strategy | SG3 — Strategic Direction | Positioning, messaging pillars (client sign-off) | ... |
| 04-architecture | SG4 — Information Architecture | Sitemap, URL structure, taxonomy | ... |
| 05-seo-blueprint | SG5 — SEO Blueprint | Keyword map, topical clusters, schema plan | ... |
| 06-ux-conversion | SG6 — UX & Conversion | User flows, conversion paths, wireframes | ... |
| 07-design-system | SG7 — Design System | Visual identity, component library | ... |
| 07.5-prototype-validation | SG7.5 — Prototype Validation | Design tournament, executive approval | ... |
| 08-content-spec | SG8 — Content Spec | Page-by-page content briefs | ... |
| 09-copywriting | SG9 — Copywriting | Approved on-page copy | ... |
| 10-ai-build-package | SG10 — AI Build Package | Build-ready implementation spec | ... |
| 10.5-wp-implementation | SG10.5 — WP Implementation | Build record | ... |
| 11-qa | SG11 — QA & Optimization | Sign-off | ... |
| 11.5-post-launch | SG11.5 — Post-Launch Growth | KPIs, experiment log | ... |

## How Stages Connect
[Note any engagement-specific sequencing detail beyond the standard WEF spine — most engagements need none.]

## Reference Material
- `_config/project-charter.md`, `decision-register.md`, and siblings — see Sec. 5.2.1.
- `_references/`: pointers to the WEF framework and active Industry Module(s).

## When to Add Stages
[Name any Service Add-On Modules in scope, per Governance Sec. 1.7 — these get their own folder outside the numbered spine, since they don't gate SG1–SG11.5.]
```

### 21.3 Stage Folder — CONTEXT.md Template (Stage Contract)

One per active Stage Gate folder. A trimmed, engagement-specific instance of that gate's 19-part Core Methodology template — link to the full chapter rather than restating it.

```markdown
# Stage Contract: [NN-stage-name] (WEF Stage Gate [N] — [Stage Gate Name])

**Status:** [Not started / Active / Complete]

## Purpose
[One to two sentences, from the Stage Gate chapter's Sec. 1.]

## Inputs
[This stage's actual inputs — prior stage output, specific Module sections, specific client-supplied material — not a restatement of the chapter's generic input list.]

## Outputs (this stage's `output/`)
[List the actual files this stage will/did produce.]

## Exit Criteria
[Copy the relevant checklist items from the Stage Gate chapter's Exit Criteria section, checked off as completed.]

## What the Next Stage Should Read From Here
[Point the next stage at the specific sections/findings that matter most — don't make it re-read everything.]
```

### 21.4 Naming Convention Standard

Applies alongside the Documentation Standard (Governance Sec. 8.3). Choose one consistent pattern per engagement and state it in the root `CLAUDE.md`; the specific format matters less than consistency, since it's what lets an AI model find and name files correctly without a database.

**WEF default pattern:** `descriptive-name-v{N}.md` (already used throughout this framework's own Required Documents naming, e.g. `discovery-report-v1.md`).

**Alternative status-suffix pattern**, useful for content mid-review: `descriptive-name_draft.md` → `descriptive-name_final.md`. Do not mix both patterns within one engagement's KB.

### 21.5 Practice-Level (Multi-Client) Root

Section 5.2 defines one client's KB. A consulting practice running several WEF engagements at once benefits from the same L0/L1 layering **one level up**, at the practice root — this is a firm-operations convenience, not a per-engagement requirement.

```markdown
# [Firm/Practice Name]

[One sentence: what the practice does.]

## Active Engagements
- /clients/[client-1]/wef — [Industry Module]. Phase: [current Stage Gate].
- /clients/[client-2]/wef — [Industry Module]. Phase: [current Stage Gate].

## Framework
- /wef — the WEF Core Methodology + Industry Module library itself (read-only reference, not engagement-specific).

## Routing
| Task | Go to | Read |
|---|---|---|
| Work for [Client 1] | /clients/[client-1]/wef | CLAUDE.md, CONTEXT.md |
| Work for [Client 2] | /clients/[client-2]/wef | CLAUDE.md, CONTEXT.md |
| Add/revise an Industry Module | /wef/WEF-v1.0/Industry-Modules | 00-Module-Template-and-Index.md |

## Critical Rules
- Never reference one client's Decision Register, Charter, or compliance findings in another client's workspace.
- A new engagement copies the KB structure (Governance Sec. 5.2) and gets its own `_config/`, not a shared one.
```

## 22. Conversion and Operational Handoff Template

### 22.1 Conversion Measurement & Operational Handoff Contract

```markdown
# Conversion Measurement & Operational Handoff Contract — [Client Name]

| Meaningful Action | User Trigger | Success State | Failure/Fallback State | Analytics Event | Parameters (No PII) | Consent Category | Destination/System | Operational Owner | Notification | Confirmed Response Expectation | Test Evidence | Failure Escalation |
|---|---|---|---|---|---|---|---|---|---|---|---|---|

## Destination and Routing Verification
- Correct client property/account verified:
- Test submission/transaction ID (non-sensitive):
- Destination receipt confirmed by:
- Duplicate/spam handling:
- Outage/manual fallback:
- Data retention/deletion owner:

## Visitor Promise Check
- Confirmation message accurately states what happens next:
- Response-time promise confirmed by the operating team:
- Alternate contact path is visible and functional:
- Privacy/consent language matches actual routing and tracking:
```

---

## 23. Cross-Engagement Contribution Templates

### 23.1 WEF-Candidate-Findings.md Template

Per Governance Sec. 15.6 (Cross-Engagement Contribution Pipeline). Every engagement Knowledge
Base gets one of these — created at initialization (New Engagement skill, Step 6) and appended
to live, whenever this engagement is active. It is the Layer 1 capture point that lets a
periodic `wef-sync` pass find every candidate finding across every concurrently-running
engagement without depending on anyone remembering to raise it separately.

```markdown
# WEF Candidate Findings — [Client/Engagement Name]

Log anything discovered live on this engagement that looks like a reusable Core Methodology or
Industry Module improvement — confirmed lessons and partial "might be nothing yet" observations
are both worth a row; triage happens at sync, not at write time. See the framework repository's
Governance Sec. 15.6 for how these get deduplicated and merged back.

| Date | Stage Gate | Description | Target Section (if known) | Status | CR ID |
|---|---|---|---|---|---|
```

**Status values:**
- `Flagged` — default on creation; not yet reviewed against the Revision Log.
- `Staged` — claimed by a reserved Change Request; a branch/PR is in flight (CR ID filled in).
- `Merged` — landed in the framework's `main`; safe to treat as adopted.
- `Rejected` — reviewed and not generalizable, or a duplicate of an existing CR (note which one,
  and why, in the Description column rather than deleting the row — the row itself is the record
  that this was considered).

Never delete a row on this log, even once `Merged` or `Rejected` — it's the audit trail that
makes the Layer 2 dedup check in Governance Sec. 15.6 actually trustworthy across sessions and
across time, the same way the Engagement Retrospective Register (Governance, Sec. 15.2) never
deletes an entry once filed.

---

*End of Core Methodology. Continue to Industry Modules.*
