# HootyLibrary 📚

A Django-powered web platform that allows readers to discover, read, and interact with books while enabling writers to publish and share their own works.

HootyLibrary was developed as a university group project by Computer Engineering students. The platform aims to provide a digital publishing space where independent authors can publish their content and connect with readers.

---

# 📌 Project Overview

Traditional publishing can create barriers for new writers who want to share their work.

HootyLibrary provides a platform that enables:

- Readers to discover and read books
- Writers to publish and share their works
- Users to interact through reviews and favorites
- Readers to manage their reading activities
- Administrators to manage platform content

The system combines book publishing, user interaction, and content management into a single web application.

---

# ✨ Features

## 🔐 Authentication & User Management

- User registration and login system
- OAuth social authentication
- User profile management
- Secure authentication workflow

Supported social login providers:

- Google
- Facebook
- Microsoft

## 📚 Book Publishing System

Authors can:

- Create and publish books
- Upload book files
- Upload book thumbnails
- Manage published content

Readers can:

- Browse available books
- Search and filter books
- Read published content
- Save favorite books

## ⭐ Reader Interaction

Users can:

- Write reviews
- Add books to favorites
- Track reading history
- Report inappropriate content

## 💬 Messaging System

The platform provides a messaging feature that allows users to communicate with each other.

## 🛠 Admin Management

Administrators can:

- Manage users
- Manage books
- Review reported content
- Control platform data

---

# 🛠 Tech Stack

## Backend

- Python
- Django 4.1

## Frontend

- HTML
- CSS
- JavaScript

## Database

- PostgreSQL
- SQLite (development)

## Deployment

Previously deployed using:

- Heroku
- Gunicorn

---

# 📦 Libraries & Dependencies

Main libraries used:

- Django Allauth  
  - OAuth authentication
  - Social login integration

- Pillow  
  - Image processing
  - Profile images and book thumbnails

- psycopg2  
  - PostgreSQL database connector

- django-heroku  
  - Heroku deployment configuration

---

# 📂 Project Structure

```
hooty_library/

├── hooty_library/
│   ├── settings.py
│   │   └── Database, middleware, authentication settings
│   │
│   ├── urls.py
│   │   └── Main route dispatcher
│   │
│   └── wsgi.py
│       └── WSGI application entry point
│
├── database_models/
│   └── models.py
│       └── Core database models
│
├── register/
│   ├── views.py
│   │   └── Authentication logic
│   └── urls.py
│
├── MAIN_APP/
│   ├── views.py
│   │   └── Homepage, search, filtering
│   └── urls.py
│
├── userProfile/
│   └── User profile management
│
├── book_views/
│   └── Book creation and viewing
│
├── admin_page/
│   └── Admin dashboard
│
├── messaging/
│   └── Messaging system
│
├── templates/
│   └── HTML templates
│
├── static/
│   ├── CSS
│   ├── JavaScript
│   └── Images
│
├── requirements.txt
└── manage.py
```

---

# 🏗 System Architecture

The application follows Django's MVT (Model-View-Template) architecture.

Request flow:

```
User Request
      |
      v
hooty_library/urls.py
      |
      v
Application Views
      |
      +-----------------------------+
      |              |              |
      v              v              v
 MAIN_APP       register       book_views
      |              |              |
      +--------------+--------------+
                     |
                     v
          database_models.models
                     |
                     v
                 Database
```

Core database models:

```
User
 |
 +-- Book
 |
 +-- Review
 |
 +-- Favorite
 |
 +-- Read
 |
 +-- Issue
 |
 +-- Report
```

All application data is managed using Django ORM.

---

# 🌐 Previous Deployment

The application was previously deployed on Heroku during development.

Deployment is currently inactive.

Production deployment was configured using:

- Heroku
- Gunicorn

---

# 📊 Database Models

Main entities:

| Model | Description |
|---|---|
| User | User accounts and profiles |
| Book | Published books |
| Review | User reviews |
| Favorite | Saved books |
| Read | Reading history |
| Issue | Reported issues |
| Report | Content moderation reports |

---

# 🎯 Learning Outcomes

Through this project, we gained experience in:

- Developing a full-stack web application using Django
- Designing relational database models
- Implementing authentication systems
- Integrating OAuth social login
- Building CRUD operations
- Handling file uploads
- Managing user-generated content
- Working with PostgreSQL databases
- Deploying Django applications using cloud platforms

---

# 👨‍💻 Contributors

University group project developed by **PikaPo**.

| Student ID | Name |
|---|---|
| 6310530016 | นายศุภชัย มาตรสุวรรณกิจ |
| 6310682726 | นายณัฐนนท์ บุญเขตต์ |
| 6310682742 | นายชัยวัตร กลั่นเรืองแสง |
| 6310682767 | นายวิชยุตม์ ทับทิม |
| 6310682825 | นายธัญญวัฒน์ ธนัครสมบัติ |

---

# 📌 Future Improvements

Possible improvements:

- Restore cloud deployment
- Add recommendation system
- Improve book search and filtering
- Add real-time messaging
- Improve UI/UX
- Add more advanced content management features
