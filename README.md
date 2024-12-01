![Screenshot 2024-12-01 231718](https://github.com/user-attachments/assets/a942de03-cefa-482e-aef5-b6c6a6b1c6ca)

![Screenshot 2024-12-01 231617](https://github.com/user-attachments/assets/fdea3569-666d-4b69-95d5-502b87a17fe1)

![Screenshot 2024-12-01 231630](https://github.com/user-attachments/assets/eb1fa9dc-765c-4f60-b580-c5d22c79efc2)

![Screenshot 2024-12-01 231736](https://github.com/user-attachments/assets/ee5cad56-4215-4938-9f7b-dca1ab7b5d8c)

![Screenshot 2024-12-01 231803](https://github.com/user-attachments/assets/fae233ad-eae3-4ac0-ba25-70b713824212)

![Screenshot 2024-12-01 231815](https://github.com/user-attachments/assets/4231704e-0a30-4d92-81d9-f6884eb63a39)








# Voting Application

This is a **Voting backend application** built with Node.js, Express.js, Mongoose, and other dependencies. It provides APIs for user and candidate management, including authentication via JWT tokens.

---

## Features

- **Authentication**:
  - Secure login and JWT-based token generation.
  - Middleware for protecting routes.
- **Role Based Endpoints Access**:
  - Roles are predefined (e.g., Admin, User, Moderator).
  - Each role has specific permissions and access levels.
- **Routing**:
  - Modular user and candidate routes for better organization.
- **Database**:
  - MongoDB integration using Mongoose.
- **Environment Variables**:
  - Secure configuration using `dotenv`.

---

## Prerequisites

Make sure you have the following installed on your machine:

- Node.js (v14.x or later)
- MongoDB (Running instance or cloud database like MongoDB Atlas)

---

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd backend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up environment variables:

   - Create a `.env` file in the project root.
   - Add the following variables:

     ```plaintext
     PORT=3000
     MONGO_URI=<your-mongo-db-connection-string>
     JWT_SECRET=<your-secret-key>
     ```

4. Start the application:

   ```bash
   nodemon server.js
   ```

   For development, use:

   ```bash
   npx nodemon server.js
   ```

---

## Project Structure

```plaintext
.
├── db.js                 
├── routes/
│   ├── userRoutes.js     
│   ├── candidateRoutes.js 
├── middleware/
│   ├── authMiddleware.js
├── server.js             
├── .env                
├── package.json         
```

---

## Available Scripts

- `npm start`: Start the server.
- `npx nodemon server.js`: Start the server in development mode with auto-restart on file changes.

---

## API Endpoints

### User Routes (`/user`)

- **POST /user/register**  
  Registers a new user.

- **POST /user/login**  
  Authenticates the user and returns a JWT token.

### Candidate Routes (`/candidate`)

- **GET /candidate/all**  
  Fetches all candidates.

- **POST /candidate/add**  
  Adds a new candidate.

---

## Middleware

- **JWT Authentication Middleware**  
  Ensures protected routes are only accessible with a valid token.

---

## Dependencies

- `express`: Fast, unopinionated web framework.
- `mongoose`: MongoDB object modeling.
- `jsonwebtoken`: JWT-based authentication.
- `dotenv`: Secure environment variable management.
- `bcrypt`: Password hashing for secure storage.
- `nodemon`: Development utility for restarting the server automatically.

---


Thank You!
