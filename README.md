<div align="left">

# Shivam Singh
**Software Engineer - Backend & Distributed Systems**  
*Designing multi-tenant SaaS architectures, high-throughput APIs, and production cloud infrastructure.*

[![Portfolio](https://img.shields.io/badge/Portfolio-0d1117?style=flat-square&logo=vercel&logoColor=white)](https://portfolio-projecttesting.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0d1117?style=flat-square&logo=linkedin&logoColor=0a66c2)](https://www.linkedin.com/in/shivam-singh-37b56b28b/)
[![Email](https://img.shields.io/badge/shivamsingh4940x@gmail.com-0d1117?style=flat-square&logo=gmail&logoColor=ea4335)](mailto:shivamsingh4940x@gmail.com)

</div>

---

### ⚡ Production Footprint

- **High-Throughput Commerce & Custom Credit Engine:** Sole architect of a production commerce backend on AWS EC2; designed the relational schema, custom credit ledger, and idempotent payment gateway webhooks sustaining **1,000 req/sec** in load tests.
- **Multi-Tenant SaaS & Access Control:** Led technical architecture for a multi-tenant B2B SaaS platform, engineering shared-schema data isolation and module-level RBAC to strictly segregate tenant data and permissions.
- **Enterprise Backend & Cloud Infrastructure:** Architected a 50+ endpoint NestJS, Prisma, and PostgreSQL system deployed across DigitalOcean VMs, load balancers, and managed database clusters—establishing structured logging, baseline Jest test suites, and a cross-platform Flutter client used daily in production.
- **Performance Optimization & API Hardening:** Cut production Next.js storefront load times by **30%** via code splitting and React Query caching, and enforced **100% endpoint validation** and error-handling coverage across REST services.
- **Technical Leadership & Mentorship:** Own end-to-end delivery from schema design to cloud deployment while driving architectural decisions, enforcing PR review standards, and mentoring 3–4 junior engineers and interns.
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
| **Observability & QA** | Prometheus, Grafana, Loki, Vitest, Postman |
| **Client & Mobile** | Next.js, React, React Query, Tailwind CSS, Flutter |
| **AI & Automation** | Model Context Protocol (MCP), Agentic Workflows, Claude Code |
