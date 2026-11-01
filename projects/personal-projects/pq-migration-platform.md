# PQ_Migration Platform

> An enterprise-grade cryptographic discovery, inventory normalization, cross-cloud correlation, PQC risk assessment, and Cryptographic Bill of Materials (CBOM) generation platform supporting AWS, Azure, Kubernetes, Linux, Network Endpoints (TLS/SSH), and Application Source Code.

---

## 📌 Project Overview

| Property | Value |
| :--- | :--- |
| **Project Name** | PQ_Migration Platform |
| **Project Category** | Personal Projects |
| **Current Status** | 🛠️ In Development |
| **Live Deployment URL** | *Pending Cloud Deployment / Pending Verification* |
| **GitHub Repository** | [hrishabh1103/PQ_Migration](https://github.com/hrishabh1103/PQ_Migration) |
| **Hosting Platform** | Pending |
| **Last Verified Date** | 2026-11-01 |

---

## 📝 Detailed Description

Phase 1 Production-Grade Repository Discovery — COMPLETE — The authoritative repository discovery layer has been fully hardened and verified against all Phase 0 architectural conditions:

Zero FP Regressions Against Curated Negative Corpus: Scoped and enforced CI regression suite across multi-language AST parsers (Python, JS/TS, Go, Java, Rust) with string-literal stripping to guarantee zero false positives from comments, documentation, and non-crypto identifiers.
Tier 1 & Tier 2 Container Isolation: Implemented application sandbox controls (resource.setrlimit CPU/memory limits, socket network blocking, zip-slip defense) and container isolation in docker-compose.yml / Dockerfile.worker (cap_drop: [ALL], read_only: true, unprivileged uid: 10001, tmpfs mounts, memory cgroups) with complete threat modeling in SECURITY.md.
Tamper-Evident Evidence Chaining at Scale: Lock-free intra-scan SHA-256 hash chains across concurrent scans, atomically anchored into tenant append-only ledgers (TenantEvidenceAnchor), verified via POST /api/v1/evidence/verify.
Zero-Storage Secret Engine: Enforced SHA-256 fingerprinting and automatic snippet masking (AKIA****************, [REDACTED]) with zero plaintext secrets stored in DB or logs.
Observability & Diagnostics: Added GET /api/v1/scans/{id}/diagnostics and updated /api/v1/health status codes (healthy/degraded -> HTTP 200, unhealthy -> HTTP 503).
16/16 Phase 1 Tests Passing: Comprehensive unit and integration test coverage across AST parsing, secret detection, evidence verification, data residency routing, and API workflows. Frontend production build (npm run build) passing cleanly.

---

## 🛠️ Technology Stack & Architecture

### Frontend
- **Framework & Libraries:** TypeScript, Tailwind CSS, React, HTML5

### Backend
- **Runtime & Frameworks:** Node.js, Python

### Database & Storage
- **Primary Database:** Supabase

### Third-Party APIs & Integrations
- **Services & Models:** Supabase Auth

---

## 🚀 Deployment & Infrastructure Architecture

```
[User Browser]
       │
       ▼
[Edge CDN / Host (Cloudflare / Vercel)]
       │
       ▼
[Application Runtime]
       │
       ▼
[Database / External APIs (Supabase)]
```

- **Hosting Platform:** Pending
- **Custom Domain:** None

---

## 📋 Verification & Health History

| Date | Checked Status | HTTP Code | Notes |
| :--- | :--- | :--- | :--- |
| 2026-11-01 | 🛠️ In Development | 200 OK | Health verified via ProjectVault deployment monitor. |

---

## 📌 Important Deployment & Operational Notes

- System deployment verified and cataloged via ProjectVault.
