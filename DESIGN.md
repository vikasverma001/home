# vikasverma.ca — Design System

The single source of truth for how this site looks and behaves. If you're
about to make a visual decision and it's already answered here, follow the
doc instead of re-deciding. If it's a *new* decision, make it here first,
then build it — that's what keeps the site coherent as it grows.

**Layers, bottom to top:** Tokens → Components → Patterns → Principles.
Tokens live in [`tokens.css`](./tokens.css). This document covers the rest.

> **Status of values:** the palette and fonts in `tokens.css` are a deliberate
> sage/cream starting point, not yet reconciled against the live CSS. Verify
> them once with dev tools (inspect → Computed/Styles) and overwrite any value
> that differs — keep the variable *names*. After that, this doc is canonical.

---

## 1. Principles

The "why" behind every other decision. When two solutions both work, the one
that honors these wins.

1. **Calm and editorial.** Sage and cream do the talking. Whitespace is a
   feature, not wasted space. The page should feel like a well-set magazine
   spread, not a dashboard.
2. **One action per moment.** At most one primary (filled sage) button in any
   view. Everything else is secondary or a text link. This is what makes the
   "Work with me" / "Get in touch" CTAs actually pull.
3. **Restraint over decoration.** No shadow where a border will do; no border
   where space will do. Reach for the lightest tool that reads clearly.
4. **The token is the source.** Never type a raw hex, px font size, or
   arbitrary margin into a component. If a value isn't in `tokens.css`, either
   it belongs there or you don't need it.
5. **Stay solo-sized.** This is a one-person site. Don't build the 50-component
   library a product team needs. Enough structure to stop deciding the same
   thing twice — and no more.

---

## 2. Foundations

### Color

Tokens are named by **role**, not hue, so a palette change never means a
rename. Full list in `tokens.css §1`.

| Role | Token | Use it for |
|---|---|---|
| Page background | `--color-bg` | The cream base behind everything |
| Surface | `--color-surface` | Cards, raised panels |
| Surface (alt) | `--color-surface-alt` | Alternating section bands |
| Primary text | `--color-ink` | Body and headings |
| Muted text | `--color-ink-muted` | Metadata, captions, dates |
| Primary action | `--color-primary` | Filled buttons, link emphasis |
| Action hover | `--color-primary-hover` | Hover/active of the above |
| Soft tint | `--color-primary-soft` | Chip backgrounds, hover fills |
| Brand sage | `--color-sage` | Logo-family accents, borders — **not** behind white text |
| Border | `--color-border` | Hairlines, card edges |

**Contrast rule:** body text must hit WCAG AA (4.5:1) against its background.
`--color-primary` is intentionally dark enough to carry white text; the
lighter `--color-sage` is **not** — use it for accents, never as a text
background. When in doubt, check the pair in a contrast tool before shipping.

### Typography

A 1.25 (major-third) scale on a 16px base. Two families: a **serif** for
display headings (your italic "I build great products" voice) and a **sans**
for body and UI. See `tokens.css §2`.

| Element | Token | Family | Weight | Leading |
|---|---|---|---|---|
| Hero H1 | `--text-4xl` | serif | 600 | tight |
| Section header | `--text-3xl` | serif | 600 | tight |
| H2 | `--text-2xl` | serif | 600 | snug |
| H3 / card title | `--text-xl` | sans | 600 | snug |
| Lead paragraph | `--text-lg` | sans | 400 | normal |
| Body | `--text-base` | sans | 400 | normal |
| Metadata / caption | `--text-sm` | sans | 500 | snug |
| Eyebrow / kicker | `--text-xs` | sans | 600 + `--tracking-wide`, uppercase | — |

**Rules:** never more than two heading sizes visible competing in one section.
Cap prose at `--measure` (68ch) so lines stay readable. The all-caps eyebrow
("WHAT I DO", "CREDENTIALS", "SELECTED WORK") always uses `--tracking-wide`.

### Spacing

One 4px-based scale (`tokens.css §3`). Margins, padding, and gaps all pull
from it — nothing hand-typed. Section bands use `--section-pad-y` top and
bottom so vertical rhythm is identical everywhere.

Rough guide: `--space-2/3` inside small elements, `--space-4/5` between
related items, `--space-8/10` between subsections, `--space-16` between major
page sections.

### Shape & elevation

Radius: `--radius-md` for cards, `--radius-full` for chips/pills. Shadows are
low-opacity and ink-tinted (warm, not gray) — `--shadow-sm` for resting cards,
`--shadow-md` on hover. Prefer a `--color-border` hairline to a shadow when
the card sits on the cream band.

### Layout & breakpoints

`--container-max` (1200px) for full width, `--content-max` (672px) for prose.
Breakpoints can't be CSS variables, so they're fixed here — use these exact
values in your media queries:

| Name | Min width | Notes |
|---|---|---|
| `sm` | 480px | large phone |
| `md` | 768px | tablet — collapse desktop nav to mobile nav here |
| `lg` | 1024px | small laptop |
| `xl` | 1200px | container max reached |

---

## 3. Components

Every reusable piece on the site, each one assembled *from* tokens. Build each
as a single Hugo partial or shortcode so it's defined once and reused. The
inventory below is taken from what's actually live on the site today.

### Logo / monogram
The layered **VV** monogram in sage/cream. Lives in `partials/logo.html` as
inline SVG (so it inherits `currentColor` and scales crisply). Fill from
`--color-sage`; never rasterize it into a PNG.

### Navigation
Driven by Hugo's menu config, rendered in `partials/header.html`.
- **Desktop:** horizontal links, `--text-sm`, `--color-ink-muted`, active page
  in `--color-ink`. Hover → `--color-primary`.
- **Mobile (< `md`):** collapses to the icon nav. Same menu data source —
  never maintain two link lists.

### Buttons
Two variants, no more.
- **Primary** — `background: var(--color-primary)`, white text, `--radius-md`,
  hover → `--color-primary-hover`. Used for *the* action ("Work with me",
  "Get in touch"). Max one per view (Principle 2).
- **Secondary** — transparent background, `1px var(--color-border)`,
  `--color-ink` text. Hover → `--color-primary-soft` fill. ("Read my blog".)

```css
.btn { font: var(--weight-semibold) var(--text-base)/1 var(--font-sans);
       padding: var(--space-3) var(--space-5); border-radius: var(--radius-md);
       transition: background var(--transition), border-color var(--transition); }
.btn--primary   { background: var(--color-primary); color: #fff; border: none; }
.btn--primary:hover { background: var(--color-primary-hover); }
.btn--secondary { background: transparent; color: var(--color-ink);
                  border: var(--border-width) solid var(--color-border); }
.btn--secondary:hover { background: var(--color-primary-soft); }
```

### Eyebrow / section kicker
The small uppercase label above each section header ("WHAT I DO",
"CREDENTIALS"). `--text-xs`, `--weight-semibold`, `--tracking-wide`,
`--color-primary`, uppercase.

### Section header
The serif headline that follows the eyebrow ("Four things I spend my time on").
`--text-3xl`, serif, `--color-ink`, `--leading-tight`.

### Stat / counter
The hero figures (20+, 30, 6, 11). Big serif number in `--text-3xl`/`4xl`
`--color-primary`, with a `--text-sm` `--color-ink-muted` label beneath. Lay
out as an even grid; gap `--space-6`.

### Feature card  *(the "What I do" cards)*
Emoji/icon, then `--text-xl` H3 title, then `--text-base` `--color-ink-muted`
body. `--color-surface`, `--radius-md`, `--shadow-sm`, padding `--space-6`.
Hover lifts to `--shadow-md`. Four across at `lg`, two at `md`, one below.

### Chip / tag  *(certifications & industries)*
Pill for the cert list ("PSM I", "Salesforce Advanced Admin") and the industry
row. `--radius-full`, `--color-primary-soft` background, `--color-ink` text,
`--text-sm`, padding `--space-2 --space-4`. Non-interactive — these are labels,
not buttons, so no hover state.

### Project card  *(Selected work)*
Category label (`--text-xs` eyebrow), title (`--text-lg`), one-line result with
the metric ("−38% handle time") emphasized in `--color-primary`. Whole card is
a link to `/projects/`. Border `--color-border`, hover → `--shadow-md`.

### Blog card
Category eyebrow, `--text-lg` title, `--text-base` `--color-ink-muted` excerpt,
then a `--text-sm` meta line (date · read time) in `--color-ink-subtle`. Links
to the post.

### CTA band
Full-width `--color-surface-alt` (or sage) band with a serif headline and one
primary button. The site's recurring "Let's talk" / "Get in touch" closer.
Padding `--section-pad-y`.

### Footer
Three zones in `partials/footer.html`: brand blurb (name + one-line
positioning + "Vikas Verma Consulting Inc. · Brampton, Ontario"), an **Explore**
column, and a **Connect** column — both rendered from Hugo menus, not
hand-listed. Copyright row at the bottom, `--text-sm` `--color-ink-muted`.

---

## 4. Patterns

How components combine into pages. Conventions, not code.

- **Section rhythm.** Every content section = eyebrow → section header →
  content, wrapped in a band with `--section-pad-y` top/bottom. Alternate
  `--color-bg` and `--color-surface-alt` backgrounds down the page so sections
  separate without hard rules.
- **Home page.** Hero (eyebrow + serif H1 + lead + two buttons + stat row) →
  "What I do" (feature cards) → Credentials (chips) → Industries (chips) →
  Selected work (project cards) → From the blog (blog cards) → CTA band →
  footer.
- **Blog post.** Constrain body to `--content-max`. H1 in serif `--text-3xl`,
  meta line beneath, prose at `--text-base`/`--leading-normal` capped at
  `--measure`. One H2/H3 hierarchy only.
- **Project page.** Lead with the problem, show the metric prominently (reuse
  the stat-counter treatment), then context. Consistency with the home-page
  project cards matters more than novelty.

---

## 5. Governance (solo edition)

Lightweight on purpose.

- **Adding a component:** check it isn't a variant of something here first
  (most "new" needs are an existing component with different content). If it's
  genuinely new, add it as one partial, document it in §3, and only introduce
  new tokens if the value will be reused.
- **Adding a token:** a value earns a token when it appears 3+ times or names a
  real concept. One-off values don't need one.
- **Changing a value:** edit `tokens.css` only. If you find yourself editing a
  hex or size in a component file, that's a signal it should have been a token.
- **The over-build smell:** if you're writing documentation for a component you
  haven't actually used on a page yet, stop. Build first, document the real
  thing.

---

## 6. Changelog

Keep a one-line note per meaningful change so future-you knows what moved.

- `2026-06-24` — Initial design system: tokens, principles, component
  inventory derived from the live site.
