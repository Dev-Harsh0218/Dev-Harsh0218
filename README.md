<h1 align="center">Harsh Bhardwaj</h1>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&duration=3200&pause=900&color=6C7086&center=true&vCenter=true&multiline=false&width=680&lines=Backend+engineer+%7C+Go+convert+%7C+Actor-model+believer;Neovim+daily+driver.+tmux+or+die.;EXPLAIN+ANALYZE+is+my+love+language.;Curious+about+distributed+systems+and+the+AI+stack." alt="typing" />
  </a>
</p>

<p align="center">
  <a href="mailto:mailharsh0218@gmail.com"><img src="https://img.shields.io/badge/Email-mailharsh0218%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white" /></a>
  <a href="https://linkedin.com/in/bhardwajharsh1802"><img src="https://img.shields.io/badge/LinkedIn-bhardwajharsh1802-0A66C2?style=flat-square&logo=linkedin&logoColor=white" /></a>
  <a href="https://dev-harsh-bhardwaj.vercel.app"><img src="https://img.shields.io/badge/Portfolio-dev--harsh--bhardwaj.vercel.app-000000?style=flat-square&logo=vercel&logoColor=white" /></a>
  <img src="https://img.shields.io/badge/Location-Noida%20NCR-3B82F6?style=flat-square&logo=googlemaps&logoColor=white" />
  <img src="https://img.shields.io/badge/Open%20to-Opportunities-22C55E?style=flat-square" />
</p>

---

```
$ whoami
backend engineer · noida · lives in a terminal

$ cat ~/.currently_doing
Go pipelines · high-throughput APIs · occasionally reaching for Erlang
when Node stops being interesting

$ cat ~/.next_chapter
Going all-in on Go. Just started walking around the AI/LLM stack — RAG,
embeddings, agents. Poking under the hood before I ship anything here.
```

---

## Where I am right now

- **Currently at** Astro Arun Pandit. Built the **Kundali Engine** (Node + Swiss Ephemeris — 50K+ req/day at sub-250ms), a Go-based **real-time data lake** (100K+ events/day, wired straight off the existing Kafka pipeline to skip a Lambda hop I didn't want to pay for), and drove ~10x latency wins on legacy APIs (one `EXPLAIN ANALYZE` did most of the heavy lifting — turns out most "scale problems" are query problems).
- **Location:** Noida NCR. Open to remote or relocation for the right team.
- **Looking for the next thing** — SDE1 / SDE2 roles, backend-leaning or full-stack. If you're hiring or know someone building interesting stuff, my inbox is above.

---

## The setup

I live in a terminal.

- **Editor:** Neovim ([`nvim-lsp-config`](https://github.com/Dev-Harsh0218/nvim-lsp-config))
- **Multiplexer:** tmux, split panes, `hjkl` or die
- **Shell:** zsh with a ridiculous number of aliases
- **Day-to-day CLI:** `rg`, `fzf`, `lazygit`, `delta`, `htop`, `jq`
- **Reads Postgres query plans for fun.** See again: `EXPLAIN ANALYZE`.

---

## Stack

<p align="center">
  <b>Languages</b><br />
  <img src="https://skillicons.dev/icons?i=go,erlang,py,js,ts,java,kotlin,php&perline=10" />
</p>

<p align="center">
  <b>Backend & Frontend</b><br />
  <img src="https://skillicons.dev/icons?i=nodejs,express,nestjs,django,react,nextjs,tailwind&perline=10" />
</p>

<p align="center">
  <b>Data & Messaging</b><br />
  <img src="https://skillicons.dev/icons?i=postgres,mysql,mongodb,redis,kafka,rabbitmq&perline=10" />
</p>

<p align="center">
  <b>Cloud, DevOps & Terminal</b><br />
  <img src="https://skillicons.dev/icons?i=aws,jenkins,nginx,docker,linux,git,github,vim,neovim,bash&perline=10" />
</p>

### Stack, sorted by "when I actually reach for it"

| For | I use |
|---|---|
| API in a hurry | **Go**, Node.js + Express, or Django |
| Event pipeline | **Go** + Kafka (+ Kinesis Firehose when downstream demands it) |
| Actor-model concurrency | Erlang / OTP |
| Autoscaling on a custom signal (like queue depth) | Boto3 + EC2 Spot Instances |
| Multi-tenant billing / SaaS glue | Node + Postgres + Redis |
| UI on top of an API | React + Tailwind (Next.js when SEO earns it) |
| Android SDK | Kotlin, sometimes Java |
| Realtime fan-out | Redis Streams, SSE, or WebSockets |
| AI / LLM stack (just started) | Python + embeddings + RAG — still assembling the mental model |
| Deploy | AWS behind Nginx, Jenkins pipelines, Docker where it earns its keep |

---

## Things I've built (the interesting ones)

### The one I'm proudest of — [Messaging Server](https://github.com/Dev-Harsh0218/Messaging_Server)
> Erlang / OTP · PostgreSQL · Kafka · RabbitMQ · S3

Slack got expensive. I'd been eyeing the actor model for months. A couple of months later we had our own WebSocket server — each connection running as its own supervised OTP process, so a peer's crash never took anyone else down. First time I really *got* why Erlang exists.

Runs at **200+ users, 50+ groups, 1M+ messages moved in ~2 months**. Zero pages so far.

**What I'd do differently:** message persistence went straight to Postgres. Should've evaluated a log-structured store on day one instead of "we'll fix it later."

### The one I've built the most surface area on — [Aduo](https://github.com/Dev-Harsh0218/aduo)
> Kotlin · Node.js · React

Two-sided AdMob-like thing. Publishers drop in a Kotlin SDK (`showBanner()`, `showInterstitial()`, `showPopup()`), advertisers manage from a React console. Async impression/click billing across multi-tenant orgs.

Split across [SDK](https://github.com/Dev-Harsh0218/aduo-sdk-kotlin) · [Backend](https://github.com/Dev-Harsh0218/aduo-backend) · [Web (Turborepo monorepo)](https://github.com/Dev-Harsh0218/aduo-web) · [Test app](https://github.com/Dev-Harsh0218/aduo-test-app). **[Live marketing](https://marketing-mu-amber.vercel.app)** · **[publisher panel](https://publisher-rust.vercel.app)** (both live).

### The one that taught me the most about attribution — [AppAnalytics](https://github.com/Dev-Harsh0218/AppAnalyticsPanel)
> Java Android SDK · Node · Kafka · React

Play Store Install Referrer attribution — organic / paid / referral. Kafka fans out to downstream, React dashboard slices by OS / device / geo / app version. Adopted by **21+ apps**. Turns out mobile attribution is 60% engineering and 40% carefully avoiding double-counting.

---

## Opinions I'm ready to defend

- **Boring infrastructure, interesting problems.** Postgres for the database, Erlang for the concurrency puzzle. Don't put your novelty budget on both.
- **`EXPLAIN ANALYZE` before you upsize the EC2.** The 10x latency win at work came from an index and a query rewrite, not a rewrite of the service.
- **Reuse over rebuild.** Almost every "we need a new pipeline" turns out to be "we can extend the existing service and skip a Lambda."
- **The event loop lies about concurrency.** JS pretends to be async. Go and Erlang don't have to pretend.
- **Vim motions are worth the two-week bill.** After that everything else feels slow.
- **Read the RFC before the blog post.** Nine times out of ten the RFC is shorter *and* clearer.

---

## GitHub

<p align="center">
  <img height="180" src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Dev-Harsh0218&theme=default" />
  <img height="180" src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=Dev-Harsh0218&theme=default" />
</p>

<p align="center">
  <img height="180" src="https://github-readme-streak-stats.herokuapp.com/?user=Dev-Harsh0218&hide_border=true" />
  <img height="180" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Dev-Harsh0218&theme=default" />
</p>

<p align="center">
  <img src="https://ghchart.rshah.org/6C7086/Dev-Harsh0218" alt="Contribution graph" />
</p>

---

## Also lying around this profile

- [`CodeForcesSolutionRepo_go`](https://github.com/Dev-Harsh0218/CodeForcesSolutionRepo_go) — CP in Go. Grinding it keeps the fundamentals sharp.
- [`dsa_ques_ans`](https://github.com/Dev-Harsh0218/dsa_ques_ans) — DSA practice repo, same reason.
- [`nvim-lsp-config`](https://github.com/Dev-Harsh0218/nvim-lsp-config) — my Neovim config, in case anyone else is optimizing key-map latency.
- [`thePortfolioProject`](https://github.com/Dev-Harsh0218/thePortfolioProject) — source for the [portfolio site](https://dev-harsh-bhardwaj.vercel.app), Next.js.

Older experiments (food-ordering, image utils, ML notebooks) are the archaeological layer — safe to ignore.

**Not on GitHub** (internal to former employers, happy to walk through architecture in a call): **LinkTester** (custom Boto3 autoscaler on RabbitMQ queue depth, handled 500K–600K links at peak), **Task-Trackier** (JIRA clone with a weighted developer scoring system, SSE + Kafka + Redis), **Kundali Engine**, and **Analytics Data Lake**.

---

## Say hi

```
$ echo $EMAIL       → mailharsh0218@gmail.com
$ open $LINKEDIN    → linkedin.com/in/bhardwajharsh1802
$ dial $PHONE       → +91 9315866109
$ open $PORTFOLIO   → dev-harsh-bhardwaj.vercel.app
```

Coffee, code, or a quick "hey we might be hiring" — always up for it.

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=Dev-Harsh0218&label=Profile+views&color=6C7086&style=flat-square" alt="Profile views" />
</p>
