# Docker-compose-with-frontend-backend-and-DB
Build a basic full-stack setup using Docker Compose with: - **Frontend** (HTML/JS) - **Backend** (Python Flask) - **Database** (PostgreSQL)

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

compose-fullstack-demo/
├── backend/
│ ├── app.py
│ └── Dockerfile
├── frontend/
│ └── index.html
├── docker-compose.yml
└── README.md

Clean Up
To stop and remove containers, volumes, and networks:

bash
Copy
Edit
docker-compose down -v
🧠 Key Docker Compose Features Used
depends_on: Defines startup order (but not readiness)

Docker internal DNS: Services can communicate by name (db, backend, etc.)

Shared network: Automatically created by Docker Compose

Retry logic in Flask: Ensures database is ready before connecting
