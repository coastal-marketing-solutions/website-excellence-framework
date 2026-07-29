# COMPONENT LIBRARY — MARKETING & TRUST

*Website Excellence Framework (WEF) v1.0 — see `00-Component-Library-Index.md` for schema and governance*

---

## CL-MKTG-001 — TrustBar

**Purpose / When to Use:** A compact compliance/credential strip that appears on every page (typically just below the header or above the footer) — licensing numbers, professional credential marks, required equal-opportunity or accessibility marks, and a link to the relevant public license-verification registry.

**When NOT to Use:** Never build a page-specific variant with different or missing facts than the site-wide version — this component must render identically (content-wise) everywhere it appears, which is exactly why it belongs in a single reusable pattern rather than page-by-page markup (Governance, Sec. 15.4, RETRO-004).

**Interface:**
```
<TrustBar licenseNumbers={[...]} verificationLink="..." marks={[...]} />
```

**Design Token Dependencies:** Neutral/brand color tokens; **type-scale floor** — this component's text must never render below the minimum legal-text size the active Industry Module's Regulatory & Compliance Landscape specifies (14px in the originating engagement — confirm per Module and per jurisdiction, as this is not a universal constant).

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Build as a single Global (site-wide, not per-page) pattern or Element hook (GeneratePress Premium's Elements module, or the equivalent global-include mechanism on an alternative stack) so a single source updates every page at once — this is the direct fix for the exact defect-propagation failure mode documented in Governance RETRO-004.

**Compliance Sensitivity:** **Very high — a standing Do-Not-Break List candidate in every engagement that uses it.** Every fact, number, and required mark in this component is regulatory content; restyle visually as needed, but content changes require Compliance/Standards Liaison sign-off, not just a Developer or AI coding agent's judgment call.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — NMLS number, state broker/lender license number, Equal Housing Opportunity mark, and NMLS Consumer Access verification link, present on every page.

**Industry Module Fit:** Essential for any Module with a licensing or credentialing regime (mortgage lending, law firm, medical/healthcare, financial advisor, real estate) — the specific facts/marks it carries are Module-specific even though the component structure is universal.

**Status:** Active. **Version:** v1.0.

---

## CL-MKTG-002 — ComplianceFooter

**Purpose / When to Use:** The site-wide footer carrying the full regulatory disclosure block — legal entity name and license statement, business address, phone, all applicable license/registration numbers, any required "record of" or "not a commitment to" disclaimer language, and links to legally required pages (privacy policy, terms, accessibility statement, licensing disclosures).

**When NOT to Use:** Never let individual pages carry an independently-edited copy of this footer's content — same reusable-pattern discipline as TrustBar (CL-MKTG-001), for the same reason.

**Interface:**
```
<ComplianceFooter entityName="..." licenseNumbers={[...]} address="..." phone="..." disclaimer="..." legalLinks={[...]} />
```

**Design Token Dependencies:** Inverse/dark-background color tokens (this component is frequently styled as a dark/brand-color footer section), **type-scale floor** (same legal-text minimum as TrustBar).

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Same Global pattern / Element hook discipline as TrustBar — single source of truth, never hand-duplicated per page.

**Compliance Sensitivity:** **Very high — standing Do-Not-Break List item.** This is the single highest-consequence component in the entire library if it drifts: it typically carries the legal entity's core regulatory identity statement.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — full company/license statement, address, phone, NMLS/state license numbers, broker-of-record designation, NMLS Consumer Access link, and links to Privacy Policy, Terms of Use, Accessibility Statement, and Licensing Disclosures.

**Industry Module Fit:** Essential for any regulated Module; the specific required fields vary by Module and must be pulled from that Module's Regulatory & Compliance Landscape, not assumed to match the mortgage-lending example.

**Status:** Active. **Version:** v1.0.

---

## CL-MKTG-003 — LeadCaptureForm

**Purpose / When to Use:** The primary conversion form — used on the homepage and on offering-specific pages — composed from Input (CL-FORM-001), Select (CL-FORM-002), Checkbox (CL-FORM-003), and the primary Button (CL-CORE-001).

**When NOT to Use:** Don't build a bespoke form structure per page when the same field set and submission behavior apply — compose from this pattern and vary only the fields that genuinely differ (e.g., which offering/program options appear in the Select).

**Interface:**
```
<LeadCaptureForm fields={[...]} onSubmit={handler} />
```

**Design Token Dependencies:** Inherits from its constituent Forms components (CL-FORM-001 through 005) and the primary Button (CL-CORE-001) — no independent tokens of its own.

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Server-side form handling and notification routing (where does a submission go, who gets notified) is engagement-specific configuration, not part of the reusable component itself — document the notify-recipient and any CRM/integration hookup in that engagement's own Development discipline outputs (SG10.5), not in this registry entry.

**Compliance Sensitivity:** High where the consent checkbox is present — see CL-FORM-003. The data fields collected and how submissions are stored/transmitted must be checked against the active Industry Module's Regulatory & Compliance Landscape.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — the "Get Pre-Qualified" form on the homepage and loan-program pages.

**Industry Module Fit:** Universal — every Module's site needs a primary lead-capture mechanism; field composition varies by Module.

**Status:** Active. **Version:** v1.0.
