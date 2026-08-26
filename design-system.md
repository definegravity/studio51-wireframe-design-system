# Studio 51 Wireframe Design System

Extracted from the ADCE Redesign wireframes. Use as a reusable baseline for all partner projects, then override with partner-specific brand tokens (colours, fonts) as needed.

---

## Typography

### Font Stack

| Role | Family | Fallback |
|------|--------|----------|
| Primary | Inter Variable | sans-serif |
| Brand/Logo | Akzidenz-Grotesk BQ | sans-serif |

### Type Scale

| Token | Size | Weight | Style | Line Height | Use |
|-------|------|--------|-------|-------------|-----|
| `heading-1` | 56px | 600 | SemiBold | 100% | Page titles |
| `heading-2` | 40px | 600 | SemiBold | 100% | Section headings |
| `heading-3` | 32px | 500 | Medium | 100% | Footer section titles, sub-sections |
| `heading-4` | 28px | 500 | Medium | 100% | Card titles |
| `heading-5` | 22px | 600 | SemiBold | 100% | Subtitles, sidebar headings |
| `heading-6` | 16px | 600 | SemiBold | 100% | Button text, nav links, overlines, footer category labels |
| `body` | 16px | 400 | Regular | 1.41 (141%) | Paragraph text, descriptions, breadcrumbs |
| `body-large` | 18px | 400 | Regular | 26px | Footer address/contact |
| `small` | 14px | 400 | Regular | 26px | Legal text, copyright |

### Typography Rules

- **Headings** use tight line-height (100%) for a compact, editorial feel.
- **Body text** uses a generous 141% line-height for readability.
- **Overline/category labels** (e.g. footer section headers) use `heading-6` in uppercase with muted colour (`grey-500`).
- **Navigation links** use `heading-6` weight (SemiBold) at body size.
- **Letter spacing** is 0 across all styles; do not add tracking.

---

## Colour Palette

### Neutrals

| Token | Hex | Use |
|-------|-----|-----|
| `white` | `#FFFFFF` | Page backgrounds, button text on dark, input backgrounds |
| `grey-50` | `#F2F4F8` | Alternate section backgrounds, breadcrumb bar |
| `grey-100` | `#F3F3F3` | Active nav item background |
| `grey-200` | `#E4E4E4` | Footer body text on dark backgrounds |
| `grey-300` | `#DFE4EA` | Image placeholder backgrounds, tag borders, divider lines |
| `grey-400` | `#BCC1CB` | Image placeholder borders, secondary borders |
| `grey-500` | `#5C5E65` | Muted text (footer category labels on dark bg) |
| `black` | `#25282D` | Primary text, primary button fills, dark section backgrounds |

### Colour Usage Rules

1. **Alternating section backgrounds**: Sections alternate between `white` and `grey-50` to create visual rhythm without colour.
2. **Dark sections**: Footer and mega-footer use `black` (`#25282D`) as background.
3. **Text on light backgrounds**: Always `black` (`#25282D`).
4. **Text on dark backgrounds**: `white` for primary text, `grey-200` (`#E4E4E4`) for secondary/address text, `grey-500` (`#5C5E65`) for muted labels.
5. **Borders on light backgrounds**: `black` for interactive elements (buttons, inputs), `grey-300`/`grey-400` for decorative borders.
6. **No accent colours in wireframes**: Partner brand colours replace or extend this palette during the design phase.

---

## Spacing

### Page-Level Spacing

| Token | Value | Use |
|-------|-------|-----|
| `page-gutter` | `clamp(20px, 2.75vw + 10px, 64px)` | Horizontal padding on all sections |
| `section-padding` | `clamp(48px, 2vw + 40px, 80px)` | Vertical padding for content sections |
| `grid-gutter` | `clamp(16px, 1vw + 12px, 32px)` | Gap between cards/columns |
| `breadcrumb-padding-y` | 16px | Vertical padding for breadcrumb bar |

### Content Spacing

| Token | Value | Use |
|-------|-------|-----|
| `gap-xs` | 8px | Inline icon gaps, tight element spacing |
| `gap-sm` | 16px | Card internal gaps, button rows, stacked form fields, footer link lists |
| `gap-md` | 24px | Form field groups, tag-to-title spacing, newsletter form internal |
| `gap-lg` | 32px | Card grid gaps, column gaps, footer column gaps |
| `gap-xl` | 48px | Title-to-content gap within sections, sidebar internal |
| `gap-2xl` | 56px | Footer major section gaps |
| `gap-3xl` | 64px | Large card grids (2-col layout row gap) |
| `gap-4xl` | 72px | Footer top-level section gaps |
| `gap-5xl` | 88px | Content block-to-block within long-form pages |

### Spacing Rules

- **Section title to content**: Use `gap-xl` (48px) between a section heading and its first child content.
- **Section title to "View all" button**: These sit on the same row, separated by `justify-between`.
- **Card grids**: Use `gap-lg` (32px) between cards in both row and column directions.
- **Form fields**: Stack with `gap-md` (24px) between rows; side-by-side fields use `gap-lg` (32px).

---

## Layout

### Grid System

| Layout | Columns | Column Width | Gap | Total Content Width |
|--------|---------|-------------|-----|-------------------|
| Page max | - | 1440px | - | Max viewport; body centred beyond this |
| Content area | - | 1344px | - | 1440px minus 2 x 48px gutter |
| 3-column cards | 3 | 427px | 32px | 1344px |
| 2-column cards | 2 | 656px | 32px | 1344px |
| Content + sidebar | ~60/40 | 771px / 427px | flexible | 1344px |

### Layout Rules

1. **Content width**: Always 1344px (page width minus gutters). Never full-bleed text.
2. **Section backgrounds**: Full-bleed to 1440px; content within is constrained by gutters.
3. **Alternating backgrounds**: Odd sections white, even sections `grey-50` (or vice versa). Maintain the rhythm.
4. **Footer columns**: 6 equal columns at 197px each with 32px gaps.

---

## Components

### Buttons

| Variant | Background | Border | Text Colour | Radius | Padding |
|---------|-----------|--------|------------|--------|---------|
| Primary | `black` | none | `white` | 80px | 24px / 12px |
| Secondary | transparent | 1px `black` | `black` | 80px | 24px / 12px |
| Inverted (on dark) | `white` | none | `black` | 80px | 24px / 12px |

- **Text**: `heading-6` (16px SemiBold)
- **Shape**: Full pill (border-radius 80px)
- **With icon**: Add 10px gap between label and icon; reduce right padding to 18px
- **Active state** (e.g. filter pills): Primary fills; inactive uses Secondary

### Input Fields

| Property | Value |
|----------|-------|
| Height | 43px |
| Border | 1px solid `black` (light bg) or `white` (dark bg) |
| Border radius | 32px |
| Padding | 24px horizontal, 4px vertical |
| Placeholder text | `body` style (16px Regular) |

### Tags

| Property | Value |
|----------|-------|
| Background | `white` |
| Border | 1px solid `grey-300` |
| Border radius | 8px |
| Padding | 12px / 8px |
| Text | `heading-6` (16px SemiBold) |

### Cards

#### Blog Card (3-column)

| Property | Value |
|----------|-------|
| Width | 427px (fills column) |
| Image height | 239px |
| Image border radius | 0 (square) |
| Title | `heading-4` (28px Medium) |
| Description | `body` (16px Regular) |
| Internal gap | `gap-sm` (16px) |

#### Programme Card (2-column)

| Property | Value |
|----------|-------|
| Width | 656px (fills column) |
| Image height | 356px |
| Title | `heading-4` (28px Medium) |
| Description | `body` (16px Regular) |
| Internal gap | `gap-sm` (16px) |

### Image Placeholders

| Property | Value |
|----------|-------|
| Background | `grey-300` |
| Border | 1px solid `grey-400` |
| Border radius | 8px |

### Breadcrumbs

| Property | Value |
|----------|-------|
| Background | `grey-50` |
| Padding | 16px vertical, 48px horizontal |
| Text | `body` (16px Regular), colour `black` |
| Separator | " / " (space-slash-space) |

### Navigation Bar

| Property | Value |
|----------|-------|
| Background | `white` |
| Padding | 24px vertical, 48px horizontal |
| Logo | Akzidenz-Grotesk BQ Bold, 28px, uppercase |
| Nav links | `heading-6` (16px SemiBold) with chevron icon |
| Active nav item | `grey-100` background, 8px border-radius |
| CTA buttons | Primary and Secondary variants |

---

## Border Radius Scale

| Token | Value | Use |
|-------|-------|-----|
| `radius-sm` | 8px | Tags, nav active states, image placeholders |
| `radius-md` | 16px | Page frame containers |
| `radius-lg` | 32px | Input fields |
| `radius-full` | 80px | Buttons (pill shape) |

---

## Shadows & Effects

None in wireframes. These are introduced during the visual design phase.

---

## Responsive Framework

All Studio 51 prototypes and wireframes must be fully responsive between 375px and 1440px viewports.

### Viewport Constraints

| Token | Value | Rule |
|-------|-------|------|
| `viewport-max` | 1440px | Content and backgrounds cap here. Body centred beyond this width. |
| `viewport-min` | 375px | Minimum supported width. Nothing should overflow or break below this. |

**Enforcement:** Do NOT set `max-width` on `body`. Section backgrounds must stretch edge-to-edge on viewports wider than 1440px. Each section is responsible for its own inner width constraint via container elements (`max-width: 1440px; margin: 0 auto`). No horizontal scroll should appear at 375px.

### Breakpoints

| Name | Width | Trigger |
|------|-------|---------|
| `desktop` | 1440px -- 1025px | Full grid, full nav, full gutters |
| `tablet` | 1024px -- 769px | Reduced grid columns, condensed nav |
| `mobile` | 768px -- 375px | Single column, hamburger nav, reduced spacing |

Write media queries as `max-width` (desktop-first) to match WordPress block theme conventions:

```css
/* Tablet */
@media (max-width: 1024px) { ... }
/* Mobile */
@media (max-width: 768px) { ... }
```

### Responsive Spacing (Fluid)

Layout spacing scales fluidly using `clamp()` between 375px and 1440px viewports. No stepped breakpoints needed.

| Token | Min (375px) | Max (1440px) | CSS |
|-------|-------------|-------------|-----|
| `page-gutter` | 20px | 64px | `clamp(20px, 2.75vw + 10px, 64px)` |
| `section-padding` | 48px | 80px | `clamp(48px, 2vw + 40px, 80px)` |
| `grid-gutter` | 16px | 32px | `clamp(16px, 1vw + 12px, 32px)` |

**Rules:**
- All section vertical padding uses `var(--section-padding)` -- never hardcode 80px or 48px
- All horizontal padding on full-bleed sections uses `var(--page-gutter)` -- never hardcode 64px or 20px
- `.hp-container` uses `var(--page-gutter)` for its horizontal padding
- Ad blocks use 32px vertical padding (fixed, not fluid -- ads have fixed dimensions)
- The promo banner uses 16px vertical padding (compact, not a content section)

### Responsive Typography (Fluid)

Typography scales fluidly using `clamp()` between 375px and 1440px viewports. No stepped breakpoints needed for type -- it interpolates smoothly.

| Token | Min (375px) | Max (1440px) | CSS |
|-------|-------------|-------------|-----|
| `heading-1` | 32px | 56px | `clamp(32px, 1.5vw + 26px, 56px)` |
| `heading-2` | 28px | 40px | `clamp(28px, 0.75vw + 25px, 40px)` |
| `heading-3` | 24px | 32px | `clamp(24px, 0.5vw + 20px, 32px)` |
| `heading-4` | 22px | 28px | `clamp(22px, 0.375vw + 19px, 28px)` |
| `heading-5` | 22px | 22px | Fixed |
| `body` | 16px | 16px | Fixed |
| `small` | 14px | 14px | Fixed |

**Rules:**
- h1 must never equal h2 at any viewport width (h1 min 32px > h2 min 28px)
- Body text, labels, and small text stay fixed -- fluid scaling doesn't benefit these sizes
- Component-specific overrides (hero title, section headings) may use their own clamp values but must respect the hierarchy

### Responsive Grid

| Layout | Desktop | Tablet | Mobile |
|--------|---------|--------|--------|
| Card grids (3-col) | 3 columns | 2 columns | 1 column |
| Card grids (2-col) | 2 columns | 2 columns | 1 column |
| Content + sidebar | 60/40 split | Stack (content then sidebar) | Stack |
| Footer columns | 3 columns | 2 columns | 1 column |
| Navigation | Full horizontal | Condensed horizontal | Hamburger menu |

### Responsive Rules

1. **No max-width on body**: Section backgrounds stretch full-viewport. Inner containers carry `max-width: 1440px; margin: 0 auto;`. This is non-negotiable.
2. **No horizontal scroll at 375px**: Test every prototype at exactly 375px. If anything overflows, fix it.
3. **Fluid between breakpoints**: Use relative units (%, vw, flex, grid) between breakpoints rather than fixed px widths for content areas. Fixed px is fine for max-widths and component dimensions.
4. **Images**: Always `max-width: 100%` and `height: auto`. Never allow images to overflow their container.
5. **Touch targets on mobile**: Minimum 44px tap target for interactive elements (buttons, links, form fields).
6. **Gutters scale down**: Page gutters reduce from 48px (desktop) to 32px (tablet) to 20px (mobile). Never go below 20px.
7. **Navigation**: Collapses to hamburger menu at 768px. No truncated or wrapping nav items.
8. **Full-bleed sections**: Background colours/images span to viewport edge at all sizes. Content within stays constrained by gutters.

---

## How to Use This for a New Project

1. **Copy this file** as your baseline design system for the new project.
2. **Replace colour tokens** with the partner's brand palette. Keep the neutral scale unless the partner has its own.
3. **Replace font family** if the partner uses a different typeface. Keep the scale ratios.
4. **Keep the spacing scale** unless there's a strong reason to deviate.
5. **Keep the component patterns** (pill buttons, card layouts, alternating backgrounds) as defaults; override per-project.
6. **Map to WordPress theme.json** during build: typography presets, colour palette, spacing scale, and layout widths all translate directly to block theme configuration.
