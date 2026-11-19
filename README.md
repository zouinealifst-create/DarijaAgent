---
title: Darija AI
emoji: 🚀
colorFrom: red
colorTo: green
sdk: docker
app_port: 7860
pinned: false
---

<div align="center">

# 🇲🇦 Darija AI — Immersion System

**An AI-powered platform that teaches Moroccan Darija through real conversations, adaptive quizzes, and cultural insights.**

[![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-3.x-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com)
[![CrewAI](https://img.shields.io/badge/CrewAI-Multi--Agent-FF6B6B?style=for-the-badge&logo=robot&logoColor=white)](https://crewai.com)
[![OpenRouter](https://img.shields.io/badge/OpenRouter-Gemma_4_31B-7C3AED?style=for-the-badge&logo=openai&logoColor=white)](https://openrouter.ai)
[![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://mongodb.com)
[![Docker](https://img.shields.io/badge/Docker-HuggingFace_Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://huggingface.co)
[![Google OAuth](https://img.shields.io/badge/Google-OAuth2-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://developers.google.com/identity)

</div>

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🤖 **AI Chat** | Ask anything, get answers in English with real Darija expressions woven in naturally |
| 🧠 **Quiz Mode** | AI-generated multiple-choice questions to test and reinforce your Darija |
| 📊 **Session Summary** | Personalized recap of everything you learned in a session |
| 🔐 **Advanced Auth** | Secure login with strong password policy, MX email validation & Google OAuth |
| 📚 **Knowledge Base** | 500+ verified Darija words integrated to prevent AI hallucinations |
| ⚡ **Performance** | MD5 response caching + token reduction for fast, reliable responses |
| 🔒 **Session Isolation** | Chat history fully isolated per user — auto-cleared on account switch |
| 🌐 **HuggingFace Ready** | Pre-configured Dockerfile for one-click Spaces deployment |

---

## 🛠️ Tech Stack

```
Backend  ──  Python 3.11 · Flask · CrewAI · Gunicorn
AI       ──  OpenRouter API · google/gemma-4-31b-it · Multi-Agent Architecture
Database ──  MongoDB Atlas (cloud) + JSON fallback (local)
Auth     ──  Google OAuth 2.0 · Session-based auth · MX DNS email validation
Frontend ──  HTML5 · Vanilla CSS (dark-mode) · JavaScript (ES6+)
Deploy   ──  Docker · Hugging Face Spaces
```

---

## 🚀 Quick Start

### 1 — Clone the repository
```bash
git clone https://github.com/zouinealifst-create/DarijaAgent.git
cd DarijaAgent
```

### 2 — Create & activate virtual environment
```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate
```

### 3 — Install dependencies
```bash
pip install -r requirements.txt
```

### 4 — Configure environment variables
Create a `.env` file at the project root:
```env
OPENROUTER_API_KEY=your_openrouter_key_here
GOOGLE_CLIENT_ID=your_google_client_id_here   # optional
MONGO_URI=your_mongodb_atlas_uri_here          # optional
```
> Get your OpenRouter key at: https://openrouter.ai/

### 5 — Run the app
```bash
python app.py
```

### 6 — Open in browser
```
http://localhost:7860
```

---

## 🐳 Hugging Face Deployment

This repo is **pre-configured** for Hugging Face Spaces:
1. Go to [huggingface.co/new-space](https://huggingface.co/new-space)
2. Choose **Docker** as your SDK
3. Link this GitHub repository
4. Add your secrets in Space Settings → Variables & Secrets
5. ✅ Done — it deploys automatically

---

## 🗂️ Project Structure

```
DarijaAgent/
├── static/
│   ├── index.html          # Landing page
│   ├── login.html          # Auth page (Email + Google OAuth)
│   ├── menu.html           # Mode selection
│   ├── chat.html           # AI chat interface
│   ├── quiz.html           # Quiz interface
│   ├── summary.html        # Session summary
│   └── app.js              # Session & UI state management
├── data/
│   └── darija_knowledge.json   # Anti-hallucination Darija KB (500+ words)
├── auth/
│   └── users.json          # Local user fallback store
├── agents.py               # CrewAI agents (Gemma 4 31B via OpenRouter)
├── tasks.py                # CrewAI task definitions
├── app.py                  # Flask server + caching + auth routes
├── main.py                 # Terminal/CLI version
├── tools.py                # Web scraper tools
├── Dockerfile              # Hugging Face Spaces config
├── requirements.txt        # Python dependencies
└── README.md
```

---

## 🔑 Demo Account

| Field | Value |
|-------|-------|
| Email | `demo@darija.ai` |
| Password | `demo1234` |

---

## ⚡ Performance Optimizations

| Optimization | Detail | Impact |
|-------------|--------|--------|
| Response Cache | MD5-hash in-memory cache | Instant on repeated questions |
| Token Reduction | `max_tokens` 400 → 200 | ~50% faster responses |
| Prompt Compression | 120 words → 30 words | 75% less processing |
| Timeout Guard | 15s hard timeout | No hanging requests |
| API Call Reduction | Cache hit avoids LLM call | ~40% fewer API requests |

---

## 🔐 Security

- **XSS Protection** — `bleach` input sanitization on all user inputs
- **SQL Injection Guards** — Pattern-based regex filtering
- **Disposable Email Blocklist** — 150+ temp-mail domains blocked
- **MX Record Validation** — Server-side DNS check on registration
- **Strong Password Policy** — Uppercase, lowercase, digit, symbol, 8+ chars
- **Session Isolation** — Each user gets isolated storage, auto-wiped on switch
- **Google OAuth** — Token verified server-side via Google's tokeninfo endpoint

---

## 👥 Team

<div align="center">

| | Name | GitHub |
|--|------|--------|
| 👨‍💻 | **Tarchi Oussama** | [![GitHub](https://img.shields.io/badge/@tarchi983-181717?style=flat-square&logo=github)](https://github.com/tarchi983) |
| 👨‍💻 | **Ali Zouine** | [![GitHub](https://img.shields.io/badge/@zouinealifst--create-181717?style=flat-square&logo=github)](https://github.com/zouinealifst-create) |
| 👨‍💻 | **Taha Rajel** | [![GitHub](https://img.shields.io/badge/@Taha--Rajel-181717?style=flat-square&logo=github)](https://github.com/Taha-Rajel) |

</div>

---

## 📝 Changelog

### v1.1 — November 2026
- 🔒 **Fixed**: Chat history isolation — user data fully wiped on account switch
- ⚡ **Fixed**: Slow responses after 2nd message — 50% token reduction + caching
- 🛡️ **Added**: Server-side MX email validation on registration
- 🧹 **Improved**: Error handling with 15s timeout guards

### v1.0 — Initial Release
- Core chat, quiz, and session summary
- Google OAuth + local JSON fallback
- MongoDB Atlas integration
- 500+ word Darija knowledge base

---

## 🤝 Contributing

```bash
# 1. Fork & clone
git checkout -b feature/your-feature

# 2. Develop & test
python -m py_compile app.py

# 3. Commit with clear messages
git commit -m "feat: your feature description"

# 4. Push & open a Pull Request
git push origin feature/your-feature
```

---

## 📄 License

This project is licensed under the **MIT License**.

---

<div align="center">

**Happy Learning Darija! 🇲🇦🎉**

*Built with ❤️ by Team DarijaAI*

</div>
