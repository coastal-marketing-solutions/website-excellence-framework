# INDUSTRY MODULE — REAL ESTATE

*Website Excellence Framework (WEF) v1.0 — Module Version 1.1 (Working Draft)*

---

## 1. Module Overview & Applicability

This Module applies to real estate brokerages, agent teams, and individual agents marketing residential (and, with light adaptation, commercial) property services — listing representation, buyer representation, and property search experiences.

**Blend commonly with:** Mortgage Lending Module (secondary, for brokerages with an in-house lending arm).

**Does not fit well:** Pure property management companies with no sales/brokerage component (closer to Home Services in service model) — usable as a starting template but expect meaningful adaptation.

## 2. Regulatory & Compliance Landscape

- **State real estate commission rules** — advertising, disclosure, and license-display requirements vary significantly by state; license number display is near-universal.
- **Fair Housing Act** — the single most important compliance constraint on real estate marketing: imagery, language, and any implication of steering by protected class must be avoided across listing descriptions, persona targeting, and neighborhood-description content.
- **MLS (Multiple Listing Service) rules of the local board** — govern how listing data may be displayed, syndicated, and attributed (IDX compliance).
- **NAR/state association advertising rules** — team name display, "Realtor" trademark usage, brokerage-of-record display requirements.
- **RESPA** — applies if the brokerage has any affiliated business arrangement (title, lending, insurance) requiring Affiliated Business Arrangement disclosures.

**Known claim-risk language patterns:** neighborhood description language that could be read as steering ("family-friendly," "up-and-coming" tied to demographic change), unsubstantiated "top producer" or ranking claims, and listing count/sales volume claims without a verifiable source.

## 3. Persona Library

| Persona | Primary Need | Top Decision Drivers | Top Objections |
|---|---|---|---|
| First-Time Buyer | Guided home search and purchase process | Trustworthy guidance, local market education, patience with questions | Overwhelm, fear of overpaying, not knowing what they can afford |
| Relocation Buyer | Out-of-area purchase, often time-compressed | Deep local/neighborhood knowledge, virtual tour capability, responsiveness across time zones | Inability to see properties in person, unfamiliarity with area |
| Move-Up/Move-Down Seller-Buyer | Simultaneous sale and purchase | Coordinated timing, accurate pricing on both sides | Timing risk, double-move logistics, pricing their home correctly |
| Investor Buyer | Cash-flow or appreciation-focused acquisition | Data (rent comps, cap rates, appreciation trends), speed on off-market deals | Agent lacking investment-specific analysis skill |
| Luxury Seller | Maximum exposure and discretion for a high-value listing | Marketing sophistication, professional photography/video, agent's luxury track record | Generic marketing treatment of a distinctive property |

## 4. Competitive Landscape Notes

Typical real estate sites cluster around three patterns: (1) large portal-style brokerage sites with strong IDX search but generic, low-personality agent bios; (2) individual agent sites built on generic templates with heavy stock photography and thin local content; (3) team sites with strong personal branding but weak topical SEO depth on specific neighborhoods. Table stakes: IDX/MLS search, agent bio with license number, contact form. Common differentiator gap: genuine neighborhood-level content depth (school data, walkability, market trend narrative) and video/visual property storytelling beyond the MLS photo set.

## 5. Positioning & Messaging Patterns

Proven angles: "the neighborhood specialist who knows [specific area] better than anyone," "the data-driven agent for investors," "the full-service team that handles [relocation logistics / luxury discretion / first-time buyer education] end to end." Avoid generic "your trusted real estate partner" positioning. Flag for compliance: any "top producer," "#1 agent," or sales volume claim needs a verifiable, current source (e.g., MLS-verified statistics, not self-reported).

## 6. Information Architecture Patterns

Typical required page types: Home; Buy (search/IDX, buyer process guide); Sell (listing valuation tool, seller process guide); Neighborhood/community pages (one per target area); Agent/Team profile pages with license numbers; Listings (individual property pages via IDX feed); Resource/guide library (market reports, buyer/seller guides); required compliance pages (brokerage-of-record disclosure, Fair Housing statement, Affiliated Business Arrangement disclosure if applicable, Privacy Policy, Accessibility Statement).

## 7. SEO & Keyword Strategy

High-value topical clusters: neighborhood-specific content ("homes for sale in [neighborhood]," "[neighborhood] real estate market trends"), persona-driven guides ("relocating to [city] guide," "first time home buyer [city]"), and agent/team local-authority content. Recommended schema: `RealEstateAgent` or `RealEstateListing` (property pages), `LocalBusiness` (brokerage/team), `Person` (agent profiles, include license number as identifier), `FAQPage`, `BreadcrumbList`. IDX-fed listing pages require careful canonicalization and indexation strategy to avoid thin/duplicate-content penalties across syndicated listings.

## 8. Trust Signal Requirements

Agent/broker license number visible on every agent bio and in the footer. Brokerage-of-record name and logo per local MLS/association rules. Client testimonials and closed-transaction proof points (with permission). Professional photography of agents and properties — this is a higher-stakes visual trust signal in real estate than in most other verticals. MLS/IDX attribution statement where required by local board rules.

## 9. Content Model & Page Types

| Page Type | Required Content Elements |
|---|---|
| Neighborhood Page | Market trend data, school information, walkability/lifestyle content, featured listings in the area, agent CTA |
| Agent/Team Profile | Photo, license number, bio, specialties, service area, testimonials, active listings |
| Buy/Sell Process Page | Step-by-step process guide, embedded valuation or search tool, FAQ block |
| Individual Listing Page | MLS-sourced data, photos/video, virtual tour if available, agent contact, Fair Housing-compliant description |

**School-information boundary:** Treat school content as factual, attributed decision-support information—not as a proxy for neighborhood desirability or demographic composition. Name the publisher, metric, scale, reporting period, and access or observation date. Distinguish broad district context from address-specific attendance assignment; do not infer that a property is assigned to a school from proximity, a map pin, an aggregator, or a postal boundary. Direct users to the responsible district or other authoritative enrollment source for current address verification, and route school-related framing through Fair Housing review before publication.

## 10. Stage Gate Injection Map

| Core Stage Gate | What This Module Supplies |
|---|---|
| SG1 Discovery | Persona Library (Sec. 3), Regulatory Landscape seed (Sec. 2) |
| SG2 Competitive Intelligence | Competitive Landscape Notes (Sec. 4) |
| SG3 Strategic Direction | Positioning & Messaging Patterns (Sec. 5) |
| SG4 Information Architecture | IA Patterns (Sec. 6) |
| SG5 SEO Blueprint | SEO & Keyword Strategy (Sec. 7) |
| SG6 UX & Conversion | Trust Signal Requirements (Sec. 8), home valuation/search tool patterns |
| SG7/7.5 Design | Trust Signal visual treatment (Sec. 8), photography/imagery standards |
| SG8/9 Content & Copy | Content Model (Sec. 9), full Regulatory Landscape (Sec. 2), Fair Housing language review |
| SG11 QA | Full Regulatory Landscape final checklist (Sec. 2), IDX data accuracy check |
| SG11.5 Growth | Persona validation (Sec. 3) |

## 11. Module-Specific Prompt Library Additions

**Prompt RE.1 — Fair Housing Compliance Scan**

```
Review the attached neighborhood/community page copy for [Client Name]'s
real estate website for any language that could be read as steering
under the Fair Housing Act — including demographic-coded language,
implications about who a neighborhood is "for," or school-quality framing
that correlates with protected-class composition. Flag specific phrases
and suggest neutral, factual alternatives (walkability, commute times,
amenity proximity, verified market data) rather than asserting
replacement language yourself as final — route to Compliance/Standards
Liaison.
```

**Prompt RE.2 — School Information Accuracy & Fair Housing Scan**

```
Review the attached neighborhood/community or listing-page school content for
[Client Name]. For every school-related statement, identify the publisher,
metric, scale, reporting period, and access/observation date. Separate district-
level context from address-specific attendance assignment. Flag any assignment
claim not verified through the responsible district or other authoritative
enrollment source, and flag subjective school-quality or neighborhood-
desirability framing that may create Fair Housing risk. Recommend neutral,
attributed wording and a direct verification path; route final language to the
Compliance/Standards Liaison.
```

## 12. Module Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-07-23 | Initial module authored as part of the WEF Core + Modules re-architecture |
| 1.1 (Working Draft) | 2026-08-13 | Added a school-information accuracy and Fair Housing boundary: attributed metrics and dates, district context separated from address-specific attendance assignment, direct authoritative verification, and a reusable review prompt. Pending formal Governance Board approval. |

---

*Continue to the Law Firm Module.*
