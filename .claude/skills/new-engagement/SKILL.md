---
name: new-engagement
description: Run WEF Project Initialization for a brand-new client website engagement — client intake questionnaire, Industry Module selection, technology stack confirmation, and scaffolding of a new "{Client} Website Blueprint" Knowledge Base folder next to this repo. Use whenever the user wants to start a new website, onboard a new client, kick off an engagement, run intake, or "initiate the WEF repo" for a new project.
---

# New Engagement Intake & Initialization

Runs WEF Governance Sec. 1 (Project Initialization) end to end: intake → Industry Module
selection → tech stack confirmation → Knowledge Base scaffold → Project Charter → first
Decision Register entries. Goal: the user answers questions once, in order, and walks away
with a real KB folder ready for Stage Gate 1 — not a checklist they have to operate by hand.

Read as needed, don't front-load: `../WEF-v1.0/Core-Methodology/01-Governance.md` Sec. 1
(workflow), Sec. 5 (KB structure/nav layer), Sec. 13.4/13.4.1 (stack); `09-Reusable-Templates.md`
Sec. 16 (Intake/Charter), Sec. 17.1 (Kickoff Agenda), Sec. 21 (CLAUDE.md/CONTEXT.md templates).
The best worked example of the target end state is any sibling `*Website Blueprint/` folder
that already has a `CLAUDE.md` + `_config/` — read one if it exists, to match tone/format.

## Step 0 — Don't re-initialize an existing engagement

Before asking anything, check the parent directory of this repo for a folder that looks like
it's already this client (`{Client Name} Website Blueprint` or similar). If one exists with a
`CLAUDE.md` already in it, stop and tell the user — offer to resume from that KB's `CLAUDE.md`
instead of running intake again. This skill is for engagements that don't exist yet.

## Step 1 — Intake conversation

Ask these conversationally (not as one giant form-dump — batch by section, let the user answer
in whatever order is natural). Source: Reusable Templates Sec. 16.1. Anything the user doesn't
know yet gets marked **PENDING** later, not guessed or invented — per the Documentation Standard,
fabricated facts (license numbers, metrics, competitor data) are a hard no.

**Company/Industry Overview**
- Business/client name, industry, business model, service area or jurisdiction(s)
- Offerings, niche specializations, credentials/licenses/registrations held

**Business Objectives**
- Primary goal for this engagement (new build / redesign / rebuild)
- Quantified success metrics, if known (fine if not — GA4/Search Console instrumentation is
  often part of the build itself)

**Current Digital Presence**
- Current website URL, if any
- Analytics access available (GA4 / Search Console)?
- Known pain points with the current site

**Team & Stakeholders**
- Marketing lead
- Compliance/standards contact, if the vertical is regulated
- Practitioners/staff available for interview
- Decision Authority for approvals — name the person(s), per gate if it splits (Governance
  Sec. 3.4 — e.g. a business owner holding strategic/design sign-off separate from a broker or
  compliance officer holding a mandatory regulatory sign-off)

**Compliance/Standards Notes**
- Known advertising or professional-conduct restrictions
- Jurisdiction-specific disclosure requirements the client is already aware of

**Competitors (client-nominated)**
- 2+ named competitors, or offer to research some once Stage Gate 2 begins

## Step 2 — Industry Module selection

List the modules actually in `../WEF-v1.0/Industry-Modules/` (read the directory, don't rely on
a memorized list — it grows). Propose the best match based on Step 1's answers and confirm with
the user via AskUserQuestion. Cover:

- **Single module** — the common case.
- **Blended** (Governance Sec. 1.5) — client spans two verticals. Name a **primary** (governs
  overall architecture/positioning) and **secondary** (governs a defined sub-section only) and
  record the boundary. Never silently merge two modules' compliance rules — the stricter one wins
  wherever they conflict.
- **No good match** — don't force-fit. Flag that a New Module Development Process (Governance
  Sec. 13.6) is needed as a parallel workstream, using the closest existing module as a starting
  template, and tell the user this affects schedule.

## Step 3 — Technology stack confirmation (layer by layer, not silently defaulted)

Per Governance Sec. 13.4.1, walk every layer and get an explicit choice — "use the WEF default"
is valid but must be **selected**, not assumed by omission:

| Layer | WEF default |
|---|---|
| Hosting | *(client choice — no framework default)* |
| CMS | WordPress |
| Theme Framework | GeneratePress Premium |
| Page Building | GenerateBlocks Pro |
| Asset/Cloud Layer | GenerateCloud |
| SEO Plugin | Rank Math SEO |
| Caching | LiteSpeed Cache |
| CDN / Edge Security | Cloudflare |
| Analytics | Google Analytics 4 |
| Search Monitoring | Google Search Console |
| Tag Management | Google Tag Manager |
| Behavioral Analytics | Microsoft Clarity |

Also confirm the **Content & Code Access Tier** (Sec. 13.4.1) for whatever host is chosen —
this is not knowable in the abstract ("we use Hostinger" doesn't tell you the plan's shell
access), so ask or note it as PENDING pending a hosting-plan check:

1. **Preferred** — SSH + WP-CLI (or stack equivalent)
2. **Fallback** — REST API + application-level credential
3. **Last resort** — browser/GUI automation only

Any layer the client hasn't decided yet is PENDING, added to the Project Backlog — not defaulted
silently and not blocking the rest of initialization.

## Step 4 — Confirm engagement name and KB location

Default location: a sibling folder next to this repo (`../{Client Name} Website Blueprint`),
matching the existing convention used across this practice's other engagements. Confirm the
exact client-facing name with the user before creating anything — it becomes the folder name,
the `CLAUDE.md`/`CONTEXT.md` titles, and the Project Charter title.

## Step 5 — Recap and get a go-ahead

Before writing any files, show the user a short recap: client name, Industry Module(s),
Decision Authority, stack choices, KB folder path. This is a real filesystem-creation action
(a new project folder, multiple files) — get an explicit "go ahead" rather than assuming silence
means yes.

## Step 6 — Scaffold the Knowledge Base

Create **only** the following (per Governance Sec. 5.2.1 Rule 2 — do not scaffold every Stage
Gate folder in advance; only Stage Gate 1's folder exists at initialization):

```
{Client Name} Website Blueprint/
├── CLAUDE.md
├── CONTEXT.md
├── 01-research/
│   ├── CONTEXT.md
│   └── output/            (empty, .gitkeep or first Discovery doc once SG1 starts)
├── _config/
│   ├── Project-Charter.md
│   ├── Decision-Register.md
│   ├── Compliance-Constraints-Log.md
│   ├── Open-Questions.md
│   ├── Assumptions-Log.md
│   └── Project-Backlog.md
├── _references/
│   └── README.md
└── blueprint/
    └── Master-Website-Blueprint.md
```

Populate each file from the templates in `09-Reusable-Templates.md` Sec. 16.2 (Charter) and
Sec. 21.1–21.3 (`CLAUDE.md`/`CONTEXT.md`/stage `CONTEXT.md`), filled with the real answers from
Steps 1–4 — not left as bracketed placeholders where an answer exists. Where an answer is
genuinely unknown, write **PENDING** and add a matching `Project-Backlog.md` line, exactly as
the Charter template expects (see any existing `*Website Blueprint/_config/Project-Charter.md`
for tone/format).

Specifics:

- **`_references/README.md`**: one paragraph pointing back at this repo
  (`../wef-github-repo/WEF-v1.0/`) and the selected Industry Module(s) — a pointer, not a copy.
- **`Decision-Register.md`**: seed it with `DEC-INIT-001` (Industry Module selection) and one
  entry per confirmed (or explicitly-deferred) stack layer from Step 3, per Sec. 13.4.1's
  requirement that every layer's confirmation is logged even when the answer is "WEF default."
- **`Compliance-Constraints-Log.md` / `Open-Questions.md` / `Assumptions-Log.md` /
  `Project-Backlog.md`**: seed each with whatever real gaps surfaced in intake (e.g. no GA4
  baseline yet, compliance contact TBD) — empty is fine if nothing surfaced, don't invent filler.
- **`blueprint/Master-Website-Blueprint.md`**: a skeleton only (section headers from Governance
  Sec. 6) — this fills in as Stage Gates complete, not at initialization.
- **`01-research/CONTEXT.md`**: the Stage 1 contract (Reusable Templates Sec. 21.3), linking
  purpose/exit-criteria back to `../WEF-v1.0/Core-Methodology/02-Research.md` rather than
  restating the chapter.

## Step 7 — Report back

Tell the user: where the folder was created, what's still PENDING (and therefore on the Project
Backlog), and the two concrete next actions — schedule the Kickoff Meeting (Reusable Templates
Sec. 17.1 agenda) and begin Stage Gate 1 (Discovery & Market Research) inside the new
`01-research/` folder. Do not start Stage Gate 1 work itself in this same pass unless the user
asks — initialization and Discovery are separate steps (Governance Sec. 1.2, steps 5–8).
