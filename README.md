<div align="left">

# Shivam Singh
**Software Engineer — Backend & Distributed Systems**  
*Designing multi-tenant SaaS architectures, high-throughput APIs, and production cloud infrastructure.*

[![Portfolio](https://img.shields.io/badge/Portfolio-0d1117?style=flat-square&logo=vercel&logoColor=white)](https://portfolio-projecttesting.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0d1117?style=flat-square&logo=linkedin&logoColor=0a66c2)](https://www.linkedin.com/in/shivam-singh-37b56b28b/)
[![Email](https://img.shields.io/badge/shivamsingh4940x@gmail.com-0d1117?style=flat-square&logo=gmail&logoColor=ea4335)](mailto:shivamsingh4940x@gmail.com)

> *Note: My day-to-day production commits live on separate company/organization GitHub accounts.*

</div>

---

### ⚡ Production Footprint

- **Multi-Tenant SaaS Architecture:** Engineered shared-schema data isolation and module-level RBAC to enforce strict tenant boundaries at scale.
- **High-Throughput Commerce & Payments:** Architected an end-to-end commerce backend on AWS EC2 with a custom credit system and webhook-driven payment pipelines, sustaining **1,000 req/sec** in load tests.
- **End-to-End Delivery:** Shipped cross-platform mobile (Flutter) and web (Next.js) applications backed by hardened NestJS/PostgreSQL services, async job queues, and full-stack observability.

---

### 🌐 Open Source

- **[OpenClaude (`PR #249`)](https://github.com/Gitlawb/openclaude/pull/249)** — Fixed a memory-exhausting infinite retry loop in the CLI authentication flow by implementing exponential backoff and a retry cap while preserving transient-failure retries.

---

### 🏗 Reference Architecture I Build & Operate

```text
+-----------------------+       +------------------------------------+
| Web (Next.js) &       |       | Load Balancer / Reverse Proxy      |
| Mobile (Flutter) Apps | ----> | (TLS Termination & Rate Limiting)  |
+-----------------------+       +-----------------+------------------+
                                                  |
                                                  v
+-----------------------+       +------------------------------------+
| Observability Stack   | < - - | NestJS Modular API Core            |
| Prometheus / Grafana  |       | (Guards, Module-Level RBAC, REST)  |
| Loki Structured Logs  | < - + +--------+------------------+--------+
+-----------------------+     :          |                  |
                              :          v                  v
                              : +----------------+  +----------------+
                              : | PostgreSQL     |  | Redis Cluster  |
                              : | Shared-Schema  |  | Cache Layer &  |
                              : | Multi-Tenancy  |  | BullMQ Broker  |
                              : +----------------+  +-------+--------+
                              :                             |
                              :                             v
                              :                     +----------------+
                              + - - - - - - - - - - | Async Workers  |
                                                    | Webhooks, Jobs |
                                                    | & Credit Ledger|
                                                    +----------------+
```

---

### 🛠 Systems & Tooling

| Layer | Technologies |
| :--- | :--- |
| **Core Backend** | TypeScript, Node.js, NestJS, Express, REST, WebSockets, BullMQ |
| **Data & ORM** | PostgreSQL, Redis, MongoDB, Prisma |
| **Infra & DevOps** | AWS (EC2), DigitalOcean, Kubernetes, Docker, GitHub Actions |
| **Observability & QA** | Prometheus, Grafana, Loki, Jest, Vitest, Postman |
| **Client & Mobile** | Next.js, React, React Query, Tailwind CSS, Flutter |
| **AI & Automation** | Model Context Protocol (MCP), Agentic Workflows, Claude Code, OpenCode, Python |
