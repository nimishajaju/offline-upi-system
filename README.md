# Bluetooth-Based Offline UPI Payment Simulation System

A backend-focused Spring Boot project that simulates offline UPI transactions using Bluetooth-style device-to-device communication. The project demonstrates secure transaction handling, encryption, duplicate transaction prevention, and replay attack protection without requiring internet connectivity.

---

# Features

- Offline UPI payment transaction simulation
- Bluetooth-style device-to-device communication flow
- Secure transaction transfer using RSA + AES hybrid encryption
- Duplicate transaction prevention using idempotency logic
- Replay attack protection using TTL (Time-To-Live) validation
- RESTful APIs for payment and account operations
- MySQL database integration using Spring Data JPA and Hibernate
- Embedded Apache Tomcat server
- Layered backend architecture

---

# Security Challenges Solved

## 1. Secure Transaction Transfer

Sensitive data like UPI PIN and account details should not be exposed during offline communication.

### Solution
- Implemented RSA-based key exchange
- Used AES encryption for secure packet transfer
- Applied hybrid encryption for better security and performance

---

## 2. Duplicate Transaction Prevention

The same payment request should not be processed multiple times.

### Solution
- Implemented idempotency handling
- Used unique transaction identifiers
- Prevented repeated transaction execution

---

## 3. Replay Attack Protection

Old transaction packets should not be reusable after a certain time.

### Solution
- Implemented TTL (Time-To-Live) validation
- Expired old transaction packets automatically
- Prevented replay attacks using timestamp validation

---

# Tech Stack

- Java 17
- Spring Boot
- Spring Data JPA
- Hibernate
- MySQL
- Maven
- REST APIs
- Embedded Apache Tomcat

---
