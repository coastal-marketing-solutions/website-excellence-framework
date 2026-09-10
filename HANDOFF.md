# Handoff — resume point for a new context window

**Written:** 2026-09-07
**Repo:** `website-excellence-framework` (remote: `coastal-marketing-solutions/website-excellence-framework`)
**Branch to start from:** `main` (all recent work is merged)
**This is a working note, not canon. Delete it once the open items below are closed.**

---

## TL;DR

The 2026-09 `icm-architect` audit of the framework repo
(`assets/WEF-ICM-Architecture-Review-2026-09-07.md`, findings F-1…F-8) is **fully worked
through and merged**. Five change requests landed:

| CR | Scope | PR | State |
|---|---|---|---|
| CR-027 | Intake skill + ICM alignment F-1–F-7 | #13, #14 | Merged |
| CR-028 | Revision Log bodies → `WEF-v1.0/_change-requests/` (F-4) | #15 | Merged |
| CR-029 | Split `01-Governance.md` → `01-governance/` (F-8, Board Option C) | #16 | Merged |
| CR-030 | `master-content-workbook` skill (F-3 completion) | #17 | Merged |

`main` HEAD at time of writing: `8e1ad11` (Merge PR #17).

---

## Open items (in priority order)

### 1. CR-029 deferred reference sweep — the one real open thread

`assets/CR-029-Reference-Sweep-Checklist.md` is the tracker. ~185 bare `Governance, Sec. N`
references across ~48 files still use the pre-split form; they should become
`Governance — <section-file>.md, Sec. N` (section→file map is in
`WEF-v1.0/Core-Methodology/01-governance/CONTEXT.md`).

- **These still resolve** (section numbers are stable + `01-Governance.md` is a pointer stub), so
  this is a precision/navigability upgrade, not a bug — do it **opportunistically**: when you
  edit any file on the checklist for another reason, sweep its Governance refs in the same PR and
  tick the box.
- Highest-density files: `99-Back-Matter.md` (34), `06-Development.md` (22), `05-Design.md` (16),
  `09-Reusable-Templates.md` (13).
- `01-governance/*` intra-chapter refs between the now-split section files: do those together in
  one pass.
- Live engagement-KB nav layers (`CLAUDE.md` / `CONTEXT.md` / stage `CONTEXT.md`) that name
  `Governance Sec. N` — separate tracked rollout, update on the next `wef-sync` pass or when that
  engagement is next worked (like CR-022's backfill).
- **Frozen — do NOT sweep:** `_change-requests/CR-0*.md`, the `assets/CR-0*-DRAFT-*` files, the
  Board memo, the ICM review. Those are point-in-time records.

### 2. Trivial Revision Log status cleanup (do with the next sweep PR)

`WEF-v1.0/00-Front-Matter.md` Revision Log: the **CR-030 row still says "Working Draft — pending
Board"** — flip to `Adopted` (merged in #17). CR-020 and CR-023 legitimately remain "Working
Draft — pending Board". Can't be done as a direct `main` push in the agent environment — fold it
into the next branch/PR.

### 3. Stale remote branches to delete (cosmetic, user does this in GitHub)

`wef-cr-027-intake-and-icm-alignment`, `wef-cr-028-revision-log-migration`,
`wef-cr-029-governance-chapter-split`, `wef-cr-029-governance-split-board-memo`,
`wef-cr-030-master-content-workbook-skill` — all merged. Also `wef-cr-023-*` and `wef-cr-024-*`
(CR-023/CR-024 are adopted in the Revision Log; branches are stale). The agent cannot delete
remote branches in this environment.

---

## How to resume

```bash
cd "C:/Users/itzel/Git-repos/website-excellence-framework"
git checkout main && git pull origin main
git log --oneline -5
```

**Orient:** `AGENTS.md` (repo router) → `WEF-v1.0/_change-requests/CONTEXT.md` (CR schema +
next-free-number rule: `max(id)+1` from the files there, currently → **CR-031**) →
`WEF-v1.0/Core-Methodology/01-governance/CONTEXT.md` (the new Governance router).

**To start any new framework change:** branch from `main` as `wef-cr-031-<slug>`, add
`WEF-v1.0/_change-requests/CR-031.md` (frontmatter `status: Reserved`) + a thin Revision Log row
*before* writing content (Governance Sec. 15.6 Layer 3), then push and open a PR.

---

## Environment gotchas

- **`gh` CLI is installed** (`C:\Program Files\GitHub CLI\gh.exe`) **but not authenticated** —
  the browser login flow can't run in a non-interactive session. The user opens and merges every
  PR via GitHub Desktop / the web.
- **The agent cannot push to `main` or delete remote branches** in this environment (blocked by
  the auto-mode classifier). Work goes on a branch → PR → the user merges.
- Windows checkout: `git` warns `LF will be replaced by CRLF` on `git add` — benign, expected.
- Before starting a new CR, check for other open `wef-cr-*` branches (see the
  Multi-Context Reconciliation Protocol) — only one integrator merges canon.

---

## Key file map

| File | Role |
|---|---|
| `assets/WEF-ICM-Architecture-Review-2026-09-07.md` | The audit — findings, walk test, prioritized table (now all "done") |
| `assets/CR-029-Reference-Sweep-Checklist.md` | **The live open item** — deferred Governance reference sweep tracker |
| `WEF-v1.0/_change-requests/` | One `CR-0NN.md` per Change Request + `CONTEXT.md`; source of the next free CR number |
| `WEF-v1.0/Core-Methodology/01-governance/` | Governance chapter, split into 15 section files + `CONTEXT.md` router |
| `WEF-v1.0/Core-Methodology/01-Governance.md` | Pointer stub — kept so old links resolve |
| `.agents/skills/master-content-workbook/SKILL.md` | New skill (SG5/SG8/SG9 workbook, SKELETON/ENRICH/FINALISE modes) |
| `.claude/…/memory/wef-icm-audit-disposition.md` | Persistent memory of this whole arc |
