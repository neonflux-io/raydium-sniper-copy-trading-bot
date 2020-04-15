# Education Platform Backend

A comprehensive Node.js/Express.js backend API for an education platform with user authentication, Q&A system, and administrative features.

## 🚀 Features

- **User Authentication** - JWT-based authentication system
- **User Management** - Registration, login, profile management
- **Q&A System** - Question and answer functionality
- **School & Subject Management** - Educational content organization
- **Ranking System** - User ranking and leaderboards
- **Notification System** - Real-time notifications
- **Email Verification** - Account verification via email
- **Admin Panel** - Administrative controls and management
- **Security Middleware** - Authentication and authorization guards

## 🛠 Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: JWT (JSON Web Tokens)
- **Password Hashing**: bcrypt
- **Email Service**: Nodemailer
- **Validation**: express-validator
- **Security**: CORS, Body Parser
- **Development**: Nodemon for hot reloading

## 📁 Project Structure

```
src/
├── config/
│   └── db.js                 # Database connection
├── controllers/
│   ├── authController.js     # Authentication logic
│   ├── userController.js     # User management
│   ├── qaController.js       # Q&A functionality
│   ├── schoolController.js   # School management
│   ├── subjectController.js  # Subject management
│   ├── rankController.js     # Ranking system
│   ├── notifyController.js   # Notifications
│   └── verifyCode.js         # Email verification
├── middlewares/
│   ├── requiredAuth.js       # Authentication middleware
│   ├── requiredAdmin.js      # Admin authorization
│   └── requiredVerify.js     # Verification middleware
├── models/
│   ├── User.js              # User model
│   ├── Question.js          # Question model
│   ├── Answer.js            # Answer model
│   ├── School.js            # School model
│   ├── Subject.js           # Subject model
│   ├── Notify.js            # Notification model
│   └── Sample.js            # Sample data model
├── routes/
│   └── api/
│       ├── index.js         # Main API routes
│       ├── authRoutes.js    # Authentication routes
│       ├── userRoutes.js    # User routes
│       ├── qaRoutes.js      # Q&A routes
│       ├── schoolRoutes.js  # School routes
│       ├── subjectRoutes.js # Subject routes
│       ├── rankRoutes.js    # Ranking routes
│       └── notifyRoutes.js  # Notification routes
└── server.js                # Main server file
```

## ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/sn-chr/backend-node.git
   cd backend-node
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Environment Setup**
   Create a `.env` file in the root directory:
   ```env
   PORT=3000
   HOST=localhost
   MONGODB_URI=mongodb://localhost:27017/education-platform
   JWT_SECRET=your_jwt_secret_key
   EMAIL_HOST=smtp.gmail.com
   EMAIL_PORT=587
   EMAIL_USER=your_email@gmail.com
   EMAIL_PASS=your_email_password
   ```

4. **Start MongoDB**
   Make sure MongoDB is running on your system.

## 🚀 Usage

### Development Mode
```bash
npm run dev
# or
yarn dev
```

### Production Mode
```bash
npm start
# or
yarn start
```

The server will start on `http://localhost:3000` (or your configured HOST and PORT).

## 📝 API Endpoints

### Authentication
- `POST /api/v1/auth/register` - User registration
- `POST /api/v1/auth/login` - User login
- `POST /api/v1/auth/verify` - Email verification

### Users
- `GET /api/v1/users/profile` - Get user profile
- `PUT /api/v1/users/profile` - Update user profile
- `GET /api/v1/users/rankings` - Get user rankings

### Q&A System
- `GET /api/v1/qa/questions` - Get all questions
- `POST /api/v1/qa/questions` - Create new question
- `POST /api/v1/qa/answers` - Submit answer

### Schools & Subjects
- `GET /api/v1/schools` - Get all schools
- `POST /api/v1/schools` - Create school (Admin only)
- `GET /api/v1/subjects` - Get all subjects
- `POST /api/v1/subjects` - Create subject (Admin only)

### Notifications
- `GET /api/v1/notifications` - Get user notifications
- `POST /api/v1/notifications` - Send notification (Admin only)

## 🔒 Security Features

- **JWT Authentication** - Secure token-based authentication
- **Password Hashing** - bcrypt for secure password storage
- **Email Verification** - Account verification system
- **Middleware Protection** - Route-level security
- **CORS Configuration** - Cross-origin request handling
- **Input Validation** - Request validation and sanitization

## 🧪 Testing

```bash
npm test
# or
yarn test
```

## 📄 License

This project is licensed under the ISC License.

## 👨‍💻 Author

**sn-chr** - [rib.armor@gmail.com](mailto:rib.armor@gmail.com)

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📞 Support

For support, email [rib.armor@gmail.com](mailto:rib.armor@gmail.com) or create an issue on GitHub.
