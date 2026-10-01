# Student Management System

A web-based **Student Management System** built using **Flask, MySQL, SQLAlchemy, and Flask-Login**. The application provides an interface for managing student records, departments, attendance, authentication, and database activity logs.

## 🚀 Features

- 🔐 User Signup & Login
- 👨‍🎓 Add Student Records
- ✏️ Edit Student Details
- 🗑️ Delete Student Records
- 🔍 Search Students by Roll Number
- 🏫 Department Management
- 📊 Attendance Management
- 📝 Student Activity Logs
- ⚡ MySQL Triggers for tracking database operations
- 🔑 Login-protected student management operations
- 🗄️ SQLAlchemy ORM for database interaction

## 🛠️ Tech Stack

**Frontend**
- HTML
- Jinja2 Templates
- CSS

**Backend**
- Python
- Flask
- Flask-SQLAlchemy
- Flask-Login

**Database**
- MySQL / MariaDB
- phpMyAdmin
- SQL Triggers

The Flask application connects to a local MySQL database through SQLAlchemy.

## 📂 Project Structure

```text
Student-Management-System/
│
├── main.py
├── requirements.txt
├── students.sql
│
├── templates/
│   ├── index.html
│   ├── login.html
│   ├── signup.html
│   ├── student.html
│   ├── studentdetails.html
│   ├── attendance.html
│   ├── search.html
│   ├── department.html
│   ├── edit.html
│   └── triggers.html
│
└── static/
    ├── css/
    ├── js/
    └── images/
```

## 🗃️ Database

The project uses a MySQL database containing tables for:

- `student`
- `department`
- `attendence`
- `user`
- `trig`
- `test`

The `student` table stores student information such as roll number, name, semester, gender, branch, email, phone number, and address.

### Database Triggers

MySQL triggers automatically record student operations:

- Student inserted
- Student updated
- Student deleted

These activities are stored in the `trig` table.

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd Student-Management-System
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

The project dependencies include Flask, Flask-SQLAlchemy, MySQL client support, Jinja2, Werkzeug and related packages.

### 4. Setup MySQL Database

Open **phpMyAdmin** or MySQL and create the database required by the application.

Import:

```text
students.sql
```

The SQL dump contains the required tables, indexes, sample records, and triggers.

### 5. Configure Database Connection

The application currently uses:

```python
mysql://root:@localhost/studentdbms
```

in `main.py`.

If your MySQL username, password, port, or database name is different, update the connection string accordingly.

### 6. Run the Application

```bash
python main.py
```

The Flask application runs in debug mode using:

```python
app.run(debug=True)
```



Then open the local address shown in the terminal, typically:

```text
http://127.0.0.1:5000/
```

## 🔑 Main Functional Routes

| Route | Purpose |
|---|---|
| `/` | Home page |
| `/login` | User login |
| `/signup` | User registration |
| `/logout` | Logout |
| `/studentdetails` | View students |
| `/addstudent` | Add a student |
| `/edit/<id>` | Edit student |
| `/delete/<id>` | Delete student |
| `/search` | Search student |
| `/addattendance` | Add attendance |
| `/department` | Manage departments |
| `/triggers` | View activity logs |
| `/test` | Test database connection |

The backend implements these routes using Flask and SQLAlchemy models.

## 🔐 Authentication

The application uses **Flask-Login** for session-based authentication. Certain operations, including adding, editing, and deleting student records, require the user to be logged in.

## 📌 Project Purpose

This project demonstrates how a full-stack student management application can connect a **Flask web application with a relational MySQL database**, while implementing CRUD operations, authentication, attendance management, and database triggers.

## 👨‍💻 Author

**Aryan Shrivastava**

B.Tech – Computer Science & Engineering

---

⭐ If you found this project useful, consider giving the repository a star!
