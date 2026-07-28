# INDUSTRY MODULE — SAAS

*Website Excellence Framework (WEF) v1.0 — Module Version 1.0*

---

## 1. Module Overview & Applicability

This Module applies to B2B and B2C software-as-a-service companies marketing a subscription software product. It is the lowest-regulatory-intensity Module in the current library, but is not compliance-free — data privacy, accessibility, and security-claim substantiation still apply, and intensify if the SaaS product itself sells into a regulated vertical (e.g., a SaaS product for healthcare practices inherits HIPAA-adjacent expectations even though the marketing site itself is not a covered entity).

**Blend commonly with:** Home Services Module (secondary, where a home services company also licenses its own operational software to franchisees/other operators).

**Does not fit well:** Consumer mobile apps with no web-based purchase/trial flow (the conversion mechanics here assume a website-driven trial-signup or demo-request funnel), and enterprise software sold exclusively through a human sales cycle with no self-serve component (the UX patterns here lean toward supporting both self-serve and sales-assisted models, but a pure enterprise motion will need lighter adaptation).

## 2. Regulatory & Compliance Landscape

- **Data privacy regulation** — GDPR (if serving EU users), CCPA/CPRA (if serving California residents), and other state privacy laws apply to the marketing site itself (cookie consent, privacy policy) and are a component of the product's own compliance posture if it's referenced in marketing claims.
- **FTC advertising/substantiation rules** — apply to performance claims ("reduces churn by 40%"), security claims ("bank-level encryption"), and comparison claims against named competitors.
- **Accessibility (ADA Title III litigation exposure)** — SaaS marketing sites are a common target of accessibility litigation in the U.S.; WCAG 2.1 AA compliance is a genuine legal-risk mitigation here, not just a best practice.
- **Vertical-inherited compliance** — if the SaaS product serves a regulated vertical (healthcare, financial services, legal), marketing claims about the product's compliance capabilities (e.g., "HIPAA-compliant," "SOC 2 Type II certified") must be accurate and current, and are frequently over-claimed.
- **Uptime/SLA claims** — if referenced in marketing content, must match the actual contractual SLA, not aspirational figures.

**Known claim-risk language patterns:** unsubstantiated performance/ROI statistics ("saves you 10 hours a week") without a cited methodology, security/compliance certification claims that are outdated or inaccurate (e.g., claiming a SOC 2 report that has lapsed), and named-competitor comparison claims that could constitute disparagement if inaccurate.

## 3. Persona Library

| Persona | Primary Need | Top Decision Drivers | Top Objections |
|---|---|---|---|
| Individual Evaluator/Champion | Researching a solution to bring to their team/manager | Fast time-to-value in a trial, clear feature-to-need mapping, credible social proof | Fear of championing a tool that fails to get budget approval or adoption |
| Economic Buyer (budget holder) | Justifying spend against ROI | Case studies with quantified results, pricing transparency, security/compliance posture | Fear of buyer's remorse, hidden costs, vendor lock-in |
| Technical Evaluator (IT/security/engineering) | Assessing integration, security, and technical fit | API/integration documentation quality, security certifications, uptime history | Vague or missing technical documentation, unsubstantiated security claims |
| Existing Customer (expansion/renewal) | Evaluating whether to expand usage or renew | Product roadmap credibility, account management quality, demonstrated ROI since adoption | Feeling under-supported post-sale, unclear upgrade path |
| Free/Self-Serve Trial User | Getting immediate value with minimal friction | Fast onboarding, clear next-step guidance, low-pressure upgrade path | Overwhelming onboarding, aggressive upgrade prompts before value is demonstrated |

## 4. Competitive Landscape Notes

Typical SaaS marketing sites cluster into: (1) well-funded competitors with strong design polish and heavy social-proof density (logos, case studies) but sometimes generic, jargon-heavy messaging; (2) earlier-stage competitors with clearer differentiation messaging but weaker technical content depth (API docs, security pages) and design polish; (3) legacy/enterprise incumbents with strong trust signals (established customer base, compliance certifications) but dated UX and slow-loading, feature-bloated sites. Table stakes: pricing page (or "contact sales" if enterprise-only), feature pages, case studies/logos, a trial/demo CTA. Common differentiator gap: genuine technical depth for the Technical Evaluator persona (most sites under-serve this persona relative to how influential they are in the buying decision) and honest, specific ROI substantiation rather than generic productivity claims.

## 5. Positioning & Messaging Patterns

Proven angles: "the [category] tool built specifically for [underserved niche/workflow]," "the alternative to [incumbent] without [specific incumbent pain point]," "the platform that [specific, quantified outcome] for teams like yours." Avoid generic "all-in-one platform" positioning without a specific wedge. Flag for compliance: any quantified performance claim ("40% faster," "$X saved") needs a cited methodology or customer source; any named-competitor comparison needs factual accuracy review to avoid disparagement exposure.

## 6. Information Architecture Patterns

Typical required page types: Home; Product/Feature pillar pages (organized by feature area or by use case/persona); Solutions/Use-Case pages (by persona or by industry vertical the SaaS serves); Pricing page; Customer Stories/Case Studies (individual + index); Security/Trust/Compliance page (certifications, data handling, uptime); Integrations/API documentation hub; Resources (blog, guides, comparison pages); required compliance pages (Privacy Policy, Terms of Service, Cookie Policy, Accessibility Statement, DPA/subprocessor list if enterprise-targeted).

## 7. SEO & Keyword Strategy

High-value topical clusters: use-case/persona + product category ("[job title] project management software"), competitor-alternative content ("[Competitor] alternatives," "[Competitor] vs [Client]" — factual-accuracy-reviewed), and problem/solution educational content. Recommended schema: `SoftwareApplication` (product pages, include `applicationCategory`, `offers` for pricing), `Organization` (homepage), `Review`/`AggregateRating` (where genuinely sourced from a review platform like G2/Capterra, never fabricated), `FAQPage`, `BreadcrumbList`. Claim-risk keyword patterns: avoid unqualified superiority claims in competitor-comparison content; ensure factual accuracy on any comparison table before publishing.

## 8. Trust Signal Requirements

Customer logos and case studies with real, verifiable outcomes (quantified where the client can substantiate the figure). Security/compliance certifications (SOC 2, ISO 27001, HIPAA-readiness, etc.) displayed accurately and kept current — a lapsed certification claim is both a compliance and a credibility risk. Uptime/status page linked where relevant to the Technical Evaluator persona. G2/Capterra/other third-party review platform ratings embedded where genuine. Clear, jargon-free pricing (or an honest "contact sales" model where usage-based/enterprise pricing genuinely can't be simplified).

## 9. Content Model & Page Types

| Page Type | Required Content Elements |
|---|---|
| Product/Feature Page | Specific capability explanation, use-case framing, screenshot/demo visual, relevant persona CTA (trial/demo) |
| Solutions/Use-Case Page | Persona- or vertical-specific framing of the product's value, case study reference, tailored CTA |
| Case Study Page | Specific, quantified outcome, customer context, methodology transparency (how the number was measured) |
| Security/Trust Page | Current certification list, data handling summary, uptime reference, subprocessor list if applicable |
| Pricing Page | Clear tier structure, feature-to-tier mapping, honest handling of usage-based or custom-quote elements |

## 10. Stage Gate Injection Map

| Core Stage Gate | What This Module Supplies |
|---|---|
| SG1 Discovery | Persona Library (Sec. 3), Regulatory Landscape seed (Sec. 2) |
| SG2 Competitive Intelligence | Competitive Landscape Notes (Sec. 4) |
| SG3 Strategic Direction | Positioning & Messaging Patterns (Sec. 5) |
| SG4 Information Architecture | IA Patterns (Sec. 6) |
| SG5 SEO Blueprint | SEO & Keyword Strategy (Sec. 7), competitor-alternative content pattern |
| SG6 UX & Conversion | Trust Signal Requirements (Sec. 8), trial/demo signup flow pattern |
| SG7/7.5 Design | Trust Signal visual treatment (Sec. 8), product-screenshot/demo visual conventions |
| SG8/9 Content & Copy | Content Model (Sec. 9), ROI/performance claim substantiation review |
| SG11 QA | Full Regulatory Landscape final checklist (Sec. 2), certification-currency verification |
| SG11.5 Growth | Persona validation (Sec. 3), self-serve funnel conversion-rate optimization |

## 11. Module-Specific Prompt Library Additions

**Prompt SAAS.1 — Competitor Comparison Accuracy Check**

```
Review the attached "[Client] vs [Competitor]" comparison page/table for
[Client Name]'s SaaS website. For each factual claim about the
competitor's product, flag whether it is (a) sourced from the
competitor's own current public documentation/pricing, (b) potentially
outdated, or (c) unverifiable from the materials provided. Do not assert
a competitor's feature set or pricing as current without a citable,
recent source — flag anything unverifiable for the team to confirm before
publication, since inaccurate comparison claims carry disparagement risk.
```

## 12. Module Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-07-23 | Initial module authored as part of the WEF Core + Modules re-architecture |

---

*This concludes the Industry Modules library for WEF v1.0. Continue to Back Matter.*
