# 💼 Professional Networking Platform

🌐 Live: 🔗 https://mini-linkedin-like-community-platform-1.onrender.com

👤 Admin / Demo User Logins

Note: For demo purposes, you can register with any email and password.

✅ Example:

Email: karthik@gmail.com

Password: Karthik25$

> **A full-stack social web application inspired by LinkedIn, allowing users to register, log in, create public posts, and view content from the community in real-time. This platform was built as a showcase of modern web development techniques, including React, Node.js, Express, MongoDB, and JWT-based authentication.**

🌟 Overview

This platform simulates a simplified version of LinkedIn's core functionalities, designed with performance and user experience in mind. It enables users to:

- Authenticate securely.
- Share text-based updates.
- Browse updates from others in the community.
- Navigate to user profiles and view user-specific content.

The UI is designed to be clean, minimal, and responsive using Tailwind CSS and custom components. This makes it both mobile-friendly and aesthetically pleasant.

🔧 Core Features (In Depth)

✅ 1. Authentication & User Management

🔁 Authentication Flow (Formik, Yup, bcrypt)

🧾 Form Handling – Formik + Yup

- User login and registration forms are built using Formik for seamless form state management.
- Validation is handled with Yup, enforcing rules like required fields, valid email format, and minimum password length.
- Real-time validation feedback is provided, enhancing the user experience.

🔒 Password Security – bcrypt

- During registration, user passwords are securely hashed using bcrypt before being stored in the database.
- On login, the provided password is compared with the hashed password using bcrypt for verification.
- Authentication is handled using JWT (JSON Web Tokens).
- Tokens are securely stored in localStorage and are validated on each page refresh to maintain session persistence.
- If the token is missing or invalid, the user is automatically redirected to the login page, ensuring protected access to private routes.

📝 2. Post Creation & Feed Display
- Authenticated users can post text updates (just like LinkedIn statuses).
- Posts include metadata like author name and timestamp.
- The feed updates automatically (every 5 seconds) to fetch the latest posts from MongoDB.

👤 3. Author & Profile View
- Each post shows the author's name and a link to their profile page.
- Users can click “View Posts” to see all posts by that specific user.
- Profile pages are dynamically routed using React Router.

💡 4. UX & Visual Design
- The UI uses Tailwind CSS for modern responsiveness.
- Includes dark mode-ready styles.
- Smooth transitions, hover animations, soft shadows, and rounded elements provide a professional feel.

⚙️ Tech Stack Used

🖥️ Frontend

React.js – Component-based architecture for UI

React Router DOM – Routing and protected routes

Tailwind CSS – Rapid styling with utility classes

Formik – Elegant form handling and state management

Yup – Form validation schema integrated with Formik

Axios – For making API requests

Lucide Icons – Modern and consistent icon set

React Hooks – For managing state and side effects (useState, useEffect, useRef)


🌐 Backend

Node.js & Express – RESTful API server

MongoDB with Mongoose – NoSQL database for storing users and posts

bcrypt – Secure password hashing before saving user credentials

jsonwebtoken (JWT) – For authentication and protected routes

☁️ Cloud & Other Tools

Cloudinary – For uploading and hosting profile images

Multer – Middleware for handling file uploads

dotenv – For environment variable management


| METHOD | ENDPOINT         | DESCRIPTION            |
| ------ | ---------------- | ---------------------- |
| POST   | `/register`      | Register a new user    |
| POST   | `/login`         | Log in existing user   |
| POST   | `/validateToken` | Check if JWT is valid  |
| GET    | `/posts`         | Fetch all public posts |
| POST   | `/posts`         | Create a new post      |
| GET    | `/profile/:id`   | Get posts by a user ID |


📌 Key Design Decisions

- Auto-refreshing feed: Eliminates the need for WebSockets while maintaining near real-time updates.
- Scoped component architecture: Reusable components for Auth, Post, Feed, Profile, etc.
- Dark mode-ready: The entire platform is visually consistent in both light and dark themes.


## 🛠️ Setup Instructions

### 1. Clone the Repository

git clone https://github.com/pdkarthik/Mini-LinkedIn-like-Community-Platform

cd Mini LinkedIn-like Community Platform

2. Backend Setup

npm install

npm start

Ensure MongoDB is running locally or replace MONGO_URI with your MongoDB Atlas string in .env:

MONGO_URI=your_mongo_uri

JWT_SECRET=your_jwt_secret

3. Frontend Setup

cd client

npm install

npm start

Frontend will run on: http://localhost:3000 (or as set in vite.config.js)


✨ Extra Features
- Profile picture upload (Cloudinary + Multer)
- User profile view with dynamic routing
- Token-based session persistence
- Dark mode-friendly design
- Beautiful UI styled with Tailwind CSS

