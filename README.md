# Studio 51 — Wireframe Design System

The reusable, brand-neutral design system Studio 51 (Team 51 at Automattic) uses as the baseline for partner wireframes and prototypes. Copy the tokens, build your wireframe, then override colours and fonts with the partner's brand during visual design.

This is the system behind the Locus Magazine prototypes, extracted back to its neutral baseline so any project can start from it.

## What's here

| File | What it is |
|------|-----------|
| [`styleguide.html`](styleguide.html) | **Live styleguide.** Open in a browser to see every token and component rendered — colours, type scale, spacing, radius, buttons, inputs, tags, cards, nav, breadcrumbs, responsive rules. |
| [`tokens.css`](tokens.css) | **Drop-in token layer.** All design tokens as CSS custom properties. Link it, then build on top. |
| [`design-system.md`](design-system.md) | **Full written spec.** Every rule, value, and usage note — the source of truth. |

## Quick start

1. Open `styleguide.html` in a browser to get oriented.
2. Copy `tokens.css` into your prototype and link it:
   ```html
   <link rel="stylesheet" href="tokens.css">
   ```
3. Build your wireframe using the tokens (`var(--black)`, `var(--gap-lg)`, `var(--radius-full)`, …).
4. During visual design, override the colour and font tokens with the partner's brand. Keep the spacing, radius, and responsive scales unless there's a strong reason not to.

## Principles

- **Neutrals only in wireframes.** No accent colours — partner brand colours come in during design.
- **Editorial headings, readable body.** Headings at tight 100% line-height; body at a generous 141%.
- **Full-pill buttons, square-ish cards.** Consistent component language across projects.
- **Fully responsive, 375px → 1440px.** No `max-width` on `body`; no horizontal scroll at 375px, ever. Type and page spacing scale fluidly via `clamp()`.
- **Maps 1:1 to WordPress.** Every token translates directly to block-theme `theme.json`: typography presets, colour palette, spacing scale, layout widths.

## Fonts

The styleguide loads **Inter** from Google Fonts. Swap the primary and brand font tokens in `tokens.css` per partner.

---

Maintained by Studio 51. Questions → Diana.
