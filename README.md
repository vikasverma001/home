# Vikas Verma — Portfolio (Hugo)

The same 5-page portfolio site, rebuilt as a [Hugo](https://gohugo.io) static site.
Identical design (Plus Jakarta Sans, cream/sage/amber palette) — but the repeated
nav, head, and styles are now defined **once** and the blog is real, editable content.

## What changed vs. the plain-HTML version

| Plain HTML | This Hugo project |
|---|---|
| Nav copy-pasted into every page | Defined once in `hugo.toml` → `[[menu.main]]`; active state is automatic |
| Each file repeated the full `<style>` block | Shared rules in `static/css/main.css`; each page loads only its own extras |
| Blog posts were hardcoded `<div>`s | Markdown files in `content/blog/` that generate the listing automatically |
| Add a post = clone a template file | Add a post = `hugo new blog/my-post.md` |

## Project layout

```
hugo.toml                # site config + navigation menu
content/
  about.md               # designed pages = front matter + their HTML body
  experience.md
  skills.md
  contact.md
  blog/
    _index.md            # blog landing copy
    *.md                 # one file per post (newest shows as "featured")
layouts/
  _default/baseof.html   # the page shell (head + nav + body + scripts)
  _default/single.html   # about/experience/skills/contact
  index.html             # home page
  blog/list.html         # blog index (builds itself from the posts)
  blog/single.html       # a single blog post
  partials/              # head.html, nav.html, scripts.html
static/
  css/*.css              # main.css (shared) + one file per page
  CNAME                  # vikasverma.ca
.github/workflows/hugo.yml   # auto-deploy to GitHub Pages on push to main
```

## Run it locally

1. Install Hugo (extended): https://gohugo.io/installation/
2. From this folder:
   ```
   hugo server
   ```
3. Open http://localhost:1313

## Add a blog post

```
hugo new blog/my-new-post.md
```
Edit the front matter (title, date, category, tags, summary, readtime), write the
body in Markdown, set `draft = false`, and it appears on `/blog/` automatically.
The most recent post (or any post with `featured = true`) becomes the big
featured card at the top.

## Edit a page

The home page lives in `layouts/index.html`. About / Experience / Skills / Contact
are in `content/*.md` — text and structure are right there in each file. Colours,
spacing, and fonts are tokens at the top of `static/css/main.css`.

## Deploy to GitHub Pages

1. Push this repo to GitHub.
2. Repo **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. Push to `main`. The included workflow builds with Hugo and publishes.
4. The `static/CNAME` file keeps `vikasverma.ca` pointed at the site (your
   Squarespace DNS already points the domain at GitHub Pages).

> Note: the included workflow pins Hugo `0.153.3`. Build output (`/public`) is
> git-ignored — GitHub Actions builds it fresh on every push.
