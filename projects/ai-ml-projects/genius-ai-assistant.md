# Genius AI Assistant

> Voice-enabled multimodal conversational AI assistant with real-time speech recognition and LLM inference.

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | Genius AI Assistant |
| **Project Category** | AI & Machine Learning |
| **Current Status** | 🟢 Live |
| **Live Deployment URL** | [https://minor-project02-genius-ai-assistant-lake.vercel.app/](https://minor-project02-genius-ai-assistant-lake.vercel.app/) |
| **GitHub Repository** | [hrishabh1103/Minor_Project02_Genius_Ai_Assistant](https://github.com/hrishabh1103/Minor_Project02_Genius_Ai_Assistant) |
| **Hosting Platform** | Vercel / Local |
| **Last Verified Date** | 2024-11-12 |

---

## 📝 Detailed Description

Multimodal conversational assistant equipped with offline Vosk speech-to-text, real-time WebSocket communication, and Google Gemini API / OpenRouter fallbacks.

---

## 🛠️ Technology Stack & Architecture

### Frontend
- **Framework & Libraries:** React, TailwindCSS, Socket.IO Client

### Backend
- **Runtime & Frameworks:** Flask, Flask-SocketIO, Python

### Database & Storage
- **Primary Database:** Redis / SQLite

### Third-Party APIs & Integrations
- **Services & Models:** Gemini API, Vosk STT Engine, OpenRouter

---

## 🚀 Deployment & Infrastructure Architecture

```
[User Browser]
       │
       ▼
[Edge CDN / Host (Vercel / Local)]
       │
       ▼
[Application Runtime]
       │
       ▼
[Database / External APIs (Redis / SQLite)]
```

- **Hosting Platform:** Vercel / Local
- **Custom Domain:** None

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2024-11-12 | 🟢 Live | HTTP 200 | Health verified via ProjectVault deployment monitor. |

---

## 📌 Important Deployment & Operational Notes

Bidirectional audio streaming pipeline with WebSocket protocol.
