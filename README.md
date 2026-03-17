<div align="center">

# Gabriel Paes Schulz

**Fullstack Developer · Product Builder · Things that ship**

*Java · TypeScript · Next.js · Quarkus · Spring Boot*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-gabriel--paes--schulz-0a66c2?style=flat-square&logo=linkedin)](https://linkedin.com/in/gabrielpaesschulz)
[![Email](https://img.shields.io/badge/Email-gabriel__paes@live.com-ea4335?style=flat-square&logo=gmail)](mailto:gabriel_paes@live.com)
[![Aprovado.ai](https://img.shields.io/badge/SaaS-Aprovado.ai-6366f1?style=flat-square)](https://aprovadoai-1ol7.vercel.app)

</div>

---

I write backend systems that don't fall apart and frontend interfaces that don't feel like an afterthought.

4+ years building and modernizing corporate systems — legacy migrations, query optimization, financial pipelines, RESTful integrations. In parallel, I ship products of my own: a SaaS in production, open-source tooling used by other developers, and a few experiments that refuse to be ordinary.

I care about code that communicates intent. About architecture that survives its own growth. About products that feel like someone actually thought about the person using them.

---

## ⚡ Things I've shipped

---

### [hookform-action](https://github.com/gabpaesschulz/hookform-action) · *OSS library*

> The missing layer between React Hook Form and your server.

The same 60+ lines of boilerplate — `useTransition`, FormData serialization, Zod error mapping, `setError()` calls — appear in every project that connects RHF to a server action. I got tired of writing it. So I abstracted it.

`hookform-action` is a monorepo with four packages, full TypeScript inference, optimistic UI with rollback, multi-step wizard persistence, a floating DevTools panel, and 81+ tests.

```ts
// Before: ~60 lines of manual wiring
// After:
const { register, handleSubmit, formState: { errors, isPending } } =
  useActionForm(loginAction, { validationMode: "onChange" });
```

`npm i hookform-action` · Next.js · `npm i hookform-action-standalone` · Vite / Remix / Astro

---

### [Aprovado.ai](https://aprovadoai-1ol7.vercel.app) · *SaaS — live in production*

> PDF → Anki flashcards in under 60 seconds, powered by LLMs.

Built and shipped end-to-end: Next.js + TypeScript frontend, LLM API integration, freemium model with three tiers (Free / Pro R$29/mo / Lifetime R$297), payment gateway with card, PIX and boleto, CI/CD on Vercel, real users since 2024.

Not a demo. Not a tutorial clone. A product.

---

### [Graveyard](https://github.com/gabpaesschulz/graveyard) · *portfolio experiment*

> A digital memorial for abandoned projects. Because what you tried and failed at matters as much as what you shipped.

Every developer has a graveyard: the folder named `old/`, the private repo, the Notion page that lived for three months. Graveyard archives them with ritual and dignity — death certificates, epitaphs, emotional weight classification, reincarnation plans, a multi-step funeral wizard, and an analytics dashboard.

Built with Next.js 15, Prisma, PostgreSQL, Framer Motion, and a data model with 15 causes of death designed from real failure patterns. Dark-only, editorial typography (Playfair Display), deliberately slow to read.

*"The projects that didn't work taught me more than the ones that did."*

---

### [FreedomCalc](https://github.com/gabpaesschulz/freedomcalc) · *local-first finance tool*

> Financial planning for developers who want to build wealth, not track pennies.

FIRE calculator, compound interest simulator, pessimist/base/optimist projections, portfolio allocation charts — all running entirely in the browser. Zero servers, zero tracking, AES-256 encryption in localStorage, PIN lock screen, privacy mode (`P` to blur all values on screen), PWA-ready.

---

### [Watch Planner](https://github.com/gabpaesschulz/letterbox-scrapper) · *Letterboxd scheduling tool*

> Turns any Letterboxd list into a smart, personalized movie-watching schedule.

Scrapes any public Letterboxd list, enriches every film via TMDB (runtime, cast, streaming providers), and distributes them across a date range respecting your daily limits. Drag-and-drop calendar, `.ics` export, shareable compressed URLs, push notifications, PDF export. Multi-language (PT/EN/ES).

---

### [Setlist](https://github.com/gabpaesschulz/setlist) · *concert & festival planner*

> Tracks the full lifecycle of a live music event — from ticket purchase to the night itself.

Budget guardrails with predictive alerts, early-purchase simulator with three scenarios, operational timeline with change history, Sympla/Eventim import by URL, `.ics` calendar export, QR Code sharing, selective backup/restore by event, hardened PWA cache policy. IndexedDB-first, offline-capable.

---

## 🔧 Stack

| Layer | Technologies |
|---|---|
| **Backend** | Java 8/11/17/21, Quarkus, Spring Boot, Node.js, REST APIs, Hexagonal Architecture |
| **Frontend** | TypeScript, Next.js, React, Angular, Tailwind CSS, Shadcn/ui |
| **Database** | PostgreSQL (CTEs, views, query optimization), MySQL, MongoDB, Prisma |
| **Engineering** | TDD, Clean Code, SOLID, code review, refactoring |
| **DevOps** | Docker, Jenkins, CI/CD, Git, Scrum/Kanban |

---

## 🪦 Things that didn't make it

The abandoned projects live in [Graveyard](https://github.com/gabpaesschulz/graveyard). Worth a visit.

---

<div align="center">

*"Persistence beats intensity when consistency stays in the game."*

</div>
