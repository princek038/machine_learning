# PulseWave — SaaS Analytics & Revenue Operations Platform

[![Vite](https://img.shields.io/badge/Vite-8.3-646CFF?style=flat&logo=vite&logoColor=white)](https://vitejs.dev/)
[![React](https://img.shields.io/badge/React-19.3-61DAFB?style=flat&logo=react&logoColor=black)](https://react.dev/)
[![Lucide Icons](https://img.shields.io/badge/Icons-Lucide-F56565?style=flat)](https://lucide.dev/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A high-performance SaaS Analytics, Revenue Operations, and Telemetry platform built with React, Vite, and custom CSS design system. Designed for executive teams, engineering leads, and financial operators.

---

## ⚡ Key Highlights & Architecture

- **Executive Analytics Overview**:
  - Real-time KPI Metric cards (MRR, ARR, Active Accounts, Net Churn Rate, LTV, Quick Ratio) with responsive SVG sparklines and trend indicators.
  - Interactive SVG Area & Line Chart with smooth cubic bezier curve interpolation, dual-series metrics (Revenue, Profit, Accounts), timeframe switches (`7D`, `30D`, `90D`, `1Y`), and tracking crosshairs with mouse hover tooltips.
  - Dynamic Subscription Tier Donut breakdown with segment hover animations and ARR metrics.
- **Live Telemetry & Websocket Stream**:
  - Live websocket telemetry simulator that streams real-time financial events, usage alerts, and upgrades.
  - Interactive event simulation trigger ("Emit Test Event") and category filtering (Payments, Upgrades, System logs).
- **Customer & Organization Directory (CRM)**:
  - Searchable by customer, organization name, or corporate domain.
  - Filterable by Subscription Plan (`Enterprise Ultra`, `Pro Scale`, `Growth Starter`) and Contract Health (`Active`, `Trialing`, `At Risk`).
  - Column sorting on Name, Contract MRR, Seats, and Status.
  - "Invite Organization Account" interactive modal dialog with form validation.
- **Geographical & Cohort Revenue Intelligence**:
  - Multi-region revenue shares across North America, EU, APAC, and Global markets.
  - Expansion vs Contraction vs Churned MRR metrics.
- **Infrastructure & Cluster Health**:
  - Production service health monitors (Global Edge Router, Ingestion Pipeline, PostgreSQL Cluster, Redis Cache).
  - Compute & memory allocation meters (Kubernetes vCPUs, Redis hit ratios, Database IOPS headroom).
- **Platform Preferences & API Keys**:
  - API credential management with copy-to-clipboard functionality.
  - Webhook URL routing, localization currency switchers (USD, EUR, GBP), and automated anomaly alert policies.
- **Aesthetic Engineering**:
  - Curated dark mode default with light mode toggle.
  - Glassmorphic panels with backdrop blurs, border glows, and typography powered by Outfit & Plus Jakarta Sans.
  - 100% build-error free, zero external CSS framework dependencies (Vanilla CSS design system).

---

## 🚀 Quick Start Guide

### 1. Prerequisites
Ensure you have Node.js (v18+) and npm installed.

### 2. Install Dependencies
```bash
npm install
```

### 3. Run Development Server
```bash
npm run dev
```
Open [http://localhost:5173](http://localhost:5173) in your browser.

### 4. Build for Production
```bash
npm run build
```

---

## 📁 Project Structure

```
├── public/                 # Static assets & icons
├── src/
│   ├── components/
│   │   ├── Header.jsx              # Global top bar, search, live toggle, theme switch
│   │   ├── Sidebar.jsx             # Workspace switcher & navigation drawer
│   │   ├── MetricCard.jsx          # KPI card with animated SVG sparklines
│   │   ├── InteractiveChart.jsx    # Bezier Area & Line chart with hover tooltips
│   │   ├── RevenueDonut.jsx        # SVG donut chart for subscription tiers
│   │   ├── LiveActivityFeed.jsx    # Real-time websocket event feed
│   │   ├── UserManagementTable.jsx # Customer subscriptions CRM & invite modal
│   │   ├── RevenueView.jsx         # Geographical revenue & expansion metrics
│   │   ├── SystemHealth.jsx        # Edge latencies & compute utilization
│   │   ├── SettingsView.jsx        # API keys, webhooks, and alert policies
│   │   └── Toast.jsx               # Floating toast notification system
│   ├── data/
│   │   └── mockData.js             # SaaS financials, customers, and telemetry data
│   ├── App.jsx                     # Root application container & state manager
│   ├── App.css                     # Complete design system & responsive layout
│   ├── index.css                   # Global variables, themes, and reset tokens
│   └── main.jsx                    # React entrypoint
├── index.html                      # SEO metadata, Google Fonts, and root container
└── vite.config.js                  # Vite bundler configuration
```
