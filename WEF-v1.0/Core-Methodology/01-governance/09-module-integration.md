# Governance — 9. Module Integration Standard

*Core Methodology — Governance, Sec. 9. Part of [`01-governance/`](CONTEXT.md) — the router for this chapter.*

---

## 9. Module Integration Standard

### 9.1 Purpose

This section is the mechanism that makes the Core + Modules architecture actually function. It defines, precisely, how an Industry Module's content enters a Core Stage Gate, and the discipline required to keep the boundary between "universal methodology" and "vertical-specific knowledge" clean over time.

### 9.2 The Module Injection Point Convention

Every Stage Gate chapter in the Core Methodology (Research, SEO & Architecture, UX & Conversion, Design, Development, QA & Optimization) contains one or more explicit **Module Injection Point** callouts, in this form:

> **Module Injection Point:** This gate consumes [specific Industry Module section] in place of generic guidance. Load the active Industry Module's [Section Name] before running this gate's workflow.

A Stage Gate is never executed by substituting improvised, ad hoc industry knowledge for a real Module Injection Point. If the active Industry Module does not yet cover something a Stage Gate needs, that gap is logged as a backlog item against the Module (Section 9.5), not silently patched inside the client engagement with no trace.

### 9.3 Standard Module Injection Map

| Core Stage Gate | Module Section(s) Injected |
|---|---|
| SG1 — Discovery & Market Research | Persona Library, Regulatory & Compliance Landscape (seed) |
| SG2 — Competitive Intelligence | Competitive Landscape Notes (typical competitor archetypes for the vertical) |
| SG3 — Strategic Direction | Positioning & Messaging Patterns |
| SG4 — Information Architecture | Information Architecture Patterns (typical sitemap/page types) |
| SG5 — SEO Blueprint | SEO & Keyword Strategy, Schema recommendations |
| SG6 — UX & Conversion | Trust Signal Requirements, industry-typical calculators/tools |
| SG7 / SG7.5 — Design | Trust Signal Requirements (visual treatment), industry visual conventions |
| SG8 / SG9 — Content Spec & Copywriting | Content Model & Page Types, Regulatory & Compliance Landscape (full) |
| SG10 / SG10.5 — Build | Any module-specific integration notes (e.g., practice-management or CRM system patterns) |
| SG11 — QA | Regulatory & Compliance Landscape (final QA checklist) |
| SG11.5 — Post-Launch Growth | Persona Library (validation against real data), Content Model (expansion) |

### 9.4 Handling Blended-Module Engagements

Where two modules are active (Section 1.5), apply both modules' relevant sections at each injection point, using the primary/secondary boundary defined in the Project Charter to determine which module governs which pages/sections. Where the two modules' compliance requirements conflict, the stricter requirement governs by default, with the conflict logged as a Decision Register entry and escalated to both Compliance/Standards Liaisons.

### 9.5 Module Gap Escalation

If a Stage Gate's Module Injection Point cannot be filled because the active Industry Module lacks the needed content, the AI Orchestrator or Engagement Lead logs a Module Gap (using the Issue Log structure in Reusable Templates) against the Module itself, not just the client engagement. Once resolved for the current client, the resolution is proposed back into the Industry Module via Change Request (Section 13.2) so the next engagement in that vertical benefits — this is the mechanism by which the Module library compounds in value over time.

### 9.6 Common Mistakes

- Treating Module Injection Points as optional reading rather than a required input — this is how mortgage-specific assumptions quietly leak into a law firm engagement, or vice versa.
- Resolving a Module Gap for one client and never feeding the learning back into the Module itself, forcing the same gap to be rediscovered on the next engagement in that vertical.
- Blending modules informally without documenting the primary/secondary boundary, leaving later team members unable to determine which rules applied to which pages.
