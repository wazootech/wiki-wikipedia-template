# Wiki Wikipedia Template

A semantic markdown knowledge base with a **Wikipedia-themed layout**, built with the [Wiki CLI](https://github.com/wazootech/wiki).

## Layout

- `wiki.yml` — Wiki configuration, namespace prefixes, and `fmt` defaults.
- `wiki/` — Contains markdown files with semantic frontmatter.
- `assets/` — Static assets (CSS, JS, logo) for the Wikipedia theme.
- `layouts/` — Token-based layout template for the Wikipedia theme.
- `build.py` — Build script using the Wiki Python library.

## Commands

- **Build** (Wikipedia theme):
  ```bash
  python build.py
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
