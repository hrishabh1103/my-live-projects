# SavingsKaro

> Smart credit card discounts, rewards optimization, and consumer savings platform.

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | SavingsKaro (SavingsKaro 1.0) |
| **Project Category** | Personal Project / FinTech |
| **Current Status** | 🟢 Live |
| **Live Deployment URL** | [https://savingskaro.vercel.app/](https://savingskaro.vercel.app/) |
| **Secondary URL** | [https://savingskaro.netlify.app/](https://savingskaro.netlify.app/) *(404 - Deprecated in favor of Vercel)* |
| **GitHub Repository** | [hrishabh1103/Savingskaro1.0](https://github.com/hrishabh1103/Savingskaro1.0) |
| **Hosting Platform** | Vercel (Primary) / Netlify (Legacy target) |
| **Last Verified Date** | 2026-10-31 |

---

## 📝 Detailed Description

SavingsKaro is an intelligent consumer financial tool designed to maximize savings, cashback, and reward points across leading Indian credit cards (HDFC, SBI, ICICI, Axis, Amex):

- **Card Deal Aggregator:** Compares live merchant discounts across dining, travel, shopping, and fuel categories.
- **AI Savings Recommendation:** Evaluates user spending categories and automatically recommends the best credit card to maximize annual net returns.
- **Dynamic Savings Calculator:** Computes cashback percentages, joining fee waivers, milestone benefits, and real-time reward conversion values.
- **Modern Responsive UI:** Features dynamic typing animations, responsive cards, and clean categorized filtering.

---

## 🛠️ Technology Stack & Architecture

### Frontend
- **Framework:** React 18 (TypeScript)
- **State Management:** Zustand (v4.5) for global filter state and card comparison basket
- **Form Handling:** React Hook Form (v7.51)
- **Styling:** TailwindCSS 3.4, PostCSS, Class Variance Authority (`cva`), `clsx`, `tailwind-merge`
- **Animation:** Framer Motion (v11) & React Type Animation
- **Icons:** Lucide React
- **Build Tool:** Vite 5

### Backend & Integrations
- **AI Recommendation Engine:** OpenAI API client (`openai` v4.28)
- **Client Routing:** React Router DOM (v6.22)

### Database
- **Storage:** In-memory structured datasets + Zustand client-side persistent storage

---

## 🚀 Deployment & Infrastructure Architecture

```
[User Browser]
       │
       ▼
[Vercel Global Edge CDN]
       │
       ▼
[Single Page Application (Vite Build: dist/)]
       │
       ▼ (Optional AI Assistant Queries)
[OpenAI API Endpoint]
```

- **Deployment Mechanism:** Continuous Deployment from GitHub to Vercel
- **Build Command:** `npm run build` (`vite build`)
- **Output Directory:** `dist`

---

## 🔑 Environment Variables Checklist

*(No sensitive values are stored here. Variable names only.)*

| Variable Name | Purpose | Scope |
| :--- | :--- | :--- |
| `VITE_OPENAI_API_KEY` | OpenAI API Key for smart savings recommendation bot | Serverless Function / Client |

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2026-10-31 | 🟢 Live | 200 OK | Verified live endpoint at `https://savingskaro.vercel.app/` (HTTP 200 OK). Note: `savingskaro.netlify.app` returns 404, repository was successfully migrated and hosted on Vercel. |

---

## 📌 Important Deployment & Operational Notes

- **Hosting Platform Resolution:** Initially recorded as Netlify; verification revealed that the live production deployment is active on Vercel at `https://savingskaro.vercel.app/`.
- **Security Best Practice:** Ensure OpenAI API keys are accessed via secure backend proxy or serverless functions to avoid exposing client-side tokens.
