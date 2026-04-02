# ⚙️ Centralized Configuration - Spring Boot Config Server Project

> 🚀 A centralized configuration management system using Spring Cloud Config Server for microservices.

---

## 📖 Introduction

This project demonstrates how to implement **Centralized Configuration** using **Spring Cloud Config Server** in a Spring Boot microservices architecture.

In microservices, managing configurations separately for each service becomes difficult. This project solves that by:

* Storing all configurations in a central repository (GitHub)
* Providing configurations dynamically to multiple services
* Reducing duplication and improving maintainability

---

## 🧠 Concepts Used

### 🔹 Spring Cloud Config Server

Config Server acts as a central place where all configuration files are stored and managed.

### 🔹 External Configuration

Configuration is stored outside the application (in GitHub), making it easy to update without modifying code.

### 🔹 Client-Server Architecture

* Config Server → Provides configurations
* Microservices → Fetch configurations at runtime

---

## 💡 Example Flow

1. Config Server connects to GitHub repository
2. Configuration files are stored (e.g., `user-service.properties`)
3. Microservices request configuration from Config Server
4. Config Server returns required configuration

Example:

* URL → `http://localhost:8888/user-service/default`
* Returns configuration for user-service

---

## 🌍 Real-Life Analogy

Think of a company:

* Head Office = Config Server
* Branches = Microservices
* Rule Book = GitHub Config Repo

Instead of each branch maintaining its own rules,
all rules are controlled from the head office.

---

## 📂 Project Structure

```id="h2ks91"
Central-config-SpringBoot/
│
├── config-server/
│   └── (Spring Cloud Config Server)
│
├── config-repo/ (GitHub Repository)
│   ├── application.properties
│   ├── user-service.properties
│   ├── order-service.properties
│
└── README.md
```

---

## ⚙️ How to Run the Project

### Step 1: Create GitHub Config Repository

Add files like:

* application.properties
* user-service.properties
* order-service.properties

---

### Step 2: Configure Config Server

In `application.properties`:

```properties id="q1k2l3"
server.port=8888
spring.cloud.config.server.git.uri=https://github.com/your-username/config-repo
```

---

### Step 3: Enable Config Server

Add annotation in main class:

```java id="l9s8d7"
@EnableConfigServer
```

---

### Step 4: Run Config Server

Start application on port `8888`

---

### Step 5: Test Configuration

Open in browser:

http://localhost:8888/user-service/default

---

## 🔀 Configuration Flow

* GitHub Repo → Config Server → Microservices

---

## 🚀 Advantages

* Centralized configuration management
* Easy to update configurations
* No need to redeploy services for config changes
* Better consistency across services
* Scalable and maintainable system

---

## 🛠️ Applications

* Microservices architecture
* Cloud-native applications
* Enterprise systems
* DevOps configuration management
* Distributed systems

---

## 🧰 Technologies Used

* Java
* Spring Boot
* Spring Cloud Config Server
* GitHub
* Maven

---

## 🧑‍💻 Author

**Vishal**
Computer Engineering Student

---
