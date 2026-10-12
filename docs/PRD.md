# Product Requirements Document (PRD): CareSlot

## 1. Project Overview
CareSlot is a web-based clinic workflow application designed to streamline patient appointments, front-desk queue management, and digital prescriptions. 

## 2. Target Audience
* **Patients:** Need an easy way to book consultation slots.
* **Receptionists:** Need a clear dashboard to manage walk-ins and the daily queue.
* **Doctors:** Need a streamlined interface to view their daily patients and issue prescriptions.

## 3. Release Plan (Features)

### MVP Release (Mid-Term Demo)
*Focus: Core CRUD operations running locally.*
* **Appointment Booking (MVP):** Patients can view available slots and create an appointment.
* **Queue Management (MVP):** Receptionists can view a list of all daily appointments and update their status (e.g., Pending to Checked-In).
* **Basic Profiles (MVP):** Hardcoded doctor profiles to facilitate booking.

### Beta Release (Final Demo)
*Focus: Security, RBAC, and Deployment.*
* **Authentication & Authorization (Beta):** Secure JWT login with distinct User Roles (Patient, Receptionist, Doctor).
* **Security Scopes (Beta):** FastAPI dependency injection to restrict endpoint access (e.g., only doctors can issue prescriptions).
* **Digital Prescriptions (Beta):** Doctors can attach medications and diagnosis notes to completed appointments.
* **Deployment (Beta):** Frontend deployed on Vercel, Backend deployed on a cloud provider.