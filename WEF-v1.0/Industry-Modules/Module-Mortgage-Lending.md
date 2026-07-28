# INDUSTRY MODULE — MORTGAGE LENDING

*Website Excellence Framework (WEF) v1.0 — Module Version 1.0*

---

## 1. Module Overview & Applicability

This Module applies to retail mortgage lenders, mortgage brokers, wholesale lenders with a consumer-facing arm, and credit unions with a significant mortgage origination business. It is the source Module for what was originally published as the standalone *Mortgage Website Excellence Framework (MWEF) v1.0* (preserved intact at `/MWEF-v1.0/`); this Module is that manual's vertical-specific content, re-expressed against the Core Methodology's fixed template.

**Blend commonly with:** Real Estate Module (for brokerages with an in-house lending arm — Real Estate as primary, this Module as secondary, governing the lending sub-section of the site).

**Does not fit well:** Commercial/business lending, hard-money/private lending with no retail consumer component — these would warrant a distinct future Module rather than a forced fit here.

## 2. Regulatory & Compliance Landscape

- **Truth in Lending Act (TILA)** and **Regulation Z** — governs disclosure of credit terms, APR representations, and advertising of credit terms.
- **Real Estate Settlement Procedures Act (RESPA)** and **Regulation X** — governs referral fees, disclosures, and settlement service practices.
- **Equal Credit Opportunity Act (ECOA)** and **Regulation B** — prohibits discrimination in credit decisions; affects both underwriting-adjacent content and advertising targeting.
- **SAFE Mortgage Licensing Act** — requires individual loan officer licensing via the **Nationwide Multistate Licensing System (NMLS)**; NMLS ID display is a near-universal requirement on both organization and individual pages.
- **Fair Housing Act** — equal housing lender statement and imagery/messaging review.
- **CFPB advertising and UDAAP guidance** — governs unfair, deceptive, or abusive acts or practices in advertising, including rate advertising and "trigger term" rules under TILA.
- **State-specific mortgage lending and advertising regulations** — vary by state; verify against the client's actual licensed-state list, not their marketing material.

**Known claim-risk language patterns:** approval-odds claims ("guaranteed approval," "everyone qualifies"), timeline claims ("close in 24 hours") without qualifying language, rate claims without required trigger-term disclosures (a stated rate, monthly payment, or down payment amount triggers additional required disclosures under Regulation Z), and "no closing cost" claims that omit how costs are actually absorbed.

## 3. Persona Library

| Persona | Primary Need | Top Decision Drivers | Top Objections |
|---|---|---|---|
| First-Time Buyer, Credit-Anxious | Low-down-payment, forgiving-credit programs (FHA, first-time buyer programs) | Perceived approval likelihood, clear step-by-step guidance | Fear of rejection, confusion about required documents, distrust of "too good to be true" advertising |
| Move-Up Buyer, Rate-Sensitive | Conventional/jumbo purchase financing | Competitive rate, speed to close, ability to compete in a multiple-offer market | Losing a bidding war due to financing contingencies, rate volatility |
| Cash-Out Refinancer | Home equity access for debt consolidation or major expense | Total cost of the loan, clarity on new payment | Distrust of "too easy" cash-out offers, confusion about equity calculations |
| Veteran/Military Borrower | VA loan programs | Zero-down eligibility, VA-specific guidance, respectful treatment of service | Lenders who don't understand VA-specific requirements |
| Self-Employed/Non-QM Borrower | Alternative documentation loan programs | Whether the lender genuinely understands non-traditional income | Being declined or steered by lenders unfamiliar with their situation |

## 4. Competitive Landscape Notes

Typical mortgage lender websites cluster into two failure patterns: (1) large national brands with strong technical SEO and brand trust but generic, low-empathy content and multi-step application friction; (2) small local lenders/brokers with strong personal-relationship positioning but weak technical SEO, thin content, and dated design. Table stakes: rate table or "check rates" CTA, NMLS disclosure, equal housing statement. Common differentiator gap: state-specific content depth (most multi-state lenders treat all states identically despite materially different loan limits and programs) and calculator quality (most calculators require full contact info before showing any result).

## 5. Positioning & Messaging Patterns

Proven angles: "the lender that replaces rate-shopping anxiety with transparency," "the specialist for [underserved segment — self-employed, first-time buyers, veterans]," "the local lender with [national lender] speed." Avoid generic "trusted local lender" positioning — it fails to differentiate and produces weak downstream content. Flag for compliance: any positioning built around speed ("fastest closing") or cost ("lowest rates") claims requires substantiation and trigger-term-compliant qualifying language.

## 6. Information Architecture Patterns

Typical required page types: Home; Loan Program pillar pages (Conventional, FHA, VA, USDA, Jumbo, Non-QM/Self-Employed, Refinance, HELOC); Persona hub pages (First-Time Buyer, Veteran, Self-Employed); State/location pages nested under each loan program for multi-state lenders; Loan Officer directory and individual profile pages; Rate/Application entry point; Resource/guide library; required compliance pages (Licensing/NMLS Consumer Access link, state-specific disclosures per licensed state, Privacy Policy, Accessibility Statement, Equal Housing Lender statement).

## 7. SEO & Keyword Strategy

High-value topical clusters: loan-program-by-state (e.g., "FHA loans Texas"), persona-driven informational content ("first time home buyer down payment assistance [state]"), and rate/payment calculator-adjacent content. Recommended schema: `FinancialService` or `Organization` (homepage), `LocalBusiness` (per licensed branch/state), `Person` with an `identifier` property for NMLS ID (loan officer profiles — display NMLS ID as visible text in addition to schema, per compliance), `FAQPage` (guide content), `BreadcrumbList`. Claim-risk keyword patterns: avoid targeting "guaranteed approval," "no credit check," or unqualified rate-comparison terms.

## 8. Trust Signal Requirements

NMLS ID must be visible (not just in schema) on the homepage footer and every loan officer profile. Equal Housing Lender logo/statement on every page with a lending offer. Loan officer bio cards should include photo, NMLS ID, direct contact, and years of experience. Security signals (SSL, data-handling statement) near any form collecting SSN or financial data. State-specific licensing statement in the footer, dynamically reflecting the visitor's relevant state where feasible.

## 9. Content Model & Page Types

| Page Type | Required Content Elements |
|---|---|
| Loan Program + State Page | State-specific loan limits, eligibility requirements, down payment/credit guidance, embedded calculator, FAQ block, loan officer CTA, state licensing statement |
| Loan Officer Profile | Photo, NMLS ID, bio, contact, service area, testimonials (if compliance-cleared) |
| Persona Hub | Step-by-step guidance, common objections addressed directly, calculator, relevant program links |
| Compliance Pages | NMLS/licensing page, per-state disclosure pages, privacy policy, accessibility statement |

## 10. Stage Gate Injection Map

| Core Stage Gate | What This Module Supplies |
|---|---|
| SG1 Discovery | Persona Library (Sec. 3), Regulatory Landscape seed (Sec. 2) |
| SG2 Competitive Intelligence | Competitive Landscape Notes (Sec. 4) |
| SG3 Strategic Direction | Positioning & Messaging Patterns (Sec. 5) |
| SG4 Information Architecture | IA Patterns (Sec. 6) |
| SG5 SEO Blueprint | SEO & Keyword Strategy (Sec. 7) |
| SG6 UX & Conversion | Trust Signal Requirements (Sec. 8), calculator patterns (affordability/payment calculators) |
| SG7/7.5 Design | Trust Signal visual treatment (Sec. 8) |
| SG8/9 Content & Copy | Content Model (Sec. 9), full Regulatory Landscape (Sec. 2) |
| SG11 QA | Full Regulatory Landscape final checklist (Sec. 2) |
| SG11.5 Growth | Persona validation (Sec. 3) |

## 11. Module-Specific Prompt Library Additions

**Prompt MTG.1 — State Loan Limit Content Generation**

```
For [Client Name]'s [loan program] page targeting [state], generate a
state-specific content outline including current conforming/FHA loan
limits by county (flag for verification against current FHFA/HUD data —
do not assert figures without a current source), state-specific first-
time buyer assistance programs if any, and state licensing statement
placement.
```

## 12. Module Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-07-23 | Extracted from standalone MWEF v1.0 into the fixed Module Template as part of the WEF Core + Modules re-architecture |

---

*Continue to the Real Estate Module.*
