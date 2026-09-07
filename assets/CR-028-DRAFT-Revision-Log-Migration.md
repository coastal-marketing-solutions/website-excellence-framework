# Change Request — CR-028 *(WORKING DRAFT — NOT ADOPTED)*

**Submitted By:** `icm-architect` review pass ([`WEF-ICM-Architecture-Review-2026-09-07.md`](WEF-ICM-Architecture-Review-2026-09-07.md), finding **F-4**)
**Date:** 2026-09-07
**Scope:** Front Matter (Revision Log); new `WEF-v1.0/_change-requests/` directory
**Governance Board Decision:** _Pending_

## Problem

`00-Front-Matter.md`'s Revision Log is an index that has absorbed content payload — rows CR-014…CR-027 each carry 5–15 lines of "what changed and why." ICM: *the catalog holds no books.* Two observed consequences:

- **CR-number collisions** — RETRO-017 (CR-021/RETRO-013 renumbered to CR-022/RETRO-017), and CR-024/CR-025 renumbered for the same reason. A hand-maintained index drifts (invariant 9).
- Reading the log to find "the highest CR number" — which `wef-sync` Step 4 requires every pass — is now a non-trivial scan of a wall of prose.

## Proposed change

1. **Create `WEF-v1.0/_change-requests/`.** One file per CR with a non-trivial body — `CR-0NN.md` — containing the full prose currently inline in the Revision Log row, plus YAML frontmatter: `id`, `date`, `status`, `sections` (list), `retros` (list), `supersedes` / `superseded_by`. Move CR-005 through CR-027; leave the single "CR-001 through CR-004 → see MWEF" row as-is.
2. **Reduce the Revision Log to a thin table:** `Change ID · Date · Section(s) · One-line summary · Status · Link`. The link points to `_change-requests/CR-0NN.md`.
3. **Add `WEF-v1.0/_change-requests/CONTEXT.md`** — a one-screen index: what this folder is, the frontmatter schema, and the rule that the next free CR number is `max(id) + 1` read from these files (not from the prose log).
4. **Update `wef-sync` Step 4** to read the next free number from `_change-requests/` frontmatter.
5. **Later (separate, optional):** generate the thin Revision Log table from `_change-requests/*` frontmatter via a script so it cannot drift. Not required for this CR — the thin hand-maintained table is already a large improvement.

## Why this is its own CR, not part of CR-027

It is ~22 new files plus a rewrite of the single most cross-referenced table in the manual. Bundling it with CR-027's naming sweep and new skill would make neither reviewable. Every `see CR-0NN` reference elsewhere in the manual keeps resolving (they are prose references to an ID, and the ID still exists), but a reviewer needs to confirm that deliberately, on its own.

## Risk if not approved

The log keeps growing; the next concurrent-session CR collision is a matter of time. Mitigated partially by CR-022's reservation discipline, not eliminated.

## Validation checklist

- [ ] Every moved CR's prose is preserved verbatim in its `_change-requests/CR-0NN.md`.
- [ ] Thin table's one-line summaries are genuinely one line and lossless enough to navigate by.
- [ ] `retros:` frontmatter cross-links resolve to the RETRO entries in Governance Sec. 15.4.
- [ ] `wef-sync` and the Multi-Context Reconciliation Protocol both updated to point at the new source of the next-free-number.
- [ ] `git diff --check` clean; all Markdown links resolve.
