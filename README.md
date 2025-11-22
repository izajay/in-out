University Gatepass Management System
A complete web application for managing university gatepasses with QR code generation and scanning functionality. Built with React + TailwindCSS (frontend) and Node.js with Express (backend).

🎯 Features
Student Portal
Register/Login with simple authentication
Apply for gatepasses with reason, date, and time
View application status (Pending/Approved/Rejected)
Display QR code when gatepass is approved
Teacher/Warden Portal
Login to view pending applications
Approve or reject gatepass requests
View all gatepass applications with filtering
See generated QR codes for approved passes
Security Portal
QR code scanner using camera
Real-time validation of scanned QR codes
Display student information and gatepass details
Visual feedback for valid/invalid gatepasses
🛠️ Technology Stack
Backend
Node.js
Express.js
JSON Web Tokens (JWT) for authentication
bcryptjs for password hashing
qrcode for QR code generation
JSON file storage (no database required)
Organized with controllers, routes, and middleware
Frontend
React 18
TailwindCSS for modern, responsive UI
React Router DOM for navigation
Vite for build tooling
html5-qrcode for QR scanning
Axios for API calls
Reusable components architecture
📦 Installation
Prerequisites
Node.js (v14 or higher)
npm or yarn
Backend Setup
Navigate to the backend directory:
cd backend
Install dependencies:
npm install
Start the server:
npm start
For development with auto-reload:

npm run dev
The backend server will run on http://localhost:5000

Frontend Setup
Navigate to the frontend directory:
cd frontend
Install dependencies:
npm install
Start the development server:
npm run dev
The frontend will run on http://localhost:3000

🔑 Default Credentials
The system comes with pre-configured demo accounts:

Username	Password	Role
student1	123456	Student
teacher1	123456	Teacher
warden1	123456	Warden
security1	123456	Security
📁 Project Structure
gatepass-system/
├── backend/
│   ├── server.js
│   ├── routes/
│   │   ├── gatepassRoutes.js
│   │   └── userRoutes.js
│   ├── controllers/
│   │   ├── gatepassController.js
│   │   └── userController.js
│   ├── middleware/
│   │   └── auth.js
│   ├── data/
│   │   ├── users.json
│   │   └── gatepasses.json
│   ├── utils/
│   │   ├── generateQR.js
│   │   └── dataHelpers.js
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Navbar.jsx
│   │   │   ├── GatepassForm.jsx
│   │   │   ├── QRDisplay.jsx
│   │   │   ├── Scanner.jsx
│   │   │   └── StatusBadge.jsx
│   │   ├── pages/
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   ├── StudentDashboard.jsx
│   │   │   ├── WardenDashboard.jsx
│   │   │   └── SecurityDashboard.jsx
│   │   ├── context/
│   │   │   └── AuthContext.jsx
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   ├── package.json
│   ├── tailwind.config.js
│   ├── postcss.config.js
│   └── vite.config.js
│
└── README.md
🚀 Usage
Student Workflow
Login with student credentials
Click "Apply for Gatepass"
Fill in the form:
Reason for gatepass
Date
Out time and In time
Submit application
View status in "My Gatepasses" section
When approved, QR code will be displayed
Teacher/Warden Workflow
Login with teacher/warden credentials
View pending applications in dashboard
Click "Approve" or "Reject" for each application
Switch between "Pending" and "All Applications" tabs
View approved gatepasses with QR codes
Security Workflow
Login with security credentials
Click "Start Scanning" to activate camera
Point camera at student's QR code
System automatically validates and displays:
✅ Valid: Shows student info and gatepass details
❌ Invalid: Shows error message
🔒 API Endpoints
Authentication
POST /api/register - Register new user
POST /api/login - User login
GET /api/me - Get current user info
Gatepass
POST /api/gatepass/apply - Apply for gatepass (Student)
GET /api/gatepass/my-passes - Get student's gatepasses
GET /api/gatepass/pending - Get pending gatepasses (Teacher/Warden)
GET /api/gatepass/all - Get all gatepasses (Teacher/Warden)
POST /api/gatepass/:id/action - Approve/reject gatepass
POST /api/gatepass/validate - Validate QR code (Security)
🎨 UI Features
TailwindCSS Design: Modern, clean, and responsive interface
Gradient Backgrounds: Beautiful color schemes
Component-based Architecture: Reusable UI components
Responsive Layout: Works perfectly on desktop, tablet, and mobile
Smooth Animations: Professional transitions and hover effects
Status Badges: Visual indicators for gatepass status
QR Code Display: Clean presentation of QR codes
Scanner Interface: Intuitive camera-based QR scanning
🔐 Security Features
Password hashing with bcryptjs
JWT token-based authentication
Role-based route protection
Input validation on backend
Secure QR code validation with expiry checks
📝 Notes
Data is stored in JSON files (no database required)
All passwords are hashed before storage
QR codes contain gatepass data as JSON
Camera access required for security dashboard
Default password for all demo accounts: 123456
Backend follows MVC architecture pattern
Frontend uses component-based architecture
🐛 Troubleshooting
Backend Issues
Ensure port 5000 is not in use
Check that all npm packages are installed
Verify data directory permissions
Make sure Node.js version is 14 or higher
Frontend Issues
Ensure port 3000 is not in use
Clear browser cache if seeing old data
Check browser console for errors
Verify TailwindCSS is properly configured
Camera Issues (Security Dashboard)
Grant camera permissions in browser
Use HTTPS in production (required for camera access)
Ensure camera is not being used by another application
🚧 Future Enhancements
Database integration (MongoDB/PostgreSQL)
Email notifications
Gatepass history and analytics
Bulk approval/rejection
Export gatepass data
Mobile app version
Dark mode support
Advanced filtering and search
📄 License
This project is open source and available for educational purposes.
