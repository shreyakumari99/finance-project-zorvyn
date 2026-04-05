# 💰 Finance Tracker Backend

![Django](https://img.shields.io/badge/Django-Backend-green)
![DRF](https://img.shields.io/badge/DRF-API-red)
![SQLite](https://img.shields.io/badge/Database-SQLite-blue)
![Docker](https://img.shields.io/badge/Docker-Supported-2496ED)
![License](https://img.shields.io/badge/License-MIT-yellow)

A Django REST API for tracking personal finances, including income, expenses, analytics, and role-based access control.

---

## 📑 Table of Contents

* [🚀 Quick Start (Docker)](#-quick-start-docker)
* [⚙️ Manual Setup](#️-manual-setup)
* [🧪 Sample Data](#-sample-data)
* [▶️ Running the Server](#️-running-the-server)
* [🌐 API Endpoints](#-api-endpoints)
* [📬 API Examples](#-api-examples)
* [✨ Features](#-features)
* [🧠 Design Decisions](#-design-decisions)
* [📦 Future Improvements](#-future-improvements)

---

## 🚀 Quick Start (Docker)

Run the project instantly:

```bash
docker build -t finance-backend .
docker run -p 8000:8000 finance-backend
```

---

## ⚙️ Manual Setup

### 1. Create Virtual Environment

```bash
python -m venv venv
```

Activate:

* Linux/macOS:

```bash
source venv/bin/activate
```

* Windows:

```bash
venv\Scripts\activate
```

---

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 3. Apply Migrations

```bash
python manage.py migrate
```

---

### 4. Create Superuser (Optional)

```bash
python manage.py createsuperuser
```

---

## 🧪 Sample Data

Load prebuilt data for testing:

```bash
python manage.py loaddata seed_data.json
```

---

## ▶️ Running the Server

```bash
python manage.py runserver
```

---

## 🌐 API Endpoints

| Endpoint             | Method   | Description                 |
| -------------------- | -------- | --------------------------- |
| `/admin/`            | GET      | Admin panel                 |
| `/api/transactions/` | GET/POST | List or create transactions |
| `/api/analytics/`    | GET      | Financial summary           |

---

## 📬 API Examples

### ➤ Create Transaction

**POST** `/api/transactions/`

```json
{
  "title": "Salary",
  "amount": 5000,
  "category": "Income"
}
```

---

### ➤ Get Transactions

**GET** `/api/transactions/`

Optional filtering:

```
/api/transactions/?category=Salary
```

---

### ➤ Analytics Response

**GET** `/api/analytics/`

```json
{
  "total_income": 10000,
  "total_expenses": 4000,
  "net_balance": 6000
}
```
## 🚀 How to Use the API?

    Run Server: python manage.py runserver

    Admin Panel: http://127.0.0.1:8000/admin/ (Use this to add/edit users and transactions).

    Transactions List: http://127.0.0.1:8000/api/transactions/

    Finance Summary: http://127.0.0.1:8000/api/analytics/
---

## ✨ Features

### ✅ Validation

* Prevents zero or negative transactions

### 🔍 Filtering

* Query-based filtering via URL parameters

### 🔐 Permissions

* **Admin:** Full CRUD access
* **Viewer/Analyst:** Read-only access

### 📊 Analytics

* Real-time calculations:

  * Income
  * Expenses
  * Balance

---

## 🧠 Design Decisions

### 📦 SQLite

* Zero configuration
* Lightweight and portable

### 🔗 Django REST Framework

* Clean API structure
* Easy frontend integration

### 🛡️ Security

* Backend validation ensures:

  * Data integrity
  * Protection from invalid requests

---

## 📦 Future Improvements

* 🔑 JWT Authentication
* 🐘 PostgreSQL support
* 📱 Frontend integration (React / Flutter)
* 📊 Advanced analytics (charts, trends)
* ☁️ Deployment (AWS / Docker Compose)

---

## 🤝 Contributing

Pull requests are welcome! Feel free to fork and improve.

---

## 📄 License

This project is licensed under the MIT License.

---


