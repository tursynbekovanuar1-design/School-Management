# 🏫 School Management System

> **Final Project for Design Patterns Course**  
> **Astana IT University — 2026**

---

## 👥 Project Team

* **Anuar Tursynbekov** (Developer 1)
* **Zhanaiym Sadyk** (Developer 2)

---

## 📌 Project Overview

The **School Management System** is an educational management platform built with **Java 17+**. It demonstrates the practical implementation of **6 Gang of Four (GoF) Design Patterns**, strictly following **SOLID principles** and **Clean Code guidelines**.

The system handles user profile creation, dynamic role allocation, academic performance evaluations (GPA calculations), and real-time automated grade updates.

---

## 🛠️ Architecture & Pattern Distribution

The project is divided equally between two developers (3 design patterns each), all orchestrated seamlessly via a central **Facade**:

| Developer | Pattern Name | Pattern Type | Responsibilities & Package |
| :--- | :--- | :--- | :--- |
| **Anuar Tursynbekov** | **Factory Method** | Creational | Instantiates user profiles (`Student`, `Teacher`, `Admin`) without tight coupling. (`school.profile`) |
| **Anuar Tursynbekov** | **Decorator** | Structural | Dynamically appends extra roles/permissions (`HeadTeacher`, `ClubLeader`) to users. (`school.role`) |
| **Anuar Tursynbekov** | **Builder** | Creational | Assembles complex student/teacher personal records (`PersonCard`). (`school.card`) |
| **Zhanaiym Sadyk** | **Observer** | Behavioral | Dispatches automated notifications to students/parents upon grade entries. (`school.notification`) |
| **Zhanaiym Sadyk** | **Strategy** | Behavioral | Encapsulates dynamic GPA computation algorithms (`Standard`, `Weighted`, `Pass/Fail`). (`school.gpa`) |
| **Zhanaiym Sadyk** | **Facade** | Structural | Provides a unified API interface (`SchoolManagementFacade`) linking all subsystems. (`school.facade`) |

---

## 📂 Repository Structure

```text
src/main/java/school/
├── card/          # Builder Pattern (Anuar Tursynbekov)
├── common/        # Enums & System Constants (Permissions, UserTypes)
├── facade/        # Facade Pattern (Zhanaiym Sadyk)
├── gpa/           # Strategy Pattern (Zhanaiym Sadyk)
├── grade/         # GradeBook & System Logics
├── notification/  # Observer Pattern (Zhanaiym Sadyk)
├── profile/       # Factory Method Pattern (Anuar Tursynbekov)
├── role/          # Decorator Pattern (Anuar Tursynbekov)
└── Main.java      # Application Main Entry Point & Scenario Verification
