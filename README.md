# Complaint Management System with Chatbot Integration & Ticket Support Generation

A comprehensive complaint management solution with AI-powered chatbot integration, smart ticketing, and multi-modal complaint submission capabilities.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [Usage Guide](#usage-guide)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

---

## 🎯 Overview

The Complaint Management System is an end-to-end solution designed to streamline complaint handling through intelligent categorization, automated ticketing, and real-time tracking. It leverages AI and machine learning to analyze complaints, assign priorities, and facilitate faster resolution.

**Key Highlights:**
- AI-powered chatbot for intelligent complaint submission
- Multi-modal input (text, voice, images)
- Real-time complaint tracking and status updates
- Automated escalation workflow
- Comprehensive admin dashboard with analytics

---

## ✨ Features

### Core Features

- **🔐 User Authentication**: Secure login/registration with JWT-based authentication
- **🤖 AI-Powered Chatbot**: Intelligent assistant for complaint submission and user support
- **🎫 Smart Ticketing System**: Automated ticket generation with intelligent priority assignment
- **📝 Multi-Modal Complaint Logging**: Submit complaints via text, voice recordings, or images
- **📊 Real-Time Tracking**: Monitor complaint status and receive live updates
- **📈 Admin Dashboard**: Comprehensive analytics, statistics, and complaint management tools
- **⚠️ Escalation Workflow**: Structured process for escalating and managing complex issues

### Advanced Enhancements

- **🎤 Voice-to-Text Conversion**: Google Speech-to-Text for voice complaint processing
- **📸 Image Analysis with YOLOv8**: Intelligent object and issue detection in uploaded images
- **🏷️ Auto-Categorization**: Machine learning-based complaint categorization
- **⭐ Smart Priority Assignment**: Severity-based prioritization system
- **📅 Interactive Timeline**: Visual representation of complaint progression and history

---

## 🛠️ Tech Stack

### Frontend

- **React.js** (v18.2.0) - UI library with Hooks and Context API
- **TailwindCSS** (v3.3.2) - Utility-first CSS framework for responsive design
- **Chart.js & React ChartJS 2** - Data visualization and analytics
- **React Router DOM** (v6.11.2) - Client-side routing
- **Axios** (v1.4.0) - HTTP client
- **React Toastify** - User notifications
- **Framer Motion** - Smooth animations

### Backend

- **Flask** (v2.3.3) - Lightweight Python web framework
- **Flask-CORS** - Cross-origin resource sharing
- **PyMongo** (v4.5.0) - MongoDB driver for Python
- **JWT (PyJWT)** - Token-based authentication
- **Google Generative AI** - Gemini API for chatbot
- **APScheduler** (v3.10.4) - Task scheduling and automation
- **Twilio** (v8.9.1) - WhatsApp integration (optional)
- **Flask-Mail** - Email notifications

### Database & Services

- **MongoDB Atlas** - Cloud database
- **Google Gemini API** - Advanced chatbot capabilities
- **Google Speech-to-Text API** - Voice processing
- **YOLOv8** - Image object detection (optional)

---

## 📁 Project Structure

```bash
complaint-management-system/
├── frontend/                          # React.js application
│   ├── src/
│   │   ├── components/
│   │   │   ├── admin/                # Admin-specific components
│   │   │   ├── auth/                 # Authentication components
│   │   │   ├── chatbot/              # Chatbot interface and related
│   │   │   ├── complaints/           # Complaint management UI
│   │   │   ├── feedback/             # Feedback components
│   │   │   ├── rewards/              # Reward system components
│   │   │   ├── layout/               # Header, footer, navbar
│   │   │   ├── EscalationCheck.js    # Escalation monitoring
│   │   │   └── hooks/                # Custom React hooks
│   │   ├── context/
│   │   │   └── AuthContext.js        # Global auth state
│   │   ├── pages/                    # Page components
│   │   ├── services/
│   │   │   └── axios.js              # API configuration
│   │   ├── App.js
│   │   └── index.js
│   ├── package.json
│   ├── postcss.config.js
│   └── tailwind.config.js
│
├── backend/                           # Flask application
│   ├── api/
│   │   ├── __init__.py
│   │   ├── auth.py                   # Authentication routes
│   │   ├── users.py                  # User management
│   │   ├── complaints.py             # Complaint operations
│   │   ├── complaints_updates.py     # Status updates
│   │   ├── chatbot.py                # Chatbot endpoints
│   │   ├── categories.py             # Category management
│   │   ├── admin.py                  # Admin operations
│   │   ├── feedback.py               # Feedback handling
│   │   ├── rewards.py                # Reward system
│   │   ├── reward_levels.py          # Reward tiers
│   │   ├── worker.py                 # Background tasks
│   │   └── __pycache__/
│   ├── models/
│   │   ├── complaint.py              # Complaint data model
│   │   ├── feedback.py               # Feedback model
│   │   └── __pycache__/
│   ├── utils/
│   │   ├── auth_middleware.py        # JWT verification
│   │   ├── notifications.py          # Email/notification service
│   │   ├── rewards.py                # Reward calculations
│   │   ├── download_model.py         # ML model management
│   │   ├── setup_dirs.py             # Directory initialization
│   │   └── __pycache__/
│   ├── app.py                        # Flask app factory
│   ├── run.py                        # Application entry point
│   ├── init_db.py                    # Database initialization
│   ├── make_admin.py                 # Admin account creation
│   ├── scheduled_tasks.py            # Background job scheduling
│   ├── requirements.txt              # Python dependencies
│   ├── .env.example                  # Environment variables template
│   └── __pycache__/
│
├── README.md                          # This file
├── .gitignore
└── LICENSE
```

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v14.0 or higher) - [Download](https://nodejs.org/)
- **Python** (v3.8 or higher) - [Download](https://www.python.org/)
- **MongoDB Atlas Account** - [Create Free Account](https://www.mongodb.com/cloud/atlas/register)
- **Git** - [Download](https://git-scm.com/)
- **npm** or **yarn** - Comes with Node.js

### API Keys Required

- **Google Gemini API Key** - [Get Key](https://makersuite.google.com/app/apikey)
- **Google Speech-to-Text API** (optional) - [Enable API](https://cloud.google.com/speech-to-text)

---

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Kishore276/complaint-management-system.git
cd complaint-management-system
```

### 2. Backend Setup

#### Create Virtual Environment

```bash
cd backend

# On Windows
python -m venv venv
venv\Scripts\activate

# On macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

#### Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Frontend Setup

```bash
cd ../frontend

# Install dependencies
npm install

# Or with yarn
yarn install
```

---

## ⚙️ Configuration

### Backend Environment Variables

1. **Create `.env` file** in the `backend` directory:

```bash
cp .env.example .env
```

2. **Update `.env` with your credentials:**

```env
# MongoDB Connection
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/complaint_system?retryWrites=true&w=majority

# JWT Configuration
SECRET_KEY=your_secure_random_key_here
FLASK_ENV=development
PORT=5000

# Google Gemini API
GEMINI_API_KEY=your_gemini_api_key_here

# Email Configuration (Optional)
SMTP_SERVER=smtp.gmail.com
SMTP_PORT=587
SMTP_USERNAME=your_email@gmail.com
SMTP_PASSWORD=your_app_password
FROM_EMAIL=your_email@gmail.com

# Twilio Configuration (Optional)
TWILIO_ACCOUNT_SID=your_account_sid
TWILIO_AUTH_TOKEN=your_auth_token
TWILIO_WHATSAPP_NUMBER=+1234567890
```

### Setup Instructions for External Services

#### MongoDB Atlas

1. Create account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas/register)
2. Create a free cluster
3. Create a database user with read/write permissions
4. Get your connection string and update `MONGO_URI` in `.env`

#### Google Gemini API

1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create a new API key
3. Add the key to `GEMINI_API_KEY` in `.env`

#### Email Configuration (Gmail)

1. Enable 2-factor authentication on your Gmail account
2. Generate an [App Password](https://support.google.com/accounts/answer/185833)
3. Use the app password in `SMTP_PASSWORD`

---

## ▶️ Running the Application

### Option 1: Run Both Servers

#### Terminal 1 - Backend Server

```bash
cd backend
venv\Scripts\activate  # or: source venv/bin/activate
python run.py
```

Backend will run on: **http://localhost:5000**

#### Terminal 2 - Frontend Server

```bash
cd frontend
npm start
```

Frontend will run on: **http://localhost:3000**

### Option 2: Production Deployment

```bash
# Backend with Gunicorn
cd backend
gunicorn -w 4 -b 0.0.0.0:5000 app:app

# Frontend build
cd frontend
npm run build
```

---

## 📖 Usage Guide

### For Regular Users

1. **Register/Login**
   - Create a new account or login with existing credentials
   - Secure JWT-based session management

2. **Submit a Complaint**
   - Navigate to "New Complaint"
   - Choose input method:
     - Text description
     - Voice recording (auto-transcribed)
     - Image upload (with object detection)
   - System automatically categorizes and assigns priority

3. **Track Complaint**
   - View complaint status on dashboard
   - Receive real-time updates
   - Access complete complaint history

4. **Provide Feedback**
   - Rate complaint resolution
   - Leave suggestions for improvement

### For Administrators

1. **Access Admin Dashboard**
   - Login with admin credentials
   - View all system complaints and analytics

2. **Manage Complaints**
   - Assign complaints to workers
   - Update complaint status
   - Add internal notes
   - Trigger escalations

3. **View Analytics**
   - Complaint trends and statistics
   - Category-wise distribution
   - Resolution time metrics
   - User satisfaction scores

4. **Manage Escalations**
   - Review escalated complaints
   - Assign to senior staff
   - Set escalation deadlines

---

## 📚 API Documentation

### Authentication Endpoints

```
POST   /api/auth/register     - Register new user
POST   /api/auth/login        - Login user
POST   /api/auth/logout       - Logout user
GET    /api/auth/profile      - Get user profile
```

### Complaint Endpoints

```
GET    /api/complaints        - List all complaints
POST   /api/complaints        - Create new complaint
GET    /api/complaints/<id>   - Get complaint details
PUT    /api/complaints/<id>   - Update complaint
DELETE /api/complaints/<id>   - Delete complaint
```

### Chatbot Endpoint

```
POST   /api/chatbot/message   - Send message to chatbot
GET    /api/chatbot/history   - Get chat history
```

### Admin Endpoints

```
GET    /api/admin/dashboard   - Admin dashboard data
GET    /api/admin/analytics   - Complaint analytics
PUT    /api/admin/complaints/<id> - Manage complaint
```

---

## 🤝 Contributing

We welcome contributions! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 💬 Support

---
## Developed By

G.Yuva Kishore Reddy  
Passionate about AI, automation, and building impactful tech solutions.

## Contact

Email: g.yuvakishorereddy@gmail.com   
WhatsApp Channel: https://whatsapp.com/channel/0029Vb3la9V7NoZtA1GUI00d

Star⭐ this repo if you found it helpful!


For support, questions, or bug reports:

- **Open an Issue**: [GitHub Issues](https://github.com/Kishore276/complaint-management-system/issues)
- **Email**: [contact@example.com](mailto:contact@example.com)
- **Documentation**: [CLOUD_SETUP.md](CLOUD_SETUP.md)

---

**Happy Complaining! 😊**
