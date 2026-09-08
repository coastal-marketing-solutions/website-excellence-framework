# Governance — 7. Project Backlog

*Core Methodology — Governance, Sec. 7. Part of [`01-governance/`](CONTEXT.md) — the router for this chapter.*

---

## 7. Project Backlog

### 7.1 Purpose

The Project Backlog tracks discrete units of work below the Stage Gate level — tasks, open questions, content items pending, dependencies on the client — so that the Project Manager has a single place to assess engagement health at any moment. Identical in structure across every industry.

### 7.2 Backlog Item Schema

| Field | Description |
|---|---|
| Item ID | Format `BL-{sequence}` |
| Title | Short description |
| Stage Gate | Associated gate |
| Owner | Assigned role/person |
| Status | Not Started / In Progress / Blocked / Client-Dependent / Done |
| Priority | P0 (blocks gate exit) / P1 / P2 |
| Dependency | What this item is blocked by, if anything |
| Due Date | Target completion |

### 7.3 Backlog Cadence

Reviewed at minimum weekly by the Project Manager; P0 items are reviewed daily until cleared. Client-Dependent items exceeding their due date by more than 5 business days are escalated to the Engagement Lead and logged as a Risk (Section 14).
