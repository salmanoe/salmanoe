# 📝 my-todo-app

A scalable, secure microservices-based TODO application powered by Spring Boot, Kafka, and Docker Compose. This project demonstrates modern backend architecture, including service-to-service communication, centralized routing, JWT-based authentication, and tailored frontend integration through a BFF (Backend for Frontend) pattern.

---

## 📦 Architecture Overview

This system includes the following components:

| Service            | Description                                               |
|--------------------|-----------------------------------------------------------|
| `api-gateway`      | Centralized entry point using Spring Cloud Gateway        |
| `security-service` | OAuth2 Authorization Server issuing JWTs                  |
| `todo-service`     | Handles TODOs with PostgreSQL as persistence              |
| `reminder-service` | Handles reminders using MongoDB                           |
| `bff`              | Backend-for-Frontend: prepares data for UI or client use  |
| `kafka` / `zookeeper` | Used for inter-service event communication            |
| `todo-db`          | PostgreSQL container for todo data                        |
| `reminder-db`      | MongoDB container for reminder data                       |

---

## 🚀 Tech Stack

- **Java 17 + Spring Boot**
- **Spring Security + OAuth2 + JWT**
- **Spring Cloud Gateway**
- **Apache Kafka + Zookeeper**
- **PostgreSQL + MongoDB**
- **Docker Compose**
- **Maven**

---

## 🛠️ Getting Started

### 1. Requirements

- Docker + Docker Compose
- Java 17
- Maven (`mvn`)
- `.env` file (see below)

### 2. Build the services

```bash
mvn clean install -DskipTests