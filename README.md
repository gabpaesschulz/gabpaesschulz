<p align="center">
  <img src="./assets/header.svg" width="100%" alt="Gabriel Paes Schulz — Fullstack Developer · Open-source Builder · Product-minded Engineer"/>
</p>

<p align="center">
  <a href="https://linkedin.com/in/gabrielpaesschulz">
    <img src="https://img.shields.io/badge/LinkedIn-gabriel--paes--schulz-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="mailto:gabriel_paes@live.com">
    <img src="https://img.shields.io/badge/Email-gabriel__paes@live.com-ea4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
  </a>
</p>

---

I build backend systems that don't fall apart, frontend interfaces that don't feel like an afterthought, and developer tools that remove the boring glue between good libraries.

**4+ years** modernizing corporate systems — legacy migrations, financial workflows, REST integrations, query optimization, internal tools and production support. Off the clock, I ship my own products and open-source tooling, usually around one theme: turning repetitive engineering pain into something cleaner, typed and reusable.

> I care about **code that communicates intent**, **architecture that survives its own growth**, and **products that feel like someone actually thought about the person using them**.

<br/>

## ✦ Selected Work

### `FilterBridge` — schema-first filters for React admin screens

<a href="https://www.npmjs.com/package/@filterbridge/core"><img src="https://img.shields.io/badge/npm-@filterbridge%2Fcore-cb3837?style=flat-square&logo=npm&logoColor=white" alt="npm"/></a>
<a href="https://filterbridge-demo.vercel.app"><img src="https://img.shields.io/badge/Live_Demo-111827?style=flat-square&logo=vercel&logoColor=white" alt="demo"/></a>
<a href="https://github.com/gabpaesschulz/filterbridge/releases/tag/v0.1.0"><img src="https://img.shields.io/badge/release-v0.1.0-5eead4?style=flat-square&logo=github&logoColor=white&labelColor=111827" alt="release"/></a>

Admin dashboards repeat the same filter logic across React state, URL params, backend DTOs and table filters. **Declare it once** — reuse the typed schema everywhere.

```ts
const filters = defineFilters({
  search: text(),
  status: select(["draft", "pending", "paid", "failed"]),
  tags:   multiSelect(["urgent", "recurring", "manual-review"]),
})

const dto    = toQueryDto(filters, state)     // → backend
const params = toSearchParams(filters, state) // → URL
```

Shipped as a pnpm monorepo of **5 packages** (`core` · `react` · `browser` · `tanstack` · `next`), with ESM/CJS output, type declarations, Vitest smoke tests and a live demo.

<br/>

### `hookform-action` — the missing layer between React Hook Form and your server

<a href="https://www.npmjs.com/package/hookform-action-core"><img src="https://img.shields.io/badge/npm-hookform--action--core-cb3837?style=flat-square&logo=npm&logoColor=white" alt="npm"/></a>
<a href="https://hookform-action-docs.vercel.app/"><img src="https://img.shields.io/badge/Docs_&_Demo-111827?style=flat-square&logo=vercel&logoColor=white" alt="docs"/></a>

Every project re-writes the same wiring to connect a form to a server action: `useTransition`, FormData serialization, Zod error mapping, `setError()` calls, pending state. I abstracted it away.

```ts
const { register, handleSubmit, formState } =
  useActionForm(loginAction, { validationMode: "onChange" })
```

Full TypeScript inference, optimistic UI with rollback, multi-step wizard persistence, a floating DevTools panel and automated tests.

```bash
npm i hookform-action-core
```

<br/>

### `Aprovado.ai` — PDF → Anki flashcards in under 60s, powered by LLMs

<a href="https://aprovadoai-1ol7.vercel.app"><img src="https://img.shields.io/badge/status-live_in_production-22c55e?style=flat-square&logo=vercel&logoColor=white&labelColor=111827" alt="live"/></a>

Built end-to-end: Next.js + TypeScript, LLM API integration, freemium model with three tiers, payment gateway (card · PIX · boleto) and CI/CD on Vercel.

> Not a tutorial clone. Not just a landing page. A real product with pricing, payment flow and usage intent.

<br/>

## ✦ Also in the Lab

| | Project | What it is |
|---|---|---|
| 🪦 | [**Graveyard**](https://github.com/gabpaesschulz/graveyard) | A digital memorial for abandoned projects — death certificates, epitaphs, a funeral wizard. Next.js 15 · Prisma · Postgres · Framer Motion. *"The projects that didn't work taught me more than the ones that did."* |
| 💰 | [**FreedomCalc**](https://github.com/gabpaesschulz/freedomcalc) | Local-first FIRE & compound-interest planner. Zero servers, AES-256 in localStorage, PIN lock, PWA-ready. |
| 🎬 | [**Watch Planner**](https://github.com/gabpaesschulz/letterbox-scrapper) | Turns any Letterboxd list into a personalized watch schedule. TMDB enrichment · drag-and-drop calendar · `.ics` export. |
| 🎤 | [**Setlist**](https://github.com/gabpaesschulz/setlist) | Concert & festival lifecycle planner with budget guardrails and predictive alerts. IndexedDB-first, offline-capable. |

<br/>

## ✦ Stack

**Backend**&nbsp;&nbsp;
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Quarkus](https://img.shields.io/badge/Quarkus-4695EB?style=flat-square&logo=quarkus&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

**Frontend**&nbsp;&nbsp;
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Data**&nbsp;&nbsp;
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)

**Craft & DevOps**&nbsp;&nbsp;
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
&nbsp;·&nbsp; TDD · SOLID · Clean Code · Hexagonal Architecture

<br/>

## ✦ GitHub

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=gabpaesschulz&show_icons=true&hide_border=true&theme=tokyonight&count_private=true&include_all_commits=true" alt="stats"/>
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=gabpaesschulz&layout=compact&hide_border=true&theme=tokyonight&langs_count=8" alt="top langs"/>
</p>

<br/>

<p align="center"><em>"Persistence beats intensity when consistency stays in the game."</em></p>
