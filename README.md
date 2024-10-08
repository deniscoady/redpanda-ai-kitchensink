# Redpanda AI Quickstart - README

This README provides an overview of the services included in the `redpanda-ai-quickstart` docker-compose setup. Each service's functionality, ports exposed, and links to web user interfaces are described for easier management.

## Table of Contents

1. [PostgreSQL](#postgresql-enterprisedb)
2. [PgAdmin 4](#pgadmin-4)
3. [Qdrant](#qdrant)
4. [Neo4j](#neo4j)
5. [Ollama](#ollama)
6. [Open WebUI](#open-webui)
7. [Redpanda](#redpanda)
8. [Redpanda Console](#redpanda-console)
9. [Port Overview](#port-overview)

---

## PostgreSQL (EnterpriseDB)

PostgreSQL is a powerful, open-source object-relational database system used for various data management applications. This deployment uses EnterpriseDB's PostgreSQL image.

- **Service**: PostgreSQL
- **Exposed Port**: `5432`
- **Login**: 
  - **Username**: `postgres`
  - **Password**: `postgres`

## PgAdmin 4

PgAdmin 4 is a web-based UI management tool for PostgreSQL databases, allowing you to easily visualize and manage PostgreSQL instances.

- **Service**: PgAdmin 4
- **Exposed Port**: `5050` (mapped from internal port 80)
- **Web UI**: [http://localhost:5050](http://localhost:5050)
- **Login Credentials**:
  - **Username**: `admin@redpanda.com`
  - **Password**: `password`

## Qdrant

Qdrant is a vector search engine optimized for AI-driven use cases, enabling search over high-dimensional vector spaces such as embeddings.

- **Service**: Qdrant
- **Exposed Port**: `6333`
- **Web UI**: [http://localhost:6333/dashboard](http://localhost:6333/dashboard)

## Neo4j

Neo4j is a graph database management system designed to store and query complex relationships between data points. It is optimal for graph-like structures.

- **Service**: Neo4j
- **Exposed Ports**: 
  - `7474` (Web Interface)
  - `7687` (Bolt Protocol for driver connections)
- **Web UI**: [http://localhost:7474](http://localhost:7474)

## Ollama

Ollama provides model inference capabilities, designed to run machine learning models efficiently. It is especially useful for AI-based workloads utilizing GPUs.

- **Service**: Ollama
- **Exposed Port**: `11434`

## Open WebUI

Open WebUI serves as a frontend interface to interact with the Ollama service, providing an easy way to manage and test AI models.

- **Service**: Open WebUI
- **Exposed Port**: `3000` (mapped from internal port 8080)
- **Web UI**: [http://localhost:3000](http://localhost:3000)

## Redpanda

Redpanda is a high-performance streaming platform that supports Kafka APIs, allowing you to build streaming architectures without the complexity of managing ZooKeeper.

- **Service**: Redpanda
- **Exposed Ports**:
  - `19092` (Kafka External)
  - `18082` (Pandaproxy External)
  - `18081` (Schema Registry External)
  - `9644` (Admin API)

## Redpanda Console

Redpanda Console provides a web-based UI for managing Redpanda clusters. You can monitor brokers, topics, partitions, and messages.

- **Service**: Redpanda Console
- **Exposed Port**: `8080`
- **Web UI**: [http://localhost:8080](http://localhost:8080)

---

## Port Overview

| Service         | Exposed Port | Service Port | Description                                 |
|-----------------|-------------|--------------|---------------------------------------------|
| PostgreSQL      | 5432        | 5432         | PostgreSQL database                         |
| PgAdmin 4       | 5050        | 80           | Web UI for PostgreSQL management            |
| Qdrant          | 6333        | 6333         | Vector search engine                        |
| Neo4j           | 7474        | 7474         | Web Interface for Neo4j                     |
| Neo4j           | 7687        | 7687         | Bolt Protocol for Neo4j connections         |
| Ollama          | 11434       | 11434        | AI model inference service                  |
| Open WebUI      | 3000        | 8080         | Web interface for AI model management       |
| Redpanda        | 9092        | 9092         | Kafka API (External)                        |
| Redpanda        | 8082        | 8082         | Pandaproxy API (External)                   |
| Redpanda        | 8081        | 8081         | Schema Registry (External)                  |
| Redpanda        | 9644        | 9644         | Admin API for Redpanda                      |
| Redpanda Console| 8080        | 8080         | Web UI for Redpanda Console                 |
