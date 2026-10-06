<img src="assets/hero.svg" width="100%" alt="Trinayan Mahato — backend systems, AI agent pipelines, infrastructure" />

<div align="center">

<a href="https://github.com/TrinayanMahato?tab=repositories"><img src="https://img.shields.io/badge/REPOSITORIES-browse-0a0e15?style=for-the-badge&logo=github&logoColor=f0b429&labelColor=0a0e15" alt="Repositories" /></a>
<a href="https://weather-app-ten-ruby-62.vercel.app"><img src="https://img.shields.io/badge/LIVE_DEMO-planbetter-0a0e15?style=for-the-badge&logo=vercel&logoColor=58c7d8&labelColor=0a0e15" alt="Live demo" /></a>
<img src="https://komarev.com/ghpvc/?username=TrinayanMahato&style=for-the-badge&color=f0b429&labelColor=0a0e15&label=VISITS" alt="Profile views" />
<a href="https://github.com/TrinayanMahato?tab=followers"><img src="https://img.shields.io/github/followers/TrinayanMahato?style=for-the-badge&logo=github&logoColor=58c7d8&label=FOLLOWERS&labelColor=0a0e15&color=0a0e15" alt="Followers" /></a>

</div>

<img src="assets/divider.svg" width="100%" alt="" />
<img src="assets/s-about.svg" width="100%" alt="01 — What I build" />

<img src="assets/about.svg" width="100%" alt="Where the time goes, and how I work" />

I build backend systems and the pipelines that make them useful — REST APIs with real authorization, agent workflows that call models and then wait for a human, and the Docker and Kubernetes plumbing that gets them running somewhere other than my laptop.

The thread through most of it is **automation that knows when to stop**. An agent that shortlists candidates should pause before scheduling interviews. A SIEM that can block an IP should email a person before it blocks permanently. Those pauses are the interesting engineering.

- **Design it** — model the data first, then let the routes fall out of the schema.
- **Build it** — small services that compose, validation at the edge, errors that surface instead of hiding.
- **Run it** — containerised, reverse-proxied, with the deployment manifests committed next to the code.
- **Document it** — a README good enough that someone else can clone the repo and get it running.

<img src="assets/divider.svg" width="100%" alt="" />
<img src="assets/s-stack.svg" width="100%" alt="02 — How it fits together" />

<img src="assets/architecture.svg" width="100%" alt="Agent pipeline: JD in, extract, embed, post, wait, human gate, shortlist, schedule" />

The pipeline above is from **Agentic Recruiter** and it's the piece of work I'd point at first. It's a LangGraph state machine with a checkpointer, so a run survives being paused: it genuinely stops at the human gate, persists, and resumes from that exact node when an admin approves. Reject the job description and the graph loops back to re-extract rather than starting over.

<img src="assets/divider.svg" width="100%" alt="" />
<img src="assets/s-work.svg" width="100%" alt="03 — Selected work" />

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/TrinayanMahato/Agentic_recruiter"><img src="assets/card-agentic.svg" width="100%" alt="Agentic Recruiter — autonomous hiring pipeline with a human approval gate" /></a></td>
<td width="50%" valign="top"><a href="https://github.com/TrinayanMahato/SIEM"><img src="assets/card-siem.svg" width="100%" alt="AI-Driven SIEM — alerts enriched with log context and triaged by an LLM" /></a></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/TrinayanMahato/Admission-module"><img src="assets/card-admission.svg" width="100%" alt="Admission Module — role-based admission API with merit shortlisting" /></a></td>
<td width="50%" valign="top"><a href="https://github.com/TrinayanMahato/threads-exchange-hub"><img src="assets/card-swapstyle.svg" width="100%" alt="SwapStyle — community clothing-exchange platform" /></a></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/TrinayanMahato/weather_app"><img src="assets/card-weather.svg" width="100%" alt="PlanBetter — live weather dashboard with OAuth" /></a></td>
<td width="50%" valign="top"><a href="https://github.com/TrinayanMahato/Hands_on_Kubernetes"><img src="assets/card-infra.svg" width="100%" alt="Infrastructure — Kubernetes manifests and NGINX reverse proxy" /></a></td>
</tr>
</table>

<details>
<summary><samp><b>&#9656;&nbsp; EVERY REPOSITORY</b></samp></summary>

<br>

| Repository | What it is | Stack |
| :--- | :--- | :--- |
| [**Agentic_recruiter**](https://github.com/TrinayanMahato/Agentic_recruiter) | LangGraph agent that parses a JD, writes the job post, shortlists resumes by vector similarity and schedules interviews — pausing for human approval. | LangGraph · OpenAI · ChromaDB · Express |
| [**SIEM**](https://github.com/TrinayanMahato/SIEM) | Webhook receiver that enriches security alerts with surrounding Elasticsearch logs, asks Gemini for a structured verdict, and enforces it via `pfctl`. | FastAPI · Gemini · Elasticsearch · Prisma |
| [**Admission-module**](https://github.com/TrinayanMahato/Admission-module) | 24-endpoint admission API — email-verified signup, document uploads, department/course management, merit-ranked shortlisting. | Express 5 · MongoDB · JWT · Joi |
| [**threads-exchange-hub**](https://github.com/TrinayanMahato/threads-exchange-hub) | *SwapStyle* — clothing-exchange platform with user and admin dashboards, listings and swap history. | React 19 · TypeScript · Vite · shadcn/ui |
| [**weather_app**](https://github.com/TrinayanMahato/weather_app) | *PlanBetter* — weather dashboard with Google OAuth, 5-day forecast and a 1-hour client cache. **[Live →](https://weather-app-ten-ruby-62.vercel.app)** | Next.js · NextAuth · MongoDB |
| [**sitaics_project**](https://github.com/TrinayanMahato/sitaics_project) | University admin dashboard — MoUs, courses and participants, with bulk Excel import and email-approved admin registration. | Express · MongoDB · SheetJS |
| [**Hands_on_Kubernetes**](https://github.com/TrinayanMahato/Hands_on_Kubernetes) | Deployment manifests for a two-tier app — Deployments, Services, NodePort exposure and Secrets. | Kubernetes |
| [**NGINX-with-CI-CD**](https://github.com/TrinayanMahato/NGINX-with-CI-CD) | Reverse proxy and load balancer for a MERN stack — SPA fallback, WebSocket upgrade, forwarded client headers. | NGINX |

</details>

<img src="assets/divider.svg" width="100%" alt="" />
<img src="assets/s-toolkit.svg" width="100%" alt="04 — Toolkit" />

<img src="assets/toolkit.svg" width="100%" alt="Toolkit across backend, AI agents, frontend, data, infrastructure and security" />

<table>
<tr><td align="right" width="150"><samp><b>LANGUAGES</b></samp></td><td>
<img src="https://img.shields.io/badge/JavaScript-0a0e15?style=flat-square&logo=javascript&logoColor=f0b429" alt="JavaScript" />
<img src="https://img.shields.io/badge/TypeScript-0a0e15?style=flat-square&logo=typescript&logoColor=f0b429" alt="TypeScript" />
<img src="https://img.shields.io/badge/Python-0a0e15?style=flat-square&logo=python&logoColor=f0b429" alt="Python" />
<img src="https://img.shields.io/badge/HTML5-0a0e15?style=flat-square&logo=html5&logoColor=f0b429" alt="HTML5" />
<img src="https://img.shields.io/badge/CSS-0a0e15?style=flat-square&logo=css3&logoColor=f0b429" alt="CSS" />
</td></tr>
<tr><td align="right"><samp><b>BACKEND</b></samp></td><td>
<img src="https://img.shields.io/badge/Node.js-0a0e15?style=flat-square&logo=nodedotjs&logoColor=58c7d8" alt="Node.js" />
<img src="https://img.shields.io/badge/Express-0a0e15?style=flat-square&logo=express&logoColor=58c7d8" alt="Express" />
<img src="https://img.shields.io/badge/FastAPI-0a0e15?style=flat-square&logo=fastapi&logoColor=58c7d8" alt="FastAPI" />
<img src="https://img.shields.io/badge/JWT-0a0e15?style=flat-square&logo=jsonwebtokens&logoColor=58c7d8" alt="JWT" />
<img src="https://img.shields.io/badge/Joi-0a0e15?style=flat-square&logoColor=58c7d8" alt="Joi" />
</td></tr>
<tr><td align="right"><samp><b>AI &amp; AGENTS</b></samp></td><td>
<img src="https://img.shields.io/badge/LangGraph-0a0e15?style=flat-square&logo=langchain&logoColor=f0b429" alt="LangGraph" />
<img src="https://img.shields.io/badge/OpenAI-0a0e15?style=flat-square&logo=openai&logoColor=f0b429" alt="OpenAI" />
<img src="https://img.shields.io/badge/Gemini-0a0e15?style=flat-square&logo=googlegemini&logoColor=f0b429" alt="Gemini" />
<img src="https://img.shields.io/badge/ChromaDB-0a0e15?style=flat-square&logoColor=f0b429" alt="ChromaDB" />
</td></tr>
<tr><td align="right"><samp><b>FRONTEND</b></samp></td><td>
<img src="https://img.shields.io/badge/React-0a0e15?style=flat-square&logo=react&logoColor=58c7d8" alt="React" />
<img src="https://img.shields.io/badge/Next.js-0a0e15?style=flat-square&logo=nextdotjs&logoColor=58c7d8" alt="Next.js" />
<img src="https://img.shields.io/badge/Vite-0a0e15?style=flat-square&logo=vite&logoColor=58c7d8" alt="Vite" />
<img src="https://img.shields.io/badge/Tailwind_CSS-0a0e15?style=flat-square&logo=tailwindcss&logoColor=58c7d8" alt="Tailwind CSS" />
</td></tr>
<tr><td align="right"><samp><b>DATA</b></samp></td><td>
<img src="https://img.shields.io/badge/MongoDB-0a0e15?style=flat-square&logo=mongodb&logoColor=f0b429" alt="MongoDB" />
<img src="https://img.shields.io/badge/Mongoose-0a0e15?style=flat-square&logo=mongoose&logoColor=f0b429" alt="Mongoose" />
<img src="https://img.shields.io/badge/Prisma-0a0e15?style=flat-square&logo=prisma&logoColor=f0b429" alt="Prisma" />
<img src="https://img.shields.io/badge/Redis-0a0e15?style=flat-square&logo=redis&logoColor=f0b429" alt="Redis" />
<img src="https://img.shields.io/badge/Elasticsearch-0a0e15?style=flat-square&logo=elasticsearch&logoColor=f0b429" alt="Elasticsearch" />
</td></tr>
<tr><td align="right"><samp><b>INFRA</b></samp></td><td>
<img src="https://img.shields.io/badge/Docker-0a0e15?style=flat-square&logo=docker&logoColor=58c7d8" alt="Docker" />
<img src="https://img.shields.io/badge/Kubernetes-0a0e15?style=flat-square&logo=kubernetes&logoColor=58c7d8" alt="Kubernetes" />
<img src="https://img.shields.io/badge/NGINX-0a0e15?style=flat-square&logo=nginx&logoColor=58c7d8" alt="NGINX" />
<img src="https://img.shields.io/badge/Vercel-0a0e15?style=flat-square&logo=vercel&logoColor=58c7d8" alt="Vercel" />
<img src="https://img.shields.io/badge/GitHub_Actions-0a0e15?style=flat-square&logo=githubactions&logoColor=58c7d8" alt="GitHub Actions" />
</td></tr>
</table>

<img src="assets/divider.svg" width="100%" alt="" />
<img src="assets/s-signals.svg" width="100%" alt="05 — Telemetry" />

<div align="center">

<img src="assets/stats.svg" width="100%" alt="Repository telemetry and language distribution" />

</div>

<!-- Contribution snake: run Actions → "Generate Snake Animation" → Run workflow once,
     then uncomment the block below and it will render.

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/TrinayanMahato/TrinayanMahato/output/github-snake-dark.svg" />
  <img src="https://raw.githubusercontent.com/TrinayanMahato/TrinayanMahato/output/github-snake.svg" width="100%" alt="Contribution graph consumed by a snake" />
</picture>
</div>
-->

<img src="assets/divider.svg" width="100%" alt="" />
<img src="assets/s-now.svg" width="100%" alt="06 — Currently" />

```console
$ tail -f ~/now.log

[ACTIVE]  Agentic Recruiter  :: hardening the resume-ranking pass, fixing the wait window
[ACTIVE]  SIEM               :: moving from dry-run to live enforcement behind approvals
[ACTIVE]  SwapStyle          :: designing the API the finished frontend is waiting on
[LEARNING] Kubernetes        :: ingress, probes and resource limits beyond NodePort
[LEARNING] System design     :: queues, caching layers and where state actually belongs
[ONGOING] Documentation      :: every repo gets a README someone else can follow
```

<table>
<tr>
<td width="50%" valign="top">

**Open to**

- Backend and full-stack internships or junior roles
- Projects involving LLM agents, RAG or retrieval pipelines
- Anything where the infrastructure is part of the job
- Collaborating on tools that other people will actually run

</td>
<td width="50%" valign="top">

**How I work**

- Data model first — routes follow from the schema
- Validation at the edge, errors that surface loudly
- A human approves anything irreversible
- Committed deployment config, not a README full of manual steps

</td>
</tr>
</table>

<img src="assets/divider.svg" width="100%" alt="" />
<img src="assets/s-reach.svg" width="100%" alt="07 — Reach me" />

<div align="center">

<a href="https://github.com/TrinayanMahato"><img src="https://img.shields.io/badge/FOLLOW_ON_GITHUB-0a0e15?style=for-the-badge&logo=github&logoColor=f0b429&labelColor=0a0e15" alt="Follow on GitHub" /></a>
<a href="https://weather-app-ten-ruby-62.vercel.app"><img src="https://img.shields.io/badge/SEE_SOMETHING_RUNNING-0a0e15?style=for-the-badge&logo=vercel&logoColor=58c7d8&labelColor=0a0e15" alt="Live project" /></a>

<img src="assets/footer.svg" width="100%" alt="Every repository here is meant to be cloned, read and run" />

</div>
