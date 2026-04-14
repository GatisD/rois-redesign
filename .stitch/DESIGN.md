# ROIS — Design System

## Brand Identity
- **Agency:** ROIS Digital Marketing
- **Market:** Latvia
- **Voice:** Confident, direct, data-backed. No fluff, no corporate filler.
- **Vibe:** Premium SaaS meets performance agency — think Linear × Vercel × a Riga studio

---

## Color Palette

### Light Mode
| Token | Hex | Usage |
|---|---|---|
| `--bg-primary` | `#FFFFFF` | Page background |
| `--bg-secondary` | `#F7F7F7` | Card / section backgrounds |
| `--bg-tertiary` | `#EFEFEF` | Subtle dividers, inputs |
| `--text-primary` | `#0A0A0A` | Headings, body |
| `--text-secondary` | `#5A5A5A` | Subtext, labels |
| `--text-muted` | `#9A9A9A` | Placeholders, captions |
| `--accent` | `#0066FF` | CTAs, links, highlights |
| `--accent-hover` | `#0052CC` | Button hover state |
| `--border` | `#E5E5E5` | Card borders, dividers |

### Dark Mode
| Token | Hex | Usage |
|---|---|---|
| `--bg-primary` | `#0A0A0A` | Page background |
| `--bg-secondary` | `#141414` | Card / section backgrounds |
| `--bg-tertiary` | `#1E1E1E` | Inputs, subtle surfaces |
| `--text-primary` | `#F5F5F5` | Headings, body |
| `--text-secondary` | `#A0A0A0` | Subtext, labels |
| `--text-muted` | `#606060` | Placeholders, captions |
| `--accent` | `#0066FF` | CTAs, links, highlights |
| `--accent-hover` | `#3385FF` | Button hover (lighter in dark) |
| `--border` | `#2A2A2A` | Card borders, dividers |

### Semantic
| Token | Hex | Usage |
|---|---|---|
| `--success` | `#00C853` | Positive metrics, confirmations |
| `--warning` | `#FFB300` | Alerts |
| `--error` | `#FF3B30` | Errors, destructive actions |

---

## Typography

### Font Stack
```css
--font-heading: 'Geist', 'Inter', system-ui, sans-serif;
--font-body:    'Geist', 'Inter', system-ui, sans-serif;
--font-mono:    'Geist Mono', 'Fira Code', monospace;
```
Load via `next/font` — zero layout shift, self-hosted.

### Scale
| Token | Size | Weight | Line Height | Usage |
|---|---|---|---|---|
| `--text-display` | 72px | 800 | 1.05 | Hero headline |
| `--text-h1` | 48px | 700 | 1.1 | Page titles |
| `--text-h2` | 36px | 700 | 1.15 | Section headings |
| `--text-h3` | 24px | 600 | 1.2 | Card titles, subsections |
| `--text-h4` | 20px | 600 | 1.25 | Labels, small headings |
| `--text-body-lg` | 18px | 400 | 1.6 | Lead paragraphs |
| `--text-body` | 16px | 400 | 1.6 | Body copy |
| `--text-sm` | 14px | 400 | 1.5 | Captions, metadata |
| `--text-xs` | 12px | 500 | 1.4 | Tags, badges |

### Rules
- Headings: letter-spacing `-0.02em` for tight, editorial look
- Body: letter-spacing `0` — never track body text wider
- Numbers/metrics: `font-variant-numeric: tabular-nums`

---

## Spacing & Layout

### Grid
- **Columns:** 12
- **Max content width:** `1280px`
- **Gutter:** `24px` (mobile: `16px`)
- **Side padding:** `clamp(16px, 5vw, 80px)`

### Spacing Scale (4px base)
```
--space-1:  4px
--space-2:  8px
--space-3:  12px
--space-4:  16px
--space-5:  20px
--space-6:  24px
--space-8:  32px
--space-10: 40px
--space-12: 48px
--space-16: 64px
--space-20: 80px
--space-24: 96px
--space-32: 128px
```

### Section Rhythm
- Section padding (desktop): `96px` top/bottom
- Section padding (mobile): `64px` top/bottom
- Component gap within sections: `48px`

---

## Components

### Buttons
```
Primary:   bg #0066FF, text white, radius 6px, padding 12px 24px, font-weight 600
Secondary: bg transparent, border 1.5px solid --border, text --text-primary, same padding
Ghost:     no border, no bg, text --accent, underline on hover
```
- Hover: `translateY(-1px)` + shadow `0 4px 16px rgba(0,102,255,0.3)`
- Active: `translateY(0)` — snap back
- Disabled: `opacity: 0.4`, `cursor: not-allowed`

### Cards
```
bg: --bg-secondary
border: 1px solid --border
border-radius: 12px
padding: 32px
transition: border-color 200ms, box-shadow 200ms
hover: border-color --accent (20% opacity), box-shadow 0 8px 32px rgba(0,0,0,0.12)
```

### Navigation
- Sticky header, `backdrop-filter: blur(12px)`, `background: rgba(10,10,10,0.8)` (dark)
- Height: 64px
- Logo: `font-size: 22px`, `font-weight: 800`, letter-spacing `-0.04em`
- Nav links: `font-size: 15px`, `font-weight: 500`, fade to accent on hover

### Metric Callouts
- Number: `--text-display` size, `font-weight: 800`, color `--accent`
- Label: `--text-sm`, `--text-secondary`, uppercase, `letter-spacing: 0.08em`
- Subtle top border in accent color (3px, left-aligned)

### Tags / Badges
- `font-size: 12px`, `font-weight: 600`, uppercase, `letter-spacing: 0.06em`
- Padding: `4px 10px`, `border-radius: 999px`
- Service tags: accent bg at 10% opacity, accent text

---

## Motion & Animation

### Principles
- Purposeful only — never animate for decoration
- Duration: `150ms` (micro), `250ms` (standard), `400ms` (page transitions)
- Easing: `cubic-bezier(0.16, 1, 0.3, 1)` (spring-like, fast out)

### Scroll Reveals
```css
/* Elements fade up on enter */
initial:  opacity: 0, translateY(24px)
animate:  opacity: 1, translateY(0)
duration: 500ms
stagger:  80ms between siblings
```

### Hover States
- Cards: `transform: translateY(-2px)` — never more
- Buttons: `transform: translateY(-1px)` + glow shadow
- Links: color transition `150ms`

### No-motion
Always respect `prefers-reduced-motion: reduce` — disable all transforms and transitions.

---

## Iconography
- Library: **Lucide Icons** (consistent stroke, 1.5px, geometric)
- Size: 20px standard, 24px in cards, 16px inline
- Color: inherits `currentColor`

---

## Dark Mode Implementation
```tsx
// next-themes or manual class toggle
<html class="dark"> → CSS variables switch automatically
// Persist in localStorage, respect prefers-color-scheme on first visit
```

---

## Imagery & Visual Style
- Photography: High-contrast, desaturated with accent color overlays
- Data viz: Minimal line/bar charts, accent blue only
- Abstract graphics: Geometric — grids, nodes, subtle dot patterns
- No stock photo clichés (no handshakes, no lightbulbs)

---

## Responsive Breakpoints
```
sm:  640px   — mobile landscape
md:  768px   — tablet
lg:  1024px  — small desktop
xl:  1280px  — standard desktop
2xl: 1536px  — wide
```

### Key responsive rules
- Hero headline: `clamp(36px, 6vw, 72px)`
- Services grid: 1 col (mobile) → 2–3 (tablet) → 5 (desktop)
- Nav: hamburger menu below `lg`

---

## Accessibility
- Color contrast: 4.5:1 minimum for body, 3:1 for large text (WCAG AA)
- Focus rings: `outline: 2px solid --accent`, `outline-offset: 3px`
- All interactive elements keyboard-navigable
- `aria-label` on icon-only buttons
- `prefers-reduced-motion` respected globally
- Semantic HTML — `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`
