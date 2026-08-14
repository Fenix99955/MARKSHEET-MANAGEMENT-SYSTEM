Here is a clean, comprehensive **README.md** file tailored for your **Marksheet Management System** project.

---

# Marksheet Management System

A desktop application built using Python's **Tkinter** for the GUI and **MySQL** for backend database management. The application provides a complete role-based workflow allowing users to sign up, log in, manage student records, update academic subject marks, and view generated student marksheets.

---

## Features

* **User Authentication:**
* **Sign Up:** Register new admin/user accounts with duplicate ID prevention.
* **Log In:** Secure credential verification against the MySQL database.


* **Student Data Management:**
* **Add Student Records:** Capture personal details (Name, Father's Name, Mother's Name, D.O.B, Class, Stream, and Admission ID).
* **Stream Customization:** Supports stream-specific subject configurations for Class XI and XII (**Science** & **Humanities**).


* **Data Editing & Updating:**
* Fetch existing student records using their **Admission ID** and update subject-wise marks dynamically.


* **Marksheet Generation:**
* Retrieve and display formatted student marksheets using the Admission ID.



---

## Tech Stack

* **GUI Framework:** Python Tkinter (`tkinter`, `ttk`, `messagebox`)
* **Database:** MySQL
* **Database Connector:** `mysql-connector-python`

---

## Database Prerequisites

To run this project, you need a local MySQL server setup. Execute the following SQL script to set up the `email` database and required tables:

```sql
CREATE DATABASE IF NOT EXISTS `email`;
USE `email`;

-- User authentication table
CREATE TABLE IF NOT EXISTS `user` (
    `id` VARCHAR(100) NOT NULL PRIMARY KEY,
    `pas` VARCHAR(100) NOT NULL
);

-- Student marksheet data table
CREATE TABLE IF NOT EXISTS `data` (
    `admissionid` INT NOT NULL PRIMARY KEY,
    `name` VARCHAR(100),
    `fathername` VARCHAR(100),
    `mothername` VARCHAR(100),
    `class` VARCHAR(10),
    `sec` VARCHAR(50),
    `dob` VARCHAR(50),
    `sub1` VARCHAR(50),
    `sub2` VARCHAR(50),
    `sub3` VARCHAR(50),
    `sub4` VARCHAR(50),
    `sub5` VARCHAR(50),
    `sub6` VARCHAR(50),
    `sub7` VARCHAR(50),
    `sub8` VARCHAR(50)
);

```

> **Note:** Update the database connection credentials (`host`, `user`, `password`) in the script if your local MySQL settings differ from `host="localhost"`, `user="root"`, `password="root"`.

---

## Project Setup & Installation

1. **Clone the Repository:**
```bash
git clone https://github.com/your-username/marksheet-management-system.git
cd marksheet-management-system

```


2. **Install Required Packages:**
Ensure Python 3.x is installed, then install the MySQL connector:
```bash
pip install mysql-connector-python

```


3. **Configure Database Connection:**
Ensure your MySQL server is running and updated with the database schema provided above.
4. **Run the Application:**
```bash
python main.py

```



---

## Application Structure & Flow

```text
├── Main Screen (Login / Signup Options)
│   ├── Signup Page (Register new admin user)
│   └── Login Page (Authenticate credentials)
│       └── Mainframe Dashboard
│           ├── Enter Student Data (Add info + input stream marks)
│           ├── Edit Student Data (Fetch & update existing marks by Admission ID)
│           └── Get Marksheet (View completed student marksheet)

```

---

## Suggested Code Improvements (Refactoring Tips)

If you plan to improve or scale this application, consider the following best practices:

1. **Parameterized SQL Queries:** Use SQL parameterization (e.g., `WHERE admissionid = %s`) consistently across all queries to prevent **SQL Injection** vulnerabilities.
2. **Window Management:** Instead of instantiating multiple root `Tk()` windows inside sub-functions (which can cause memory leaks or UI glitches), use `Toplevel()` windows or frame-switching techniques within a single `Tk()` instance.
3. **Database Centralization:** Centralize database connection parameters into a configuration file or a dedicated helper module rather than re-establishing connections inside each inner function.
4. **Layout Flexibility:** Replace fixed pixel coordinate placing (`.place()`) with responsive layout managers (`.pack()` or `.grid()`) to ensure smooth rendering across different display resolutions.
