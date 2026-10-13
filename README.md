<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=180&color=0:0D1117,50:123D5A,100:1F6FEB&text=ANIKET%20KUMAR&fontColor=FFFFFF&fontSize=36&fontAlignY=36&desc=FULL%20STACK%20DEVELOPER&descAlignY=60&descSize=15&animation=fadeIn" width="100%" alt="Aniket Kumar — Full Stack Developer" />

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=15&duration=3200&pause=950&color=58A6FF&center=true&vCenter=true&width=360&lines=Building+products+that+scale;Real-time+systems+%2B+AI;Learning+Go+in+public;Design.+Measure.+Improve." width="95%" alt="Animated developer introduction" />

[![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?style=flat-square&logo=github)](https://github.com/flutter-create-ani)
[![LeetCode](https://img.shields.io/badge/LeetCode-aniec25-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/u/aniec25/)
[![Go](https://img.shields.io/badge/Learning-Go-00ADD8?style=flat-square&logo=go&logoColor=white)](https://github.com/flutter-create-ani/go_learning)

<img src="https://komarev.com/ghpvc/?username=flutter-create-ani&label=Profile%20views&color=1f6feb&style=flat-square" alt="Profile views" />

</div>

---

## 👋 About me

**Full Stack Developer · Software Development Engineer I at ARM Worldwide**

I build end-to-end products: user interfaces, APIs, AI workflows, background jobs and real-time communication systems. I care about **correctness, observability, latency and deliberate scaling**.

- 🏢 Previously: **Broki Services** and **Specstem Digital**
- 🧠 Interested in **distributed systems, RAG, WebRTC and reliability**
- 🌱 Learning **Go**, SRE and production engineering
- 🎯 Practicing DSA on **[LeetCode · aniec25](https://leetcode.com/u/aniec25/)**

> **How I work:** Understand requirements → model failure modes → ship the simplest sound design → measure → optimize → document trade-offs.

## 🧰 Tech stack

<div align="center">

**Languages**

<img src="https://skillicons.dev/icons?i=js,ts,java,go,python,dart&perline=3" alt="JavaScript TypeScript Java Go Python Dart" width="210" />

**Frontend & mobile**

<img src="https://skillicons.dev/icons?i=react,nextjs,flutter,tailwind&perline=4" alt="React Next.js Flutter Tailwind" width="210" />

**Backend & data**

<img src="https://skillicons.dev/icons?i=nodejs,express,postgres,mysql,mongodb,redis&perline=3" alt="Node.js Express PostgreSQL MySQL MongoDB Redis" width="210" />

**Cloud & delivery**

<img src="https://skillicons.dev/icons?i=aws,gcp,docker,nginx,githubactions,linux&perline=3" alt="AWS GCP Docker Nginx GitHub Actions Linux" width="210" />

</div>

**Other tools:** `Kafka` · `BullMQ` · `RabbitMQ` · `Socket.IO` · `WebRTC` · `LiveKit` · `LangChain` · `RAG` · `Vector Search` · `MCP`

## 📈 Engineering activity

<div align="center">

<a href="https://github.com/flutter-create-ani"><img src="https://github-readme-stats.vercel.app/api?username=flutter-create-ani&show_icons=true&theme=tokyonight&hide_border=true" width="100%" alt="GitHub statistics" /></a>

<a href="https://github.com/flutter-create-ani?tab=repositories"><img src="https://github-readme-stats.vercel.app/api/top-langs/?username=flutter-create-ani&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" width="100%" alt="Most used repository languages" /></a>

[![See GitHub contributions](https://img.shields.io/badge/See_Contribution_Calendar-1F6FEB?style=for-the-badge&logo=github)](https://github.com/flutter-create-ani)

</div>

> GitHub's native contribution calendar can show eligible public **and private contribution counts** when enabled in your GitHub settings. Public stats cards cannot reliably include private contributions without authenticated access. The cards above are hosted by third parties and may occasionally fail.

<!-- If you set up a separate authenticated GitHub metrics workflow that writes github-metrics.svg to main, uncomment this line:
<img src="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/main/github-metrics.svg" width="100%" alt="Authenticated GitHub contribution calendar" />
-->

## 🐍 LeetCode submission snake

<div align="center">

[![LeetCode · aniec25](https://img.shields.io/badge/LeetCode-aniec25-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/aniec25/)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/output/leetcode-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/output/leetcode-snake.svg" />
  <img src="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/output/leetcode-snake-dark.svg" width="100%" alt="Animated LeetCode submissions for aniec25" />
</picture>

</div>

<details>
<summary><b>How the snake stays updated</b></summary>

Your [LeetCode workflow](.github/workflows/leetcode-snake.yml) should run [`scripts/generate.py`](scripts/generate.py) with `LEETCODE_USERNAME: aniec25`, then publish `leetcode-snake.svg` and `leetcode-snake-dark.svg` to the `output` branch. The animation only displays after successful generation and publication. This is a custom LeetCode activity animation, not the GitHub `Platane/snk` contribution snake.

</details>

## 🚀 Selected engineering work

### 🤖 Luminary · ARM Worldwide

Full-stack AI workflows and multi-model orchestration.

`Next.js` · `React` · `Node.js` · `LLM routing`

### 🏃 Komorebi.fit

Wearable integrations, device sync and notification processing.

`Terra API` · `Redis` · `BullMQ` · `Background jobs`

### 📞 CallHQ.ai · Broki Services

CRM automation, AI integrations and backend improvements.

`Node.js` · `RAG` · `FastAPI` · `Cloud Run`

### ⚙️ Specstem Digital

Backend APIs and asynchronous processing.

`Express` · `AWS` · `BullMQ`

> These are high-level descriptions of my work, not disclosures of proprietary production architecture.

## 🏗️ System design lab

Architecture is about **trade-offs**, not collecting infrastructure components. Expand a design below to see the approach and reasoning.

<details open>
<summary><b>01 · Scalable RAG: ingestion to answer</b></summary>

```mermaid
flowchart TB
  A[Documents / APIs] --> B[Ingestion API]
  B --> C[Queue]
  C --> D[Chunk + Embed Workers]
  D --> E[(Vector Index)]
  F[User Query] --> G[Hybrid Retrieval]
  E --> G
  G --> H[Rerank + Context Budget]
  H --> I[LLM Router]
  I --> J[Streaming Answer]
```

**Why this design?** Queues absorb ingestion spikes and support retries. Hybrid retrieval combines keyword and semantic matching. Reranking improves relevance but adds latency. Model routing can balance cost and quality but complicates fallbacks.

**Watch:** recall, grounded-answer quality, queue lag, token cost, p95 latency.

</details>

<details>
<summary><b>02 · Real-time messaging: durable delivery</b></summary>

```mermaid
flowchart TB
  A[Web / Mobile] --> B[Load Balancer]
  B --> C[WebSocket Gateways]
  C --> D[(Redis Presence)]
  C --> E[Message Service]
  E --> F[(Durable DB)]
  E --> G[Event Bus]
  G --> H[Fan-out Workers]
  H --> C
```

**Why this design?** WebSockets support low-latency communication but need reconnect handling. Presence can be ephemeral; messages need durable persistence. Use message IDs, acknowledgements, idempotency and backpressure.

**Watch:** connection count, reconnect rate, p99 delivery latency, dropped events.

</details>

<details>
<summary><b>03 · Notifications: burst handling</b></summary>

```mermaid
flowchart TB
  A[Product Events] --> B[Notification Service]
  B --> C[Redis / BullMQ]
  C --> D[Workers]
  D --> E[Push / Email / In-app]
  D --> F[(Delivery State)]
  D --> G[Retry / Dead Letter]
```

**Why this design?** Queues absorb bursts but make delivery asynchronous. Apply user preferences, idempotency keys, bounded retries and provider-specific rate limits.

**Watch:** queue age, success rate, duplicates, p95 delivery time.

</details>

<details>
<summary><b>04 · My production design checklist</b></summary>

- **Correctness:** Which writes must be atomic? Where is eventual consistency acceptable?
- **Traffic:** Peak QPS, read/write ratio, concurrency and hot keys?
- **Data:** Schema, indexes, retention and migration strategy?
- **Reliability:** Timeouts, retries, idempotency and failure isolation?
- **Observability:** Metrics, traces, logs, SLOs and alerts?
- **Cost:** Can simpler scaling solve the bottleneck first?

</details>

<sub>Diagrams are illustrative reference architectures, not verified internal deployments of any employer.</sub>

## 🧪 Learning in public

<div align="center">

[![Go learning repository](https://img.shields.io/badge/Follow_My_Go_Learning-00ADD8?style=for-the-badge&logo=go&logoColor=white)](https://github.com/flutter-create-ani/go_learning)

**Go · Production Engineering · Observability · Distributed Systems · Algorithms**

</div>

---

## 🌐 Featured personal websites

<div align="center">

### 🎮 GS Esports

<a href="https://gsesports.in/"><img src="https://image.thum.io/get/width/900/crop/520/noanimate/https://gsesports.in/" width="100%" alt="Preview of GS Esports website" /></a>

**Esports, competitive gaming and community experiences**

[![Visit GS Esports](https://img.shields.io/badge/VISIT_GS_ESPORTS-2563EB?style=for-the-badge&logo=googlechrome&logoColor=white)](https://gsesports.in/)

### 🧪 PieNot Labs

<a href="https://pienotlabs.vercel.app/"><img src="https://image.thum.io/get/width/900/crop/520/noanimate/https://pienotlabs.vercel.app/" width="100%" alt="Preview of PieNot Labs website" /></a>

**Personal web project**

[![Visit PieNot Labs](https://img.shields.io/badge/VISIT_PIENOT_LABS-7C3AED?style=for-the-badge&logo=vercel&logoColor=white)](https://pienotlabs.vercel.app/)

</div>

> GitHub strips `<iframe>` elements from README files. These are responsive clickable previews, dependent on an external screenshot service. See [`websites.html`](websites.html) for a responsive iframe gallery suitable for a separate hosted page; each site may block iframe embedding.

---

<div align="center">

**Build simply · Measure carefully · Scale deliberately**

[![Repositories](https://img.shields.io/badge/GitHub-Repositories-181717?style=flat-square&logo=github)](https://github.com/flutter-create-ani?tab=repositories)
[![LeetCode](https://img.shields.io/badge/LeetCode-aniec25-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/u/aniec25/)

<img src="https://capsule-render.vercel.app/api?type=waving&section=footer&height=80&color=0:1F6FEB,100:0D1117" width="100%" alt="Footer wave" />

</div>
