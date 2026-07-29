# COMPONENT LIBRARY — FORMS

*Website Excellence Framework (WEF) v1.0 — see `00-Component-Library-Index.md` for schema and governance*

---

## CL-FORM-001 — Input

**Purpose / When to Use:** Labeled text field for any lead-capture, contact, or application form.

**When NOT to Use:** Don't use for single-choice selection among fixed options — use Select (CL-FORM-002) or Radio (CL-FORM-004) instead.

**Interface:**
```
<Input label="Field label" type="text|email|tel|..." placeholder="..." required error="message" />
```

**Design Token Dependencies:** Body type-scale token (never the small/disclaimer type-scale token — form fields should always be at or above base body size for usability), border/focus-ring color tokens, error-state color token.

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Must show a visible, sufficiently thick keyboard-focus ring (WCAG 2.1 AA — this is a common accessibility failure point for custom-styled inputs) and an inline error message pattern, not a color-only error indicator (color alone fails WCAG for users with color-vision deficiency).

**Compliance Sensitivity:** Low for the field itself; high for what data it's allowed to collect and how it's transmitted/stored — confirm against the active Industry Module's Regulatory & Compliance Landscape (e.g., TCPA consent-related fields, HIPAA-adjacent health information, financial account numbers) before adding a new field type.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — used across the Contact and Get Pre-Qualified/lead-capture forms.

**Industry Module Fit:** Universal.

**Status:** Active. **Version:** v1.0.

---

## CL-FORM-002 — Select

**Purpose / When to Use:** Dropdown for choosing among a defined, moderate-length list of options (e.g., a product/program type, a state).

**When NOT to Use:** For 2–4 mutually exclusive options where all can be shown at once, prefer Radio (CL-FORM-004) — it reduces interaction cost. For very long option lists, consider a searchable/typeahead pattern instead (not yet in this registry — a candidate for future promotion if built).

**Interface:**
```
<Select label="Field label" options={[...]} />
```

**Design Token Dependencies:** Same as Input (CL-FORM-001).

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Native `<select>` semantics preferred over a custom-styled dropdown component unless the design system specifically requires custom option rendering — native selects carry accessibility and mobile-usability behavior for free.

**Compliance Sensitivity:** Low for the field; the option list itself may need Compliance/Standards Liaison review if it represents regulated product categories (e.g., loan program types).

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — used for loan-program selection in the lead-capture form.

**Industry Module Fit:** Universal.

**Status:** Active. **Version:** v1.0.

---

## CL-FORM-003 — Checkbox

**Purpose / When to Use:** Consent/agreement toggle — most commonly a required legal consent checkbox on a lead-capture or contact form (e.g., "I agree to be contacted").

**When NOT to Use:** Don't use for a binary settings preference with immediate effect — that's Switch (CL-FORM-005).

**Interface:**
```
<Checkbox label="Consent text" checked={bool} onChange={handler} />
```

**Design Token Dependencies:** Same as Input; checked-state color token.

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Where used for a legal consent capture (TCPA or equivalent), the exact consent language is Compliance/Standards Liaison-owned content (Development, SG8/SG9), not something the component itself should hardcode — the component provides the interaction pattern, the copy is supplied per engagement.

**Compliance Sensitivity:** **High when used for consent capture** — treat the consent copy as a Do-Not-Break List candidate in any engagement's Design Constraints Package once approved by Compliance/Standards Liaison.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — "I agree to be contacted by phone or email" consent capture on the lead-capture form.

**Industry Module Fit:** Universal — especially high-value for any Module with TCPA or equivalent contact-consent exposure (mortgage lending, real estate, financial advisory, medical/healthcare, home services).

**Status:** Active. **Version:** v1.0.

---

## CL-FORM-004 — Radio

**Purpose / When to Use:** Single-choice field among a small set of mutually exclusive, simultaneously visible options (e.g., "Purchase" vs. "Refinance").

**When NOT to Use:** For longer option lists, use Select (CL-FORM-002) instead.

**Interface:**
```
<Radio name="group" value="option" label="Label" checked={bool} onChange={handler} />
```

**Design Token Dependencies:** Same as Input; selected-state color token.

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Group radio inputs under a shared `name` attribute per native HTML form semantics — do not simulate radio-group behavior with JS-only state management where native form submission is expected to work.

**Compliance Sensitivity:** Low.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — Purchase vs. Refinance selector.

**Industry Module Fit:** Universal.

**Status:** Active. **Version:** v1.0.

---

## CL-FORM-005 — Switch

**Purpose / When to Use:** Binary settings toggle with immediate effect (e.g., an email-updates opt-in on an account or preferences view).

**When NOT to Use:** Don't use for a form-submission consent checkbox — that's Checkbox (CL-FORM-003); Switch implies an immediately-applied state change, Checkbox implies a value submitted with a form.

**Interface:**
```
<Switch on={bool} onToggle={handler} label="Label" />
```

**Design Token Dependencies:** Same as Input; on/off-state color tokens.

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Requires interactive JS for the toggle state and, typically, a backing API/settings-persistence endpoint — heavier than the other Forms components; confirm the engagement actually needs live-toggle behavior (an account/portal feature) rather than a simple form field before selecting this over Checkbox.

**Compliance Sensitivity:** Low for the control itself; high for whatever setting it controls if that setting affects consent or communication preferences (same TCPA/consent considerations as Checkbox).

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — scaffolded for a future account/preferences view (email-updates opt-in); not deployed to a live page in that engagement.

**Industry Module Fit:** Most relevant for Modules with a client-portal or account-management surface (mortgage lending servicing portals, SaaS account settings, financial advisor client portals).

**Status:** Experimental — built but not yet confirmed in a live, in-production implementation. **Version:** v0.1.
