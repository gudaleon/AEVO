# AEVO — Architect · Execute · Verify · Own

**Collaborative research and teaching framework** for human-led, AI-assisted scientific work.

**Status:** Private research workspace. The GitHub repository was initially named `AVEO` by mistake; **AEVO** is the correct name. Rename the repository in **Settings → General → Repository name** to `AEVO` (the installed connector cannot rename repositories).

## The framework

| Stage | Principal purpose | Accountability |
| --- | --- | --- |
| **Architect** | Define research question, scope, conceptual model, assumptions, acceptance criteria and verification plan | Human-led |
| **Execute** | Collect evidence, develop analyses/code, run models, draft outputs | Human and AI tools |
| **Verify** | Independently test claims, code, citations, uncertainty, logic and replicability | Human-led with AI cross-review |
| **Own** | Make and document decisions, limitations, corrections, publication responsibility | Human only |

**Canonical source manuscript:** [From Running Models to Orchestrating Science](manuscript/Neumann_AEVO_Orchestrating_Environmental_Modelling_DRAFT.md) (imported without editorial changes, September 2026 baseline). This is an **unpublished position-paper draft**; its Section 7 briefly introduces AEVO as an educational corollary. The full teaching framework is a **separate proposed workstream**, not an established validated intervention.

## Cross-account AI collaboration

Each AI account (ChatGPT, Claude, Gemini, Grok, Cursor, or another system) should treat this repository as the **shared record**, not its chat history. Read [AGENTS.md](AGENTS.md), [STATE.md](STATE.md), [TASKS.md](TASKS.md), [DECISIONS.md](DECISIONS.md), [CONTRIBUTING.md](CONTRIBUTING.md) and the manuscript before working. Use issues to propose work, branches/PRs for changes, and the [handoff template](templates/AI_HANDOFF.md) for provenance.

- **No silent overwrites.** Keep the original imported manuscript intact; edit a new working file/branch.
- **No fabricated evidence.** Preserve citations and source links; distinguish peer-reviewed results, preprints, proposals, and hypotheses.
- **No unverified publication claims.** Use explicit status labels.
- **Human sign-off.** AI accounts can propose and review; the human author accepts, rejects, and merges.
- **Security/privacy.** Do not commit tokens, confidential manuscripts/reviews, personal student data, private files without permission, or proprietary material without sharing rights.

## Repository map

- `manuscript/` — source draft
- `teaching/` — distinct pedagogy paper workstream
- `STATE.md` — current reproducible status and references
- `TASKS.md` — prioritized backlog and owners
- `DECISIONS.md` — human decisions and reasoning
- `EVIDENCE_LEDGER.csv` — claim/source/verification tracking
- `AGENTS.md` — cross-model operating rules
- `templates/AI_HANDOFF.md` — portable task handoff

**Maintainer:** Alex Neumann. Private, unpublished working materials; no distribution licence is granted by default.
