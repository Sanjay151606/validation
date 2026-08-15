# 🔐 Full-Stack Authentication & Enterprise Validation Engine

> Production-ready authentication microservice featuring JWT verification, Passport.js session persistence, Redis rate limiting, and MongoDB schema validation.

[![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)](https://nodejs.org)
[![Express.js](https://img.shields.io/badge/Framework-Express.js-000000?style=flat-square&logo=express&logoColor=white)](https://expressjs.com)
[![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)](https://mongodb.com)
[![Redis](https://img.shields.io/badge/Cache-Redis-DC382D?style=flat-square&logo=redis&logoColor=white)](https://redis.io)

---

## 📌 Overview & Problem Statement
Secure authentication requires defense-in-depth: robust password hashing, session management, token verification, and strict API rate limiting to mitigate brute-force attacks.

This project delivers a complete enterprise authentication boilerplate and validation engine built during the Cognifyz Technologies internship.

---

## ✨ Key Features
- **Dual Authentication Modes:** Supports both stateless JSON Web Tokens (JWT) and stateful Passport.js sessions.
- **Enterprise Form Validation:** Multi-tier server-side schema sanitation and error formatting.
- **DDoS / Brute-Force Defense:** Redis-backed request throttling via `express-rate-limit`.
- **Structured Error Handling:** Centralized error-handling middleware with custom operational exception classes.

---

## 🛠️ Tech Stack
- **Backend:** Node.js, Express.js, Passport.js, JWT, bcryptjs, Morgan
- **Database:** MongoDB (Mongoose ODM)
- **Caching / Throttling:** Redis, `express-session`
- **Views:** EJS, Express EJS Layouts

---

## 🚀 Getting Started Locally

### 1. Clone & Install
```bash
git clone https://github.com/Sanjay151606/fullstack-auth-validation.git
cd fullstack-auth-validation
npm install
```

### 2. Configure Environment Variables
Create a `.env` file (refer to `.env.example`):
```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/auth_db
SESSION_SECRET=your_session_secret
JWT_SECRET=your_jwt_secret
REDIS_URL=redis://localhost:6379
```

### 3. Run Server
```bash
npm start
```
Server runs on `http://localhost:3000`.

---

## 👤 Author
**Sanjay**  
- LinkedIn: [linkedin.com/in/sanjayselvamani/](https://www.linkedin.com/in/sanjayselvamani/)  
- Portfolio: [sanjay151606.github.io/new-portfolio/](https://sanjay151606.github.io/new-portfolio/)  
- Email: [ssanjay41571@gmail.com](mailto:ssanjay41571@gmail.com)
