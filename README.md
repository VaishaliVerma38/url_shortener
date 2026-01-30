# url_shortener
This project is a URL Shortener Service built using Laravel (10/11/12).   The system supports multi-company architecture, role-based access control and restricted URL visibility rules as defined in the assignment.

 Features Overview

### 👥 Company & Users
- The system supports **multiple companies**
- Each company can have **multiple users**
- Users belong to exactly **one company**

### 🔐 Roles & Permissions
Supported roles:
- **SuperAdmin**
- **Admin**
- **Member**
- **Sales**
- **Manager**

Role-based restrictions:
- **SuperAdmin**
  - Created via **Database Seeder (raw SQL)**
  - Cannot create short URLs
  - Cannot view all short URLs across companies
  - Cannot invite Admins to a new company

- **Admin**
  - Cannot create short URLs
  - Can only view short URLs **not created in their own company**
  - Cannot invite Admins or Members in their own company

- **Member**
  - Cannot create short URLs
  - Can only view short URLs **not created by themselves**

---

## 🔗 URL Shortener Rules
- Short URLs are **NOT publicly accessible**
- Short URLs **resolve and redirect** only when accessed through authorized flow
- URL visibility strictly follows role-based rules

---

## 🧪 Tests Covered
- Admin and Member cannot create short URLs
- SuperAdmin cannot create short URLs
- Admin can only view URLs not created in their own company
- Member can only view URLs not created by themselves
- Short URLs redirect correctly and are not publicly resolvable

---

## 🛠️ Tech Stack

- **Framework:** Laravel 10 / 11 / 12
- **Language:** PHP 8+
- **Database:** MySQL / SQLite
- **Authentication:** Laravel Auth / Sanctum / Jetstream
- **ORM:** Eloquent
- **Testing:** Laravel Feature & Unit Tests

---

## 🚀 Local Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/url-shortener.git
cd url-shortener
