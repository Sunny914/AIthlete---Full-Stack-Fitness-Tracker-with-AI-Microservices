# AIthlete---Full-Stack-Fitness-Tracker-with-AI-Microservices
The application is a fully featured fitness tracker where users can log their activity data. Based on this logged data, the application leverages AI to generate personalized health recommendations for the users.

📌 Description

Built a fitness tracking application using Spring Boot microservices and React, integrating AI (Google Gemini API) for personalized health recommendations.

✨ Features

✔ User Authentication – Secure login and registration with OAuth2 + Keycloak
✔ Activity Logging – Track workouts, steps, calories, and more
✔ AI-Powered Insights – Get personalized health tips using Google Gemini API
✔ Microservices Architecture – API Gateway, Service Discovery, Centralized Config
✔ Asynchronous AI Processing – Implemented via RabbitMQ for non-blocking workflows
✔ Responsive UI – Built with React, Vite, Material UI, Redux Toolkit
✔ Real-Time Communication – Powered by Spring WebFlux & WebClient

🛠 Tech Stack
Backend

Spring Boot, Spring Cloud (Gateway, Eureka, Config)

Spring Data JPA, Spring Data MongoDB

RabbitMQ, Spring AMQP

WebClient, Lombok

Frontend

React, Vite, Redux Toolkit, Material UI, Axios

Databases

PostgreSQL, MongoDB

AI Integration

Google Gemini API

Security

OAuth2, Keycloak, JWT, PKCE

Tools & DevOps

Docker, Postman, PGAdmin, MongoDB Compass

📂 Architecture

The app follows a microservices architecture with:

API Gateway for routing

Service Discovery (Eureka) for dynamic scaling

Centralized Config Server for configuration management

RabbitMQ for message-based asynchronous AI processing

🚀 Deployment

Backend: Deployed on Docker containers

Frontend: React app deployed via Netlify / Render

🔗 Links

GitHub Repository: Click Here

Live Demo: Click Here
