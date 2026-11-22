# Hackathon Workforce Suite & HRMS REST API

[![PHP Version](https://img.shields.io/badge/PHP-8.2%2B-777bb4?style=for-the-badge&logo=php&logoColor=white)](https://php.net)
[![REST API](https://img.shields.io/badge/REST-API-0052CC?style=for-the-badge&logo=postman&logoColor=white)](https://postman.com)
[![MySQL](https://img.shields.io/badge/MySQL-8.0%2B-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://mysql.com)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

An agile, lightweight Human Resource Management System (HRMS) and Workforce Operations REST API engineered during a competitive hackathon virtual round. Features role-based access control, attendance clock-in/out, leave application approval workflows, payroll ledger calculation, and multi-tenant announcement broadcasting.

---

## ?? System Architecture

```
+-------------------------------------------------------------------------+
|                              FRONTEND TIER                              |
|   - Admin Control Suite (employees, attendance, leaves, payroll, news)  |
|   - Employee Self-Service (dashboard, attendance clock, leave status)   |
|   - Vanilla JS Fetch API Gateway (`frontend/js/api.js`)                 |
+------------------------------------|------------------------------------+
                                     v JSON HTTP REST
+-------------------------------------------------------------------------+
|                             API ROUTER TIER                             |
|   - Universal Route Dispatcher (`backend/api.php`)                      |
|   - Session & RBAC Middleware (`backend/auth.php`)                      |
|   - Singleton PDO Connection Pool (`backend/db.php`)                    |
+------------------------------------|------------------------------------+
                                     v
+-------------------------------------------------------------------------+
|                             DATABASE TIER                               |
|   - Relational MySQL Schema (employees, attendance, leaves, payroll)    |
|   - Seeder & Transaction Fixtures (`backend/seed.php`)                  |
+-------------------------------------------------------------------------+
```

---

## ? Key Capabilities

- **RESTful Resource Routing**: Single entrypoint dispatcher (`backend/api.php`) handling `GET`, `POST`, `PUT`, `DELETE` operations on workforce entities.
- **Role-Based Access Control**: Strict segregation between `admin` privileges (salary disbursement, leave approvals) and `employee` self-service portals.
- **Attendance & Geolocation Clocking**: Timestamped attendance logging with work duration calculation and audit reports.
- **Leave Lifecycle Management**: Multi-state leave workflow (`pending`, `approved`, `rejected`) with employee balance deductions.
- **Automated Database Seeder**: Transaction-wrapped seeder script (`seed.php`) populating demo organizations, staff rosters, and historical payroll.

---

## ?? Tech Stack

- **Backend**: Core PHP 8.2+ (PDO Singleton, JSON REST API, Password Hashing)
- **Frontend**: Responsive HTML5, Modern CSS Grid & Flexbox, Asynchronous JavaScript (Fetch API)
- **Database**: MySQL 8.0+ / MariaDB

---

## ?? Getting Started

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/RG-Creators/hackathon-workforce-suite.git
   cd hackathon-workforce-suite
   ```

2. **Database Setup**:
   - Create database `human_resource`:
     ```sql
     CREATE DATABASE human_resource CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
     ```
   - Seed database using the CLI:
     ```bash
     php backend/seed.php
     ```

3. **Run Application**:
   ```bash
   php -S localhost:8000
   ```
   - Access Login: `http://localhost:8000/frontend/login.html`
   - Default Admin: `admin@hrms.com` / `admin123`
   - Default Employee: `john.doe@company.com` / `password123`

---

## ?? License
This repository is licensed under the [MIT License](LICENSE).
