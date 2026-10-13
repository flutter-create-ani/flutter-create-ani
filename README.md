<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=230&color=0:0D1117,45:123D5A,100:1F6FEB&text=Aniket%20Kumar&fontColor=FFFFFF&fontSize=55&fontAlignY=37&desc=Full%20Stack%20Developer%20%E2%80%A2%20Distributed%20Systems%20%E2%80%A2%20AI%20Engineering&descAlignY=59&animation=fadeIn" width="100%" alt="Aniket Kumar banner" />

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=21&pause=1000&color=58A6FF&center=true&vCenter=true&width=800&lines=I+build+full-stack+products+that+scale;Real-time+systems+%7C+Cloud+%7C+AI;Learning+Go+and+production+engineering;Design+for+correctness%2C+then+measure+and+scale" alt="Animated introduction" />

[![GitHub](https://img.shields.io/badge/GitHub-flutter--create--ani-181717?style=for-the-badge&logo=github)](https://github.com/flutter-create-ani)
[![LeetCode](https://img.shields.io/badge/LeetCode-anie25-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/anie25/)
[![Go Learning](https://img.shields.io/badge/Learning-Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)](https://github.com/flutter-create-ani/go_learning)

</div>

## 👨‍💻 About me

Full Stack Developer with experience building **SaaS platforms, real-time features, AI workflows, background processing pipelines, and cloud-deployed services**. I enjoy understanding bottlenecks, evaluating trade-offs, and building systems that remain maintainable as they grow.

- 🏢 **Software Development Engineer I — ARM Worldwide**
- 🛠️ Previously **Broki Services** and **Specstem Digital**
- 🧠 Interested in **distributed systems, scalable RAG, WebRTC, observability, and reliability**
- 🌱 Currently learning **Go** and deepening my production-engineering skills
- 🎯 Practicing algorithms on **[LeetCode / anie25](https://leetcode.com/u/anie25/)**

## ⚡ My toolkit

<div align="center">
<img src="https://skillicons.dev/icons?i=js,ts,java,go,python,dart,react,nextjs,nodejs,express,flutter,tailwind&perline=6" alt="Languages and frameworks" />
<br/>
<img src="https://skillicons.dev/icons?i=postgres,mysql,mongodb,redis,firebase,aws,gcp,docker,githubactions,nginx,git,linux&perline=6" alt="Databases, cloud and infrastructure" />
</div>

**Also working with:** Kafka · BullMQ · RabbitMQ · Socket.IO · WebRTC · LiveKit · LangChain · RAG · Vector Search · MCP · REST APIs

## 📊 Live GitHub dashboard

<div align="center">
<img height="175" src="https://github-readme-stats.vercel.app/api?username=flutter-create-ani&show_icons=true&theme=github_dark&hide_border=true&rank_icon=github" alt="GitHub stats" />
<img height="175" src="https://github-readme-stats.vercel.app/api/top-langs/?username=flutter-create-ani&layout=compact&theme=github_dark&hide_border=true&langs_count=8" alt="Top languages" />
<br/>
<img width="95%" src="https://github-readme-activity-graph.vercel.app/graph?username=flutter-create-ani&theme=github-compact&hide_border=true&area=true" alt="GitHub activity graph" />
</div>

> These GitHub cards are served by third-party providers and may be cached or rate-limited.

## 🐍 Animated LeetCode submission calendar

<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/output/leetcode-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/output/leetcode-snake.svg" />
  <img width="100%" alt="Animated LeetCode submission calendar for anie25" src="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/output/leetcode-snake-dark.svg" />
</picture>

[![LeetCode Stats](https://leetcard.jacoblin.cool/anie25?theme=dark&font=JetBrains%20Mono&ext=heatmap)](https://leetcode.com/u/anie25/)

</div>

> The animated calendar uses **LeetCode submission activity**, not GitHub commits. It appears after the first successful **Generate LeetCode Submission Snake** workflow run. The visualization follows submission dates; it is not the original Platane/snk cell-eating algorithm. LeetCode's public calendar data and third-party stat cards may sometimes be unavailable.

## 🚀 Engineering experience

| Product / team | What I worked on | Engineering themes |
|---|---|---|
| **ARM Worldwide · Luminary** | Full-stack AI platform, LLM orchestration | Next.js, React, Node.js, LLM routing |
| **Komorebi.fit** | Fitness integrations, device sync, notifications | Terra API, background jobs, event handling |
| **Broki Services · CallHQ.ai** | CRM automation, AI integrations, API improvements | Node.js, RAG, GCP Cloud Run |
| **Specstem Digital** | Backend services and background processing | Express, AWS, BullMQ |

## 🏗️ Architecture lab — how I approach scale

> The following diagrams are **illustrative reference architectures** based on engineering patterns I study and apply. They do not disclose or represent verified internal architectures of employers.

<details open>
<summary><b>🤖 Scalable RAG: ingestion, retrieval, generation</b></summary>

```mermaid
flowchart LR
  A[Documents / APIs] --> B[Ingestion API]
  B --> C[Queue]
  C --> D[Chunk + Embed Workers]
  D --> E[(Vector Store)]
  F[User Query] --> G[Query Embedding]
  G --> H[Hybrid Retrieval]
  E --> H
  H --> I[Rerank + Context Budget]
  I --> J[LLM Router]
  J --> K[Streaming Response]
```

**Design trade-offs:** Async ingestion isolates spikes but adds processing delay; hybrid retrieval improves recall but costs more; reranking can improve relevance but increases latency; LLM routing controls cost while adding fallback complexity. Evaluate recall, p95 latency, token cost, and answer quality before tuning.

</details>

<details>
<summary><b>💬 Real-time messaging: delivery and fan-out</b></summary>

```mermaid
flowchart LR
  A[Clients] --> B[Load Balancer]
  B --> C[WebSocket Nodes]
  C --> D[(Redis Presence)]
  C --> E[Message API / Service]
  E --> F[(Message Database)]
  E --> G[Event Bus]
  G --> H[Fan-out Workers]
  H --> C
```

**Design trade-offs:** WebSockets provide low-latency bidirectional communication but require connection management; Redis presence is fast but ephemeral; message persistence and idempotent consumers help handle retries and duplicates.

</details>

<details>
<summary><b>🔔 High-volume notifications: queue-backed delivery</b></summary>

```mermaid
flowchart LR
  A[Business Events] --> B[Notification API]
  B --> C[Queue / BullMQ]
  C --> D[Workers]
  D --> E[Push / Email / In-app]
  D --> F[(Delivery Status)]
  D --> G[Retries / DLQ]
```

**Design trade-offs:** Queues absorb bursts but introduce eventual consistency. Use idempotency keys, bounded retries, rate limits, and delivery metrics. Monitor queue lag and p95 processing latency.

</details>

## 🧪 Currently exploring

<div align="center">

[![Go Learning Repository](https://github-readme-stats.vercel.app/api/pin/?username=flutter-create-ani&repo=go_learning&theme=github_dark&hide_border=true)](https://github.com/flutter-create-ani/go_learning)

</div>

**Engineering principle:** *Start simple. Measure real bottlenecks. Scale deliberately. Document trade-offs.*

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&section=footer&height=100&color=0:1F6FEB,100:0D1117" width="100%" alt="Footer" />
</div>
