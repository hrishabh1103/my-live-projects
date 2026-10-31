# Traviyaa

> Modern Indian travel and stay booking platform built with React, Vite, and Supabase, tailored as a culturally localized alternative to Airbnb.

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | Traviyaa (Traviya — An Indian Alternative to Airbnb) |
| **Project Category** | Client Project |
| **Current Status** | 🟢 Live |
| **Live Deployment URL** | [https://traviyaa.vercel.app/](https://traviyaa.vercel.app/) |
| **GitHub Repository** | [hrishabh1103/Traviya-an-Indian-alternative-to-AirBnB-](https://github.com/hrishabh1103/Traviya-an-Indian-alternative-to-AirBnB-) |
| **Pre-Production Repo** | [hrishabh1103/Traviya-PreProductionBuild](https://github.com/hrishabh1103/Traviya-PreProductionBuild) |
| **Hosting Platform** | Vercel Edge Network |
| **Last Verified Date** | 2026-10-31 |

---

## 📝 Detailed Description

Traviyaa is a localized hospitality and travel booking web application designed specifically for Indian travelers and homestay hosts. It offers:

- **Curated Indian Homestays & Heritage Properties:** Listings of authentic havelis, hill station cottages, beachside homestays, and spiritual retreats across popular Indian destinations (e.g., Rajasthan, Himachal, Kerala, Goa).
- **Interactive Search & Discovery:** Filter stays by state, city, budget, amenities (pure-veg kitchen, pet-friendly, private pool), and accommodation type.
- **Booking & Reservation Interface:** Seamless booking calendar with real-time availability checks, transparent pricing breakdowns, and guest booking workflows.
- **Host Onboarding Experience:** Intuitive form for property hosts to publish listings, upload high-resolution photos, and set custom night rates.

---

## 🛠️ Technology Stack & Architecture

### Frontend
- **Framework:** React 18 (TypeScript)
- **Routing:** React Router DOM (v7)
- **Styling:** TailwindCSS with PostCSS and custom responsive design
- **Icons & Assets:** Lucide React
- **Build Tool:** Vite 5 (Fast ESM bundling and optimized production chunking)

### Backend & Database
- **BaaS Platform:** Supabase
- **Database:** PostgreSQL (with tables for properties, hosts, bookings, and reviews)
- **Client Library:** `@supabase/supabase-js` (v2.57+)
- **Storage:** Supabase Storage for property gallery images

### Third-Party APIs & Services
- **Hosting CDN:** Vercel Global Edge Network
- **Authentication:** Supabase Auth (Email & OAuth sign-in)

---

## 🚀 Deployment & Infrastructure Architecture

```
[User Browser]
       │
       ▼
[Vercel Edge Network (Global CDN / DNS)]
       │
       ▼
[Vercel Serverless Static Bundle (Vite Build)]
       │
       ▼
[Supabase Backend (PostgreSQL + REST API + Auth)]
```

- **Deployment Mechanism:** Automatic Vercel Git integration on push to `main`
- **Build Command:** `vite build`
- **Output Directory:** `dist`

---

## 🔑 Environment Variables Checklist

*(No sensitive values are stored here. Variable names only.)*

| Variable Name | Purpose | Scope |
| :--- | :--- | :--- |
| `VITE_SUPABASE_URL` | Supabase Project API endpoint | Client Vite Build |
| `VITE_SUPABASE_ANON_KEY` | Supabase Public Anonymous API key | Client Vite Build |

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2026-10-31 | 🟢 Live | 200 OK | Verified live endpoint at `https://traviyaa.vercel.app/`. Returns HTTP 200 OK with full interactive catalog. |

---

## 📌 Important Deployment & Operational Notes

- **URL Discovery:** Previously marked as pending verification; discovered live production URL is `https://traviyaa.vercel.app/` alongside pre-production preview build.
- **SPA Routing:** Configured `vercel.json` rewrite rules (`"source": "/(.*)", "destination": "/index.html"`) to prevent 404s on deep links.
