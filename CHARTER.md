# Project Charter: Project Framework

**Charter ID:** PROJ-001
**Created:** 2026-04-05
**Last Updated:** 2026-04-05
**Status:** 🟢 Active
**Type:** Personal / Business Strategy

---

## 1. Overview

**One-line description:**
> A personal operating system for running projects — how work gets tracked, decisions get documented, and progress gets communicated.

**Problem statement:**
Without a consistent system, projects accumulate debt: tasks fall through the cracks, decisions get forgotten, and there's no record of how or why things were built. This framework solves that by establishing shared rules for how Claude and the human work together across all future projects.

**Success looks like:**
The framework is used on the first real project without needing structural changes. The charter is clear, task IDs stay in sync, the changelog is published, and the interaction model feels natural and unambiguous.

---

## 2. Goals & Non-Goals

### Goals — ranked by importance

- [ ] **G1 — Define the human–Claude–world interaction model:** How decisions flow between Sunny, Claude, and the external world must be explicitly documented — in prose and as a flowchart.
- [ ] **G2 — Create a reusable project charter template:** A structured, fill-in-the-blank charter that works across software, content, business, and personal projects.
- [ ] **G3 — Establish a publishable changelog system:** Honest, readable entries with a human voice. Could be published as a portfolio or blog.
- [ ] **G4 — Build a task management system with traceable IDs:** Tasks carry a TASK-NNN ID that links across charters, timelines, and changelog entries.
- [ ] **G5 — Set up GitHub as the home for all project files:** All framework and project files live in version-controlled repos.
- [ ] **G6 — Prove the framework works:** Run a real project through it end to end.

### Non-Goals
- Not building tooling or automation around the framework
- Not designing for teams — this is a solo + Claude system
- Not creating a perfect system upfront — it improves with use

---

## 3. Stakeholders

| Role | Name | Involvement |
|---|---|---|
| Owner | Sunny | Final decisions, sign-off |
| Contributor | Claude | Active work, drafting, structuring |

---

## 4. Scope & Deliverables

### In Scope
- `FRAMEWORK.md` — the living core document
- `INTERACTION.md` — explicit definition of how Sunny, Claude, and the external world interact, including a flowchart
- `CHARTER.md` — this file
- `TASKS.md` — master task registry
- `RISKS.md` — programme-level risk register
- `changelog/CHANGELOG.md` — running project log
- `README.md` — repo introduction
- GitHub repo set up and populated

### Out of Scope
- Automating any part of the workflow
- Building a UI or dashboard for the framework
- Defining frameworks for specific project types

### Definition of Done
The framework has been successfully used on at least one real project without needing structural changes. All files are on GitHub and the changelog has at least one published entry.

---

## 5. Timeline & Milestones

| Milestone | Date | Description | Status |
|---|---|---|---|
| Kickoff | 2026-04-05 | Framework structure and rules established, published to GitHub | ✅ Done |
| Interaction Model Complete | 2026-04-10 | INTERACTION.md written and approved | 🔄 In Progress |
| Framework Validated | 2026-05-05 | Successfully used on a first real project | ⬜ Not Started |

---

## 6. Budget

### Stage 1 — Active

| Item | Unit Cost | Duration | Total |
|---|---|---|---|
| Claude Pro subscription | $20/month | 3 months | $60 |

**Ceiling:** $60

---

## 7. Linked Documents

| Document | Location |
|---|---|
| Interaction model | [INTERACTION.md](./INTERACTION.md) |
| Task board | [TASKS.md](./TASKS.md) |
| Risk register | [RISKS.md](./RISKS.md) |
| Changelog | [changelog/CHANGELOG.md](./changelog/CHANGELOG.md) |
| Notes | [NOTES.md](./NOTES.md) |

---

## 8. Communication Plan

**Check-in frequency:** As needed
**Decision log:** [changelog/CHANGELOG.md](./changelog/CHANGELOG.md)
