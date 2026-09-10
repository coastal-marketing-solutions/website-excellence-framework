# `assets/`

Material that supports the WEF methodology but is **not canon** — canon lives in `WEF-v1.0/`.
Everything here is one of three kinds: **live reference** (use it), **tracker** (open work), or
**archived** (historical, in `_archive/`).

| File | Kind | What it is |
|---|---|---|
| `WEF-Multi-Context-Reconciliation-Protocol.md` | **live reference** | How to reconcile framework changes proposed by several engagements / AI contexts at once — one canonical integrator, read-only packets from the rest. Referenced from `CONTRIBUTING.md` and `AGENTS.md`. |
| `New-Website-Intake-Worksheet.md` | **live reference** | Plain, sendable mirror of the canonical intake question set (`WEF-v1.0/Core-Methodology/09-Reusable-Templates.md` Sec. 16.2). The `intake` skill renders/ingests from Sec. 16.2; if the two diverge, Sec. 16.2 wins. |
| `templates/engagement-KB/` | **live reference** | Literal skeleton a new engagement Knowledge Base is copied from (`new-engagement` skill, Step 6). |
| `banner.svg` | **live reference** | README banner image. |
| `WEF-ICM-Architecture-Review-2026-09-07.md` | **audit of record** | The `icm-architect` audit (findings F-1 … F-8) that CR-027 – CR-031 trace to. Status: all findings resolved. Kept as the audit of record; `AGENTS.md` points here for "why the repo is shaped this way." |
| `WEF-ICM-Cleanup-Pass-2-2026-09-07.md` | **tracker** | Second audit pass (findings C-1 … C-8). C-1 – C-5 done (CR-031, CR-032); C-6 – C-8 open. Retire when C-6 – C-8 close. |
| `CR-029-Reference-Sweep-Checklist.md` | **tracker** | The one live open thread from CR-029 — repoint ~185 bare `Governance, Sec. N` references to the split section files, opportunistically. |
| `_archive/` | **archived** | Superseded proposal drafts and point-in-time records — see below. |

## `_archive/`

Kept for provenance, not for use. Each file carries an `ARCHIVED` banner pointing at its live
successor; internal links inside them may be stale.

| File | Superseded by |
|---|---|
| `CR-027-DRAFT-Intake-Skill-and-ICM-Alignment.md` | `WEF-v1.0/_change-requests/CR-027.md` |
| `CR-028-DRAFT-Revision-Log-Migration.md` | `WEF-v1.0/_change-requests/CR-028.md` |
| `CR-029-DRAFT-Governance-Chapter-Split.md` | `WEF-v1.0/_change-requests/CR-029.md` |
| `CR-029-Board-Decision-Memo-Governance-Chapter-Split.md` | `WEF-v1.0/_change-requests/CR-029.md` (decision carried forward) |
| `WEF-Three-Engagement-Reconciliation-Crosswalk-2026-08-13.md` | `WEF-Multi-Context-Reconciliation-Protocol.md` |

## Adding to `assets/`

A new file here should be classifiable as one of the three kinds above and added to the table.
When a tracker's work is done, move it (and any drafts it spawned) to `_archive/` with a banner
and update the successor link — don't delete (`WEF-Multi-Context-Reconciliation-Protocol.md`
rule 1: protect the record).
