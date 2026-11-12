<div align="center">

# ⚡ UNIORA — Intelligent Welfare Schemes & Civic Empowerment Platform

<p align="center">
  <b>A seed-funded, AI-powered e-governance engine connecting citizens to applicable Central and State Government welfare schemes through intelligent eligibility matching and automated document verification.</b>
</p>

[![Seed Funded](https://img.shields.io/badge/Seed_Funded-KPRIET_Innovation_Cell-success?style=for-the-badge&logo=target)](https://kpriet.ac.in)
[![Cloudflare Workers](https://img.shields.io/badge/Deployed-Cloudflare_Workers-F38020?style=for-the-badge&logo=cloudflare)](https://uni-ora.uniora-official.workers.dev/dashboard/)
[![FastAPI](https://img.shields.io/badge/Backend-FastAPI-009688?style=for-the-badge&logo=fastapi)](https://fastapi.tiangolo.com/)
[![Supabase](https://img.shields.io/badge/Database-Supabase_PostgreSQL-3ECF8E?style=for-the-badge&logo=supabase)](https://supabase.com/)
[![Google GenAI](https://img.shields.io/badge/Vision_AI-Google_Gemini-4285F4?style=for-the-badge&logo=google)](https://ai.google.dev/)
[![Python 3.11](https://img.shields.io/badge/Python-3.11+-blue?style=for-the-badge&logo=python)](https://python.org)

<br />

### 🌐 [Live Production Platform](https://uni-ora.uniora-official.workers.dev/dashboard/)
**Experience the live dashboard:** [https://uni-ora.uniora-official.workers.dev/dashboard/](https://uni-ora.uniora-official.workers.dev/dashboard/)

</div>

---

## 📌 Executive Summary

**UNIORA** was conceived to solve one of the greatest challenges in Indian civic governance: *the discovery and last-mile accessibility of government welfare schemes*. Over 500+ welfare initiatives remain underutilized because eligible citizens are unaware of their entitlements or find eligibility criteria and document verification overwhelming.

UNIORA provides a centralized, rule-based matching engine and AI-driven document verification system that evaluates demographic criteria (caste, income, occupation, age, disability, education) in milliseconds, computes an actionable **Application Readiness Score**, and guides the citizen through application procedures.

> 🏆 **Institutional Recognition:** Awarded **Seed Funding** by the **KPRIET Innovation Cell** for technical viability, social impact, and innovative civic architecture.

---

## 🌟 Core Modules & Architecture

The platform is architected around 10 modular micro-features designed for accessibility, high performance, and offline-first responsiveness:

### 1. 🎯 Scheme Recommendation Engine (`01_scheme_recommendation`)
- Compares user demographic inputs with a categorized database of Central & State schemes.
- Provides ranked scheme suggestions sorted by impact, monetary benefits, and enrollment deadlines.

### 2. 🤖 Ask Uniora – Interactive AI Assistant (`02_ask_uniora`)
- Rule-based natural language guidance system.
- Assists citizens in plain language regarding scheme qualifications, prerequisite certificates, and deadlines.

### 3. 🔍 GenAI Document Verification & OCR (`03_documents_verification`)
- Built using **Google GenAI Vision (Gemini API)** and **Pillow**.
- Scans and validates submitted government IDs (Aadhaar, Ration Cards, Income Certificates, Community Certificates).
- Detects discrepancies in applicant name, DOB, or eligibility parameters before submission, preventing rejected applications.

### 4. ⚡ Real-Time Eligibility Evaluation (`04_eligible_schemes`)
- Fast, multi-criteria filtering evaluating gender, caste, annual income, land ownership, and education.
- Delivers instant eligibility results with clear checklists showing *why* a citizen qualifies or what criteria is missing.

### 5. 📊 My Readiness Score (`05_my_readiness`)
- Computes a dynamic 0–100% readiness score for any targeted scheme.
- Lists exact missing documents, pending renewals, and nearest government centres to obtain required paperwork.

### 6. 🏛️ Government Services Portal (`06_government_services`)
- Direct gateway routing users to official state e-Sevai, Umang, DigiLocker, and national departmental portals.
- Eliminates scam portals by offering authenticated deep links to authorized application forms.

### 7. 🌐 Multilingual & Inclusive UX (`07_faq`, `08_settings`, `09_language`, `10_profile`)
- Designed for low-bandwidth rural environments.
- Comprehensive FAQs, language toggles, profile management, and high-contrast accessibility options.

---

## 🏗️ System Architecture & Data Flow

```
+-------------------------------------------------------------------+
|                        Client Layer                               |
|        Responsive Web Dashboard (HTML5, Modern CSS, JS)           |
+---------------------------------+---------------------------------+
                                  |
                                  v
+---------------------------------+---------------------------------+
|                        Edge Proxy Tier                            |
|        Cloudflare Workers Serverless Edge (Sub-50ms Latency)      |
+---------------------------------+---------------------------------+
                                  |
                                  v
+---------------------------------+---------------------------------+
|                        Backend API                                |
|        FastAPI (Python 3.11) + Uvicorn Asynchronous Server        |
|        * Rule Engine & Scheme Evaluator                           |
|        * Google GenAI Vision (Gemini Document Validation)         |
+---------------------------------+---------------------------------+
                                  |
                                  v
+---------------------------------+---------------------------------+
|                        Database & Storage                         |
|        Supabase PostgreSQL + Row-Level Security (RLS)             |
|        * User Profiles & Demographic Encodings                    |
|        * Schemes Master Dataset & Eligibility Matrices            |
|        * Encrypted User Document Storage                          |
+-------------------------------------------------------------------+
```

---

## 🛠️ Technology Stack

| Domain | Technology / Tool | Purpose |
|:---|:---|:---|
| **Backend API** | **FastAPI** (`v0.110.0+`), **Uvicorn** | High-throughput asynchronous RESTful API |
| **Edge & CDN** | **Cloudflare Workers** | Global serverless edge routing & caching (<50ms) |
| **Database** | **Supabase (PostgreSQL)** | Relational database with Row Level Security (RLS) |
| **Vision AI** | **Google GenAI (Gemini)**, **Pillow** | Intelligent OCR & document authenticity validation |
| **Networking** | **HTTPX**, **Requests** | Asynchronous HTTP client for schemes data ingestion |
| **Frontend** | **HTML5, CSS3, Vanilla JS** | Lightweight, accessible, and fast-loading web UI |
| **Auth** | **Supabase Auth** | Token-based secure citizen authentication |

---

## 📂 Project Directory Structure

```
UNIORA/
├── auth/                       # User login, registration, and session management
├── backend/                    # Core server entrypoints and background processors
├── common/                     # Global styles, shared headers, scripts & utilities
├── dashboard/                  # Main citizen dashboard interface
├── features/                   # Independent micro-feature modules
│   ├── 01_scheme_recommendation/
│   ├── 02_ask_uniora/          # Chatbot assistant & rule engine
│   ├── 03_documents_verification/ # GenAI OCR & document validation
│   ├── 04_eligible_schemes/    # Multi-parameter eligibility matcher
│   ├── 05_my_readiness/        # Application readiness score calculator
│   ├── 06_government_services/ # State & central e-governance service links
│   ├── 07_faq/
│   ├── 08_settings/
│   ├── 09_language/
│   └── 10_profile/
├── supabase/
│   ├── migrations/             # SQL schema migrations (001 to 003)
│   ├── policies/               # Row-Level Security (RLS) policies
│   └── seed/                   # Master schemes database seed scripts
├── .env.example                # Template for environment variables
├── .gitignore                  # Git ignore rules
├── requirements.txt            # Python dependencies
└── README.md                   # Comprehensive project documentation
```

---

## 💻 Local Development Setup

### 1. Prerequisites
- Python 3.11 or higher
- Git
- Supabase account & project
- Google Gemini API key

### 2. Clone the Repository
```bash
git clone https://github.com/Abu1820/UNIORA.git
cd UNIORA
```

### 3. Create & Activate Virtual Environment
```bash
# Windows
python -m venv venv
.\venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 4. Install Dependencies
```bash
pip install -r requirements.txt
```

### 5. Configure Environment Variables
Copy `.env.example` to `.env` and fill in your keys:
```env
SUPABASE_URL=https://your-project.supabase.co
SUPABASE_KEY=your_supabase_anon_key
GEMINI_API_KEY="your_gemini_api_key"
```

### 6. Run Database Migrations (Supabase)
Run the SQL scripts located in `supabase/migrations/` inside your Supabase SQL Editor:
- `001_initial_schema.sql`
- `002_schemes_table.sql`
- `003_user_documents.sql`
- `supabase/policies/rls_policies.sql`

### 7. Start the Local Server
```bash
uvicorn backend.main:app --reload --port 8000
```
Visit `http://localhost:8000/dashboard/` to test the application locally.

---

## 🌐 Live Production Deployment

* **Edge Hosting:** Cloudflare Workers
* **Production URL:** [https://uni-ora.uniora-official.workers.dev/dashboard/](https://uni-ora.uniora-official.workers.dev/dashboard/)

---

## 👥 Contributors & Acknowledgements

* **Lead Architect & Developer:** **Abdul Majeed R** ([@Abu1820](https://github.com/Abu1820))
* **Institution:** KPR Institute of Engineering and Technology (KPRIET)
* **Funding:** Seed-funded by **KPRIET Innovation Cell**

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — free for educational and research use.
