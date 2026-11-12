# ⚡ UNIORA — Intelligent Civic Welfare & Government Schemes Platform

<div align="center">

**A seed-funded, AI-powered e-governance platform connecting citizens to applicable Central and State Government welfare schemes through automated rule-based eligibility evaluation and Google Gemini Vision document verification.**

</div>

---

## 🌐 Live Demo & Production Deployment

👉 **Live Web Application:** **[https://uni-ora.uniora-official.workers.dev/dashboard/](https://uni-ora.uniora-official.workers.dev/dashboard/)**  
⚡ **Edge Infrastructure:** Cloudflare Workers Serverless Global Edge (<50ms Worldwide Ping)  
🏛️ **Funding & Incubation:** Seed-funded by **KPRIET Innovation Cell**

---

## 📖 Project Overview

Over 500+ Central and State welfare initiatives remain underutilized because eligible citizens are unaware of their entitlements or find complex qualifying criteria and document verification overwhelming.

**UNIORA** solves this last-mile civic governance gap:
- **Instant Eligibility Matching**: Evaluates citizen demographics (caste, income, occupation, age, disability, education) in milliseconds.
- **Vision AI Verification**: Analyzes uploaded certificates using Google Gemini Vision to catch errors before submission.
- **Dynamic Readiness Score**: Generates a 0–100% preparedness rating highlighting exactly what documents are missing.

---

## 🚀 Key Modules & Capabilities

| Module | Core Functionality |
|---|---|
| **01. Scheme Recommendation** | Personalized ranking algorithm sorting 500+ schemes by monetary benefit, eligibility fit, and deadlines. |
| **02. Ask Uniora** | Rule-based conversational assistant guiding citizens through qualifying conditions and steps. |
| **03. GenAI Document Verification** | OCR and authenticity scanner powered by **Google Gemini Vision API** to validate IDs (Aadhaar, Income, Community). |
| **04. Eligible Schemes Engine** | Multi-parameter filtering engine calculating qualification matrices in sub-50ms. |
| **05. My Readiness Score** | 0–100% preparedness rating with custom checklists for missing paperwork. |
| **06. Government Services Gateway** | Authenticated gateway to official state e-Sevai, Umang, and DigiLocker portals. |
| **07–10. Civic Inclusivity Suite** | Multilingual language toggles, citizen demographic profiles, and accessibility preferences for rural connectivity. |

---

## 🏗️ System Architecture & Data Flow

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

## 🛠️ Complete Tech Stack

* **Backend Framework:** Python 3.11, FastAPI (`v0.110.0+`), Uvicorn
* **AI & Vision:** Google GenAI Vision (`google-genai`), Pillow
* **Database & Auth:** Supabase PostgreSQL, Row-Level Security (RLS)
* **Edge Routing & CDN:** Cloudflare Workers Serverless Runtime
* **Networking & Ingestion:** HTTPX, Requests, Python-Multipart
* **Frontend:** HTML5, CSS3 Grid/Flexbox, JavaScript (ES6+)

---

## 📂 Project Directory Structure

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

## 💻 Local Development Setup

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

## 👥 Authors & Acknowledgements

* **Lead Architect & Developer:** **Abdul Majeed R** ([@Abu1820](https://github.com/Abu1820))
* **Institution:** KPR Institute of Engineering and Technology (KPRIET)
* **Incubation:** Seed-funded by **KPRIET Innovation Cell**

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
