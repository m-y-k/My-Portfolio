# CLAUDE.md — Portfolio Project Guide

## What This Is
Personal portfolio website for **Mohammad Yusuf Khan**, a Java backend engineer in Delhi. Single-page static site sent directly to startup founders, CTOs, recruiters, and engineering leads.

## Spec Files (source of truth)
All specs live in `portfolio-spec/`. If you need to change something, edit the relevant spec first:
- `01_PRD.md` — product requirements, audience, goals, success criteria
- `02_DESIGN_SPEC.md` — visual system: colors, typography, components, motion
- `03_BUILD_SPEC.md` — tech stack, file structure, performance, deployment, acceptance checklist
- `04_CONTENT.md` — every piece of copy and SVG, used **verbatim** (do NOT paraphrase)
- `05_AGENT_PROMPT.md` — agent prompt template and tips

## Tech Stack
- **Single-file HTML** (`index.html`) — all CSS in `<style>`, all JS in `<script>`
- **Vanilla CSS3** — no Tailwind, no preprocessors
- **Vanilla JavaScript** — no frameworks, no jQuery
- **Google Fonts**: Fraunces (variable serif) + JetBrains Mono
- No build step required — open `index.html` in a browser

## Design System (quick reference)
- **Palette**: warm dark editorial. Single accent: saffron `#E8A33D`
- **Background**: `#0F0E0C` (warm near-black), never pure black or pure white
- **Text**: `#F2EADA` (headings), `#BDB39F` (body), `#7C7466` (muted)
- **Fonts**: Fraunces for headings/body, JetBrains Mono for labels/nav/chips
- **Motion**: reveal-on-scroll via IntersectionObserver, hero stagger. Honor `prefers-reduced-motion`
- **Anti-patterns**: no glassmorphism, no purple/pink/blue, no skill bars, no typing effects, no particles

## Content Rules
- All copy comes from `04_CONTENT.md` — use it **exactly as written**
- Words in `*asterisks*` → italic + `--accent-soft` color
- Words in `**double asterisks**` → `<strong>` or `<b>`
- Bold words in work bullets get saffron underline highlight

## Key URLs
| Site | URL |
|------|-----|
| AOG India | https://aogindia.com/ |
| Shalimar Restaurant | https://shalimar-restaurant-bdn.onrender.com/ |
| Rollz N' Zingz | https://rollz-n-zingz.vercel.app/ |
| Tiger Royal Signatures | https://tiger-the-royal-signatures-pvt-ltd.onrender.com/ |
| Faheem Cabs | https://faheem-cabs.onrender.com/ |
| HMS | https://hms-frontend-eq2r.onrender.com |
| LinkedIn | https://www.linkedin.com/in/m-y-k-/ |
| GitHub | https://github.com/m-y-k |
| LeetCode | https://leetcode.com/u/myk220897/ |
| Email | mohammad.yusufkhan12345@gmail.com |
| Phone | +91 70374 88868 |

## Performance Targets
- Lighthouse ≥ 95 on all four categories
- Page weight < 100KB (excl. fonts), < 300KB total
- FCP < 800ms on 3G
- Works with JS disabled (content visible, animations off)

## Page Sections (DOM order)
1. `<nav>` — sticky top nav
2. `<header id="top">` — hero
3. `<section id="metrics">` — 4 metric tiles
4. `<section id="work">` — 2 work items
5. `<section id="projects">` — 4 project cards
6. `<section id="sites">` — 6 site cards with inline SVG thumbnails
7. `<section id="toolkit">` — 6 toolkit rows
8. `<section id="about">` — manifesto (3 paragraphs + signature)
9. `<section id="contact">` — contact card
10. `<footer>` — copyright + back-to-top

## Deployment
- **GitHub Pages**: push to `main`, Settings → Pages → Source: `main` / root
- **Local**: `python -m http.server 8000` or just open `index.html`
- **Cloudflare/Netlify**: drag-and-drop the folder

## Do NOT Add
- Dark/light toggle, language switcher, cookie banner
- Blog, newsletter, contact form, social share buttons
- CMS, admin panel, analytics, tracking
- Project case study sub-pages
