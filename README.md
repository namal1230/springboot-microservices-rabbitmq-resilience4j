🚀 Spring Boot Microservices Architecture

A Spring Boot Microservices project demonstrating a modern distributed system using messaging, resilience patterns, distributed tracing, and CI/CD automation.

This project showcases how to build scalable and fault-tolerant microservices using the Spring Cloud ecosystem.

📌 Features

🔹 Microservices architecture with multiple services

🔹 Asynchronous communication using RabbitMQ

🔹 Distributed tracing with Zipkin

🔹 Service resilience using Resilience4j

🔹 Circuit Breaker implementation using Circuit Breaker Pattern

🔹 Configuration refresh with Spring Cloud Bus

🔹 Containerized services using Docker

🔹 Automated build and deployment with GitLab CI/CD

🏗️ Architecture

The system follows a distributed microservices architecture where services communicate through REST APIs and asynchronous messaging.

Components

API Gateway

Service Registry (Eureka)

Config Server

Order Service

Product Service

Notification Service

Messaging Queue

Monitoring and Tracing Tools

🛠️ Tech Stack
Technology	Purpose
Spring Boot	Backend microservices
Spring Cloud	Microservices ecosystem
RabbitMQ	Event-driven communication
Zipkin	Request tracing
Resilience4j	Fault tolerance
Docker	Containerization
GitLab CI/CD	Continuous Integration & Deployment
⚙️ CI/CD Pipeline

The project includes an automated CI/CD pipeline implemented using GitLab.

Pipeline stages:

1️⃣ Build
2️⃣ Test
3️⃣ Package
4️⃣ Docker Image Build
5️⃣ Deploy

Example .gitlab-ci.yml stages:

stages:
  - build
  - test
  - docker
  - deploy

The pipeline automatically:

Builds the Spring Boot services

Runs tests

Builds Docker images

Deploys services

📦 Messaging with RabbitMQ

Services communicate asynchronously through RabbitMQ queues.

Example flow:

Order Service → RabbitMQ Queue → Notification Service

Benefits:

Loose coupling

Better scalability

Reliable message delivery

🛡️ Fault Tolerance

The system uses Resilience4j to prevent cascading failures.

Implemented patterns:

Circuit Breaker

Retry

Rate Limiter

Timeout handling

Example:

@CircuitBreaker(name = "productService", fallbackMethod = "fallbackMethod")
📊 Distributed Tracing

Using Zipkin, we can trace requests across multiple microservices.

Example request flow:

API Gateway → Order Service → Product Service → Database

Zipkin visualizes request latency and service dependencies.

🔗 Repository Links
GitLab Repository
https://gitlab.com/namal1230/cicd-pipeline-integrate.git
🚀 Getting Started
1️⃣ Clone the Repository
git clone https://gitlab.com/namal1230/cicd-pipeline-integrate.git
2️⃣ Start Infrastructure

Run Docker containers:

docker-compose up

This will start:

RabbitMQ

Zipkin

Microservices

3️⃣ Run Services

Start each Spring Boot service:

mvn spring-boot:run
📷 System Diagram

You can add an architecture diagram here.

[ Client ]
     |
     v
[ API Gateway ]
     |
 -------------------------
 |           |           |
 v           v           v
Order     Product     Notification
Service    Service       Service
     |
     v
   RabbitMQ
📚 Learning Purpose

This project demonstrates:

Event-driven microservices

Resilience patterns

Distributed tracing

DevOps CI/CD practices

👨‍💻 Author

Namal Dilmith

Software Engineering Student | Java Developer | Microservices Enthusiast
