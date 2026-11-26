<div align="center">

# 🌍 Terra Twin AI

### AI Planetary Digital Twin

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![Tech Stack](https://img.shields.io/badge/Stack-FastAPI%20%7C%20React%20%7C%20SQLite%20%7C%20Gemini%20AI-blue.svg)]()
[![License](https://img.shields.io/badge/license-MIT-green.svg)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)]()

**A full-stack digital twin of Earth that simulates and predicts environmental, economic, industrial, transportation, and social changes using Gemini AI, FastAPI, and React.**

[Explore the Docs](#-api-documentation) · [Report Bug](../../issues) · [Request Feature](../../issues)

</div>

---

## 📖 About The Project

**Terra Twin AI** is an AI-powered digital replica of Planet Earth. It acts as a "digital twin" that continuously models and predicts how our world is changing across **five critical domains**:

1. 🌡️ **Environmental** (Temperature, CO₂, Pollution)
2. 💰 **Economic** (GDP, Inflation, Markets)
3. 🏭 **Industrial** (Production, Energy Consumption)
4. 🚗 **Transportation** (Traffic, Logistics)
5. 👥 **Social** (Population, Health, Migration)

The system generates realistic simulation data, stores it in a database, and uses **Google Gemini API** to forecast future scenarios based on user queries. All of this is visualized in a beautiful, interactive React dashboard.

> **Note:** This is a practice/learning project designed to demonstrate full-stack architecture, AI integration, and modern UI/UX design. It is not intended for production or enterprise use.

---

## ✨ Key Features

- 🌐 **Interactive Earth Globe** — Real-time visualization of planetary data.
- 📊 **5 Domain Dashboards** — Dedicated views for Environment, Economy, Industry, Transport, and Society.
- 🤖 **Gemini AI Predictions** — Ask natural language questions and get AI-generated forecasts.
- 📈 **Rich Data Visualization** — Line, Bar, Pie, Area, and Radar charts using Recharts.
- 🕓 **Prediction History** — Every forecast is stored and easily revisitable.
- 🎨 **Modern UI** — Dark space theme with glassmorphism, animations (Framer Motion), and a responsive layout.
- 🔐 **JWT Authentication** — Secure login and register system.
- 📚 **Auto API Docs** — Swagger UI available at `/docs` for easy testing.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | React 18, Vite, Tailwind CSS, Recharts, Framer Motion, react-globe.gl |
| **Backend** | Python 3.10+, FastAPI, SQLAlchemy, Pydantic |
| **Database** | SQLite (Lightweight, no external DB setup required) |
| **AI Engine** | Google Gemini API (`gemini-1.5-flash`) |
| **Authentication** | JWT (JSON Web Tokens) + bcrypt |

---

## 📁 Folder Structure

```text
terra-twin-ai/
├── backend/                  # FastAPI Backend
│   ├── app/
│   │   ├── models/           # Database Tables
│   │   ├── schemas/          # Pydantic Validation
│   │   ├── routers/          # API Endpoints
│   │   ├── services/         # Business Logic & Gemini API
│   │   └── core/             # Config & Security
│   ├── main.py               # App Entry Point
│   └── requirements.txt      # Python Dependencies
│
├── frontend/                 # React Frontend
│   ├── src/
│   │   ├── components/       # Reusable UI components
│   │   ├── pages/            # App Pages
│   │   ├── services/         # API fetch calls
│   │   └── context/          # State Management
│   ├── package.json          # Node Dependencies
│   └── vite.config.js        # Vite Config
│
└── database/                 # SQLite DB & Scripts


git clone https://github.com/vishakha2121/terra-twin-ai.git
cd terra-twin-ai



cd backend
python -m venv venv

# Activate Virtual Environment
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Setup Environment Variables
# Create a .env file and add your Gemini API key:
# GEMINI_API_KEY=your_api_key_here

# Run the server
uvicorn main:app --reload


cd frontend
npm install
npm run dev