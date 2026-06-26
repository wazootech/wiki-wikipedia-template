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
