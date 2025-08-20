# 🧩 User Access Portal

A secure, company-aware access dashboard for enterprise applications. This portal integrates Active Directory authentication, SQL Server stored procedures, and a React frontend to deliver personalized app visibility based on a user's office location.

🔗 GitHub: [deepslate-lab/UAP](https://github.com/deepslate-lab/UAP)

---

## 🚀 Features

- 🔐 LDAP-based user authentication
- 🏢 Company-scoped app visibility using AD office field
- 🧠 SQL Server stored procedures for all mutations and queries
- 🖥️ Responsive React frontend with dynamic app grid
- 📊 Audit logging for all changes and access events
- 🛠️ Modular Express backend with clean route separation

---

## 🧱 Tech Stack

| Layer       | Technology               |
|-------------|--------------------------|
| Frontend    | React + TypeScript + Vite |
| Backend     | Node.js + Express         |
| Auth        | LDAP via `ldapjs`         |
| Database    | SQL Server + Stored Procedures |
| Styling     | Tailwind CSS              |

---

🧾 Database Setup
Run all migration files in /migrations against your SQL Server instance. These include:

Table creation (Apps, Companies, AuditLogs)

Stored procedures (sp_AddCompany, sp_GetUserApps, etc.)

Indexes and audit cleanup routines

Use SSMS or a migration runner to apply them in order.

🧠 Architecture Notes
App visibility is scoped by the user's physicalDeliveryOfficeName (AD office field)

All backend mutations are routed through stored procedures for auditability

Frontend uses context providers for apps and auth state

Audit logs include IP, user identity, and before/after snapshots
