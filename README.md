# Hospital Management API

A full-stack Hospital Management System built with a Node.js and Express.js backend and a React frontend. The application provides user authentication and complete CRUD operations for managing hospital records.

## Tech Stack

### Backend

- **Runtime:** Node.js
- **Framework:** Express.js
- **Database:** MongoDB
- **ODM:** Mongoose
- **Authentication:** Passport.js (Local Strategy)
- **Password Hashing:** bcryptjs

### Frontend

- **Framework:** React 19
- **Build Tool:** Vite
- **Routing:** React Router
- **State Management:** React Context API

## Project Structure

```text
Hospital-Management-API/
│
├── Backend/
│   ├── Config/
│   │   ├── db.js
│   │   └── passport.js
│   │
│   ├── Controllers/
│   │   ├── authcontroller.js
│   │   └── hospitalscontroller.js
│   │
│   ├── Models/
│   │   ├── user.js
│   │   └── hospitals.js
│   │
│   ├── Router/
│   │   ├── auth_router.js
│   │   └── hospitals_router.js
│   │
│   ├── .env.example
│   ├── package.json
│   └── server.js
│
├── Frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Navbar.jsx
│   │   │   ├── HospitalCard.jsx
│   │   │   └── ProtectedRoute.jsx
│   │   │
│   │   ├── context/
│   │   │   └── AuthContext.jsx
│   │   │
│   │   ├── pages/
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   ├── Dashboard.jsx
│   │   │   └── HospitalForm.jsx
│   │   │
│   │   ├── api.js
│   │   ├── App.jsx
│   │   └── main.jsx
│   │
│   ├── package.json
│   └── vite.config.js
│
├── Assignment 2.txt
├── README.md
└── .gitignore
