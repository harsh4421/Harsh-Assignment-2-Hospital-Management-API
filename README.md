# Hospital Management System

A full-stack Hospital Management System built using Node.js, Express.js, MongoDB, and React. The application provides user authentication and allows authenticated users to create, view, update, and delete hospital records.

## Features

- User registration
- User login and logout
- User authentication using Passport.js
- Password hashing using bcryptjs
- Protected frontend routes
- Add a new hospital
- View all hospitals
- View a hospital by ID
- Update hospital information
- Delete a hospital
- MongoDB database integration
- RESTful API using Express.js
- React-based frontend
- CORS support for frontend-backend communication

## Tech Stack

### Backend

- Node.js
- Express.js
- MongoDB
- Mongoose
- Passport.js
- bcryptjs
- dotenv
- CORS

### Frontend

- React
- JavaScript
- React Router
- Context API
- Vite
- CSS

## Project Structure

```text
Hospital-Management-System/
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
│   ├── .gitignore
│   ├── package.json
│   ├── package-lock.json
│   └── server.js
│
├── Frontend/
│   ├── public/
│   │
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
│   ├── .gitignore
│   ├── eslint.config.js
│   ├── index.html
│   ├── package.json
│   ├── package-lock.json
│   └── vite.config.js
│
├── Assignment 2.txt
└── README.md
```

## Prerequisites

Before running the project, make sure the following are installed:

- Node.js
- npm
- MongoDB (local or MongoDB Atlas)
- A modern web browser

Check Node.js and npm installation:

```bash
node -v
npm -v
```

## Backend Setup

Open a terminal in the project root.

```bash
cd Backend
npm install
```

Create a `.env` file inside the `Backend` folder.

Example:

```env
MONGODB_URI=your_mongodb_connection_string
PORT=4000
SESSION_SECRET=your_session_secret
```

Do not upload the `.env` file to GitHub.

Start the backend server:

```bash
npm run dev
```

The backend runs on:

```text
http://localhost:4000
```

## Frontend Setup

Open another terminal from the project root:

```bash
cd Frontend
npm install
```

Start the frontend:

```bash
npm run dev
```

Vite will display the frontend URL in the terminal. It is normally:

```text
http://localhost:5173
```

## Running the Project

The project requires two terminals.

### Terminal 1 - Backend

```bash
cd Backend
npm install
npm run dev
```

### Terminal 2 - Frontend

```bash
cd Frontend
npm install
npm run dev
```

After both servers are running, open the frontend URL provided by Vite in your browser.

## API Endpoints

### Authentication

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/auth/register` | Register a new user |
| POST | `/auth/login` | Login an existing user |
| POST | `/auth/logout` | Logout the current user |

### Hospital Management

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/hospitals` | Get all hospitals |
| GET | `/hospitals/:id` | Get a hospital by ID |
| POST | `/hospitals` | Create a new hospital |
| PUT | `/hospitals/:id` | Update hospital information |
| DELETE | `/hospitals/:id` | Delete a hospital |

## Frontend Routes

| Route | Description | Authentication |
|-------|-------------|----------------|
| `/login` | Login page | No |
| `/register` | Registration page | No |
| `/` | Hospital dashboard | Yes |
| `/hospitals/new` | Add a new hospital | Yes |
| `/hospitals/:id/edit` | Edit hospital information | Yes |

## Authentication

The application provides user authentication using Passport.js.

The authentication system includes:

- User registration
- User login
- User logout
- Password hashing with bcryptjs
- Protected frontend routes
- Authentication state management using React Context API

Users must be authenticated to access protected hospital management features.

## Hospital Management

Authenticated users can perform CRUD operations on hospital records.

### Create Hospital

Users can add a new hospital by entering the required hospital information through the frontend form.

### View Hospitals

Users can view all hospital records from the dashboard.

A specific hospital can also be retrieved using its ID.

### Update Hospital

Users can edit and update the information of an existing hospital.

### Delete Hospital

Users can delete an existing hospital record.

## Application Flow

The application follows this architecture:

```text
React Frontend
      |
      v
Express.js API
      |
      v
Router
      |
      v
Controller
      |
      v
Mongoose
      |
      v
MongoDB
```

Authentication follows this flow:

```text
React Frontend
      |
      v
Authentication Request
      |
      v
Express.js
      |
      v
Passport.js
      |
      v
User Model
      |
      v
MongoDB
```

## Environment Variables

The backend uses environment variables for database and server configuration.

Example:

```env
MONGODB_URI=your_mongodb_connection_string
PORT=4000
SESSION_SECRET=your_session_secret
```

The `.env` file should remain local and must not be committed to GitHub.

The repository contains `.gitignore` rules to prevent sensitive environment variables and dependencies from being uploaded.

## Error Handling

The application handles common errors including:

- Invalid login credentials
- Invalid hospital IDs
- Hospital not found
- Invalid request data
- Authentication errors
- Database errors
- Server errors

The backend returns appropriate HTTP status codes and JSON responses.

## Backend Responsibilities

The backend handles:

- Express server setup
- MongoDB connection
- User authentication
- Password hashing
- Database models
- Hospital CRUD operations
- API routing
- Request processing
- JSON responses
- Error handling

## Frontend Responsibilities

The frontend handles:

- User registration
- User login
- User logout
- Authentication state
- Protected routes
- Hospital dashboard
- Adding hospitals
- Viewing hospitals
- Editing hospitals
- Deleting hospitals
- Communication with the backend API

## Security

The application follows basic security practices such as:

- Password hashing using bcryptjs
- Environment variables for sensitive configuration
- `.env` excluded from Git
- Protected frontend routes
- Authentication using Passport.js
- Server-side error handling

## Future Improvements

Possible improvements include:

- Hospital search
- City-based filtering
- Pagination
- Role-based authentication
- Admin dashboard
- Hospital statistics
- Improved form validation
- Better loading states
- Improved error messages
- Cloud deployment

