# 📚 StudyNotion Backend

The backend service for **StudyNotion**, a full-stack EdTech platform designed to provide seamless online learning experiences.  
This service powers authentication, course management, payments, and media handling.

---

## 🚀 Tech Stack
- **Runtime:** Node.js  
- **Framework:** Express.js  
- **Database:** MongoDB + Mongoose  
- **Authentication:** JWT, Bcrypt  
- **Payments:** Razorpay  
- **Media Storage:** Cloudinary  
- **Email Service:** Nodemailer  
- **Utilities:** Dotenv, Nodemon, etc.  

---

## ✨ Features
- 🔑 **Authentication & Security**
  - User sign-up, login, logout
  - OTP-based email verification
  - Password encryption with Bcrypt
  - JWT-based session handling

- 🎓 **Learning Management**
  - Course creation, update, and deletion (Instructor only)
  - Enrollments & progress tracking
  - Ratings & reviews system

- 💳 **Payments**
  - Secure course purchase with Razorpay
  - Payment success/failure webhook handling

- ☁️ **Media & File Uploads**
  - Cloudinary integration for videos, thumbnails, and documents

- 📩 **Email & Notifications**
  - OTP emails
  - Password reset emails

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository
```bash
git clone https://github.com/Priyanshupriyadarshi29/study-notion-backend.git
cd study-notion-backend
2️⃣ Install dependencies
bash
Copy code
npm install
3️⃣ Configure Environment Variables
Create a .env file in the root directory:

env
Copy code
PORT=5000
MONGODB_URI=your_mongo_db_url
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_key
CLOUDINARY_API_SECRET=your_cloudinary_secret
RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_KEY_SECRET=your_razorpay_secret
MAIL_HOST=smtp.example.com
MAIL_USER=your_email@example.com
MAIL_PASS=your_email_password
4️⃣ Run the server
bash
Copy code
npm run dev
Server runs at: http://localhost:5000

📡 API Endpoints
🔐 Auth Routes
Method	Endpoint	Description
POST	/api/auth/signup	Register new user
POST	/api/auth/login	Login user
POST	/api/auth/verify	Verify OTP
POST	/api/auth/reset	Reset password

🎓 Course Routes
Method	Endpoint	Description
GET	/api/courses	Get all courses
GET	/api/courses/:id	Get single course
POST	/api/courses	Create course (Instructor)
PUT	/api/courses/:id	Update course (Instructor)
DELETE	/api/courses/:id	Delete course (Instructor)

💳 Payment Routes
Method	Endpoint	Description
POST	/api/payments/order	Create order
POST	/api/payments/verify	Verify payment

📁 Project Structure
bash
Copy code
study-notion-backend/
│── config/        # DB & Cloudinary configs
│── controllers/   # Route controllers
│── middlewares/   # Custom middlewares (auth, error handling)
│── models/        # Mongoose models
│── routes/        # API routes
│── utils/         # Helper utilities (mail, JWT, etc.)
│── index.js       # Entry point
│── package.json   # Dependencies & scripts
│── .env           # Environment variables
│── .gitignore     # Ignored files
🤝 Contributing
Fork the repo

Create a new branch (feature/xyz)

Commit your changes

Push the branch

Create a Pull Request
