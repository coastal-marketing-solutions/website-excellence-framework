# Change Request — CR-029 *(WORKING DRAFT — NOT ADOPTED)*

**Submitted By:** `icm-architect` review pass ([`WEF-ICM-Architecture-Review-2026-09-07.md`](WEF-ICM-Architecture-Review-2026-09-07.md), finding **F-8**)
**Date:** 2026-09-07
**Scope:** `WEF-v1.0/Core-Methodology/01-Governance.md` → a `01-governance/` sub-folder; every cross-reference to `Governance, Sec. X` across the manual
**Governance Board Decision:** _Pending — this one genuinely needs Board discussion, not just sign-off_

## Problem

`01-Governance.md` is one 883-line file (~40k tokens) doing ~15 distinct jobs: initialization, roles, charter, decision register, KB structure, blueprint, backlog, doc standards, module integration, project memory, version control, firm QA, 13 governance policies, risk, retrospectives. ICM invariants 1 and 7: one folder / one job, and load only what the step needs (~2k–8k tokens). A task needing only the Decision Register schema currently loads the entire chapter. RETRO-013/014 are partly *"a rule buried in this file was never re-read."*

## Proposed change (for discussion — not a final design)

Split into `WEF-v1.0/Core-Methodology/01-governance/` with its own `CONTEXT.md` router (the L1 pattern applied recursively, per `icm-architect` `references/core.md`):

```
01-governance/
  CONTEXT.md              # router: which file for which question
  01-initialization.md    # Sec. 1
  02-organization.md      # Sec. 2 (roles, RACI)
  03-charter.md           # Sec. 3
  04-decision-register.md # Sec. 4
  05-knowledge-base.md    # Sec. 5 (incl. 5.2.1 nav layer)
  06-blueprint.md         # Sec. 6
  07-backlog.md           # Sec. 7
  08-documentation.md     # Sec. 8
  09-module-integration.md# Sec. 9
  10-project-memory.md    # Sec. 10
  11-version-control.md   # Sec. 11
  12-firm-qa.md           # Sec. 12
  13-policies.md          # Sec. 13 (tech stack, compliance governance, new-module process)
  14-risk.md              # Sec. 14
  15-retrospectives.md    # Sec. 15 (Retrospective Register, Cross-Engagement Pipeline)
```

Section numbers stay stable inside each file, so existing `Governance, Sec. 13.5` references still make sense — but every such reference across all 10 Core chapters, 13 Industry Modules, the Component Library, and Reusable Templates should be updated to name the specific file (`Governance — 13-policies.md, Sec. 13.5`). That sweep is the bulk of the work and the bulk of the risk.

## Open questions for the Board

- Is the token-budget problem real enough in practice to justify a change touching hundreds of cross-references? (The chapter is reference material, loaded selectively — the counter-argument is that a disciplined reader already loads only the section they need.)
- Should this instead be solved by a generated in-file table of contents + anchor links, leaving the single file intact? Lower risk, most of the navigation benefit.
- If split: keep `01-Governance.md` as a pointer stub, or remove it and let `01-governance/CONTEXT.md` be the entry?

## Why this is deliberately not in CR-027

CR-027's own review says so: *"a major structural change touching every cross-reference in the manual … deserves its own CR and Board discussion."* Doing it unilaterally would contradict Governance Sec. 13.3 (no consultant overrides Core structure without Board sign-off).

## Interim mitigation already shipped in CR-027

None to the file itself. If the Board wants a low-risk step now, adding a generated ToC to `01-Governance.md` is a candidate that needs no cross-reference sweep.
