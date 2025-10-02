# task_manager_backend

A full-stack Task Management application with user authentication, role-based authorization, and admin control. Built with **React** for frontend and **Node.js + Express + MongoDB** for backend.

---

## Features

### User
- Register and login
- Create, read, update, delete personal tasks
- Mark tasks as complete/incomplete
- Protected routes with JWT authentication

### Admin
- View all user tasks
- Delete any user task
- Role-based authorization (admins only)
- Admin dashboard

---

## Tech Stack

- **Frontend:** React, React Router, Tailwind CSS
- **Backend:** Node.js, Express.js, MongoDB, Mongoose
- **Authentication:** JWT (JSON Web Tokens)
- **Security:** Helmet, CORS
- **Password Hashing:** bcrypt.js
- **Validation:** express-validator
- **Deployment:** Vercel (frontend) + Render / local (backend)

---

## Project Structure

server/
├─ controllers/
│ ├─ authController.js
│ └─ taskController.js
├─ middleware/
│ └─ authMiddleware.js
├─ models/
│ ├─ Task.js
│ └─ User.js
├─ routes/
│ ├─ authRoutes.js
│ └─ taskRoutes.js
├─ server.js
frontend/
├─ src/
│ ├─ components/
│ │ └─ Navbar.jsx
│ ├─ contexts/
│ │ └─ AuthContext.jsx
│ ├─ pages/
│ │ ├─ Dashboard.jsx
│ │ ├─ AdminDashboard.jsx
│ │ ├─ Register.jsx
│ │ └─ Login.jsx
│ └─ App.jsx



## Getting Started

### Backend

1. Install dependencies:
```bash
cd server
npm install

##env creation-
MONGO_URL=<your_mongodb_connection_string>
JWT_SECRET_KEY=<your_jwt_secret>
PORT=4000


Usage

Register as a user

Login to access your dashboard

Create tasks and manage them

If you are an admin:

Access the admin dashboard

View all tasks

Delete any task



API Endpoints
Auth

POST /api/auth/register – Register a user

POST /api/auth/login – Login user

Tasks (User)

POST /api/tasks – Create task

GET /api/tasks – Get user tasks

GET /api/tasks/:id – Get single task

PUT /api/tasks/:id – Update task

DELETE /api/tasks/:id – Delete task

Tasks (Admin)

GET /api/tasks/admin/all – Get all tasks (admin only)

DELETE /api/tasks/admin/:id – Delete any task (admin only)
