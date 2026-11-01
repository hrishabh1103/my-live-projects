# Customer Support Bot

> RAG-powered conversational support chatbot with vector similarity matching and semantic retrieval.

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | Customer Support Bot |
| **Project Category** | AI & Machine Learning |
| **Current Status** | 🛠️ In Development |
| **Live Deployment URL** | *Pending Cloud Deployment / Pending Verification* |
| **GitHub Repository** | [hrishabh1103/Pabbly_ChatBot](https://github.com/hrishabh1103/Pabbly_ChatBot) |
| **Hosting Platform** | Target: Railway |
| **Last Verified Date** | 2026-11-01 |

---

## 📝 Detailed Description

Enterprise Retrieval-Augmented Generation (RAG) assistant utilizing FastAPI, ChromaDB vector indexing, and SentenceTransformers for instant context-aware document queries.

---

## 🛠️ Technology Stack & Architecture

### Frontend
- **Framework & Libraries:** Next.js, TailwindCSS

### Backend
- **Runtime & Frameworks:** FastAPI, Python, Uvicorn

### Database & Storage
- **Primary Database:** ChromaDB

### Third-Party APIs & Integrations
- **Services & Models:** SentenceTransformers, Hugging Face Hub

---

## 🚀 Deployment & Infrastructure Architecture

```
[User Browser]
       │
       ▼
[Edge CDN / Host (Target: Railway)]
       │
       ▼
[Application Runtime]
       │
       ▼
[Database / External APIs (ChromaDB)]
```

- **Hosting Platform:** Target: Railway
- **Custom Domain:** None

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2026-11-01 | 🛠️ In Development | 200 OK | Health verified via ProjectVault deployment monitor. |

---

## 📌 Important Deployment & Operational Notes

Embeddings cached in ChromaDB with semantic reranking for sub-200ms query retrieval.
