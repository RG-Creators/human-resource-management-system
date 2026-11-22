# Human Resource Management System (HRMS) & Workforce Operations Suite

[![PHP Version](https://img.shields.io/badge/PHP-8.2%2B-777bb4?style=for-the-badge&logo=php&logoColor=white)](https://php.net)

> [!IMPORTANT]
> **Commercial Intellectual Property Notice & Source Code Sale:**
> This repository contains a production-ready, proprietary software solution engineered by **Ronit Goswami (RG Creators)**. It is available for commercial acquisition, full IP buyout, or custom enterprise licensing.
> 
> - **Asset Classification:** Enterprise HRMS & Payroll
> - **Commercial Valuation / Fair Market Estimate:** **₹50,000 – ₹80,000 INR** *(Full Source Code & Commercial Rights)*
> - **Full IP Buyout & Exclusive Ownership:** **₹1,10,000 INR**
> - **Target Industry:** Corporate HR, Enterprise Workforce Operations, Payroll & Talent Management
> - **Handover Deliverables:**
>   - Complete HRMS backend REST API source code and SPA portal interfaces
>   - Employee lifecycle management (onboarding, departments, designations, exit interviews)
>   - Leave management engine with approval hierarchies and accrual rules
>   - Comprehensive salary ledger, payslip generation, and attendance calculation models
>   - Postman API test collections, database schemas, and seed data
>   - 30 days of dedicated technical handover and integration support
> - **Official Portfolio:** [https://rgcreators.netlify.app](https://rgcreators.netlify.app)
> - **Acquisition & Licensing Inquiries:** [rgcreatorsofficial@gmail.com](mailto:rgcreatorsofficial@gmail.com)

---

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


---

## 🚀 Future Roadmap & Next-Gen Implementation Ideas (Ready for Expansion)

The following extensive architectural and feature expansions have been designed and architected for rapid implementation, transforming this solution into a high-capacity, enterprise-grade platform:

1. **Statutory Indian Payroll Compliance Engine:** Automated calculation of PF, ESI, Professional Tax, TDS tax regimes, and Form 16 generator.
2. **Biometric Attendance Push Listener:** Direct TCP/IP and API listener for ZKTeco, Essl, and Realtime biometric punch machines.
3. **Geofenced Mobile Punch with Anti-Spoof Liveness:** GPS radius verification combined with AI facial liveness detection for remote and field staff.
4. **360-Degree Performance Appraisal & OKR Suite:** Quarterly appraisal cycles, manager/peer review scoring, and KPI achievement heatmaps.
5. **AI Resume Parsing & ATS (Applicant Tracking System):** Automated candidate CV parsing, skill keyword scoring, and interview scheduling pipeline.
6. **Digital Employee Onboarding with Aadhaar e-Sign:** Paperless document verification with DigiLocker and automated digital contract signing.
7. **Employee Self-Service (ESS) Mobile App:** Native Flutter mobile app for instant leave applications, expense claims, and payslip downloads.
8. **Automated Shift Scheduling & Overtime Validation:** Dynamic rotational shift planner with automatic overtime pay approval workflows.
9. **Enterprise Asset Lifecycle & IT Equipment Tracking:** Hardware allocation logging, warranty status, maintenance tickets, and return audits.
10. **Predictive Employee Attrition & Sentiment Analytics:** Machine learning models forecasting flight risk based on leave patterns and review sentiments.

---

## 💼 Commercial Acquisition & Licensing Agreement

For source code inspection, live technical walkthrough, pricing negotiations, or exclusive enterprise buyout:
- **Lead Architect & Developer:** Ronit Goswami (RG Creators)
- **Primary Contact Email:** [rgcreatorsofficial@gmail.com](mailto:rgcreatorsofficial@gmail.com)
- **Official Portfolio:** [https://rgcreators.netlify.app](https://rgcreators.netlify.app)
- **Location:** Kolkata, West Bengal, India
