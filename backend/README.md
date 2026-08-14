# Kinetic Backend (Spring Boot)

## What it is
A Spring Boot Java REST API backend for the Kinetic Workout Tracker, serving user authentication and exercise/workout logging.

## What it does
* **Secure Auth Controller**: Exposes login and registration endpoints using JWT (JSON Web Tokens) to secure resource endpoints.
* **Workout Tracker Schema**: Exposes endpoints to CRUD workouts, individual exercises, and workout-exercise associations.
* **Performance Reporting**: Aggregates exercise log data to produce workout summaries and reports.
* **Database Persistency**: Integrates with PostgreSQL (Neon.tech pooler by default) to store and manage active entities.

## How to execute it
### Prerequisites
* Java Development Kit (JDK) 17 or higher.
* Maven (wrapper included in folder).

### Steps
1. **Configure Environment Variables**:
   Create a `.env` file in the root `backend` directory:
   ```env
   CORS_ALLOWED_ORIGINS=http://localhost:5173
   DB_URL=jdbc:postgresql://<neon_db_host>/kinetic?sslmode=require
   DB_USERNAME=your_db_user
   DB_PASSWORD=your_db_password
   JWT_SECRET=your_base64_jwt_secret_key
   JWT_EXPIRATION=86400000
   ```

2. **Run Application**:
   Navigate to the backend directory and execute:
   ```bash
   ./mvnw spring-boot:run
   ```
   The backend API service will listen on `http://localhost:8080`.

### REST API Endpoints
* **Authentication**: `/api/v1/auth/signup`, `/api/v1/auth/login`
* **Workouts**: `/api/v1/workouts` (CRUD)
* **Exercises**: `/api/v1/exercises` (CRUD)
* **Workout Exercise Link**: `/api/v1/workout-exercises`
* **Reports**: `/api/v1/reports`
