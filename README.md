# event-driven-microservices
# Event-Driven Microservices — Financial Backend

High-performance backend services for consumer-facing financial applications, built for 50,000+ daily active users.

Built based on production experience at Goldman Sachs.

## What it does
- REST API layer handling real-time commerce and subscription workflows
- Event-driven communication between services via Kafka
- Low-latency data access with Redis caching layer
- Full observability with structured logging and Datadog metrics

## Tech Stack
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat&logo=postgresql&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

## Architecture
```
API Gateway → Service A (Go) ─→ Kafka ─→ Service B (Java/Spring Boot)
                  ↓                              ↓
            PostgreSQL                       Redis Cache
                  ↓                              ↓
            Datadog Metrics              Notification Service
```

## Key Features
- **Microservices** — each service independently deployable via Docker + Kubernetes
- **Schema-first design** — PostgreSQL schemas optimised for high-throughput financial transactions
- **Redis caching** — sub-millisecond reads on hot data paths
- **35% latency reduction** on notification delivery vs previous monolith architecture

## Performance
| Metric | Value |
|--------|-------|
| Daily active users | 50,000+ |
| Notification latency reduction | 35% |
| Test coverage | 85%+ |
| Post-release critical defects | 0 |
