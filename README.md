# **AIthlete – Full-Stack Fitness Tracker with AI & Microservices**  

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)  
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)  
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)  
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)  
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)  
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white)  
![Keycloak](https://img.shields.io/badge/Keycloak-000000?style=for-the-badge&logo=keycloak&logoColor=white)  
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)  

---

## **📌 Description**  
A **full-stack fitness tracking application** with **Spring Boot microservices** and **React frontend**, powered by **Google Gemini AI** to provide **personalized health tips and recommendations**.  

This project demonstrates **microservices architecture, reactive programming, secure authentication, and AI-driven insights**.  

---

## **✨ Key Features**
- **Microservices Architecture** using **API Gateway, Eureka, and Spring Cloud Config**.  
- **Asynchronous AI Recommendations** via **RabbitMQ** for non-blocking performance.  
- **Secure Authentication & Authorization** with **OAuth2, Keycloak, PKCE, and JWT**.  
- **Inter-Service Communication** with **Spring WebFlux (WebClient)** for reactive calls.  
- **Responsive Frontend** built with **React, Vite, Redux Toolkit, and Material UI**.  
- **AI-Powered Health Tips** using **Google Gemini API**.  
- **Containerized Deployment** with **Docker** for scalability.  

---

## **🛠 Tech Stack**
- **Backend:** Java, Spring Boot, Spring Cloud (Gateway, Eureka, Config), WebFlux, RabbitMQ, PostgreSQL, MongoDB, OAuth2, Keycloak, JWT  
- **Frontend:** React, Vite, Redux Toolkit, Material UI  
- **AI Integration:** Google Gemini API  
- **Deployment:** Docker, Docker Hub  
- **Tools:** IntelliJ IDEA, VS Code, Postman, Figma  

---

## **✅ Key Highlights**
- **Reactive Microservices Communication** with Spring WebFlux.  
- **Event-Driven Architecture** powered by RabbitMQ.  
- **Secure OAuth2 PKCE Login Flow** with Keycloak.  
- **AI-Driven Recommendations** using Gemini API.  
- **Fully Containerized Setup** for seamless deployment.  

---

## **📂 Project Architecture**
```mermaid
flowchart TB
    subgraph Frontend
        A[React App (Vite, Redux Toolkit, MUI)]
    end
    
    subgraph Backend
        B[API Gateway]
        C[User Service - PostgreSQL]
        D[Activity Service - MongoDB]
        E[AI Service - Gemini API]
    end
    
    subgraph Infra
        F[(Keycloak - Auth)]
        G[(RabbitMQ - Message Broker)]
    end

    A -->|OAuth2 PKCE| F
    A -->|REST API Calls| B
    B --> C
    B --> D
    B --> E
    C -->|User Data| C
    D -->|Activity Data| D
    E -->|AI Health Tips| A
    C --> G
    D --> G
    G --> E
```

---

## **🚀 Getting Started**

### Prerequisites
- Java 17+  
- Node.js 18+  
- PostgreSQL & MongoDB  
- Docker (for containerized setup)  

### Backend Setup
```bash
# Navigate to backend service folder
cd backend
./mvnw spring-boot:run
```

### Frontend Setup
```bash
# Navigate to frontend folder
cd frontend
npm install
npm run dev
```

### Run with Docker
```bash
docker-compose up --build
```

---

## **🤝 Contributing**
Contributions are welcome! Please open an issue or submit a pull request.  

---

## **📜 License**
This project is licensed under the MIT License.
