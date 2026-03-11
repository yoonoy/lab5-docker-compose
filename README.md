# Lab 5 — Multi-container Application with Docker Compose

## Project Description

This project demonstrates a multi-container web application using Docker Compose.
The application consists of:

* **Flask API** (backend)
* **PostgreSQL** database
* **Redis** cache

All services run in separate Docker containers and communicate through a custom Docker network.

---

## Architecture

Client → Flask API → PostgreSQL
↘ Redis Cache

---

## Technologies Used

* Docker
* Docker Compose
* Python (Flask)
* PostgreSQL
* Redis

---

## Project Structure

```
lab5-docker-compose
│
├── api
│   ├── app.py
│   ├── Dockerfile
│   └── requirements.txt
│
├── docker-compose.yml
├── .env.example
├── .gitignore
└── README.md
```

---

## Setup

Clone the repository:

```
git clone https://github.com/YOUR_USERNAME/lab5-docker-compose.git
cd lab5-docker-compose
```

Create `.env` file:

```
cp .env.example .env
```

---

## Run the application

Build and start containers:

```
docker compose up --build -d
```

Check running containers:

```
docker compose ps
```

---

## API Endpoints

Health check

```
GET /health
```

Test database connection

```
GET /db-test
```

Test Redis cache

```
GET /cache-test
```

---

## Testing

Example commands:

```
curl http://localhost:5003/health
curl http://localhost:5003/db-test
curl http://localhost:5003/cache-test
```

---

## Stop containers

```
docker compose down
```

---

## Author

Aiganysh
Computer Science Student
