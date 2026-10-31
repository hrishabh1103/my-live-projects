# Contributing & Maintenance Guide

This document describes how to maintain, register, and update live project records in this directory.

---

## 🚀 How to Add a New Project

Whenever you deploy a new website, web application, or machine learning model, follow these steps:

### 1. Copy the Project Template
Copy the base template from `templates/project-template.md` to the appropriate subdirectory in `projects/`:
- **Client Projects:** `projects/client-projects/<project-slug>.md`
- **Personal Projects:** `projects/personal-projects/<project-slug>.md`
- **AI & ML Projects:** `projects/ai-ml-projects/<project-slug>.md`

```bash
cp templates/project-template.md projects/personal-projects/my-new-app.md
```

### 2. Fill in Project Information
Complete all sections in the markdown file:
- **Project Name** & Description
- **Live URL** (Must be a valid, accessible URL)
- **GitHub Repository** link
- **Hosting Platform** (e.g. Cloudflare Workers, Vercel, AWS, Render)
- **Technology Stack** (Frontend, Backend, Database, APIs)
- **Status Badge** (See Status System below)
- **Last Verified Date** (Set to the current date `YYYY-MM-DD`)

### 3. Update the Master Indexes
Add an entry for your new project in:
1. `README.md` (in the relevant category table and summary count)
2. `PROJECTS.md` (in the master directory table)

### 4. Verify Live Health
Before marking any project as **🟢 Live**, ensure that its public URL returns HTTP 200:
```bash
curl -I https://your-new-app.vercel.app/
```

---

## 🏷️ Project Status System

Always adhere strictly to these status standards:

| Status | Badge Code | Meaning |
| :--- | :--- | :--- |
| **🟢 Live** | `![Live](https://img.shields.io/badge/Status-Live-2ea44f?style=flat-square)` | Deployment is actively running, verified via HTTP 200. |
| **🟡 Needs Verification** | `![Needs Verification](https://img.shields.io/badge/Status-Needs%20Verification-dfb317?style=flat-square)` | Public URL exists or was noted, but has not yet been verified. |
| **🛠️ In Development** | `![In Development](https://img.shields.io/badge/Status-In%20Development-blue?style=flat-square)` | Actively being developed; local or staging builds only. |
| **🔴 Offline** | `![Offline](https://img.shields.io/badge/Status-Offline-d73a49?style=flat-square)` | Deployment confirmed unavailable or decommissioned. |
| **📦 Archived** | `![Archived](https://img.shields.io/badge/Status-Archived-lightgrey?style=flat-square)` | Repository is preserved for historical reference; no longer maintained. |

> **Rule:** Never mark an unverified URL or local-only project as 🟢 Live.

---

## 🔒 Security & Privacy Guidelines

- **NEVER** commit `.env`, `.env.local`, or any file containing secrets.
- **NEVER** hardcode private API keys, database connection strings, passwords, or Supabase service-role keys in markdown files.
- Only record environment variable **names** (keys) in the architecture checklists.
- Keep repository visibility aligned with the target project's licensing and client agreements.

---

## 🤖 Automated URL Health Check

This repository includes a scheduled GitHub Actions workflow (`.github/workflows/health-check.yml`) that runs weekly to ping all documented live URLs. If an endpoint returns an error or timeout, the action logs a status warning for review.
