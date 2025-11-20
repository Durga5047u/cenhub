# 🌐 CenHub — Unified eLearning & Assessment Platform

CenHub is a full-stack eLearning platform designed to support online assessments, programming practice, performance analytics, and centralized content management.  
It provides a seamless learning and testing experience for students, administrators, and super admins through a secure **Role-Based Access Control (RBAC)** system.

---

## 📌 **Features Overview**

### 🔐 Authentication & RBAC
- Single login interface for all user roles.
- JWT-based secure authentication.
- Automatic redirection based on role (Client / Admin / Server).
- Protected API routes for role-specific access.

---

## 👨‍🎓 **Client (Student) Features**
- MCQ-based assessments across Aptitude, Verbal, Reasoning, Programming & DBMS.
- Weekly assessments with instant result evaluation.
- In-browser code editor with support for Java, C, C++, Python.
- File import support for coding challenges.
- Real-time code execution with input/output terminal.
- Interactive performance dashboard:
  - Overall test analytics
  - Subject-wise analysis
- Anti-cheat test window monitoring:
  - First tab switch → Warning  
  - Second switch → Auto-submit test

---

## 👨‍🏫 **Admin Features**
- Content and test management system:
  - Create / update / delete MCQ and programming tasks.
  - Upload assessments and coding challenges.
- Student performance monitoring.
- Event creation and management.
- Full control over test series content.

---

## 🛡️ **Server (Super Admin) Features**
- Manage admin accounts & permissions.
- Oversee platform operations.
- Enforce RBAC rules and maintain system security.
- Approve admin access requests.

---

## 🧱 **Technology Stack**

### 🔹 Frontend
- React.js  
- HTML5, CSS3  
- Axios  
- React Router  
- Recharts / Chart.js (analytics)

### 🔹 Backend
- Spring Boot  
- Spring Security + JWT  
- REST APIs

### 🔹 Database
- PostgreSQL  
- JPA + Hibernate  

### 🔹 Other
- Language execution: GCC, Python 3, JDK  
- Build tool: Maven  

---

## 📊 **System Architecture**

### **Frontend (React.js)**
- Communicates with backend using REST APIs.
- Manages JWT tokens in local storage.
- Role-based navigation and dashboard rendering.

### **Backend (Spring Boot)**
- Authentication, RBAC, and REST API logic.
- Code execution APIs for programming tests.
- Secure JWT-based authorization.
- Data handling and evaluation logic.

### **Database (PostgreSQL)**
- Stores user details, questions, submissions, results, roles, requests, and content.

---

## ⚙️ **Key Modules**

### 🔐 Unified Login System
- All users login from a single page.
- Role identified via JWT claims.
- Redirected to:
  - `/client/dashboard`
  - `/admin/dashboard`
  - `/server/dashboard`

---

### 📚 **Client Dashboard**
- Personalized analytics.
- Test summary charts.
- Coding activity history.
- Weekly assessments.

---

### 🧑‍💼 **Admin Panel**
- Add/Edit/Delete MCQ questions.
- Upload coding challenges.
- Event management.
- View student progress & analytics.

---

### 🛠️ **Server (Super Admin)**
- Approve/reject admin access requests.
- Manage system-wide settings.
- Admin list management.

---

## 🗄️ **Database Setup (PostgreSQL)**

Add this to `application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/cenhub
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
