# 🏥 Ruby on Rails Patient Management System UI Design — v3.0

This folder contains a moqqup for a full-stack Ruby on Rails project designed for the **2025 Ruby on Rails Coding Assessment** for **makerble**. It introduces a structured, role-based architecture, clearer file separation, and refined user experiences for **Receptionists**, **Doctors**, and **Nurses**.

---

## 🗂️ A Bit of an Overview

Here's a sneak peek for easy access:

<details>
  <summary>🔐 Login Page - click toggle to open</summary>

  ![Login Page](./Login_Page.png)

</details>

### Doctors and nurses only

<details>
  <summary>👨‍⚕️ Doctor/Nurse Dashboard - click toggle to open</summary>

  ![Doctor Dashboard](./Doctor/Doctor_dashboard_page.png)

</details>

<details>
  <summary>🩺 Doctor/Nurse Patient View Page - click toggle to open</summary>

  ![Doctor/Nurse Patient View](./Doctor/Patient_View_page_for_doctorsnurses.png)

</details>

<details>
  <summary>💊 Prescription Add Page - click toggle to open</summary>

  ![Prescription Add Page](./Doctor/Prescription_Add_page.png)

</details>

<details>
  <summary>💉 Treatment Add Page - click toggle to open</summary>

  ![Treatment Add Page](./Doctor/Treatment_Add_page.png)

</details>

### Receptionits only

<details>
  <summary>👩‍💼 Receptionist Patient View Page - click toggle to open</summary>

  ![Receptionist Patient View](./Receptionist/Patient_View_page_for_receptionists.png)

</details>

<details>
  <summary>👩‍💼 Receptionist Dashboard - click toggle to open</summary>

  ![Receptionist Dashboard](./Receptionist/Patients_dashboard_page.png)

</details>

<details>
  <summary>👩‍💼 Receptionist Dashboard (With Patient Add Feature Version) - click toggle to open</summary>

  ![Receptionist Dashboard (With Patient Add Feature Version)](./Receptionist/Patients_dashboard_page_1.png)

</details>

<details>
  <summary>🗓️ Appointment Add/Edit Form Page - click toggle to open</summary>

  ![Appointment Add/Edit Form Page](./Receptionist/Appointment_AddEdit_page.png)

</details>

---

## 📁 Directory Structure

```bash

v3.0/
├── Login_Page.png
├── doctor/
│   ├─- Doctor_dashboard_page.png
│   ├── Patient_View_page_for_doctorsnurses.png
│   ├── Prescription_Add_page.png
│   └── Treatment_Add_page.png
├── receptionist/
│   ├── Appointment_AddEdit_page.png
│   ├── Patient_View_page_for_receptionists.png
│   ├── Patients_dashboard_page.png
│   └── Patients_dashboard_page_1.png
└── user_flow_diagram.png
```

---

## User flow diagram

![User flow diagram](./user_flow_diagram.png)

---

## 🔐 Authentication

- **Login Page**
  - Location: `/v3.0/Login_Page.png`
  - Single sign-in form for all roles
  - Redirects based on role:
    - Receptionist → Patients Dashboard
    - Doctor/Nurse → Dashboard with graph + schedule

---

## 👩‍💼 Receptionist UI

### 🧾 Patients Dashboard
- Files: `Patients_dashboard_page.png`, `Patients_dashboard_page_1.png`
- Features:
  - View and manage patients
  - Pagination
  - Add/Edit/Delete patients

### 👁️ Patient View Page
- File: `Patient_View_page_for_receptionists.png`
- Accessible only to receptionists
- Features:
  - Upcoming Appointments
  - Recent Treatments
  - Active Prescriptions
- Can view
  - Appointments
  - Prescriptions
  - Treatments
- Can add/edit:
  - Appointments

### 🗓️ Appointment Add/Edit Page
- File: `Appointment_AddEdit_page.png`
- Form to:
  - Add/edit appointment datetime
  - Assign/Unassign doctors/nurses via email
  - Add notes
  - Cancel appointments

---

## 🧑‍⚕️ Doctor/Nurse UI

> **Doctors and Nurses share the same UI.**

### 📈 Dashboard
- File: `Doctor_dashboard_page.png`
- Components:
  - **Patient Registration Graph** (week view)
  - **Schedule of the Day** showing patient appointments and assigned staff

### 🧍 Patient View Page
- File: `Patient_View_page_for_doctorsnurses.png`
- Features:
  - Recent Treatments
  - Active Prescriptions
- Can view
  - Prescriptions
  - Treatments
- Can add:
  - Prescriptions
  - Treatments
- Can disactivate:
  - Prescriptions
- Cannot do anything else

### 💊 Add Prescription Page
- File: `Prescription_Add_page.png`
- Fields:
  - Prescription name, frequency, renewal limit
  - Notes

### 💉 Add Treatment Page
- File: `Treatment_Add_page.png`
- Fields:
  - Treatment name
  - Administering doctor(s)/nurse(s)
  - Date/time given
  - Follow-up time
  - Notes

---

## 🧭 User Role Routing Flow

```text
Login →
  ├── Receptionist
  │   ├── Patients Dashboard
  │   ├── Patient Detail View
  │   ├── Add/Edit Appointment
  │   └── Add/Edit Treatment & Prescription
  └── Doctor/Nurse
      ├── Dashboard (Graph + Daily Schedule)
      ├── Read-only Patient View
      ├── Add Treatment
      └── Add Prescription
````

---

## 📊 Feature Comparison

| Feature                         | Receptionist | Doctor/Nurse |
| ------------------------------- | ------------ | ------------ |
| View all patients               | ✅            | ❌            |
| Add/edit patient info           | ✅            | ❌            |
| Add/edit appointments           | ✅            | ❌            |
| View schedule and stats         | ❌            | ✅            |
| Add treatments & prescriptions  | ❌            | ✅            |
| View patient records            | ✅            | ✅            |

---

## ✅ What’s New in v4.0

* 🗃 User flow diagram is now here !!!

---

## 🧩 Suggested Enhancements

* Export patient data to CSV/PDF
* Notification system for upcoming appointments
* Add filtering/search to patient dashboard

---
