# Docker-compose-with-frontend-backend-and-DB
Build a basic full-stack Dockerized environment using MySQL, Python Flask backend, and NGINX frontend.

# 🚀 Full-Stack App with Docker Compose (Frontend + Backend + MySQL)

This is a simple full-stack application using **Docker Compose**, demonstrating how different services (frontend, backend, database) can communicate over a shared Docker network.

---

## 📦 Stack Overview

| Component | Tech Used      | Description                             |
|-----------|----------------|-----------------------------------------|
| Frontend  | NGINX + HTML   | Static site served by NGINX             |
| Backend   | Flask (Python) | REST API with DB connectivity check     |
| Database  | MySQL 5.7      | Stores sample data                      |

---

## 🗂️ Project Structure
.
├── backend/
│   ├── app.py
│   ├── Dockerfile
│   ├── requirements.txt
│   └── wait-for-db.sh
├── frontend/
│   ├── index.html
│   └── submit.html
├── docker-compose.yml
└── README.md

1. Prerequisites
Docker installed (https://docs.docker.com/get-docker/)
Docker Compose installed (https://docs.docker.com/compose/install/)

2. Build and start services
docker-compose up --build

3. Access the application
Frontend (form): http://localhost:8080
Backend API (Flask): http://localhost:5000

Clean Up
To stop and remove containers, volumes, and networks:
docker-compose down -v

Features
User-friendly HTML form to submit names.
Data persistence with MySQL container using volumes.
Backend built with Python Flask handling form submission and database insertion.
Frontend served by NGINX for static content.
Health checks and service dependencies to improve container startup order.
