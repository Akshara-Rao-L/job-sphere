# Job Sphere – Full Stack Job Portal (MERN)

Job Sphere is a **full‑stack MERN (MongoDB, Express.js, React.js, Node.js)** web application that connects **job seekers** and **employers** on a single platform. Employers can post and manage job listings, while job seekers can browse jobs, apply with ease, and track their applications in real time.

This project demonstrates **production‑level architecture**, clean separation of concerns, secure authentication, and scalable frontend & backend design.

---

##  Features

###  Job Seekers

* User authentication (Register / Login)
* Browse and search available jobs
* Apply for jobs
* View and manage applied jobs
* Update profile and password

###  Employers

* Create, update, and delete job postings
* View applications for posted jobs
* Manage job listings from dashboard

###  Platform Features

* JWT‑based authentication & authorization
* Role‑based access control
* Secure REST APIs
* Email notifications (via utility service)
* Redux Toolkit for state management
* Cron jobs for automation (newsletter / background tasks)
* Centralized error handling

---

##  Tech Stack

### Frontend

* **React.js (Vite)**
* **Redux Toolkit** (state management)
* **React Router**
* **Axios**
* **CSS**

### Backend

* **Node.js**
* **Express.js**
* **MongoDB + Mongoose**
* **JWT Authentication**
* **Nodemailer** (emails)
* **Node‑Cron** (automation)

---

##  Project Structure

```
job-sphere/
├── backend/
│   ├── automation/        # Cron jobs
│   ├── config/            # Environment configs
│   ├── controllers/       # Route controllers
│   ├── database/          # DB connection
│   ├── middlewares/       # Auth & error handlers
│   ├── models/            # Mongoose schemas
│   ├── routes/            # API routes
│   ├── utils/             # JWT & email utilities
│   ├── app.js
│   └── server.js
│
├── frontend/
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── pages/         # App pages
│   │   ├── store/         # Redux store & slices
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── vite.config.js
│
├── README.md
└── package.json
```

---

##  Authentication Flow

* JWT tokens are generated on login/registration
* Tokens are stored securely on the client
* Protected routes enforced via middleware
* Role‑based authorization for employers & job seekers

---

##  Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/job-sphere.git
cd job-sphere
```

### 2. Backend Setup

```bash
cd backend
npm install
```

Create a `config.env` file:

```env
PORT=5000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email
EMAIL_PASS=your_email_password
```

Run backend server:

```bash
npm run dev
```

### 3. Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

Frontend runs on: **[http://localhost:5173](http://localhost:5173)**
Backend runs on: **[http://localhost:5000](http://localhost:5000)**

---

##  API Overview

| Method | Endpoint             | Description     |
| ------ | -------------------- | --------------- |
| POST   | /api/users/register  | Register user   |
| POST   | /api/users/login     | Login user      |
| GET    | /api/jobs            | Get all jobs    |
| POST   | /api/jobs            | Create job      |
| POST   | /api/applications    | Apply for job   |
| GET    | /api/applications/me | My applications |

---

##  Future Improvements

* Advanced job search & filters
* Resume upload & parsing
* Admin dashboard
* Real‑time notifications
* Company profiles

---

##  Author

**Job Sphere** built  by *[Akshara Rao]*
A project focused on real‑world MERN architecture and scalable development practices.

---

##  License

This project is licensed under the **MIT License**.
