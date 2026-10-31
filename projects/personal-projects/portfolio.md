# Personal Portfolio (3D Interactive)

> Immersive 3D software engineering portfolio built with Three.js, React Three Fiber, Framer Motion, and TailwindCSS.

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | Personal Portfolio Website (Hrishabh Gupta) |
| **Project Category** | Personal Project |
| **Current Status** | 🟢 Live |
| **Live Deployment URL** | [https://hrishabhgupt.vercel.app/](https://hrishabhgupt.vercel.app/) |
| **GitHub Repository** | [hrishabh1103/Profession_portfolio](https://github.com/hrishabh1103/Profession_portfolio) |
| **Alternate Mirrors** | [hrishabh1103/profile.website](https://github.com/hrishabh1103/profile.website) |
| **Hosting Platform** | Vercel |
| **Last Verified Date** | 2026-10-31 |

---

## 📝 Detailed Description

The flagship personal portfolio website of **Hrishabh Gupta**, highlighting full-stack engineering, AI/ML expertise, and distributed systems capabilities. Key features include:

- **3D Canvas & WebGL Visuals:** Interactive 3D desktop workstation canvas and floating spatial objects rendered using WebGL via Three.js.
- **Fluid Micro-Interactions:** Smooth page animations, tilt cards via `react-parallax-tilt`, and staggered reveal transitions powered by Framer Motion.
- **Experience Timeline:** Interactive vertical timeline documenting education, engineering roles, and hackathon accomplishments via `react-vertical-timeline-component`.
- **Project Showcase:** Filterable gallery displaying live deployed projects, GitHub links, and technology tags.
- **Contact Integration:** Functional messaging form connected directly to EmailJS for instant client/recruiter outreach.

---

## 🛠️ Technology Stack & Architecture

### Frontend
- **3D Graphics Engine:** Three.js, `@react-three/fiber`, `@react-three/drei`, `maath`
- **Framework:** React 18 (TypeScript)
- **Animation:** Framer Motion (v9)
- **Styling:** TailwindCSS, PostCSS, Autoprefixer
- **UI Components:** `react-parallax-tilt`, `react-vertical-timeline-component`, `react-icons`
- **Build Tool:** Vite 5 with TypeScript compiler

### Backend & Database
- **Backend:** Not Applicable (Jamstack Serverless Architecture)
- **Database:** Not Applicable

### Third-Party APIs & Services
- **Hosting:** Vercel Global Edge CDN
- **Contact Email Delivery:** EmailJS (`@emailjs/browser`)

---

## 🚀 Deployment & Infrastructure Architecture

```
[Visitor Browser]
       │
       ▼
[Vercel Global Edge Network]
       │
       ▼
[Vite Optimized Static Bundle (HTML / WebGL Canvas / JS Chunks)]
       │
       ▼ (Contact Form Submission)
[EmailJS REST Gateway -> Direct Inbox Delivery]
```

- **Deployment Mechanism:** Continuous Deployment from GitHub `main` branch to Vercel
- **Build Command:** `tsc && vite build`
- **Output Directory:** `dist`

---

## 🔑 Environment Variables Checklist

*(No sensitive values are stored here. Variable names only.)*

| Variable Name | Purpose | Scope |
| :--- | :--- | :--- |
| `VITE_APP_EMAILJS_SERVICE_ID` | EmailJS service configuration identifier | Public Client |
| `VITE_APP_EMAILJS_TEMPLATE_ID`| EmailJS contact form template identifier | Public Client |
| `VITE_APP_EMAILJS_PUBLIC_KEY` | EmailJS public client authorization key | Public Client |

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2026-10-31 | 🟢 Live | 200 OK | Verified live endpoint at `https://hrishabhgupt.vercel.app/`. Returns 200 OK with fully functional 3D canvas and animations. |

---

## 📌 Important Deployment & Operational Notes

- **WebGL Performance:** GLTF/GLB 3D assets are compressed using Draco compression to maintain fast initial loading speeds across mobile and desktop connections.
- **Vercel Caching:** Static assets are configured with immutable cache headers for peak Lighthouse performance.
