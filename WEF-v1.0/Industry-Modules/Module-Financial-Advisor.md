# INDUSTRY MODULE — FINANCIAL ADVISOR

*Website Excellence Framework (WEF) v1.0 — Module Version 1.0*

---

## 1. Module Overview & Applicability

This Module applies to Registered Investment Advisors (RIAs), independent broker-dealer-affiliated advisors, and financial planning practices marketing directly to individual and family clients. It assumes a relationship-based, high-trust advisory sales model rather than a transactional brokerage/trading platform.

**Blend commonly with:** Law Firm Module (secondary, for advisory practices with embedded estate-planning legal services).

**Does not fit well:** Retail trading platforms, robo-advisors, or institutional asset management marketing to other institutions rather than individual clients — each has a materially different regulatory and UX model.

## 2. Regulatory & Compliance Landscape

- **SEC Marketing Rule (Investment Advisers Act Rule 206(4)-1)** — governs testimonials, endorsements, third-party ratings, and performance advertising for SEC-registered advisors; testimonials and endorsements are permitted only with specific required disclosures.
- **FINRA advertising rules** — apply to broker-dealer-affiliated advisors' communications with the public (Rule 2210 and related), including principal review/approval requirements for certain content before publication.
- **State securities regulator rules** — apply to state-registered (rather than SEC-registered) advisors; verify the client's actual registration status.
- **Form ADV disclosure** — advisors must make Form ADV Part 2 (the "brochure") available to clients/prospects; many firms link it from the website, and website claims must be consistent with Form ADV representations.
- **CRD number (Central Registration Depository)** — the individual/firm identifier, checkable via FINRA BrokerCheck or SEC IAPD, analogous in role to an NMLS ID.

**Known claim-risk language patterns:** performance claims without required disclosures (net-of-fee basis, time period, benchmark comparison), guaranteed-return language (never permissible for securities-related advice), testimonials without the SEC Marketing Rule's required disclosures (compensation, conflicts of interest), and "fiduciary" claims that must accurately reflect the advisor's actual regulatory status (not all financial professionals are fiduciaries at all times).

## 3. Persona Library

| Persona | Primary Need | Top Decision Drivers | Top Objections |
|---|---|---|---|
| Pre-Retiree | Retirement income and transition planning | Advisor's specific retirement-planning expertise, clarity on fee structure | Fear of running out of money, distrust of commission-driven advice |
| Recent Inheritance/Windfall Recipient | Guidance on a sudden, unfamiliar financial situation | Discretion, patience, education-first approach (not high-pressure sales) | Fear of being taken advantage of, decision paralysis |
| High-Net-Worth Family | Comprehensive wealth management, often multi-generational | Sophistication, breadth of services (tax, estate, investment coordination), discretion | Finding an advisor who can handle genuine complexity, not just investment selection |
| Young Professional/Early Accumulator | Getting started with a real financial plan | Approachability, fee transparency for a smaller portfolio, education | Feeling too small/unimportant for a "real" advisor, fee structure opacity |
| Business Owner (exit/succession planning) | Business valuation, exit strategy, succession-linked financial planning | Advisor's specific experience with business owners, coordination with other professionals (attorney, CPA) | Advisors who only understand personal, not business, financial complexity |

## 4. Competitive Landscape Notes

Typical financial advisor sites cluster into: (1) large wirehouse/broker-dealer advisor pages built on a corporate template with minimal differentiation between advisors; (2) independent RIA sites with strong personal branding but thin, generic "our philosophy" content lacking specific proof points; (3) niche-focused advisors (e.g., advisors for physicians, for divorcing spouses, for tech-equity-compensation clients) with strong differentiation but sometimes weak technical SEO. Table stakes: advisor bio, CRD-checkable credentials, contact form, Form ADV link. Common differentiator gap: genuine fee transparency (many sites still avoid stating fee structure clearly) and niche-specific educational content addressing the exact financial situation a target persona is in.

## 5. Positioning & Messaging Patterns

Proven angles: "the fee-only fiduciary for [specific niche — physicians, business owners, divorcing spouses]," "the advisor who coordinates your full financial picture, not just your portfolio," "the planning-first alternative to a product-sales-driven advisor." Avoid generic "personalized wealth management" positioning. Flag for compliance: any "fiduciary" claim must accurately reflect actual regulatory status at all times the claim is made (not just at account opening); any performance or outcome claim requires SEC Marketing Rule-compliant disclosure.

## 6. Information Architecture Patterns

Typical required page types: Home; Services pillar pages (Financial Planning, Investment Management, Retirement Planning, Estate Planning Coordination, Tax Planning Coordination); Persona/niche hub pages (e.g., "Financial Planning for Physicians"); Advisor/Team profile pages (with CRD number and registration status); Fee Structure/Transparency page; Resources/Insights library; required compliance pages (Form ADV link, Privacy Policy, Accessibility Statement, general disclosure/disclaimer page covering advisory relationship terms).

## 7. SEO & Keyword Strategy

High-value topical clusters: niche/persona + service ("financial planning for physicians," "retirement planning [city]"), situational/educational content ("how to plan for a business exit," "what to do with an inheritance"), and fee-transparency content (increasingly a differentiating search topic as consumers actively search "fee-only financial advisor near me"). Recommended schema: `FinancialService` (homepage), `LocalBusiness` (office locations), `Person` (advisor profiles, include CRD number as identifier), `FAQPage`, `BreadcrumbList`. Claim-risk keyword patterns: avoid "guaranteed returns" or implied-performance terms; prefer planning-process and fee-transparency terms.

## 8. Trust Signal Requirements

CRD number and registration status (SEC- or state-registered) displayed on advisor profiles, checkable against FINRA BrokerCheck/SEC IAPD. Fee structure stated clearly and specifically (fee-only vs. fee-based vs. commission, and the actual percentage/structure where feasible) — this is one of the single highest-trust-impact disclosures in this vertical. Form ADV Part 2 linked and current. Any credential (CFP®, CFA, ChFC, etc.) displayed accurately with the certifying body's actual mark/requirements respected. Any testimonial or endorsement carries the SEC Marketing Rule's required disclosure.

## 9. Content Model & Page Types

| Page Type | Required Content Elements |
|---|---|
| Service Pillar Page | Plain-language service explanation, process overview, fee-structure reference or link, advisor CTA, FAQ block |
| Advisor/Team Profile | Photo, CRD number, credentials (accurately represented), bio, niche/specialty, registration status statement |
| Fee Transparency Page | Specific, clear fee structure explanation, comparison to alternative models if honestly presentable |
| Niche/Persona Hub Page | Situational education addressing the specific persona's financial complexity, relevant advisor CTA |

## 10. Stage Gate Injection Map

| Core Stage Gate | What This Module Supplies |
|---|---|
| SG1 Discovery | Persona Library (Sec. 3), Regulatory Landscape seed (Sec. 2) |
| SG2 Competitive Intelligence | Competitive Landscape Notes (Sec. 4) |
| SG3 Strategic Direction | Positioning & Messaging Patterns (Sec. 5) |
| SG4 Information Architecture | IA Patterns (Sec. 6) |
| SG5 SEO Blueprint | SEO & Keyword Strategy (Sec. 7) |
| SG6 UX & Conversion | Trust Signal Requirements (Sec. 8), consultation-booking flow pattern |
| SG7/7.5 Design | Trust Signal visual treatment (Sec. 8), professional visual convention notes |
| SG8/9 Content & Copy | Content Model (Sec. 9), full Regulatory Landscape (Sec. 2), SEC Marketing Rule testimonial review |
| SG11 QA | Full Regulatory Landscape final checklist (Sec. 2), CRD/Form ADV link verification |
| SG11.5 Growth | Persona validation (Sec. 3) |

## 11. Module-Specific Prompt Library Additions

**Prompt FA.1 — SEC Marketing Rule Testimonial Compliance Scan**

```
Review the attached testimonial or endorsement content for [Client Name]'s
financial advisory website. Confirm whether the required SEC Marketing
Rule disclosures are present: whether the person is a client, whether
compensation was provided, and any material conflicts of interest.
Flag any testimonial missing these disclosures for Compliance/Standards
Liaison review — do not draft final disclosure language yourself; this
requires the firm's actual compensation/relationship facts.
```

## 12. Module Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-07-23 | Initial module authored as part of the WEF Core + Modules re-architecture |

---

*Continue to the SaaS Module.*
