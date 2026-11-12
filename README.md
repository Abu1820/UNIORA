<div align="center">

# ⚡ UNIORA
### Intelligent Welfare Schemes & Civic Empowerment Platform

A centralized, AI-assisted civic e-governance engine connecting citizens to applicable Central and State Government welfare schemes through automated eligibility matching and GenAI document verification.

<br />

<a href="https://uni-ora.uniora-official.workers.dev/dashboard/">
  <img src="https://img.shields.io/badge/🚀_Live_Demo-Launch_UNIORA_Dashboard-6366f1?style=flat&logo=cloudflare&logoColor=white" alt="Launch Live Platform" height="24" />
</a>
&nbsp;
<a href="https://kpriet.ac.in">
  <img src="https://img.shields.io/badge/Institutional_Award-Seed_Funded-059669?style=flat&logo=target&logoColor=white" alt="Seed Funded" height="24" />
</a>
&nbsp;
<img src="https://img.shields.io/badge/Python-3.11+-0284c7?style=flat&logo=python&logoColor=white" alt="Python" height="24" />
&nbsp;
<img src="https://img.shields.io/badge/FastAPI-Framework-0d9488?style=flat&logo=fastapi&logoColor=white" alt="FastAPI" height="24" />
&nbsp;
<img src="https://img.shields.io/badge/Supabase-PostgreSQL-10b981?style=flat&logo=supabase&logoColor=white" alt="Supabase" height="24" />
&nbsp;
<img src="https://img.shields.io/badge/Google_Gemini-Vision_OCR-7c3aed?style=flat&logo=google&logoColor=white" alt="Google Gemini" height="24" />

<br />

```
FastAPI  •  Cloudflare Workers Edge  •  Supabase PostgreSQL (RLS)  •  Google GenAI Vision  •  Rule Engine
```

<p>
  <a href="#-key-capabilities"><b>Features</b></a> &nbsp;•&nbsp;
  <a href="#%EF%B8%8F-system-architecture"><b>Architecture</b></a> &nbsp;•&nbsp;
  <a href="#-tech-stack"><b>Tech Stack</b></a> &nbsp;•&nbsp;
  <a href="#-project-structure"><b>Structure</b></a> &nbsp;•&nbsp;
  <a href="#-quick-start"><b>Setup</b></a> &nbsp;•&nbsp;
  <a href="https://uni-ora.uniora-official.workers.dev/dashboard/"><b>Live Demo ↗</b></a>
</p>

</div>

---

## 📌 Executive Summary

Over 500+ Central and State welfare initiatives remain underutilized because eligible citizens are unaware of their entitlements or find eligibility criteria and document verification overwhelming.

**UNIORA** bridges this last-mile civic governance gap:
- **Instant Eligibility Matching**: Evaluates citizen demographics (caste, income, occupation, age, disability, education) in milliseconds.
- **Vision AI Verification**: Analyzes uploaded certificates using Google Gemini Vision to catch errors before submission.
- **Dynamic Readiness Score**: Generates a 0–100% preparedness rating highlighting exactly what documents are missing.

> 🏆 **Institutional Recognition:** Awarded **Institutional Seed Funding** by the **KPRIET Innovation Cell** for technical novelty and high community impact.

---

## 🚀 Key Capabilities

| # | Module | Core Functionality |
|---|---|---|
| **01** | **Scheme Recommendation** | Personalized ranking algorithm sorting 500+ schemes by monetary benefit, eligibility fit, and deadlines. |
| **02** | **Ask Uniora** | Rule-based conversational assistant guiding citizens through qualifying conditions and steps. |
| **03** | **GenAI Document Verification** | OCR and authenticity scanner powered by **Google Gemini Vision API** to validate IDs (Aadhaar, Income, Community). |
| **04** | **Eligible Schemes Engine** | Multi-parameter filtering engine calculating qualification matrices in sub-50ms. |
| **05** | **My Readiness Score** | 0–100% preparedness rating with custom checklists for missing paperwork. |
| **06** | **Government Services Gateway** | Authenticated gateway to official state e-Sevai, Umang, and DigiLocker portals. |
| **07–10** | **Civic Inclusivity Suite** | Multilingual language toggles, citizen demographic profiles, and accessibility preferences for rural connectivity. |

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                       Client Layer                          │
│     Accessible, High-Performance Web Dashboard (HTML/JS)    │
└──────────────────────────────┬──────────────────────────────┘
                               │
                               ▼
┌─────────────────────────────────────────────────────────────┐
│                     Edge Proxy Tier                         │
│     Cloudflare Workers Serverless Edge (<50ms Global Ping)  │
└──────────────────────────────┬──────────────────────────────┘
                               │
                               ▼
┌─────────────────────────────────────────────────────────────┐
│                    FastAPI Backend (Python)                 │
│     * Real-time Multi-Criteria Rule Engine                  │
│     * Google GenAI Vision (Gemini Document Validation)      │
└──────────────────────────────┬──────────────────────────────┘
                               │
                               ▼
┌─────────────────────────────────────────────────────────────┐
│                   Database & Security                       │
│     Supabase PostgreSQL with Row Level Security (RLS)       │
└─────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Tech Stack

- **Backend:** Python 3.11, FastAPI (`v0.110.0+`), Uvicorn
- **AI & Vision:** Google GenAI Vision (`google-genai`), Pillow
- **Database:** Supabase PostgreSQL, Row-Level Security (RLS)
- **Edge & CDN:** Cloudflare Workers Serverless Runtime
- **Networking:** HTTPX, Requests, Python-Multipart
- **Frontend:** HTML5, CSS3 Grid/Flexbox, JavaScript (ES6+)

---

## 📂 Project Structure

```
UNIORA/
├── auth/                       # User authentication & session management
├── backend/                    # Core API endpoints & background services
├── common/                     # Global styles, navbar & helper utilities
├── dashboard/                  # Main citizen dashboard interface
├── features/                   # 10 Micro-feature implementations
│   ├── 01_scheme_recommendation/
│   ├── 02_ask_uniora/          # Chatbot & rule engine
│   ├── 03_documents_verification/ # Vision AI document verification
│   ├── 04_eligible_schemes/    # Real-time eligibility evaluation
│   ├── 05_my_readiness/        # Application readiness score calculator
│   ├── 06_government_services/ # Verified e-governance service links
│   ├── 07_faq/
│   ├── 08_settings/
│   ├── 09_language/
│   └── 10_profile/
├── supabase/
│   ├── migrations/             # SQL schema migrations (001–003)
│   └── policies/               # Row-Level Security (RLS) policies
├── .env.example                # Environment variables template
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation
```

---

## 💻 Quick Start

```bash
# 1. Clone repository
git clone https://github.com/Abu1820/UNIORA.git
cd UNIORA

# 2. Set up virtual environment
python -m venv venv
.\venv\Scripts\activate   # Windows
# source venv/bin/activate # macOS/Linux

# 3. Install dependencies
pip install -r requirements.txt

# 4. Configure environment
cp .env.example .env

# 5. Start development server
uvicorn backend.main:app --reload --port 8000
```

---

## 🌐 Production Deployment

- **Live URL:** [https://uni-ora.uniora-official.workers.dev/dashboard/](https://uni-ora.uniora-official.workers.dev/dashboard/)
- **Infrastructure:** Cloudflare Workers Serverless Edge

---

## 👥 Authors & Acknowledgements

* **Lead Architect & Developer:** **Abdul Majeed R** ([@Abu1820](https://github.com/Abu1820))
* **Institution:** KPR Institute of Engineering and Technology (KPRIET)
* **Grant:** Seed-funded by **KPRIET Innovation Cell**

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
