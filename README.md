# Python_Django_Projects
# 🧑‍💼 Employee Management System

A web-based application built with **Django** and **Django REST Framework** to manage employees, departments, leaves, and attendance. This system allows full **CRUD** operations and uses **MySQL** for backend data storage. The frontend is created using **HTML, CSS, and Bootstrap**.

---

## 🔧 Technologies Used

- **Frontend**: HTML, CSS, Bootstrap  
- **Backend**: Django, Django REST Framework  
- **Database**: MySQL  
- **Architecture**: MTV (Model-Template-View)

---

## 📁 Modules

### 1. EmployeeInfo
- Add, view, edit, and delete employee records.
- Fields: Name, Email, Phone, Department, Joining Date.

### 2. Department
- Manage departments with fields: Name, Head, Location.

### 3. Leave
- Employees can apply for leave (status: Pending by default).
- Leave cannot be edited after applying but can be deleted.

### 4. Attendance
- Mark daily attendance.
- Options to replace attendance with leave or delete entry.

---

## 📦 Features

- Full CRUD for all modules.
- REST API integrated with HTML templates.
- Bootstrap-based responsive user interface.
- Form validation and error handling using `try-except`.

---

## 🗃️ Database Models

Each module has its own model:
- **Employee**: `id`, `name`, `email`, `phone`, `department`, `joining_date`
- **Department**: `id`, `name`, `head`, `location`
- **Leave**: `id`, `employee_name`, `leave_type`, `start_date`, `end_date`, `reason`, `status`
- **Attendance**: `id`, `employee_name`, `date`, `status`

---

## 🚀 How to Run the Project

```bash
# Clone the repository
git clone https://github.com/yourusername/employee-management-system.git
cd employee-management-system

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Configure MySQL settings in settings.py

# Apply migrations
python manage.py makemigrations
python manage.py migrate

# Run the server
python manage.py runserver
