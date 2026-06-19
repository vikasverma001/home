# CLAUDE.md

Context for working on this repository. Read this before making changes.

## What this is

The source for **vikasverma.ca** — the personal portfolio of **Vikas Verma**
(Product Manager & Solutions Architect, founder of Vikas Verma Consulting Inc.).
It's a [Hugo](https://gohugo.io) static site. No theme — all layouts are bespoke
and live in `layouts/`.

## Run locally

1. Install Hugo **extended** (the deploy workflow pins `0.153.3`).
2. From the repo root: `hugo server`
3. Open http://localhost:1313

## Deploy (how it goes live)

- Pushing to **`main`** triggers `.github/workflows/hugo.yml`, which builds with
  Hugo and deploys to **GitHub Pages**. A green run = live in a minute or two.
- `/public/` is **git-ignored** and built fresh by Actions on every push. Never
  commit it.
- `static/CNAME` holds `vikasverma.ca`. Squarespace DNS points the domain at
  GitHub Pages. **Do not remove or change `CNAME`.**
- Repo **Settings → Pages → Source** must be **"GitHub Actions"** (not branch deploy).

## Project structure

```
hugo.toml                    # site config + the nav menu (defined ONCE here)
content/
  about.md  experience.md    # "designed" pages: front matter + raw HTML body
  skills.md contact.md
  blog/
    _index.md                # blog landing copy
    *.md                     # one Markdown file per post
  projects/
    _index.md                # projects landing copy
    *.md                     # one file per case study
layouts/
  _default/baseof.html       # page shell: head + pagecss block + nav + main + footer + scripts
  _default/single.html       # about / experience / skills / contact
  index.html                 # home page (own template)
  blog/list.html  blog/single.html
  projects/list.html
  partials/                  # head.html, nav.html, footer.html, scripts.html
static/
  css/main.css               # shared styles + DESIGN TOKENS (:root)
  css/<page>.css             # per-page styles (home, about, experience, skills, blog, case-study, projects, contact)
  img/logo.svg  favicon.svg  # sage-green rounded square, V-chevron "VV" monogram
  img/blog/*.svg  img/certs/*.svg
  CNAME
```

## Key conventions (follow these)

- **Navigation is defined once** in `hugo.toml` under `[[menu.main]]`. Active state
  and the mobile menu are generated automatically by `layouts/partials/nav.html`.
  To add, rename, or reorder nav items, edit `hugo.toml` only — never hardcode nav
  links into a template or page.
- **Per-page CSS**: a content page sets `css = "<name>"` in its front matter, which
  loads `static/css/<name>.css` through the `pagecss` block in `baseof.html`. The
  home page sets its stylesheet inside `layouts/index.html`.
- **Raw HTML in content is allowed** — `markup.goldmark.renderer.unsafe = true` is on,
  which is why the designed pages put bespoke markup directly in their `.md` bodies.
- Keep `baseURL = "https://vikasverma.ca/"`.
- Don't commit `/public/` or `/resources/_gen/`.

## Design tokens

Defined in `:root` at the top of `static/css/main.css`. **Use these variables —
don't hardcode hex values or font names** in new styles.

- **Palette**: creams (`--cream` `#FAF8F5`, `--cream-mid`, `--cream-dark`),
  text/ink (`--ink` `#1A1814`, `--ink-mid`, `--ink-light`),
  sage greens (`--sage` `#4A7C59`, `--sage-light`, `--sage-dark`),
  amber accents (`--amber` `#C8823A`, `--amber-light`), plus `--border`, `--white`.
- **Font**: `--font` is **Inter**, loaded from Google Fonts in `layouts/partials/head.html`.
  (Note: the README still mentions "Plus Jakarta Sans" — that's outdated; the live
  font is Inter.)
- **Shape/spacing**: `--radius-lg` (20px), `--radius-md` (14px), `--radius-sm` (50px),
  `--nav-h` (64px nav height).

## Adding content

**Blog post** — `hugo new blog/<slug>.md`, then fill the front matter and set
`draft = false`. The newest post, or any post with `featured = true`, becomes the
large featured card on `/blog/`. Front matter fields used:

```toml
title    = "..."
date     = 2026-05-15
image    = "/img/blog/<slug>.svg"
category = "..."
tags     = ["...", "..."]
summary  = "..."
readtime = "6 min read"
featured = true   # optional — promotes this post to the featured card
```

**Case study** — add `content/projects/<slug>.md`. Copy an existing one as a
template; front matter is `title`, `description`, `css = "case-study"`, `weight = 0`.
Match the voice and structure of the existing case studies.

## Quick map: task → file

| Task | Where |
|---|---|
| Add / rename / reorder a nav item | `hugo.toml` → `[[menu.main]]` |
| Edit the home page | `layouts/index.html` |
| Edit About / Experience / Skills / Contact copy | the matching `content/*.md` |
| Add a blog post | `hugo new blog/<slug>.md` |
| Add a case study | new `content/projects/<slug>.md` |
| Change colours, fonts, or spacing | tokens in `static/css/main.css` |
| Restyle one page only | that page's `static/css/<name>.css` |
| Adjust the footer | `layouts/partials/footer.html` |
