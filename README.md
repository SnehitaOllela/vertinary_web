# vertinary_web
# 🐾 OVAS – Online Veterinary Appointment System

## 📌 Project Overview

**OVAS (Online Veterinary Appointment System)** is a web-based application developed using **PHP and MySQL** to simplify the process of booking and managing veterinary appointments.

The system allows pet owners to view available veterinary services, submit appointment requests, and contact the veterinary center online. An administrator can manage appointments, services, categories, users, and customer inquiries through a dedicated admin panel.

---

## 🎯 Objectives

The main objectives of the Online Veterinary Appointment System are:

* To provide an easy online platform for veterinary appointment booking.
* To reduce manual appointment management.
* To allow pet owners to submit their pet and owner details online.
* To help administrators manage appointment requests efficiently.
* To manage veterinary services and service categories.
* To maintain customer inquiries and appointment records.
* To provide an organized admin dashboard for managing the system.

---

## ✨ Features

### 👤 User Side

* Home page
* About Us
* Veterinary services
* Service categories
* Online appointment booking
* Pet information submission
* Owner information submission
* Appointment schedule selection
* Contact/Inquiry form
* Appointment confirmation/status

### 🔐 Admin Side

* Secure admin login
* Admin dashboard
* Appointment management
* View appointment details
* Update appointment status
* Service management
* Add, edit and delete services
* Category management
* User management
* Customer inquiry management
* System information/settings
* Appointment calendar

---

## 🛠️ Technologies Used

| Technology   | Purpose                       |
| ------------ | ----------------------------- |
| PHP          | Backend development           |
| MySQL        | Database management           |
| HTML5        | Web page structure            |
| CSS3         | Styling                       |
| JavaScript   | Client-side functionality     |
| jQuery       | Dynamic web functionality     |
| Bootstrap    | Responsive UI                 |
| AdminLTE     | Admin dashboard               |
| FullCalendar | Appointment calendar          |
| Font Awesome | Icons                         |
| Apache       | Web server                    |
| XAMPP        | Local development environment |

---

## 📂 Project Structure

```text
OVAS/
│
├── admin/
│   ├── appointments/
│   ├── categories/
│   ├── inquiries/
│   ├── services/
│   ├── system_info/
│   ├── user/
│   ├── home.php
│   ├── index.php
│   └── login.php
│
├── classes/
│   ├── DBConnection.php
│   ├── Login.php
│   ├── Master.php
│   ├── SystemSettings.php
│   └── Users.php
│
├── database/
│   └── ovas_db.sql
│
├── inc/
│   ├── header.php
│   ├── footer.php
│   ├── navigation.php
│   └── topBarNav.php
│
├── uploads/
│
├── libs/
│
├── config.php
├── initialize.php
├── index.php
├── home.php
├── about.php
├── services.php
├── appointment.php
├── add_appointment.php
└── contact_us.php
```

---

## 🗄️ Database

The project uses a MySQL database named:

```text
ovas_db
```

### Main Database Tables

* `users` – Stores administrator/user information.
* `appointment_list` – Stores veterinary appointment requests.
* `category_list` – Stores pet/service categories.
* `service_list` – Stores available veterinary services.
* `message_list` – Stores customer inquiries.
* `system_info` – Stores system configuration and information.

The complete database structure and sample data are available in:

```text
database/ovas_db.sql
```

---

# ⚙️ Installation and Setup

## 1. Install XAMPP

Download and install **XAMPP** on your computer.

Start the following services from the XAMPP Control Panel:

```text
Apache
MySQL
```

---

## 2. Copy the Project

Extract the project ZIP file.

Copy the `ovas` folder into:

```text
C:\xampp\htdocs\
```

The project path should look like:

```text
C:\xampp\htdocs\ovas
```

---

## 3. Create the Database

Open your browser and go to:

```text
http://localhost/phpmyadmin
```

Create a new database:

```text
ovas_db
```

---

## 4. Import the SQL File

Inside phpMyAdmin:

1. Select the `ovas_db` database.
2. Click **Import**.
3. Select:

```text
database/ovas_db.sql
```

4. Click **Import/Go**.

The required tables and sample records will be created automatically.

---

## 5. Configure Database Connection

Open:

```text
initialize.php
```

The default database configuration is:

```php
DB_SERVER = "localhost"
DB_USERNAME = "root"
DB_PASSWORD = ""
DB_NAME = "ovas_db"
```

If your MySQL username or password is different, update these values accordingly.

Also make sure the base URL matches your project location:

```php
base_url = "http://localhost/ovas/"
```

---

## 6. Run the Project

Open your browser and visit:

```text
http://localhost/ovas/
```

The main website should now be displayed.

---

# 🔑 Admin Panel

The administrator panel can be accessed through:

```text
http://localhost/ovas/admin/
```

The admin panel provides access to:

* Dashboard
* Appointments
* Services
* Categories
* Inquiries
* Users
* System Settings

> **Note:** Change the default administrator credentials after setting up the project.

---

# 🔄 System Workflow

```text
User
  ↓
Visit Website
  ↓
View Veterinary Services
  ↓
Select Appointment
  ↓
Enter Owner & Pet Details
  ↓
Submit Appointment
  ↓
Appointment Stored in MySQL
  ↓
Admin Reviews Request
  ↓
Admin Updates Appointment Status
  ↓
User Receives Updated Status
```

---

# 📅 Appointment Management

When a user submits an appointment, the system stores information such as:

* Appointment code
* Appointment date
* Owner name
* Contact number
* Email
* Address
* Pet category
* Pet breed
* Pet age
* Selected services
* Appointment status
* Date created
* Date updated

### Appointment Status

```text
0 → Pending
1 → Confirmed
2 → Cancelled
```

The administrator can view and update appointment requests from the admin panel.

---

# 📊 Admin Dashboard

The dashboard provides an overview of the system, including:

* Total services
* Pending appointment requests
* Confirmed appointment requests
* Cancelled appointment requests
* Appointment calendar

This allows the administrator to quickly monitor veterinary appointments.

---

# 🔒 Security

The application includes:

* Admin authentication
* Session-based login
* Protected admin pages
* Database connection handling
* User session management

For production deployment, additional security measures such as stronger password hashing, input validation, CSRF protection, HTTPS, and secure database credentials should be implemented.

---

# 🚀 Future Enhancements

The system can be improved by adding:

* Online payment integration
* Email/SMS appointment notifications
* Doctor/veterinarian profiles
* User registration and login
* Pet medical history
* Prescription management
* Appointment rescheduling
* Automatic appointment reminders
* Doctor availability management
* Mobile application
* Online consultation/video calling
* Reports and analytics

---

# 👨‍💻 Intended Users

### Pet Owners

Can:

* Browse veterinary services
* Submit appointment requests
* Provide pet information
* Send inquiries

### Administrator

Can:

* Manage appointments
* Manage services
* Manage categories
* Manage users
* Manage inquiries
* Monitor appointment schedules

---

# 📄 Project Information

**Project Name:** Online Veterinary Appointment System (OVAS)

**Project Type:** Web-Based Application

**Backend:** PHP

**Database:** MySQL

**Frontend:** HTML, CSS, JavaScript, Bootstrap

**Web Server:** Apache

**Development Environment:** XAMPP

---

# 📝 License

This project is intended for educational and academic purposes. Modify and distribute it according to the license or permissions associated with the original project.

---

## 📞 Support

If you encounter problems while running the project, verify:

1. Apache is running.
2. MySQL is running.
3. `ovas_db` database has been created.
4. `ovas_db.sql` has been imported.
5. Database credentials in `initialize.php` are correct.
6. The project is placed inside the XAMPP `htdocs` directory.
7. The URL is:

```text
http://localhost/ovas/
```

---

⭐ **OVAS – Making Veterinary Appointment Management Simple and Efficient.**
