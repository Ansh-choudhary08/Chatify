# 💬 Chatify

> A real-time full-stack chat application that enables users to communicate through instant messaging with authentication, online user status, and a responsive chat interface.

## 📌 Overview

**Chatify** is a full-stack real-time messaging application built using the **MERN stack**.

The application provides users with a secure platform to register, log in, view other users, see online status, and exchange messages in real time.

The project demonstrates practical implementation of:

- Authentication and authorization
- RESTful APIs
- Real-time communication
- Database integration
- Secure cookies
- Rate limiting
- Production deployment
- Frontend-backend integration

---

## ✨ Features

### 🔐 Authentication
- User signup and login
- Secure logout functionality
- Authentication using cookies
- Protected routes
- Persistent authentication state

### 💬 Real-Time Messaging
- Send and receive messages instantly
- Real-time message updates
- Chat interface for one-to-one conversations
- Message history

### 🟢 Online User Status
- Displays users who are currently online
- Real-time online/offline status updates

### 👤 User Profiles
- User profile functionality
- Profile information management
- Update profile endpoint

### 🛡️ Security
- HTTP cookie-based authentication
- API rate limiting
- Protected backend routes
- Environment variables for sensitive configuration

### 📱 Responsive UI
- Modern chat interface
- Responsive layout
- Sidebar for conversations/users
- Clean messaging experience

---

## 🛠️ Tech Stack

### Frontend
- React.js
- JavaScript
- HTML5
- CSS3

### Backend
- Node.js
- Express.js

### Database
- MongoDB
- MongoDB Atlas

### Real-Time Communication
- Socket.IO

### Authentication & Security
- Cookies
- Authentication middleware
- Rate limiting

### Tools & Deployment
- Git
- GitHub
- Postman
- Vercel
- Render

---

## 🏗️ Project Architecture

```text
                         ┌──────────────────┐
                         │      User        │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │ React Frontend   │
                         │                  │
                         │ Chat UI          │
                         │ Login / Signup   │
                         │ User Sidebar     │
                         └────────┬─────────┘
                                  │
                         HTTP / REST API
                                  │
                                  ▼
                    ┌──────────────────────────┐
                    │   Node.js + Express.js   │
                    │         Backend          │
                    │                          │
                    │ Authentication           │
                    │ User APIs                │
                    │ Message APIs             │
                    │ Rate Limiting            │
                    └────────────┬─────────────┘
                                 │
                    ┌────────────┴────────────┐
                    │                         │
                    ▼                         ▼
          ┌──────────────────┐      ┌──────────────────┐
          │     MongoDB      │      │    Socket.IO     │
          │                  │      │                  │
          │ Users            │      │ Real-Time        │
          │ Messages         │      │ Communication    │
          └──────────────────┘      └──────────────────┘
🔄 How It Works
1. User Authentication

The user creates an account or logs into an existing account.

User
  │
  ▼
Signup / Login
  │
  ▼
Express API
  │
  ▼
Authentication
  │
  ▼
Secure Cookie
  │
  ▼
Authenticated User
2. Sending Messages
User A
  │
  ▼
Chat Interface
  │
  ▼
Backend API
  │
  ▼
Message Processing
  │
  ▼
MongoDB
  │
  ▼
Socket.IO
  │
  ▼
User B receives message
3. Online Users

Socket.IO maintains real-time connections between users and allows the application to determine which users are currently online.

📂 Project Structure
Chatify/
│
├── backend/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── lib/
│   ├── server.js
│   ├── package.json
│   └── ...
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── store/
│   │   ├── lib/
│   │   └── ...
│   │
│   ├── public/
│   ├── package.json
│   └── ...
│
├── .gitignore
└── README.md

The exact folder structure may vary depending on the current version of the project.

⚙️ Installation & Setup
1. Clone the Repository
git clone https://github.com/Ansh-choudhary08/Chatify.git
2. Navigate to the Project
cd Chatify
🔧 Backend Setup

Navigate to the backend:

cd backend

Install dependencies:

npm install

Create a .env file inside the backend directory:

PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
NODE_ENV=development

Start the backend server:

npm run dev
🎨 Frontend Setup

Open another terminal and navigate to the frontend:

cd frontend

Install dependencies:

npm install

Create the required environment file:

VITE_API_URL=http://localhost:5000

Start the frontend:

npm run dev

The application will be available at the local development URL provided by Vite.

🔐 Environment Variables

Do not commit .env files or secret credentials to GitHub.

Backend
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
NODE_ENV=development
Frontend
VITE_API_URL=your_backend_url

Add environment files to .gitignore:

.env
.env.local
.env.production
🌐 Deployment

Chatify is deployed using:

Frontend: Vercel
Backend: Render
Database: MongoDB Atlas
🔗 Live Application

Frontend:
https://chatify-frontend-chi.vercel.app/

Backend:
https://chatify-backend-xxxx.onrender.com/

Replace the backend URL above with the exact Render URL if it differs from the current deployment.

🧪 API Testing

Backend APIs can be tested using Postman.

Example API categories:

Authentication
├── Signup
├── Login
├── Logout
└── Get Current User

Users
├── Get Users
└── Update Profile

Messages
├── Get Messages
└── Send Message
🔒 Security Considerations

Chatify implements several security-related practices:

Authentication using secure cookies
Protected API routes
Rate limiting
Environment variables for secrets
Backend validation
CORS configuration for production deployment
🚀 Key Learning Outcomes

Through this project, I gained practical experience with:

Building a complete MERN stack application
Designing REST APIs using Express.js
Working with MongoDB
Implementing authentication
Managing authentication state on the frontend
Implementing real-time communication with Socket.IO
Connecting React with a Node.js backend
Handling production CORS and cookies
Deploying frontend and backend separately
Debugging production deployment issues
Using Git and GitHub for version control
🔮 Future Improvements

Potential improvements include:

📎 File and image sharing
🎤 Voice messages
👥 Group conversations
✍️ Typing indicators
✅ Message read receipts
🔔 Push notifications
🔎 Message search
🗑️ Delete/edit messages
🌙 Dark/light theme customization
📱 Improved mobile experience
👨‍💻 Author
Ansh Choudhary

GitHub:
https://github.com/Ansh-choudhary08

Portfolio:
https://ansh-choudhary-portfolio.netlify.app/

⭐ Support

If you found this project useful, consider giving the repository a ⭐ on GitHub!


**One important thing:** I intentionally left the Render backend URL as a placeholder because I don't have the exact URL in the current context. Your known GitHub repository is:

`https://github.com/Ansh-choudhary08/Chatify.git`

If you give me your **actual Chatify Vercel + Render URLs**, I can make the README completely final with 
