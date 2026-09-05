# Hey, I'm Harsh

Backend engineer from Noida. I like building things that don't fall over, and I reach for Erlang when Node feels too well-behaved.

Currently a Software Engineer at Astro Arun Pandit, where I spend most of my time on high-throughput APIs, Go event pipelines, and figuring out why yesterday's fast query is today's slow one.

---

## What I'm up to

- **On notice** — actively looking for SDE1 / SDE2 roles (Full-Stack or Backend). Available immediately after 30-day notice period. Ping me if you're hiring.
- **Recently shipped:** Kundali Engine (Node + Swiss Ephemeris, 50K+ req/day at sub-250ms) and a Go-based real-time data lake that piggybacks on our existing Kafka pipeline instead of adding a separate Lambda service.
- **Where I'm heading next:** doubling down on **Go** — it's the direction I want the next chapter of my career to point. The data-lake work at Astro has convinced me the boring-fast concurrency story Go tells is exactly what I want to build on.
- **Just started on:** **AI / LLM applications** — agents, embeddings, RAG, prompt-engineered tool use. Early days; poking at the stack from the ground up before I start shipping things here.

---

## Some things I've built

### The one I'm proudest of — [Messaging Server](https://github.com/Dev-Harsh0218/Messaging_Server) 
> Erlang / OTP · PostgreSQL · Kafka · RabbitMQ · S3

Started when Slack got expensive for the team. I'd been curious about the actor model for a while, so I built our replacement in Erlang — each WebSocket connection is a supervised OTP process, which meant connection crashes never took down anyone else's session. First time I really *got* why the actor model exists. Runs at 200+ users across 50+ groups, has moved 1M+ messages, hasn't woken me up yet.

**What I'd redo:** the message-storage layer. I went straight to Postgres — should have considered a log-structured store from the start.

### The most fun to demo — [Ads SDK Platform](https://ads-sdk-demo.vercel.app)
> Kotlin · Node.js · React

Two-sided AdMob-inspired platform. Publishers integrate a Kotlin Android SDK (`showBanner()`, `showInterstitial()`, `showPopup()`); advertisers manage campaigns from a React admin console. Async billing pipeline for impressions/clicks across a multi-tenant org structure. **[Live demo](https://ads-sdk-demo.vercel.app)** — kick the tires.

**Repos:** [Kotlin SDK](https://github.com/Dev-Harsh0218/adsSdkKotlin) · [Backend](https://github.com/Dev-Harsh0218/ads_sdk_backend) · [Console](https://github.com/Dev-Harsh0218/ads_sdk_frontend) · [Test app](https://github.com/Dev-Harsh0218/adsSdkTestingApp)

### The one that taught me the most about attribution — [AppAnalytics](https://github.com/Dev-Harsh0218/AppAnalyticsPanel)
> Java · Node.js · Kafka · React

Java Android SDK that hooks into the Play Store Install Referrer API and attributes installs (organic / paid / referral). Events fan out to Kafka for downstream processing; a React dashboard slices by OS, device, app version, geography. Adopted by 21+ apps. Turns out mobile attribution is 60% engineering and 40% carefully avoiding double-counting.

---

## How I think about engineering

Three things I try not to compromise on:

1. **Reuse over rebuild.** Almost every "new pipeline needed" turns out to be "extend an existing service." Cheaper, less on-call surface.
2. **Boring choices for infrastructure, interesting choices for problems.** Postgres for the database, Erlang for the concurrency puzzle.
3. **Measure before optimizing.** The 10x latency win on the Kundali APIs came from a single `EXPLAIN ANALYZE` — not a rewrite.

---

## Tech I reach for

| When I need... | I usually reach for |
|---|---|
| A production API fast | **Go**, Node.js + Express, or Django |
| Actor-model concurrency | Erlang / OTP |
| An event pipeline | **Go** + Kafka |
| Exploring AI / LLM tooling | Python, embeddings, RAG — still assembling my toolkit here |
| Autoscaling on custom signals | Boto3 + EC2 Spot Instances |
| A UI to go with a backend | React + Tailwind (or Next.js) |
| An Android SDK | Kotlin, sometimes Java |
| Caching or realtime fan-out | Redis, SSE, WebSockets |
| Deploying anything | AWS (EC2/RDS/S3) behind Nginx, wired through Jenkins |

---

## GitHub stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Dev-Harsh0218&show_icons=true&count_private=true&hide_border=true" alt="Harsh's GitHub stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Dev-Harsh0218&layout=compact&hide_border=true" alt="Top languages" />
</p>

---

## Also poking around here

- [CodeForcesSolutionRepo_go](https://github.com/Dev-Harsh0218/CodeForcesSolutionRepo_go) — CodeForces problems in Go, mostly for keeping my brain from atrophying
- [dsa_ques_ans](https://github.com/Dev-Harsh0218/dsa_ques_ans) — DSA practice, same reason
- [thePortfolioProject](https://github.com/Dev-Harsh0218/thePortfolioProject) — source for my [portfolio site](https://dev-harsh-bhardwaj.vercel.app)
- A few older/dormant experiments — food ordering site, image stuff, ML notebook — the archaeological layer

Some of the things I've built at work (LinkTester with a Boto3 autoscaler, Task-Trackier JIRA-clone, Kundali Engine, Analytics Data Lake) aren't open-sourced — internal to former employers. Happy to walk through architecture in a call.

---

## Say hi

- **Email:** mailharsh0218@gmail.com
- **LinkedIn:** [linkedin.com/in/bhardwajharsh1802](https://linkedin.com/in/bhardwajharsh1802)
- **Portfolio:** [dev-harsh-bhardwaj.vercel.app](https://dev-harsh-bhardwaj.vercel.app)
- **Phone / WhatsApp:** +91 9315866109

Coffee, code, or a quick "hey we might be hiring" — always up for a conversation.
