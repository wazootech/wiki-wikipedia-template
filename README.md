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
