# Build Specification

## 1. Tech Stack
- **HTML5**, semantic markup throughout
- **CSS3**, vanilla — no Tailwind, no preprocessors required (Sass/Less acceptable but compile to plain CSS in output)
- **Vanilla JavaScript** — no framework, no jQuery, no build dependencies
- **Google Fonts** (Fraunces + JetBrains Mono) loaded via `<link>` with `font-display: swap`

**Optional but acceptable** if it produces purely static output:
- Astro (preferred if a build step is wanted — produces zero-JS HTML by default)
- Eleventy (11ty)
- Plain HTML in a single file (also fully acceptable — actually preferred for max simplicity)

**Not allowed**: Next.js with SSR, Gatsby, Nuxt with hydration, anything that ships a runtime to the client by default.

## 2. File Structure (single-file approach — recommended)
```
/
├── index.html        # The entire site: HTML + CSS in <style> + JS in <script>
├── README.md         # Setup, edit, deploy instructions
├── LICENSE           # MIT
└── .nojekyll         # Empty file, for GitHub Pages
```

## 2b. File Structure (multi-file approach — if preferred)
```
/
├── index.html
├── styles/
│   └── main.css
├── scripts/
│   └── main.js
├── assets/
│   └── (any future images)
├── README.md
├── LICENSE
└── .nojekyll
```

## 3. Page Structure (in DOM order)
1. `<nav>` — sticky top nav
2. `<header class="hero" id="top">` — hero section
3. `<section id="metrics">` — production receipts (4 metric tiles)
4. `<section id="work">` — experience (2 work items)
5. `<section id="projects">` — backend systems (4 project cards)
6. `<section id="sites">` — client websites (6 site cards with inline SVG thumbnails)
7. `<section id="toolkit">` — skills (6 toolkit rows)
8. `<section id="about">` — manifesto (3 paragraphs + signature)
9. `<section id="contact" class="contact">` — contact card
10. `<footer>` — copyright + back-to-top

## 4. Content
**All copy is in `04_CONTENT.md`. Do not paraphrase, invent, or shorten. Use the text exactly as provided.** This includes microcopy like section eyebrows, button labels, and the manifesto paragraphs.

## 5. SEO & Metadata
In `<head>`:
```html
<title>Mohammad Yusuf Khan — Java Backend Engineer</title>
<meta name="description" content="Java backend engineer with 3 years building production systems that move money, sync inventory, and don't fall over at 10K daily transactions. Spring Boot, Microservices, AWS." />
<meta name="theme-color" content="#0F0E0C" />
<meta property="og:title" content="Mohammad Yusuf Khan — Java Backend Engineer" />
<meta property="og:description" content="3 years shipping Spring Boot systems for ERP, payments, and reconciliation. Plus six production websites for real businesses." />
<meta property="og:type" content="website" />
<meta property="og:url" content="https://[REPLACE-WITH-DEPLOY-URL]" />
<meta name="twitter:card" content="summary_large_image" />
```

Add a favicon — generate a simple SVG favicon with the letter `K` in saffron on a dark background, inline:
```html
<link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect width='100' height='100' fill='%230F0E0C'/><text x='50' y='72' font-family='serif' font-size='72' font-style='italic' text-anchor='middle' fill='%23E8A33D'>K</text></svg>" />
```

## 6. JavaScript
Only one script — an IntersectionObserver for reveal animations. Vanilla, no dependencies. Fewer than 20 lines. Place in a `<script>` tag at the end of `<body>`.

## 7. Browser Support
- Chrome / Edge: latest 2 versions
- Firefox: latest 2 versions
- Safari: latest 2 versions (desktop + iOS)
- Graceful degradation in older browsers — content must remain readable

## 8. Performance Requirements
- Total page weight (HTML + CSS + JS, excluding fonts): **<100KB**
- Total with fonts: **<300KB**
- No render-blocking resources beyond the single Google Fonts stylesheet
- Use `preconnect` to `fonts.googleapis.com` and `fonts.gstatic.com` in `<head>`

## 9. Inline SVG Thumbnails for Site Cards
Each of the 6 site cards in the "Shipped" section has a custom inline SVG thumbnail (no external image files). Use the SVGs provided in `04_CONTENT.md` exactly. They use `viewBox="0 0 320 200"` with gradient backgrounds matching each brand's vibe.

If Mohammad later provides real screenshots, they should be swappable by replacing the `<svg>` block with `<img src="..." alt="...">` — keep the parent structure intact.

## 10. Repository / Deployment

### `README.md` must include:
1. One-line description
2. **How to run locally**: just open `index.html` in a browser, or use `python3 -m http.server 8000`
3. **How to edit content**: open `index.html` in any text editor, find the section, change the text
4. **How to deploy to GitHub Pages**:
   - Push to GitHub
   - Settings → Pages → Source: deploy from branch `main` / root
   - Done. URL appears in 1–2 minutes.
5. **How to deploy to Cloudflare Pages / Netlify**: drag-and-drop the folder onto their dashboard

### `LICENSE`: MIT, year 2026, author "Mohammad Yusuf Khan"

### `.nojekyll`: empty file (prevents GitHub Pages from running Jekyll on the site)

## 11. Acceptance Checklist
The agent must verify all of the following before declaring the build complete:

- [ ] Page loads with no console errors or warnings
- [ ] All 6 site cards display correctly with their inline SVG thumbnails
- [ ] All 4 metric tiles render with correct numbers
- [ ] All 2 work items render with correct dates and bullets
- [ ] All 4 project cards render
- [ ] All 6 toolkit rows render
- [ ] Manifesto drop cap renders correctly in Fraunces italic
- [ ] Sticky nav stays visible on scroll
- [ ] Status dot in hero pulses
- [ ] Reveal animations trigger on scroll for non-hero sections
- [ ] Hero elements stagger their reveal on initial load
- [ ] Hover states work on: nav links, work items (slide right), project cards (lift), site cards (lift), CTAs
- [ ] All text is readable on both `--bg` and `--bg-lift` backgrounds (WCAG AA)
- [ ] Keyboard navigation works: Tab moves through all interactive elements with visible focus
- [ ] Layout is intact at viewport widths: 320, 375, 768, 1024, 1440, 2560
- [ ] `mailto:` link opens email client; `tel:` link triggers dial on mobile
- [ ] All external links use `rel="noopener noreferrer"` and `target="_blank"`
- [ ] `prefers-reduced-motion` honored — animations disabled when set
- [ ] Lighthouse: Performance ≥95, Accessibility ≥95, Best Practices ≥95, SEO ≥95
- [ ] Site renders correctly with JavaScript disabled (animations off, content visible)
- [ ] Favicon shows in browser tab
- [ ] OG tags present and valid

## 12. Out of Scope (do NOT add)
- Dark/light theme toggle (it's already dark by design)
- Language switcher
- Cookie banner (no cookies are set)
- Newsletter signup
- Blog
- Project case study sub-pages
- Contact form (`mailto:` only)
- Social share buttons
