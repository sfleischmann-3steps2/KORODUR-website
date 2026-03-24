# Feature-Matrix — Konsolidierte Synthese
**Stand:** 2026-03-24 | **Version:** 1.0 | **Phase:** 2 – Benchmark (Sprint 2.3)
**Quellen:** competitors.md + zielgruppenplattformen.md

---

## 1. Wettbewerber Feature-Matrix

| Feature | MC-Bau (INT) | Flowcrete | Vandex | Sika | Mapei | Ardex | MC-Bau (DE) | Chemotechnik | Knauf | Weber | **KORODUR** |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Planerbereich | Nein | Nein | Nein | Teilw. | **Ja** | Teilw. | Nein | Nein | **Ja** | **Ja** | **Nein** |
| Ausschreibungstexte | Nein | Nein | Nein | Teilw. | Teilw. | **Ja** | Via Heinze | Nein | **Ja (GAEB)** | **Ja** | Teilw. (HTML/PDF) |
| GAEB-Export | Nein | Nein | Nein | Nein | Nein | Unklar | Nein | Nein | **Ja** | **Ja** | **Nein** |
| BIM-Objekte | Nein | Nein | Nein | Teilw. | **Ja** | **Ja** | Via Heinze | Nein | **Ja** | **Ja** | **Nein** |
| EPDs | **Ja** | Nein | Nein | **Ja** | **Ja** | Teilw. | Via Heinze | Nein | Teilw. | Teilw. | **Nein** |
| Produktfinder | Nein | Nein | Nein | **Ja** | Teilw. | **Ja** | Nein | Nein | **Ja** | Nein | **Nein** |
| Konfigurator/Berater | Nein | Nein | Nein | **Ja (10+)** | **Ja** | **Ja** | Nein | Nein | **Ja** | Nein | **Nein** |
| Verbrauchsrechner | Nein | Nein | Nein | **Ja** | **Ja** | **Ja** | Nein | Nein | Nein | Nein | **Nein** |
| TDS ohne Login | **Ja** | **Ja** | **Ja** | **Ja** | **Ja** | **Ja** | **Ja** | Unklar | **Ja** | **Ja** | **Ja** |
| Referenzprojekte | **Ja** | **Ja** | Minimal | **Ja** | Teilw. | Teilw. | **Ja** | **Ja** | Teilw. | Teilw. | **Ja (~130)** |
| Ref.-Produkt-Link | Teilw. | Nein | Nein | Nein | Nein | Nein | Teilw. | **Ja** | Nein | Nein | **Nein** |
| Verarbeitungsvideos | Nein | Nein | **Ja** | Teilw. | Teilw. | **Ja** | Nein | Nein | Teilw. | Teilw. | **Nein** |
| Schulungen/Academy | Nein | Nein | Nein | **Ja** | Teilw. | **Ja** | Nein | Nein | Teilw. | **Ja** | **Nein** |
| Haendlersuche | Nein | Nein | Nein | Teilw. | Nein | **Ja** | Nein | Nein | **Ja** | **Ja** | **Nein** |
| Download-Center | **Ja** | **Ja** | Teilw. | **Ja** | **Ja** | **Ja** | **Ja** | Nein | **Ja** | **Ja** | **Nein** |
| CTAs auf Seiten | Teilw. | Teilw. | Teilw. | **Ja** | Teilw. | **Ja** | Teilw. | Nein | **Ja** | **Ja** | **Nein** |
| Zielgruppen-Navigation | Nein | **Ja (Sectors)** | Nein | Teilw. | **Ja** | Teilw. | Nein | Nein | **Ja** | Teilw. | **Nein** |
| Mehrsprachig | DE/EN/RU/SK | EN (Regionen) | EN/DE | 60+ | 40+ | DE/EN/TR/PL | DE | Nur DE | DE | DE | DE/EN/FR |
| Mobile-optimiert | **Ja** | **Ja** | Teilw. | **Ja** | **Ja** | **Ja** | **Ja** | Nein | **Ja** | **Ja** | Teilw. |
| Moderner Tech-Stack | Teilw. | Teilw. | Nein | **Ja (React)** | Teilw. | Teilw. | **Ja (MODX)** | Nein | **Ja (Next.js)** | Teilw. | Nein (WP+Elementor) |

**KORODUR-Bilanz: 2 von 20 Features vorhanden (TDS ohne Login + Referenzprojekte). 18 Features fehlen oder sind unzureichend.**

---

## 2. Differenzierungspotenziale (was kein Wettbewerber gut macht)

| Chance | Warum es funktionieren kann | Aufwand |
|--------|---------------------------|---------|
| **Integrierte Produkt-Referenz-Verknuepfung** | Kein Wettbewerber verbindet Produkt → Referenz → Technik → Ausschreibung nahtlos | Mittel |
| **Technische Daten als HTML** (nicht nur PDF) | Alle verstecken Daten in PDFs — SEO-Goldgrube + Mobile-Vorteil | Mittel |
| **Transparente Produktvergleiche** | Kein Wettbewerber bietet ehrliche Vergleichstabellen eigener Produkte | Niedrig |
| **Spezialisierung kommunizieren** | Tier-2/3 sind Generalisten — KORODUR als Hartstoff-Experte positionieren | Niedrig |
| **Nachhaltigkeit im Industrieboden** | Kein Tier-1-Wettbewerber kommuniziert das ueberzeugend | Hoch |
| **Mehrsprachiger Verarbeiter-Content** | Keiner bietet umfassend mehrsprachige Praxisinhalte | Mittel |

---

## 3. Priorisierte Feature-Roadmap

### Prioritaet 1 — Quick Wins & Must-Haves (sofort starten)
*Niedriger bis mittlerer Aufwand, hoher Impact*

| # | Feature | Zielgruppe | Aufwand | Inspiration |
|---|---------|-----------|---------|-------------|
| 1 | **CTAs auf jeder Seite** ("Jetzt anfragen", "Beraten lassen", Tel.) | Alle | Niedrig | Hilti |
| 2 | **Zielgruppen-Einstiege Homepage** ("Fuer Planer / Verarbeiter / Haendler") | Alle | Niedrig | Heinze, Rockwool |
| 3 | **YouTube-Videos einbetten** auf Produktseiten | Verarbeiter | Niedrig | Bauhandwerk |
| 4 | **Technische Daten als HTML** auf Produktseiten | Planer/Verarbeiter | Mittel | Schoeck, Hilti |
| 5 | **Download-Center** (TDS, SDS, DoP, LV — filterbar, ein Ort) | Alle | Mittel | Schoeck, Rockwool |
| 6 | **Ausschreibungstexte GAEB-Format** pro Produkt | Planer | Mittel | Heinze, Knauf |
| 7 | **Haendlerfinder** (Karte + PLZ + "Wo kaufen?" auf Produktseiten) | Handel | Mittel | Raab Karcher |

### Prioritaet 2 — Strategische Features (Phase 3/4)
*Mittlerer bis hoher Aufwand, hoher strategischer Impact*

| # | Feature | Zielgruppe | Aufwand | Inspiration |
|---|---------|-----------|---------|-------------|
| 8 | **Produktfinder nach Anwendung** (Entscheidungsbaum) | Planer/Verarbeiter | Hoch | Hilti "Make it fit" |
| 9 | **Referenzprojekte mit Produktverknuepfung** | Planer | Mittel | Chemotechnik, Heinze |
| 10 | **Mengen-/Verbrauchsrechner** | Verarbeiter | Niedrig | Knauf Insulation |
| 11 | **EPDs erstellen** fuer Kernprodukte | Planer | Hoch | Rockwool, Mapei |
| 12 | **Nachhaltigkeitsbereich ausbauen** | Planer | Hoch | Rockwool |
| 13 | **Heinze-Profil optimieren** + AUSSCHREIBEN.DE | Planer | Niedrig | MC-Bau, Schoeck |
| 14 | **Geschuetzter Haendlerbereich** (Login) | Handel | Hoch | Wuerth, Hagebau |
| 15 | **Mobile-First Redesign** | Alle | Hoch | Hilti |
| 16 | **FAQ pro Produktgruppe** | Verarbeiter | Niedrig | - |
| 17 | **Newsletter** fuer Haendler/Planer | Handel/Planer | Niedrig | Heinze |
| 18 | **Fachwissen-Blog** | Alle | Mittel | BauNetz Wissen |

### Prioritaet 3 — Langfristige Investitionen (spaeter)
*Hoher Aufwand, langfristiger Wert*

| # | Feature | Zielgruppe | Aufwand |
|---|---------|-----------|---------|
| 19 | BIM-Objekte fuer Kernprodukte | Planer | Sehr hoch |
| 20 | Vergleichstabellen (HE 3 vs HE 65 etc.) | Alle | Mittel |
| 21 | PIM-System (crossbase o.ae.) | Intern | Sehr hoch |
| 22 | Schulungs-/Webinar-Plattform | Verarbeiter | Mittel |
| 23 | Normen-Referenzseite | Planer | Mittel |
| 24 | Praxisberichte / Projekt des Monats | Alle | Mittel |

---

## 4. Strategische Kernbotschaft

### KORODUR's groesste Chance:
> **Als Spezialist fuer mineralische Industrieboeden die erste wirklich nutzerfreundliche B2B-Website der Nische bauen.**

Die direkten Wettbewerber (MC-Bauchemie, Flowcrete, Vandex, Chemotechnik) sind digital genauso schwach. Die Grossen (Sika, Mapei, Knauf) sind stark, aber Generalisten. KORODUR kann mit fokussierter Umsetzung der Prioritaet-1-Features einen **First-Mover-Vorteil** in der Nische erreichen.

### Was KORODUR NICHT braucht:
- Eigene BIM-Software/Plugins (zu komplex)
- E-Commerce/Online-Shop (Vertrieb laeuft ueber Fachhandel)
- Community/Forum (zu wenig Nutzer)
- Eigene Bemessungssoftware (Produkte nicht berechnungsintensiv genug)
- Fleet Management / Tool-Tracking (anderes Geschaeftsmodell)

---

*Konsolidiert aus Wettbewerber-Benchmark (10 Unternehmen) und Zielgruppenplattformen-Benchmark (18 Plattformen) am 2026-03-24.*
