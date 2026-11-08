# Contributing to AEVO

## Recommended workflow

1. Read `AGENTS.md`, `STATE.md`, and relevant manuscript/ledger files.
2. Open an issue identifying task ID, scope, base commit, intended checks and outputs.
3. Work on a branch named `ai/<provider>-<task-id>-<short-topic>` (e.g. `ai/gemini-T002-citation-audit`); do not push unreviewed changes directly to `main`.
4. Submit a PR that includes a completed `templates/AI_HANDOFF.md` summary and citations.
5. Independent reviewer comments on correctness, traceability, and gaps. Human maintainer accepts or requests changes.
6. After merge, update `STATE.md`, `TASKS.md`, `DECISIONS.md` as applicable; Git history remains the authoritative record of what changed.

## Scientific standards

- Do not create, alter or invent references without verifying them against primary sources.
- Quotes and borrowed content must respect copyright and attribution.
- Preserve the imported baseline under `manuscript/`; a revised paper should be a separate version/file or branch.
- All quantitative assertions require a source or a reproducible calculation and uncertainty note.
- Treat hypotheses and teaching design claims as proposals until empirically validated.
- Note source access restrictions (paywalls, inaccessible materials) and the resulting verification gaps.
- Make negative results and rejected suggestions traceable rather than erasing them.

## Security and copyright

Do not upload secrets, account data, confidential reviews, copyrighted full texts without permission, research-participant data or identifying student records. This is a private unpublished project, not an open-license invitation.
