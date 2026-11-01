# Dr. Vishal Bhattacharya Clinic

> Full-stack Clinic Management System and patient operations platform deployed on Cloudflare Workers.

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | Dr. Vishal Bhattacharya Clinic |
| **Project Category** | Client Projects |
| **Current Status** | 🟢 Live |
| **Live Deployment URL** | [https://dr-vishal-clinic.hrishabhbase.workers.dev/](https://dr-vishal-clinic.hrishabhbase.workers.dev/) |
| **GitHub Repository** | [hrishabh1103/Dr_Bhattacharya_Clinic_Management_System](https://github.com/hrishabh1103/Dr_Bhattacharya_Clinic_Management_System) |
| **Hosting Platform** | Cloudflare Workers |
| **Last Verified Date** | 2024-08-15 |

---

## 📝 Detailed Description

End-to-end medical facility operations website built for a real-world healthcare provider. Streamlines daily outpatient department (OPD) workflows, scheduling, and patient record management. Deployed at the edge using OpenNext and Cloudflare Workers with Supabase PostgreSQL.

---

## 🛠️ Technology Stack & Architecture

### Frontend
- **Framework & Libraries:** Next.js 14, React, TailwindCSS, TypeScript

### Backend
- **Runtime & Frameworks:** OpenNext, Cloudflare Workers Runtime

### Database & Storage
- **Primary Database:** Supabase PostgreSQL

### Third-Party APIs & Integrations
- **Services & Models:** Supabase Auth, Supabase Realtime

---

## 🚀 Deployment & Infrastructure Architecture

```
[User Browser]
       │
       ▼
[Edge CDN / Host (Cloudflare Workers)]
       │
       ▼
[Application Runtime]
       │
       ▼
[Database / External APIs (Supabase PostgreSQL)]
```

- **Hosting Platform:** Cloudflare Workers
- **Custom Domain:** `dr-vishal-clinic.hrishabhbase.workers.dev`

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2024-08-15 | 🟢 Live | HTTP 200 | Health verified via ProjectVault deployment monitor. |

---

## 📌 Important Deployment & Operational Notes

Server-side logic runs on Cloudflare global edge network with sub-100ms response time.
