<div align="center">

# Gabriel Paes Schulz

**Fullstack Developer · Open-source Builder · Product-minded Engineer**

*Java · TypeScript · React · Next.js · Quarkus · Spring Boot*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-gabriel--paes--schulz-0a66c2?style=flat-square\&logo=linkedin)](https://linkedin.com/in/gabrielpaesschulz)
[![Email](https://img.shields.io/badge/Email-gabriel__paes@live.com-ea4335?style=flat-square\&logo=gmail)](mailto:gabriel_paes@live.com)
[![npm](https://img.shields.io/badge/npm-%40filterbridge%2Fcore-cb3837?style=flat-square\&logo=npm)](https://www.npmjs.com/package/@filterbridge/core)
[![Demo](https://img.shields.io/badge/Demo-FilterBridge-111827?style=flat-square\&logo=vercel)](https://filterbridge-demo.vercel.app)

</div>

---

I build backend systems that do not fall apart, frontend interfaces that do not feel like an afterthought, and developer tools that remove the boring glue between good libraries.

I have 4+ years of experience building and modernizing corporate systems: legacy migrations, financial workflows, RESTful integrations, query optimization, dashboards, internal tools and production support.

Outside work, I ship my own products and open-source tools — from npm libraries to SaaS experiments — usually around the same theme: turning repetitive engineering pain into something cleaner, typed and reusable.

I care about code that communicates intent.
About architecture that survives its own growth.
About products that feel like someone actually thought about the person using them.

---

## ⚡ Things I've shipped

---

### [FilterBridge](https://github.com/gabpaesschulz/filterbridge) · *OSS TypeScript library*

> Schema-first filters for React admin screens.

Admin dashboards often repeat the same filter logic across React state, URL search params, backend DTOs and table filters. FilterBridge lets you declare filters once and reuse that typed schema across those layers.

Published as a pnpm monorepo with 5 npm packages:

| Package                                                                          | Purpose                                                           |
| -------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| [`@filterbridge/core`](https://www.npmjs.com/package/@filterbridge/core)         | Filter DSL, parsing, URL serialization and backend DTO generation |
| [`@filterbridge/react`](https://www.npmjs.com/package/@filterbridge/react)       | `useFilterBridge` hook for local filter state                     |
| [`@filterbridge/browser`](https://www.npmjs.com/package/@filterbridge/browser)   | Browser URL synchronization helpers                               |
| [`@filterbridge/tanstack`](https://www.npmjs.com/package/@filterbridge/tanstack) | TanStack Table adapter                                            |
| [`@filterbridge/next`](https://www.npmjs.com/package/@filterbridge/next)         | Next.js App Router search params adapter                          |

Built with TypeScript, tsup, Vitest, ESM/CJS output, declaration files, smoke tests and a public Vercel demo.

```ts
import {
  defineFilters,
  multiSelect,
  parseFilters,
  select,
  text,
  toQueryDto,
  toSearchParams,
} from "@filterbridge/core"

const filters = defineFilters({
  search: text(),
  status: select(["draft", "pending", "paid", "failed"]),
  tags: multiSelect(["urgent", "recurring", "manual-review"]),
})

const state = parseFilters(filters, {
  search: "acme",
  status: "paid",
  tags: "urgent,recurring",
})

const dto = toQueryDto(filters, state)
const params = toSearchParams(filters, state)
```

[Live demo](https://filterbridge-demo.vercel.app) · [npm](https://www.npmjs.com/package/@filterbridge/core) · [v0.1.0 release](https://github.com/gabpaesschulz/filterbridge/releases/tag/v0.1.0)

---

### [hookform-action](https://github.com/gabpaesschulz/hookform-action) · *OSS library*

> The missing layer between React Hook Form and your server.

The same boilerplate tends to appear in every project that connects React Hook Form to a server action: `useTransition`, FormData serialization, Zod error mapping, `setError()` calls and pending state management. I got tired of writing it, so I abstracted it.

`hookform-action` is a monorepo with multiple packages, full TypeScript inference, optimistic UI with rollback, multi-step wizard persistence, a floating DevTools panel and automated tests.

```ts
// Before: manual server-action wiring
// After:
const {
  register,
  handleSubmit,
  formState: { errors, isPending },
} = useActionForm(loginAction, {
  validationMode: "onChange",
})
```

`npm i hookform-action` · Next.js
`npm i hookform-action-standalone` · Vite / Remix / Astro

---

### [Aprovado.ai](https://aprovadoai-1ol7.vercel.app) · *SaaS — live in production*

> PDF → Anki flashcards in under 60 seconds, powered by LLMs.

Built and shipped end-to-end: Next.js + TypeScript frontend, LLM API integration, freemium model with three tiers, payment gateway with card, PIX and boleto, and CI/CD on Vercel.

Not a tutorial clone.
Not just a landing page.
A product with pricing, payment flow and real usage intent.

---

### [Graveyard](https://github.com/gabpaesschulz/graveyard) · *portfolio experiment*

> A digital memorial for abandoned projects. Because what you tried and failed at matters as much as what you shipped.

Every developer has a graveyard: the folder named `old/`, the private repo, the Notion page that lived for three months. Graveyard archives them with ritual and dignity — death certificates, epitaphs, emotional weight classification, reincarnation plans, a multi-step funeral wizard and an analytics dashboard.

Built with Next.js 15, Prisma, PostgreSQL, Framer Motion and a data model with 15 causes of death designed from real failure patterns. Dark-only, editorial typography, deliberately slow to read.

*"The projects that did not work taught me more than the ones that did."*

---

### [FreedomCalc](https://github.com/gabpaesschulz/freedomcalc) · *local-first finance tool*

> Financial planning for developers who want to build wealth, not track pennies.

FIRE calculator, compound interest simulator, pessimist/base/optimist projections and portfolio allocation charts — all running entirely in the browser.

Zero servers.
Zero tracking.
AES-256 encryption in localStorage, PIN lock screen, privacy mode and PWA-ready architecture.

---

### [Watch Planner](https://github.com/gabpaesschulz/letterbox-scrapper) · *Letterboxd scheduling tool*

> Turns any Letterboxd list into a smart, personalized movie-watching schedule.

Scrapes any public Letterboxd list, enriches every film via TMDB and distributes them across a date range while respecting daily limits.

Features include drag-and-drop calendar, `.ics` export, shareable compressed URLs, push notifications, PDF export and multi-language support.

---

### [Setlist](https://github.com/gabpaesschulz/setlist) · *concert & festival planner*

> Tracks the full lifecycle of a live music event — from ticket purchase to the night itself.

Budget guardrails, predictive alerts, early-purchase simulator, operational timeline, Sympla/Eventim import by URL, `.ics` calendar export, QR Code sharing, selective backup/restore and hardened PWA cache policy.

IndexedDB-first and offline-capable.

---

## 🔧 Stack

| Layer                      | Technologies                                                                      |
| -------------------------- | --------------------------------------------------------------------------------- |
| **Backend**                | Java 8/11/17/21, Quarkus, Spring Boot, Node.js, REST APIs, Hexagonal Architecture |
| **Frontend**               | TypeScript, React, Next.js, Angular, Tailwind CSS, Shadcn/ui                      |
| **Database**               | PostgreSQL, MySQL, MongoDB, Prisma                                                |
| **Quality & Architecture** | TDD, Clean Code, SOLID, code review, refactoring, typed APIs                      |
| **DevOps**                 | Docker, Jenkins, CI/CD, Git, pnpm workspaces, Vercel                              |
| **Open-source tooling**    | npm packages, monorepos, ESM/CJS builds, TypeScript declarations, Vitest, tsup    |

---

## 🧭 What I like building

* Developer tools with strong TypeScript inference
* Admin dashboards and internal tools
* REST integrations and backend-facing frontend architecture
* Schema-driven UI/state patterns
* Local-first tools and privacy-conscious products
* Projects with a clear idea, a real demo and a finished release

---

## 🪦 Things that did not make it

The abandoned projects live in [Graveyard](https://github.com/gabpaesschulz/graveyard). Worth a visit.

---

<div align="center">

*"Persistence beats intensity when consistency stays in the game."*

</div>
