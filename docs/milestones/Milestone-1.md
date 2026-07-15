## Topic: Project Architecture

### What is Separation of Concerns?

Separation of Concerns means each layer of the application has a single responsibility.

Routes
→ Receive requests.

Controllers
→ Handle request/response.

Services
→ Business logic.

Models
→ Database interaction.

Benefits:
- Easier maintenance
- Easier testing
- Cleaner code
- Better scalability

## Express Server

### Objective
Create the first backend server for FinSight AI.

### What I Learned
- How to create an Express application.
- How middleware works.
- How to load environment variables.
- How to create a REST endpoint.
- How to run the server using Nodemon.

### Commands Used

```bash
npm run dev

## MongoDB Connection

### Objective
Connect the Express backend to MongoDB Atlas using Mongoose.

### Files Created
- server/config/db.js

### Files Updated
- server/server.js
- server/.env

### Challenges Faced

#### Issue 1
MongoDB SRV DNS error

Error:
querySrv ECONNREFUSED

Solution:
Used the Legacy MongoDB connection string (mongodb://...) instead of the SRV connection string.

#### Issue 2
Authentication failed

Error:
bad auth : authentication failed

Solution:
Updated the correct database user password in the connection string.

### Result

Successfully connected to MongoDB Atlas.

Output:

✅ MongoDB Connected



## User Model

### Objective

Create the User schema using Mongoose.

### Concepts Learned

- Schema
- Model
- Validation
- unique
- required
- trim
- lowercase
- timestamps

### Files Created

- server/models/User.js

### Result

Successfully created the User model.

## Register API

### Files Created

- server/controllers/authController.js
- server/routes/authRoutes.js

### Concepts Learned

- Controller
- Route
- bcrypt
- HTTP Status Codes
- Request Validation
- Duplicate User Check

### Endpoint

POST /api/auth/register

### Result

Created user registration API.