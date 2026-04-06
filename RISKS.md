# Programme Risk Register

*Cross-project risks affecting the overall programme. Project-specific risks live in each project's own `RISKS.md`.*

*Score = Likelihood × Impact (L=1, M=2, H=3). Score ≥ 6 = address immediately.*

---

| Risk ID | Description | Likelihood | Impact | Score | RAG | Mitigation | Status |
|---|---|---|---|---|---|---|---|
| RISK-001 | Framework becomes too complex to maintain consistently | Medium | High | 6 | 🔴 | Mitigation unresolved — TASK-005 created to define what "too complex" looks like in practice and address this risk | Open |
| RISK-002 | Task IDs fall out of sync between master registry and project files | Medium | Medium | 4 | 🟡 | Master TASKS.md is always updated first | Open |
| RISK-003 | Budget stages bypassed under time pressure | Low | Low | 1 | 🟢 | Stage gates require explicit human sign-off; Claude cannot unlock unilaterally | Open |
| RISK-004 | Claude acts outside the interaction model — edits files without presenting exact content first | Medium | Medium | 4 | 🟡 | Flowchart updated to gate all non-NOW.md file edits behind content approval; rule clarified in INTERACTION.md Section 7. Needs more real-session testing before mitigation can be considered effective | Open |
| RISK-005 | Sunny rubber-stamps approvals without fully reviewing proposed content — undermining the approval model | Medium | Medium | 4 | 🟡 | Claude keeps proposals concise and readable; flags explicitly when a change is high-stakes. Mitigation will be updated if experience shows it isn't working | Open |
| RISK-006 | Scope creep — work expands beyond establishing the interaction basis, pulling the project away from its core mission | Medium | Medium | 4 | 🟡 | Claude checks alignment at natural checkpoints; flags when work seems to diverge from charter goals | Open |
| RISK-007 | Extended inactivity causes NOW.md to go stale and session context to be lost | Medium | Medium | 4 | 🟡 | NOW.md is written to be self-sufficient; Claude re-reads all key docs when context seems stale | Open |

---

*Next available ID: RISK-008*
