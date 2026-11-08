# Instructions for every AI collaborator

**Identity:** AEVO = Architect, Execute, Verify, Own. Repository file names and project title are canonical. Do not perpetuate the AVEO typo.

## Onboarding (mandatory)

1. Read `README.md`, `STATE.md`, `TASKS.md`, `DECISIONS.md`, `CONTRIBUTING.md`, and the relevant canonical manuscript.
2. State your AI provider/model/version if known, date, repository branch/commit SHA, scope, task ID, and inputs inspected.
3. Work from repository artifacts, not unverified recollections from a different chat/account. Request missing artifacts rather than guessing.
4. Submit analysis as a branch/PR or an issue with a change proposal. Never mark a task accepted, verified, or merged without evidence.
5. Update the evidence ledger or provide row changes with exact source identity, DOI/URL, publication year, claim, verification method, and limitations.
6. Require independent verification for scientific, statistical, numerical, ethical, or high-impact claims. Record negative findings and unresolved questions.
7. Ask human maintainer to approve any change of scientific thesis, authorship, sharing/access, journal target, or publication status.

## Contribution log fields

- ID; timestamp (UTC); AI account alias, provider and model; task/issue; base commit SHA; work performed; files read/changed; references used; validation/tests performed and results; unresolved concerns; PR/commit URL; human decision.
- If no code or repository access, paste the above in your response and provide a unified diff or complete proposed file.
- Do not claim AI contributions were reviewed by another model unless another reviewer actually inspected the work.

## Verification standard

- **Source fidelity:** original claims attributable to actual readable papers; citation not merely plausible.
- **Technical checks:** unit consistency, conservation constraints, sensitivity/identifiability, code execution, tests, independent calculations where relevant.
- **Epistemic labels:** `verified`, `partially checked`, `unverified`, `proposed`, `disputed`.
- **No silent deletions:** when superseding a claim, preserve its ID and record why.

## Privacy/security

Never commit API keys, passwords, institutional restricted data, unpublished third-party material without permission, identifiable student records, confidential peer reviews, or personal account information. Avoid embedding full chat transcripts. Keep the repository private unless the human maintainer authorizes release.

## Manuscript distinction

The environmental modelling perspective is not equivalent to a dedicated AEVO pedagogical paper. Do not conflate their statuses or infer outcomes of teaching experiments that have not been run.
