# AI-Powered Expense Tracker

![license](https://img.shields.io/badge/license-MIT-green)
![status](https://img.shields.io/badge/status-Completed-brightgreen)

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Setup and Installation](#setup-and-installation)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Screenshots](#screenshots)
- [License](#license)

---

## Introduction

The **AI-powered Expense Tracker** is a full-stack web application that allows users to log their expenses and receive **AI-generated financial insights**. This project demonstrates the use of **Django** for the backend, **React + MUI** for the frontend, and **NGINX** for load balancing. It also leverages **Docker** to make deployment and scaling seamless.

This project was built as a **test project** to showcase skills in full-stack development, system design, API creation, and deployment strategies.

---

## Features

- **Expense Management**: Add, update, and delete expenses.
- **AI Insights**: Receive insights about your spending patterns (e.g., overspending alerts).
- **Django Backend**: Handles CRUD operations and API endpoints.
- **React Frontend with MUI**: A user-friendly and responsive interface.
- **NGINX Load Balancing**: Distributes requests across multiple backend instances.
- **Dockerized Deployment**: Backend, frontend, and NGINX services managed through Docker Compose.

---

## Technologies Used

- **Frontend**: React, Material-UI (MUI)
- **Backend**: Django, Django REST Framework, PostgreSQL
- **Load Balancer**: NGINX
- **Containerization**: Docker, Docker Compose

---

## Project Structure

```
ExpenseTracker/
├── backend/
│   ├── Dockerfile
│   ├── start_instances.sh
│   ├── manage.py
│   ├── requirements.txt
│   ├── expense_tracker/
│   │   └── settings.py, urls.py, wsgi.py, etc.
│   ├── expenses/
│       └── models.py, serializers.py, views.py, urls.py
├── frontend/
│   ├── Dockerfile
│   ├── public/
│   │   └── index.html
│   ├── src/
│       └── App.js, components/, styles.css
├── nginx/
│   └── nginx.conf
└── docker-compose.yml
```

---

## Setup and Installation

### Prerequisites

Ensure you have the following installed on your machine:
- **Docker** and **Docker Compose**  
- **Python 3.9+** (for backend development)  
- **Node.js 14+ / Yarn** (for frontend development)

### Backend Setup

1. Navigate to the `backend/` folder:
   ```bash
   cd backend
   ```

2. Create a virtual environment and install dependencies:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

3. Apply migrations:
   ```bash
   python manage.py migrate
   ```

### Frontend Setup

1. Navigate to the `frontend/` folder:
   ```bash
   cd frontend
   ```

2. Install frontend dependencies:
   ```bash
   yarn install
   ```

3. (Optional) Run the frontend locally:
   ```bash
   yarn start
   ```

---

## Running the Application

1. **Build and run all services using Docker Compose**:
   ```bash
   docker-compose up --build
   ```

2. **Access the frontend** at:  
   [http://localhost](http://localhost)

3. **API Endpoints** are load-balanced across Django instances on ports **8001** and **8002** via NGINX.

---

## API Endpoints

- **GET /api/expenses/**: Retrieve all expenses.
- **POST /api/expenses/**: Create a new expense.
- **PUT /api/expenses/{id}/**: Update an expense.
- **DELETE /api/expenses/{id}/**: Delete an expense.
- **GET /api/insights/**: Retrieve AI-generated spending insights.

Example Response from **GET /api/insights/**:

```json
{
  "insights": [
    "You're overspending this month!",
    "You logged a high-value expense.",
    "You're tracking expenses diligently."
  ]
}
```

---

## Screenshots

### 1. Dashboard with Expenses and AI Insights

![Dashboard Screenshot](https://via.placeholder.com/800x400?text=Dashboard)

---

## License

This project is licensed under the **MIT License**.

---

## Conclusion

This **AI-powered Expense Tracker** project demonstrates my ability to build and deploy full-stack applications with modern tools and technologies. The setup shows my understanding of **scalable system design**, API development, and deployment with **NGINX and Docker**. I look forward to discussing this project further and sharing how it aligns with the role I’m applying for.

---
