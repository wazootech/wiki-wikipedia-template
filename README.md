# Wiki Wikipedia Template

A semantic markdown knowledge base with a **Wikipedia-themed layout**, powered by the [Wiki CLI](https://github.com/wazootech/wiki).

## Layout

- `wiki.yml` — Wiki configuration, namespace prefixes, and `fmt` defaults.
- `wiki/` — Contains markdown files with semantic frontmatter.
- `assets/` — Static assets (CSS, logo) for the Wikipedia theme.
- `layouts/` — Jinja2 template for the Wikipedia-themed layout.
- `build.py` — Custom build script using the Wiki Python API.

## Commands

- **Build** (Wikipedia theme):
  ```bash
  python build.py
  ```
- **Build** (minimal default layout):
  ```bash
  wiki build
  ```
- **Preview** (starts a local dev server):
  ```bash
  wiki serve
  ```
- **Check** (integrity: SHACL, JSON Schema, route safety):
  ```bash
  wiki check
  ```
- **Lint** (conventions: broken links, filename pattern, heading style):
  ```bash
  wiki lint
  ```

The Wikipedia-themed build output goes to `_site/`.

## Deployment

This wiki builds to a static site. Any provider that serves static files works.

### GitHub Pages (preferred)

1. Go to **Settings &rarr; Pages &rarr; Source: GitHub Actions**
2. Push to the default branch &mdash; the \.github/workflows/deploy-pages.yml\ workflow builds and deploys automatically
3. Your site appears at \https://{org}.github.io/{repo}/\

### Vercel

1. Import this repo at [vercel.com/new](https://vercel.com/new)
2. **Build command:** \pip install wazootech-wiki && wiki build --output-dir .vercel/output --site-base-url /\
3. **Output directory:** \.vercel/output\
4. Deploy

### Netlify

1. Import this repo at [app.netlify.com/start](https://app.netlify.com/start)
2. **Build command:** \pip install wazootech-wiki && wiki build --output-dir _site --site-base-url /\
3. **Publish directory:** \_site\
4. Deploy

### Cloudflare Pages

1. Import this repo in the Cloudflare dashboard
2. **Build command:** \pip install wazootech-wiki && wiki build --output-dir _site --site-base-url /\
3. **Output directory:** \_site\
4. Deploy
