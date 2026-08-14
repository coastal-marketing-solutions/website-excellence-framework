# WEF Multi-Context Reconciliation Protocol

Use this protocol when two or more AI contexts, consultants, or website engagements have independently identified improvements for the Website Excellence Framework (WEF).

## Core Rule: One Canonical Integrator

Only one designated context edits, versions, commits, or pushes the WEF canon during reconciliation. All other contexts are **contributors**: they inspect the current canon and submit structured change packets, but do not modify canonical WEF files.

This avoids three common failure modes:

- two contexts overwrite or interleave changes in the same file;
- the same concept appears twice under different names or section numbers; and
- one context marks a version adopted while another correctly treats it as a working draft.

If contributors share the same local repository, they must not run `git reset`, `git checkout`, `git restore`, `git clean`, pull/rebase, commit, or push. The working tree may contain another context's work.

## Roles

### Canonical Integrator

The integrator:

1. freezes direct canon edits by contributors;
2. preserves the current working tree and identifies pre-existing/unrelated changes;
3. receives one change packet per engagement/context;
4. builds a requirement-level crosswalk before editing;
5. resolves duplication, conflicts, scope, terminology, and version status;
6. implements one coherent change set;
7. runs cross-reference, Markdown, and change-control validation; and
8. presents unresolved policy decisions to the user instead of silently choosing when business intent materially differs.

### Contributor Context

A contributor:

1. reviews the current WEF canon as it exists now;
2. identifies the work or recommendations originating from its own engagement;
3. compares each item with current canon rather than assuming it is still absent;
4. classifies each item as already covered, complementary, conflicting, obsolete, or genuinely new;
5. supplies evidence and proposed placement; and
6. does not edit canon, version history, revision logs, README badges, or Git history.

## Required Change Packet

Every contributor returns this structure:

```markdown
# WEF Reconciliation Packet — [Engagement/Website]

## Packet Metadata
- Contributor context/website:
- Date reviewed:
- WEF repository/path reviewed:
- Git branch/commit if known:
- Current WEF working-draft version observed:
- Canon editing performed during this reconciliation: No

## Executive Summary
[Five to ten sentences describing the reusable lessons and the most important collision risks.]

## Proposed Items

| ID | Recommendation/Rule | Originating Evidence or Incident | Industry-Agnostic Principle | Proposed Layer | Proposed Canon Location | Current Canon Coverage | Relationship | Risk if Omitted | Risk if Adopted | Recommendation |
|---|---|---|---|---|---|---|---|---|---|---|

Allowed `Proposed Layer` values:
- Core Methodology
- Reusable Template
- Component Library
- Industry Module
- Platform Implementation Note
- Engagement-only (do not promote)

Allowed `Relationship` values:
- Already covered — no change
- Duplicate — consolidate wording
- Complementary — extend existing rule
- Conflict — decision required
- Supersedes older rule
- New gap

## Conflict Details

For each item marked `Conflict — decision required`:

### [Item ID] — [Short name]
- Existing canon says:
- This engagement recommends:
- Why they differ:
- Evidence supporting each side:
- Can the conflict be resolved by scope, stage, site type, risk tier, or Industry Module?
- Recommended resolution:
- User/Governance Board decision needed:

## Exact Proposed Language

[For each genuinely new or complementary item, provide concise proposed language. Do not patch files.]

## Existing Work Attribution

- Canon files this context previously edited, if any:
- Concepts this context believes it introduced:
- Changes visible in the working tree that this context did not create or cannot attribute:
- Any uncommitted or untracked files that must be preserved:

## Evidence Register

| Evidence ID | Source/Incident | Source Class | Date/Access Date | Claim Supported | Limitations | Current/Needs Revalidation |
|---|---|---|---|---|---|---|

## Recommended Disposition

- Adopt now:
- Merge into an existing rule/template:
- Keep in Industry Module:
- Keep engagement-only:
- Defer pending evidence:
- Requires user/Governance Board decision:
```

## Reconciliation Decision Rules

The integrator applies these rules in order:

1. **Protect user work and history.** Never discard an unattributed working-tree change merely to obtain a clean diff.
2. **One concept, one canonical home.** Put the normative rule in the appropriate Core section; templates execute it and link back instead of restating a second doctrine.
3. **Separate universal from vertical.** Cross-industry process belongs in Core. Industry claims, regulations, personas, terminology, and page patterns remain in the appropriate Industry Module.
4. **Separate strategy from tools.** Tool-independent requirements belong in Core; Rank Math, Site Kit, WordPress, Hostinger, or other vendor instructions belong in implementation notes unless the confirmed default stack requires a worked example.
5. **Resolve apparent conflicts by scope first.** Check whether both recommendations are valid for different stages, site types, risk levels, environments, or modules before choosing one.
6. **Prefer outcomes and evidence over proxy scores.** Search visibility, meaningful actions, accessibility, compliance, reliability, and maintainability outrank plugin scores or arbitrary quantity targets.
7. **Prefer current primary evidence.** When recommendations genuinely conflict, prioritize applicable law/compliance, current authoritative documentation, verified first-party behavior, repeatable production evidence, then informed professional judgment—in that order.
8. **No silent policy decisions.** If two defensible rules imply materially different cost, risk, scope, or client outcomes, log the conflict and request a user/Governance Board decision.
9. **Version once.** Only the integrator assigns the Change Request number, working-draft version, affected-sections list, approval status, README badge, and final revision-log wording.
10. **Verify the public/generated result.** A clean document diff is necessary but not sufficient when a rule changes generated output, analytics, publishing, or deployment behavior.

## Copy/Paste Prompt for Each Contributor Context

Replace the bracketed website name before sending.

```text
You are one of three contributor contexts helping reconcile independent website-engagement lessons into the Website Excellence Framework (WEF).

Engagement represented by this context: [WEBSITE / PROJECT NAME]

The WEF repository may be shared with other active contexts and may already contain uncommitted work. Effective immediately, do not edit any canonical WEF file, README, version history, revision log, Git branch, commit, or remote. Do not run git reset, checkout, restore, clean, pull/rebase, commit, or push. Preserve all unattributed changes.

Your job is an audit and handoff, not a merge:

1. Review the current WEF repository and its current working tree as read-only.
2. Identify every best practice, standard, workflow, template, safeguard, or lesson that originated in this engagement/context and might be reusable across industries.
3. Compare each recommendation against the canon as it exists now. Do not assume a recommendation is still missing merely because you proposed it earlier.
4. Classify every item as:
   - Already covered — no change
   - Duplicate — consolidate wording
   - Complementary — extend existing rule
   - Conflict — decision required
   - Supersedes older rule
   - New gap
5. Separate industry-agnostic Core guidance from industry-specific Module content, platform/vendor implementation notes, and engagement-only facts.
6. For conflicts, quote or precisely paraphrase both rules, explain whether scope/stage/site type/risk tier resolves the difference, cite the evidence for each, and state whether a user/Governance Board decision is required.
7. Report any WEF files you previously edited and any current working-tree changes you cannot confidently attribute to yourself.
8. Produce the full “WEF Reconciliation Packet” structure defined below. Do not provide only a prose summary and do not patch the repository.

[PASTE THE “Required Change Packet” TEMPLATE FROM assets/WEF-Multi-Context-Reconciliation-Protocol.md HERE, OR READ THAT FILE DIRECTLY IF THIS CONTEXT HAS ACCESS TO THE REPOSITORY.]

Be conservative about promotion into Core: a repeated or clearly universal operational principle belongs in Core; a one-off preference does not. Preserve current primary-source links and identify anything requiring revalidation. End with a concise list of the five highest-priority items for the canonical integrator.
```

## Integrator Intake Prompt

After both contributor packets are available, use this prompt in the designated integrator context:

```text
Act as the sole canonical integrator for WEF. Reconcile the attached contributor packets with the current WEF working tree and the changes already developed in this context.

Before editing:
1. inventory the working tree and preserve unattributed changes;
2. build a requirement-level crosswalk across all three engagements;
3. identify exact duplicates, complementary rules, true conflicts, and scope-resolvable differences;
4. separate Core, Template, Component Library, Industry Module, implementation-note, and engagement-only material;
5. present only material unresolved policy decisions to me before choosing.

Then implement one coherent working-draft change set. Each concept must have one canonical normative home, with templates and indexes linking to it rather than duplicating doctrine. Reconcile section numbers, terminology, cross-references, version history, Change Request status, glossary/index entries, and README version badge. Do not mark a working draft adopted without explicit approval. Do not commit or push unless I separately authorize it.

Validate UTF-8 readability, Markdown fences/tables, unique version and Change Request rows, unique canonical templates, internal cross-references, git diff --check, and the final changed-file inventory. Report which packet items were adopted, merged, deferred, rejected, kept vertical, or left for a decision, with rationale.
```

## Recommended Three-Context Sequence

1. Pause direct WEF editing in all three contexts.
2. Keep this NFGC context as the canonical integrator because it currently holds the reconciled WEF working tree.
3. Send the contributor prompt to the other two contexts, replacing the website/project name.
4. Have each context return its full packet in chat. If desired, save each response under a unique non-canon filename such as `assets/reconciliation-packets/YYYY-MM-DD-project-slug.md`; never let both contexts write the same packet file.
5. Paste both packets into the integrator context or provide their exact saved paths.
6. The integrator produces the crosswalk first, asks only for true policy decisions, then performs the single canonical merge.
7. Review and approve the resulting working draft before commit/push and formal Governance Board adoption.
