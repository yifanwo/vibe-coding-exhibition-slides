---
# Global Frontmatter Configuration
theme: default
background:
title: (Vibe) Coding for Curating a Web-Native Exhibition
info: |
  Editorial Neobrutalist Two-Column Slidev Template
fonts:
  sans: 'Plus Jakarta Sans'
  display: 'Syne'
  mono: 'Space Mono'
  weights: '400,500,700,800'
class: text-left
highlighter: shiki
drawings:
  persist: false
transition: slide-up
mdc: false
---

# (Vibe) Coding for Curating a Web-Native Exhibition

<div class="h-24"></div>
Yifan WANG

<div class="h-3"></div>
<span class="ml-3 opacity-72 text-sm">
Assistant Librarian (Digital Humanities)
</span>

<div class="h-2"></div>
<span class="ml-3 opacity-72 text-sm">
HKUST Library
</span>

<div class="pt-8"></div>
<span class="ml-0 opacity-89 text-sm">
2026-11-05 
</span>

<div class="pt-4">
  <span @click="$slidev.nav.next" class="dream-pill cursor-pointer">
   Keys<carbon:arrow-right class="inline"/> <carbon:arrow-down class="inline"/> · Scroll <carbon:arrows-vertical class="inline"/>
  </span>
</div>

---
layout: default
---

# 1. Who am I
<div class="h-4"></div>

<kbd class="neo-kbd">@HKUST-Library/Digital-Strategies/Digital-Scholarship ~</kbd>

<div class="h-4"></div>

### $ Projects/Websites
- https://digitalhumanities.hkust.edu.hk/
- https://library.hkust.edu.hk/ds

<div class="h-4"></div>

### $ Experience
- <span class="neo-box">[digital]</span>Classicist, <span class="neo-box">[computational]</span>Art Historian, <span class="neo-box">[video]</span>Game Researcher
- Contemporary Art Curation, Cultural Governance, Creative Industries: Research & Copywriting & Project Management

---

# 2. A Survey to Shape the Session

###### www.menti.com
###### 5417 3911
<WebPreview src="https://www.menti.com/alzykod7cuwf" height="h-82"/>

---

# 3. Why am I here

### Course-related: 
Hands-on sharing for course project <kbd class="neo-kbd">26FALL "HUMA1660 Introduction to Chinese Art"</kbd>
### Skills:
Interactive Storytelling, Digital Exhibition → Portfolio & Resume
### Methodologies:
- Critical Thinking -> AI-assisted workflows
- DH -> No/[Minimal Coding](https://go-dh.github.io/mincomp/about/)
- Media/Postphenomenology -> Human Agency, Human Autonomy
- Curatorial/Curating: Knowledge Generation & Presentation
### Dark Arts Defense
   - kick things off
     - welcome expand & debug
     - context: task/project-specific; token economical, test the limits/pressure test
   - very personal, experiential
     - no cs/stem orthodox background, textbook terminology/framework
     - authentic, rational, cohesive, consistent, reflective
   - gaming
      <br/><span class="neo-box">/role/digital_humanist</span>
      <br/><span class="neo-box">/mechanics/open-world, sandbox, simulation, strategy, (puzzle{ai riddles}/survival{deadlines})adventure game</span>

---
layout: split-showcase
ratio: left-slim
---

# 4. Scope/Context: Overview

::left::

### `{[(Vibe)]}`Coding
  - AI(assisted/enhanced/empowered): tools + workflow
### Web-native
  - html, css, javascript -> ...
### Exhibition
  - Chinese Art
  - ~ 8 artifacts -> No large database management
  - No 3D assets, No 3D room, No 3D engines
  - Research-oriented, close reading, storytelling -> No Agentic AIs

::right::

### 🏗️ HOW A WEBSITE IS STRUCTURED (FULL-STACK)

```text
┌──────────────────────────────────────────────────────────────┐
│ 📱 FRONTEND — what the user sees (runs in the browser)        │
├──────────────────────────────────────────────────────────────┤
│ Languages     HTML5 / CSS3 / JavaScript / TypeScript         │
│ UI Library    React / Vue / Svelte / Angular / SolidJS       │
│ Meta-Framework Next.js / Nuxt / SvelteKit / Astro / Remix    │
│ Styling       Tailwind CSS / CSS Modules / MUI / Chakra      │
│ State & Data  React Query / Zustand / Redux / Pinia          │
│ Routing       React Router / Vue Router / TanStack Router    │
│ Forms         React Hook Form / Zod / Yup                    │
│ Graphics      Canvas / SVG / D3.js / Three.js / p5.js        │
│ Build & DX    Vite / Webpack / ESLint / Prettier             │
│ Testing       Vitest / Jest / Testing Library / Playwright   │
└───────────────────────────┬──────────────────────────────────┘
                            │
             🌐 HTTP / REST / GraphQL / WebSockets / tRPC
                            │
┌───────────────────────────▼──────────────────────────────────┐
│ ⚙️ BACKEND — business logic, APIs, and server-side concerns   │
├──────────────────────────────────────────────────────────────┤
│ Runtimes      Node.js / Deno / Bun / Python / Ruby / PHP    │
│ Frameworks    Express / Fastify / NestJS / Hono              │
│               Django / FastAPI / Flask                       │
│               Rails / Laravel / Spring Boot / ASP.NET Core   │
│ API Styles    REST / GraphQL / tRPC / WebSockets             │
│ Auth          Auth0 / Clerk / Passport / JWT / OAuth         │
│ CMS (coupled) WordPress / Drupal / Joomla                    │
│ CMS (headless) Contentful / Sanity / Strapi / Hygraph        │
│ Validation    Zod / Joi / Yup / class-validator              │
│ Background    BullMQ / Celery / Sidekiq / Temporal           │
└───────────────────────────┬──────────────────────────────────┘
                            │
          🗄️ SQL / ORM / Query Builder / Cache / Queue
                            │
┌───────────────────────────▼──────────────────────────────────┐
│ 💾 DATA & PERSISTENCE — storage, retrieval, and async work    │
├──────────────────────────────────────────────────────────────┤
│ Relational DB PostgreSQL / MySQL / SQLite                    │
│ NoSQL DB      MongoDB / DynamoDB / Cassandra                 │
│ Cache         Redis / Memcached                              │
│ ORM / Query   Prisma / Drizzle / TypeORM / Kysely            │
│               SQLAlchemy / Django ORM / ActiveRecord         │
│ Migrations    Prisma Migrate / Drizzle Kit / Alembic         │
│ Object Storage S3 / Cloudinary / GCS / Supabase Storage      │
│ Message Queue RabbitMQ / Kafka / NATS / Redis Streams        │
└───────────────────────────┬──────────────────────────────────┘
                            │
          🖥️ reverse proxy / TLS / static file serving
                            │
┌───────────────────────────▼──────────────────────────────────┐
│ 🖥️ WEB SERVER & EDGE — the first process that receives a     │
│    request before it reaches your application code            │
├──────────────────────────────────────────────────────────────┤
│ Reverse Proxy Nginx / Caddy / Apache / HAProxy               │
│ Edge Runtime  Cloudflare Workers / Vercel Edge / Deno Deploy │
│ CDN           Cloudflare / Fastly / AWS CloudFront           │
└───────────────────────────┬──────────────────────────────────┘
                            │
          🚀 build / test / deploy / observe
                            │
┌───────────────────────────▼──────────────────────────────────┐
│ 🚀 DELIVERY & OPERATIONS — how code goes from repo to user     │
├──────────────────────────────────────────────────────────────┤
│ Version       Git / GitHub / GitLab / Bitbucket              │
│ CI / CD       GitHub Actions / GitLab CI / Jenkins / CircleCI│
│ Containers    Docker / Podman / Kubernetes                   │
│ Hosting       Vercel / Netlify / Cloudflare Pages            │
│               Railway / Render / Fly.io                      │
│               AWS / GCP / Azure / DigitalOcean               │
│ Monitoring    Sentry / Datadog / Grafana / New Relic         │
│ Logging       Grafana Loki / ELK / Datadog Logs              │
└──────────────────────────────────────────────────────────────┘
```

> co-worked with `Google AI` and `Copilot`, generated with `DeepSeek`

---
layout: split-showcase
ratio: left-slim
---

# 5. Scope/Context: Architecture

::left::

### `{[(Vibe)]}`Coding
  - AI(assisted/enhanced/empowered): tools + workflow
### Web-native
  - html, css, javascript -> ...
### Exhibition
  - Chinese Art
  - ~ 8 artifacts -> No large database management
  - No 3D assets, No 3D room, No 3D engines
  - Research-oriented, close reading, storytelling -> No Agentic AIs

::right::
### 🗺️ ARCHITECTURAL PATHS
- every lane produces a website; the choice is where HTML is generated, where state lives, and who operates the server

```text
┌──────────────────────────────────────────────────────────────┐
│ 🅰 PLAIN HTML / CSS / JS — no build, no runtime              │
├──────────────────────────────────────────────────────────────┤
│ HTML written directly · CSS · vanilla JS                     │
│ Build: none                                                  │
│ Host: any static host / even a local file                    │
│ Best for: single pages, prototypes, teaching, zero deps      │
│ Tools: none beyond the browser                               │
│ +  zero setup — a file and a browser is the whole stack      │
│ −  repeated content is copy-paste                            │
└──────────────────────────────────────────────────────────────┘
┌──────────────────────────────────────────────────────────────┐
│ 🅱 STATIC SITE GENERATOR (SSG) — HTML built at build time    │
├──────────────────────────────────────────────────────────────┤
│ Tools: Astro · Hugo · Eleventy (Build Awesome) · Jekyll ·    │
│ VitePress · Docusaurus · Zola · SvelteKit (export) ·         │
│ Next.js (export)                                             │
│ Build:  one command → folder of ready HTML/CSS/JS            │
│ Host: static host / CDN                                      │
│ Best for: blogs, docs, marketing, content sites              │
│ +  content in markdown, one template for all pages           │
│ +  fast, cheap, SEO-friendly, no server to secure            │
│ −  build step to learn · rebuild on content change           │
└──────────────────────────────────────────────────────────────┘
┌──────────────────────────────────────────────────────────────┐
│ 🅲 SINGLE PAGE APPLICATION (SPA) — HTML rendered in browser   │
├──────────────────────────────────────────────────────────────┤
│ Tools: React · Vue · Angular · Svelte · SolidJS + Vite       │
│ Build: Vite / Webpack / framework CLI                        │
│ Host: static host (needs JS to render)                       │
│ Best for: dashboards, editors, app-like interactivity        │
│ +  one codebase, largest ecosystem and AI training data      │
│ −  blank page without JS · weaker SEO, slower first paint    │
└──────────────────────────────────────────────────────────────┘
┌──────────────────────────────────────────────────────────────┐
│ 🅳 SERVER-SIDE RENDER (SSR) — HTML rendered on a server       │
├──────────────────────────────────────────────────────────────┤
│ Tools: Next.js · Nuxt · SvelteKit · Remix · TanStack Start   │
│         Rails · Django · Laravel · Spring · ASP.NET + HTMX   │
│ Modes: per request (SSR) · cached (ISR) · mixed per route    │
│ Host: Node runtime / serverless / edge                       │
│ Best for: personalized, request-time, SEO-critical apps      │
│ +  fresh data per request, SEO-friendly, secrets server-side │
│ −  a server to run, pay for, and keep warm                   │
└──────────────────────────────────────────────────────────────┘
┌──────────────────────────────────────────────────────────────┐
│ 🅴 VISUAL / NO-CODE BUILDER — no code, platform-owned         │
├──────────────────────────────────────────────────────────────┤
│ Tools:  Webflow · Framer · Wix · Squarespace · Weebly ·      │
│         Google Sites · Canva Websites                        │
│ Build:  none — drag, drop, publish                           │
│ Host:   bundled with the platform (paid tiers)               │
│ Best for: non-coders, small business, design-led landing     │
│ +  fastest route from idea to a polished, responsive site    │
│ −  no code ownership · export and lock-in limits             │
└──────────────────────────────────────────────────────────────┘
```

> co-worked with `DeepSeek`, `Google AI`, and `Copilot`.

---
layout: split-showcase
ratio: left-slim
---

# 6. Scope/Context: Streamline

::left::

### `{[(Vibe)]}`Coding
  - AI(assisted/enhanced/empowered): tools + workflow
### Web-native
  - html, css, javascript -> ...
### Exhibition
  - Chinese Art
  - ~ 8 artifacts -> No large database management
  - No 3D assets, No 3D room, No 3D engines
  - Research-oriented, close reading, storytelling -> No Agentic AIs
### Methodologies
  - open-tools/source - <span class="neo-mark">own codes</span>
  - open-access/publishing - <span class="neo-mark">no paywall</span>
  <br/>*creative commons - copyright →*
  - critical thinking & reflective making
  - <kbd class="neo-kbd">curating/curatorial</kbd> as meaning-making

::right::

### 🔀 DECISION FLOW

```text
┌────────────────────────────────────────────────────────┐
│ Own and Write the code?                                │
└──────────────┬─────────────────────────┬───────────────┘
            no │                     yes │
               ▼                         ▼
   ┌─────────────────────┐  ┌─────────────────────────────┐
   │ 🅴 VISUAL BUILDER   │  │ Own and operate a server?    │
   └─────────────────────┘  └──────┬──────────────────┬───┘
                                no │              yes │
                                   ▼                  ▼
                          ┌─────────────────────┐  ┌────────────────────┐
                          │ mostly static,      │  │ 🅳 SERVER-RENDERED  │
                          │ or app-like         │  └────────────────────┘
                          │ interactivity?      │
                          └───┬─────────────┬───┘
                       static │     app-like│
                              ▼             ▼
                    ┌──────────────┐  ┌──────────┐
                    │ 🅰 PLAIN HTML │  │ 🅲 SPA    │
                    │ 🅱 SSG        │  └──────────┘
                    └──────────────┘
                              └───────┬───────┘
                                  **HYBRID**
```

> co-worked with `DeepSeek`

---
layout: split-showcase
ratio: left-slim
---

# 7. Streamline: Lifecycle Phases

::left::

### `{[(Vibe)]}`Coding
  - AI(assisted/enhanced/empowered): tools + workflow
### Web-native
  - html, css, javascript -> ...
### Exhibition
  - Chinese Art
  - ~ 8 artifacts -> No large database management
  - No 3D assets, No 3D room, No 3D engines
  - Research-oriented, close reading, storytelling -> No Agentic AIs
### Methodologies
  - open-tools/source - <span class="neo-mark">own codes</span>
  - open-access/publishing - <span class="neo-mark">no paywall</span>
  <br/>*creative commons - copyright →*
  - critical thinking & reflective making
  - <kbd class="neo-kbd">curating/curatorial</kbd> as meaning-making


::right::

### 🔄 Project-specific Lifecycle

```text
┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
│ 1. RESEARCH  │──>│ 2. DESIGN    │──>│ 3. DEVELOP   │──>│ 4. BUILD     │
├──────────────┤   ├──────────────┤   ├──────────────┤   ├──────────────┤
│ Contents     │   │ Wireframes   │   │ HTML/CSS     │   │ Vite         │
│ Metadata     │   │ Storyboards  │   │ React        │   │ TypeScript   │
│ Images       │   │ UX/UI Flow   │   │ Github Repos │   │ Next.js      │
│ Narratives   │   │ Architecture │   │ Cursor/Replit│   │ Node.js      │
└──────────────┘   └──────────────┘   └──────────────┘   └──────┬───────┘
      │                                                         │
      ▲            ┌──────────────┐   ┌──────────────┐   ┌──────▼───────┐
      └──────  ◄ ──│ 7. ITERATE   │<──│ 6. DEPLOY    │<──│ 5. TEST      │
                   ├──────────────┤   ├──────────────┤   ├──────────────┤
                   │ Analytics/SEO│   │ Github       │   │ Accessibility│
                   │ Feedbacks    │   │ Netlify      │   │ Performance  │
                   │ Reflections  │   │ Vercel       │   │ Devices      │
                   │ Maintenance  │   │ Cloudflare   │   │ Responsiveness│
                   └──────────────┘   └──────────────┘   └──────────────┘
```

### 🚏 Checkpoint
- each phase can be AI-assisted/enhanced
- human-in-the-loop, orchestration on models & tasks

---
layout: split-showcase
ratio: left-slim
---

# 8. Phase 1: RESEARCH

::left::

```text
┌───────────────┐
│ 1. RESEARCH   │
├───────────────┤
│ Contents      │
│ Metadata      │
│ Images        │
│ Narratives    │
└────────┬──────┘
         │
         ▼
```

::right::

### 📣 Research-based, Research-Oriented 
**AI tools for Your Research**
  - [HKUST Library - AI Literacy for End-Users: Use AI Wisely](https://libguides.hkust.edu.hk/ai-literacy/use-wisely)
  - [A Snapshot of GenAI Tools for Research](https://asterzhao.github.io/ai-research-tools-snapshot/)
  - [Scite & Consensus MCP](https://library.hkust.edu.hk/news-events/news/connect-your-ai-tools-trusted-scholarly-resources-introducing-scite-consensus-mcp)

<div class="h-4"></div>

### 💪 Project Management 
**From Research to Deliverable Contents**
1. Curatorial (Visual + Interactive) Narrative:
    - Research Question -> Research Essay -> Storyline/Storyboards
    - e.g. Real-world Exhibitions
    - A collection (https://dpul.princeton.edu/japanese2026/feature/the-early-to-mid-20th-century)
  <br/>→ An [exhibition](https://theme.npm.edu.tw/exh109/She/en/page-1.html) 
  <br/>→ [More interactive](https://news.cgtn.com/event/2022/The-Song-Painted/index.html?num=0)
2. Components: 
    - Hypertext + Images + <span class="neo-mark">Non-linear + Interconneted + Transition</span>
3. Inventory Management -> <kbd class="neo-kbd">Object-Oriented</kbd>
    - **texts**: title, artist, date, medium, origin, provenance, short intro, long analysis, labels, categories/relation, reference, further reading, links...
    - **images**: hero, details, assets, (models), (processed img)...
    - **metadata**

---
layout: split-showcase
ratio: left-slim
---

# 9. Phase 2: DESIGN

::left::

```text
┌───────────────┐
│ 2. DESIGN     │
├───────────────┤
│ Wireframes    │
│ Storyboards   │
│ UX/UI Flow    │
│ Architecture  │
└────────┬──────┘
         │
         ▼
```

::right::

### Toolkits

- [Wireframe](https://www.figma.com/resource-library/what-is-wireframing/)
- Moodboard: 
  - Notion, Canva Whiteboard, Miro...
### Inspirations/Resources:
  - https://www.awwwards.com/
  - https://land-book.com/
  - https://www.landing.gallery/
  - https://motionsites.ai/
  - https://recent.design/
  - https://www.inspora.design/

### Prompts w/ AIs
- https://www.scrolltide.co/
- https://onepromptdesign.com/
- https://refero.design/
- ...

### Design System
- Grid System, Color platte, Typography
- Visual Structure, Visual Style
- Concise (readable, avoid redundancy)

---
layout: split-showcase
ratio: left-wide
---

# 10. - BRANCH - MinimalComputing

::left::

### General: DH Open Source Tools for Digital Collections
| **Scalar**

<WebPreview src="https://scalar.me/anvc/scalar/showcase/" height="h-30" />

| **Omeka**

<WebPreview src="https://info.omeka.net/showcase/" height="h-30" />

| [Telar](https://telar.org/) [showcase](https://landscapes.telar.org/)
| [Wax](https://minicomp.github.io/wiki/wax/) [showcase](https://stylerevolution.github.io/)
| [More tools](https://atla.libguides.com/digitizing-collections/online-content-platforms)

::right::

### Specific: Interactive Visual Novel
| **Twine**
  - ✨ .twee -> .html
  - ✨ nonlinear,gamifying, story-rich
  - archaeology/art history/history, interactive exhibition
  - **[guide](https://lotte-w.github.io/Twine-Workshop-Guide/)**
  - [basic syntax](https://www.futurelearn.com/info/courses/fundamentals-of-creative-technologies-and-interactive-experiences/0/steps/451384)
  - [blogs](https://review.gale.com/2024/06/25/building-interactive-narratives-with-twine/)
  - [showcase](https://itch.io/games/tag-twine)

<br/>*ai-assisted draft - embedded to html →*

---
layout: split-showcase
ratio: left-slim
---

# 11. Phase 3: DEVELOP - Paths

::left::

```text
┌───────────────┐
│ 3. DEVELOP    │
├───────────────┤
│ HTML/CSS/JS   │
│ React         │
│ Github Repos  │
│ Cursor/Replit │
└────────┬──────┘
         │
         ▼
```

::right::

<div class="h-4"></div>

### Path 1: Github Repository -> Fork

<div class="h-4"></div>

### Path 2: Reverse Engineering 1 -> (half)Scratch

<div class="h-4"></div>

### Path 3: Prompt -> Site Generation

<div class="h-4"></div>

### Path 4: NL -> Coding Agent

<div class="h-4"></div>

### Path 5: (NL + Prompt) Scroll + Style -> html

<div class="h-4"></div>

### Path 6: NL -> Twine -> html

<div class="h-4"></div>

### Path 7: Reverse Engineering 2 -> (hybrid)Scratch

---
layout: split-showcase
ratio: left-wide
---

# 12. Phase3/DEVELOP/Path 1

::left::

### Path 1: Github Repository -> Fork

<WebPreview src="https://tympanus.net/Tutorials/InfiniteCanvas/" height="h-82" />

::right::

### Github

https://github.com/edoardolunardi/infinite-canvas

---
layout: split-showcase
ratio: equal
---

# 13. Phase3/DEVELOP/Path 2

::left::

### Path 2: Reverse Engineering 1 -> (half)Scratch

In the example of:
- https://tympanus.net/Tutorials/InfiniteCanvas/
- https://github.com/edoardolunardi/infinite-canvas

<div class="h-4"></div>

Built:

https://library.hkust.edu.hk/ds-colab/p005/infinite-canvas/

::right::

### Poe/`Claude Sonnet 4.6`:

- plan project structure: the first draft
```text
infinite-canvas/
├── public/
│   └── images/             ← drop all 75 images here
│       ├── 001.jpg
│       ├── 002.jpg  ... (75 total)
├── src/
│   ├── types.ts            ← shared TypeScript interfaces
│   ├── data/
│   │   └── images.ts       ← YOUR ONLY MAINTENANCE FILE
│   ├── utils/
│   │   ├── layout.ts       ← auto-computes 3D positions
│   │   └── dragState.ts    ← tiny shared state module
│   ├── shaders/
│   │   └── photo.ts        ← GLSL vertex + fragment shaders
│   ├── components/
│   │   ├── PhotoMesh.tsx   ← single image plane
│   │   ├── CameraController.tsx  ← drag + scroll + inertia
│   │   └── Scene.tsx       ← canvas + fog + all photos
│   ├── App.tsx
│   ├── main.tsx
│   └── index.css
└── package.json
```
- work on assets: /public/image
- fine-tune: tile, transparency, hover, canvas...
- limits: conversation length, forgetting, misjudgement

---
layout: default
---

# 14. Phase3/DEVELOP/-Loop

### Path 3 - 7 : Project Demo - DScape MiniArchive

<div class="h-3"></div>

<span class="neo-box">LOOP</span>

### Phase 1: Research -> Contents Preparation
  - objects.json
      > w/ `DeepSeek`
  - images processing photos
      > w/ `GPT-Image 2.5` & `Grok-Imagine-2`
  - (to be finished) 2.5D Three.js assets
      > w/ `Gemini 4 Argon`
  - storyline.md
      > w/ `DeepSeek`

<div class="h-4"></div>

### Phase 2: Design
  - references/inspirations
  - preferred styles, color palette, typography, layout

---
layout: split-showcase
ratio: equal
---

# 15. Phase3/DEVELOP/Path 3

::left::

### Path 3: Prompt -> Site Generation

- Prompt from [Motionsites](https://motionsites.ai/3d-websites?prompt=feathers-atlas)

<WebPreview src="https://motionsites.ai/3d-websites?prompt=feathers-atlas" height="h-44" />

<div class="h-4"></div>

- Prompt tailored to project
  - produce a skill.md if needed
  > w/ `DeepSeek`

::right::

### Prototype

*Using the same prompt and skill produces similar webpages across various AI tools.*

<WebPreview src="https://yifanwo.github.io/dscape-archive/1.0.3.html" height="h-72" />

> w/ `Cursor - Grok4.7`

---
layout: split-showcase
ratio: left-slim
---

# 16. Phase3/DEVELOP/Path 4

::left::

### Path 4: NL -> Coding Agent
- cover/header for reference: https://doingsts.com/
- img + json
- let it design hover, animation, scroll, interaction, info card prompt

::right::

### Prototype

<WebPreview src="https://yifanwo.github.io/dscape-archive/1.0.4.html" height="h-72" />

> w/ `Cursor - Grok4.7`
---
layout: split-showcase
ratio: left-slim
---

# 17. Phase3/DEVELOP/Path 5

::left::

### Path 5: (NL + Prompt) Scroll + Style -> html

NL -> Prompt -> Test
- Style: Particle, ASCII
- GSAP Scroll

> w/ `DeepSeek`
> 
<div class="h-4"></div>

### reference:
- ASCII animation [shark-stackedlol](https://x.com/insporadesign/status/2113519530387681343)

::right::

### Prototype

### 1. PARTICLE

<WebPreview src="https://yifanwo.github.io/dscape-archive/1.0.5-1.html" height="h-72" />

> w/ `Gemini 4 Argon`

<div class="h-4"></div>

### 2. ACID PARTICLE + **Scroll Sections**

<WebPreview src="https://yifanwo.github.io/dscape-archive/1.0.5-2.html" height="h-72" />

> w/ `MiniMax`

<div class="h-4"></div>

<WebPreview src="https://yifanwo.github.io/dscape-archive/1.0.5-3.html" height="h-72" />

> w/ `Gemini 4 Argon`

<div class="h-4"></div>

### 3. ASCII + **Storyline**
<WebPreview src="https://yifanwo.github.io/dscape-archive/1.0.5-4.html" height="h-72" />
> w/ `Gemini 4 Argon`

---
layout: split-showcase
ratio: left-slim
---

# 18. Phase3/DEVELOP/Path 6

::left::

### Path 6: NL -> Twine -> html

Ask:
- create .twee
- visual style

::right::

### Prototype

<WebPreview src="https://yifanwo.github.io/dscape-archive/1.0.6-1.html" height="h-72" />

> w/ `Grok Bot`

<div class="h-4"></div>

<WebPreview src="https://yifanwo.github.io/dscape-archive/1.0.6-2.html" height="h-72" />

> w/ `Gemini 4 Argon`

---
layout: split-showcase
ratio: left-slim
---

# 19. Phase3/DEVELOP/Path 7

::left::

### Path 7: Reverse Engineering 2 -> (hybrid)Scratch

### ↓ Sketch: 
> (hand draw / figma, canva...) simple wireframe
<div class="h-3"></div>

### ↓ Study: 
https://unifiersofjapan.framer.website/
> w/ `Gemini 4 Argon`
<div class="h-3"></div>

### ↓ Generate Prototype
> w/ ~Gemini 4 Argon`
<div class="h-3"></div>

### ↓ Edits
> w/ `Gemini 4 Argon` + local `Qwen 3.6`

::right::

### Prototype

```text
npm run dev
```

<div class="h-4"></div>

<WebPreview src="https://yifanwo.github.io/dscape-archive/1.0.7.html" height="h-72" />

---
layout: split-showcase
ratio: left-slim
---

# 20. Phase 4/5: BUILD/TEST

::left::

```text
┌───────────────┐
│ 4. BUILD      │
├───────────────┤
│ Vite          │
│ TypeScript    │
│ Next.js       │
│ Node.js       │
└────────┬──────┘
         │
         ▼
┌───────────────┐
│ 5. TEST       │
├───────────────┤
│ Accessibility │
│ Performance   │
│ Devices       │
│ Responsiveness│
└────────┬──────┘
         │
         ▼
```

::right::

### Edits

- (hybrid)Scratch
- handicraft
- human review

> Vscode + Roo/Kilo (`Qwen3.6`)

---
layout: split-showcase
ratio: left-slim
---

# 21. Phase 6: DEPLOY

::left::

```text
┌───────────────┐
│ 6. DEPLOY/PUBLISH│
├───────────────┤
│ GitHub        │
│ Vercel        │
│ Cloudflare    │
│ Netlify       │
└────────┬──────┘
         │
         ▼
```

::right::

### Examples

- https://charming-belekoy-7350e3.netlify.app/
- https://hkust-lib-ds.github.io/dscape1.0-beta/
- https://canton1945-infinite-canvas.pages.dev/

```text
┌──────────────┬───────────────────────┬──────────────────────────────┐
│ HOST         │ WHAT YOU GET          │ BACKEND / SERVER?            │
├──────────────┼───────────────────────┼──────────────────────────────┤
│ GitHub Pages │ static files only     │ ✕ none possible. No backend, │
│              │                       │   no functions, no database. │
│              │                       │   Pure 🅰/🅱/🅲 only.       │
├──────────────┼───────────────────────┼──────────────────────────────┤
│ Cloudflare   │ static + optional     │ ✓ add a /functions folder →  │
│ Pages        │ Pages Functions       │   deploys automatically,     │
│              │                       │   same domain, you never see │
│              │                       │   or patch a server          │
├──────────────┼───────────────────────┼──────────────────────────────┤
│ Vercel       │ static + optional     │ ✓ add an /api folder →       │
│              │ serverless functions  │   same domain, auto-scaled,  │
│              │                       │   you never manage a server  │
├──────────────┼───────────────────────┼──────────────────────────────┤
│ Netlify      │ static + optional     │ ✓ Serverless functions +     │
│              │ forms & identity      │   built-in form handling     │
│              │                       │   (very beginner-friendly)   │
└──────────────┴───────────────────────┴──────────────────────────────┘
```

> explained by `DeepSeek`

---
layout: split-showcase
ratio: left-slim
---

# 22. Phase 7: ITERATE

::left::

```text
┌───────────────┐
│ 7. ITERATE    │
├───────────────┤
│ Analytics/SEO │
│ Feedbacks     │
│ Reflections   │
│ Maintenance   │
└────────┬──────┘
         │
         ▼
```

::right::

### ! ATTENTION

[Vibe Coding Literacy](https://libguides.lib.hku.hk/AI-literacy/vibe-coding)
- **human review**
  - errors, inefficiencies, or security vulnerabilities
  - quality and maintainability
  - precise requirements and oversight
- **practice guidelines**
  - Give clear, specific prompts: Avoid ambiguity; detailed requests yield better results.
  - Break tasks into steps: Let AI handle one focused item at a time for more precise output.
  - Iterate incrementally: Start simple and add complexity in stages.
  - Employ version control: Regularly checkpoint progress to allow easy rollback.
  - Thoroughly review and test AI code: Don’t deploy without rigorous validation, particularly for security.
  - Adopt secure coding habits: Never hardcode sensitive info; use environment variables and authentication.
  - Combine AI with human expertise: Utilise vibe coding to accelerate development, but constantly review for quality, maintainability, and security.
  - Invest in prompt engineering: Good prompts are key to reliable AI output.
  - Document everything: Make sure code choices and project structure are clear for future collaborators.

[Copyright, Privacy, Credits](https://libguides.hkust.edu.hk/ai-literacy/copyright)

---
layout: default
---

# 23. Itsy-bitsies

### 1. DE-AI: 
  no demo of ClaudeCode/Codex, but if you want to work with them, consider skills & counterskills, e.g. [taste skill](https://www.tasteskill.dev/) & (https://impeccable.style/)

### 2. Polish: 
  ai-slop easy-spotted, no pains, no gains

### 3. Timeline:
  ⏳slow-cooked preparing, ⚡quick rendering, ⏳ long editing

### 4. Credits:
  even reference screencaps that fed AIs

### 5. Logs:
  version tracks, metadata, working logs, **! multi-tasking across various AIs**

### 👉 NEXT:
  Present your work on [DHI website](https://digitalhumanities.hkust.edu.hk/) and [DHI Repos](https://github.com/HUMA5630-Digital-Humanities), share your *exploration journey* on DHI Website.

---

# 24. Re-thinking `{[(Vibe)]}` Coding

### [Nintendo’s Shigeru Miyamoto](https://www.videogameschronicle.com/news/shigeru-miyamoto-explains-why-ai-wont-make-human-creativity-obsolete/):
> “While the act of creation is inherently satisfying, there’s a danger: one might find satisfaction in the labor itself and mistakenly believe that a high-quality piece of work has been created,” he said. “In that sense, the more AI replaces these tasks, the more it provides an opportunity to reflect on what’s really important, which I think is a positive thing.”
> <div class="h-3"></div>
> 
> “Looking back at past designs, there are some that were created merely by copying and pasting. Yet, such work rarely stands the test of time; it lacks the individual’s particular design intention,” Miyamoto said.

<div class="h-4"></div>

### [Enduring Methods for an Emerging Medium: The Generative AI Studio](https://gail.wharton.upenn.edu/research-and-insights/enduring-methods-emerging-medium/)
> The crit is a path to discernment.
> <div class="h-3"></div>
> 
> Management skills matter.
> <div class="h-3"></div>
> 
> Building too early is a trap.
> <div class="h-3"></div>
> 
> Enduring methods can unlock emerging technologies.

---

# 25. Thank you

### Questions & Comments:
### ↓
### lbyifan@ust.hk

<hr class="my-12 border-[#D83B78]/25" />

### Presented with Slidev (markdown + vue + vite)
###### layout/implementation assistance: `Gemini 4 Argon`
###### deploy/debug assistance: `GPT-5.6 Sol`