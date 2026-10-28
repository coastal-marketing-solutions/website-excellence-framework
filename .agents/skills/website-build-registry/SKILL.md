---
name: website-build-registry
description: Keeps a running, honest record of where a client website build lives (domains, DNS, hosting, deployment, code, plugins, integrations, backups, secrets-by-name-only) and who holds each account, plus a dated changelog of every change — so the build can be audited or handed to another host, vendor, or the client's own team at any time. Use this any time code, theme, hosting, deployment settings, plugins or integrations, DNS or domains, backups, or account ownership change on a client website project; after every deploy or upload; monthly even if nothing changed; before a client meeting; and before any handover or vendor switch. Trigger on mentions of deploying, hosting changes, DNS or domain changes, plugin/integration updates, account ownership, "who owns this", "where does this live", site migration, or client handover — even if the user doesn't say "register" or "changelog" by name.
---

# Website Build Registry

A build registry is a paper trail for a website you build on behalf of a client, kept
separately from the build itself. While the build sits on your own accounts (your
hosting, your API keys, your plugin licenses), this record is how the client can verify
nothing is hidden, and how anyone — the client, a new vendor, you six months from now —
can pick up exactly where things stand without re-discovering it from scratch.

This skill works on any website project, for any client, in any framework or CMS. It
does not assume WordPress, a specific host, or a specific stack — the first-run step
figures that out by inspection.

## Where things live in the project

This skill is project-scoped: everything it reads and writes lives inside the website
project's own repo or folder, never in this skills repo. A given project accumulates:

1. **`BUILD-REGISTER.md`** — the current state. Where each thing lives and who holds it now.
2. **`CHANGELOG.md`** — one dated entry per change to the build, newest first.
3. **The project's own status file** (e.g. `PICKUP.md`, `STATUS.md`) if one already exists.
   Don't create one unless asked.
4. **`reports/YYYY-MM-register-summary.md`** — the monthly client-facing summary.
5. **`PROJECT-RULES.md`** — this project's house rules (see below). Created once per
   project, then just read.

Bundled templates for the first four are in `assets/` in this skill — use them as the
starting skeleton rather than inventing section headers each time, so every project's
register reads the same way.

## Project rules

Each website project has its own facts, forbidden claims, and approval requirements —
these never belong in the skill itself, because they vary per client. Look for
`PROJECT-RULES.md` in the project root.

- **If it exists**, read it before doing anything else this run.
- **If it doesn't exist**, this is the first time this skill has run on this project.
  Copy `assets/PROJECT-RULES-template.md` into the project root as `PROJECT-RULES.md`,
  ask the user once (in one message, not one question at a time) for:
  - the source file for business facts (name, address, hours, claims, reviews) and
    where fact changes get logged
  - topics or claims that must never appear anywhere in this build
  - what needs approval before deploying, buying, sending, or posting
  - any other house rules (tone, naming, no em dashes, whatever they mention)

  Fill in what they give you, write "unknown, to confirm" for anything they skip, and
  continue with the run — don't block on a perfect answer.

## When to run

Any time code, theme, data files, hosting or deployment settings, plugins or tools,
integrations, DNS or domains, backups, or accounts (or who holds them) change; after
any deploy or upload; monthly even if nothing changed; before a client meeting; before
any handover.

## First run (BUILD-REGISTER.md and CHANGELOG.md don't exist yet)

1. Inspect the project and the live site. Identify the platform(s): framework or CMS,
   host, deployment method, integrations. Read config files, package files, deployment
   settings, the hosting or platform dashboard if it's open, and the live site (headers,
   titles, a few pages). **Do not guess** — where you can't verify something, write
   "unknown, to confirm" and add it to Open items.
2. Create `BUILD-REGISTER.md` from `assets/BUILD-REGISTER-template.md`. Every row gets a
   "Held by" and "Last verified" column. The template's sections: Domains and DNS;
   Hosting and deployment (platform, account, project/site name, plan and its terms,
   URL, who holds the account now, planned transfer trigger or date); Code, content and
   files (where each lives, format, version control); Versions (framework, CMS, runtime,
   theme, plugins); Plugins and tools (name, license holder, renewal date, what breaks
   if it lapses); Integrations (forms and where requests go, email sender, CRM,
   analytics, consent banner, spam protection); Google and listings (Business Profile,
   Search Console, Analytics, Bing, Apple, Yelp, BBB, and who is an owner); Backups and
   recovery (what, where, how often, last restore test); Secrets (names only, never
   values, and where the value lives); Renewal and expiry calendar (domain,
   certificates, plan, licenses); Open items.
3. Create `CHANGELOG.md` from `assets/CHANGELOG-template.md` and back-fill what you can
   verify from project/git history, marking anything you can't confirm as "not
   recorded".

## Every run (do all steps, every time)

1. **Check the real state before writing anything**: deployment list, live headers and
   a page title, plugin/theme screens, hosting dashboard. Compare against the register
   and list any difference as drift under Open items. If you can't check something,
   write "not verified" with today's date — never a guess.
2. Update only the rows that changed. Set "Last verified" to today on every row you
   actually checked. Never delete history — mark removed items "removed (date)".
3. Add a `CHANGELOG.md` entry for every change, using the template below, including how
   to undo it.
4. Update the renewal/expiry calendar if any date changed.
5. Update the project's own status file if one exists (don't create one otherwise).
6. Re-read everything you just wrote and strip any secret value that crept in (see
   Rules below).
7. Run the project's own checks if it has them (build, link check, claims/copy check)
   and confirm the live site(s) still load.
8. Finish with a 3–6 line plain-language summary for the client: what changed, where it
   lives, what they need to do (if anything). No jargon, no promises of rankings, calls,
   or revenue.

## Changelog entry template

```
### YYYY-MM-DD: short title
- What changed:
- Where (file, platform, page, plugin):
- Why / who asked:
- Deployed to (URL, deployment name or version):
- How to undo:
- Checks run (and result):
- Client action needed (or "none"):
```

## Rules

These hold regardless of how the request is phrased, because the whole point of the
register is that the client can trust it:

- **Never write secrets** — no passwords, API keys, tokens, license keys, recovery
  codes, or one-time links, anywhere (register, changelog, summary, commit messages).
  Record only the account/variable name and who or what holds the value (e.g. "form
  service key, held in the owner's password manager").
- **Never invent a fact, version, date, plan name, or owner.** Unknown means "unknown,
  to confirm" — not a plausible guess.
- **For every account, write who holds it now** (agency or client), their role (owner,
  admin, helper), and the planned transfer date or trigger.
- **Keep business facts in their one source file** (phone, address, hours, claims,
  reviews — named in `PROJECT-RULES.md`); point to it, never copy the facts into the
  register.
- **Keep each client's data separate.** Never record another client's or another
  location's accounts or data in this project's files.
- **This skill only reads and writes the five files above.** Never deploy, buy, send,
  post, delete, or change an account setting while running it — that's a different task,
  even if the register shows it's needed.
- Plain language a non-technical client can read — no jargon, no hype.

## Monthly report

Write `reports/YYYY-MM-register-summary.md` from `assets/register-summary-template.md`:
a one-page status and ownership summary — what exists, what changed this month, what
renews in the next 90 days, who holds each account, open items, and what's needed from
the client.

## Handover trigger

If the client asks to leave, switch vendors, or take the site over, stop normal work
and build an exit kit from the register: accounts and who holds them, files and
backups, licenses, documentation, search continuity (old/new addresses, sitemap, Search
Console, Analytics), and a signed handover record. Use the project's own handoff
document if it has one; otherwise build the kit directly from `BUILD-REGISTER.md`.

## Definition of done

Register rows match reality and carry today's date where verified; every change has a
changelog entry with how to undo it; drift is listed under Open items; no secret value
appears anywhere; the client has a short plain-language summary.

## Starting a run

Check whether `BUILD-REGISTER.md` and `CHANGELOG.md` exist in the project. Missing →
run First run. Present → run Every run. Either way, read or create `PROJECT-RULES.md`
first, and finish by showing the plain-language summary.
