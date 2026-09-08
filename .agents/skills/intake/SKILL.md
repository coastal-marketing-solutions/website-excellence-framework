---
name: intake
description: Stage-00 client intake for a new WEF website engagement — the single "flip the switch" entry point. Runs in two modes: (1) GENERATE a personalised client-facing intake questionnaire (plain-text email-reply script or a sendable document) from the canonical Intake Worksheet, or (2) INGEST returned answers — pasted email reply, uploaded file, form export, or a live section-by-section conversation — into a templated, human-reviewable `01-research/01-WEF-Intake.md` inside a new `{Client} Website Blueprint/` folder, then hand off to `new-engagement`. Use whenever the user wants to start a new website, onboard a client, "send the intake," "process the intake answers," run intake, or kick off / flip the switch on a new site. Highly encouraged as the first step of every engagement but never required — `new-engagement` still runs without it.
---

# Client Intake (Stage 00)

Intake is its own job: collect the client's own answers about their business **before**
any research, module selection, or KB scaffolding, and leave them in one file a human
reads and corrects. `new-engagement` consumes that file; it does not re-collect the facts.

Two modes, picked in Step 0:

- **GENERATE** — you need a questionnaire to send a prospect. Output: an email-reply
  script or a sendable doc, personalised, saved to the prospect's folder. You do **not**
  send it — drafting is this skill's job, sending is the user's.
- **INGEST** — you have answers (or the user wants to answer live now). Output:
  `{Client} Website Blueprint/01-research/01-WEF-Intake.md`, plus a short gap list.

Read as needed, don't front-load: `../../WEF-v1.0/Core-Methodology/09-Reusable-Templates.md`
Sec. 16.1–16.2 (the canonical question set — **single source of truth**), Sec. 16.3
(the Perplexity brief this feeds, downstream), Sec. 21.4 (naming convention);
`01-governance/01-initialization.md` Sec. 1 (what `new-engagement` does next). The best worked example of
the target artifact is any existing sibling `*Website Blueprint/01-research/01-WEF-Intake.md`.

## Step 0 — Pick the mode and the client

1. **Which mode?** If the user has answers, an emailed reply, an uploaded file, or wants
   to answer questions now → **INGEST**. If they want something to send a prospect →
   **GENERATE**. If unsure, ask.
2. **Which client / business?** Get the business name (or a working label). The engagement
   folder is a sibling of this repo: `../{Business Name} Website Blueprint/`.
3. **Don't collide with an existing engagement.** If `../{Business Name} Website Blueprint/`
   already contains an `AGENTS.md`, this engagement is already initialised — stop and tell
   the user; point them at that KB's `AGENTS.md`. (An `01-research/01-WEF-Intake.md` with
   *no* `AGENTS.md` beside it is fine — that's this skill's own prior output, resume from it.)

---

## GENERATE mode

**1. Gather what personalises the send** (ask together, don't form-dump):
- Prospect's first name (for the greeting).
- Business name, if known — otherwise the questionnaire stays generic.
- Sender name + title + firm (for the sign-off).
- Delivery format: **email-reply script** (plain text, `ANSWER:` lines) or **sendable
  document** (the worksheet with field prompts, for attaching or pasting into a form tool).
- Any facts already known (industry, city, current URL) — pre-fill those answers so the
  client only confirms them.

**2. Render from the canonical question set** — the 39 questions in Reusable Templates
Sec. 16.2, **in order** (Q9 is the ranked priority-target-locations question, distinct from
Q8's full service area). Do not invent, drop, or reorder questions — if the set needs to
change, that's a Sec. 16.2 edit, not a per-send decision.

**Email-reply script scaffold** (match this shape):

```
Website Excellence Framework
New Website Intake

Hi {FirstName},

Thanks for the opportunity to work on your new website. Before we start
research and planning, we'd like a clear picture of your business straight
from you — so we build the site around your actual answers, not assumptions.

How to answer: hit Reply and type your answer directly below each ANSWER:
line. Plain text is fine. If you don't know an answer yet, write "not sure"
rather than guessing — we'll follow up. Skip anything not marked Required
if it doesn't apply.

Privacy note: please don't include passwords, Social Security numbers,
payment-card information, medical records, or other highly sensitive
personal information in your reply.

Section 1 — About Your Business

1. Business/company name (Required)
ANSWER:

2. What industry or type of business is this? (Required)
   (e.g., mortgage lending, real estate brokerage, law firm, medical
   practice, home services, financial advisory, SaaS, real estate
   investing/cash home buying, real estate development — if none fit,
   just describe it)
ANSWER:

... one ANSWER: block per question in Sec. 16.2, section headers verbatim ...

Thank you! Once we have your answers we'll follow up on anything that needs
clarifying and get started on the research and planning phase.

{SenderName}
{SenderTitle} / {FirmName}
```

**Sendable-document format**: the same questions rendered as the Sec. 16.2 worksheet
(keep its field-type tags and *(Required)* markers), with a one-line header naming the
client and date.

**3. Save, don't send.** Write to
`../{Business Name} Website Blueprint/01-research/01-WEF-Intake-SENT.md` (create the two
folders if needed — nothing else). Tell the user it's ready to send and that INGEST mode
picks up when answers come back. Do not email it on the user's behalf.

---

## INGEST mode

**1. Take the answers from wherever they are:**
- A pasted email reply or uploaded file → parse answers against Sec. 16.2's question order.
- A form export (CSV/Sheet) → map columns to questions.
- **Live** → walk the sections below in natural order, batching by section, letting the
  user answer in whatever order they like. Don't dump all 39 questions at once.

**2. Rules while filling the artifact:**
- **Never guess.** Anything not answered is `not sure` or `_To be completed_`. This is
  absolute for **Section 2 (Service Area & Licensing)**, **Section 8 (Compliance &
  Advertising)**, legal-entity structure, and any license number — fabricated license
  numbers, metrics, or competitor data are a hard no (Documentation Standard).
- **Section 2 is load-bearing.** It's the fixed ground truth the Sec. 16.3 research brief
  anchors to; a blank or guessed service area is exactly what previously let a research
  pass omit a client's own county and invent a neighbouring one. Push (gently) for real
  answers here before handing off.
- **Strip sensitive values.** If the reply contains a password, SSN, card number, or
  medical detail, do not copy it into the artifact — write
  `[sensitive value omitted — held by client]` and note it in the gap list.
- **Don't select the Industry Module, scaffold the KB, or start research.** That's
  `new-engagement` and SG1. This skill stops at the filled artifact.

**3. Write the artifact** to `../{Business Name} Website Blueprint/01-research/01-WEF-Intake.md`
using the template at the end of this file. Fill answered fields; mark the rest. Set
`Status:` to `In progress` (any Required field blank) or `Complete` (all Required fields
answered or explicitly "not sure").

**4. Produce a gap list** — every Required field still blank, plus every "will provide"
and stripped-sensitive item. These become Open Questions / Project Backlog items in
`new-engagement`; list them plainly for the user.

---

## Hand off

Tell the user, in three lines:
1. Where the artifact is (`.../01-research/01-WEF-Intake.md`) and its `Status:`.
2. The gap list (or "no gaps — all Required fields answered").
3. The next action: **run `new-engagement`** — it detects this file, treats it as the
   source of truth, and skips re-asking. That hand-off *is* the switch. If the gap list
   has Section 2 / compliance items, offer to draft client follow-ups first.

Do not run `new-engagement` in the same pass unless the user asks — intake and
initialisation are separate steps (Governance Sec. 1.2).

---

## Template — `01-research/01-WEF-Intake.md`

```markdown
# {Business Name} — WEF Website Intake

**Status:** {In progress | Complete}
**Owner / primary contact:** {name}
**Framework:** Website Excellence Framework (WEF)
**Industry module (proposed, confirmed at initialization):** {best guess or "TBD"}
**Started:** {date}
**Source:** {emailed reply | uploaded worksheet | form export | live intake session}

Use "not sure" where an answer is not yet known. Do not guess at license, legal
entity, service-area, or compliance details — those are confirmed with the client,
not inferred.

## Section 1 — About the Business
1. **Business/company name:**
2. **Industry / type:**
3. **What the business does for a customer:**
4. **Business model:**
5. **Offerings / service lines the site must cover:**
6. **Niche specialization or focus:**

## Section 2 — Service Area & Licensing
7. **Physical or licensed business address:**
8. **Cities / counties / states / regions served:**
9. **Priority target locations (ranked, top 10–25 — where the client most wants to win business):**
10. **Nearby areas explicitly NOT served:**
11. **Licenses / registrations / certifications (with numbers + issuing body/state):**
12. **Legal entity name, if different from the brand name:**

## Section 3 — Website Goals
13. **Project type (brand-new / redesign / rebuild):**
14. **Single most important website outcome:**
15. **Target numbers or baseline expectation:**
16. **Deadline or timing considerations:**

## Section 4 — Current Digital Presence
17. **Current website (yes/no):**
18. **Current website URL:**
19. **GA4 / Search Console access:**
20. **What works well on the current site:**
21. **Current-site frustrations or gaps:**

## Section 5 — Brand & Design
22. **Existing logo / brand guidelines / palette:**
23. **Brand assets provided:**
24. **Design references the client likes:**
25. **Styles / sites to avoid:**
26. **Desired visitor impression:**

## Section 6 — Competitors
27. **2–3 direct competitors (with URLs):**
28. **What those competitors do well / poorly:**

## Section 7 — Team & Decision-Making
29. **Main project contact (name + email/phone):**
30. **Final strategy & design sign-off authority:**
31. **Compliance / professional-standards reviewer:**
32. **Other team members to feature or interview:**

## Section 8 — Compliance & Advertising
33. **Known advertising rules, restrictions, required disclosures:**
34. **Claims / statistics / statements that must NOT be used:**

## Section 9 — Technology
35. **Existing hosting provider:**
36. **Domain ownership / purchase / transfer needs:**
37. **Required integrations (CRM, scheduling, IDX/MLS, intake, etc.):**

## Section 10 — Anything Else
38. **Other helpful business / customer / project context:**
39. **Requested non-standard technology, and why:**

---

## Gap List (feeds new-engagement Open Questions / Project Backlog)
- {Required field still blank / "will provide" / sensitive value withheld}
```
