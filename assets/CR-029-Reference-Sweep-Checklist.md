# CR-029 — Deferred Reference Sweep Checklist

**Owner:** Framework maintainer (currently ajgonzalez2k)
**Cadence:** opportunistic — when a listed file is next edited for any reason, sweep its
`Governance, Sec. N` references in the same PR. No hard deadline; the checklist is the tracking
mechanism so the migration finishes instead of becoming permanent drift.
**Closes:** when every box below is checked. Delete this file and note completion in
`_change-requests/CR-029.md` frontmatter (`status: Adopted`, add a "sweep complete" line).

## What "sweep" means

Change bare `Governance, Sec. 13.5` → `Governance — 13-policies.md, Sec. 13.5` (name the section
file). Section→file map is in
[`../WEF-v1.0/Core-Methodology/01-governance/CONTEXT.md`](../WEF-v1.0/Core-Methodology/01-governance/CONTEXT.md).
Bare references still *resolve* (section numbers are stable) — this is a precision/navigability
upgrade, not a bug fix, which is why it can be deferred.

## Core Methodology chapters

- [ ] `WEF-v1.0/Core-Methodology/02-Research.md` (5)
- [ ] `WEF-v1.0/Core-Methodology/03-SEO-Architecture.md` (2)
- [ ] `WEF-v1.0/Core-Methodology/05-Design.md` (16)
- [ ] `WEF-v1.0/Core-Methodology/06-Development.md` (22)
- [ ] `WEF-v1.0/Core-Methodology/07-QA-Optimization.md` (5)
- [ ] `WEF-v1.0/Core-Methodology/08-AI-Workflows.md` (8)
- [ ] `WEF-v1.0/Core-Methodology/09-Reusable-Templates.md` (13)
- [ ] `WEF-v1.0/Core-Methodology/10-AI-Agent-Services.md` (5)
- [ ] `WEF-v1.0/Core-Methodology/01-governance/*` — intra-chapter refs between the now-split section files (do these together, one pass)

## Front / Back matter

- [ ] `WEF-v1.0/00-Front-Matter.md` (7)
- [ ] `WEF-v1.0/99-Back-Matter.md` (34) — highest single-file count; do carefully
- [ ] `WEF-v1.0/Component-Library/00-Component-Library-Index.md` (5)
- [ ] `WEF-v1.0/Component-Library/Category-Marketing-Trust.md` (1)

## Industry Modules

- [ ] `WEF-v1.0/Industry-Modules/Module-Cash-Home-Buyer.md` (5)
- [ ] `WEF-v1.0/Industry-Modules/Module-Real-Estate-Development.md` (2)
- [ ] `WEF-v1.0/Industry-Modules/Module-Distressed-Property-Advocate.md` (2)
- [ ] `WEF-v1.0/Industry-Modules/Module-Commercial-Real-Estate.md` (1)
- [ ] `WEF-v1.0/Industry-Modules/Module-Expired-Listings-Commercial.md` (1)
- [ ] `WEF-v1.0/Industry-Modules/Module-Probate-Real-Estate-Investor.md` (1)
- [ ] `WEF-v1.0/Industry-Modules/Module-Real-Estate-Luxury-Agent.md` (1)

## Skills

- [ ] `.agents/skills/wef-sync/SKILL.md` (5 bare refs remain in step bodies)
- [ ] `.agents/skills/new-engagement/SKILL.md` (bare refs remain outside the "Read as needed" line already fixed)
- [ ] `.agents/skills/intake/SKILL.md` (any remaining bare refs)

## Engagement-KB template (`assets/templates/engagement-KB/`)

- [ ] `_config/Project-Charter.md` (6)
- [ ] `CONTEXT.md` (4)
- [ ] `AGENTS.md` (2)
- [ ] `blueprint/Master-Website-Blueprint.md`, `_references/README.md`, `_config/WEF-Candidate-Findings.md`, `_config/Project-Backlog.md`, `_config/Open-Questions.md`, `_config/Decision-Register.md`, `_config/Compliance-Constraints-Log.md`, `_config/Assumptions-Log.md` (1 each — do in one pass)

## Live engagement KBs (separate tracked rollout)

- [ ] Each active engagement's `CLAUDE.md` / `CONTEXT.md` / stage `CONTEXT.md` navigation layer
      that references `Governance Sec. N` — update on the next `wef-sync` pass or when that
      engagement is next worked, the way CR-022's `WEF-Candidate-Findings.md` backfill was handled.

## Frozen — do NOT sweep (point-in-time records)

`WEF-v1.0/_change-requests/CR-0*.md` · `assets/CR-027-DRAFT-*` · `assets/CR-028-DRAFT-*` ·
`assets/CR-029-DRAFT-*` · `assets/CR-029-Board-Decision-Memo-*` ·
`assets/WEF-ICM-Architecture-Review-2026-09-07.md`. These describe history as it was; leaving the
old reference form is correct.
