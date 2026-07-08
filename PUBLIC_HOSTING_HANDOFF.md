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

- `www.principiaresearch.ie` serves this RnD org Pages repo, but DNS still has `www CNAME BoredDuffa.github.io`. To remove Benjamin's personal GitHub namespace from DNS, change it to `www CNAME rndprincipiacapital.github.io`.
- `principiaresearch.ie` root already points at GitHub Pages IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, and `185.199.111.153`.
- `principiacapital.ie` currently needs DNS/admin changes before it can point to GitHub Pages.
- Firebase `web.app` hosts cannot be transferred by Git alone; ownership must be transferred inside Firebase/Google Cloud or replaced by the static mirrors above.
- Cloud Run Gold frontend/backend cannot be moved to GitHub Pages as a live backend. They require Google Cloud ownership, billing, provider credentials, and deployment access. The GitHub Pages mirror only preserves public static data/docs.

## Exact DNS Records For Full Personal-GitHub Removal

For `principiaresearch.ie`:

- Root/apex `A` records:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- `www` CNAME:
  - change from `BoredDuffa.github.io`
  - to `rndprincipiacapital.github.io`

For `principiacapital.ie`, if Dillon wants the exact corporate domain on free GitHub Pages:

- Create an org-owned public repo, for example `RnDprincipiacapital/principia-capital-pages`.
- Copy the clean static corporate site files into that repo.
- Add a `CNAME` file containing `principiacapital.ie`.
- Enable GitHub Pages from `main` and `/`.
- Set DNS:
  - root/apex `A` records to GitHub Pages IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
  - `www` CNAME to `rndprincipiacapital.github.io`
  - remove the current Firebase CNAME `principia-capital.web.app` from `www` after the Pages custom domain is ready

I attempted to create `RnDprincipiacapital/principia-capital-pages` from the current GitHub token, but GitHub denied it: `BoredDuffa cannot create a repository for RnDprincipiacapital`. An org owner must create that repo or grant the needed permission.
