# Dr. Vishal Bhattacharya Clinic

> Full-stack Clinic Management System and patient operations platform deployed on Cloudflare Workers using OpenNext.

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | Dr. Vishal Bhattacharya Clinic Management System |
| **Project Category** | Client Project |
| **Current Status** | 🟢 Live |
| **Live Deployment URL** | [https://dr-vishal-clinic.hrishabhbase.workers.dev/](https://dr-vishal-clinic.hrishabhbase.workers.dev/) |
| **GitHub Repository** | [hrishabh1103/Dr_Bhattacharya_Clinic_Management_System](https://github.com/hrishabh1103/Dr_Bhattacharya_Clinic_Management_System) |
| **Hosting Platform** | Cloudflare Workers (Serverless Edge) |
| **Last Verified Date** | 2026-10-31 |

---

## 📝 Detailed Description

Dr. Vishal Bhattacharya Clinic Management System is an end-to-end medical facility operations website built for a real-world healthcare provider. The system streamlines daily outpatient department (OPD) workflows, scheduling, and record-keeping:

- **Patient Self-Service Portal:** Online appointment scheduling, doctor availability lookup, clinic timings, and consultation request submissions.
- **Doctor & Staff Portal:** Authenticated administrative dashboard for managing patient queues, viewing medical history, writing digital prescriptions, and logging visit notes.
- **Clinic Operations:** Front-desk reception coordination, appointment status tracking (Pending, Confirmed, Completed, Cancelled), and daily billing summaries.
- **Edge Performance:** Sub-100ms global latency achieved by running server-side logic directly on Cloudflare's global edge network.

---

## 🛠️ Technology Stack & Architecture

### Frontend
- **Framework:** Next.js 14+ (App Router, TypeScript)
- **Styling:** TailwindCSS, PostCSS, Lucide Icons
- **UI Components:** Custom accessible forms, modals, status tags, and responsive tables
- **Optimization:** Automatic asset optimization via OpenNext static assets bundler

### Backend
- **Runtime:** Cloudflare Workers V8 JavaScript runtime with `nodejs_compat`
- **Adapter:** OpenNext (`open-next.config.ts`, `.open-next/worker.js`)
- **API Routes:** Next.js Server Actions and Route Handlers

### Database & Security
- **Database:** Supabase (Managed PostgreSQL)
- **Authentication:** Supabase Auth (Role-based access for Doctors, Staff, and Patients)
- **Data Protection:** PostgreSQL Row-Level Security (RLS) policies protecting sensitive medical records

### Third-Party APIs & Services
- **Hosting / Edge CDN:** Cloudflare Workers
- **Database / Auth:** Supabase
- **Configuration:** `wrangler.json` (Compatibility date: 2024-09-23)

---

## 🚀 Deployment & Infrastructure Architecture

```
[Patient / Doctor Browser]
            │
            ▼
[Cloudflare Global Edge Anycast Network]
            │
            ▼
[Cloudflare Worker (.open-next/worker.js)]
       │                          │
       ▼                          ▼
[.open-next/assets]      [Supabase PostgreSQL (Database + Auth)]
 (Static CSS / JS / Images)
```

- **Deployment Mechanism:** Wrangler CLI / GitHub deployment via Cloudflare Workers
- **Build Pipeline:** `npm run build` -> `npx open-next build` -> `wrangler deploy`
- **Entrypoint:** `.open-next/worker.js` with static binding to `.open-next/assets`

---

## 🔑 Environment Variables Checklist

*(No sensitive values are stored here. Variable names only.)*

| Variable Name | Purpose | Scope |
| :--- | :--- | :--- |
| `NEXT_PUBLIC_SUPABASE_URL` | Supabase API URL endpoint | Client & Worker |
| `NEXT_PUBLIC_SUPABASE_ANON_KEY` | Supabase public anonymous access key | Client & Worker |
| `SUPABASE_SERVICE_ROLE_KEY` | Administrative service key for backend migrations | Secure Server |

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2026-10-31 | 🟢 Live | 200 OK | Verified live endpoint on Cloudflare Workers; homepage and appointment UI render with 200 OK. |

---

## 📌 Important Deployment & Operational Notes

- **OpenNext Architecture:** Next.js is transformed into Cloudflare Worker bundle using OpenNext to support SSR and API routes at edge cost-efficiency.
- **Database Connectivity:** Uses Supabase connection pooling (port 6543 / PgBouncer or direct HTTPS REST) to handle transient serverless connections from Cloudflare Workers without exhausting database sockets.
