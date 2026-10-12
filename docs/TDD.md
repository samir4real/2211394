# Technical Design Document (TDD): CareSlot

## 1. System Architecture
The project utilizes a decoupled architecture:
* **Frontend:** React with TypeScript, built using Vite. Communicates with the backend via RESTful HTTP requests.
* **Backend:** FastAPI (Python) serving JSON responses.
* **Database:** SQLite (MVP) transitioning to PostgreSQL (Beta) using an ORM like SQLAlchemy.

## 2. Database Schema (Entities)
* **Users:** `id`, `name`, `email`, `password_hash`, `role`
* **Appointments:** `id`, `patient_id`, `doctor_id`, `date`, `status`
* **Prescriptions (Beta):** `id`, `appointment_id`, `diagnosis`, `medications`

## 3. API Endpoints Design

### MVP Endpoints (No Auth Required)
* `GET /api/v1/doctors` - Retrieve available doctors.
* `POST /api/v1/appointments` - Create a new appointment.
* `GET /api/v1/appointments/today` - Retrieve today's queue.
* `PATCH /api/v1/appointments/{id}/status` - Update appointment status.

### Beta Endpoints (Auth & Scopes Required)
* `POST /api/v1/auth/login` - Authenticate and return JWT.
* `POST /api/v1/prescriptions` - Create a prescription (Scope: `prescriptions:write`).
* `GET /api/v1/prescriptions/me` - Get logged-in user's prescriptions (Scope: `prescriptions:read_own`).