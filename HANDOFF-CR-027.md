# Handoff — CR-027 (Intake skill + ICM alignment)

**Written:** 2026-09-07
**Repo:** `website-excellence-framework` (remote: `coastal-marketing-solutions/website-excellence-framework`)
**Branch:** `wef-cr-027-intake-and-icm-alignment` (pushed)
**PR:** [#13](https://github.com/coastal-marketing-solutions/website-excellence-framework/pull/13) — open, pending review + Governance Board approval
**This file is a working note, not canon — it is committed on the `wef-cr-027-*` branch so a new session can find it. Delete it before merge, or leave it for the follow-up CRs.**

---

## Where things stand

An `icm-architect` audit of the framework produced `assets/WEF-ICM-Architecture-Review-2026-09-07.md` (8 findings, F-1…F-8). Findings **F-1, F-2, F-3, F-5, F-6, F-7** are implemented on the branch above and pushed. **F-4** and **F-8** are drafted as separate Change Requests but not implemented.

### Done (on branch, pending PR + Governance Board approval)

| Finding | What changed |
|---|---|
| F-1 | `AGENTS.md` + `CLAUDE.md` at repo root (router + one-line pointer) |
| F-2 | Governance Sec. 8.3 → defers to Reusable Templates Sec. 21.4; every `-v{N}.md` Required-Document name swept to `Title-Case-No-Version.md` in `output/` across chapters 02, 04, 05, 06, 07, 10 |
| F-3 | `master-content-workbook` skill marked outstanding; procedure inlined to Reusable Templates Sec. 8.4; 3 dangling `Sec. 9.x` refs redirected |
| F-5 | New `.agents/skills/intake/SKILL.md`; `01-WEF-Intake.md` wired into Governance Sec. 1.3, Research SG1 Sec. 3 + Sec. 10; `new-engagement` Steps 1 & 6 rewritten |
| F-6 | Reusable Templates Sec. 16.2 gains Q9 (ranked priority locations), Q9–Q38 → Q10–Q39; Sec. 16.3 brief updated; `assets/New-Website-Intake-Worksheet.md` synced + relabelled; Sec. 16.1 note added |
| F-7 | New `assets/templates/engagement-KB/` skeleton (13 files); `new-engagement` Step 6 = "copy + fill" |
| — | `00-Front-Matter.md` Revision Log: CR-027 row added |

### Not done — next actions

1. **PR [#13](https://github.com/coastal-marketing-solutions/website-excellence-framework/pull/13) is open.** Address any review feedback on the same branch (`git push` updates the PR automatically). Merge only after Governance Board approval (Governance Sec. 13.2–13.3). `gh` CLI was not installed last session — `winget install GitHub.cli` + `gh auth login` if you want CLI review/merge.

2. **F-4 → CR-028** (`assets/CR-028-DRAFT-Revision-Log-Migration.md`): create `WEF-v1.0/_change-requests/CR-0NN.md` (one per CR-005…CR-027), thin the Revision Log table to `ID · Date · Sections · one-line · Status · Link`, add `_change-requests/CONTEXT.md`, update `wef-sync` Step 4 + the Multi-Context Reconciliation Protocol to read the next free CR number from frontmatter. **Its own branch/PR** — do not fold into CR-027.

3. **F-8 → CR-029** (`assets/CR-029-DRAFT-Governance-Chapter-Split.md`): split `01-Governance.md` into `01-governance/` with a `CONTEXT.md` router. **Needs a Governance Board design decision first** (single file + generated ToC vs. full split) — don't implement unilaterally. Take the draft's "Open questions for the Board" to them.

4. **`master-content-workbook` skill** (surfaced by F-3): still doesn't exist. Either build `.agents/skills/master-content-workbook/SKILL.md` from the procedure now inlined in Reusable Templates Sec. 8.4, or leave Sec. 8.4's inline version as the permanent home and drop the "skill outstanding" language.

---

## How to resume in a new Code session

```bash
cd "C:/Users/itzel/Git-repos/website-excellence-framework"
git fetch origin
git checkout wef-cr-027-intake-and-icm-alignment   # if continuing CR-027 review fixes
git log --oneline -3
```

**Orient first:** read `AGENTS.md` (new repo router), then `assets/WEF-ICM-Architecture-Review-2026-09-07.md` (findings + prioritized table with per-item status), then `assets/CR-027-DRAFT-Intake-Skill-and-ICM-Alignment.md` (exact proposed language, §1–§9).

**If PR review comes back with change requests:** make edits on this same branch, commit, push — the PR updates automatically.

**If starting CR-028 or CR-029:** branch from `main` (not from this branch) once CR-027 is merged:
```bash
git checkout main && git pull
git checkout -b wef-cr-028-revision-log-migration
```

---

## Verification commands (re-run after any further edits)

```bash
cd "C:/Users/itzel/Git-repos/website-excellence-framework"

# No stray -v{N}.md Required-Document names left (only the Sec. 21.4 explainer should match):
grep -rnE '[a-z-]+-v[0-9]+\.md' WEF-v1.0/Core-Methodology/

# Intake wiring resolves everywhere it's referenced:
grep -rln 'intake` skill\|01-WEF-Intake.md\|.agents/skills/intake' WEF-v1.0/ .agents/ AGENTS.md

# Worksheet ends at Q39:
grep -nE '^3[0-9]\. ' WEF-v1.0/Core-Methodology/09-Reusable-Templates.md | tail -3

# Code-fence parity in the big-edit files (each count must be even):
for f in WEF-v1.0/Core-Methodology/09-Reusable-Templates.md .agents/skills/intake/SKILL.md; do echo "$f: $(grep -c '^```' "$f")"; done

git diff --check
```

---

## Key file map

| File | Role |
|---|---|
| `assets/WEF-ICM-Architecture-Review-2026-09-07.md` | The audit — findings, walk test, prioritized table (source of truth for what's done vs staged) |
| `assets/CR-027-DRAFT-Intake-Skill-and-ICM-Alignment.md` | CR-027 — exact proposed language, §1–§9, + validation checklist |
| `assets/CR-028-DRAFT-Revision-Log-Migration.md` | F-4, not implemented |
| `assets/CR-029-DRAFT-Governance-Chapter-Split.md` | F-8, not implemented, needs Board |
| `.agents/skills/intake/SKILL.md` | The new skill (GENERATE + INGEST + embedded artifact template) |
| `.agents/skills/new-engagement/SKILL.md` | Steps 1 & 6 changed — consumes intake, copies the KB skeleton |
| `assets/templates/engagement-KB/` | Literal KB skeleton `new-engagement` copies |
| `AGENTS.md` / `CLAUDE.md` (repo root) | New routing entry file |

## Notes / gotchas

- Windows checkout: `git` warns `LF will be replaced by CRLF` on commit — benign, expected.
- The framework's governance requires Core changes to go through a Change Request + Methodology Governance Board (Governance Sec. 13.1–13.2). CR-027's canon edits are on the branch as the review artifact; **the PR is the Board-review vehicle — do not merge to `main` without that approval.**
- `assets/WEF-Multi-Context-Reconciliation-Protocol.md`: if other people/contexts are also editing the framework, only one integrator merges canon — check for other open `wef-cr-*` branches before starting CR-028/029.
