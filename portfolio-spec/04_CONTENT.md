# Content Document — All Copy & Data

This file contains every piece of text, every list item, and every SVG thumbnail used in the site. **Use this content verbatim.** Do not paraphrase, shorten, "improve," or invent content not listed here.

Words wrapped in `*asterisks*` should render as italic and use the saffron-soft color (`--accent-soft`). Words wrapped in `**double asterisks**` are bold/emphasized in body copy (use `<strong>` or `<b>`).

---

## SITE METADATA
- **Page title**: `Mohammad Yusuf Khan — Java Backend Engineer`
- **Meta description**: `Java backend engineer with 3 years building production systems that move money, sync inventory, and don't fall over at 10K daily transactions. Spring Boot, Microservices, AWS.`
- **OG description**: `3 years shipping Spring Boot systems for ERP, payments, and reconciliation. Plus six production websites for real businesses.`

---

## NAVIGATION
- **Logo mark** (left): `M.Y.K — backend.engineer` (the `K` colored saffron, the rest in cream; "— backend.engineer" in muted color)
- **Nav links** (right): Work · Systems · Shipped · Toolkit · Contact
  - Each link's `href` is `#work`, `#projects`, `#sites`, `#toolkit`, `#contact` respectively

---

## HERO SECTION

**Eyebrow** (with pulsing green dot):
> Open to senior backend roles · India / Remote

**H1** (line breaks preserved):
> I build backend systems that
> *move money* and don't
> fall over at scale.

**Lede paragraph**:
> **Mohammad Yusuf Khan.** Java engineer with ~3 years shipping Spring Boot microservices for ERP, payments, and reconciliation — the boring, load-bearing kind. On the side, I've shipped six production websites for real businesses, because the fastest way to learn what users want is to put something in front of them.

**Meta row** (4 items, label above value):
| Label | Value |
|---|---|
| Based | Nirman Vihar, Delhi |
| Stack | Java · Spring Boot · MySQL · AWS |
| Now | Building a BGMI streamer toolkit |
| Reach | mohammad.yusufkhan12345@gmail.com (linked via `mailto:`) |

---

## SECTION 01 — RECEIPTS (Metrics)

**Section number**: `01 / Receipts`
**Title**: `Numbers from *production*.`
**Subtitle**: `From the boring metrics that actually matter to engineering leaders — throughput, latency, reduction.`

**4 Metric tiles** (large numeral + small saffron unit + mono caption):

1. **`10K`** + **`/day`** — `Transactions processed by APIs I built & own`
2. **`35`** + **`%`** — `API performance gain via MySQL indexing & query rewrites`
3. **`200`** + **`+`** — `REST endpoints designed, validated, documented`
4. **`40`** + **`%`** — `Duplicate code removed by enforcing SOLID & patterns`

---

## SECTION 02 — TRAJECTORY (Experience)

**Section number**: `02 / Trajectory`
**Title**: `Where I've *shipped*.`
**Subtitle**: `Two roles, both backend-heavy, both with cross-functional ownership beyond the JD.`

### Work item 1
- **Date column**: `Dec 2024 — Jan 2026` (with line break)
- **Title**: `Software Engineer at SunbaseData LLC` (the company name in saffron italic)
- **Role line**: `Remote · Software Developer`
- **Bullets** (`<b>` words bolded with saffron underline-highlight):
  - Designed **HLD & LLD** for ERP and financial automation microservices — payments, invoices, reconciliation, inventory.
  - Built REST APIs handling **10K+ daily transactions** with validation, pagination, and global exception handling.
  - Integrated **QuickBooks** + third-party accounting APIs for automated reconciliation workflows.
  - Optimized MySQL queries and indexing → **35% API perf gain**; added Prometheus / Grafana / SLF4J observability.
  - Containerized with Docker, deployed on **AWS EC2/S3** through Jenkins CI/CD; secured with Spring Security, JWT, OAuth 2.0, RBAC.
- **Stack chips**: Spring Boot · Microservices · MySQL · AWS · Jenkins · React · QuickBooks

### Work item 2
- **Date column**: `Feb 2023 — Nov 2024`
- **Title**: `Software Engineer at Vision Softech` (company in saffron italic)
- **Role line**: `ITO, Delhi · Software Developer`
- **Bullets**:
  - Migrated **legacy JEE/JSP/Servlet** systems to a modern Spring Boot architecture without breaking production.
  - Built **200+ REST endpoints** with proper validation, error handling, and modular separation.
  - Wired Hibernate/JPA with MySQL; tuned for reporting workloads pulling heavy aggregates.
  - Shipped React.js admin dashboards and JWT-secured access modules.
  - Stood up CI/CD via Jenkins + GitLab/Bitbucket; reduced duplicate code by **40%** applying SOLID & design patterns.
- **Stack chips**: Java · Spring MVC · Hibernate · JWT · React · Docker · GitLab CI

---

## SECTION 03 — SYSTEMS (Backend Projects)

**Section number**: `03 / Systems`
**Title**: `Production-grade *backend systems*.`
**Subtitle**: `Three platforms I designed end-to-end — from architecture sketches to deployed, observable services.` *(Note: copy says "three" but four cards display; this is intentional — the fourth is "in progress" and frames it as bonus.)*

### Project card 1
- **Badge**: `In progress · Doctors Group`
- **Title**: `Cloud-native *clinic* platform`
- **Description**: Full-stack clinic automation: patient flows, billing, inventory, notifications. Microservices behind a React UI, secured with Spring Security + OAuth 2.0, async schedulers for reminders and stock sync, deployed Dockerized on AWS with Jenkins CI/CD and Prometheus/Grafana on top.
- **Stack chips**: Spring Boot · Microservices · React · MySQL · AWS · RBAC

### Project card 2
- **Badge**: `SunbaseData LLC`
- **Title**: `Payment *reconciliation* & sync engine`
- **Description**: Spring Boot services that sync and reconcile payments across ERP, QuickBooks, and gateways. Multithreaded background workers and async jobs absorb 10K+ daily transactions; JPA/Hibernate tuned with care for reporting reads. Secured with JWT/OAuth2, monitored via Grafana.
- **Stack chips**: Multithreading · Async Jobs · QuickBooks API · JPA · Docker · Grafana

### Project card 3
- **Badge**: `SunbaseData LLC`
- **Title**: `Expense & invoice *automation*`
- **Description**: End-to-end expense and invoice workflow with event-driven processing, validation pipelines, and configurable approval chains. Reusable microservices, role-based modules, automated deploys via Maven/Gradle + Jenkins, documented with Swagger and tested with JUnit + Postman.
- **Stack chips**: Event-driven · REST APIs · React · Swagger · JUnit

### Project card 4
- **Badge**: `Personal · Building now`
- **Title**: `BGMI *streamer* toolkit`
- **Description**: A web app + companion mobile app for Indian BGMI streamers and gamers — built because the existing tooling is fragmented. Goal is to give creators a single dashboard for sensitivity configs, tournament tracking, and stream overlays. Backend in Spring Boot, mobile in React Native, designed mobile-first.
- **Stack chips**: Spring Boot · React Native · YouTube API · In progress

---

## SECTION 04 — SHIPPED (Client Websites)

**Section number**: `04 / Shipped`
**Title**: `Six websites *for real businesses*.`
**Subtitle**: `Restaurants, fashion, transport, gaming. Built independently — research, design, code, deploy, talk to the owner, fix what's confusing.`

**Intro callout** (saffron left border, italic):
> None of these were assigned to me. **I found the businesses, pitched, scoped, built, and shipped.** The fastest engineering education I've had — because the feedback loop is the owner calling you when something breaks.

### Site 1 — AOG India
- **Kind**: Gaming Network · LIVE
- **Title**: AOG India
- **Description**: Alliance of Gamers — a creator network platform connecting Indian gaming streamers with brands and audiences.
- **URL**: `https://aogindia.com/`
- **Thumbnail SVG** (320×200, deep blue gradient with circular emblem):
```html
<svg viewBox="0 0 320 200" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
  <defs><linearGradient id="g1" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#1a1f3a"/><stop offset="100%" stop-color="#0a0e1f"/></linearGradient></defs>
  <rect width="320" height="200" fill="url(#g1)"/>
  <circle cx="60" cy="100" r="48" fill="none" stroke="#E8A33D" stroke-width="2" opacity="0.9"/>
  <path d="M40 100 L80 100 M60 80 L60 120" stroke="#E8A33D" stroke-width="2"/>
  <text x="130" y="92" font-family="JetBrains Mono" font-size="11" fill="#F2EADA" letter-spacing="2">AOG</text>
  <text x="130" y="108" font-family="Fraunces" font-size="14" fill="#F2C078" font-style="italic">Alliance of Gamers</text>
  <text x="130" y="128" font-family="JetBrains Mono" font-size="9" fill="#7C7466" letter-spacing="1">CREATOR · NETWORK</text>
</svg>
```

### Site 2 — Shalimar Restaurant
- **Kind**: Restaurant · LIVE
- **Title**: Shalimar Restaurant
- **Description**: The Royal Taste of Budaun — menu, story, location, and direct ordering for a heritage restaurant.
- **URL**: `https://shalimar-restaurant-bdn.onrender.com/`
- **Thumbnail SVG** (deep red-brown):
```html
<svg viewBox="0 0 320 200" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
  <defs><linearGradient id="g2" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#3a1d12"/><stop offset="100%" stop-color="#1a0a05"/></linearGradient></defs>
  <rect width="320" height="200" fill="url(#g2)"/>
  <text x="160" y="80" text-anchor="middle" font-family="Fraunces" font-size="28" fill="#F2EADA" font-style="italic">Shalimar</text>
  <line x1="100" y1="95" x2="220" y2="95" stroke="#E8A33D" stroke-width="1"/>
  <text x="160" y="115" text-anchor="middle" font-family="JetBrains Mono" font-size="9" fill="#F2C078" letter-spacing="3">RESTAURANT · BUDAUN</text>
  <text x="160" y="145" text-anchor="middle" font-family="Fraunces" font-size="11" fill="#BDB39F" font-style="italic">The Royal Taste</text>
</svg>
```

### Site 3 — Rollz N' Zingz
- **Kind**: Food / Ordering · LIVE
- **Title**: Rollz N' Zingz
- **Description**: Online ordering and menu site for a quick-service food brand — cart, item options, location-based delivery.
- **URL**: `https://rollz-n-zingz.vercel.app/`
- **Thumbnail SVG** (warm amber with circular badge):
```html
<svg viewBox="0 0 320 200" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
  <defs><linearGradient id="g3" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#3a2a0e"/><stop offset="100%" stop-color="#1a1305"/></linearGradient></defs>
  <rect width="320" height="200" fill="url(#g3)"/>
  <rect x="40" y="60" width="80" height="80" rx="40" fill="#E8A33D"/>
  <text x="80" y="108" text-anchor="middle" font-family="Fraunces" font-size="32" fill="#1a1305" font-style="italic" font-weight="600">R</text>
  <text x="140" y="92" font-family="Fraunces" font-size="20" fill="#F2EADA">Rollz</text>
  <text x="140" y="112" font-family="Fraunces" font-size="20" fill="#F2C078" font-style="italic">N' Zingz</text>
  <text x="140" y="135" font-family="JetBrains Mono" font-size="8" fill="#7C7466" letter-spacing="2">ORDER ONLINE</text>
</svg>
```

### Site 4 — Tiger Royal Signatures
- **Kind**: Fashion E-commerce · LIVE
- **Title**: Tiger — Royal Signatures
- **Description**: Luxury Pakistani fashion brand site — collections, lookbook, product pages, inquiry flow.
- **URL**: `https://tiger-the-royal-signatures-pvt-ltd.onrender.com/`
- **Thumbnail SVG** (very dark luxury):
```html
<svg viewBox="0 0 320 200" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
  <defs><linearGradient id="g4" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#1a1410"/><stop offset="100%" stop-color="#0a0805"/></linearGradient></defs>
  <rect width="320" height="200" fill="url(#g4)"/>
  <text x="160" y="78" text-anchor="middle" font-family="Fraunces" font-size="22" fill="#F2EADA" letter-spacing="4">TIGER</text>
  <line x1="80" y1="92" x2="240" y2="92" stroke="#E8A33D" stroke-width="0.5"/>
  <text x="160" y="112" text-anchor="middle" font-family="Fraunces" font-size="11" fill="#F2C078" font-style="italic">The Royal Signatures</text>
  <text x="160" y="142" text-anchor="middle" font-family="JetBrains Mono" font-size="8" fill="#7C7466" letter-spacing="3">LUXURY · PAKISTANI · FASHION</text>
</svg>
```

### Site 5 — Faheem Cabs
- **Kind**: Booking / Transport · LIVE
- **Title**: Faheem Cabs
- **Description**: Budaun-to-Delhi cab booking platform — route info, fare estimation, contact-to-book flow tuned for mobile.
- **URL**: `https://faheem-cabs.onrender.com/`
- **Thumbnail SVG** (deep green with cab icon):
```html
<svg viewBox="0 0 320 200" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
  <defs><linearGradient id="g5" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#0e2a1f"/><stop offset="100%" stop-color="#05140e"/></linearGradient></defs>
  <rect width="320" height="200" fill="url(#g5)"/>
  <rect x="50" y="80" width="60" height="34" rx="6" fill="#E8A33D"/>
  <circle cx="65" cy="120" r="6" fill="#1a1305"/>
  <circle cx="95" cy="120" r="6" fill="#1a1305"/>
  <text x="135" y="92" font-family="Fraunces" font-size="18" fill="#F2EADA">Faheem</text>
  <text x="135" y="110" font-family="Fraunces" font-size="14" fill="#F2C078" font-style="italic">Cabs</text>
  <text x="135" y="130" font-family="JetBrains Mono" font-size="8" fill="#7C7466" letter-spacing="2">BUDAUN → DELHI</text>
</svg>
```

### Site 6 — Hospital Management System
- **Kind**: Web Application · LIVE
- **Title**: Hospital Management System
- **Description**: Full-stack HMS — patient records, appointments, billing, role-based access. Spring Boot + React.
- **URL**: `https://hms-frontend-eq2r.onrender.com`
- **Thumbnail SVG** (cool blue with clipboard + cross):
```html
<svg viewBox="0 0 320 200" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
  <defs><linearGradient id="g6" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#1a1d2e"/><stop offset="100%" stop-color="#0a0c14"/></linearGradient></defs>
  <rect width="320" height="200" fill="url(#g6)"/>
  <rect x="60" y="70" width="50" height="60" rx="3" fill="none" stroke="#E8A33D" stroke-width="1.5"/>
  <line x1="68" y1="84" x2="102" y2="84" stroke="#E8A33D" stroke-width="1"/>
  <line x1="68" y1="92" x2="102" y2="92" stroke="#E8A33D" stroke-width="1"/>
  <line x1="68" y1="100" x2="92" y2="100" stroke="#E8A33D" stroke-width="1"/>
  <path d="M85 108 L85 122 M78 115 L92 115" stroke="#E8A33D" stroke-width="1.5"/>
  <text x="135" y="92" font-family="Fraunces" font-size="22" fill="#F2EADA">HMS</text>
  <text x="135" y="115" font-family="Fraunces" font-size="11" fill="#F2C078" font-style="italic">Hospital Mgmt</text>
  <text x="135" y="135" font-family="JetBrains Mono" font-size="8" fill="#7C7466" letter-spacing="2">SYSTEM</text>
</svg>
```

---

## SECTION 05 — TOOLKIT

**Section number**: `05 / Toolkit`
**Title**: `What I *reach for*.`
**Subtitle**: `Tools I've used in production — not a checklist of buzzwords.`

**6 toolkit rows** (label + items separated by `·`):

1. **Backend** — Java 8+ · Spring Boot · Spring MVC · Spring Security · Microservices · REST · JEE/Servlets · Multithreading · SLF4J
2. **Architecture** — HLD · LLD · SOLID · Design Patterns · Clean Architecture · Event-driven · Async & Schedulers
3. **Data** — MySQL · JPA · Hibernate · JDBC · Query optimization · Indexing · Transactions
4. **Security** — JWT · OAuth 2.0 · RBAC · CORS · Spring Security
5. **DevOps & Cloud** — AWS EC2 · AWS S3 · Docker · Jenkins · Maven · Gradle · Git/GitLab/Bitbucket
6. **Frontend & Observability** — React.js · JavaScript · HTML/CSS · Swagger · Prometheus · Grafana · Postman/Bruno

---

## SECTION 06 — NOTE (Manifesto)

**Section number**: `06 / Note`
**Title**: `A short note on *how I work*.`

**Three paragraphs** (first paragraph has saffron italic drop cap on first letter):

1. Most of what I know I learned by being uncomfortable. When I joined my first job, I didn't know JPA from JDBC — I figured it out by breaking things and reading the stack traces. When I wanted to understand frontend, I didn't take a course; I went and built six websites for actual businesses, because **nothing teaches you faster than a restaurant owner texting at 11pm asking why the menu won't load**.

2. I'm scrappy in a specific way: I'd rather *research a problem until I can defend a solution* than wait for someone to hand me the answer. I write production Spring Boot for the day job, but I also know what it costs to find a customer, scope a project, ship it, and support it.

3. If you're a founder or tech lead and you need someone who'll own a system end-to-end without theatrics — I'm probably worth a 20-minute call.

**Signature**: `— mohammad yusuf khan · delhi · 2026`

---

## CONTACT SECTION

**Eyebrow**: `Let's build something`

**Heading** (with line break):
> Hire me, or just
> *say hello*.

**Paragraph**: I'm open to senior backend / full-stack roles, full-time or contract. Fastest reply by email.

**CTAs** (in order):
1. **Primary** (solid saffron): `✦ Email me` → `mailto:mohammad.yusufkhan12345@gmail.com`
2. `+91 70374 88868` → `tel:+917037488868`
3. `LinkedIn ↗` → `https://www.linkedin.com/in/m-y-k-/`
4. `GitHub ↗` → `https://github.com/m-y-k`
5. `LeetCode ↗` → `https://leetcode.com/u/myk220897/`

---

## FOOTER
- Left: `© 2026 · Mohammad Yusuf Khan · Built static, hosted free.`
- Right: `Hand-coded HTML + CSS · back to top ↑` (the "back to top" links to `#top`)

---

## PLACEHOLDER URLS (Mohammad will fill in)
| Where | Replace with |
|---|---|
| All 6 site card `href` | The actual live URL of each website |
| LinkedIn CTA | `https://linkedin.com/in/m-y-k-` |
| GitHub CTA | `https://github.com/m-y-k` |
| LeetCode CTA | `https://leetcode.com/u/myk220897/` |
| OG `og:url` meta | The eventual deploy URL (e.g., `https://yusufkhan.dev`) |

If a URL is unknown at build time, leave `href="#"` and add a code comment: `<!-- TODO: replace with [SITE_NAME] live URL -->`
