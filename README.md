# Distributed Job Queue System

A scalable distributed task queue system inspired by BullMQ and Sidekiq architectures.

## Features

- Priority-based job scheduling
- Delayed job execution
- Retry mechanism with exponential backoff
- Dead-letter queue for failed jobs
- Concurrent worker processing
- Horizontal scalability support
- Real-time monitoring dashboard
- Redis-backed distributed queue system

---

## Architecture

The system consists of multiple microservices:

- **user-service** → creates and submits jobs
- **order-server** → processes order-related tasks
- **mail-server** → handles email/background jobs

Redis acts as the central queue broker for distributed task processing.

---

## Tech Stack

- Node.js
- Express.js
- Redis
- BullMQ
- Docker

---

## Project Structure

```bash
mail-server/
order-server/
user-service/
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/Harshraj1703/Distributed-job-queue.git
```

Install dependencies inside each service:

```bash
npm install
```

---

## Running the Project

Start Redis server first.

Then run services individually:

```bash
node app.js
```

Or using nodemon:

```bash
npm run dev
```

---

## Future Improvements

- Kubernetes deployment
- Prometheus + Grafana monitoring
- WebSocket live logs
- Authentication & authorization
- CI/CD pipeline with GitHub Actions

---

## Learning Outcomes

This project helped in understanding:

- Distributed systems architecture
- Background job processing
- Worker concurrency
- Fault tolerance
- Retry strategies
- Queue management with Redis
- Scalable backend design
