# WhoisOutThere - Swiss Talent Intelligence System

[![Live Demo](https://img.shields.io/badge/Live-Production-success)](https://recruitingdecidor-frontend-production.up.railway.app)
[![Architecture](https://img.shields.io/badge/Architecture-9%20Microservices-blue)]()
[![i18n](https://img.shields.io/badge/i18n-DE%20%7C%20EN%20%7C%20FR-green)]()
[![Portfolio](https://img.shields.io/badge/More_About_Me-aeberhard.ai-red)](https://aeberhard.ai)

## 🧠 Why I Built This

After 12 years in government digital transformation (TEMOSTA23/Logib), I witnessed how "10+ years experience required" filters out brilliant people with 8 years. That's a 67% talent pool reduction for 2 years difference.

Coming from a 47-year journey through banking precision, political consensus-building, and federal statistics, I realized: **We don't have a talent shortage. We have a discovery problem.**

## The Menschen-Centric Philosophy

The "Menschen hinter der Stelle sehen" (see the people behind the job) philosophy emerged from frustration with keyword-based recruiting systems. Instead of filtering out talent based on arbitrary requirements, we transform job postings into market intelligence about WHO applies and WHO gets excluded.

**Developer insight**: Traditional ATS systems optimize for elimination. We optimize for inclusion by showing companies the human cost of their requirements.

## What It Actually Does

WhoisOutThere is a Swiss-focused talent intelligence platform that:

- **PDF Processing Pipeline**: Multi-strategy extraction (PyMuPDF → Tesseract OCR → AI Vision fallback)
- **Two-Phase AI Analysis**: 
  - Phase 1: 8 parallel modules extract job DNA (requirements, culture, psychology)
  - Phase 2: 3-stage synthesis generates concrete human personas using Swiss labor market data
- **Bedürfnisgruppen, Not Fake Personas**: Creates need-based talent segments with actual demographic backing
- **Trilingual by Design**: Native DE/EN/FR support throughout the stack

## Railway Microservices Architecture

**Performance bottleneck solved**: Moving from Supabase Edge Functions (2-minute timeout) to Railway microservices (no limits).

### The 9-Service Symphony

1. **Frontend Service** - Next.js 15.3.2 with bulletproof i18n
2. **Inngest Orchestrator** - Fire & forget async workflows  
3. **PDF Extraction** - PyMuPDF → 0.2s per document (99% cheaper than AI)
4. **Analysis Engine** - 8 parallel modules, 90s total execution
5. **Synthesis Service** - Context → Analysis → Personas (3-stage pipeline)
6. **Data Normalization** - Transform AI chaos into Chart.js-ready APIs
7. **Context Discovery** - Swiss labor market intelligence engine
8. **Reports Generator** - HTML/PDF with Human Spectrum visualization (in development)
9. **~~Visualization Service~~** - Deprecated (business logic moved to Data Normalization)

### Tech Stack That Actually Works

- **Frontend**: Next.js 15.3.2, TypeScript, TailwindCSS (zero hardcoded strings policy)
- **Backend**: Node.js, PostgreSQL 17.4 (17 new JSONB GIN indexes for 50-80% faster queries)
- **AI Models**: Gemini 2.5 → 2.5 Flash → 1.5 Flash (fallback chain for rate limits)
- **Infrastructure**: Railway auto-scaling, Inngest for complex workflows
- **Database**: Row-Level Security on all 31 tables, 50+ policies, materialized views

## Real Performance Metrics (Not Marketing Fluff)

| Component | Actual Performance | Engineering Notes |
|-----------|-------------------|-------------------|
| PDF Extraction | ~0.2s per document | PyMuPDF beats AI by 99% cost, 10x speed |
| Phase 1 Analysis | ~90 seconds | 8 modules in parallel, bottleneck is Gemini rate limits |
| Phase 2 Synthesis | 2-3 minutes | Railway removed the 2-minute Edge Function wall |
| API Response Times | <200ms | PostgreSQL 17 JSONB indexes doing their job |
| Database Queries | 50-80% faster | After PostgreSQL 17 upgrade with 17 new GIN indexes |
| i18n Validation | 100% coverage | Zero hardcoded strings policy enforced |

## Swiss Labor Market Specialization

**Why Swiss-focused?** Different countries have different talent dynamics. Rather than building a generic solution, we specialized:

- **Regional Intelligence**: Zurich vs. Geneva vs. Basel talent preferences
- **Multilingual Reality**: Native DE/FR/IT/EN support (not just translation layers)
- **Education System Integration**: Swiss apprenticeship system, Fachhochschule, ETH pathways
- **Local Market Data**: Actual Swiss salary bands, commute patterns, industry concentrations

## Engineering Challenges Solved

**Database Performance Crisis**: At >1M profiles, PostgreSQL queries were hitting 10+ seconds. Solution: 17 carefully crafted JSONB GIN indexes targeting our specific query patterns.

**AI Rate Limiting**: Gemini 2.5 availability is unpredictable. Built a fallback chain with degradation gracefully handled in the UI.

**Timeout Hell**: Supabase Edge Functions' 2-minute limit killed complex analysis. Railway microservices removed this constraint entirely.

**i18n at Scale**: Zero hardcoded strings policy across 9 services. Custom validation tools catch violations during CI/CD.

## 🎯 The "Aha!" Moments

### When Government Experience Met AI
Working on TEMOSTA23 (6M CHF budget, 30+ team), I saw how bureaucracy creates talent blindness. The same precision that helped win a UN award could revolutionize how we see Menschen.

### When "Swiss-Focused" Became the Strength
Everyone builds global. But Zurich isn't San Francisco. Geneva isn't London. **Swiss talent moves differently** - by train schedules, language regions, and cantonal boundaries. That specificity became our superpower.

## 💭 What I Learned (Technical & Personal)

### Technical Victories
- **PostgreSQL 17 saved us**: Those 17 JSONB indexes turned 10s queries into 200ms
- **Railway removed all limits**: From Edge Function timeout hell to unlimited processing
- **i18n is a philosophy**: Zero hardcoded strings across 9 services = true multilingual

### Personal Insights
- **Government teaches scale**: Managing 30+ people prepared me for 9 microservices
- **Banking teaches precision**: Every talent metric must be verifiable
- **Politics teaches consensus**: The Menschen philosophy bridges HR and engineering
- **47 years converge**: Every domain I've touched contributes to this solution

## Current Development Status (Honest Assessment)

**✅ Production-Ready:**
- Core two-phase analysis pipeline
- PDF extraction with fallbacks
- Trilingual frontend
- Data normalization APIs
- PostgreSQL 17 with full RLS

**🚧 Active Development:**
- Report Generation Service (HTML/PDF exports)
- Enhanced What-If scenarios (API complete, UI pending)
- Advanced visualization components

**🔮 Planned:**
- ML-based demographic interpolation
- Commute pattern analysis
- Industry-specific persona templates

## 🔗 Portfolio & Contact

Learn more about my work and other projects:
- **Portfolio**: [aeberhard.ai](https://aeberhard.ai)
- **LinkedIn**: [Patric Aeberhard](https://www.linkedin.com/in/patricaeberhard/)
- **Email**: patric@aeberhard.ai
- **Live Platform**: [recruitingdecidor-frontend-production.up.railway.app](https://recruitingdecidor-frontend-production.up.railway.app)

---

*This showcase demonstrates the technical architecture behind WhoisOutThere without exposing proprietary code or business secrets.*

*This showcase represents the public-facing aspects of WhoisOutThere. Proprietary algorithms and business logic are not included. Built by [Patric Aeberhard](https://aeberhard.ai) as part of a comprehensive Swiss talent intelligence platform.*