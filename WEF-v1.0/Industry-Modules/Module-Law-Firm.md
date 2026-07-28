# INDUSTRY MODULE — LAW FIRM

*Website Excellence Framework (WEF) v1.0 — Module Version 1.0*

---

## 1. Module Overview & Applicability

This Module applies to law firms and solo practitioners across practice areas — personal injury, family law, estate planning, criminal defense, business law, immigration, and similar — with the understanding that practice-area-specific content depth (Section 9) will vary more than the structural pattern does.

**Blend commonly with:** Financial Advisor Module (secondary, for estate-planning firms offering fee-based planning services).

**Does not fit well:** Large multi-office national law firms with primarily B2B/corporate clients and no consumer-facing lead generation model — the conversion mechanics here assume a consumer or small-business prospective client evaluating and contacting a firm directly.

## 2. Regulatory & Compliance Landscape

- **State bar advertising rules** — vary significantly by state; nearly all states require some disclaimer language on case results, prohibit guarantees of outcome, and regulate the use of terms like "specialist" or "expert."
- **Rules of Professional Conduct (state-specific, generally modeled on ABA Model Rules)** — govern attorney advertising, solicitation, and client testimonials (many states restrict or require disclaimers on testimonials referencing case outcomes).
- **Case result and testimonial disclaimers** — most states require "past results do not guarantee future outcomes" or similar language adjacent to any case result or testimonial content.
- **Attorney-client privilege and confidentiality considerations** — content and intake forms must avoid soliciting privileged/confidential details before an attorney-client relationship is established; intake forms typically require a "no attorney-client relationship until engagement letter signed" disclaimer.
- **Jurisdictional licensing** — attorneys are licensed per state/jurisdiction; multi-state firms must clearly indicate which attorneys are licensed where.

**Known claim-risk language patterns:** outcome guarantees ("we will win your case," "guaranteed settlement"), unqualified superlatives ("best lawyer," "top firm") without a verifiable, permitted award/ranking basis, and case result figures presented without required disclaimer language.

## 3. Persona Library

| Persona | Primary Need | Top Decision Drivers | Top Objections |
|---|---|---|---|
| Post-Accident Client (Personal Injury) | Representation after an injury, often insurance-adversarial | Perceived aggressiveness/advocacy, no-fee-unless-we-win structure clarity, responsiveness | Fear of cost, distrust of "ambulance chaser" stereotype, uncertainty about case value |
| Divorcing Spouse (Family Law) | Guidance through a high-emotion, high-stakes legal process | Empathy combined with competence, clarity on process and cost, discretion | Fear of an adversarial process escalating, cost uncertainty, emotional vulnerability |
| Estate Planning Client | Will/trust/estate structure guidance | Trust, thoroughness, plain-language explanation of complex options | Procrastination-inducing complexity, discomfort discussing mortality/family conflict |
| Criminal Defense Client/Family | Urgent representation, often for a family member | Speed of response, experience with the specific charge type, clear fee structure | Fear, urgency, distrust of the legal system, cost concern |
| Small Business Owner (Business Law) | Contract, entity formation, or dispute guidance | Responsiveness, business-context understanding (not just legal theory), predictable billing | Cost unpredictability, past bad experience with unresponsive counsel |

## 4. Competitive Landscape Notes

Typical law firm sites cluster into: (1) large-spend PI/mass-tort firms with aggressive paid-search-driven design and heavy trust-signal saturation (awards, verdicts, testimonials) but often generic, templated practice-area content; (2) small/solo practice sites with strong personal credibility signals but thin content depth and dated design; (3) boutique firms with strong brand but weak local/practice-area SEO. Table stakes: practice area pages, attorney bios with jurisdiction, contact form, some case result/testimonial content with disclaimers. Common differentiator gap: genuine plain-language educational content addressing specific client fears (what happens at each stage of a case) and case-value or process-estimator tools.

## 5. Positioning & Messaging Patterns

Proven angles: "the firm that explains every step so you're never in the dark," "the specialist in [specific injury type/practice niche] with a documented track record," "the firm that treats a [divorce/estate plan/business matter] as a relationship, not a transaction." Avoid generic "aggressive advocates" positioning without specific proof points. Flag for compliance: any case result, verdict, or settlement figure requires the jurisdiction's required disclaimer language adjacent to it, and any "specialist"/"expert" designation must match what the state bar actually permits (board certification, if applicable).

## 6. Information Architecture Patterns

Typical required page types: Home; Practice Area pillar pages (one per practice area); Sub-practice-area cluster pages (e.g., under Personal Injury: Car Accidents, Truck Accidents, Slip and Fall); Attorney profile pages (with jurisdiction/bar admission); Case Results/Testimonials page (with disclaimer); Persona/situation hub pages (e.g., "What to do after a car accident"); Resource/guide library; required compliance pages (Attorney Advertising disclaimer, Privacy Policy, Accessibility Statement, jurisdiction-specific bar-required disclosures).

## 7. SEO & Keyword Strategy

High-value topical clusters: practice-area + location ("car accident lawyer [city]"), situational/informational content ("what to do after a car accident," "how long does a divorce take in [state]"), and case-value/process education. Recommended schema: `Attorney` or `LegalService` (homepage/practice area pages), `LocalBusiness` (office locations), `Person` (attorney profiles, include bar admission jurisdiction), `FAQPage`, `BreadcrumbList`. Claim-risk keyword patterns: avoid "guaranteed settlement" or "win your case" style targets; prefer process/education and local-authority terms.

## 8. Trust Signal Requirements

Bar admission/jurisdiction licensing displayed on every attorney profile. Case results and testimonials must carry the jurisdiction-required disclaimer adjacent to the claim, not buried in a separate legal page. Awards/rankings (Super Lawyers, AV Preeminent, etc.) displayed with accurate sourcing. "No fee unless we win" or fee-structure clarity where applicable to the practice area (common in PI). Professional, restrained visual treatment tends to outperform aggressive/loud design in most practice areas outside high-volume PI marketing.

## 9. Content Model & Page Types

| Page Type | Required Content Elements |
|---|---|
| Practice Area Page | Plain-language explanation of the legal issue, process overview, relevant case results (with disclaimer), attorney CTA, FAQ block |
| Attorney Profile | Photo, jurisdiction/bar admission, bio, practice areas, notable results (with disclaimer), contact |
| Case Results/Testimonials Page | Required jurisdiction disclaimer prominently adjacent to every result, verifiable sourcing |
| Situational Guide Page | Step-by-step "what happens next" content addressing the persona's specific fear/urgency |

## 10. Stage Gate Injection Map

| Core Stage Gate | What This Module Supplies |
|---|---|
| SG1 Discovery | Persona Library (Sec. 3), Regulatory Landscape seed (Sec. 2) |
| SG2 Competitive Intelligence | Competitive Landscape Notes (Sec. 4) |
| SG3 Strategic Direction | Positioning & Messaging Patterns (Sec. 5) |
| SG4 Information Architecture | IA Patterns (Sec. 6) |
| SG5 SEO Blueprint | SEO & Keyword Strategy (Sec. 7) |
| SG6 UX & Conversion | Trust Signal Requirements (Sec. 8), case-value estimator tool pattern |
| SG7/7.5 Design | Trust Signal visual treatment (Sec. 8), restrained/professional visual convention notes |
| SG8/9 Content & Copy | Content Model (Sec. 9), full Regulatory Landscape (Sec. 2), disclaimer placement |
| SG11 QA | Full Regulatory Landscape final checklist (Sec. 2), disclaimer adjacency check |
| SG11.5 Growth | Persona validation (Sec. 3) |

## 11. Module-Specific Prompt Library Additions

**Prompt LAW.1 — Case Result Disclaimer Placement Check**

```
Review the attached page copy for [Client Name]'s law firm website for
any case result, verdict, settlement figure, or outcome-implying
testimonial. For each instance found, confirm whether the required
jurisdiction disclaimer ("past results do not guarantee future outcomes"
or the [state] bar's specific required language) appears immediately
adjacent to it. Flag any instance missing adjacent disclaimer language
for Compliance/Standards Liaison review — do not draft the final
disclaimer text yourself; confirm the exact required wording with the
Liaison.
```

## 12. Module Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-07-23 | Initial module authored as part of the WEF Core + Modules re-architecture |

---

*Continue to the Medical / Healthcare Module.*
