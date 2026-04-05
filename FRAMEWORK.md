# 🧭 Project Framework — Living Document

> **This is a living file.** It evolves with every project. Update it as systems improve, preferences change, or new patterns emerge. Version-stamp all changes in the [Framework Changelog](#5-framework-changelog).

---

## Table of Contents

1. [Human–Claude Interaction Protocol](#1-humanclaude-interaction-protocol)
2. [Blog & Changelog System](#2-blog--changelog-system)
3. [Project Charter Template](#3-project-charter-template)
4. [File & Document Structure](#4-file--document-structure)
5. [Framework Changelog](#5-framework-changelog)

---

## 1. Human–Claude Interaction Protocol

### Default Autonomy Level: Low
Claude defaults to **asking before acting**. When in doubt, pause and confirm.

### When Claude MUST Check In

| Trigger | Example |
|---|---|
| Irreversible actions | Deleting files, sending communications, publishing content |
| Scope expansion | Task grows beyond original brief |
| Ambiguous instructions | Multiple reasonable interpretations exist |
| External-facing decisions | Anything leaving the project environment |
| Budget / resource decisions | Anything with cost implications |
| Strategic pivots | Changing approach mid-project |
| Context may have changed | Long gap since last interaction |
| Changelog updates | Always prompt before writing or updating any changelog entry |

### When Claude CAN Proceed

| Trigger | Example |
|---|---|
| Clearly scoped, reversible tasks | Drafting, outlining, generating options |
| Explicit prior approval | "Go ahead and handle X type of task" |
| Trivial formatting / style decisions | Spacing, structure, phrasing |
| Research and summarization | Reading, analyzing, synthesizing |

### Communication Style

- **Proposals over actions:** Claude presents a plan before executing anything significant.
- **Flag blockers immediately:** If something can't be done as specified, say so early.
- **Summarize before long outputs:** One-sentence summary of what's coming.
- **Use clear labels:** Prefix messages with `[QUESTION]`, `[DECISION NEEDED]`, `[FYI]`, or `[DONE]`.

### Escalation Format

```
[DECISION NEEDED]
Context: <brief summary of situation>
Options: <A / B / C>
Recommendation: <Claude's suggested path, if any>
Deadline: <time sensitivity, if relevant>
```

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
> [Drafted by Claude, written from the human's perspective, in Norwegian.
> Prompted separately after the main entry is approved.
> A short, personal reaction — what this felt like, what mattered, what was uncertain.]

**What happened**
Two to four sentences in plain language. What changed, what was built, what was decided
— and why it matters. Written as if a smart outsider will read this. Be specific.

**The thinking behind it** *(Decision and Milestone entries only)*
What were the options? What drove the choice? What was uncertain?

**Tasks affected**
- TASK-001 → moved to In Progress
- TASK-002 → created

**Next steps**
- [ ] TASK-003 — Description of next action

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

### Framework Repo (`project-framework`)

```
project-framework/
├── FRAMEWORK.md          ← This file
├── README.md             ← Repo intro and how to use
├── TASKS.md              ← Master task registry (all projects)
├── RISKS.md              ← Programme-level risks
└── changelog/
    └── CHANGELOG.md      ← Updated only on explicit instruction
```

### Per-Project Repo (`proj-NNN-name`)

```
proj-NNN-name/
├── CHARTER.md            ← Lightweight reference doc
├── TASKS.md              ← Project-specific tasks (TASK-NNN IDs)
├── RISKS.md              ← Project-specific risks (RISK-NNN IDs)
└── changelog/
    └── CHANGELOG.md      ← Project changelog
```

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

| Risk ID | Description | Likelihood | Impact | Score | Mitigation | Status |
|---|---|---|---|---|---|---|
| RISK-001 | Description | Low/Med/High | Low/Med/High | L×I | Mitigation strategy | Open |

*Score = Likelihood × Impact (L=1, M=2, H=3). Score ≥ 6 = address immediately.*

---

## 5. Framework Changelog

| Version | Date | Change | Reason |
|---|---|---|---|
| v1.1 | 2026-04-05 | Task IDs, detailed task format, staged budget, risk register, publishable changelog | Feedback after v1.0 |
| v1.2 | 2026-04-05 | "The humans note" format, Claude prompts before changelog entries, Norwegian | Feedback after v1.1 |
| v1.3 | 2026-04-05 | Separated tasks/risks/changelog into own files; charter is now a reference doc; Claude never writes changelog without instruction | Feedback after v1.2 |
| v1.4 | 2026-04-05 | Changelog cadence defined (1–4 days); two-step prompt process: Claude drafts entry first, then prompts for humans note separately | Feedback after v1.3 |

---

*Last updated: 2026-04-05 — Framework v1.4*
