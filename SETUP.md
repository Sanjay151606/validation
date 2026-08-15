# Quick Setup Guide

## ✅ Current Status
Your application is **running successfully** on http://localhost:3000

## What's Working
- ✅ Express server with EJS templating
- ✅ All routes (Home, Advanced, Register)
- ✅ API endpoints (gracefully handle missing database)
- ✅ Client-side validation and interactions
- ✅ Responsive design with Bootstrap 5
- ✅ Advanced CSS animations

## Optional: Enable Full Features

### 1. MongoDB (for user authentication and data persistence)

**Option A: Local MongoDB**
```bash
# Install MongoDB from https://www.mongodb.com/try/download/community
# Then add to .env:
MONGODB_URI=mongodb://localhost:27017/cognifyz_db
```

**Option B: MongoDB Atlas (Free Cloud)**
1. Create account at https://www.mongodb.com/cloud/atlas
2. Create a free cluster
3. Get connection string and add to .env:
```
MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/dbname/cognifyz_db
```

### 2. Redis (for caching and background jobs)

**Windows:**
```bash
# Install Redis using WSL or Docker
# Docker: docker run -d -p 6379:6379 redis
# Then add to .env:
REDIS_URL=redis://localhost:6379
```

### 3. Weather API (for external API demo)

1. Get free API key from https://openweathermap.org/api
2. Add to .env:
```
EXTERNAL_API_KEY=your_api_key_here
```

## Testing the Application

### 1. Home Page
Visit: http://localhost:3000
- Test the contact form
- View recent submissions (requires MongoDB)

### 2. Advanced Features
Visit: http://localhost:3000/advanced
- See CSS animations
- Test weather API (requires API key)

### 3. User Registration
Visit: http://localhost:3000/register-form
- Test password strength validation
- Register user (requires MongoDB)

### 4. API Endpoints
Test with curl or Postman:
```bash
# Get forms
curl http://localhost:3000/api/forms

# Register user (requires MongoDB)
curl -X POST http://localhost:3000/auth/register \
  -H "Content-Type: application/json" \
  -d '{"username":"testuser","email":"test@example.com","password":"Test@123"}'
```

## Development Mode

For auto-reload on file changes:
```bash
npm run dev
```

## Troubleshooting

**Port already in use:**
```bash
# Change PORT in .env file
PORT=3001
```

**Database connection errors:**
- The app works without MongoDB, but authentication features require it
- Check your MONGODB_URI in .env

**Redis errors:**
- The app works without Redis, but caching and job queue features require it
- Check your REDIS_URL in .env

## Project Features by Task

- **Task 1**: ✅ HTML forms + Express server
- **Task 2**: ✅ Server-side validation
- **Task 3**: ✅ Advanced CSS + Bootstrap
- **Task 4**: ✅ Complex form validation
- **Task 5**: ✅ RESTful API
- **Task 6**: ⚠️ User auth (needs MongoDB)
- **Task 7**: ⚠️ External API (needs API key)
- **Task 8**: ⚠️ Caching/Jobs (needs Redis)

✅ = Working now | ⚠️ = Needs configuration
