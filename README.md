# Hi there, I'm Abakar Aliev 👋
### Backend & Cloud-Native Engineer | Go • Python • Kubernetes

[![LinkedIn](https://img.shields.io/badge/LinkedIn-abakar--ai--golang-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abakar-ai-golang)
[![Telegram](https://img.shields.io/badge/Telegram-@aliev__abakar-2CA5E0?style=flat-square&logo=telegram&logoColor=white)](https://t.me/aliev_abakar)
[![Email](https://img.shields.io/badge/Email-salachali@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:salachali@gmail.com)

<details>
<summary><b>🇷🇺 Нажмите, чтобы прочитать на русском языке / Click to view Russian version</b></summary>
<br>

###  Обо мне

Backend-разработчик с фундаментальным бэкграундом в инжиниринге и прикладной математике (**6 лет в гидродинамическом и математическом моделировании пластовых систем**).

Специализируюсь на проектировании **высоконадежных распределенных систем и REST/WebSocket API на Go 1.23+**, а также интеграции **прикладных AI/LLM-контуров и асинхронных пайплайнов на Python 3.12+**.

-  **Фокус разработки**: высокопроизводительные сетевые сервисы, конкурентность (`sync`, каналы, детекция гонок `-race`), транзакционная целостность (`pgx/v5`) и архитектура Zero-Trust.
-  **Безопасность и надежность**: строгая изоляция тенантов (защита от IDOR), криптография Argon2id, Refresh Token Rotation (RTR) с Replay Attack Killswitch и защита от DoS (`MaxBytesReader`).
-  **Cloud-Native**: развертывание и управление сервисами в Kubernetes (**k3s**), автоматизация CI/CD (Gitea Actions, GitHub Actions), multi-stage Docker сборка и мониторинг в Prometheus.

---

###  Стек технологий и инструменты

```
  ┌───────────────┬─────────────────────────────────────────────────────────────┐
  │ Backend       │ Go (1.23+), Python (3.12+), Chi, Gin, FastAPI, Pydantic v2  │
  │ Databases     │ PostgreSQL, MariaDB, Redis, pgvector, golang-migrate        │
  │ Messaging     │ Apache Kafka, RabbitMQ                                      │
  │ AI / ML       │ RAG Pipelines, Vector Search, OpenAI / Gemini API, SSE      │
  │ Cloud & Infra │ Docker, Kubernetes (k3s), Ingress-Nginx, Linux, systemd     │
  │ Observability │ Prometheus, Grafana, k6 load testing                        │
  │ Frontend      │ Vue 3, Composition API, Pinia, TypeScript, Tailwind CSS     │
  └───────────────┴─────────────────────────────────────────────────────────────┘
```

---

###  Флагманский архитектурный проект

###  [**crm-ai**](https://github.com/adexcell/crm-ai) — Production-Ready B2B SaaS CRM Monorepo
> Масштабируемое серверное ядро мультитенантной CRM-системы на Go 1.23 со строгими инвариантами безопасности и Cloud-Native деплоем.

- **Мультитенантность и защита от IDOR**: гарантированная изоляция данных организаций на уровне схемы БД, транзакций и репозиториев (`WHERE organization_id = $1`).
- **Zero-Trust аутентификация и сессии**:
  - Хеширование паролей **Argon2id** (защита от GPU-брутфорса и timing attacks).
  - Ротация токенов (RTR) с хранением SHA-256 хешей в PostgreSQL.
  - **Replay Attack Killswitch**: мгновенный отзыв всех сессий пользователя при повторе токена.
  - Защита от гонок при рефреше: **15-секундный Grace Period**, подтвержденный стресс-тестами (`go test -race`).
- **Безопасность и устойчивость**: потоковый JSON-декодер с `http.MaxBytesReader` (1 МБ) для защиты от DoS; анти-переборный сброс паролей через атомарный Redis `GETDEL`.
- **Инфраструктура и CI/CD**: контейнеризация с multi-stage Docker сборкой, проверка линтером `golangci-lint` и pre-commit хуками, развертывание в локальный кластер **k3s** с Ingress-Nginx и Graceful Shutdown по сигналу `SIGTERM`.

**Стек**: `Go 1.23` • `Chi` • `pgx/v5 (pgxpool)` • `Redis` • `PostgreSQL` • `Argon2id` • `Docker` • `k3s` • `Gitea Actions CI/CD` • `Vue 3`

---

###  Коммерческий опыт (NDA / Закрытые репозитории)

- **Travel SaaS Platform** (Go, Chi, PostgreSQL, Redis, pgvector, SSE streaming): 40+ таблиц, RAG семантический поиск, платежные шлюзы (ЮKassa, Альфа-Банк).
- **Сервис управления регистрами 1С** (Go, MariaDB, Generics & Reflection): универсальный слой доступа к данным, снизивший дублирование кода на 40%.
- **High-Load движок генерации документов** (Python, FastAPI, ProcessPoolExecutor, `img2pdf` в памяти): ускорение сборки PDF в 3.5 раза без нагрузки на диск.
- **Оптимизация распределенной системы** (Go, Apache Kafka): микробатчинг сообщений, устранивший задержки доставки при пиковом потоке.

</details>

---

###  About Me

Backend engineer with a solid background in engineering and applied mathematics (**6 years in petroleum reservoir engineering & mathematical modeling**). 

I specialize in building **high-reliability distributed systems and REST/WebSocket APIs on Go 1.23+**, combined with **AI/LLM pipelines and automations on Python 3.12+**.

-  **Core Focus**: High-performance network programming, concurrency (`sync`, channels, `-race`), transactional integrity (`pgx/v5`), and Zero-Trust architecture.
-  **AppSec & Reliability**: Multi-tenancy with strict IDOR isolation, Argon2id cryptography, Refresh Token Rotation (RTR) with Replay Attack Killswitch, and DoS mitigation (`MaxBytesReader`).
-  **Cloud-Native**: Deploying and managing services in Kubernetes (**k3s**) with automated CI/CD pipelines (Gitea Actions, GitHub Actions), multi-stage Docker builds, and Prometheus observability.

---

###  Tech Stack & Tooling

```
  ┌───────────────┬─────────────────────────────────────────────────────────────┐
  │ Backend       │ Go (1.23+), Python (3.12+), Chi, Gin, FastAPI, Pydantic v2  │
  │ Databases     │ PostgreSQL, MariaDB, Redis, pgvector, golang-migrate        │
  │ Messaging     │ Apache Kafka, RabbitMQ                                      │
  │ AI / ML       │ RAG Pipelines, Vector Search, OpenAI / Gemini API, SSE      │
  │ Cloud & Infra │ Docker, Kubernetes (k3s), Ingress-Nginx, Linux, systemd     │
  │ Observability │ Prometheus, Grafana, k6 load testing                        │
  │ Frontend      │ Vue 3, Composition API, Pinia, TypeScript, Tailwind CSS     │
  └───────────────┴─────────────────────────────────────────────────────────────┘
```

#### Badges
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)

---

###  Flagship Architecture Showcase

###  [**crm-ai**](https://github.com/adexcell/crm-ai) — Production-Ready B2B SaaS CRM Monorepo
> Scalable, multi-tenant B2B SaaS CRM system core built from scratch with Go 1.23, strict security invariants, and Cloud-Native deployment.

- **Multi-tenancy & IDOR Defense**: Organization-scoped isolation across database schemas, transactions, and repository queries (`WHERE organization_id = $1`).
- **Zero-Trust Auth & Sessions**:
  - Secure password hashing with **Argon2id** (protection against GPU-bruteforce and timing attacks).
  - Refresh Token Rotation (RTR) with SHA-256 token hashing in PostgreSQL.
  - **Replay Attack Killswitch**: immediate revocation of all user sessions upon token re-use detection.
  - Concurrency-safe token refresh: **15-second Grace Period** verified under high-concurrency race testing (`go test -race`).
- **AppSec & Resilience**: Streaming JSON decoder with `http.MaxBytesReader` (1 MB) for DoS mitigation; anti-enumeration password reset via atomic Redis `GETDEL`.
- **Infrastructure & CI/CD**: Containerized with multi-stage Docker builds, verified via `golangci-lint` and pre-commit hooks, deployed into a local **k3s** cluster with Ingress-Nginx and Graceful Shutdown on `SIGTERM`.

**Tech Stack**: `Go 1.23` • `Chi` • `pgx/v5 (pgxpool)` • `Redis` • `PostgreSQL` • `Argon2id` • `Docker` • `k3s` • `Gitea Actions CI/CD` • `Vue 3`

---

###  Commercial & Domain Experience (Proprietary / NDA)

- **Travel SaaS Platform** (Go, Chi, PostgreSQL, Redis, pgvector, SSE streaming): 40+ tables, RAG semantic search, payment gateways (YooKassa, Alfa-Bank).
- **1C Registry Management Service** (Go, MariaDB, Generics & Reflection): universal data access layer reducing boilerplate code by 40%.
- **High-Load PDF Document Engine** (Python, FastAPI, ProcessPoolExecutor, in-memory `img2pdf`): 3.5x throughput optimization without disk I/O bottlenecks.
- **Distributed System Optimization** (Go, Apache Kafka): micro-batching implementation eliminating delivery lag during traffic spikes.

---

###  Get in Touch

- **LinkedIn**: [linkedin.com/in/abakar-ai-golang](https://www.linkedin.com/in/abakar-ai-golang)
- **Telegram**: [@aliev_abakar](https://t.me/aliev_abakar)
- **Email**: [salachali@gmail.com](mailto:salachali@gmail.com)
