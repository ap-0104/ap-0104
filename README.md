# Ansh Prasad

**Senior Backend Infrastructure Engineer | Technical Product Owner**

Backend engineer specializing in email infrastructure, distributed systems, and high-throughput SaaS platforms. I build the backend layer that determines whether a platform succeeds at scale — the part most users never see but which governs every metric that matters.

---

## About

3.7 years architecting and scaling SMTP delivery systems, domain warmup engines, inbox placement infrastructure, and multi-ESP orchestration layers from zero to production.

- Processed **100M+ emails/day** at **350–400 emails/sec** with zero downtime
- Scaled domain warmup from **40K to 400K+ emails/day per domain** over 21 days
- Rebuilt a cascading SMTP pipeline from scratch — **600× throughput improvement**
- Built inbox placement scoring with **30+ RBL checks** and **95% spam detection accuracy**
- Deep expertise in **SPF, DKIM, DMARC, DNS, IP reputation** — production every day
- Continuously research how Gmail, Outlook, and Yahoo evolve their filtering logic through proprietary methods

---

## Personal Projects

### InboxTri — Self-Hosted Email Campaign Engine
[inboxtri.com](https://inboxtri.com)

A full-stack, production-grade email campaign engine with a high-throughput Python sending engine backed by Kafka and Redis. All sensitive data is encrypted at rest with AES-256-GCM. Includes a 5-layer email analyzer with SpamAssassin integration.

- Multi-SMTP campaign dispatch with round-robin and TLD-based domain routing
- Real-time open pixel tracking, click redirects, and DSN-based bounce classification
- Automatic DKIM RSA-2048 key generation and DNS verification per sender domain
- IP warmup with configurable daily ramp schedule per SMTP server
- 5-layer email analyzer: SpamAssassin + 12 CAN-SPAM rules + HTML intelligence + per-provider inbox placement prediction (Gmail/Outlook/Yahoo) + AI rewrite suggestions
- AES-256-GCM encryption on all sensitive fields at rest
- HMAC-SHA256 signed webhooks for all delivery events
- Suppression management supporting 10M+ row async CSV import

**Stack:** Python 3.11 · Apache Kafka · Redis · Docker · PostgreSQL · SpamAssassin

---

## Company Projects

### Mailcrux — SMTP & Email Infrastructure

Took full ownership of the Mailcrux backend on Ruby on Rails — engineered a high-throughput SMTP delivery system with isolated IP pools, idempotent sending queues, and per-sender authentication pipelines implementing circuit breaker patterns to prevent reputation bleed between customer segments.

| Metric | Value |
|--------|-------|
| Throughput improvement | 100× |
| Response latency | −60% |
| Platform uptime | 99% |

- IP pool architecture with per-IP release control and sender isolation
- Circuit breaker patterns preventing reputation bleed across segments
- Rate limiting per SMTP with hour/day granularity
- Queue-based processing via Kafka/RabbitMQ with backpressure controls
- Hardened REST API pipelines with rate limiting and idempotency enforcement
- Horizontal scaling via multiple SMTP servers

**Stack:** Ruby on Rails · RabbitMQ · Kafka · Docker

---

### Sendcrux — Campaign Orchestration Engine

Designed the multi-ESP orchestration engine — a fault-tolerant sending layer with real-time capacity validation, bounce classification, self-healing campaign scheduling, retry strategies, and dead letter queue handling across multiple ESP providers.

| Metric | Value |
|--------|-------|
| Emails/day | 100M+ |
| Sending rate | 350–400/sec |
| Events/day | 100M+ |

- Multi-ESP integration with real-time capacity validation
- Fault-tolerant self-healing campaign scheduling
- Dead letter queue handling and retry strategies
- CRM automation pipelines covering full subscriber lifecycle
- Partner Program backend with idempotent commission calculation
- Automated monthly payout processing

**Stack:** Kafka · Event-Driven Architecture · Backpressure Controls · Laravel

---

### WarmupIP — Autonomous Domain Warmup Engine

Engineered an autonomous domain warmup engine with provider-aware ramp-up scheduling that adapts sending velocity in real-time using backpressure signals from bounce rates and ESP feedback loops, scaling each domain from 40K to 400K+ emails/day over 21 days while maintaining sender reputation above deliverability thresholds.

| Metric | Value |
|--------|-------|
| Throughput | 350–400/sec |
| Peak volume/domain | 400K+/day |
| Warmup period | 21 days |

- Provider-aware ramp-up scheduling with real-time velocity adaptation
- Backpressure signals from bounce rates and ESP feedback loops
- Scales domains from 40K to 400K+ emails/day over 21 days
- Reputation monitoring above deliverability thresholds
- Engagement simulation — opens, clicks, replies
- Gradual volume scaling with automated adjustment

**Stack:** Laravel · RabbitMQ · Redis · Python · Docker

---

### Inbox Placement Platform — Deliverability Testing & ML Scoring

Designed and shipped a multi-provider inbox placement scoring system as a Dockerized microservice, integrating SPF/DKIM/DMARC validation, 30+ real-time RBL checks, and an ML-backed spam classification pipeline achieving 95% detection accuracy — delivering cold-start domain health scores in under 3 seconds at full production load.

| Metric | Value |
|--------|-------|
| RBL checks | 30+ |
| Detection accuracy | 95% |
| Score latency | <3 seconds |

- Placement detection via metadata — no email opening required
- SPF/DKIM/DMARC validation pipeline
- 30+ real-time RBL blacklist integrations
- ML-backed spam classification with 95% detection accuracy
- Cold-start domain health scores in under 3 seconds
- Dockerized microservice at full production load

**Stack:** Python · Docker · SPF/DKIM/DMARC

---

### Master Inbox — Unified Multi-Provider Mailbox Platform

Built the Master Inbox platform integrating Google Workspace Admin, Gmail API, IMAP, Microsoft Graph API, Azure AD Admin, and Microsoft 365 Admin — consolidating multi-provider mailboxes into a unified interface with AI-powered reply summarization, sentiment detection, and automated responses.

| Metric | Value |
|--------|-------|
| Providers | 6+ |
| Interface | Unified |
| Management | Multi-provider at scale |

- Google Workspace Admin & Gmail API integration
- Microsoft Graph API, Azure AD Admin, Microsoft 365 Admin
- IMAP-based unified mailbox consolidation
- AI-powered reply summarization and sentiment detection
- Automated response workflows
- Multi-provider mailbox management at scale

**Stack:** Google APIs · Microsoft Graph API · Ruby on Rails · IMAP

---

## Technical Skills

**Backend & Architecture**
- Python
- PHP / Laravel
- Ruby on Rails
- Distributed Systems Design
- High-Throughput Processing

**Messaging & Queues**
- Apache Kafka
- Distributed Queue Management

**Database**
- Microsoft SQL Server
- Stored Procedures & Views
- Query Optimization
- Indexing Strategies

**Infrastructure**
- Docker
- Linux Administration
- Server Automation
- Performance Tuning

**Email Infrastructure**
- SMTP Architecture
- Multi-ESP Orchestration
- Domain Warmup
- Inbox Placement
- SPF / DKIM / DMARC
- RBL Monitoring
- Sender Reputation Management

**Protocols & APIs**
- REST APIs / Webhooks
- IMAP / OAuth2
- Google Workspace Admin API / Gmail API
- Microsoft Graph API / Azure AD Admin / Microsoft 365 Admin

---

## Research

Conducted extensive case studies on warmup automation mechanisms across Gmail, Outlook, and Yahoo. Each provider requires a distinct approach based on domain age, sending volume, and warmup stage. Tested methods achieve consistent **70–80% engagement success rates** across providers. Actively researching provider-specific filtering logic, inbox placement signals, and behavioral detection patterns to build warmup infrastructure that stays ahead of deliverability changes.

---

## Connect

- Portfolio: [prasad.ipsnox.com](https://prasad.ipsnox.com)
- LinkedIn: [linkedin.com/in/prasad-96aba1222](https://www.linkedin.com/in/prasad-96aba1222)
- Email: anshprasad0104@gmail.com
- Project: [inboxtri.com](https://inboxtri.com)

**Available immediately.**
