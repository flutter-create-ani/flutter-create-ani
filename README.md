<div align="center">

# Hey, I'm Aniket Kumar 👋

### Full Stack Developer · Distributed Systems · AI Engineering

*Building scalable, real-time products and designing systems for reliability, performance, and growth.*

[![Portfolio](https://img.shields.io/badge/Portfolio-Explore-0A66C2?style=for-the-badge&logo=googlechrome&logoColor=white)](https://github.com/flutter-create-ani)
[![GitHub](https://img.shields.io/badge/GitHub-flutter--create--ani-181717?style=for-the-badge&logo=github)](https://github.com/flutter-create-ani)
[![LeetCode](https://img.shields.io/badge/LeetCode-My%20Progress-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/YOUR_LEETCODE_USERNAME/)

</div>

---

## ⚡ What I build

<table>
<tr>
<td width="50%" valign="top">

**🌐 Full-stack products**

React, Next.js, Flutter, Node.js, TypeScript, REST APIs, PostgreSQL and MongoDB.

</td>
<td width="50%" valign="top">

**⚙️ Scalable backends**

Redis, BullMQ, Kafka, WebSockets, real-time chat, queues, caching and asynchronous processing.

</td>
</tr>
<tr>
<td valign="top">

**🤖 AI-powered systems**

RAG, LangChain, vector search, LLM orchestration, voice agents and MCP integrations.

</td>
<td valign="top">

**☁️ Cloud & reliability**

AWS, GCP Cloud Run, Docker, GitHub Actions, observability and production optimization.

</td>
</tr>
</table>

## 🧑‍💻 Experience & selected engineering work

| Team / product | Focus | Engineering highlights |
|---|---|---|
| **ARM Worldwide** | Software Development Engineer I | Full-stack development, multi-LLM orchestration, real-time systems, notification pipelines |
| **Komorebi.fit** | Fitness platform | Terra API integrations, device data synchronization, notification preferences |
| **Luminary** | AI platform | Next.js / React / Node.js, LLM orchestration and product development |
| **Broki Services / CallHQ.ai** | SaaS and automation | Workflow automation, RAG integrations, API optimization and GCP deployments |
| **Specstem Digital** | Backend engineering | Node.js, Express, AWS and background jobs |

> The diagrams below illustrate architectural approaches I work with; they are not claims about the exact internal production topology of any employer.

## 🏗️ How I think about system design

**Design for correctness first, then scale the bottleneck you can measure.**

| Problem | Design choice | Trade-off |
|---|---|---|
| Bursty writes and notifications | Queue-based asynchronous workers | Eventual consistency and retry complexity |
| Repeated high-volume reads | Redis caching | Cache invalidation and stale reads |
| Real-time messaging | WebSockets + shared coordination layer | Connection lifecycle and ordering |
| Retrieval-augmented generation | Ingestion → chunking → embeddings → retrieval → reranking → LLM | Retrieval quality, latency and cost |
| Distributed integrations | Idempotency keys, retries and dead-letter queues | Operational overhead |

<details>
<summary><b>🔎 Scalable RAG architecture — click to expand</b></summary>

```text
Documents / APIs
       |
       v
Ingestion + Validation ---> Background Queue
                                  |
                                  v
                          Chunk + Embed
                                  |
                                  v
                          Vector Index
                                  |
User -> API -> Auth -> Query Embedding -> Hybrid Retrieval
                                          |
                                          v
                                      Reranking
                                          |
                                          v
                                 Context + LLM
                                          |
                                          v
                              Grounded Response
```

**Scale considerations:** asynchronous ingestion, document versioning, tenant-aware filtering, caching, tracing, token budgets and retrieval evaluation.

</details>

<details>
<summary><b>📡 Real-time system architecture — click to expand</b></summary>

```text
Clients
  |
Load Balancer
  |
WebSocket / API Nodes
  |             \
  |              -> Redis (presence / coordination)
  v
Message Service -> Database
  |
  v
Event Queue -> Notification Workers -> Push / In-app
```

**Trade-offs:** delivery acknowledgements, deduplication, backpressure, reconnect recovery and message ordering.

</details>

## 🛠️ Technology stack

<div align="center">

![Skills](https://skillicons.dev/icons?i=js,ts,java,go,python,dart,react,nextjs,nodejs,express,flutter,postgres,mongodb,mysql,redis,aws,gcp,docker,githubactions,git,linux&perline=7)

</div>

## 📈 GitHub activity

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=flutter-create-ani&show_icons=true&include_all_commits=true&theme=tokyonight&hide_border=true" alt="GitHub statistics" height="165" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=flutter-create-ani&layout=compact&theme=tokyonight&hide_border=true" alt="Most used public repository languages" height="165" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=flutter-create-ani&theme=tokyo-night&hide_border=true" alt="GitHub contribution activity graph" width="100%" />

</div>

### 🐍 Contribution snake — refreshed daily

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/output/github-snake.svg" />
  <img alt="Snake animation eating my GitHub contributions" src="https://raw.githubusercontent.com/flutter-create-ani/flutter-create-ani/output/github-snake.svg" width="100%" />
</picture>

</div>

## 🧩 LeetCode progress

<div align="center">

[![LeetCode Stats](https://leetcard.jacoblin.cool/aniec25?theme=dark&font=Inter&ext=heatmap)](https://leetcode.com/aniec25/)

[![LeetCode Profile](https://img.shields.io/badge/Practice-Data%20Structures%20%26%20Algorithms-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/aniec25/)

</div>

*LeetCode stats are provided by an external card service and may be cached or temporarily unavailable.*

## 🚀 Currently exploring

- **Go:** language fundamentals, concurrency and backend development.
- **AI engineering:** production RAG, agents and LLM evaluation.
- **SRE:** observability, reliability, load testing and incident response.
- **System design:** resilient distributed services and real-time infrastructure.

## 🤝 Connect

<div align="center">

**Interested in full-stack engineering, AI systems, and scalable products?**

[![GitHub](https://img.shields.io/badge/Explore%20my%20repositories-181717?style=for-the-badge&logo=github)](https://github.com/flutter-create-ani?tab=repositories)

</div>
