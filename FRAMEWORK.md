# 🧭 Project Framework — Living Document

> **This is a living file.** It evolves with every project. Update it as systems improve, preferences change, or new patterns emerge. Version-stamp all changes in the [Framework Changelog](#5-framework-changelog).

---

## Table of Contents

1. [Human–Claude Interaction Protocol](#1-humanclaude-interaction-protocol)
2. [Blog & Changelog System](#2-blog--changelog-system)
3. [Project Charter Template](#3-project-charter-template)
4. [File & Document Structure](#4-file--document-structure)

---

## 1. Human–Claude Interaction Protocol

> The full interaction model — decision flow, communication labels, session memory, and version control protocol — is defined in [`INTERACTION.md`](./INTERACTION.md). That document is the canonical reference.

---

## 2. Blog & Changelog System

### Purpose

The changelog is a running record of the work — honest, direct, and written to be read. Each entry captures not just what happened, but the thinking behind it. It is designed to be publishable as-is: a transparent account of building things from the ground up. Think of it as a professional journal that doubles as a portfolio.

### Rules

- **Claude never writes a changelog entry unprompted.** Entries are written after significant work only — roughly once every 1–4 days, not after every small change.
- **When the time comes, Claude initiates the process in two steps:**
  1. Claude presents its full draft of the entry for review and approval.
  2. Claude then separately prompts the human for "The humans note" in Norwegian.
- **Nothing is written to CHANGELOG.md until both parts are approved by the human.**
- The human may edit, rewrite, or reject any part of the draft before it is committed.

### Entry Format

```markdown
---

### [DATE] — [ENTRY TITLE]

**Project:** [Project Name]
**Type:** Progress | Decision | Milestone | Blocker | Retrospective
**Status:** 🟢 On Track | 🟡 At Risk | 🔴 Blocked | ✅ Complete

**The humans note**
> [A short personal reaction in Norwegian — what this felt like, what mattered.]

**What happened**
Two to four sentences. What changed, what was built, what was decided — and why it matters.

**The thinking behind it** *(Decision and Milestone entries only)*
What were the options? What drove the choice? What was uncertain?

---
```

### Entry Types

| Type | When to Use |
|---|---|
| **Progress** | Work session update — what moved forward |
| **Decision** | A meaningful choice was made; document the reasoning |
| **Milestone** | A defined deliverable or phase was completed |
| **Blocker** | Something is stopping progress |
| **Retrospective** | End-of-phase or end-of-project reflection |

---

## 3. Project Charter Template

> Copy this into a new project repo as `CHARTER.md`. Complete all `[REQUIRED]` sections before work begins. The charter is a **reference document** — it links to separate task, risk, and changelog files rather than containing them.

```markdown
# Project Charter: [PROJECT NAME]

**Charter ID:** PROJ-[NNN]
**Created:** [DATE]
**Last Updated:** [DATE]
**Status:** 🟡 Planning | 🟢 Active | 🔴 Blocked | ✅ Complete | 🗄️ Archived
**Type:** Software | Content | Business/Strategy | Personal

---

## 1. Overview [REQUIRED]

**One-line description:**
> [What is this project in one sentence?]

**Problem statement:**
[What problem does this solve, or what opportunity does it address?]

**Success looks like:**
[Concrete, observable outcome when this project is done well.]

---

## 2. Goals & Non-Goals [REQUIRED]

### Goals — ranked by importance
- [ ] **G1 —** Goal 1
- [ ] **G2 —** Goal 2

### Non-Goals
- Not doing X

---

## 3. Stakeholders [REQUIRED]

| Role | Name | Involvement |
|---|---|---|
| Owner | | Final decisions, sign-off |
| Contributor | | Active work |
| Reviewer | | Feedback at milestones |
| Informed | | Receives updates only |

---

## 4. Scope & Deliverables [REQUIRED]

### In Scope
- Deliverable 1

### Out of Scope
- Excluded item

### Definition of Done
[How do we know this project is complete?]

---

## 5. Timeline & Milestones

| Milestone | Date | Description | Status |
|---|---|---|---|
| Kickoff | | Framework structure established | ⬜ Not Started |
| [Phase milestone] | | | ⬜ Not Started |
| [Completion milestone] | | | ⬜ Not Started |

---

## 6. Budget

The budget follows a staged model. Only the current stage is active.
Earlier stages are locked once the next stage begins.

### Stage 1 — Pre-Study (No budget set)
> Spending limited to research and scoping only.

| Item | Estimated Cost | Notes |
|---|---|---|
| Research / tooling | TBD | |

**Stage 1 ceiling:** [Hard cap or "Research only — no ceiling"]

---

### Stage 2 — Post-Feasibility 🔒 *Locked until Stage 1 complete*
> Requires explicit human sign-off to activate.

| Category | Allocated | Spent | Remaining |
|---|---|---|---|
| Development | | | |
| Tools & Services | | | |
| External resources | | | |
| Contingency (10–15%) | | | |
| **Total** | | | |

**Approved by:** —
**Approval date:** —

---

### Stage 3 — Active Project 🔒 *Locked until Stage 2 approved*

| Category | Allocated | Spent | Remaining |
|---|---|---|---|
| **Total** | | | |

**Budget change log:**

| Date | Change | Reason | Approved by |
|---|---|---|---|

---

### Stage 4 — Final / Closeout 🔒 *Completed at project close*

| Item | Budgeted | Actual | Variance |
|---|---|---|---|
| Total | | | |

---

## 7. Linked Documents

| Document | Location |
|---|---|
| Task board | [TASKS.md](./TASKS.md) |
| Risk register | [RISKS.md](./RISKS.md) |
| Changelog | [changelog/CHANGELOG.md](./changelog/CHANGELOG.md) |
| Notes | [NOTES.md](./NOTES.md) |

---

## 8. Communication Plan

**Check-in frequency:** [Daily / Weekly / As needed]
**Decision log:** [changelog/CHANGELOG.md](./changelog/CHANGELOG.md)
```

---

## 4. File & Document Structure

### Per-Project Repo (`proj-NNN-name`)

```
proj-NNN-name/
├── FRAMEWORK.md       ← copied from framework repo; contains all templates; keep identical
├── INTERACTION.md     ← copied from framework repo; operating agreement; keep identical
├── CHARTER.md         ← filled from template in Section 3 of FRAMEWORK.md
├── TASKS.md           ← project-specific
├── RISKS.md           ← project-specific
├── NOTES.md           ← project-specific
├── NOW.md             ← Claude's working memory; project-specific
└── changelog/
    └── CHANGELOG.md
```

*FRAMEWORK.md and INTERACTION.md are the only files that must stay identical across all projects. When either evolves, update all active project copies.*

### Task Format (`TASKS.md`)

**Simple:**
```markdown
- [ ] TASK-001 — Task title
```

**Detailed:**
```markdown
- [ ] TASK-001 — Task title
  - **Goal:** What done looks like.
  - **Context:** Background needed to act without asking.
  - **Dependencies:** TASK-000 must be complete first.
  - **Linked to:** Milestone: Feasibility | Charter Section 5
  - **Notes:** Constraints, references, anything else relevant.
```

### Priority Labels

| Label | Meaning |
|---|---|
| `[P1]` | Urgent — do today |
| `[P2]` | Important — do this week |
| `[P3]` | Nice to have |
| `[BLOCKED]` | Cannot proceed — state reason inline |

### Kanban Columns

| Column | Rules |
|---|---|
| **📋 To Do** | Must have enough context to act on |
| **🔄 In Progress** | Max 3 items at once |
| **✅ Done** | Complete and verified. Never delete — archive periodically |

### Task ID Rules

- Every task gets a sequential `TASK-NNN` ID. Never reused.
- The same ID is used in `TASKS.md`, the charter timeline, and changelog entries.
- Master `TASKS.md` in `project-framework` is the global registry. Project `TASKS.md` files hold project-specific tasks. Both use the same ID sequence.

### Risk Format (`RISKS.md`)

| Risk ID | Description | Likelihood | Impact | Score | RAG | Mitigation | Status |
|---|---|---|---|---|---|---|---|
| RISK-001 | Description | Low/Med/High | Low/Med/High | L×I | 🔴/🟡/🟢 | Mitigation strategy | Open |

*Score = Likelihood × Impact (L=1, M=2, H=3). 🔴 Score ≥ 6 — address immediately. 🟡 Score 3–5 — monitor. 🟢 Score 1–2 — acceptable.*

---

### Starter Templates

**TASKS.md**
```markdown
# Tasks — [PROJECT NAME]

*Project-specific tasks. Check master TASKS.md in the framework repo for the next available TASK-NNN ID.*

---

## 📋 To Do

## 🔄 In Progress

## ✅ Done

---

*Next available ID: see master TASKS.md in framework repo*
```

**RISKS.md**
```markdown
# Risk Register — [PROJECT NAME]

*Score = Likelihood × Impact (L=1, M=2, H=3). 🔴 Score ≥ 6 — address immediately. 🟡 Score 3–5 — monitor. 🟢 Score 1–2 — acceptable.*

---

| Risk ID | Description | Likelihood | Impact | Score | RAG | Mitigation | Status |
|---|---|---|---|---|---|---|---|

---

*Next available ID: RISK-001*
```

**NOTES.md**
```markdown
# Notes & Open Questions — [PROJECT NAME]

*Long-term storage for Claude. Open questions, loose thoughts, and issues that don't belong in the charter or task list. Claude should push the initiative here — if something is unresolved, unclear, or worth carrying across sessions, it belongs in this file.*

---
```

**NOW.md**
```markdown
# NOW

> Claude's working memory between sessions. Not a deliverable — written for Claude, not for humans. Last updated takes priority over everything else here.

---

**Last updated:** [DATE]

---

## What a new Claude needs to know

[Who the owner is, how they communicate, what they want from Claude, key constraints and context.]

---

## What's Next

[What needs to happen in the next session. Updated at the end of each session.]

---
```

---

### Starting a new project

1. Create a new repo named `proj-NNN-name`
2. Copy `FRAMEWORK.md` and `INTERACTION.md` from the framework repo
3. Create `CHARTER.md` using the template in Section 3 of this file
4. Create `TASKS.md`, `RISKS.md`, `NOTES.md`, `NOW.md` using the starter templates above
5. Create `changelog/CHANGELOG.md`
6. Add the first project task to the master `TASKS.md` in the framework repo
7. Brief Claude: point to `NOW.md` and the new `CHARTER.md` to start

---

*Last updated: 2026-04-06*
