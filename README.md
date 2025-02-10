# Task Manager API

## Description
Task Manager API is a backend service built with Node.js and Express that provides user authentication and task management functionalities. It allows users to register, log in, create, update, delete, and retrieve tasks. The API uses MongoDB as the database and JWT for authentication.

## Features
- User Registration & Login (JWT Authentication)
- Task Management (CRUD operations)
- Secure authentication middleware
- MongoDB database integration
- Environment variable support using dotenv

## Tech Stack
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB & Mongoose** - Database and ODM
- **JWT** - Authentication
- **bcrypt.js** - Password hashing
- **cors** - Cross-Origin Resource Sharing
- **dotenv** - Environment variables
- **nodemon** - Development tool for auto-restart

## Installation

### Prerequisites
- Node.js installed (latest LTS recommended)
- MongoDB installed or a MongoDB Atlas account

### Steps to Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repository/task-manager-api.git
   cd task-manager-api
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

3. Create a `.env` file in the root directory and add the following:
   ```env
   PORT=5000
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_secret_key
   ```

4. Start the server:
   ```sh
   npm run dev  # Runs in development mode with nodemon
   npm start    # Runs in production mode
   ```

## API Endpoints

### Authentication Routes
| Method | Endpoint       | Description             |
|--------|--------------|-------------------------|
| POST   | `/api/auth/register` | Register a new user |
| POST   | `/api/auth/login`    | Authenticate user and get token |

### Task Routes (Protected)
| Method | Endpoint       | Description             |
|--------|--------------|-------------------------|
| GET    | `/api/tasks`  | Get all tasks for the authenticated user |
| POST   | `/api/tasks`  | Create a new task |
| PUT    | `/api/tasks/:id` | Update an existing task |
| DELETE | `/api/tasks/:id` | Delete a task |

## Project Structure
```
/task-manager-api
│── /models
│   ├── User.js
│   ├── Task.js
│── /routes
│   ├── auth.js
│   ├── tasks.js
│── /middleware
│   ├── auth.js
│── .env (not included in repo)
│── index.js
│── package.json
```

## Middleware
- `auth.js`: Protects routes using JWT authentication.


