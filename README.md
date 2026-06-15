# Nebraska Eviction Scraper — User Guide (public docs)

Public, user-facing documentation for the Nebraska Eviction Scraper, built with
[MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and published via
**Cloudflare Pages**.

> This repo is intentionally **user docs only** — how to sign in, run a scrape,
> schedule, and read the CSV. Operations/deployment docs live privately with the app.

## Local preview

```bash
pip install -r requirements.txt
mkdocs serve         # http://127.0.0.1:8000
```

## Build

```bash
mkdocs build         # outputs the static site to ./site
```

## Hosting (Cloudflare Workers Builds)

Deployed as a static-assets Worker. `wrangler.jsonc` points `assets.directory` at
the MkDocs output (`./site`). In the Cloudflare project's build settings:

- **Build command:** `mkdocs build`  (deps auto-install from `requirements.txt`)
- **Deploy command:** `npx wrangler deploy`

The build runs `mkdocs build` → produces `./site` → `wrangler deploy` uploads it as
static assets. Every push to `main` triggers a rebuild and deploy.
