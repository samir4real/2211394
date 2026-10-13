# Software Requirements Specification (SRS): CareSlot

## 1. Functional Requirements

### MVP Release
* **REQ-MVP-01:** The system shall allow users to retrieve a list of available doctors and their time slots via a REST API.
* **REQ-MVP-02:** The system shall allow the creation of an appointment record containing patient details, doctor ID, and date.
* **REQ-MVP-03:** The system shall allow receptionists to fetch all appointments for the current day.
* **REQ-MVP-04:** The system shall allow updating the status of an appointment.

### Beta Release
* **REQ-BETA-01:** The system shall require user authentication to access protected routes.
* **REQ-BETA-02:** The system shall enforce Role-Based Access Control (RBAC) ensuring patients cannot access the receptionist queue dashboard.
* **REQ-BETA-03:** The system shall allow doctors to create a prescription record linked to a specific appointment ID.

## 2. Non-Functional Requirements
* **Tech Stack:** React + TypeScript (Frontend), FastAPI + Python (Backend).
* **Performance:** API endpoints should respond in under 300ms locally.
* **Security (Beta):** Passwords must be hashed using bcrypt before database insertion.