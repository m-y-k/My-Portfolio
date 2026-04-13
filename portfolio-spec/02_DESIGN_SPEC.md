# Design Specification

## 1. Aesthetic Direction
**Warm dark editorial.** Think: a thoughtful engineer's notebook crossed with a print magazine. Confident, quiet, type-led. Avoid: glassmorphism, purple gradients, neon glow, 3D scenes, particle backgrounds, hero animations, gradient text.

The site itself is proof of taste. A founder seeing it should think *"this person has judgment."*

## 2. Color System
Use CSS custom properties at `:root`. Do not hard-code colors anywhere else.

```
--bg:           #0F0E0C   /* warm near-black, page background */
--bg-lift:      #17150F   /* slightly raised surface */
--surface:      #1C1A14   /* cards, lifted elements */
--line:         #2A2620   /* borders, dividers */
--line-strong:  #3A342B   /* hover/focus borders */
--text:         #F2EADA   /* primary text — warm cream, NOT pure white */
--text-soft:    #BDB39F   /* body paragraphs */
--text-mute:    #7C7466   /* labels, metadata, footer */
--accent:       #E8A33D   /* saffron — single accent, used sparingly */
--accent-soft:  #F2C078   /* accent at lighter weight, for italic display words */
--accent-deep:  #B87A1F   /* accent for hover states on accent elements */
--good:         #8FB369   /* "available" status dot only */
```

**Rules:**
- Saffron (`--accent`) is the *only* accent color. Do not introduce blue, pink, etc.
- Body text is `--text-soft`, not `--text`. Reserve `--text` for headings and emphasized words.
- Never use pure white (`#FFFFFF`) or pure black (`#000000`) anywhere.

## 3. Typography
Two fonts. Both from Google Fonts. Use `font-display: swap`.

```
--serif: "Fraunces", "Iowan Old Style", Georgia, serif;
--mono:  "JetBrains Mono", ui-monospace, "SF Mono", Menlo, monospace;
```

**Fraunces** is variable — leverage it:
- Display headings: `font-variation-settings: "opsz" 144, "SOFT" 50;`
- Italic accent words: `font-variation-settings: "opsz" 144, "SOFT" 100, "WONK" 1;` and `font-style: italic;` and color `--accent-soft`
- Body: default settings, weight 380–420

**JetBrains Mono** uses:
- Section numbers, eyebrow labels, navigation, chips/tags, metric units, button text
- Always uppercase with `letter-spacing: 0.08em–0.14em` for labels
- Sizes: 10.5px–13px

**Type scale:**
- Hero H1: `clamp(44px, 7.4vw, 96px)`, line-height 0.96, letter-spacing -0.025em
- Section title H2: `clamp(28px, 4vw, 44px)`, letter-spacing -0.02em
- Card H3: 24–26px
- Body: 17px, line-height 1.55
- Lede paragraph: `clamp(18px, 2.1vw, 22px)`, line-height 1.5
- Small/mono labels: 11–13px

## 4. Layout
- Max content width: `1120px`
- Horizontal gutter: `clamp(20px, 4vw, 56px)`
- Section vertical padding: `clamp(72px, 12vh, 128px)`
- All sections separated by a `1px solid var(--line)` bottom border, except the last.

**Section header pattern** (used for every section):
- Two-column grid: 180px (section number + label) | 1fr (title + subtitle)
- Section number: mono, uppercase, with a `border-top: 1px solid var(--accent)` over a 80px width
- Titles use one *italic* word in `--accent-soft` for emphasis (e.g., "Numbers from *production*.")
- On mobile (<760px): collapses to single column

## 5. Components

### Navigation (sticky top)
- Translucent dark background with `backdrop-filter: blur(14px)`
- Left: monospace mark `M.Y.K — backend.engineer` (the K in saffron)
- Right: 5 anchor links (mono, 12.5px, soft color, hover → saffron with a bullet dot indicator on the left)
- Hide nav links on mobile (<720px)

### Metric tile
- 4-column grid (2 on mobile), 1px gap on `--line` background to create hairline dividers
- Each tile: large serif numeral + small mono unit (e.g., `10K` + `/day` superscript in saffron)
- Mono caption below in `--text-mute`
- Background lifts to `--bg-lift` on hover

### Work item (experience)
- 3-column grid: date (mono) | body | stack chips
- Date in mono, uppercase, `--text-mute`
- Hover: shifts content right by 12px (transition 0.25s)
- Bullets use `→` arrow in saffron, and `<b>` tags inside bullets get a subtle saffron highlight (`linear-gradient(transparent 65%, rgba(232,163,61,0.18) 65%)`)

### Project card (backend systems)
- 2-column grid, 1px gap, hairline dividers
- Each card: badge (mono, uppercase, with leading dot) → title (serif, with one italic word) → description → stack chips at bottom
- Background lifts on hover

### Site card (client websites)
- 3-column grid (2 on tablet, 1 on mobile), 24px gap
- Each card has a 16:10 illustrated thumbnail (inline SVG, no external images), plus body
- Body shows: kind/category in mono, "● LIVE" status in green mono, title in serif, short description, "visit site →" CTA in saffron mono
- Hover: lifts 4px, border strengthens

### Toolkit row
- 2-column grid, 1px gap
- Each row: small saffron mono label + comma-separated items in serif
- Use `·` separators (not bullets) between items in `--text-mute`

### Manifesto block
- Max-width 760px, centered
- First paragraph uses a drop cap: `::first-letter` sized 3.6em, italic, saffron, Fraunces with WONK on
- Three paragraphs, large serif (20–26px clamp), warm color
- Signature line in mono, uppercase, muted

### Contact card
- Full-width centered card with subtle vertical gradient (`--bg-lift` to `--bg`)
- Large serif heading with one italic accent word
- Pill-shaped CTAs (`border-radius: 999px`):
  - Primary: solid saffron, dark text
  - Secondary: outlined, hover → saffron text + saffron border
- All CTAs in mono, 13px

## 6. Motion
**Restraint over flash.** No parallax, no scroll-jacking.

- **Reveal-on-scroll**: elements with `.reveal` class fade up 20px over 0.8s using `cubic-bezier(.2,.8,.2,1)`. Triggered by IntersectionObserver at threshold 0.12.
- **Hero stagger**: each `.hero .reveal` element gets a `transition-delay` of `index * 120ms`.
- **Status dot pulse**: 2.4s ease-in-out infinite shadow pulse.
- **Hover transitions**: 0.2–0.3s, all easing `ease`.
- Honor `prefers-reduced-motion: reduce` — disable all animations and reveal everything immediately.

## 7. Texture & Atmosphere
A single subtle SVG noise overlay (`opacity: 0.035`, `mix-blend-mode: overlay`) on the body via `::before`. Inline SVG data URI — no external request. This adds warmth and prevents the dark background from feeling flat.

## 8. Selection
Customize text selection to saffron background with dark text:
```css
::selection { background: var(--accent); color: #1A1207; }
```

## 9. Accessibility
- All text must meet WCAG AA contrast against its background (the chosen palette already does — verify).
- All interactive elements need visible focus states (use `outline: 2px solid var(--accent); outline-offset: 2px;` if default browser ring is removed).
- All links to external sites: `target="_blank" rel="noopener noreferrer"`.
- All decorative SVGs should have `aria-hidden="true"`.
- Page must have a logical heading hierarchy: one H1, then H2 per section.
- Sufficient touch targets on mobile (min 44×44px).

## 10. Anti-patterns (do NOT do)
- ❌ Pure white text on pure black
- ❌ Inter, Roboto, Arial, system-ui as primary fonts
- ❌ Purple/pink/blue gradients
- ❌ Glassmorphism cards with multiple blurs
- ❌ Skill bars / proficiency percentages
- ❌ Animated typing effects on the hero ("I am a ___ developer")
- ❌ Floating particles / 3D backgrounds / Three.js scenes
- ❌ Auto-playing carousels
- ❌ Multiple accent colors
- ❌ Emoji in headings (the `✦` in the email CTA is the only allowed glyph)
