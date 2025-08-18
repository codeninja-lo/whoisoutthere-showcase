# RecruitingDecidor - "Menschen hinter der Stelle sehen"

[![Live Demo](https://img.shields.io/badge/Live-Production-success)](https://recruitingdecidor-frontend-production.up.railway.app)
[![Tech Stack](https://img.shields.io/badge/Stack-Next.js%20%7C%20Supabase%20%7C%20Railway-blue)]()
[![Languages](https://img.shields.io/badge/Languages-DE%20%7C%20EN%20%7C%20FR-green)]()

## 🎯 Die Vision

**"Menschen hinter der Stelle sehen"** - RecruitingDecidor transformiert Stellenausschreibungen in konkrete Menschen mit Namen, Geschichten und Lebensrealitäten. Unternehmen sehen WER sie mit ihrer Stellenausschreibung erreichen und WEN sie ausschließen.

## 🚀 Was es wirklich macht

RecruitingDecidor ist eine AI-gestützte Plattform zur Analyse von Stellenausschreibungen:

- **PDF/Text-Extraktion**: Verarbeitet Stellenausschreibungen aus verschiedenen Quellen
- **2-Phasen AI-Analyse**: 
  - Phase 1: Extrahiert Anforderungen, Skills, kulturelle Aspekte
  - Phase 2: Generiert konkrete Personas basierend auf Marktdaten
- **Personas mit Leben**: Erstellt Menschen mit Namen, Hintergründen, Motivationen
- **Multi-Language**: Unterstützt Deutsch, Englisch und Französisch

## 🏗️ Technische Architektur

### Microservices auf Railway (9 Services)

1. **Frontend** - Next.js 15.3.2 mit i18n
2. **Inngest Handler** - Orchestriert asynchrone Workflows  
3. **PDF Service** - Extrahiert Text aus PDFs (PyMuPDF)
4. **Analysis Service** - 8 parallele AI-Module für Phase 1
5. **Phase2 Service** - Generiert Menschen-Personas
6. **Data Normalization** - API-friendly Datenaufbereitung
7. **Context Discovery** - Markt-Intelligence Engine

### Tech Stack

- **Frontend**: Next.js 15.3.2, TypeScript, TailwindCSS
- **Backend**: Node.js, Supabase (PostgreSQL 17)
- **AI**: Google Gemini 2.5, OpenAI GPT-4
- **Infrastructure**: Railway (Microservices), Inngest (Workflows)
- **Database**: PostgreSQL 17 mit JSONB und Materialized Views

## 📊 Echte Performance-Metriken

| Component | Performance |
|-----------|------------|
| PDF Extraction | ~0.2s per document |
| Phase 1 Analysis | ~90 seconds (8 parallel modules) |
| Phase 2 Synthesis | 2-3 minutes |
| API Response | <200ms |

## 🌍 Schweizer Arbeitsmarkt-Fokus

Speziell optimiert für den Schweizer Arbeitsmarkt mit:
- Verständnis für regionale Unterschiede
- Mehrsprachigkeit (DE/FR/IT/EN)
- Schweizer Bildungssystem-Integration
- Lokale Arbeitsmarkt-Daten

## 🔐 Privacy & Security

- Row-Level Security (RLS) auf allen Tabellen
- Verschlüsselte API Keys
- GDPR-konform
- Keine Speicherung von persönlichen Daten der generierten Personas

## 🚧 Aktueller Status

**Production**: Die Plattform läuft produktiv mit allen Core-Features.

**In Entwicklung**:
- Report Generation Service
- Enhanced What-If Scenarios
- Erweiterte Visualisierungen

## 🔗 Links

- **Live Platform**: [recruitingdecidor-frontend-production.up.railway.app](https://recruitingdecidor-frontend-production.up.railway.app)
- **Documentation**: Siehe `/docs` für technische Details

---

*Dieses Repository zeigt die öffentlichen Aspekte von RecruitingDecidor. Proprietärer Code und Geschäftslogik sind nicht enthalten.*