# Agent Prompt — Paste this into Antigravity / Claude Sonnet

Copy the block below into Antigravity Terminal as your initial prompt. Attach all four spec files (`01_PRD.md`, `02_DESIGN_SPEC.md`, `03_BUILD_SPEC.md`, `04_CONTENT.md`) and the existing reference `index.html` to the conversation.

---

```
You are building a personal portfolio website for Mohammad Yusuf Khan, a Java backend engineer in Delhi. He is sending this site directly to startup founders, CTOs, recruiters, and engineering leads to get hired.

I have attached four specification documents and one reference file. Read all of them in this order before writing any code:

1. 01_PRD.md         — what we're building and for whom
2. 02_DESIGN_SPEC.md — visual system (colors, fonts, components, motion)
3. 03_BUILD_SPEC.md  — tech stack, file structure, performance, deployment
4. 04_CONTENT.md     — every piece of copy and SVG, to be used verbatim
5. index.html        — a working reference implementation

Your job:

1. Read all five files end-to-end.
2. Build the site as a single static index.html file (HTML + <style> + <script> all in one), unless you have a strong reason to split into separate files — in which case, follow the multi-file structure in BUILD_SPEC §2b.
3. Use the content from 04_CONTENT.md exactly. Do not paraphrase, "improve," shorten, or invent any text.
4. Match the design system in 02_DESIGN_SPEC.md exactly — same colors, same fonts, same components.
5. Use the reference index.html as your baseline, but improve on it where you find issues. Specifically:
   - Verify accessibility (semantic HTML, ARIA where needed, focus states, contrast)
   - Verify keyboard navigation works end-to-end
   - Verify the layout holds at 320px, 375px, 768px, 1024px, 1440px, 2560px
   - Verify reduced-motion is honored
6. Create README.md, LICENSE (MIT, year 2026, author "Mohammad Yusuf Khan"), and an empty .nojekyll file.
7. Run through the acceptance checklist in BUILD_SPEC §11. Do not declare done until every item passes.
8. Open the site in a browser, take a screenshot of the rendered result, and confirm visually that it matches the design intent.

Constraints to never violate:
- No external JS frameworks (no React, Vue, jQuery, etc.).
- No CSS frameworks (no Tailwind, Bootstrap, etc.).
- No external image files — all visuals are inline SVG provided in CONTENT.md.
- No tracking scripts, no analytics, no cookies.
- Must work with JS disabled (animations off, content visible).
- Must hit Lighthouse ≥95 on Performance, Accessibility, Best Practices, SEO.

When you are done, output:
- A list of every file you created
- A summary of any deviations from the spec (and why)
- The Lighthouse scores
- One-line deploy instructions for GitHub Pages

Begin by reading all five attached files. Do not write code until you have read them.
```

---

## Why this prompt structure works

- **Forces sequential reading** before any code is written — prevents the agent from skimming and inventing.
- **Names the four files explicitly** so the agent doesn't ignore one.
- **Provides a reference implementation** so the agent has something concrete to compare against.
- **Lists explicit improvements to make** — not just "build this" but "fix these specific things while you're at it."
- **Has an acceptance gate** at the end — the agent has to self-check before declaring done.
- **Lists hard constraints in their own block** — easier for the model to keep them in working memory.
- **Specifies what to output at the end** — gives you a clean handoff back.

## Tips for working with the agent

1. **Don't accept "done" without screenshots.** Ask the agent to render the site (Antigravity has a browser) and screenshot every section.
2. **Test the responsive breakpoints yourself** by resizing your browser. Agents often miss mobile.
3. **Run Lighthouse in the actual deployed URL**, not just locally — fonts and CDN behavior differ.
4. **Replace the placeholder URLs** (the 6 site links + LinkedIn/GitHub/LeetCode) before sending to anyone.
5. **If the agent asks clarifying questions**, point it back to the spec files. Resist the urge to answer inline — keep the spec as the single source of truth so the next iteration is reproducible.

## After the build

1. Push to a fresh GitHub repo named `portfolio` or `yusufkhan.dev`.
2. Settings → Pages → Source: deploy from `main` branch, root folder.
3. (Optional, recommended) Buy a domain (~₹800/year on Namecheap or Cloudflare) and point it at GitHub Pages. A custom domain like `yusufkhan.dev` lands far better than `username.github.io/portfolio` when a CEO opens it.
4. Send the link.
