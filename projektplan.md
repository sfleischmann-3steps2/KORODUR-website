# Projektplan: KORODUR Website Relaunch
**Stand:** 2026-03-24 | **Projektleiter:** Agent 0 | **Auftraggeberin:** Steffi (Applied AI Manager)

---

## Projektteam

| Rolle | Agent | Einsatzphase | Hauptaufgabe |
|-------|-------|-------------|--------------|
| **Projektleiter** | Agent 0 | Alle | Steuerung, QS, Phasenübergänge |
| **Stratege** | Agent 1 | Phase 1–3 | Positionierung, Zielgruppen-Strategie |
| **Content Creator** | Agent 2 | Phase 1, 3–4 | Content Audit, Messaging, Texte |
| **SEO-Spezialist** | Agent 3 | Phase 1–2 | Technical SEO, Keyword-Analyse |
| **CRO-Optimierer** | Agent 4 | Phase 1–2 | Conversion-Analyse, CTA-Bewertung |
| **Recherche-Agent** | Agent 7 | Phase 1–2 | Website-Crawling, Datensammlung |
| **Konzept-Agent** | Agent 12 | Phase 3 | IA, Seitentypen, Wireframes |
| **Wettbewerbs-Agent** | Agent 13 | Phase 2 | Competitor Deep-Dives |

---

## Phase 1 – Analyse (aktiv)

### Sprint 1.1: Technical Audit
**Task-Datei:** `01_analyse/TASK_technical_audit.md`
**Output:** `01_analyse/technical_audit.md`
**Verantwortlich:** SEO-Spezialist (Agent 3) + Recherche-Agent (Agent 7)

| # | Arbeitsschritt | Agent | Methode |
|---|---------------|-------|---------|
| 1 | HTTP-Header, robots.txt, sitemap.xml abrufen | Agent 7 | WebFetch |
| 2 | Stack erkennen (WP-Version, Theme, Plugins) | Agent 7 | WebFetch + HTML-Analyse |
| 3 | Meta-Tags, Hreflang, Schema.org, Canonicals | Agent 3 | WebFetch + SEO-Analyse |
| 4 | URL-Struktur & Mehrsprachigkeit dokumentieren | Agent 3 | Sitemap-Analyse |
| 5 | Performance-Einschätzung (Bildformate, JS, Lazy Loading) | Agent 7 | WebFetch |
| 6 | Cookie/Consent & Tracking identifizieren | Agent 7 | WebFetch |
| 7 | Seitentypen-Inventar erstellen | Agent 3 | Sitemap + Stichproben |
| 8 | Bewertungsmatrix + Empfehlungen zusammenfassen | PL (Agent 0) | Review + Konsolidierung |

### Sprint 1.2: Struktur- & Inhaltsaudit
**Task-Datei:** `01_analyse/TASK_structure_content_audit.md`
**Output:** `01_analyse/structure_audit.md` + `01_analyse/content_audit.md`
**Verantwortlich:** Content Creator (Agent 2) + CRO-Optimierer (Agent 4)

| # | Arbeitsschritt | Agent | Methode |
|---|---------------|-------|---------|
| 1 | Navigationsstruktur vollständig erfassen (Haupt + Footer) | Agent 7 | WebFetch Homepage |
| 2 | Informationsarchitektur bewerten (Klicktiefe pro Zielgruppe) | Agent 2 | Manuelle Navigation |
| 3 | Zielgruppen-Navigation analysieren (Einstiegspunkte?) | Agent 2 | Content-Analyse |
| 4 | Mehrsprachige Konsistenz prüfen (DE/EN/FR) | Agent 7 | Stichproben WebFetch |
| 5 | Produktseiten inventarisieren (Name, TDS, SDS, Bilder) | Agent 2 | Produktbereich crawlen |
| 6 | Content-Qualitätsbewertung (1–5 Skala) | Agent 2 | Bewertungsmatrix |
| 7 | CTA-Analyse (Homepage + Produktseiten) | Agent 4 | CRO-Perspektive |
| 8 | Content-Gaps pro Zielgruppe identifizieren | Agent 2 + Agent 4 | Gap-Analyse |

**Sprint 1.1 und 1.2 laufen parallel** – keine Abhängigkeiten untereinander.

---

## Phase 2 – Benchmark (nach Phase 1)

### Sprint 2.1: Wettbewerber-Benchmark
**Task-Datei:** `02_benchmark/TASK_competitors.md`
**Output:** `02_benchmark/competitors.md`
**Verantwortlich:** Wettbewerbs-Agent (Agent 13) + Stratege (Agent 1)

| # | Arbeitsschritt | Agent |
|---|---------------|-------|
| 1 | Tier 1 analysieren: MC-Bauchemie, Flowcrete, Vandex | Agent 13 |
| 2 | Tier 2 analysieren: Sika, Mapei, Ardex, Chemotechnik | Agent 13 |
| 3 | Tier 3 analysieren: Knauf, Saint-Gobain Weber | Agent 13 |
| 4 | Strategische Einordnung + Differenzierungspotenziale | Agent 1 |
| 5 | Feature-Matrix erstellen | Agent 13 + PL |

### Sprint 2.2: Zielgruppenplattformen-Benchmark
**Task-Datei:** `02_benchmark/TASK_zielgruppenplattformen.md`
**Output:** `02_benchmark/zielgruppenplattformen.md`
**Verantwortlich:** Recherche-Agent (Agent 7) + Stratege (Agent 1)

| # | Arbeitsschritt | Agent |
|---|---------------|-------|
| 1 | Planer-Plattformen: Heinze, DETAIL, BauNetz, STLB-Bau, BIMobject | Agent 7 |
| 2 | Verarbeiter-Plattformen: Bauhandwerk, EF-Magazin, ZDB | Agent 7 |
| 3 | Handels-Plattformen: Hagebau, Würth, Raab Karcher | Agent 7 |
| 4 | Best-Practice B2B: Hilti, Bosch Pro, Rockwool, Schöck, Knauf Insulation | Agent 7 |
| 5 | Feature-Ideenliste priorisiert zusammenstellen | Agent 1 + PL |

### Sprint 2.3: Feature-Matrix (Synthese)
**Output:** `02_benchmark/feature_matrix.md`
**Abhängigkeit:** Sprint 2.1 + 2.2 müssen fertig sein
**Verantwortlich:** Stratege (Agent 1) + Projektleiter

---

## Abhängigkeiten

```
Phase 1:  Sprint 1.1 ──┐
                        ├──→ Phase 1 Review ──→ Phase 2
          Sprint 1.2 ──┘

Phase 2:  Sprint 2.1 ──┐
                        ├──→ Sprint 2.3 (Feature-Matrix) ──→ Phase 3
          Sprint 2.2 ──┘
```

---

## Heute starten: Arbeitsaufträge

### Sofort (parallel):
1. **SEO-Spezialist + Recherche-Agent → Technical Audit**
   - korodur.de crawlen: HTTP-Header, robots.txt, sitemap, HTML-Analyse
   - SEO-Struktur bewerten, Seitentypen inventarisieren
   - Output: `01_analyse/technical_audit.md`

2. **Content Creator + CRO-Optimierer → Structure & Content Audit**
   - Navigationsstruktur erfassen, Produktseiten inventarisieren
   - Content-Qualität bewerten, Gaps identifizieren
   - Output: `01_analyse/structure_audit.md` + `01_analyse/content_audit.md`

### Nach Phase 1 Review:
3. Wettbewerber-Benchmark starten (Agent 13)
4. Zielgruppenplattformen-Benchmark starten (Agent 7)

---

## Qualitätskriterien pro Phase

| Phase | Fertig wenn... |
|-------|---------------|
| Phase 1 | Alle 3 Output-Dateien erstellt, von PL reviewed, keine offenen Fragen |
| Phase 2 | Alle 3 Output-Dateien erstellt, Feature-Matrix konsolidiert |
| Phase 3 | IA + Personas + Seitentypen + Rollout-Plan dokumentiert und freigegeben |
| Phase 4 | Pro Umsetzungsphase: Design → Review → Build → Test → Launch |
