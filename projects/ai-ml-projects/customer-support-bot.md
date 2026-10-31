# Customer Support Bot (Pabbly ChatBot)

> Intelligent customer support chatbot utilizing ChromaDB vector search, SentenceTransformers embeddings, and Hugging Face Flan-T5 text generation.

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | Customer Support Bot (Pabbly ChatBot) |
| **Project Category** | AI & Machine Learning Project |
| **Current Status** | 🛠️ In Development (Ready for Cloud Deployment) |
| **Live Deployment URL** | *Pending Public API Deployment* |
| **GitHub Repository** | [hrishabh1103/Pabbly_ChatBot](https://github.com/hrishabh1103/Pabbly_ChatBot) |
| **Hosting Platform** | Local Server (Target: Render / Railway / Google Cloud Run) |
| **Last Verified Date** | 2026-10-31 |

---

## 📝 Detailed Description

Customer Support Bot is a Retrieval-Augmented Generation (RAG) support assistant engineered to resolve customer inquiries, sales questions, and technical troubleshooting queries for SaaS platforms (demonstrated with Pabbly FAQ datasets):

- **Domain Knowledge Ingestion:** Automatically parses CSV/Excel FAQ repositories (`Support FAQ.csv`, `Sales FAQ.csv`) and generates structured vector embeddings.
- **Semantic Similarity Search:** Leverages `SentenceTransformers` (`all-MiniLM-L6-v2`) and ChromaDB vector store to locate exact and contextually similar support resolutions regardless of user phrasing.
- **Contextual Answer Synthesis:** Feeds retrieved relevant FAQ contexts into Hugging Face `google/flan-t5-base` text-to-text generative pipeline for natural, human-like answers.
- **RESTful API Service:** FastAPI backend exposing `/chat` endpoint with asynchronous query processing.

---

## 🛠️ Technology Stack & Architecture

### Backend & API
- **Framework:** FastAPI / Python 3.10+
- **ASGI Server:** Uvicorn
- **API Protocols:** REST HTTP JSON endpoints

### AI, NLP & Vector Database
- **Embeddings:** `sentence-transformers` (`all-MiniLM-L6-v2`)
- **Vector Database:** `chromadb` persistent collection storage
- **Generative LLM:** Hugging Face `transformers` pipeline (`google/flan-t5-base`)
- **Similarity Metric:** Scikit-learn cosine similarity calculation

### Frontend
- **Interface:** Lightweight embedded chat widget (HTML5 / CSS3 / JavaScript)

---

## 🚀 Deployment & Infrastructure Architecture

```
[Customer Support Widget]
            │
    (POST /chat)
            │
            ▼
[FastAPI Backend Service]
            │
            ▼
[SentenceTransformer Embedding Generator]
            │
            ▼
[ChromaDB Vector Search (Semantic Retrieval)]
            │
            ▼
[Hugging Face Flan-T5 (Context-grounded Generation)]
            │
            ▼
[Structured Response to User]
```

- **Deployment Status:** Functional backend pipeline with persistent vector database; ready for single-container Docker deployment on serverless platforms.

---

## 🔑 Environment Variables Checklist

*(No sensitive values are stored here. Variable names only.)*

| Variable Name | Purpose | Scope |
| :--- | :--- | :--- |
| `HUGGINGFACE_HUB_TOKEN` | Hugging Face token for accelerated model downloading | Backend runtime |
| `PORT` | Web service listener port (default: 8000) | Server environment |

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2026-10-31 | 🛠️ In Development | N/A | Codebase complete on GitHub (`Pabbly_ChatBot`); embedding pipeline and ChromaDB integration verified. |

---

## 📌 Important Deployment & Operational Notes

- **Model Caching:** During initial container boot, pre-cache `all-MiniLM-L6-v2` and `google/flan-t5-base` weights in Docker build stage to minimize cold-start latency.
- **Vector Index:** ChromaDB database directory (`chroma_db/`) should be mounted to persistent volume or initialized at deployment time from `Support FAQ.csv`.
