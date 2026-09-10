# Website Excellence Framework — repository map

WEF is an industry-agnostic **Core Methodology** (numbered Stage Gates, run in
order, on every engagement) plus a library of pluggable **Industry Modules** (one
selected per engagement, two blended where a client spans verticals). This file
routes; it holds no methodology content.

## Where things live

| Path | What it is |
|---|---|
| `WEF-v1.0/00-Front-Matter.md` | Intro, Core + Modules architecture, Version History, thin Revision Log index. Read once. |
| `WEF-v1.0/_change-requests/` | One `CR-0NN.md` per Change Request (full prose + frontmatter); source of the next free CR number. `CONTEXT.md` first. |
| `WEF-v1.0/Core-Methodology/01…10` | The Stage Gate spine, in order (Governance → … → AI Agent Services). Chapter 01 is a folder — `01-governance/CONTEXT.md` routes its 15 sections. |
| `WEF-v1.0/Industry-Modules/` | Vertical packs; start at `00-Module-Template-and-Index.md`. |
| `WEF-v1.0/Component-Library/` | Cross-industry registry of reusable UI components; `00-Component-Library-Index.md` first. |
| `WEF-v1.0/99-Back-Matter.md` | Glossary, references, index, appendices. |
| `.agents/skills/` | Runnable skills — see routing table below. |
| `assets/` | Protocols, worksheets, templates, and review docs that support the method but are not canon — see `assets/README.md` for what's live vs archived. |
| `assets/templates/engagement-KB/` | Literal starter an engagement KB is copied from (per `new-engagement` Step 6). |

## Route by task

| I want to… | Go to |
|---|---|
| Start a new client website | `.agents/skills/intake/` → then `.agents/skills/new-engagement/` |
| Generate / process a client's intake answers | `.agents/skills/intake/SKILL.md` |
| Initialise the engagement Knowledge Base after intake | `.agents/skills/new-engagement/SKILL.md` |
| Run a Stage Gate | `WEF-v1.0/Core-Methodology/` — the chapter for that gate, with the active Industry Module open alongside |
| Build / extend the Master Content Workbook (SG5 / SG8 / SG9) | `.agents/skills/master-content-workbook/SKILL.md` |
| Add or fix an Industry Module | `WEF-v1.0/Industry-Modules/00-Module-Template-and-Index.md` |
| Roll one engagement's findings back into the framework | `.agents/skills/wef-sync/SKILL.md` |
| Reconcile changes from several engagements / contexts at once | `assets/WEF-Multi-Context-Reconciliation-Protocol.md` |
| Propose a methodology change | `WEF-v1.0/Core-Methodology/09-Reusable-Templates.md` Sec. 3 (Change Request template) |
| Understand the ICM structure this repo is built on | `assets/WEF-ICM-Architecture-Review-2026-09-07.md` |

## Rules

- Core Methodology changes go through a Change Request + Methodology Governance
  Board (Governance Sec. 13.1–13.2), written up in `WEF-v1.0/_change-requests/CR-0NN.md` and
  indexed in the Front-Matter Revision Log.
  Never edit canon silently. When several contexts have changes, only one
  integrator edits canon — see the Multi-Context Reconciliation Protocol.
- Industry-specific facts (regulations, personas, page patterns) live in Industry
  Modules, never in the Core.
- One home per fact — link, don't copy.
- File naming inside an engagement KB: `Title-Case-No-Version.md` in each stage's
  `output/` (Reusable Templates Sec. 21.4); client-supplied inputs at the stage
  folder root.
