# Governance — 2. Consulting Organization

*Core Methodology — Governance, Sec. 2. Part of [`01-governance/`](CONTEXT.md) — the router for this chapter.*

---

## 2. Consulting Organization

### 2.1 Purpose

Defines the standing roles used across every WEF engagement, their responsibilities, and their decision rights. These roles are identical across industries; only the subject matter they apply expertise to changes. Not every engagement staffs every role as a distinct human — smaller engagements may consolidate roles — but every responsibility below must be explicitly assigned to someone (human or AI-with-human-reviewer) before Stage Gate 1 begins.

### 2.2 Role Definitions

| Role | Primary Responsibility | Typical Stage Gate Ownership |
|---|---|---|
| **Engagement Lead** | Overall accountability for engagement outcomes, client relationship, Decision Register authority, Industry Module selection | All gates (approval) |
| **Project Manager** | Schedule, backlog, risk register, meeting cadence, cross-role coordination | All gates (operations) |
| **Research Consultant** | Market research, discovery synthesis, competitive intelligence | SG1, SG2, SG3 |
| **Strategy Consultant** | Positioning, strategic direction, business objective alignment | SG3, SG6 |
| **Information Architect** | Sitemap, content hierarchy, navigation, taxonomy | SG4 |
| **SEO Specialist** | Keyword architecture, topical maps, technical SEO, schema strategy | SG5, SG8, SG10.5, SG11.5 |
| **UX Designer** | User flows, conversion paths, wireframes | SG6, SG7 |
| **Visual Designer** | Design system, visual identity, GeneratePress/GenerateBlocks design specification | SG7, SG7.5 |
| **Copywriter** | On-page copy, calculator/tool microcopy, disclosures coordination | SG9 |
| **Developer / WordPress Implementer** | GeneratePress/GenerateBlocks build, performance, integrations | SG10, SG10.5 |
| **QA Analyst** | Functional, performance, accessibility, SEO, and compliance QA | SG11 |
| **Compliance/Standards Liaison (client-side)** | Reviews all claims, disclosures, and regulated content per the active Industry Module | SG8, SG9, SG11 (mandatory wherever the Industry Module flags the vertical as regulated) |
| **AI Orchestrator (human)** | Manages LLM Handoff Protocol, prompt quality, output verification, Module context injection | All gates |
| **Knowledge Librarian** *(optional, recommended at engagement scale — added from cross-engagement evidence)* | Files and cross-references every accepted deliverable into the Knowledge Base; audits for duplicate or contradictory entries; **performs no content judgment whatsoever** — cannot resolve a genuine contradiction, only surface it to the Engagement Lead | All gates (filing/audit only, not decision-making) |
| **Design Fidelity Reviewer** *(added from cross-engagement evidence, Sec. 15.4 RETRO-021)* | Recurring, independent verification — at defined checkpoints across Development and Post-Launch, not only once at SG7.5/SG10.5 handoff — that in-progress and live build output still matches the SG7.5-approved Design Constraints Package and Design Tokens (Design, Appendix). Runs the Design Export Validation Gate's Three-Part Validation (Design, Appendix) at each checkpoint, not only at initial export. **Holds direct remediation authority**: when a checkpoint finds build output has drifted from an already-approved spec — a wrong token, a missing or structurally-deviant component, styling that doesn't match the Do-Not-Break List — the Design Fidelity Reviewer corrects the live build/code directly against the Design Constraints Package, rather than only filing a finding for a future, unowned session to maybe act on; this closes the exact loop RETRO-021 found open, where a flagged-but-unremediated gap was indistinguishable from one nobody had checked at all. Remediation is bounded to *restoring already-approved spec*; any case where the spec itself is ambiguous or silent is escalated to the Visual Designer as a design decision, never resolved unilaterally. Distinct from the Visual Designer (who makes net-new design decisions) — the Design Fidelity Reviewer implements no design it didn't already find pre-approved elsewhere. Its code-level remediation work necessarily overlaps the Developer's construction work on the same component; see Sec. 2.4 for how that's kept from collapsing into self-certification | SG7.5 (baseline capture), SG10.5 (recurring — detect and remediate), SG11, SG11.5 |

**On the Knowledge Librarian role:** this separates *deciding what's accepted* (Engagement Lead/Project Manager, a judgment call) from *filing and auditing it correctly* (Knowledge Librarian, zero judgment authority) — two independent real-world sources converged on this same separation-of-duties pattern without coordinating: a live WEF engagement's own governance system, and an external AI-driven marketing agency's independently designed team roster. On engagements below a size threshold set in the Project Charter, this role may be folded into the Project Manager's Section 2.2 duties, but the *function* (duplicate/contradiction audits, catching e.g. the same Open Question filed twice under different IDs) should not be skipped just because it isn't staffed as a separate person.

### 2.3 RACI Summary (Engagement-Level)

| Activity | Engagement Lead | Project Manager | Specialists | Client |
|---|---|---|---|---|
| Project Charter approval (incl. Module selection) | A | R | C | A |
| Stage Gate exit sign-off | A | R | R | I (or A for SG3, SG7.5, SG11) |
| Decision Register entries | A | R | R | I |
| Compliance/standards sign-off (where applicable) | I | I | C | A |
| Go-live authorization | A | R | C | A |
| Design fidelity spot-check & remediation (recurring, SG10.5 onward) | I | I | R (Design Fidelity Reviewer), A (Engagement Lead) | I |

*(R = Responsible, A = Accountable, C = Consulted, I = Informed)*

### 2.4 Best Practices

- Never let the Visual Designer also serve as final QA Analyst on the same engagement — independent review of design fidelity requires separation of duties. The same separation applies to the Design Fidelity Reviewer's *detection* function: whoever originally built a component should not be the sole one certifying it's still on-spec.
- The Design Fidelity Reviewer's *remediation* function is deliberately different: it is expected to fix drift directly against the already-approved Design Constraints Package, which means writing to the same code the Developer wrote. This is not a separation-of-duties violation, because the reviewer only restores a spec someone else already approved — it never makes a new design decision or signs off on its own new design work. A remediation that requires a judgment call the spec doesn't already answer is escalated to the Visual Designer, not resolved as if it were mechanical.
- The Design Fidelity Reviewer's recurring SG10.5+ checks (Sec. 2.2) are not satisfied by the one-time SG10.5 Global Styles spot-check (Development, Sec. 06, Checklist) — see Sec. 15.4, RETRO-021. On engagements light enough to consolidate this role into another (commonly the QA Analyst; never the Visual Designer, and the Developer only if a second, independent detection pass is preserved), the recurring cadence must still be explicitly scheduled, not left to happen opportunistically.
- The Compliance/Standards Liaison must be client-side, not a firm consultant role-playing compliance; WEF firms do not issue legal, medical, financial, or other professional opinions.
- On engagements under a certain size (defined in the Project Charter), the AI Orchestrator role may be held by the Engagement Lead directly, but must still be explicitly named.
