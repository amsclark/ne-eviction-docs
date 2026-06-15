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

## Hosting (Cloudflare Pages)

Connected to Cloudflare Pages with:

- **Build command:** `pip install -r requirements.txt && mkdocs build`
- **Build output directory:** `site`
- **Environment variable:** `PYTHON_VERSION = 3.12`

Every push to `main` triggers a rebuild and deploy.
