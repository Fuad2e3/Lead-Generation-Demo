<div align="center">

# 🎯 Lead Generation Demo
### **Intelligent B2B Prospecting & Google Sheet Auto-Enrichment System**

[![Platform](https://img.shields.io/badge/Platform-n8n_Workflow-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io/)
[![Engine](https://img.shields.io/badge/Engine-Automation_Pipeline-blue?style=for-the-badge)](https://n8n.io/)
[![Integration](https://img.shields.io/badge/Integration-Google_Sheets-34A853?style=for-the-badge&logo=googlesheets&logoColor=white)](https://developers.google.com/sheets/api)
[![Format](https://img.shields.io/badge/Format-JSON_Workflow-orange?style=for-the-badge&logo=json&logoColor=white)](Lead%20Generation.json)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

**Automate lead prospecting, domain verification, and spreadsheet enrichment at scale with zero friction.**

---

[Explore Features](#-key-features) • [Workflow Architecture](#-workflow-architecture) • [Execution Flow](#-execution-pipeline) • [Tech Stack](#-tech-stack)

</div>

---

## 📖 Overview
**Lead Generation Demo** is an enterprise-grade automated data enrichment and prospecting pipeline powered by **n8n**. Designed to eliminate hours of manual data entry, the system accepts a live Google Sheet, crawls company domains, scrapes decision-maker contact points, validates email health, and writes clean, verified intelligence directly back to your spreadsheet in real time.

---

## ✨ Key Features

- ⚡ **1-Click Webhook Trigger:** Initiates automated enrichment directly via a user-friendly form interface with instant background confirmation.
- 🔍 **Automated Domain & Company Crawling:** Extracts company descriptions, social media profiles (LinkedIn, X, Facebook), and phone numbers.
- 📧 **Contact & Email Discovery:** Scrapes public mailto links, applies pattern generation, and executes email syntax & MX screening.
- 📊 **Real-Time Google Sheets Auto-Update:** Reads target rows, detects missing data columns, and updates enriched cells asynchronously.
- 🛡️ **Rate-Limit & Anti-Blocking Resilient:** Implements intelligent batching and delay timers to protect API quotas.
- 📈 **Audit Logging:** Detailed execution statuses and success rate tracking for every row.

---

## 📁 Project Structure

```text
Lead-Generation-Demo/
├── 🎯 Lead Generation.json     # Complete n8n workflow definition
├── 📁 workflows/               # Supporting sub-flow handlers
├── 📁 assets/                  # Architecture diagrams & documentation
└── README.md                   # System documentation & architecture guide
```

---

## 🏗️ Workflow Architecture

```text
[Form Trigger: Sheet Link]
         │
         ▼
[Fetch Google Sheet Metadata & GID]
         │
         ▼
[Read Rows & Detect Unenriched Records]
         │
         ▼
[Parallel Scraping & Domain Intelligence Engine]
  ├── Company Details Extraction
  ├── Email Discovery & MX Validation
  └── Social Links Resolution (LinkedIn, Twitter)
         │
         ▼
[Format & Validate Output Data]
         │
         ▼
[Google Sheets API: Batch Row Auto-Update]
```

---

## 🛠️ Tech Stack

| Layer | Technology | Purpose |
| :--- | :--- | :--- |
| **Workflow Engine** | [n8n](https://n8n.io) | Visual low-code node orchestration |
| **Data Sink** | Google Sheets API v4 | Real-time bi-directional spreadsheet sync |
| **Data Extraction** | Custom HTTP Scraper Nodes | Headless metadata and link parsing |
| **Language** | JavaScript (Node.js runtime) | Custom node transformation logic |
| **Deployment** | Self-hosted Docker / n8n Cloud | High-availability workflow execution |

---

## 📄 License
Distributed under the MIT License. See `LICENSE` for more information.

<div align="center">

**Developed ❤️ by Softece**

</div>
