```
                    ██████╗ ██████╗  ██████╗ ██████╗ ██╗ ██████╗██╗   ██╗
                    ██╔══██╗██╔══██╗██╔═══██╗██╔══██╗██║██╔════╝╚██╗ ██╔╝
                    ██████╔╝██████╔╝██║   ██║██║  ██║██║██║  ███╗╚████╔╝
                    ██╔═══╝ ██╔══██╗██║   ██║██║  ██║██║██║   ██║ ╚██╔╝
                    ██║     ██║  ██║╚██████╔╝██████╔╝██║╚██████╔╝  ██║
                    ╚═╝     ╚═╝  ╚═╝ ╚═════╝ ╚═════╝ ╚═╝ ╚═════╝   ╚═╝
```

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=24&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&multiline=true&repeat=true&width=600&height=80&lines=Freelance+Backend+Engineer;Building+Systems+That+Scale)](https://github.com/prodigy90)

[![Profile Views](https://komarev.com/ghpvc/?username=prodigy90&color=1a1b27&style=for-the-badge&label=PROFILE+VIEWS)](https://github.com/prodigy90)
[![GitHub Followers](https://img.shields.io/github/followers/prodigy90?style=for-the-badge&color=1a1b27&labelColor=1a1b27&logo=github)](https://github.com/prodigy90)
[![Twitter Follow](https://img.shields.io/twitter/follow/ladipov?style=for-the-badge&color=1a1b27&labelColor=1a1b27&logo=x)](https://twitter.com/ladipov)

</div>

---

## `> whoami`

```go
package main

type Engineer struct {
    Name        string
    Location    string
    Philosophy  string
    Alias       string
    Contact     string
    Role        string
}

var prodigy = Engineer{
    Name:       "Prodigy",
    Location:   "Nigeria",
    Philosophy: "I will win.",
    Alias:      "Victor James",
    Contact:    "admin@wasbot.ng",
    Role:       "Freelance Backend Engineer",
}

var stack = map[string][]string{
    "databases": {"PostgreSQL", "MySQL", "Redis", "MinIO"},
    "languages": {"Go", "TypeScript", "Python", "JavaScript"},
    "messaging": {"WhatsApp API", "Telegram Bot API", "WebSockets"},
    "backend":   {"Gin", "Express.js", "Telegraf", "Asynq", "BullMQ"},
    "devops":    {"K8s", "K3s", "Docker", "Traefik", "GitHub Actions"},
}

var currentFocus = []string{
    "Payment System Integration",
    "Multi-tenant SaaS Platforms",
    "High-Availability Messaging",
    "Serverless Pod Architectures",
}
```

---

## `> skills --list`

<details>
<summary><b>Performance Optimization</b></summary>
<br>

| Area     | Expertise                                                   |
| -------- | ----------------------------------------------------------- |
| Memory   | Leak detection, garbage collection tuning, profiling        |
| Caching  | Redis strategies, cache invalidation, CDN integration       |
| Analysis | Load testing, bottleneck identification, benchmarking       |
| API      | Response time improvements, payload optimization, caching   |
| Database | Query optimization, indexing strategies, connection pooling |

</details>

<details>
<summary><b>System Scaling</b></summary>
<br>

| Area           | Expertise                                               |
| -------------- | ------------------------------------------------------- |
| Load Balancing | Nginx, HAProxy, cloud load balancers                    |
| Databases      | Sharding, replication, read replicas                    |
| Monitoring     | Grafana, Prometheus, alerting pipelines                 |
| Availability   | Failover strategies, health checks, circuit breakers    |
| Architecture   | Horizontal scaling, microservices, event-driven systems |

</details>

<details>
<summary><b>Messaging Automation</b></summary>
<br>

| Area      | Expertise                                               |
| --------- | ------------------------------------------------------- |
| Telegram  | Bot development, webhooks, multi-tenant platforms       |
| Real-time | WebSocket servers, message queuing, event streaming     |
| Scale     | Rate limiting, queue processing, concurrent sessions    |
| WhatsApp  | Business automation, bulk messaging, session management |

</details>

<details>
<summary><b>Backend Development</b></summary>
<br>

| Area         | Expertise                                           |
| ------------ | --------------------------------------------------- |
| DevOps       | Docker, CI/CD, deployment automation                |
| Architecture | Clean code, SOLID principles, design patterns       |
| Security     | Input validation, encryption, secure sessions       |
| APIs         | REST design, GraphQL, authentication, rate limiting |

</details>

---

## `> projects --active`

### WASBOT

> WhatsApp automation platform with serverless K8s architecture

```yaml
url: https://www.wasbot.ng
status: Production
arch: Microservices Monorepo (6 services)
stack: [Go, TypeScript, PostgreSQL, Redis, K3s, Traefik]
```

**Architecture:**

- **Serverless WhatsApp Sessions** - Worker pods created on-demand per user
- **Dual-Server Setup** - App server (K3s) + Data server (PostgreSQL/Redis)
- **K3s Cluster** - API server with RBAC manages pod lifecycle dynamically
- **Custom whatsmeow fork** - Enhanced with status recipient support

**Services:**

- `wasbot-backend` - Go/Gin API + dynamic worker pods
- `wasbot-frontend` - Next.js 16 dashboard with Better Auth
- `email-service-go` - Transactional emails via SMTP/Resend
- `affiliate-system-go` - Referral tracking with commission payouts
- `webhook-router-go` - Multi-currency payment routing (Paystack/Flutterwave)

**Features:**

- Google Contacts OAuth integration
- Link preview generation for messages
- Multi-currency: NGN, USD, EUR, GBP, KES, GHS, ZAR
- History sync with MinIO persistence (tier-based limits)
- Subscription tiers: Trial → Basic → Premium → Enterprise

---

### Telegram Multi-tenant SaaS

> Production-ready platform running 100+ tenant bots in single process

```yaml
status: Production Ready
stack: [Node.js, TypeScript, MySQL, Redis, BullMQ, Telegraf]
```

**Architecture:**

- **Subscription-Aware** - Only runs bots with active subscriptions
- **Bot Orchestrator** - Manages `Map<tenantId, Map<botId, TenantBot>>`
- **Complete Tenant Isolation** - Composite PKs, tenant_id FKs on all tables
- **MySQL-First Design** - Persistent state in DB, Redis for ephemeral cache only

**Features:**

- Auto-accept system with configurable delays
- Message sequences with rich media + custom buttons
- Smart trigger router (Button → Command → Text priority)
- Broadcast system with delivery tracking
- Variable system: `[name]`, `[user:STAGE]`, tenant variables
- Admin messaging campaigns with priority levels
- Payment integration with auto-renewal reminders

---

## `> contributions --open-source`

<table>
<tr>
<td width="50%">

### [baileys](https://github.com/WhiskeySockets/Baileys)

WhatsApp Web API for Node.js

- Performance optimizations
- Stability improvements
- Connection management

</td>
<td width="50%">

### [whatsmeow](https://github.com/tulir/whatsmeow)

WhatsApp Web API for Go

- Code optimizations
- Testing and validation
- Bug fixes and debugging

</td>
</tr>
</table>

---

## `> tech --stack`

<div align="center">

**Languages**

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

**Backend**

![Gin](https://img.shields.io/badge/Gin-00ADD8?style=flat-square&logo=go&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![Telegraf](https://img.shields.io/badge/Telegraf-26A5E4?style=flat-square&logo=telegram&logoColor=white)

**Databases & Storage**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![MinIO](https://img.shields.io/badge/MinIO-C72E49?style=flat-square&logo=minio&logoColor=white)

**DevOps & Cloud**

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![K3s](https://img.shields.io/badge/K3s-FFC61C?style=flat-square&logo=k3s&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Traefik](https://img.shields.io/badge/Traefik-24A1C1?style=flat-square&logo=traefikproxy&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**Tools & Queues**

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![BullMQ](https://img.shields.io/badge/BullMQ-DC382D?style=flat-square&logo=redis&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)

</div>

---

## `> stats --github`

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=prodigy90&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=58a6ff&text_color=c9d1d9" height="165" alt="GitHub Stats" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=prodigy90&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9&langs_count=6" height="165" alt="Top Languages" />

<img src="https://streak-stats.demolab.com?user=prodigy90&theme=github-dark-blue&hide_border=true&background=0D1117&stroke=58a6ff&ring=58a6ff&fire=58a6ff&currStreakLabel=58a6ff" alt="GitHub Streak" />

<img src="https://github-profile-trophy.vercel.app/?username=prodigy90&theme=darkhub&no-frame=true&no-bg=true&margin-w=4&row=1&column=6" alt="GitHub Trophies" />

</div>

---

## `> learning --current`

```diff
+ Advanced distributed systems patterns
+ Event sourcing & CQRS architectures
+ gRPC for inter-service communication
+ Advanced PostgreSQL (partitioning, JSONB)
+ Observability at scale (OpenTelemetry)
```

---

## `> philosophy`

```
"I will win."
```

Not just a statement—a commitment to solving hard problems and building systems that scale.

| Principle                        | Description                              |
| -------------------------------- | ---------------------------------------- |
| **Optimize first, scale second** | Make it fast before making it big        |
| **Measure everything**           | You can't improve what you don't measure |
| **Pragmatic solutions**          | Right tool for the job, not the newest   |
| **Ship iteratively**             | Perfect is the enemy of done             |
| **Learn from failures**          | Every bug is a lesson                    |

---

## `> experience --freelance`

```
[+] Built serverless WhatsApp platform with K8s pod-per-session architecture
[+] Designed multi-tenant Telegram SaaS handling 100+ bots in single process
[+] Implemented multi-currency payment systems (7 currencies, 2 processors)
[+] Created microservices monorepo with 6 Go/Node.js services
[+] Set up K3s clusters with Traefik ingress and automatic TLS
[+] Built affiliate systems with commission tracking and payouts
```

**Focus Areas:** `Kubernetes` `Multi-tenant SaaS` `Payment Integration` `Messaging Automation` `Microservices`

---

## `> contact --available`

<div align="center">

[![Email](https://img.shields.io/badge/Email-admin@wasbot.ng-1a1b27?style=for-the-badge&logo=gmail&logoColor=white)](mailto:admin@wasbot.ng)
[![Website](https://img.shields.io/badge/Website-wasbot.ng-1a1b27?style=for-the-badge&logo=safari&logoColor=white)](https://www.wasbot.ng)

[![Twitter](https://img.shields.io/badge/@ladipov-1a1b27?style=for-the-badge&logo=x&logoColor=white)](https://twitter.com/ladipov)
[![LinkedIn](https://img.shields.io/badge/Prodigy-1a1b27?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/victor-james-ladipo)
[![Instagram](https://img.shields.io/badge/@ladipovj-1a1b27?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/ladipovj)
[![YouTube](https://img.shields.io/badge/Prodigy-1a1b27?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/c/victorjamesladipo)

</div>

---

## `> services --available`

| Service                    | Description                                            |
| -------------------------- | ------------------------------------------------------ |
| **Backend Development**    | APIs, microservices, system architecture               |
| **Performance Consulting** | Optimization, profiling, bottleneck analysis           |
| **Scaling Solutions**      | High-availability, load balancing, distributed systems |
| **Messaging Automation**   | WhatsApp/Telegram bots, real-time systems              |
| **Code Reviews**           | Architecture feedback, best practices                  |

---

<div align="center">

```
╔═══════════════════════════════════════════════════════════════╗
║  Building fast, scalable systems one optimization at a time   ║
╚═══════════════════════════════════════════════════════════════╝
```

**[@prodigy90](https://github.com/prodigy90)**

</div>
