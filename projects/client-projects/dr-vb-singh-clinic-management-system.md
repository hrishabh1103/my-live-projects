# Dr VB Singh Clinic Management System

> A modern, production-grade Next.js clinic management and queue platform customized for **Dr. V. B. Singh** (Orthopedic, Ligament, Sports Injury & Arthroscopy Surgeon in Rewa, Madhya Pradesh).

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | Dr VB Singh Clinic Management System |
| **Project Category** | Client Projects |
| **Current Status** | 🟢 Live |
| **Live Deployment URL** | [https://dr-vb-singh-clinic.drvbsinghclinic.workers.dev/](https://dr-vb-singh-clinic.drvbsinghclinic.workers.dev/) |
| **GitHub Repository** | [hrishabh1103/Dr_VB_Singh_Clinic_Management](https://github.com/hrishabh1103/Dr_VB_Singh_Clinic_Management) |
| **Hosting Platform** | Cloudflare Workers |
| **Last Verified Date** | 2026-11-06 |

---

## 📝 Detailed Description

## 🌟 Key Features

### 1. 🏥 Patient-Facing Portal & Online Booking
- **Smart Appointment Booking**: Real-time slot booking with morning and evening OPD shifts.
- **Patient Health Record Portal**: Dedicated `/patient` portal where patients log in via mobile number or patient ID to view and download digital prescriptions, lab reports, radiology X-rays, and prescription slips.
- **One-Click Demo Patient Logins**: Built-in instant login buttons for testing and demonstration.
- **Live Waiting Queue**: Public token tracker at `/live-queue` showing current serving token and estimated waiting time.

### 2. 👩‍💼 Receptionist Desk & Queue Management (`/admin/reception`)
- **Queue Operations**: Call Next, Mark Waiting, Complete Consult, or Delay tokens.
- **Walk-in OPD Registration**: Generate instant tokens for emergency and walk-in patients.
- **📷 Prescription Photo Capture**:
  - Direct live camera capture (via device webcam or mobile back camera).
  - High-resolution file upload for printed prescriptions and diagnostic slips.
  - Automatic compression and attachment to the patient's medical records.
  - Instant visibility in the patient's portal and doctor's panel.

### 3. 💰 Billing & Total Earnings Dashboard (`/admin/earnings`)
- **Live Financial KPIs**:
  - Today's Total Collections & Gross Charges.
  - Estimated Monthly OPD & Surgical Revenue.
  - Standard Orthopedic OPD Consultation Fee tracker.
- **Payment Distribution**: Breakdown by UPI/QR, Cash, Card/POS, and Bank Transfer.
- **Orthopedic Fee Catalog**: Standard pricing for OPD Consultations, X-Rays, Joint Injections, Casts/Braces, and Surgery Deposits.
- **Patient Payment Ledger**: Searchable, filterable transaction history.
- **Interactive Fee Collection**: Fast `+ Collect Fee / Add Bill` modal with automated balance tracking.
- **Printable Receipts**: Professional branded receipts with clinic details, patient info, and payment breakdown.

### 4. 🩺 Doctor Calling & Clinical Console (`/admin/doctor-panel`)
- Next-patient calling interface with audio chime.
- Real-time patient medical history and uploaded documents preview.
- Digital Rx Prescription builder with orthopedics medication catalog and dosage presets.

### 5. 📺 Waiting Room TV Display (`/queue-display`)
- High-contrast, large-format full-screen queue display for clinic TV monitors.
- Token announcements with sound and flash effects.

---

## 🛠️ Tech Stack
- **Framework**: Next.js 15 (App Router), React 19, TypeScript
- **Styling**: Tailwind CSS, Lucide Icons, Canvas Confetti
- **Charts**: Recharts
- **Database & Storage**: Supabase (PostgreSQL) with seamless Offline-First Local Mock Database fallback

---

## 🚀 Getting Started

### 1. Install Dependencies
```bash
npm install
```

### 2. Run Local Development Server
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

### 3. Production Build
```bash
npm run build
npm start
```

-

---

## 🛠️ Technology Stack & Architecture

### Frontend
- **Framework & Libraries:** React, TypeScript, Tailwind CSS

### Backend
- **Runtime & Frameworks:** Node.js

### Database & Storage
- **Primary Database:** Supabase

### Third-Party APIs & Integrations
- **Services & Models:** Gemini API

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
[Database / External APIs (Supabase)]
```

- **Hosting Platform:** Cloudflare Workers
- **Custom Domain:** None

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2026-11-06 | 🟢 Live | 200 OK | Health verified via ProjectVault deployment monitor. |

---

## 📌 Important Deployment & Operational Notes

- System deployment verified and cataloged via ProjectVault.
