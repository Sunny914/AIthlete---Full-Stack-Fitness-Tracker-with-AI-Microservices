# **Full-Stack Fitness Tracker with AI & Microservices**  

**Description:**  
Built a **fitness tracking application** using **Spring Boot microservices** and **React**, integrating **Google Gemini AI** for personalized health recommendations.  

---

## **✨ Key Features**
- **Microservices Architecture** with **API Gateway**, **Eureka Service Discovery**, and **Spring Cloud Config**  
- **Asynchronous AI Processing** via **RabbitMQ** for non-blocking recommendation generation  
- **Secure Authentication** using **OAuth2 + Keycloak** with **PKCE flow** and **JWT tokens**  
- **User Service** with **PostgreSQL** and **Activity Service** with **MongoDB**  
- **React Frontend** (Vite, Redux Toolkit, Material UI) integrated via **Axios** and secured with **OAuth2 PKCE**  

---

## **🛠 Tech Stack**
- **Backend:** Spring Boot, Spring Cloud (Gateway, Eureka, Config), Spring Data JPA, Spring Data MongoDB, RabbitMQ, WebClient  
- **Frontend:** React, Vite, Redux Toolkit, Material UI, Axios  
- **Databases:** PostgreSQL, MongoDB  
- **Security:** OAuth2, Keycloak, JWT, PKCE  
- **AI:** Google Gemini API  
- **Tools:** IntelliJ IDEA, VS Code, Postman, Docker, PGAdmin, MongoDB Compass  

---

sequenceDiagram
    participant User
    participant Frontend
    participant Keycloak
    participant API Gateway
    participant Services

    User->>Frontend: Login Request
    Frontend->>Keycloak: OAuth2 PKCE Authorization
    Keycloak->>Frontend: Authorization Code
    Frontend->>Keycloak: Exchange Code for Token
    Keycloak->>Frontend: Access + Refresh Token
    Frontend->>API Gateway: API Request with JWT
    API Gateway->>Services: Validate Token & Forward Request
    Services->>API Gateway: Response
    API Gateway->>Frontend: Return Data

    ---

## **🏗️ Architecture**

### **1. High-Level Architecture**
```mermaid
flowchart TD
    A[React Frontend] -->|Axios + OAuth2 PKCE| B[API Gateway]
    B -->|Service Discovery| C[Eureka Server]
    B --> D[User Service (PostgreSQL)]
    B --> E[Activity Service (MongoDB)]
    E -->|Publish Activity Data| F[RabbitMQ]
    F -->|Consume Data| G[AI Service (Google Gemini API)]
    G -->|Send Recommendations| D
