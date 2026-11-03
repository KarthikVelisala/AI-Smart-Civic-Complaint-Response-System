# 🏙️ AI Smart Civic Complaint & Response System

### AI-Powered Civic Issue Reporting & Management Platform

An AI-powered full-stack web application that simplifies civic issue reporting and management. Citizens can report problems such as garbage accumulation, potholes, damaged streetlights, and water leakage. The system uses AI-based classification to identify complaints, route them to the appropriate municipal departments, and track their resolution through a centralized dashboard.

---

## 📌 Project Overview

The AI Smart Civic Complaint & Response System aims to bridge the communication gap between citizens and municipal authorities through an intelligent digital platform.

The application provides:
- Citizen complaint registration and tracking.
- AI-powered civic issue classification.
- Automated department assignment.
- Real-time complaint status updates.
- Location-based complaint reporting.
- Administrative dashboards and analytics.

The goal is to improve transparency, reduce manual complaint processing, and make civic issue management more efficient.

## 🏗️ System Architecture

```text
       Citizen / Authority / Admin
                    |
                    v
           React Frontend
                    |
                    v
          Node.js + Express API
              /          \
             v            v
         MongoDB       Socket.io
             |
             v
       Python Flask AI Engine
          /           \
         v             v
     OpenCV          NLP / TensorFlow
         |
         v
   AI Classification
```

## 🚀 Key Features

### 🤖 AI-Powered Classification
- Classifies civic complaints using image and text inputs.
- Supports categories such as garbage, potholes, streetlights, and water leakage.
- Uses MobileNetV2-based image classification architecture.
- Includes NLP keyword-based classification fallback.

### 📍 Location-Based Reporting
- Browser-based GPS location detection.
- Geographic tagging of reported complaints.
- OpenStreetMap reverse geocoding integration.

### ⚡ Real-Time Updates
- Socket.io integration for live complaint updates.
- Instant status notifications.
- Real-time communication between citizens and authorities.

### 📊 Admin Dashboard
- Complaint statistics and analytics.
- Category-wise complaint distribution.
- Department-wise complaint tracking.
- Complaint trend visualization.
- Location-based complaint heatmaps.

### 🔐 Authentication & Authorization
- JWT-based authentication.
- Role-based access control.
- Separate Citizen, Authority, and Admin roles.

### 📱 Responsive UI
- Mobile-friendly interface.
- Modern dashboard design.
- Responsive complaint management interface.

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Frontend | React.js, Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB |
| AI/ML | Python, TensorFlow, OpenCV |
| AI Architecture | MobileNetV2, NLP |
| Real-Time Communication | Socket.io |
| Authentication | JWT |
| Maps & Location | OpenStreetMap, Browser Geolocation |
| Deployment | Docker, Docker Compose |
| Development Tools | Git, GitHub, VS Code |

## 🚀 Getting Started

### Prerequisites

- Node.js 20+
- Python 3.11+
- MongoDB
- Git
- Docker Desktop (recommended)

### 1. Clone the Repository

```bash
git clone https://github.com/KarthikVelisala/AI-Smart-Civic-Complaint-System.git

cd AI-Smart-Civic-Complaint-System
```

### 2. Run Using Docker

```bash
docker-compose up --build
```

### 3. Application Services

| Service | URL |
|---|---|
| Frontend | http://localhost:3000 |
| Backend | http://localhost:5000 |
| AI Engine | http://localhost:8000 |
| MongoDB | mongodb://localhost:27017 |

### 4. Manual Installation

**Backend**

```bash
cd server
npm install
cp .env.example .env
node config/seed.js
npm run dev
```

**AI Engine**

```bash
cd ai-engine
pip install -r requirements.txt
python app.py
```

**Frontend**

```bash
cd client
npm install
cp .env.example .env
npm run dev
```

Configure the required environment variables before starting each service.

## 🤖 AI Model Training

The project supports training an image classification model using a categorized civic issue dataset.

```bash
cd ai-engine

python model/train.py
```

Supported image categories:

- Garbage
- Pothole
- Streetlight
- Water Leakage
- Other

The model training process uses the MobileNetV2 architecture.

A keyword-based classification fallback is available when a trained model is not configured.

## 📡 API Endpoints

### Authentication

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register a user |
| POST | `/api/auth/login` | Authenticate user |
| GET | `/api/auth/me` | Retrieve current user |

### Complaint Management

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/complaints` | Submit a complaint |
| GET | `/api/complaints` | Retrieve complaints |
| GET | `/api/complaints/:id` | Retrieve complaint details |
| PATCH | `/api/complaints/:id/status` | Update complaint status |
| DELETE | `/api/complaints/:id` | Delete a complaint (Admin) |

### Admin Analytics

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/admin/stats` | Dashboard statistics |
| GET | `/api/admin/heatmap` | Complaint location data |
| GET | `/api/admin/trends` | Complaint trend analysis |

## 📁 Project Structure

```text
AI-Smart-Civic-Complaint-System/
│
├── client/
│   ├── src/
│   │   ├── pages/
│   │   ├── components/
│   │   ├── context/
│   │   ├── hooks/
│   │   └── api/
│   └── Dockerfile
│
├── server/
│   ├── models/
│   ├── routes/
│   ├── controllers/
│   ├── middleware/
│   └── Dockerfile
│
├── ai-engine/
│   ├── app.py
│   ├── classifier.py
│   ├── model/
│   │   └── train.py
│   └── Dockerfile
│
└── docker-compose.yml
```

## 🎯 Project Objectives

- Digitize traditional civic complaint registration.
- Reduce manual complaint categorization.
- Improve communication between citizens and authorities.
- Enable transparent complaint tracking.
- Use AI-assisted classification to improve complaint management.
- Provide actionable insights through administrative analytics.

## 👨‍💻 Developed by

**Karthik Velisala**

Computer Science & Engineering Graduate | Full Stack Developer

- GitHub: [github.com/KarthikVelisala](https://github.com/KarthikVelisala)
- LinkedIn: [linkedin.com/in/karthik-velisala](https://www.linkedin.com/in/karthik-velisala)

---

⭐ If you find this project interesting, consider giving the repository a star!
