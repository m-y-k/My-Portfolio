# Portfolio Build — Handoff Package

This folder contains everything an AI coding agent (Antigravity, Claude Sonnet, Cursor, etc.) needs to build Mohammad Yusuf Khan's portfolio website without further input.

## Files in this package

| # | File | Purpose | Who reads it |
|---|------|---------|--------------|
| 01 | `01_PRD.md` | Product requirements: what we're building, audience, goals, success criteria | Agent (first) |
| 02 | `02_DESIGN_SPEC.md` | Visual system: colors, typography, components, motion, anti-patterns | Agent |
| 03 | `03_BUILD_SPEC.md` | Tech stack, file structure, performance targets, deployment, acceptance checklist | Agent |
| 04 | `04_CONTENT.md` | Every piece of copy, every SVG, every URL placeholder — used verbatim | Agent |
| 05 | `05_AGENT_PROMPT.md` | The exact prompt to paste into Antigravity, plus tips for managing the agent | You |
| 06 | `index.html` (reference) | A working baseline implementation the agent should match and improve | Agent |

## How to use this

1. Open `05_AGENT_PROMPT.md`, copy the prompt block.
2. Open Antigravity Terminal (or your AI coding environment of choice).
3. Attach files `01` through `04` and the reference `index.html` to the conversation.
4. Paste the prompt.
5. Let the agent work.
6. When it claims done, run through the acceptance checklist in `03_BUILD_SPEC.md` §11 yourself.
7. Replace placeholder URLs (6 site links + LinkedIn / GitHub / LeetCode).
8. Deploy.

## What you still need to do manually

These cannot be done by the agent — gather them before or right after the build:

- [ ] **6 live URLs** for the client websites (AOG India, Shalimar, Rollz N' Zingz, Tiger Royal Signatures, Faheem Cabs, HMS)
- [ ] **LinkedIn URL** (your full profile link)
- [ ] **GitHub URL** (your username)
- [ ] **LeetCode URL** (your username)
- [ ] (Optional) **Custom domain** — buy on Cloudflare/Namecheap (~₹800/yr) and connect to GitHub Pages. Recommended: `yusufkhan.dev` or `mohammadyusufkhan.com`. Lands much better when a founder opens it.
- [ ] (Optional) **Real screenshots** of the 6 client sites — much better than the illustrated SVG cards. To swap, replace each `<svg>...</svg>` block in the site cards with `<img src="screenshots/aog.jpg" alt="AOG India homepage">`.

## Spec philosophy

Each document does one job:
- **PRD** = the *why* and the *who*
- **Design spec** = the *look*
- **Build spec** = the *how* and the *constraints*
- **Content** = the *what to say*

Keep them separate so when you iterate later (new project, updated copy, restyle), you only edit one file. Don't merge them.

## Iteration after launch

When you want to change something later:
- New project → edit `04_CONTENT.md`, re-run the agent
- Visual tweak → edit `02_DESIGN_SPEC.md`, re-run the agent
- New section → update `01_PRD.md` and `04_CONTENT.md`, re-run the agent

This way the spec stays the source of truth and the code stays disposable. If you ever want to rebuild from scratch on a new framework, you just hand the same specs to the agent again.
