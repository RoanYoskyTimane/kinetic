# Kinetic - Workout Tracker App

## What it is
Kinetic is a full-stack workout tracking and reporting web application composed of a Java Spring Boot REST API backend and a React + TypeScript + Vite frontend configured for Cloudflare deployments.

## What it does
* **User Authentication**: Secure user register/login dashboards backed by Spring Security and JSON Web Tokens (JWT).
* **Workout Management**: Log workout sessions, record active dates, and monitor exercise completion.
* **Exercise Catalog**: Create, view, and assign exercise entries (reps, sets, equipment details) to workouts.
* **Workout Exercises Mapping**: Customize links between exercises and workouts, updating specific routines.
* **Progress Reports**: Retrieve and compute analytics data mapping workouts over time.

## How to execute it
To run Kinetic, you will need to start both the Spring Boot API backend and the React web client.

### 1. Execute the Backend (Spring Boot)
Go to the `backend` directory and run:
```bash
cd backend
./mvnw spring-boot:run
```
The backend API server will launch and listen on `http://localhost:8080` (or as configured in `.env`).

For detailed backend configuration, database setup, and credentials, see the [backend documentation](file:///home/roan-yosky-timane/Projects/kinetic/backend/README.md).

### 2. Execute the Frontend (React + Vite)
Go to the `frontend` directory, install dependencies, and run:
```bash
cd frontend
npm install
npm run dev
```
The client app will launch and open on `http://localhost:5173`.

For detailed frontend client variables and Cloudflare Wrangler deployment commands, see the [frontend documentation](file:///home/roan-yosky-timane/Projects/kinetic/frontend/README.md).
