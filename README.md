<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=230&color=0:0D1117,50:123D5A,100:1F6FEB&text=ANIKET%20KUMAR&fontColor=FFFFFF&fontSize=52&fontAlignY=38&desc=FULL%20STACK%20DEVELOPER%20%7C%20DISTRIBUTED%20SYSTEMS%20%7C%20AI&descAlignY=61&animation=fadeIn" alt="Aniket Kumar" />

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=3200&pause=900&color=58A6FF&center=true&vCenter=true&width=850&lines=Building+products+from+UI+to+infrastructure;Designing+reliable+real-time+systems;Exploring+AI%2C+Go%2C+and+production+engineering;Measure+first.+Optimize+what+matters." alt="Animated engineering introduction" />

[![Portfolio](https://img.shields.io/badge/GitHub-Portfolio-181717?style=for-the-badge&logo=github)](https://github.com/flutter-create-ani)
[![LeetCode](https://img.shields.io/badge/LeetCode-anie25-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/anie25/)
[![Go](https://img.shields.io/badge/Currently_Learning-Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)](https://github.com/flutter-create-ani/go_learning)

<img src="https://komarev.com/ghpvc/?username=flutter-create-ani&label=Profile%20Views&color=1f6feb&style=flat" alt="Profile views" />

</div>

---

## ⚡ Engineering at a glance

<table>
<tr>
<td width="50%" valign="top">

### 👨‍💻 Who I am

Full Stack Developer and Software Development Engineer building **web applications, backend services, real-time communication, and AI-powered workflows**.

- 🏢 **SDE I · ARM Worldwide**
- 🧩 Previously **Broki Services** and **Specstem Digital**
- 🔭 Interested in system design, distributed systems, RAG and reliability
- 🌱 Learning **Go** and production engineering
- 🧠 Solving algorithms on [LeetCode](https://leetcode.com/u/anie25/)

</td>
<td width="50%" valign="top">

### 🎯 How I engineer

```text
Understand the product
        ↓
Model data and failure cases
        ↓
Ship the simplest sound design
        ↓
Measure p95 / p99 and errors
        ↓
Scale the proven bottleneck
```

**Principle:** Correctness first. Observability always. Complexity only when justified.

</td>
</tr>
</table>

## 🧰 Technology radar

<div align="center">

**Languages & frontend**

<img src="https://skillicons.dev/icons?i=js,ts,java,go,python,dart,react,nextjs,flutter,tailwind&perline=10" alt="Languages and frontend" />

**Backend, data & infrastructure**

<img src="https://skillicons.dev/icons?i=nodejs,express,postgres,mysql,mongodb,redis,firebase,aws,gcp,docker,nginx,githubactions&perline=12" alt="Backend and infrastructure" />

`Kafka` · `BullMQ` · `RabbitMQ` · `Socket.IO` · `WebRTC` · `LiveKit` · `LangChain` · `RAG` · `MCP` · `Vector Search` · `REST APIs`

</div>

## 📈 Live engineering activity

<div align="center">

<img width="49%" src="https://github-readme-stats.vercel.app/api?username=flutter-create-ani&show_icons=true&theme=github_dark&hide_border=true&rank_icon=github" alt="GitHub statistics" />
<img width="49%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=flutter-create-ani&layout=compact&theme=github_dark&hide_border=true&langs_count=8" alt="Most used GitHub languages" />

<img width="98%" src="https://github-readme-activity-graph.vercel.app/graph?username=flutter-create-ani&theme=github-compact&hide_border=true&area=true" alt="GitHub activity graph" />

</div>

<sub>GitHub cards are provided by external services and may occasionally fail or display cached data. Language statistics reflect public repository contents, not engineering proficiency.</sub>

## 🐍 LeetCode activity — an animated submission calendar

<div align="center">

<a href="https://leetcode.com/u/anie25/"><img src="https://img.shields.io/badge/Practice_Profile-anie25-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" alt="LeetCode profile" /></a>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/output/leetcode-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/output/leetcode-snake.svg" />
  <img width="100%" src="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/output/leetcode-snake-dark.svg" alt="LeetCode submission animation for anie25 — available after workflow publishes" />
</picture>

</div>

<details>
<summary><b>ℹ️ How this animation stays updated</b></summary>

The [`leetcode-snake.yml`](.github/workflows/leetcode-snake.yml) workflow runs the [generator](scripts/generate.py) and publishes its SVG output to the `output` branch. The image only renders after a successful workflow run. This animation represents **LeetCode submissions**, not GitHub commits; it is a custom visualization rather than the original `Platane/snk` algorithm.

The source of truth for solved problems is the [LeetCode profile](https://leetcode.com/u/anie25/). The generator depends on access to LeetCode activity data.

</details>

## 🚀 Selected engineering work

| Product / team | Focus | Technology / patterns |
| :--- | :--- | :--- |
| **ARM Worldwide · Luminary** | Full-stack AI workflows and multi-model orchestration | Next.js, React, Node.js, LLM routing |
| **Komorebi.fit** | Wearable integration, sync, notifications | Terra API, Redis, BullMQ, background processing |
| **Broki Services · CallHQ.ai** | CRM automation, AI integrations and backend optimization | Node.js, RAG, FastAPI, GCP Cloud Run |
| **Specstem Digital** | Backend APIs and asynchronous processing | Express, AWS, BullMQ |

> These are summaries of my contributions and technologies, not disclosures of proprietary system internals.

## 🧠 Systems design playground

I document architecture by starting with **requirements and failure modes**, then comparing simpler and more scalable alternatives.

<details open>
<summary><b>01 · Retrieval-Augmented Generation — asynchronous ingestion and retrieval</b></summary>

```mermaid
flowchart LR
  A[Documents / APIs] --> B[Ingestion Service]
  B --> C[Job Queue]
  C --> D[Chunk + Embed Workers]
  D --> E[(Vector Index)]
  F[User Question] --> G[Query Processing]
  G --> H[Hybrid Search]
  E --> H
  H --> I[Rerank / Context Limit]
  I --> J[Model Router]
  J --> K[Stream Answer]
```

| Decision | Benefit | Cost / risk |
| :--- | :--- | :--- |
| Queue ingestion | Handles spikes, retries | Index freshness lag |
| Hybrid retrieval | Better lexical + semantic recall | More tuning and infrastructure |
| Reranking | Better context relevance | Added latency and cost |
| Model routing | Latency/cost control | Fallback and evaluation complexity |

**Measure:** retrieval recall, grounded answer quality, token cost, queue age, p95 end-to-end latency.

</details>

<details>
<summary><b>02 · Real-time messaging — connections, persistence and fan-out</b></summary>

```mermaid
flowchart LR
  A[Mobile / Web] --> B[Load Balancer]
  B --> C[WebSocket Gateways]
  C --> D[(Redis Presence)]
  C --> E[Message Service]
  E --> F[(Durable Store)]
  E --> G[Event Stream]
  G --> H[Delivery Workers]
  H --> C
```

**Design choices:** Persist messages before acknowledging durable delivery; use message IDs for deduplication; treat presence as ephemeral; use backpressure and reconnect/resume logic. Redis helps with transient coordination, not as the sole source of durable messages.

**Measure:** active connections, reconnect rate, delivery lag, dropped events and p99 send-to-receive latency.

</details>

<details>
<summary><b>03 · Notification pipeline — bursts, retries and idempotency</b></summary>

```mermaid
flowchart LR
  A[Product Events] --> B[Notification Service]
  B --> C[Redis / BullMQ]
  C --> D[Delivery Workers]
  D --> E[Push / Email / In-app]
  D --> F[(Delivery State)]
  D --> G[Retry / Dead Letter]
```

**Design choices:** Queue bursts to protect downstream providers; enforce user preferences before sending; use deduplication keys; bound retry attempts; monitor dead-letter queues and provider failures.

**Measure:** queue lag, duplicate-send rate, delivery success rate, p95 processing latency.

</details>

<details>
<summary><b>04 · System design checklist — my trade-off framework</b></summary>

| Dimension | Questions I ask |
| :--- | :--- |
| **Correctness** | What must be atomic? What can be eventually consistent? |
| **Load** | Read/write ratio? Peak concurrency? Hot keys? |
| **Data** | SQL vs document store? Index strategy? Retention? |
| **Reliability** | Timeouts? Retries? Idempotency? Failure isolation? |
| **Observability** | Logs, metrics, traces, SLOs and alert thresholds? |
| **Cost** | Can we scale workers before adding more services? |

</details>

<sub>Architecture diagrams are illustrative reference designs and are not claims about internal production deployments.</sub>

## 🧪 Building in public

<div align="center">

<a href="https://github.com/flutter-create-ani/go_learning">
  <img width="75%" src="https://github-readme-stats.vercel.app/api/pin/?username=flutter-create-ani&repo=go_learning&theme=github_dark&hide_border=true" alt="Go learning repository" />
</a>

**Current focus:** Go · production engineering · observability · distributed systems · algorithmic problem solving

</div>

## 🤝 Connect

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-Explore_Repositories-181717?style=for-the-badge&logo=github)](https://github.com/flutter-create-ani?tab=repositories)
[![LeetCode](https://img.shields.io/badge/LeetCode-Problem_Solving-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/anie25/)

**Build simply · Measure carefully · Scale deliberately**

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&section=footer&height=100&color=0:1F6FEB,100:0D1117" alt="Footer wave" />

</div>
