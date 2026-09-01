# savant-share: PUBLIC Publishing Boundary

This repository is PUBLIC. Everything committed here, including full git history, is world-readable. GitHub Pages deploys from `main` branch, `/docs` folder.

## Hard rules
- Nothing enters `docs/` without intentional publishing approval (an approved green-light ID).
- Plaintext sensitive client material is PROHIBITED: revenue, spend, ROAS, conversion metrics, private dashboards, strategy, proposals, pricing, internal reports, competitive intelligence, private datasets, internal notes.
- Secrets are PROHIBITED. Never commit `.env` or any credential. Never expose tokens or keys in HTML, JS, comments, or commit messages.
- Future encrypted deliverables arrive here as ENCRYPTED OUTPUT ONLY. Plaintext source stays in the private workspace. Committing plaintext "because the deployed copy is encrypted" exposes it through GitHub itself.
- Do not publish private client metrics or data unless explicitly approved for public release, or encrypted under the (future) encryption system.
- History is forever: a bad commit to a public repo is a disclosure event, not an undo.
- **This is a delivery surface, never a discovery surface.** Nothing published here is an SEO, marketing, or discovery asset, and no page is ever optimised to be found.
- **`docs/robots.txt` always carries an all-agents, all-paths disallow.** It is not removed, narrowed, or given exceptions. A page that needs to be found does not belong in this repo.
- **Every page ships `noindex,nofollow`.** The encrypted-publishing shell in `savant-workspace/publishing/encrypt_page.js` emits `noindex,nofollow,noarchive` plus `referrer: no-referrer` by default, and a test enforces it. A page added here by any other route carries the same tags or it is not added.
- **Crawler blocking is the outermost of three layers, never the one doing the work.** `robots.txt` is a request that well-behaved crawlers honour and everything else ignores; the meta tags are the same. **The actual control is that every deliverable is AES-256-GCM encrypted before it enters this repo.** Never let a crawler directive substitute for encryption.

## Structure
- `docs/` the deployed tree (Pages serves this as the site root)
  - `reports/` `dashboards/` `presentations/` plus other content types as needed
