# WEF ICM Cleanup — Pass 2

**Date:** 2026-09-07
**Method:** `icm-architect` skill, Restructure/audit mode, run against `main` after CR-027–CR-030 merged.
**Scope:** a second sweep for cleanup items *not already tracked* in `HANDOFF.md`. This is an identify-only pass — nothing here is implemented.

---

## Already tracked (in `HANDOFF.md` — not re-listed here)

- **CR-029 deferred Governance reference sweep** — `assets/CR-029-Reference-Sweep-Checklist.md` is the live tracker; ~185 bare `Governance, Sec. N` refs to repoint opportunistically. Still resolve, so it's a precision upgrade not a bug.
- **CR-030 Revision Log row** still says "Working Draft — pending Board" — flip to `Adopted` (merged in PR #17).
- **Stale remote branches** — `wef-cr-023-*`, `wef-cr-024-*`, `wef-cr-027-*`…`wef-cr-030-*` — user deletes in GitHub.

## Verdict on the CR-027–030 work

Well executed and ICM-sound. The thin Revision Log + per-CR `_change-requests/CR-0NN.md` files + a real `CONTEXT.md` contract (with the `max(id)+1` next-number rule) is a faithful invariant-2/9 fix. The `01-governance/` split has proper H1 headings, an italic back-pointer on every section file, and a question-routing table in `CONTEXT.md`. Both new folders pass the walk test. The intake integration (below) survived all four merges intact.

**Intake step — confirmed integrated.** `.agents/skills/intake/SKILL.md` is on `main`; it is wired into `AGENTS.md` (routing table), `01-governance/01-initialization.md` (init checklist, encouraged-not-gated), `02-Research.md` (SG1 Inputs + Workflow step 1), `01-governance/08-documentation.md` (names the `01-research/01-WEF-Intake.md` path), `09-Reusable-Templates.md` Sec. 16.1–16.2 (canonical question set + the new Q9 priority-locations question), and `new-engagement` Steps 1 & 6. Revision Log CR-027 = `Adopted`; canonical writeup at `_change-requests/CR-027.md`.

---

## New findings

Severity: **High** = a catalog contradicts the filesystem or an approval claim points at nothing; **Medium** = real drift, no breakage yet; **Low** = tidy-up / accept.

### C-1 — `Module-Real-Estate-Luxury-Agent.md` is a half-catalogued Industry Module *(High — invariant 9, and the framework's own Governance Sec. 13.6)*

The file exists and is listed in `Industry-Modules/00-Module-Template-and-Index.md` (row + a blended-module example). But:

- Its own "Development Note" states: *"Submitted to the Methodology Governance Board as a Change Request (see Front Matter Revision Log) and approved for addition to the permanent Industry Modules library at v1.0."* **There is no such row in the Revision Log**, and **no `_change-requests/CR-0NN.md` file** for it. CR-005–CR-013 (which added every other module) don't cover it.
- It's **absent from `README.md`** — the "What's here" tree lists 13 modules and the header badge says "**13** Industry Modules"; the actual count is 14 (plus the template).
- It's **absent from `00-Front-Matter.md`**'s Table of Contents Industry-Modules list (13 bullets).

So a module claims Board approval via a pointer that resolves to nothing, and two of the three top-level catalogs don't know it exists.

**Fix:** mint the next free CR (**CR-031**) as a retroactive record of the module's addition — Revision Log row + `_change-requests/CR-031.md` (`status: Adopted`, `sections: [Industry Modules — Module-Real-Estate-Luxury-Agent.md]`) — *or*, if it was genuinely approved under an existing CR, cite that number in the module text. Then add the module to `README.md` (tree + badge → 14) and the `00-Front-Matter.md` TOC list. Fold the C-2 count fixes into the same PR.

### C-2 — File/module counts are stale in the entry documents *(Medium — invariant 8)*

- `00-Front-Matter.md` Document Control → "Companion Files": `Core Methodology (10 files)` — now 9 `.md` files **+ the `01-governance/` folder** (16 files) **+ the `_change-requests/` folder**. `Industry Modules (13 files)` — actually 14 modules + 1 template = 15. Verify `Component Library (6 files)`.
- `00-Front-Matter.md` §6 "How to Use" → "read … the entire Core Methodology (all 10 files)" — chapter 01 is now a folder.
- `README.md` → "**13** Industry Modules … and 6 more"; the "Framework at a glance" table.

**Fix:** update the counts; where a chapter became a folder, say so (e.g. "10 chapters — chapter 01 is the `01-governance/` folder of 15 section files + a router").

### C-3 — `/MWEF-v1.0/` is referenced as a present directory but isn't in this repo *(Medium — invariant 8 / reference integrity)*

~8 references assert MWEF is "preserved intact / unmodified at `/MWEF-v1.0/`": `00-Front-Matter.md` (Version History row, Document Control "Predecessor", "Relationship to Predecessor", Revision Log CR-001–004 row), `99-Back-Matter.md` (glossary, references list, appendix), `Industry-Modules/Module-Mortgage-Lending.md`. The directory does not exist here. Every one of those pointers dangles for anyone working from this repository, and `README.md` also says "preserved unmodified at `/MWEF-v1.0/`".

**Fix:** decide the intent. The Document Control table says the storage of record is the private "Firm Knowledge Base" — if MWEF is deliberately private, reword every reference to "preserved in the firm Knowledge Base; not included in this public repository." If it should be public, add it. Don't leave assertions of a path that isn't there.

### C-4 — `assets/` mixes live reference, historical process records, and a live tracker with nothing distinguishing them *(Medium — invariant 4, "structure is documentation")*

| File | Actually is |
|---|---|
| `WEF-Multi-Context-Reconciliation-Protocol.md` | **live** reference |
| `New-Website-Intake-Worksheet.md`, `templates/`, `banner.svg` | **live** |
| `CR-029-Reference-Sweep-Checklist.md` | **live** tracker (open work) |
| `CR-027-DRAFT-*.md`, `CR-028-DRAFT-*.md`, `CR-029-DRAFT-*.md` | **superseded** — the canonical writeups are now `_change-requests/CR-0NN.md` (reconciliation protocol rule 2: one concept, one home) |
| `CR-029-Board-Decision-Memo-*.md` | **historical** point-in-time record |
| `WEF-ICM-Architecture-Review-2026-09-07.md` | **historical** (all findings resolved — see C-5) |
| `WEF-Three-Engagement-Reconciliation-Crosswalk-2026-08-13.md` | **historical** (pre-dates this arc) |

**Fix:** add `assets/README.md` classifying every file (live / historical / tracker). Move the superseded and historical docs to `assets/_archive/` (propose, don't silently delete — reconciliation protocol + ICM restructure rule); give each `CR-0NN-DRAFT` a one-line header pointing at its canonical `_change-requests/CR-0NN.md`. Consider relocating `CR-029-Reference-Sweep-Checklist.md` to `_change-requests/CR-029-reference-sweep.md`, beside `CR-029.md`.

### C-5 — `WEF-ICM-Architecture-Review-2026-09-07.md` §5 status table is stale *(Low)*

It still shows F-4/F-8 as "staged" and CR-028/CR-029 as "(draft)". All four CRs (027–030) are merged. Add a dated banner at the top ("All eight findings resolved — CR-027…CR-030, merged 2026-09-07") and mark the §5 rows done, then it's ready to archive per C-4.

### C-6 — `HANDOFF.md` lives in the repo entry surface *(Low — accept for now)*

It's a working note beside `AGENTS.md` / `CLAUDE.md` / `README.md`, and it says itself "Delete it once the open items below are closed." Useful right now (it's the CR-029 sweep tracker). **Fix:** at closeout of the sweep + the CR-030 row flip, delete it or fold its residue into `assets/` / the persistent memory note.

### C-7 — `CONTRIBUTING.md` doesn't mention the `_change-requests/` workflow *(Low)*

CR-028 made every Core change a `CR-0NN.md` file + a thin Revision Log row, next number = `max(id)+1` from `_change-requests/`. `CONTRIBUTING.md` still describes only "open an Issue / PRs welcome." **Fix:** add a short "Change Requests" subsection pointing at `WEF-v1.0/_change-requests/CONTEXT.md` and the reserve-before-you-write rule.

### C-8 — `01-Governance.md` (stub) and `01-governance/` (folder) are case-adjacent *(Low — accept, but record it)*

They differ only by case + `.md`. `git` and case-insensitive filesystems cope (the extension disambiguates), and the stub exists precisely so `01-Governance.md` links keep resolving — renaming would defeat it. **Fix:** none; add one line to `01-governance/CONTEXT.md` noting the adjacency is deliberate so a later restructure doesn't "tidy" it.

---

## Suggested batching

| PR | Contents | Findings |
|---|---|---|
| **CR-031** | Retroactive record + full cataloguing of the Luxury Agent module; fix all stale counts in `README.md` and `00-Front-Matter.md` | C-1, C-2 |
| **CR-032** | `assets/` housekeeping: `assets/README.md`, `assets/_archive/`, move superseded DRAFTs + historical docs, stub headers, update the ICM review status; delete `HANDOFF.md` if the CR-029 sweep is also done | C-4, C-5, C-6 |
| **fold into the next content PR** | `/MWEF-v1.0/` reference wording; `CONTRIBUTING.md` Change-Request subsection; `01-governance/CONTEXT.md` adjacency note | C-3, C-7, C-8 |

C-3 could also ride in CR-031 since it touches the same two entry documents.
