# `_change-requests/` — Change Request bodies

**What this folder is.** One file per adopted or in-flight Change Request against the WEF
Core Methodology, Industry Modules, Component Library, or repo tooling — `CR-0NN.md`, holding
the full "what changed and why" prose. The Front-Matter Revision Log
(`../00-Front-Matter.md`) is the thin index over these files: `ID · Date · Section(s) · one-line ·
Status · Link`. The prose lives here; the catalog stays a catalog (ICM invariants 2 and 9).

**Reads:** nothing — these are leaf documents.
**Writes:** a new `CR-0NN.md` per Change Request, plus the matching thin row in the Revision Log.
**Human-checks:** the Methodology Governance Board reviews each CR here (via its PR) before the
Revision Log row flips to `Adopted`.

## Frontmatter schema

```yaml
---
id: CR-0NN                     # canonical Change Request number
date: YYYY-MM-DD               # date submitted / adopted (matches the Revision Log row)
status: Adopted                # Adopted | Working Draft | Reserved | Pending Governance Board approval
sections:                     # free-text list, from the Revision Log "Section(s) Affected" column
  - Governance Sec. 15.6
  - .agents/skills/wef-sync/SKILL.md
retros: []                    # [RETRO-0NN, ...] entries this CR added to Governance Sec. 15.4; [] if none
supersedes: []                # [CR-0NN, ...] this CR replaces; [] if none
superseded_by: []             # [CR-0NN, ...] that later replaced this one; [] if none
---
```

## The next-free-number rule

The next free Change Request number is **`max(id from every file in this folder) + 1`**, counting
`Reserved` and `Working Draft` files — never reuse a number that is merely pending. Read it from
these files' frontmatter, **not** by scanning the Revision Log prose. This is the single source
`wef-sync` Step 4 and the Multi-Context Reconciliation Protocol (rule 9) consult before reserving
a number. Reserve by adding the `CR-0NN.md` file (status `Reserved`) *and* its Revision Log row
before work begins, and re-check immediately before merge — reservation lowers collision odds, it
does not eliminate them (see RETRO-017).

## Scope boundary

`CR-001` through `CR-004` predate the WEF re-architecture and are not moved here — see
`/MWEF-v1.0/00-Front-Matter.md` for that history, as the single Revision Log row still records.
