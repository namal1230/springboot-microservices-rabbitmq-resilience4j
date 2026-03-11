---

# 🚀 Spring Boot Microservices Architecture

A **Spring Boot Microservices project** demonstrating a modern distributed system using messaging, resilience patterns, distributed tracing, and CI/CD automation.

This project showcases how to build **scalable and fault-tolerant microservices** using the Spring Cloud ecosystem.

---

# 📌 Features

* 🔹 Microservices architecture with multiple services
* 🔹 Asynchronous communication using RabbitMQ
* 🔹 Distributed tracing with Zipkin
* 🔹 Service resilience using Resilience4j
* 🔹 Circuit Breaker implementation using Circuit Breaker Pattern
* 🔹 Configuration refresh with Spring Cloud Bus
* 🔹 Containerized services using Docker
* 🔹 Automated build and deployment with GitLab CI/CD

---

# 🏗️ Architecture

The system follows a **distributed microservices architecture** where services communicate through **REST APIs and asynchronous messaging**.

## Components

* API Gateway
* Service Registry (Eureka)
* Config Server
* **Employee Service**
* **Department Service**
* Notification Service
* Messaging Queue
* Monitoring and Tracing Tools

---

# 🛠️ Tech Stack

| Technology   | Purpose                             |
| ------------ | ----------------------------------- |
| Spring Boot  | Backend microservices               |
| Spring Cloud | Microservices ecosystem             |
| RabbitMQ     | Event-driven communication          |
| Zipkin       | Request tracing                     |
| Resilience4j | Fault tolerance                     |
| Docker       | Containerization                    |
| GitLab CI/CD | Continuous Integration & Deployment |

---

# 📦 Messaging with RabbitMQ

Services communicate **asynchronously through RabbitMQ queues**.

### Example Flow

```
Employee Service → RabbitMQ Queue → Notification Service
```

---

# 📊 Distributed Tracing

Using **Zipkin**, we can trace requests across multiple microservices.

### Example Request Flow

```
API Gateway → Employee Service → Department Service → Database
```
### 🔗 Repository Links
# GitLab Repository
```
https://gitlab.com/namal1230/cicd-pipeline-integrate.git
```
### 🚀 Getting Started
# 1️⃣ Clone the Repository
```
git clone https://gitlab.com/namal1230/cicd-pipeline-integrate.git
```

# 📷 System Diagram

```
[ Client ]
     |
     v
[ API Gateway ]
     |
 -------------------------
 |                       |
 v                       v
Employee Service     Department Service
        |
        v
      RabbitMQ
