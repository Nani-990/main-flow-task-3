Here’s a complete `README.md` for your **Login and Signup System using PHP** project. You can include this in your project root directory:

---

```markdown
# 🔐 Login & Signup System using PHP

A basic and secure user authentication system that allows users to **register**, **log in**, and access a **protected dashboard**. This project demonstrates core full stack concepts using **PHP, MySQL, HTML, and CSS**.

## 📌 Features

- User Registration with validation
- Secure Password Hashing (using `password_hash`)
- User Login with session handling
- Protected dashboard (accessible only after login)
- Logout functionality
- Error handling (e.g., duplicate user, wrong password)
- Basic responsive styling using HTML & CSS

---

## 🧰 Technologies Used

- **Frontend**: HTML, CSS  
- **Backend**: PHP  
- **Database**: MySQL  
- **Server**: Apache (XAMPP/WAMP/LAMP)

---

## 🏗️ Database Setup

1. Open **phpMyAdmin**.
2. Create a database named: `user_auth`.
3. Run the following SQL:

```sql
CREATE DATABASE user_auth;

USE user_auth;

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(100) NOT NULL UNIQUE,
    email VARCHAR(100) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

## 📁 Folder Structure

```
/user-login-registrartion-project
│
├── db.php              # Database connection
├── signup.php          # Handles user registration
├── login.php           # Handles login logic
├── logout.php          # Ends user session
├── dashboard.php       # Protected page
│
├── signup.html         # Signup form (frontend)
├── login.html          # Login form (frontend)
├── style.css           # Basic styling
└── README.md           # Project documentation
```

---

## 🚀 How to Run the Project

1. **Clone or download** this repository into your local web server directory (e.g., `htdocs` in XAMPP).
2. Start **Apache** and **MySQL** using XAMPP/WAMP.
3. Import the `user_auth` database using phpMyAdmin (see SQL above).
4. Open your browser and go to:

```
http://localhost/user-auth-project/signup.html
```

5. Register a new user, then login and access the protected dashboard.

---

## 🧪 Testing Checklist

| Test Case | Expected Result |
|-----------|------------------|
| Signup with valid data | Redirect to login with success |
| Signup with existing username/email | Show error |
| Passwords don't match | Show validation error |
| Login with correct credentials | Redirect to dashboard |
| Login with wrong credentials | Show error |
| Access dashboard without login | Redirect to login |
| Logout | Destroys session and redirects to login |

---

## 🔐 Security Features

- Passwords are hashed using `password_hash()`
- SQL Injection prevented using **Prepared Statements**
- Sessions used to protect authenticated routes
- Inputs are validated before protect
