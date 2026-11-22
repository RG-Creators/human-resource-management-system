# Human Resource Management System (HRMS) & Workforce Operations Suite

[![PHP Version](https://img.shields.io/badge/PHP-8.2%2B-777bb4?style=for-the-badge&logo=php&logoColor=white)](https://php.net)
[![REST API](https://img.shields.io/badge/REST-API-0052CC?style=for-the-badge&logo=postman&logoColor=white)](https://postman.com)
[![MySQL](https://img.shields.io/badge/MySQL-8.0%2B-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://mysql.com)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

An agile, lightweight Human Resource Management System (HRMS) and Workforce Operations REST API engine. Features role-based access control, attendance clock-in/out, leave application approval workflows, payroll ledger calculation, and multi-department announcement broadcasting.

---

## 🏗️ System Architecture

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

## ⚡ Key Capabilities

- **RESTful Resource Routing**: Single entrypoint dispatcher (`backend/api.php`) handling `GET`, `POST`, `PUT`, `DELETE` operations on workforce entities.
- **Role-Based Access Control**: Strict segregation between `admin` privileges (salary disbursement, leave approvals) and `employee` self-service portals.
- **Attendance & Geolocation Clocking**: Timestamped attendance logging with work duration calculation and audit reports.
- **Leave Lifecycle Management**: Multi-state leave workflow (`pending`, `approved`, `rejected`) with employee balance deductions.
- **Automated Database Seeder**: Transaction-wrapped seeder script (`seed.php`) populating demo organizations, staff rosters, and historical payroll.

---

## 🛠️ Tech Stack

- **Backend**: Core PHP 8.2+ (PDO Singleton, JSON REST API, Password Hashing)
- **Frontend**: Responsive HTML5, Modern CSS Grid & Flexbox, Asynchronous JavaScript (Fetch API)
- **Database**: MySQL 8.0+ / MariaDB

---

## 🚀 Getting Started

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/RG-Creators/human-resource-management-system.git
   cd human-resource-management-system
   ```

2. **Database Setup**:
   - Create a MySQL database named `hrms_db` or import the schema.
   - Run `backend/seed.php` to populate default roles, mock staff members, and attendance fixtures.

3. **Launch Local Server**:
   - Serve using Apache/WAMP or built-in PHP server:
     ```bash
     php -S localhost:8000
     ```
   - Access the Admin Portal or Employee Dashboard from `frontend/index.html`.

---

## 📄 License
This project is open-source under the [MIT License](LICENSE).
