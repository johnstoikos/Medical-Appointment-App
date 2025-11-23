# Medical Appointment Management Web Application

## Overview
This project is a **web-based system for managing medical appointments** developed using **Java Servlets**, **JSP**, and **PostgreSQL**.  
It is designed to serve three types of users — **patients**, **doctors**, and **administrators** — each with dedicated functionality and interfaces.  

The goal was to build a realistic, secure, and user-friendly platform simulating a complete e-health appointment system.

---

## Authors
- **Anargyrou Lamprou Aikaterini** – P22009  
- **Stoikos Ioannis Panagiotis** – P22164  
- **Kotsantis Makris Vasileios** – P19082  
- **Dizou Christina** – P22039  

 *Course:* Programming for the Web and the Internet  
 *Semester:* 2024–2025  

---

## System Architecture
The system follows a **3-tier architecture**, separating concerns between presentation, business logic, and data persistence:

| Layer | Description |
|--------|--------------|
| **Presentation Layer** | JSP, HTML, CSS, Bootstrap — handles user interface and interaction. |
| **Business Logic Layer** | Java Servlets — processes user requests, applies logic, and connects UI with the database. |
| **Data Layer** | PostgreSQL — stores user accounts, doctor availability, and appointments. |

This separation ensures **maintainability, scalability, and clear role separation**.

---

## Database Design
The relational database includes the following key tables:

- **users** – stores login credentials (username, hashed password with salt, role).  
- **patients** – extends `users` with AMKA, address, and phone number.  
- **doctors** – extends `users` with specialty, office, and contact info.  
- **admins** – administrative users managing the system.  
- **availabilities** – holds doctors’ available dates and times.  
- **appointments** – stores booked appointments, linking patients and doctors.

**Foreign keys** ensure referential integrity (e.g., each patient or doctor corresponds to a valid user).  

---

## System Features

### Patient Module
Patients can:
- **Register** via an online form with full personal information.  
- **Search available appointments** filtered by doctor specialty.  
- **Book appointments**, choosing a doctor, date, time, and payment method (cash or card).  
- **View appointment history** (scheduled, completed, or canceled).  
- **Cancel appointments**, allowed only if more than 3 days before the scheduled date.  
- **View doctor profiles** with basic information (specialty, office, contact).  

---

### Doctor Module
Doctors can:
- **Declare availability** (days and times) via an intuitive form.  
- **View their schedule** filtered by day or week, including patient details and appointment status.  
- **Cancel appointments** under the same 3-day rule as patients.  
- **Access patient lists** for all their appointments, including key personal data such as AMKA.  

---

### Administrator Module
Administrators have complete control over the system:
- **Add new users** (patients, doctors, or other admins) via a detailed form.  
- **Remove doctors** who no longer provide services.  
- **Access an Admin Dashboard** that displays:
  - Number of total users, doctors, patients  
  - Active appointments  
  - System summary statistics  

This provides full **management visibility and control**.

---

## Security Features
- **Hashed & salted passwords** for secure credential storage.  
- **Session management** — sessions are created upon login and invalidated on logout.  
- **Role-based access control (RBAC)** — each user type only accesses relevant functionality.  

---

## User Interface
Built with **Bootstrap**, ensuring:
- Clean and modern design aligned with a **medical theme** (blue/white tones, consistent icons).  
- Responsive layout across all user roles.

Each role has a dedicated, intuitive menu:
- **Patients:** book, cancel, and view appointments  
- **Doctors:** manage availability and view schedules  
- **Admins:** manage users and system statistics  

---

## Lessons & Achievements
Through this project, the team:
- Designed a **normalized relational database** with consistent foreign key relationships.  
- Learned to develop dynamic web pages using **Java Servlets** and **JSP** integrated with PostgreSQL.  
- Applied **security practices** such as password hashing and session management.  
- Improved **frontend design skills** with Bootstrap for a professional look and feel.  

---

## Technologies Used
| Category | Technology |
|-----------|-------------|
| Backend | Java Servlets |
| Frontend | JSP, HTML, CSS, Bootstrap |
| Database | PostgreSQL |
| Architecture | 3-Tier |
| Security | Hashed passwords (hash + salt), session handling, RBAC |

---

## How to Run
1. Clone or download the project.  
2. Import into **Apache Tomcat** or another compatible servlet container.  
3. Set up a **PostgreSQL database** and update the connection credentials in the configuration file.  
4. Deploy and run the web application.  
5. Access via browser at `http://localhost:8080/medical-appointments`.  

---

## Conclusion
The **Medical Appointment Management System** successfully demonstrates:
- Integration of multiple technologies (Servlets, JSP, PostgreSQL, Bootstrap).  
- Implementation of real-world use cases for patients, doctors, and admins.  
- Emphasis on **security**, **usability**, and **modular architecture**.  

The final result is a **complete, practical, and extensible medical scheduling system**, aligned with real healthcare workflows.

---

## License
This project is intended for **academic and educational purposes**.
