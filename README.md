# 📌 LibroVault: Library Management System

A **desktop-based Library Management System** built using **Python (Tkinter)** and **MySQL**, designed for efficient book management with separate **Admin** and **User** roles.
This project demonstrates real-world database connectivity, GUI programming, and approval-based workflows.
📝 *This is a school project.*

---

## 📜 Features

### 👤 User Features

✅ View available (non-archived) books
✅ Request books with approval-based issuing
✅ Track:

* Due dates
* Fines
* Request status (pending / approved / rejected)

### 🛠 Admin Features

✅ Add new books
✅ Archive & restore books
✅ View complete book inventory
✅ Approve or reject user requests
✅ Automatic update of available copies

### 🗄 Database Features

✅ MySQL relational database
✅ Enforced foreign key constraints
✅ Structured tables for:

* Users
* Books
* Authors
* Categories
* Loans

---

## 🛠 Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Suhavi-k/LibraNova.git
cd librovault
```

### 2️⃣ Install Dependencies

Make sure **Python 3.10+** is installed.

```bash
pip install -r requirements.txt
```

---

## 🐳 Database Setup (Docker Recommended)

### 3️⃣ Start MySQL Server

```bash
docker-compose up -d
```

This creates:

* Database: `library_db`
* User: `libuser`
* Password: `libpassword`
* Port: `3307`

---

### 4️⃣ Initialize Database

Run **once**:

```bash
python setup.py
```

(Optional) To generate more sample data:

```bash
python seed.py
```

---

## 🚀 How to Run

```bash
python app.py
```

You will be prompted:

```
Login as (admin/user):
```

* **admin** → Admin Dashboard
* **user** → User Dashboard

⚠ *Currently, the user is hardcoded as `USER_ID = 2` for demonstration purposes.*

---

## 🧠 Book Request Workflow

1️⃣ User requests a book → status set to `pending`
2️⃣ Admin approves →

* Status becomes `approved`
* Available copies decrease
  3️⃣ Admin rejects →
* Status becomes `rejected`

---

## 🗂 Project Structure

```
.
├── admin_ui.py        # Admin dashboard (Tkinter)
├── user_ui.py         # User dashboard (Tkinter)
├── app.py             # Application entry point
├── db.py              # Database connection handler
├── schema.sql         # Database schema
├── setup.py           # Initial setup & seeding
├── seed.py            # Extended fake data seeding
├── docker-compose.yml # MySQL container config
├── requirements.txt   # Dependencies
├── README.md

```

---

## 📝 Contribution

Want to improve **LibroVault**? Contributions are welcome!

* Fork the repository
* Create a new branch
* Commit your changes
* Push to your fork
* Open a Pull Request

---

## 📧 Contact

Have questions or suggestions?

📩 **Email:** [suhavikaur30@gmail.com](mailto:suhavikaur30@gmail.com)

---

✨ *Enjoy managing your library with LibroVault!*

---
