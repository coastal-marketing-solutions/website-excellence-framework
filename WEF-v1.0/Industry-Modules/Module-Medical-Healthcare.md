# INDUSTRY MODULE — MEDICAL / HEALTHCARE

*Website Excellence Framework (WEF) v1.0 — Module Version 1.0*

---

## 1. Module Overview & Applicability

This Module applies to private medical practices, specialty clinics, dental practices, and small-to-mid-size healthcare groups marketing directly to patients. It assumes a patient-acquisition and patient-education marketing model, not a hospital-system enterprise site with employee/investor-relations complexity.

**Blend commonly with:** Generally standalone; a med-spa or elective-cosmetic practice may warrant lighter compliance treatment than a clinical specialty practice — note this explicitly in the Project Charter rather than assuming uniform regulatory intensity across all "medical" clients.

**Does not fit well:** Hospital systems, health insurance marketplaces, or pharmaceutical marketing (each has materially different regulatory regimes — FDA promotional rules for pharma, for instance — that this Module does not cover).

## 2. Regulatory & Compliance Landscape

- **HIPAA (Health Insurance Portability and Accountability Act)** — governs protected health information (PHI); any contact form, patient portal link, or chat widget must avoid collecting PHI in a non-secure channel, and privacy policy language must address HIPAA specifically, not just generic data privacy.
- **State medical/dental board advertising rules** — govern claims about outcomes, board certification display, and use of "specialist" terminology.
- **FTC health claim substantiation rules** — outcome and efficacy claims (especially for elective/cosmetic procedures) require a reasonable basis and cannot be deceptive; before/after imagery is commonly regulated (typical patient results disclaimers, no cherry-picked outlier results without disclosure).
- **Board certification display rules** — practitioners must accurately represent board certification status per the specific certifying body; "board certified" claims are a common compliance flag if imprecise.
- **Informed consent and treatment-risk disclosure norms** — while not always a website-content legal requirement per se, procedure pages describing risks/benefits should avoid language that could be read as circumventing the in-person informed consent process.

**Known claim-risk language patterns:** guaranteed outcome claims ("guaranteed pain-free," "permanent results" without qualification), before/after imagery without disclosure of typicality, and "board certified" claims that don't specify the certifying board accurately.

## 3. Persona Library

| Persona | Primary Need | Top Decision Drivers | Top Objections |
|---|---|---|---|
| New Patient, Symptom-Driven | Timely appointment for a specific health concern | Perceived expertise, ease of scheduling, insurance acceptance | Long wait times, unclear insurance coverage, anxiety about the visit itself |
| Chronic Condition Patient | Ongoing management relationship | Continuity of care, practitioner's specific experience with their condition | Fear of being "just a number," past bad experiences with dismissive providers |
| Elective/Cosmetic Procedure Patient | Aesthetic or elective treatment decision | Before/after evidence, practitioner's specific technique/experience, cost transparency | Fear of poor results, cost surprise, embarrassment about the inquiry |
| Referred Patient | Following a referral from another provider | Confirmation the practice takes their insurance/referral, smooth handoff | Confusion about next steps, redundant intake paperwork |
| Caregiver/Family Member | Researching care on behalf of a parent or dependent | Practice's experience with the specific population (geriatric, pediatric), communication with family | Difficulty finding practices that clearly serve this population well |

## 4. Competitive Landscape Notes

Typical medical practice sites cluster into: (1) larger specialty groups with strong technical polish but generic, corporate-feeling content; (2) solo/small practices with strong practitioner personal brand but thin condition-specific educational content and weak online scheduling integration; (3) elective/cosmetic practices with heavy before/after galleries but inconsistent disclosure practices. Table stakes: practitioner bios with credentials, insurance-accepted list, online scheduling or contact. Common differentiator gap: genuine condition-specific educational content (most practices under-invest in patient education content relative to how much it drives both SEO and pre-visit trust) and clear, honest cost/insurance transparency.

## 5. Positioning & Messaging Patterns

Proven angles: "the practice that takes the time most providers don't," "the specialist in [specific condition/population] with [specific credential/experience]," "the practice that makes [elective procedure] transparent from consultation to recovery." Avoid generic "compassionate, quality care" positioning. Flag for compliance: any positioning built on outcome superiority ("best results in [city]") requires a substantiable basis and is generally high-risk without it.

## 6. Information Architecture Patterns

Typical required page types: Home; Condition/Service pillar pages (one per major condition treated or procedure offered); Practitioner profile pages (with credentials/board certification); Patient resources (FAQ, what-to-expect, pre/post-procedure instructions); Insurance/Billing information page; New Patient intake information page; required compliance pages (HIPAA-compliant Privacy Policy, Notice of Privacy Practices, Accessibility Statement, informed-consent-adjacent disclaimers on procedure pages).

## 7. SEO & Keyword Strategy

High-value topical clusters: condition/symptom-driven informational content ("[symptom] causes and treatment," "[condition] specialist near me"), procedure-specific content with cost/process transparency, and practitioner/credential-driven local-authority content. Recommended schema: `MedicalOrganization` or `MedicalClinic` (homepage), `Physician` or `MedicalBusiness` (practitioner profiles, include board certification as a credential property), `MedicalWebPage` for condition content (signals E-E-A-T-relevant medical review), `FAQPage`, `BreadcrumbList`. Claim-risk keyword patterns: avoid "guaranteed" outcome terms; prefer condition-education and process-transparency terms.

## 8. Trust Signal Requirements

Practitioner credentials and board certification displayed accurately (name the specific certifying board) on every practitioner profile. Content review/authorship attribution on medical information pages (who wrote/reviewed it, and their credentials) — a significant trust and SEO signal (aligned with Google's E-E-A-T guidance for medical content). Before/after imagery (where used) accompanied by a "individual results may vary" disclosure and, where required, the typicality of the shown result. HIPAA-compliant intake/contact mechanism clearly indicated (not a generic contact form implying PHI can be submitted insecurely).

## 9. Content Model & Page Types

| Page Type | Required Content Elements |
|---|---|
| Condition/Service Page | Plain-language condition explanation, treatment options overview, practitioner-authored or reviewed byline, FAQ block, appointment CTA |
| Practitioner Profile | Photo, credentials, board certification (specific board named), bio, conditions/procedures treated, contact/scheduling |
| Procedure Page (elective) | Process overview, cost transparency where possible, before/after gallery with disclosure, risk/benefit overview (general, not a substitute for informed consent), consultation CTA |
| New Patient / Insurance Page | Accepted insurance list, intake process, HIPAA-compliant contact method |

## 10. Stage Gate Injection Map

| Core Stage Gate | What This Module Supplies |
|---|---|
| SG1 Discovery | Persona Library (Sec. 3), Regulatory Landscape seed (Sec. 2) |
| SG2 Competitive Intelligence | Competitive Landscape Notes (Sec. 4) |
| SG3 Strategic Direction | Positioning & Messaging Patterns (Sec. 5) |
| SG4 Information Architecture | IA Patterns (Sec. 6) |
| SG5 SEO Blueprint | SEO & Keyword Strategy (Sec. 7), E-E-A-T authorship signal requirements |
| SG6 UX & Conversion | Trust Signal Requirements (Sec. 8), HIPAA-safe intake flow design |
| SG7/7.5 Design | Trust Signal visual treatment (Sec. 8), before/after gallery disclosure treatment |
| SG8/9 Content & Copy | Content Model (Sec. 9), full Regulatory Landscape (Sec. 2), practitioner-review byline sourcing |
| SG11 QA | Full Regulatory Landscape final checklist (Sec. 2), HIPAA-safe form check |
| SG11.5 Growth | Persona validation (Sec. 3) |

## 11. Module-Specific Prompt Library Additions

**Prompt MED.1 — HIPAA-Safe Intake Flow Review**

```
Review the attached conversion flow / contact form design for [Client
Name]'s medical practice website. Identify any point where a visitor
could be prompted to submit protected health information (symptom
details, diagnosis, treatment history) through a non-secure or non-HIPAA-
compliant channel (a standard contact form, an unencrypted chat widget).
Recommend where a HIPAA-compliant intake method or secure patient portal
link should replace a generic form field, and flag the finding for
Compliance/Standards Liaison confirmation rather than asserting a fix as
final.
```

## 12. Module Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-07-23 | Initial module authored as part of the WEF Core + Modules re-architecture |

---

*Continue to the Home Services Module.*
