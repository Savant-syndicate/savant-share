# savant-share: PUBLIC Publishing Boundary

This repository is PUBLIC. Everything committed here, including full git history, is world-readable. GitHub Pages deploys from `main` branch, `/docs` folder.

## Hard rules
- Nothing enters `docs/` without intentional publishing approval (an approved green-light ID).
- Plaintext sensitive client material is PROHIBITED: revenue, spend, ROAS, conversion metrics, private dashboards, strategy, proposals, pricing, internal reports, competitive intelligence, private datasets, internal notes.
- Secrets are PROHIBITED. Never commit `.env` or any credential. Never expose tokens or keys in HTML, JS, comments, or commit messages.
- Future encrypted deliverables arrive here as ENCRYPTED OUTPUT ONLY. Plaintext source stays in the private workspace. Committing plaintext "because the deployed copy is encrypted" exposes it through GitHub itself.
- Do not publish private client metrics or data unless explicitly approved for public release, or encrypted under the (future) encryption system.
- History is forever: a bad commit to a public repo is a disclosure event, not an undo.

## Structure
- `docs/` the deployed tree (Pages serves this as the site root)
  - `reports/` `dashboards/` `presentations/` plus other content types as needed
