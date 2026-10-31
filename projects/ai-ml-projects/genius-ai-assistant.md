# Genius AI Assistant

> Multimodal, voice-controlled AI assistant with multilingual speech recognition, Gemini API, OpenRouter, and real-time interaction.

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | Genius AI Assistant (Minor Project 02 / Jarvis) |
| **Project Category** | AI & Machine Learning Project |
| **Current Status** | 🟢 Live (Frontend Interface Deployed) |
| **Live Deployment URL** | [https://minor-project02-genius-ai-assistant-lake.vercel.app/](https://minor-project02-genius-ai-assistant-lake.vercel.app/) |
| **Mirror Deployment** | [https://genius-ai-minor-project.vercel.app/](https://genius-ai-minor-project.vercel.app/) |
| **GitHub Repository** | [hrishabh1103/Minor_Project02_Genius_Ai_Assistant](https://github.com/hrishabh1103/Minor_Project02_Genius_Ai_Assistant) |
| **Related Repositories**| [hrishabh1103/Jarvis.build](https://github.com/hrishabh1103/Jarvis.build) · [hrishabh1103/Genius_Ai_Summarizer](https://github.com/hrishabh1103/Genius_Ai_Summarizer) |
| **Hosting Platform** | Vercel (Frontend) · Self-hosted / Local Server (Python & Node Backend) |
| **Last Verified Date** | 2026-10-31 |

---

## 📝 Detailed Description

Genius AI Assistant is an interactive AI companion combining real-time speech processing with cutting-edge Large Language Models. Built as an academic and practical demonstration for B.Tech Computer Science (Data Science specialization):

- **Voice Interaction & Speech Recognition:** Integrated Vosk offline speech recognition and Google SpeechRecognition for hands-free queries.
- **Multilingual Support:** Automatic language detection using `langdetect` with native support for English and Hindi commands and conversational replies.
- **Dual LLM Integrations:** Connects with Google Gemini API (`@google/generative-ai`) and OpenRouter for ultra-low-latency response generation.
- **Voice Control & System Actions:** Capable of opening applications, playing media, answering factual questions, and managing reminders.
- **Modern Dashboard UI:** Built with drag-and-drop task widgets (`@hello-pangea/dnd`), real-time socket updates, and audio visualization.

---

## 🛠️ Technology Stack & Architecture

### Frontend
- **Framework:** React 18 (TypeScript)
- **State Management:** Zustand
- **Widgets & DnD:** `@hello-pangea/dnd`, `date-fns`
- **Networking:** Socket.io client (`socket.io-client` v4.8)
- **Styling:** TailwindCSS, PostCSS, Lucide React
- **Build Tool:** Vite 5

### Backend
- **Python Backend:** Flask, `Flask-Cors`, `Flask-SocketIO`
- **Speech Engine:** Vosk Speech Recognizer / `SpeechRecognition`
- **Node.js Gateway:** Express.js (`server.js`) with CORS and dotenv
- **Language Detection:** `langdetect`

### AI & Third-Party APIs
- **LLM APIs:** Google Gemini API (`@google/generative-ai`), OpenRouter API (OpenAI client)
- **Text-to-Speech:** Native Web Speech API / Python TTS engine

---

## 🚀 Deployment & Infrastructure Architecture

```
[User Microphone / Browser]
            │
    (WebSockets / HTTP)
            │
            ▼
[Vercel Frontend CDN (Vite React Build)]
            │
            ▼
[Python / Node Backend (server.py / server.js)]
       │                      │
       ▼                      ▼
[Speech Recognition]     [Gemini / OpenRouter LLM]
```

- **Frontend Deployment:** Vercel Continuous Deployment
- **Backend Runtime:** Python 3.10+ virtual environment / Node runtime

---

## 🔑 Environment Variables Checklist

*(No sensitive values are stored here. Variable names only.)*

| Variable Name | Purpose | Scope |
| :--- | :--- | :--- |
| `GEMINI_API_KEY` | Google Gemini API secret key | Server-side |
| `OPENROUTER_API_KEY` | OpenRouter API authentication key | Server-side |
| `PORT` | Local or production backend listener port | Server environment |

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2026-10-31 | 🟢 Live | 200 OK | Verified live frontend deployment at `https://minor-project02-genius-ai-assistant-lake.vercel.app/` (HTTP 200 OK). Mirror at `https://genius-ai-minor-project.vercel.app/` also verified HTTP 200. |

---

## 📌 Important Deployment & Operational Notes

- **Full Voice Functionality:** Requires the local Python speech bridge (`python server.py`) or deployed WebSocket container to process raw audio input and mic streams.
