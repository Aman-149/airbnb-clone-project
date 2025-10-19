# airbnb-clone-project

![GitHub repo size](https://img.shields.io/github/repo-size/yourusername/airbnb-clone-project)
![GitHub contributors](https://img.shields.io/github/contributors/yourusername/airbnb-clone-project)
![GitHub last commit](https://img.shields.io/github/last-commit/yourusername/airbnb-clone-project)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Django](https://img.shields.io/badge/Django-4.x-green)
![MySQL](https://img.shields.io/badge/MySQL-8.x-blue)
![Docker](https://img.shields.io/badge/Docker-ready-lightblue)
![GraphQL](https://img.shields.io/badge/GraphQL-integrated-pink)

---

## 📘 Project Overview
The **Airbnb Clone Project** is a full-stack web application designed to replicate the core features of the Airbnb platform.  
It focuses on **backend development**, **database design**, **API implementation**, and **security best practices**.  
Learners gain hands-on experience with modern frameworks and workflows used in real-world software engineering.

---

## 🎯 Project Goals
- Build a functional property booking platform using **Django** and **MySQL**.  
- Implement **secure RESTful and GraphQL APIs**.  
- Learn collaborative development with **GitHub**.  
- Apply **CI/CD pipelines** for deployment automation.  
- Document and plan a scalable software system effectively.

---

## 👥 Team Roles

| **Role** | **Responsibilities** |
|-----------|----------------------|
| 🧭 **Project Manager** | Oversees the workflow, timelines, and ensures project quality. |
| 🧱 **Backend Developer** | Develops server-side logic using Django, builds APIs, and integrates the database. |
| 🎨 **Frontend Developer** | Designs user interfaces and integrates frontend with backend APIs. |
| 🗄️ **Database Administrator (DBA)** | Creates and maintains the database schema using MySQL, ensuring performance and integrity. |
| ⚙️ **DevOps Engineer** | Manages CI/CD pipelines, containerization (Docker), and production deployment. |
| 🧪 **QA Engineer (Tester)** | Performs testing (unit, integration, end-to-end) to ensure reliability and quality. |
| 📚 **Documentation Specialist** | Maintains all documentation including README, setup guides, and API references. |

---
## 🧰 Technology Stack

| **Technology** | **Purpose** |
|----------------|-------------|
| 🐍 **Django** | Backend web framework for building APIs and handling business logic. |
| 🛢️ **MySQL** | Relational database system for structured data storage. |
| ⚡ **GraphQL** | Query language for APIs allowing flexible data fetching. |
| 🐳 **Docker** | Containerization tool ensuring environment consistency. |
| 🔁 **GitHub Actions** | CI/CD automation for testing, building, and deploying the app. |
| 🚀 **Nginx / Gunicorn** | Web and WSGI servers for production deployment. |
| 🔐 **JWT (JSON Web Tokens)** | Handles secure user authentication and authorization. |
| 🧩 **Postman / Swagger** | Used for API testing and auto-generated documentation. |

---
## 🗃️ Database Design

**Key Entities & Fields:**

1. **Users**
   - `id`, `username`, `email`, `password_hash`, `role`, `date_joined`
   - A user can own multiple properties and make multiple bookings.

2. **Properties**
   - `id`, `owner_id`, `title`, `description`, `location`, `price_per_night`
   - Each property belongs to one user and can have multiple bookings and reviews.

3. **Bookings**
   - `id`, `user_id`, `property_id`, `check_in`, `check_out`, `total_price`
   - A booking belongs to both a property and a user.

4. **Reviews**
   - `id`, `user_id`, `property_id`, `rating`, `comment`, `created_at`
   - Each review is linked to a property and a user.

5. **Payments**
   - `id`, `booking_id`, `amount`, `payment_method`, `status`, `transaction_date`
   - Each payment is tied to one booking.

**Entity Relationships:**
- **User → Property:** One-to-Many  
- **User → Booking:** One-to-Many  
- **Property → Booking:** One-to-Many  
- **Property → Review:** One-to-Many  
- **Booking → Payment:** One-to-One  

---
## ⚙️ Feature Breakdown

| **Feature** | **Description** |
|--------------|-----------------|
| 👤 **User Management** | Handles user registration, authentication (JWT), and profiles. |
| 🏡 **Property Management** | Hosts can add, update, and remove property listings. |
| 📅 **Booking System** | Users can book available properties and view booking history. |
| ⭐ **Review System** | Guests can leave ratings and comments on properties. |
| 💳 **Payment Integration** | Securely processes payments and stores transaction records. |
| 🔍 **Search & Filter** | Filters listings based on location, price, and date. |
| 🛠️ **Admin Dashboard** | Admin monitors users, properties, payments, and reviews. |

---
## 🔐 API Security

| **Measure** | **Purpose** |
|--------------|-------------|
| **Authentication & Authorization** | Implemented using JWT to secure endpoints. |
| **Input Validation** | Prevents SQL injection and XSS attacks. |
| **Rate Limiting** | Limits excessive API calls to protect against brute force attacks. |
| **HTTPS & Secure Headers** | Encrypts data in transit and adds protective headers. |
| **Role-Based Access Control (RBAC)** | Grants access based on user roles (Admin, Host, Guest). |

**Why Security Matters:**
- Protects sensitive user and payment data.  
- Prevents unauthorized access and data breaches.  
- Ensures trust, reliability, and system integrity.

---
## 🔄 CI/CD Pipeline

**Overview:**  
A **CI/CD pipeline** automates code integration, testing, and deployment, ensuring smooth and consistent delivery.

**Benefits:**
- Early detection of bugs through automated testing.  
- Faster deployment with minimal human intervention.  
- Continuous delivery of updates without downtime.

**Tools Used:**
- 🧩 **GitHub Actions:** Workflow automation for testing and deployment.  
- 🐳 **Docker:** Containerized builds for consistency.  
- 🌐 **Nginx:** Reverse proxy for serving production traffic.  
- ☁️ **AWS / Render / DigitalOcean (optional):** Hosting and scaling the deployed app.

---
