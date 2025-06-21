# 🏥 Ruby on Rails Patient Management System UI Design — v3.0

This folder contains a moqqup for a full-stack Ruby on Rails project designed for the **2025 Ruby on Rails Coding Assessment** for **makerble**. It introduces a structured, role-based architecture, clearer file separation, and refined user experiences for **Receptionists**, **Doctors**, and **Nurses**.

---

## 🗂️ A Bit of an Overview

Here's a sneak peek for easy access:

<details>
  <summary>🔐 Login Page</summary>

  ![Login Page](./Login_Page.png)

</details>

---

<details>
  <summary>👨‍⚕️ Doctor/Nurse Dashboard</summary>

  ![Doctor Dashboard](./Doctor/Doctor_dashboard_page.png)

</details>

<details>
  <summary>🩺 Doctor/Nurse Patient View Page</summary>

  ![Doctor/Nurse Patient View](./Doctor/Patient_View_page_for_doctorsnurses.png)

</details>

<details>
  <summary>💊 Prescription Add Page</summary>

  ![Prescription Add Page](./Doctor/Prescription_Add_page.png)

</details>

<details>
  <summary>💉 Treatment Add Page</summary>

  ![Treatment Add Page](./Doctor/Treatment_Add_page.png)

</details>

---

<details>
  <summary>👩‍💼 Receptionist Patient View Page</summary>

  ![Receptionist Patient View](./Receptionist/Patient_View_page_for_receptionists.png)

</details>

<details>
  <summary>👩‍💼 Receptionist Dashboard</summary>

  ![Receptionist Dashboard](./Receptionist/Patients_dashboard_page.png)

</details>

<details>
  <summary>👩‍💼 Receptionist Dashboard (With Patient Add Feature Version)</summary>

  ![Receptionist Dashboard (With Patient Add Feature Version)](./Receptionist/Patients_dashboard_page_1.png)

</details>

<details>
  <summary>🗓️ Appointment Add/Edit Form Page</summary>

  ![Appointment Add/Edit Form Page](./Receptionist/Appointment_AddEdit_page.png)

</details>

---

## 📁 Directory Structure

```bash

v3.0/
├── Login\_Page.png
├── doctor/
│   ├── Doctor\_dashboard\_page.png
│   ├── Patient\_View\_page\_for\_doctorsnurses.png
│   ├── Prescription\_Add\_page.png
│   └── Treatment\_Add\_page.png
└── receptionist/
├── Appointment\_AddEdit\_page.png
├── Patient\_View\_page\_for\_receptionists.png
├── Patients\_dashboard\_page.png
└── Patients\_dashboard\_page\_1.png

```

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

## ✅ What’s New in v3.0

* 🔁 Organized directory structure (`doctor/`, `receptionist/`)
* 🧑‍🤝‍🧑 Finalised unified UI for doctors and nurses
* 🗃 Modular form pages for appointments, prescriptions, and treatments
* 🧼 Cleaner, professional UI per role

---

## 🧩 Suggested Enhancements

* Export patient data to CSV/PDF
* Notification system for upcoming appointments
* Add filtering/search to patient dashboard

---
