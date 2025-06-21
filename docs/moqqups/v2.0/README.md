# 🏥 Ruby on Rails Patient Management System UI Design 

This folder contains a moqqup for a full-stack Ruby on Rails project designed for the **2025 Ruby on Rails Coding Assessment** for **makerble**. It provides two main user roles — **Receptionists** and **Doctors** — with tailored interfaces for handling patient data and appointment scheduling.

---

## 🔐 Authentication

- **Login Page**
  - Route: `/login`
  - Shared login for all user roles (Receptionist, Doctor, Nurse)
  - Redirects based on role:
    - Receptionist → Patients Dashboard
    - Doctor/Nurse → Patient Dashboard with Graph + Schedule

---

## 👩‍💼 Receptionist-Only Features

### 📋 Patients Dashboard
- Route: `/patients`
- Manage all patients (CRUD)
- View a paginated table with edit/delete controls
- Embedded **Add/Edit Patient** form

### 🧾 Patient View Page *(Receptionist-Only)*
- Route: `/patients/:id/view`
- Read-only access to:
  - Recent Treatments
  - Active Prescriptions
- Access full patient details:
    - Upcoming appointments
- Can add/edit appointments.

### 🗓️ Appointment Add/Edit Form Page
> Note: This wrongly labeled as "Appointment View Page" — this was a typo.

- Used to create or modify an appointment
- Fields:
  - Scheduled datetime
  - List of doctor(s)/nurse(s) (email-based)
  - Notes
  - Option to delete participant entries or cancel appointment

---

## 👨‍⚕️ Doctor/Nurse-Only Features

### 📈 Doctor/Nurse Dashboard
- Route: `/dashboard`
- Displays:
  - **Patient Registration Graph** (last 7 days)
  - **Schedule of the Day** with appointments
    - Time
    - Patient ID
    - Assigned staff

### 📂 Patient View Page *(Doctor/Nurse-Only)*
- Route: `/patients/:id`
- Access full patient details:
  - Recent Treatments
  - Active Prescriptions
- Can add treatments, and prescriptions

---

## 📊 Feature Overview

| Feature                    | Receptionist | Doctor/Nurse |
|---------------------------|--------------|--------------|
| Patient CRUD              | ✅            | ❌            |
| Appointment Scheduling    | ✅            | ❌ (view-only)|
| Graph + Daily Schedule    | ❌            | ✅            |
| Treatment/Prescription Add| ❌ (view-only)| ✅            |
| View Patient Records      | ✅            | ✅            |

---

## 💡 Future Improvements
- Appointment filtering and search

- Role management UI (admin panel)

- Email notifications/reminders

- Treatment approval flow for doctors

---
