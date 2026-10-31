# Video Analyzer (VisionTrack AI)

> Automated video intelligence platform combining OpenCV, face_recognition, EasyOCR, and Supabase for real-time entity tracking and plate recognition.

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | Video Analyzer (VisionTrack AI) |
| **Project Category** | AI & Machine Learning Project |
| **Current Status** | 🛠️ In Development (Demo & Academic Ready) |
| **Live Deployment URL** | *Pending Cloud Deployment / Local Demo* |
| **GitHub Repository** | [hrishabh1103/VisionTrackai](https://github.com/hrishabh1103/VisionTrackai) |
| **Hosting Platform** | Localhost / Demo Server (Target: Render / Cloud Run) |
| **Last Verified Date** | 2026-10-31 |

---

## 📝 Detailed Description

VisionTrack AI is a computer vision and video analytics platform engineered for automated surveillance, security monitoring, and forensic video investigation:

- **Computer Vision Face Detection:** Scans video streams frame-by-frame using deep learning face recognition algorithms, extracting facial landmarks and matching against identity databases.
- **License Plate OCR:** Utilizes EasyOCR for high-accuracy text extraction from vehicle plates with pattern validation and perspective correction.
- **Entity Timeline Tracking:** Groups similar detected faces and vehicles across video timelines, compiling timestamped event logs with confidence scores.
- **Modern Dashboard UI:** Built with React, Vite, and TailwindCSS to provide side-by-side video playback, detection heatmaps, and bounding-box overlays.

---

## 🛠️ Technology Stack & Architecture

### Frontend
- **Framework:** React 18 (TypeScript)
- **Styling:** TailwindCSS, PostCSS, Autoprefixer
- **Build Tool:** Vite 5 with ESLint configuration
- **Components:** Video playback canvas, frame timeline scrubber, detection log table

### Backend & AI Pipeline
- **Runtime:** Python 3.10+
- **Computer Vision:** OpenCV (`cv2`)
- **Face Recognition:** `face_recognition` (dlib C++ backend)
- **Optical Character Recognition:** `EasyOCR` (PyTorch backend)

### Database & Storage
- **Database:** Supabase (PostgreSQL) for detection events, timestamps, and identity registries
- **Media Storage:** Supabase Storage bucket for cropped detection thumbnails

---

## 🚀 Deployment & Infrastructure Architecture

```
[Video Stream / Upload File]
              │
              ▼
[Python Processing Pipeline (OpenCV + face_recognition + EasyOCR)]
              │
      ┌───────┴───────┐
      ▼               ▼
[Supabase DB]   [Supabase Storage]
 (Logs & Meta)   (Detection Crops)
      │               │
      └───────┬───────┘
              ▼
[React + Vite Frontend Dashboard]
```

- **Deployment Status:** Local development and demonstration build ready; containerized Docker deployment recommended for GPU-enabled cloud nodes.

---

## 🔑 Environment Variables Checklist

*(No sensitive values are stored here. Variable names only.)*

| Variable Name | Purpose | Scope |
| :--- | :--- | :--- |
| `VITE_SUPABASE_URL` | Supabase API URL endpoint | Frontend Vite build |
| `VITE_SUPABASE_ANON_KEY` | Supabase Public Anonymous API key | Frontend Vite build |
| `SUPABASE_SERVICE_ROLE_KEY` | Supabase service key for video worker ingestion | Backend Python script |

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2026-10-31 | 🛠️ In Development | N/A | Codebase complete on GitHub (`VisionTrackai`); local demo operational; public cloud URL pending container deployment. |

---

## 📌 Important Deployment & Operational Notes

- **Hardware Acceleration:** The `face_recognition` (dlib) and `EasyOCR` engines benefit from CUDA GPU acceleration when deployed in production.
- **Cloud Hosting Recommendation:** Deploy backend on Google Cloud Run with GPU or an AWS EC2 `g4dn` instance for real-time video stream ingestion.
