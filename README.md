<div align="center">

<img src="./hero.svg" width="100%" alt="Savorealo"/>

<br/>

<a href="https://savorealo.com">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=1000&color=FF6B00&center=true&vCenter=true&repeat=true&width=680&height=50&lines=AI-powered+gastronomic+social+network+%F0%9F%8D%B4;Generate+recipes+with+Claude+AI+%F0%9F%A4%96;Share%2C+discover%2C+savour+%F0%9F%8D%B7;Angular+21+%C2%B7+Flutter+%C2%B7+Cloudflare+Workers+%E2%9A%A1;PostgreSQL+17+%C2%B7+29+tables+%C2%B7+RLS+%C2%B7+FTS+%F0%9F%97%84%EF%B8%8F;Final+Degree++%E2%86%92+Startup+%F0%9F%9A%80" alt="Typing SVG"/>
</a>

<br/><br/>

<a href="https://savorealo.com">
  <img src="https://img.shields.io/badge/%F0%9F%8C%90-savorealo.com-FF6B00?style=for-the-badge&labelColor=0a0300"/>
</a>
&nbsp;
<img src="https://img.shields.io/badge/STATUS-In_development-27ae60?style=for-the-badge&labelColor=0a0300"/>
&nbsp;
<img src="https://img.shields.io/badge/SPRINT-1_completed-FF6B00?style=for-the-badge&labelColor=0a0300"/>
&nbsp;
<img src="https://img.shields.io/badge/PLATFORM-Web_%7C_iOS_%7C_Android-FF8C00?style=for-the-badge&labelColor=0a0300"/>

<br/><br/>

<!-- Language switcher -->
<a href="./README.md">
  <img src="https://img.shields.io/badge/%F0%9F%87%AA%F0%9F%87%B8-Español-FF6B00?style=flat-square&labelColor=0a0300"/>
</a>
&nbsp;
<img src="https://img.shields.io/badge/%F0%9F%87%AC%F0%9F%87%A7-English_(current)-555?style=flat-square&labelColor=0a0300"/>

<br/><br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

</div>

<br/>

## What is Savorealo?

**Savorealo** is the first 100% gastronomic social network with integrated AI. Users publish recipes, food posts and restaurant reviews — and if they don't know what to cook, they tell the AI what ingredients they have and within seconds they receive a personalised recipe ready to publish.

> *Not just a recipe app. It's Instagram for foodies, with an AI chef in your pocket.*

<br/>

<div align="center"><img src="./divider.svg" width="100%" alt="—"/></div>

<br/>

## Features

<table>
<tr>
<td width="50%">

**Social network**
- 📸 &nbsp;Personalised feed with multimedia posts
- 👥 &nbsp;Follow users and restaurants
- 💬 &nbsp;Comments, likes and saves
- 📖 &nbsp;Stories with 24h expiration
- 💌 &nbsp;Direct messages and group chats
- 🔔 &nbsp;Real-time notifications

</td>
<td width="50%">

**Gastronomy + AI**
- 🤖 &nbsp;Recipe generator with Claude AI
- 📷 &nbsp;Upload a photo — AI identifies ingredients
- 🌾 &nbsp;Allergen and preference system
- 🗺️ &nbsp;Restaurant directory with reviews
- 🔍 &nbsp;Full-text search in Spanish
- 📊 &nbsp;Culinary categories and filters

</td>
</tr>
</table>

<br/>

<div align="center"><img src="./divider.svg" width="100%" alt="—"/></div>

<br/>

## Tech stack

<div align="center">

**Frontend & Mobile**

<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=angular,flutter,dart,kotlin,tailwind,figma&theme=dark&perline=6"/>
</a>

<br/><br/>

**Backend & Infrastructure**

<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=ts,nodejs,graphql,prisma,postgres,cloudflare&theme=dark&perline=6"/>
</a>

<br/><br/>

**AI, Automation & DevOps**

<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=github,githubactions,supabase,vitest&theme=dark&perline=4"/>
</a>

</div>

<br/>

<details>
<summary><b>📋 Full stack table</b></summary>
<br/>

| Layer | Technology | Version | Notes |
|---|---|---|---|
| **Web framework** | Angular | 21.x | Signals + Zoneless |
| **UI Components** | PrimeNG + Tailwind CSS | 21.x / v4 | Custom design system |
| **Mobile** | Flutter + Dart | 3.x | iOS and Android |
| **Native modules** | Kotlin | — | Android |
| **API** | GraphQL Yoga v5 | latest | The Guild, spec-compliant |
| **GraphQL schema** | Pothos | latest | Code-first, type-safe |
| **ORM** | Prisma + Edge | latest | With Prisma Accelerate |
| **Backend runtime** | Cloudflare Workers | — | Edge serverless, 300 cities |
| **Database** | PostgreSQL 17 | via Supabase | 29 tables, RLS, FTS Spanish |
| **Auth** | Supabase Auth | latest | JWT + OAuth |
| **Media storage** | Cloudflare R2 | — | No egress fees |
| **Cache / Sessions** | Cloudflare KV | — | Edge-distributed |
| **Realtime** | Cloudflare Durable Objects | — | Persistent WebSockets |
| **Connection pool** | Cloudflare Hyperdrive | — | Workers → Supabase |
| **Generative AI** | Claude API (Anthropic) | Sonnet 4 | Recipe generation |
| **AI orchestration** | n8n | — | AI → DB workflow |
| **Language** | TypeScript 5 strict | 5.x | End-to-end type safety |
| **Testing** | Vitest + Playwright | latest | Unit + E2E |
| **CI/CD** | GitHub Actions | — | Automatic deploy |

</details>

<br/>

<div align="center"><img src="./divider.svg" width="100%" alt="—"/></div>

<br/>

## Architecture

```mermaid
graph TD
  subgraph C["👤 Clients"]
    WEB["🌐 Angular 21 · Cloudflare Pages"]
    MOB["📱 Flutter · iOS & Android"]
  end

  subgraph CF["☁️ Cloudflare Edge — 300 cities"]
    WORKER["⚡ Worker — GraphQL API\nYoga v5 · Pothos · Prisma"]
    KV["🗄️ KV Store\nSessions · Cache · Rate limit"]
    R2["📦 R2 Storage\nPhotos · Videos · Media"]
    DO["🔔 Durable Objects\nRealtime · WebSockets"]
    HYP["🔌 Hyperdrive\nConnection Pool"]
  end

  subgraph SB["🟢 Supabase · eu-central-1"]
    PG["🐘 PostgreSQL 17\n29 tables · RLS · FTS"]
    AUTH["🔐 Supabase Auth · JWT"]
  end

  subgraph AI["🤖 AI & Automation"]
    N8N["⚙️ n8n · Orchestration"]
    CLAUDE["🧠 Claude API · Anthropic"]
  end

  WEB -->|GraphQL HTTPS| WORKER
  MOB -->|GraphQL HTTPS| WORKER
  WORKER <--> KV
  WORKER --> R2
  WORKER <--> DO
  WORKER --> HYP --> PG
  WORKER --> AUTH
  WORKER --> N8N --> CLAUDE

  style CF fill:#1a0800,stroke:#FF6B00,color:#fff
  style SB fill:#0a1a0a,stroke:#27ae60,color:#fff
  style AI fill:#0a0a1a,stroke:#7c3aed,color:#fff
  style C fill:#1a1a1a,stroke:#666,color:#fff
```

> **Edge-first.** No servers to manage. No manual scaling. Automatic HTTPS. Deploy in seconds. Estimated MVP cost: **~€5–10/month**.

<br/>

<div align="center"><img src="./divider.svg" width="100%" alt="—"/></div>

<br/>

## Database

<div align="center">

![PostgreSQL](https://img.shields.io/badge/PostgreSQL_17-29_tables-FF6B00?style=flat-square&logo=postgresql&logoColor=white&labelColor=0a0300)
&nbsp;
![RLS](https://img.shields.io/badge/RLS-100%25_enabled-27ae60?style=flat-square&labelColor=0a0300)
&nbsp;
![FTS](https://img.shields.io/badge/Full--text-Spanish-FF8C00?style=flat-square&labelColor=0a0300)
&nbsp;
![Migrations](https://img.shields.io/badge/Migrations-30_applied-3498db?style=flat-square&labelColor=0a0300)

</div>

<br/>

<table>
<tr>
<td width="33%" valign="top">

**👤 Users & Social**
```
users
person_profiles
business_profiles
user_settings
follows
```
**🌾 Allergens & Prefs**
```
allergens
allergen_ingredients
user_allergies
preferences
user_preferences
```

</td>
<td width="33%" valign="top">

**📝 Content**
```
posts          ← polymorphic
recipes        ← post extension
ingredients
recipe_ingredients
post_media
```
**❤️ Interactions**
```
likes
comments
saved_posts
viewed_posts
```

</td>
<td width="33%" valign="top">

**💬 Messaging**
```
conversations
conversation_participants
direct_messages
contacts
```
**🔔 Events & AI**
```
notifications
feed_events
places
place_reviews
ai_generations
```

</td>
</tr>
</table>

<br/>

<div align="center"><img src="./divider.svg" width="100%" alt="—"/></div>

<br/>

## AI generation — the differentiator

<div align="center">
<img src="./flow-ai.svg" width="100%" alt="AI generation flow"/>
</div>

<br/>

| Flow | Input | Process |
|---|---|---|
| **Manual** | Ingredients + dietary restrictions | Claude generates → user reviews → publishes |
| **Photo** | Image of ingredients | Claude Vision identifies → same flow |
| **n8n** | Orchestration middleware | Retries, per-user rate limiting, metrics |

<br/>

<div align="center"><img src="./divider.svg" width="100%" alt="—"/></div>

<br/>

## Request flow

<div align="center">
<img src="./flow-request.svg" width="100%" alt="Request flow"/>
</div>

<br/>

<div align="center"><img src="./divider.svg" width="100%" alt="—"/></div>

<br/>

## Project activity

<div align="center">
<img
  src="https://github-readme-activity-graph.vercel.app/graph?username=savorealo&bg_color=0a0300&color=FF9A00&line=FF6B00&point=FFD080&area=true&area_color=FF6B00&hide_border=false&border_color=FF6B00&title_color=FF9A00&custom_title=Savorealo%20team%20activity"
  width="100%"
  alt="Activity graph"
/>
</div>

<br/>

<div align="center"><img src="./divider.svg" width="100%" alt="—"/></div>

<br/>

## CI/CD Pipeline

<div align="center">
<img src="./flow-cicd.svg" width="100%" alt="CI/CD pipeline"/>
</div>

<br/>

Push to any tracked branch triggers a GitHub Actions workflow that runs checks and deploys automatically — no manual steps needed.

<br/>

**Backend — Cloudflare Worker (GraphQL API)**

<div align="center">

| Branch | Project | Worker route | Trigger |
|---|---|---|---|
| `main` | `savorealo-api` | `app.savorealo.com/api/*` | Push → GitHub Actions → deploy |
| `develop` | `savorealo-api-staging` | `develop.app.savorealo.com/api/*` | Push → GitHub Actions → deploy |

</div>

<br/>

**Frontend — Cloudflare Pages (Angular 21)**

<div align="center">

| Branch | Domain | Notes | Trigger |
|---|---|---|---|
| `main` | `app.savorealo.com` | Includes internal Worker for SSR (auth page) | Push → GitHub Actions → deploy |
| `develop` | `develop.app.savorealo.com` | Includes internal Worker for SSR (auth page) | Push → GitHub Actions → deploy |

</div>

<br/>

<div align="center">

| Branch | Role |
|---|---|
| `feat/*` · `fix/*` | Local development only — no automatic deploy |

</div>

[Conventional Commits](https://www.conventionalcommits.org/) &nbsp;·&nbsp; Commitlint + Husky &nbsp;·&nbsp; PRs max 400 lines

<br/>

<div align="center"><img src="./divider.svg" width="100%" alt="—"/></div>

<br/>

## Repositories

<div align="center">

| Repository | Description | Main stack |
|---|---|---|
| [`savorealo-web`](#) | Angular 21 frontend | Angular · Tailwind · PrimeNG · Apollo |
| [`savorealo-mobile`](#) | Flutter iOS/Android app | Flutter · Dart · Kotlin |
| [`savorealo-api`](#) | GraphQL edge backend | Workers · Yoga v5 · Pothos · Prisma |
| [`savorealo-infra`](#) | Cloudflare configuration | Wrangler · IaC |

> 🔒 Private repositories — request access from the team.

</div>

<br/>

<div align="center"><img src="./divider.svg" width="100%" alt="—"/></div>

<br/>

## Local development

<details>
<summary><b>⚡ Backend — GraphQL API (Cloudflare Workers)</b></summary>
<br/>

```bash
cd savorealo-api
npm install
cp .env.example .env        # fill in Supabase + Cloudflare credentials
wrangler dev                # → http://localhost:8787/graphql
```
</details>

<details>
<summary><b>🌐 Web frontend — Angular 21</b></summary>
<br/>

```bash
cd savorealo-web
npm install
cp environments/environment.example.ts environments/environment.ts
ng serve                    # → http://localhost:4200
```
</details>

<details>
<summary><b>📱 Mobile — Flutter</b></summary>
<br/>

```bash
cd savorealo-mobile
flutter pub get
flutter run
```
</details>

<br/>

<div align="center"><img src="./divider.svg" width="100%" alt="—"/></div>

<br/>

## Team

<div align="center">

<table>
<tr>
  <td align="center" width="50%">
    <br/>
    <img src="https://img.shields.io/badge/Full--Stack_Web_%2B_Backend-FF6B00?style=for-the-badge&labelColor=0a0300"/>
    <br/><br/>
    <sub>Angular 21 · GraphQL API · Cloudflare Workers · TypeScript</sub>
    <br/><br/>
  </td>
  <td align="center" width="50%">
    <br/>
    <img src="https://img.shields.io/badge/Mobile_Developer-FF6B00?style=for-the-badge&labelColor=0a0300"/>
    <br/><br/>
    <sub>Flutter · Dart · iOS · Android · Kotlin</sub>
    <br/><br/>
  </td>
</tr>
</table>

<br/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=13&duration=4000&pause=2000&color=FF6B00&center=true&vCenter=true&repeat=true&width=500&height=28&lines=Final+Degree++%E2%86%92+Startup+%F0%9F%9A%80;Sprint+1+completed+%C2%B7+April+2026+%E2%9C%85;Cooking+the+future+of+gastronomy+%F0%9F%8D%B3" alt="footer typing"/>

<br/><br/>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

<br/>

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0a0300,50:c45000,100:FF6B00&height=140&section=footer&animation=fadeIn" width="100%"/>

</div>
