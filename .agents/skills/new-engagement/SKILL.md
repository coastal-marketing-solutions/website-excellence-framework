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
Sec. 16.2 (Intake Worksheet), Sec. 16.3 (Perplexity Research Prompt), Sec. 16.4 (Charter),
Sec. 17.1 (Kickoff Agenda), Sec. 21 (AGENTS.md/CONTEXT.md templates).
The best worked example of the target end state is any sibling `*Website Blueprint/` folder
that already has a `AGENTS.md` + `_config/` — read one if it exists, to match tone/format.

## Step 0 — Don't re-initialize an existing engagement

Before asking anything, check the parent directory of this repo for a folder that looks like
it's already this client (`{Client Name} Website Blueprint` or similar). If one exists with a
`AGENTS.md` already in it, stop and tell the user — offer to resume from that KB's `AGENTS.md`
instead of running intake again. This skill is for engagements that don't exist yet.

## Step 1 — Intake: check for a completed Worksheet before running live Q&A

Ask the user first whether a completed Client Intake Worksheet (Reusable Templates Sec. 16.2)
already exists for this client — an emailed response, a Google Forms/Typeform export, or any
file with the client's own answers. **If one exists, use it as the source of truth and skip the
live conversational Q&A below** — read the file directly, and only ask follow-up questions for
anything genuinely missing or ambiguous in it. This is the preferred path: the Worksheet is
designed so a client can fill it out asynchronously, and re-asking everything live when a
completed Worksheet already exists is exactly the duplicated-effort this skill exists to avoid.

If no completed Worksheet exists yet, either (a) send the user the Worksheet template
(Reusable Templates Sec. 16.2) to forward to the client and pause here until it comes back, or
(b) if the user wants to proceed immediately without waiting on the client, run the same
questions as a live conversation instead — batch by section below, let the user answer in
whatever order is natural, don't form-dump all of it at once. Either path, anything not yet
known gets marked **PENDING**, not guessed or invented — per the Documentation Standard,
fabricated facts (license numbers, metrics, competitor data) are a hard no.

**Worksheet Section 2 (Service Area & Licensing) is load-bearing — don't proceed past this step
with those fields still blank if it's at all avoidable.** They're the fixed facts Step 3.5's
Perplexity research prompt anchors to; missing them here is exactly what previously let a
research pass silently omit a client's own office location and include a market the client
never confirmed — see Reusable Templates Sec. 16.3's rationale for the specific real case this
prevents.

**Live-conversation fallback (Worksheet's section structure, condensed):**

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

## Step 3.5 — Perplexity Deep Research Brief

Build the research prompt from `09-Reusable-Templates.md` Sec. 16.3, using the *now-confirmed*
Industry Module(s) from Step 2 and the intake facts from Step 1 — this step only runs after
Module selection, never before, so the prompt is scoped by what the framework already knows
about the vertical rather than generic. Fill every bracketed placeholder in the template with
the actual intake answers, and paste in the selected Module's Competitive Landscape Notes and
SEO & Keyword Strategy sections in full, not summarized.

Hand the completed prompt to the user to run in Perplexity (or an equivalent deep-research
tool) — this is a manual handoff step, not something this skill executes itself. Pause here
until the user returns with the resulting `.md` file.

**On receiving the result, reconcile before accepting it.** Check every geographic claim,
competitor, and factual assertion in the returned brief against the Worksheet's Section 2
answers (Step 1). Anything present in the brief but absent from, or in tension with, the
confirmed intake facts becomes an Open Question or Decision Register entry requiring client
confirmation — it does not get silently carried into the Sitemap once Stage Gate 4 begins. Save
the reconciled brief into `01-research/` as a cited research input for Stage Gate 1, not as the
Discovery Report itself.

If the user wants to skip this step entirely (e.g., a very small or well-understood engagement),
that's a legitimate call — log it as a Decision Register entry noting the step was skipped and
why, rather than silently omitting it.

## Step 4 — Confirm engagement name and KB location

Default location: a sibling folder next to this repo (`../{Client Name} Website Blueprint`),
matching the existing convention used across this practice's other engagements. Confirm the
exact client-facing name with the user before creating anything — it becomes the folder name,
the `AGENTS.md`/`CONTEXT.md` titles, and the Project Charter title.

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
├── AGENTS.md
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
│   ├── Project-Backlog.md
│   └── WEF-Candidate-Findings.md
├── _references/
│   └── README.md
└── blueprint/
    └── Master-Website-Blueprint.md
```

Populate each file from the templates in `09-Reusable-Templates.md` Sec. 16.2 (Charter) and
Sec. 21.1–21.3 (`AGENTS.md`/`CONTEXT.md`/stage `CONTEXT.md`), filled with the real answers from
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
- **`WEF-Candidate-Findings.md`**: create from the template (`09-Reusable-Templates.md` Sec.
  23.1), header row only — this engagement hasn't produced any findings yet at initialization.
  Per Governance Sec. 15.6 (Cross-Engagement Contribution Pipeline), append a row here any time
  something discovered live on this engagement looks like a reusable Core Methodology or
  Industry Module improvement, so a periodic `wef-sync` pass picks it up alongside whatever
  other engagements are running concurrently.
- **`blueprint/Master-Website-Blueprint.md`**: a skeleton only (section headers from Governance
  Sec. 6) — this fills in as Stage Gates complete, not at initialization.
- **`01-research/CONTEXT.md`**: the Stage 1 contract (Reusable Templates Sec. 21.3), linking
  purpose/exit-criteria back to `../WEF-v1.0/Core-Methodology/02-Research.md` rather than
  restating the chapter.
- If Step 3.5 produced a reconciled Perplexity brief, save it into `01-research/` alongside
  `output/` (as a client-supplied research input, per the existing convention — see any prior
  engagement's `01-research/` folder for the pattern) and note in `CLAUDE.md`/`AGENTS.md`'s
  Current State that it's there, ready to be consumed once Stage Gate 1 actually starts.

## Step 7 — Report back

Tell the user: where the folder was created, what's still PENDING (and therefore on the Project
Backlog), whether a reconciled Perplexity brief is waiting in `01-research/`, and the two
concrete next actions — schedule the Kickoff Meeting (Reusable Templates Sec. 17.1 agenda) and
begin Stage Gate 1 (Discovery & Market Research) inside the new `01-research/` folder. Do not
start Stage Gate 1 work itself in this same pass unless the user asks — initialization and
Discovery are separate steps (Governance Sec. 1.2, steps 5–8).
