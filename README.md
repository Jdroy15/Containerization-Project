# FinTrack – Secure & Scalable Finance Tracker

## 📌 Project Description
FinTrack is a **containerized web application** designed to help users **track expenses, analyze spending habits, and manage budgets** efficiently. The system is built using **microservices architecture** with a **secure, scalable deployment**.

---

## 📌 Features
### ✅ **Frontend (React/Next.js)**
- **User-friendly dashboard** for managing transactions.
- **Real-time updates** using WebSockets.

### ✅ **Microservices Architecture**
1️⃣ **Auth Service (Node.js + JWT)**
   - User authentication (Signup, Login, Password Reset).
   - Secure **OAuth2 (Google, GitHub login)**.

2️⃣ **Finance Service (FastAPI/Node.js)**
   - CRUD operations for **transactions, budgets, and categories**.
   - Real-time transaction sync with the frontend.
   - API calls for **currency conversion**.

3️⃣ **Analytics Service (Python/FastAPI)**
   - **Machine Learning** for spending predictions.
   - Provides **monthly spending insights**.

### ✅ **Database Setup**
- **PostgreSQL for Finance & Auth** (Isolated via Docker networks).
- **Redis for caching & session storage**.

### ✅ **Containerization & Deployment**
- **Docker + Docker Compose** for service orchestration.
- **Nginx as a Reverse Proxy** (Bonus Points!).
- **CI/CD pipeline (GitLab) for auto-deployment**.

### ✅ **Security & Best Practices**
- **Database Volume Persistence** (Data survives container restarts).
- **Containerized CI/CD pipeline** for testing and deployment.
- **Role-based Access Control (RBAC) for multi-user security).

---

## 📌 Technologies Used
- **Frontend:** React.js / Next.js + WebSockets
- **Backend:** Node.js (Express) + FastAPI (Python)
- **Database:** PostgreSQL (Finance & Auth), Redis (Caching)
- **Containerization:** Docker, Docker Compose
- **Reverse Proxy:** Nginx
- **Security:** JWT + OAuth2

---

## 📌 Setup & Installation
### 🔹 **Prerequisites**
Ensure you have the following installed:
- **Node.js** (v18+)
- **Docker & Docker Compose**
- **Git**
- **Python 3.8+**

### 🔹 **Clone the Repository**
```bash
$ git clone https://github.com/yourusername/fintrack.git
$ cd fintrack
```

### 🔹 **Environment Variables**
Create a `.env` file in the root directory and add:
```env
PORT=3000
DATABASE_URL=postgres://user:password@db:5432/fintrack
JWT_SECRET=your_secret_key
REDIS_URL=redis://redis:6379
```

### 🔹 **Start the Application**
Run the following command to **build and start** the services:
```bash
$ docker-compose up --build
```

### 🔹 **Access the Application**
- **Frontend:** `http://localhost:3000`
- **API Gateway:** `http://localhost:8000`
- **PostgreSQL Admin:** `http://localhost:5432`
- **Redis:** `http://localhost:6379`

---

## 📌 API Endpoints
### **Auth Service**
| Method | Endpoint | Description |
|--------|------------|-----------------|
| POST   | `/auth/signup` | Register a new user |
| POST   | `/auth/login` | Authenticate user |
| POST   | `/auth/reset-password` | Reset user password |

### **Finance Service**
| Method | Endpoint | Description |
|--------|------------|-----------------|
| GET    | `/finance/transactions` | Get all user transactions |
| POST   | `/finance/transactions` | Add a new transaction |
| DELETE | `/finance/transactions/:id` | Remove a transaction |

### **Analytics Service**
| Method | Endpoint | Description |
|--------|------------|-----------------|
| GET    | `/analytics/spending` | Get spending insights |
| GET    | `/analytics/predictions` | Get ML-based budget predictions |

---

## 📌 CI/CD Pipeline
The **GitLab CI/CD pipeline** automatically builds, tests, and deploys the application.

### **Pipeline Stages:**
1️⃣ **Code Linting & Formatting** 🔍
2️⃣ **Unit & Integration Testing** ✅
3️⃣ **Security Scanning (SAST)** 🔐
4️⃣ **Docker Image Build & Push to Docker Hub** 🐳
5️⃣ **Deploy to Production (via GitLab Runners)** 🚀

---

## 📌 Contribution Guidelines
We welcome contributions! Follow these steps:
1️⃣ **Fork the repo** and create a new branch.
2️⃣ **Commit changes** with proper documentation.
3️⃣ **Create a Pull Request** (PR) for review.

---

## 📌 License
This project is **MIT licensed**. See the [LICENSE](LICENSE) file for details.

---
