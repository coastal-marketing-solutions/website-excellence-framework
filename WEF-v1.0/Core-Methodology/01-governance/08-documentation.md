# Governance — 8. Documentation Standards

*Core Methodology — Governance, Sec. 8. Part of [`01-governance/`](CONTEXT.md) — the router for this chapter.*

---

## 8. Documentation Standards

### 8.1 Purpose

Consistent documentation is what allows deliverables to move between human consultants and AI models — and between engagements in entirely different industries — without translation loss. All WEF deliverables follow the standards below.

### 8.2 Formatting Standards

- Markdown as the canonical authoring format for all strategy, research, and specification documents.
- Headings follow strict hierarchy (H1 document title, H2 major section, H3 subsection); no skipped levels.
- Tables used for any structured comparison, rubric, or schema — never prose paragraphs describing tabular data.
- Every deliverable begins with a metadata block: Client, Active Industry Module(s), Stage Gate, Author (human or AI model + reviewer), Date, Version, Status.

### 8.3 File Naming Convention

The canonical convention is defined in **Reusable Templates, Sec. 21.4** and is `Title-Case-No-Version.md`, saved inside each Stage Gate folder's `output/` subdirectory — e.g. `04-architecture/output/Sitemap.md`, `05-seo-blueprint/output/Keyword-to-Page-Map.md`. Client-supplied source inputs (a returned intake, a research brief) sit at the stage-folder root rather than in `output/` — e.g. `01-research/01-WEF-Intake.md`.

The earlier `{stage-gate-number}-{deliverable-short-name}-v{version}.md` pattern is **superseded** — all three audited engagements independently converged on the convention above (see Sec. 21.4). As of CR-027, every Required-Document name in the Core Methodology chapters has been reconciled to it; there is no longer a live instruction anywhere to create a literal `-v{N}.md` file.

In-document version tracking (v0.x → v1.0 → …) continues per Sec. 8.4 and Sec. 11 — versions live in the document's metadata block, not the filename.

### 8.4 Versioning Within Documents

Draft versions are tracked as v0.x; the first client- or Engagement-Lead-approved version becomes v1.0; subsequent approved revisions increment the minor or major version per Section 11.

### 8.5 Common Mistakes

- Producing deliverables as unstructured chat transcripts instead of formatted Knowledge Base documents.
- Mixing draft and approved content in the same file without a status marker, causing downstream gates to build on unapproved assumptions.
- Omitting the Active Industry Module field from a deliverable's metadata block, making it ambiguous which module's requirements the document was built against.
