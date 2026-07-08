# Public Hosting Handoff

This repository is the current free, org-owned GitHub Pages surface for public Principia sites and static mirrors.

## Already Fully On Free Org Hosting

- Principia Research: `https://www.principiaresearch.ie/`
- SME Dual Engine public site: `https://rndprincipiacapital.github.io/sme-dual-engine-public/`

## Static Mirrors Added Here

Base URL after GitHub Pages rebuild:

`https://www.principiaresearch.ie/public-sites/`

Mirrors:

- Corporate site: `/public-sites/principia-capital/`
- Real Estate dashboard: `/public-sites/real-estate/`
- House dashboard: `/public-sites/house/`
- Galway SME dashboard: `/public-sites/galway-sme/`
- Gold static evidence/data: `/public-sites/gold/`

## What Still Requires Account/DNS Ownership

- `principiacapital.ie` currently needs DNS/admin changes before it can point to GitHub Pages.
- Firebase `web.app` hosts cannot be transferred by Git alone; ownership must be transferred inside Firebase/Google Cloud or replaced by the static mirrors above.
- Cloud Run Gold frontend/backend cannot be moved to GitHub Pages as a live backend. They require Google Cloud ownership, billing, provider credentials, and deployment access. The GitHub Pages mirror only preserves public static data/docs.
