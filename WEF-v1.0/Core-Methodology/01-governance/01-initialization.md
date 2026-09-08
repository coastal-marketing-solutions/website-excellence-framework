# Governance — 1. Project Initialization

*Core Methodology — Governance, Sec. 1. Part of [`01-governance/`](CONTEXT.md) — the router for this chapter.*

---

## 1. Project Initialization

### 1.1 Purpose

Project Initialization converts a signed Statement of Work (SOW) into a running engagement with an assigned team, a provisioned Knowledge Base, a **selected Industry Module**, and a scheduled first Stage Gate. It exists to prevent the single most common cause of engagement failure: starting substantive work before the team agrees on scope, roles, module selection, and success criteria.

### 1.2 Initialization Workflow

```
 SOW Signed
     │
     ▼
 [1] Engagement Lead assigned ──────► Engagement Lead confirms scope vs. SOW
     │
     ▼
 [2] Industry Module selected ───────► Confirm against Charter industry
     │                                  classification (Sec. 1.5); note if a
     │                                  blend of two modules is required
     ▼
 [3] Core team staffed (see Sec. 2) ─► Roles assigned; specialists booked
     │
     ▼
 [4] Knowledge Base provisioned ─────► Folder structure created (Sec. 5),
     │                                  Industry Module linked
     ▼
 [5] Project Charter drafted ────────► See Sec. 3; signed by client + Engagement Lead
     │
     ▼
 [6] Kickoff Meeting held ───────────► Template: Reusable Templates, Meeting Templates
     │
     ▼
 [7] Master Website Blueprint seeded ► Skeleton document created (Sec. 6)
     │
     ▼
 [8] Stage Gate 1 scheduled ─────────► Engagement formally begins
```

### 1.3 Initialization Checklist

- [ ] SOW reviewed by Engagement Lead against WEF standard scope boundaries
- [ ] Client intake captured as `01-research/01-WEF-Intake.md` — strongly preferred via the `intake` skill (`.agents/skills/intake/`), or from any equivalent completed Client Intake Worksheet (Reusable Templates, Sec. 16.2); encouraged, not a hard gate — if intake was run only as live Q&A, the answers are still written to that file before Stage Gate 1
- [ ] Client industry classified and the corresponding Industry Module selected (or a documented two-module blend agreed — see Sec. 1.5)
- [ ] Client primary contact and decision authority (Section 3.4) confirmed in writing
- [ ] Core team assigned and calendars blocked for Stage Gates 1–3 at minimum
- [ ] Knowledge Base workspace created at `/clients/{client-name}/wef/`
- [ ] Project Charter drafted and routed for signature, naming the active Industry Module(s)
- [ ] Kickoff meeting scheduled within 5 business days of SOW signature
- [ ] Compliance/regulatory contact identified, if the active Industry Module flags the client's vertical as regulated
- [ ] Technology stack confirmed or default stack (Governance, Sec. 13.4) accepted
- [ ] Digital Estate & Access Map identifies the owner, operational custodian, access tier, recovery path, and environment boundary for every production system; no secret values are stored in the Knowledge Base
- [ ] Billing/scope guardrails communicated to full team

### 1.4 Industry Module Selection

At initialization, the Engagement Lead selects the Industry Module that matches the client's business from the current library (Industry Modules front matter). Selection is a Decision Register entry (`DEC-INIT-001`), not an informal choice — it determines which personas, compliance landscape, keyword strategy, trust signals, and content model will be consumed at every downstream Module Injection Point.

**If no existing Industry Module matches the client's vertical**, do not force-fit an adjacent module. Trigger the New Module Development Process (Section 13.6) as a parallel workstream, using the closest existing module as a starting template, and flag the schedule impact to the client.

### 1.5 Blended-Module Engagements

Some clients span two verticals (e.g., a real estate brokerage that also originates mortgages in-house, or a law firm with an embedded financial-planning practice). In these cases:

- Name a **primary** module (governs overall site architecture and positioning) and a **secondary** module (governs a defined sub-section of the site) explicitly in the Project Charter.
- Log the blend decision and its boundary (which pages/sections follow which module) as a Decision Register entry.
- Never silently merge two modules' compliance requirements — apply the stricter of the two wherever they conflict, and flag the conflict to both modules' relevant Compliance Liaison(s) for resolution.

### 1.6 Common Mistakes

- Starting Discovery interviews (Stage Gate 1) before the Project Charter is signed and the Industry Module is confirmed, resulting in scope and persona disputes later.
- Selecting an Industry Module casually or defaulting to whichever module the team last used, rather than verifying it actually matches the client's regulatory and business model.
- Failing to identify a compliance contact at initialization for a regulated vertical — this routinely causes rework in Development (Copywriting) and QA & Optimization.
- Force-fitting a client into the nearest existing module instead of triggering the New Module Development Process when the fit is genuinely poor.

### 1.7 Service Add-On Modules (Optional, Orthogonal to Industry Modules)

An **Industry Module** (Sec. 1.4) selects which vertical's rules apply — exactly one is required per engagement. A **Service Add-On Module** is a different, optional axis entirely: an additional capability the firm delivers on top of the website build, independent of vertical. Zero, one, or several may be active on a single engagement, in any combination, alongside any Industry Module.

The current Service Add-On library lives in AI Agent Services (Core Methodology, file 10):

- **Stage Gate 12A — Chat AI Agent-as-a-Service**: an AI chat agent embedded on the client's website itself.
- **Stage Gate 12B — Voice AI Agent-as-a-Service**: an AI voice agent operating over telephony, delivered independent of the website.

Unlike Industry Modules, Service Add-On Modules do not gate or get gated by the mandatory Stage Gate spine (SG1–SG11.5) — an engagement can complete its website Stage Gates and launch with a Service Add-On still in progress, not yet scoped, or never scoped at all. Name active Service Add-On(s) explicitly in the Project Charter (Sec. 3.2) the same way an Industry Module is named — an add-on delivered without a Charter entry is scope no one formally agreed to.
