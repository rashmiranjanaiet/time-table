🚀 My Performance Hub

A full-stack web application built using React + Vite (Frontend) and Node.js + Express (Backend) with Gemini API integration, JWT-based authentication, and per-user local data storage.

📌 Tech Stack
🖥 Frontend

React

Vite

Axios

React Router

Recharts (for analytics/graphs)

⚙ Backend

Node.js

Express.js

JWT (Authentication)

bcrypt (Password hashing)

Gemini API (AI integration)

Local JSON Database (backend/data/db.json)

✨ Features

🔐 JWT-based Login & Registration

👤 Per-user data isolation

📊 Performance analytics dashboard

🤖 AI-powered insights using Gemini API

💾 Local JSON file storage

⚡ Fast Vite development setup

🌙 Dark mode support (if enabled)

📁 Project Structure
my-performance-hub/
│
├── frontend/               # React + Vite app
│   ├── src/
│   ├── index.html
│   └── vite.config.js
│
├── backend/
│   ├── routes/
│   ├── middleware/
│   ├── controllers/
│   ├── data/
│   │   └── db.json
│   └── server.js
│
└── README.md

🔧 Installation & Setup
1️⃣ Clone the Repository
git clone https://github.com/your-username/my-performance-hub.git
cd my-performance-hub

2️⃣ Backend Setup
cd backend
npm install


Create a .env file inside backend:

PORT=5000
JWT_SECRET=your_secret_key
GEMINI_API_KEY=your_gemini_api_key


Run backend:

npm start


Server runs at:

http://localhost:5000

3️⃣ Frontend Setup
cd frontend
npm install
npm run dev


App runs at:

http://127.0.0.1:5173

🔐 Authentication Flow

User registers

Password is hashed using bcrypt

JWT token is generated

Token stored in frontend (localStorage)

Protected routes validated via middleware

🤖 Gemini API Integration

Sends user performance data

Receives AI-generated suggestions

Displays AI insights on dashboard

💾 Data Storage

All user data stored in:

backend/data/db.json


Structured per user

No external database required

📊 Dashboard

Performance tracking

Graph visualization

AI recommendations

User-based data isolation

🛡 Security Features

Password hashing

JWT authentication

Protected backend routes

Environment variable protection

🚀 Future Improvements

MongoDB integration

Role-based authentication

Deployment (Render/Vercel)

Refresh token system

Cloud storage integration

👨‍💻 Author

Rashmi Ranjan
Computer Science Student
Full-Stack Developer

📄 License

This project is for educational and development purposes.
