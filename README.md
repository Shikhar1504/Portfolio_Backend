# Backend API

This repository contains the backend API for a portfolio management system, built with Node.js and Express. It provides a robust set of endpoints for managing user profiles, projects, skills, timelines, and messages, along with authentication, file uploads, and email functionalities.

## Features

- **User Management:** Secure user authentication and authorization using JWT.
- **Profile Management:** Endpoints for managing user profiles, including personal details and contact information.
- **Project Management:** CRUD operations for portfolio projects, including details and associated media.
- **Skill Management:** Manage a list of skills with proficiency levels.
- **Timeline Management:** Organize and display career or educational timelines.
- **Message Handling:** Functionality for handling contact messages.
- **Cloudinary Integration:** Seamless file uploads and management for images and other assets.
- **Email Service:** Integrated email sending capabilities (e.g., for contact forms or notifications).
- **Database Integration:** MongoDB integration using Mongoose for data persistence.
- **Error Handling:** Centralized error handling and asynchronous error catching.

## Technologies Used

- **Node.js:** JavaScript runtime environment.
- **Express.js:** Web application framework for Node.js.
- **MongoDB:** NoSQL database.
- **Mongoose:** MongoDB object data modeling (ODM) for Node.js.
- **JWT (JSON Web Tokens):** For secure authentication.
- **Bcrypt:** For password hashing.
- **Cloudinary:** Cloud-based image and video management.
- **Nodemailer:** For sending emails.
- **Cookie-parser:** Parse Cookie header and populate `req.cookies`.
- **CORS:** Middleware for enabling Cross-Origin Resource Sharing.
- **Dotenv:** Load environment variables from a `.env` file.
- **Express-fileupload:** For handling file uploads.
- **Supabase (potentially):** Although a dependency, its direct usage isn't immediately clear from `server.js` or `package.json` as a primary database, but it might be used for specific services.

## Setup and Installation

To get this project up and running on your local machine, follow these steps:

### Prerequisites

- Node.js (LTS version recommended)
- MongoDB (local or cloud-hosted)

### 1. Clone the repository

```bash
git clone <repository-url>
cd backend
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Variables

Create a `.env` file in the root directory of the project and add the following environment variables:

```
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET_KEY=your_jwt_secret_key
JWT_EXPIRES=7d
COOKIE_EXPIRE=7
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
SMTP_HOST=your_smtp_host
SMTP_PORT=your_smtp_port
SMTP_SERVICE=your_smtp_service
SMTP_MAIL=your_smtp_email
SMTP_PASSWORD=your_smtp_password
```

- Replace placeholders with your actual credentials.
- `MONGO_URI`: Your MongoDB connection string (e.g., `mongodb://localhost:27017/your_database_name` or a MongoDB Atlas URI).
- `JWT_SECRET_KEY`: A strong, random string for JWT signing.
- `CLOUDINARY_*`: Your Cloudinary account credentials.
- `SMTP_*`: Your SMTP server details for sending emails.

### 4. Running the Application

#### Development Mode

To run the application in development mode with `nodemon` (which automatically restarts the server on file changes):

```bash
npm run dev
```

#### Production Mode

To run the application in production mode:

```bash
npm start
```

The server will start on the port specified in your `.env` file (e.g., `http://localhost:5000`).
