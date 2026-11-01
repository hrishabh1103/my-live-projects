# Video Analyzer

> Automated video content extraction, facial recognition, and OCR license plate parsing pipeline.

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | Video Analyzer |
| **Project Category** | AI & Machine Learning |
| **Current Status** | 🛠️ In Development |
| **Live Deployment URL** | *Pending Cloud Deployment / Pending Verification* |
| **GitHub Repository** | [hrishabh1103/VisionTrackai](https://github.com/hrishabh1103/VisionTrackai) |
| **Hosting Platform** | Target: Cloud Run |
| **Last Verified Date** | 2026-11-01 |

---

## 📝 Detailed Description

High-throughput computer vision analysis pipeline leveraging OpenCV, face_recognition, and EasyOCR for automated video indexing and scene transcription stored in Supabase.

---

## 🛠️ Technology Stack & Architecture

### Frontend
- **Framework & Libraries:** React, Vite

### Backend
- **Runtime & Frameworks:** Python, OpenCV

### Database & Storage
- **Primary Database:** Supabase PostgreSQL

### Third-Party APIs & Integrations
- **Services & Models:** face_recognition, EasyOCR, Supabase Storage

---

## 🚀 Deployment & Infrastructure Architecture

```
[User Browser]
       │
       ▼
[Edge CDN / Host (Target: Cloud Run)]
       │
       ▼
[Application Runtime]
       │
       ▼
[Database / External APIs (Supabase PostgreSQL)]
```

- **Hosting Platform:** Target: Cloud Run
- **Custom Domain:** None

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2026-11-01 | 🛠️ In Development | 200 OK | Health verified via ProjectVault deployment monitor. |

---

## 📌 Important Deployment & Operational Notes

Processes high-resolution video streams for facial landmarks and text recognition.
