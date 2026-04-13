# Product Requirements Document — Mohammad Yusuf Khan Portfolio

## 1. Summary
A static, single-page personal portfolio website for **Mohammad Yusuf Khan**, a Java backend engineer with ~3 years of production experience. The site will be sent directly to recruiters, founders, CEOs, and engineering leads as a hiring/credibility asset.

## 2. Audience (in priority order)
1. **Startup founders / CEOs** — non-technical or semi-technical, skim in 30 seconds, want proof of shipping and ownership.
2. **CTOs / Tech Leads** — read carefully, evaluate technical depth, look for system-design thinking.
3. **HR / Recruiters** — scan for keywords, role fit, location, contact info.
4. **Peer engineers** — judge taste, code quality, opinions.

## 3. Goals
- Land an interview in **under 60 seconds** of reader attention.
- Communicate that Mohammad is a **scrappy operator** who researches, ships, and supports — not just a JD-executor.
- Showcase both **production backend rigor** (Spring Boot microservices, 10K+ daily txns) and **shipping range** (six live client websites built independently).
- Be **instantly accessible** — must load in under 1 second on a 3G connection.

## 4. Non-Goals
- No CMS, no blog, no admin panel.
- No analytics tracking by default (privacy-respecting; user can add later if desired).
- No login, no forms beyond a `mailto:` link.
- No dynamic data fetching, no SSR, no API calls.
- No tracking pixels, no third-party JS beyond Google Fonts.

## 5. Success Criteria
- Lighthouse score **≥95** on Performance, Accessibility, Best Practices, SEO.
- First Contentful Paint **<800ms** on a cold load.
- Total page weight **<300KB** (excluding fonts).
- Renders correctly on Chrome, Safari, Firefox, Edge — desktop and mobile.
- Zero JavaScript errors in console.
- Fully responsive from **320px to 2560px** viewport widths.
- Works with JS disabled (degrades gracefully — animations off, content visible).

## 6. Constraints
- **Open source**: every line readable; MIT license in repo.
- **Static**: no server, no build step required for deploy. (A build step like Astro/Vite is fine if the *output* is plain static HTML/CSS/JS.)
- **Free hosting target**: GitHub Pages, Cloudflare Pages, or Netlify free tier.
- **No proprietary dependencies**.
- **Single-author maintainability**: Mohammad must be able to edit copy by opening one or two files in any text editor.

## 7. Deliverables
- A Git repository with the source code.
- A `README.md` with setup, edit, and deploy instructions.
- A `LICENSE` file (MIT).
- One-command deploy instructions for GitHub Pages.
