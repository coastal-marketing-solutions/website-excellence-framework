# INDUSTRY MODULE — HOME SERVICES

*Website Excellence Framework (WEF) v1.0 — Module Version 1.0*

---

## 1. Module Overview & Applicability

This Module applies to residential (and light commercial) trade service businesses: HVAC, plumbing, electrical, roofing, remodeling/general contracting, pest control, landscaping, and similar. It assumes a service-area-based, often emergency-and-scheduled-service dual business model.

**Blend commonly with:** SaaS Module (secondary, for a home services company that also licenses its own scheduling/dispatch software to franchisees or other operators).

**Does not fit well:** Large national franchise brands where the site's primary job is franchisee lead-routing rather than direct local conversion — usable as a starting template but expect meaningful adaptation to a multi-location franchise IA pattern.

## 2. Regulatory & Compliance Landscape

Regulatory intensity here is materially lower than the other Modules in this library, but is not zero:

- **State/municipal contractor licensing** — most trades require a license number to be displayed on advertising in many jurisdictions; verify the client's specific state/municipal requirement rather than assuming none applies.
- **FTC advertising rules** — general truth-in-advertising requirements apply to pricing claims, "satisfaction guaranteed" language, and before/after imagery.
- **EPA/environmental regulations** — apply specifically to certain trades (e.g., refrigerant handling in HVAC, lead-safe practices in older-home renovation, pesticide application in pest control) and may require certification display.
- **Warranty/guarantee language** — "lifetime warranty," "guaranteed for X years" claims must accurately reflect the actual warranty terms and are a common source of consumer complaint if imprecise.

**Known claim-risk language patterns:** "same day service guaranteed" without operational ability to back it up, "licensed and insured" claims without current, verifiable license/insurance status, and price-range advertising that doesn't reflect typical actual job costs.

## 3. Persona Library

| Persona | Primary Need | Top Decision Drivers | Top Objections |
|---|---|---|---|
| Emergency/Urgent Need (e.g., no heat, burst pipe) | Fastest possible response | Speed, 24/7 availability, ability to book immediately | Fear of being overcharged in a vulnerable moment, uncertainty about actual response time |
| Planned Project (e.g., remodel, roof replacement) | Research-driven vendor selection over days/weeks | Portfolio quality, reviews, transparent estimating process | Fear of hidden costs, contractor reliability/no-shows, quality of past work |
| Routine/Maintenance Service (e.g., HVAC tune-up, pest control plan) | Recurring, low-friction service relationship | Convenience, consistent scheduling, fair recurring pricing | Being upsold unnecessarily, inconsistent technician quality |
| Insurance-Claim-Driven (e.g., storm damage roof) | Coordinating repair with an insurance claim | Experience working directly with insurers, documentation quality | Confusion navigating the claims process, distrust of storm-chasing contractors |
| Price-Comparison Shopper | Getting multiple quotes before deciding | Fast, easy quote/estimate process, transparent pricing structure | Friction in getting even a rough estimate, feeling pressured by an in-home sales pitch |

## 4. Competitive Landscape Notes

Typical home services sites cluster into: (1) large-spend franchise/national brand sites with strong paid-search infrastructure but generic, templated local pages; (2) local independent operators with strong reputation/reviews but thin site content and weak technical SEO; (3) newer digitally-savvy operators with strong online booking UX but less-established trust signals. Table stakes: service list, service-area coverage, phone number/booking CTA, reviews. Common differentiator gap: instant online booking/estimate tools (most sites still funnel to a phone call for anything beyond a basic contact form) and genuine before/after project portfolios with real project detail rather than generic stock imagery.

## 5. Positioning & Messaging Patterns

Proven angles: "the [trade] company that shows up when we say we will," "the specialist in [niche — high-efficiency systems, historic home renovation, eco-friendly pest control]," "the transparent-pricing alternative to the upsell-heavy competitor." Avoid generic "quality work, fair prices" positioning. Flag for compliance: any specific response-time guarantee ("we'll be there in 60 minutes or it's free") must reflect actual operational capability and be substantiable.

## 6. Information Architecture Patterns

Typical required page types: Home; Service pillar pages (one per major service line — e.g., AC Repair, Furnace Installation, Duct Cleaning under HVAC); Service-area/location pages (one per city/region served, especially important for multi-location or wide-service-area operators); Project Portfolio/Gallery; Reviews/Testimonials page; Financing/Pricing information page; About/Team page with license/insurance/certification display; Booking/Quote request flow.

## 7. SEO & Keyword Strategy

High-value topical clusters: service + location ("AC repair [city]," "emergency plumber [city]"), problem/symptom-driven content ("why is my furnace making noise," "signs you need a roof replacement"), and seasonal/maintenance content. Recommended schema: `HomeAndConstructionBusiness` or the specific trade subtype (`Plumber`, `Electrician`, `RoofingContractor`, `HVACBusiness`), `LocalBusiness` with `areaServed` per location page, `Review`/`AggregateRating` (where genuinely sourced — never fabricated), `FAQPage`, `BreadcrumbList`. This vertical benefits especially strongly from Google Business Profile integration alongside on-site SEO — flag for the client's broader local SEO program, even though GBP itself is outside this framework's website-build scope.

## 8. Trust Signal Requirements

License number and insurance status displayed in the footer and on the About/Team page (per the jurisdiction's actual requirement — verify, don't assume a blanket "licensed and insured" claim is sufficient). Real, verifiable reviews (aggregate rating schema only where genuinely sourced from a review platform, never fabricated). Technician photos/bios where feasible — this materially increases trust for an in-home service. Before/after project photography specific to the client's actual work, not stock imagery. Response-time and availability claims stated accurately and consistent with actual dispatch capability.

## 9. Content Model & Page Types

| Page Type | Required Content Elements |
|---|---|
| Service + Location Page | Service description, service-area confirmation, pricing transparency (range or starting price where feasible), embedded booking/quote tool, reviews specific to that service/area if available |
| Project Portfolio Page | Real before/after photography, project scope description, location, customer quote if available |
| About/Team Page | License/insurance/certification display, technician bios/photos, company history/values |
| Booking/Quote Flow | Minimal-friction request form or instant estimate tool, clear next-step expectation (response time) |

## 10. Stage Gate Injection Map

| Core Stage Gate | What This Module Supplies |
|---|---|
| SG1 Discovery | Persona Library (Sec. 3), Regulatory Landscape seed (Sec. 2) |
| SG2 Competitive Intelligence | Competitive Landscape Notes (Sec. 4) |
| SG3 Strategic Direction | Positioning & Messaging Patterns (Sec. 5) |
| SG4 Information Architecture | IA Patterns (Sec. 6) |
| SG5 SEO Blueprint | SEO & Keyword Strategy (Sec. 7) |
| SG6 UX & Conversion | Trust Signal Requirements (Sec. 8), instant quote/booking tool pattern |
| SG7/7.5 Design | Trust Signal visual treatment (Sec. 8), warmer/approachable visual convention notes |
| SG8/9 Content & Copy | Content Model (Sec. 9), license/warranty claim accuracy review |
| SG11 QA | Full Regulatory Landscape final checklist (Sec. 2), license/insurance display verification |
| SG11.5 Growth | Persona validation (Sec. 3) |

## 11. Module-Specific Prompt Library Additions

**Prompt HS.1 — Service-Area Location Page Generation**

```
For [Client Name]'s [service type] business serving [location], generate
a location page content outline including: locally-relevant service
framing (climate/housing-stock factors relevant to this trade in this
area), service-area boundary clarity, any location-specific licensing
statement, and a booking/quote CTA. Do not fabricate local statistics or
review counts; flag any local data point as needing client verification.
```

## 12. Module Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-07-23 | Initial module authored as part of the WEF Core + Modules re-architecture |

---

*Continue to the Financial Advisor Module.*
