# Changelog

This is the running record of work across all projects — progress updates, decisions, milestones, and reflections. Written to be read, not just filed.

---

### 2026-04-06 — Framework Restructured for Reuse

**Project:** Project Framework (PROJ-001)
**Type:** Milestone
**Status:** 🟢 On Track

**The humans note**
> Dette har vært en interessant runde. Jeg føler at modellen nå jobber mer slik som jeg forventer at den skal jobbe. Det er veldig bra! Jeg ønsker fortsatt at vi skal jobbe mer sammen for at den skal bli mer autonom. Det tror jeg kan komme på plass om litt.
>
> Nå føler jeg at det rammeverket som er her kan brukes i forbindelse med andre prosjekter. Ja, selvfølgelig kunne vi ha gjort en finpuss her og der. Men jeg tror at både jeg og Claude kan lære mye av å bare å ta det nåværende verktøyet og teste det i et noenlunde ekte scenarie.
>
> Et lite problem som jeg føler at jeg har støtt på, som kan bli et problem er tilgjengelige tokens, eller tilgjengelig bruk av tjenesten. Slik det foreligger nå så bruker vi lett opp alt vi har av datakraft i løpet av en halvtime, selv med pro-lisens. Om dette er fordi vi er i Cowork e.l. er jeg litt usikker på. Det er mulig at vi må forandre på oppsettet om vi har lyst til å jobbe videre på fornuftig vis.
>
> Dette har hittil vært et veldig gøy og lærerikt eksperiment. Spent på å se hva som skjer videre!
>
> S🌞nny

**What happened**
The framework is now genuinely reusable. Session 2 added starter templates for all project files and an explicit "starting a new project" checklist to FRAMEWORK.md, so any future project can be bootstrapped cleanly. Alongside this, the interaction model was tightened — file edits now require exact proposed content before approval, reflected in both prose and an updated flowchart. The risk register was reviewed and expanded with four new risks including user-side risks. Token efficiency was addressed by trimming verbose sections and restricting session-start reads to NOW.md only.

**The thinking behind it**
The session surfaced that the framework needed to be separated from PROJ-001's specific files — and that portability required clarity about what travels with every project (FRAMEWORK.md and INTERACTION.md, identical copies) versus what is project-specific. The token efficiency discussion was a useful forcing function: complexity has a real cost per session, and that shapes how we define the threshold in TASK-005.

---

### 2026-04-05 — Kickoff: Framework Established

**Project:** Project Framework (PROJ-001)
**Type:** Milestone
**Status:** ✅ Complete

**The humans note**
> Dette var veldig gøy altså! Så målet her er å bli bedre kjent med KI-tjenester, og hvordan man aktivt kan bruke disse for å tilby support i prosjekter. Prosjekter er mye rart, men styringen av dem omhandler nødvendigvis mye om forvaltning av informasjon. Og her er antakeligvis Claude og andre tjenester bedre enn oss allerede i dag.
>
> Jeg tror dette kan bli veldig bra. Nå gjelder det å lage et godt grensesnitt mellom meg selv og Claude - jeg merker at den enda er litt for lite autonom for min del. Men vi kommer til å klare det etterhvert og da er det bare å peise på!
>
> S🌞nny

**What happened**
Built a complete operational framework from scratch in a single session. The system now covers how work gets tracked, how decisions get made, how Claude and Sunny collaborate day to day, and how everything gets documented. The interaction model in particular required several rounds of iteration — by the end of the session it had grown from a basic decision flowchart into a full operating agreement covering session memory, version control, disagreement handling, and approval conventions.

**The thinking behind it**
The goal from the start was to build something worth showing, not just something that works. Every piece — the changelog, the charter, the interaction model — is designed to be legible to an outside reader. What emerged during the session was as important as what was planned: the system improved by actually being used while it was being built. That feedback loop is the point.

**Tasks affected**
- TASK-000 → Done (four pillars defined)
- TASK-001 → Done (framework built and published)
- TASK-003 → Done (PROJ-001 charter written)
- TASK-004 → In Progress (INTERACTION.md — active, ongoing)

**Next steps**
- [ ] TASK-004 — Continue iterating INTERACTION.md
- [ ] TASK-002 — Identify and charter the first real project (on hold)

---
