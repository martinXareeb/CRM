# NEXORA CRM — Universal Enterprise SaaS Platform

NEXORA CRM is a complete, modular, enterprise-grade Universal Customer Relationship Management and Business Operations SaaS platform built with **Next.js 16 (Turbopack)**, **TypeScript**, **Tailwind CSS**, and **Prisma ORM**.

---

## 🌟 Key Capabilities & Modules

1. **Executive Business Overview & KPI Dashboard**
   - Real-time pipeline valuation, revenue attribution, collected vs outstanding receivables.
   - Lead conversion analytics and customer service SLA compliance meters.
   - Monthly actual vs quota forecasting visualization.

2. **Lead Lifecycle & 1-Click Conversion Pipeline**
   - Inbound lead capture with AI score indicators (0–100).
   - Search, status filtering, qualification notes, and estimated deal value.
   - **1-Click Conversion Action**: Instantly converts qualified leads into Accounts, Contacts, and Pipeline Deals in database transactions.

3. **Sales CRM & Kanban Pipeline**
   - Multi-stage visual Kanban boards with probability weighting.
   - Interactive stage progression (Lead In → Discovery & Demo → Proposal → Negotiation → Closed Won).
   - Quotation line items and weighted sales forecasting.

4. **360-Degree Contacts & Account Directories**
   - Comprehensive contact relationship timelines, associated company accounts, and cross-module linkages.
   - Corporate accounts directory with annual revenue metrics and industry filters.

5. **Customer Support & Service Desk**
   - Automated `#TICK-XXXX` ticket numbering with SLA countdown timers.
   - Two-way conversation threads supporting **Internal Staff Notes** vs **Customer-Visible Replies**.
   - Public-facing **Customer Support Portal & Help Center** (`/portal`).

6. **Invoicing, Payments & Financial Ledger**
   - Automated invoice numbering (`INV-YYYY-XXX`) with line items, tax calculation, and payment terms.
   - Real-time **Record Payment Modal** deducting partial or full settlements from balance due.
   - Instant printable/previewable PDF invoice layout.

7. **Universal Workflow Automation Builder**
   - Event-driven visual rules (Triggers, Conditions, Actions).
   - Integrated **Execution Simulator** creating verified logs in the audit trace.

8. **NEXORA AI Copilot & Dedicated AI Studio**
   - Natural language CRM queries, customer health briefs, and sales follow-up email drafting.
   - Available via slide-out drawer on all screens and a dedicated `/ai` studio with prebuilt playbooks.
   - Deterministic enterprise mode out-of-the-box with optional live API key support.

9. **HR & Office Administration**
   - Employee directory with multi-branch allocation (SF HQ & London EMEA).
   - Leave request approval workflow (Annual, Sick, Casual) with 1-click status decisions.

10. **Multi-Tenant Security & Append-Only Audit Logging**
    - Granular Role-Based Access Control (Owner, Admin, Sales Manager, Support Agent, Finance Manager).
    - Session cookies with JWT signing and bcrypt password encryption.
    - Immutable audit logs tracking security and financial operations.

---

## 🚀 Quick Start Guide

### 1. Prerequisites
- **Node.js** v18+ (tested on Node v24)
- **npm** v9+

### 2. Install Dependencies
```bash
npm install
```

### 3. Initialize Database & Seed Demo Data
```bash
npx prisma db push
npm run seed
```

This creates the database `prisma/dev.db` and provisions the realistic enterprise demo organization **Nexora Global Innovations Inc.** with realistic leads, deals, contacts, invoices, tickets, tasks, and audit logs.

### 4. Run the Development Server
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) or [http://localhost:3001](http://localhost:3001).

---

## 🔑 Demo Personas & Credentials

All seeded accounts use password: `Password123!`

| Persona | Name | Role | Email |
| :--- | :--- | :--- | :--- |
| **Owner / CEO** | Alexander Wright | `OWNER` | `admin@nexora.io` |
| **Sales Manager** | Elena Rostova | `SALES_MANAGER` | `sales@nexora.io` |
| **Support Lead** | David Chen | `SUPPORT_AGENT` | `support@nexora.io` |
| **Finance Manager** | Sophia Alvarez | `FINANCE_MANAGER` | `finance@nexora.io` |

*Tip: You can switch between active personas at any moment using the top navigation bar persona dropdown or the 1-click login buttons on the login screen.*

---

## 🧪 Running Automated Tests

Run the comprehensive 24-point automated test suite:
```bash
npm test
```

### Verified Test Categories:
- **Authentication & Cryptography** (bcrypt hashing, JWT token signature)
- **RBAC Matrix Enforcement** (permission guards per role)
- **Tenant Isolation** (organization-scoped records)
- **Lead Qualification & 1-Click Conversion** (atomic deal generation)
- **Financial Ledger Reconciliation** (partial/full payments, balance deduction)
- **NEXORA AI Copilot Queries** (intelligence briefs & proposal drafting)

---

## 🏗️ Technology Architecture

- **Framework**: Next.js 16 (App Router, Turbopack)
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS
- **ORM & DB**: Prisma ORM with SQLite (zero-config local) / PostgreSQL (production)
- **Security**: bcryptjs, jsonwebtoken, HttpOnly Cookies
- **Icons**: Lucide React
