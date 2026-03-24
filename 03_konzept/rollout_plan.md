# Rollout-Plan: KORODUR Website Relaunch
**Stand:** 2026-03-24 | **Version:** 1.0 | **Phase:** 3 -- Konzept
**Erstellt von:** Claude Code (Agent 0 -- Projektleitung)
**Basis:** technical_audit.md, ia_new.md, zielgruppen.md, feature_matrix.md

---

## Executive Summary

Der Relaunch von korodur.de erfolgt in **5 Phasen** (Phase 0--4) ueber einen Zeitraum von ca. **12--15 Monaten**. Jede Phase liefert sichtbare, oeffentliche Ergebnisse. WordPress bleibt vorerst als CMS; ein Tech-Stack-Wechsel wird fruehestens in Phase 4 evaluiert.

**Kernprinzipien:**
- Schrittweise statt Big Bang -- Alt und Neu laufen parallel
- Analytics SOFORT -- ohne Daten kein messbarer Erfolg
- Jede Phase adressiert alle drei Zielgruppen (Planer, Verarbeiter, Handel)
- SEO-Integritaet: 301-Redirects fuer alle URL-Aenderungen, keine Indexverluste
- Realistisch fuer Mittelstaendler mit AI-Team (keine Enterprise-Agentur)

**Phasen-Ueberblick:**

| Phase | Titel | Zeitrahmen | Kern-Deliverables |
|-------|-------|-----------|-------------------|
| **0** | Sofort-Massnahmen | Woche 1--2 | Analytics, SEO-Bugfixes, Monitoring-Baseline |
| **1** | Quick Wins | Woche 3--8 | CTAs, Videos, Meta-Tags, Heinze/AUSSCHREIBEN.DE |
| **2** | Strukturelle Verbesserungen | Woche 9--20 | Neue Navigation, Download-Center, Haendlerfinder, Homepage-Relaunch |
| **3** | Neue Inhalte & Features | Woche 21--40 | Planerbereich, GAEB, HTML-Produktdaten, Anwendungsseiten, Verbrauchsrechner |
| **4** | Langfristige Investitionen | Ab Woche 41 | EPDs, BIM, Haendlerportal, ggf. Tech-Stack-Wechsel |

```
Woche:  1    4    8    12   16   20   24   28   32   36   40   44   48   52+
        |----|----|----|----|----|----|----|----|----|----|----|----|----|----|
Phase 0 |████|
Phase 1      |█████████|
Phase 2                |████████████████████|
Phase 3                                    |████████████████████████████|
Phase 4                                                                |████→
        ─────────────────────────────────────────────────────────────────────→
        Analytics laeuft ab Woche 1 durch ──────────────────────────────────→
```

---

## Phase 0 -- Sofort-Massnahmen (Woche 1--2)

**Ziel:** Messbare Baseline schaffen und kritische Bugs fixen, BEVOR der Relaunch beginnt. Ohne Analytics-Daten ist kein Relaunch-Erfolg nachweisbar.

### 0.1 Scope

| # | Massnahme | Aufwand | Verantwortlich | Prio |
|---|----------|---------|----------------|------|
| 0.1 | **GA4 ODER Matomo installieren** | 2--4h | Steffi (AI-Team) | KRITISCH |
| 0.2 | **H1-Tag auf Homepage (DE + EN + FR) setzen** | 30 Min | Steffi (WP-Backend) | KRITISCH |
| 0.3 | **Schema.org Breadcrumb-Bug fixen** ("Maison" → "Startseite") | 30 Min | Steffi (Yoast/WPML-Config) | HOCH |
| 0.4 | **URL-Tippfehler korrigieren** (`/dattenblaetter/` → `/datenblaetter/` mit 301-Redirect) | 15 Min | Steffi (WP-Backend) | HOCH |
| 0.5 | **EN-Homepage Title fixen** ("Homepage -- korodur" → beschreibender Title mit Keywords) | 15 Min | Steffi (Yoast SEO) | HOCH |
| 0.6 | **OG:Image auf Homepage setzen** (Social-Sharing-Vorschaubild) | 30 Min | Steffi (Yoast SEO) | MITTEL |
| 0.7 | **Hreflang-Tags im HTML-Head aktivieren** (WPML-Einstellung) | 1h | Steffi (WPML-Config) | MITTEL |
| 0.8 | **"bauarbeiten-im-gange" deindexieren** (noindex oder 301 auf Homepage) | 15 Min | Steffi (WP-Backend) | NIEDRIG |

### 0.2 Abhaengigkeiten

- **Keine** -- alles kann sofort auf der bestehenden WordPress-Site umgesetzt werden
- GA4 braucht ggf. Abstimmung mit Complianz-Cookie-Consent (Statistics-Kategorie)
- Datenschutzerklaerung muss um GA4/Matomo-Abschnitt ergaenzt werden

### 0.3 Geschaetzter Zeitrahmen

- **1--2 Wochen** (inkl. GA4-Test und DSGVO-Anpassung)
- Analytics muss ab Tag 1 laufen -- jeder Tag ohne Daten ist ein verlorener Tag

### 0.4 Definition of Done

- [ ] GA4 oder Matomo liefert Seitenaufrufe, Nutzerquellen und Echtzeit-Daten
- [ ] Complianz-Cookie-Banner zeigt Analytics korrekt unter "Statistics"
- [ ] Datenschutzerklaerung um Analytics-Abschnitt ergaenzt
- [ ] H1 auf DE-, EN- und FR-Homepage vorhanden (genau 1 pro Seite)
- [ ] Schema.org Breadcrumb zeigt "Startseite" (DE), "Home" (EN), "Accueil" (FR)
- [ ] `/service/dattenblaetter/` leitet per 301 auf `/service/datenblaetter/` weiter
- [ ] EN-Homepage Title ist beschreibend (z.B. "Industrial Floor Systems & Repair Mortars -- KORODUR")
- [ ] OG:Image auf allen drei Homepages gesetzt

---

## Phase 1 -- Quick Wins (Woche 3--8)

**Ziel:** Sichtbare Verbesserungen auf der bestehenden WordPress-Site, die sofort Conversion und User Experience verbessern. Kein Redesign, keine Strukturaenderung -- nur Ergaenzungen.

### 1.1 Scope

| # | Feature | Zielgruppe | Aufwand | Abhaengigkeit |
|---|---------|-----------|---------|---------------|
| 1.1 | **CTAs auf allen Seiten** ("Jetzt anfragen", Telefonnummer, "Beratung") | Alle | Niedrig (Elementor-Widget wiederverwendbar) | Keine |
| 1.2 | **YouTube-Videos auf Produktseiten einbetten** | Verarbeiter | Niedrig (YouTube-URLs existieren bereits) | Keine |
| 1.3 | **Meta-Tags systematisch fixen** (Title, Description fuer Top-30 Seiten) | SEO | Niedrig (Yoast-Felder befuellen) | Phase 0 abgeschlossen |
| 1.4 | **Technische Hotline prominent auf jeder Seite** (Sticky Header/Footer) | Verarbeiter | Niedrig (Elementor-Template) | Telefonnummer von KORODUR |
| 1.5 | **Heinze-Profil optimieren / erstellen** | Planer | Niedrig (externe Plattform) | Produktdaten von KORODUR |
| 1.6 | **AUSSCHREIBEN.DE Praesenz aufbauen** | Planer | Niedrig (externe Plattform) | Ausschreibungstexte von KORODUR |
| 1.7 | **Footer-Redesign** (Kontaktdaten, Social Media, Quick Links fuer alle 3 Zielgruppen) | Alle | Niedrig (Elementor-Footer) | Keine |
| 1.8 | **Verwandte Produkte / Cross-Links auf Produktseiten** | Alle | Niedrig (WooCommerce "Related Products" oder manuell) | Keine |
| 1.9 | **Referenz-Highlights auf Homepage** (3--4 ausgewaehlte Projekte mit Bild) | Alle | Niedrig (Elementor-Sektion) | Bilder von KORODUR |

### 1.2 Abhaengigkeiten

| Von KORODUR benoetigt | Fuer Feature | Deadline |
|-----------------------|-------------|----------|
| YouTube-Kanal-Link + gewuenschte Videos pro Produkt | 1.2 | Woche 3 |
| Technische Hotline-Nummer (dediziert oder Zentrale?) | 1.4 | Woche 3 |
| Top-3 Referenzprojekte mit hochaufloesenden Bildern | 1.9 | Woche 4 |
| Heinze-Zugangsdaten oder Freigabe fuer Profilerstellung | 1.5 | Woche 5 |
| Ausschreibungstexte (mindestens Top-10 Produkte) | 1.6 | Woche 6 |

### 1.3 Geschaetzter Zeitrahmen

- **6 Wochen** (Woche 3--8)
- Parallelisierbar: CTAs + Videos + Meta-Tags koennen gleichzeitig bearbeitet werden
- Heinze + AUSSCHREIBEN.DE laufen parallel, da externe Plattformen

### 1.4 Definition of Done

- [ ] CTA-Button ("Jetzt anfragen" oder "Beratung") auf mindestens 80% der Inhaltsseiten
- [ ] YouTube-Videos auf mindestens 10 Produktseiten eingebettet
- [ ] Meta-Title und Meta-Description fuer die Top-30-Seiten (nach Traffic) individuell gesetzt
- [ ] Technische Hotline-Nummer in Header oder Sticky-Element auf jeder Seite sichtbar
- [ ] Heinze-Profil angelegt oder aktualisiert mit Basisdaten + Top-10-Produkten
- [ ] AUSSCHREIBEN.DE-Profil angelegt (mindestens Firmeneintrag)
- [ ] Footer zeigt Kontaktdaten, Zielgruppen-Quick-Links, Social Media
- [ ] Mindestens 5 Produktseiten haben "Verwandte Produkte"-Block
- [ ] Referenz-Highlights-Sektion auf Homepage (DE)

### 1.5 Erfolgskriterien (messbar ab Woche 10)

- Baseline-Traffic bekannt (aus Phase 0 Analytics)
- CTR aus Suchergebnissen steigt (durch bessere Meta-Tags)
- Kontaktanfragen steigen (durch CTAs -- Formular-Submissions tracken!)
- Verweildauer auf Produktseiten steigt (durch Videos)

---

## Phase 2 -- Strukturelle Verbesserungen (Woche 9--20)

**Ziel:** Die Informationsarchitektur grundlegend verbessern. Neue Navigation, zentrales Download-Center, Haendlerfinder, Zielgruppen-Einstiege auf Homepage. Dies ist die groesste Phase mit den meisten WordPress-Aenderungen.

### 2.1 Scope

| # | Feature | Zielgruppe | Aufwand | Abhaengigkeit |
|---|---------|-----------|---------|---------------|
| 2.1 | **Neue Hauptnavigation implementieren** (6 Punkte + Mega-Menue) | Alle | HOCH | ia_new.md als Vorlage, alle Seiten muessen existieren |
| 2.2 | **Zielgruppen-Einstiege auf Homepage** ("Fuer Planer / Verarbeiter / Haendler") | Alle | MITTEL | Zielgruppen-Landingpages muessen existieren |
| 2.3 | **Download-Center** (TDS, SDS, DoP, LV -- filterbar, ein Ort) | Alle | HOCH | Alle PDFs gesammelt + kategorisiert |
| 2.4 | **Haendlerfinder** (Karte + PLZ-Suche + "Wo kaufen?" auf Produktseiten) | Handel | HOCH | Haendlerliste von KORODUR Vertrieb |
| 2.5 | **Homepage-Relaunch** (neue Struktur gemaess ia_new.md Wireframe) | Alle | HOCH | 2.1 + 2.2 muessen stehen |
| 2.6 | **Doppelstruktur aufloesen** (`/bereiche/` + `/produkt-kategorie/` → `/produkte/`) | SEO | HOCH | Redirect-Map erstellen |
| 2.7 | **URL-Redirects Phase 2** (301 fuer alle zusammengelegten Seiten) | SEO | MITTEL | Redirect-Map als CSV |
| 2.8 | **Produktgruppen-Seiten neu gestalten** (Bereiche-Content + Kategorie-Listing zusammen) | Alle | MITTEL | 2.6 abgeschlossen |
| 2.9 | **FAQ pro Produktgruppe** | Verarbeiter | NIEDRIG | FAQ-Inhalte von KORODUR Technik |
| 2.10 | **Newsletter-Anmeldung integrieren** (Footer + Zielgruppen-Landingpages) | Alle | NIEDRIG | Newsletter-Tool auswaehlen (z.B. Mailchimp, Brevo) |

### 2.2 Abhaengigkeiten

| Von KORODUR benoetigt | Fuer Feature | Deadline |
|-----------------------|-------------|----------|
| **Vollstaendige Haendlerliste** (Name, PLZ, Ort, Adresse, ggf. Koordinaten) | 2.4 | Woche 10 |
| **Alle PDFs digital** (TDS, SDS, DoP, LV -- pro Produkt kategorisiert) | 2.3 | Woche 10 |
| **Freigabe neue Navigation** durch GF | 2.1 | Woche 9 |
| **Freigabe neue Homepage-Struktur** durch GF | 2.5 | Woche 12 |
| **FAQ-Inhalte** (Top-5 Fragen pro Produktgruppe) | 2.9 | Woche 14 |
| **Newsletter-Datenschutz-Freigabe** (Anwalt/DSB) | 2.10 | Woche 12 |

### 2.3 SEO-Risikomanagement (URL-Aenderungen)

**KRITISCH:** Phase 2 veraendert die URL-Struktur grundlegend. Ohne saubere 301-Redirects droht massiver SEO-Verlust.

| Risiko | Gegenmassnahme |
|--------|---------------|
| Indexverlust bei URL-Umstellung | Vollstaendige Redirect-Map (858 URLs) als CSV VOR Go-Live erstellen |
| Broken Links von externen Seiten | Google Search Console ueberwachen, Crawl-Errors pruefen |
| Doppelte Inhalte waehrend Uebergang | Canonical-Tags setzen, alte Seiten nicht sofort loeschen |
| Sitemap-Inkonsistenzen | Neue Sitemap generieren, alte URLs NICHT mehr in Sitemap |

**Vorgehen:**
1. Redirect-Map als CSV erstellen (ALT-URL → NEU-URL, alle 858 Eintraege)
2. Redirects in WordPress implementieren (Redirection-Plugin oder .htaccess)
3. Alte Seiten auf "Draft" setzen (nicht loeschen!)
4. Neue Sitemap an Google Search Console uebermitteln
5. 4 Wochen nach Go-Live: Crawl-Errors pruefen, Redirects validieren

### 2.4 Geschaetzter Zeitrahmen

- **12 Wochen** (Woche 9--20)
- Sprint-Empfehlung:
  - Woche 9--10: Navigation + Redirect-Map vorbereiten
  - Woche 11--14: Download-Center + Haendlerfinder entwickeln
  - Woche 15--17: Homepage-Relaunch + Zielgruppen-Einstiege
  - Woche 18--20: URL-Umstellung, Redirects, Testing, Go-Live Phase 2

### 2.5 Definition of Done

- [ ] Neue 6-Punkte-Navigation live (Produkte, Anwendungen, Fuer Planer, Service & Downloads, Unternehmen, Kontakt)
- [ ] Mega-Menue funktional fuer alle 6 Navigationspunkte
- [ ] Homepage zeigt Zielgruppen-Einstiege (3 Kacheln), Produktbereiche, USPs, Referenz-Highlights
- [ ] Download-Center unter `/service/downloads/` live, filterbar nach Typ (TDS, SDS, DoP, LV) und Produktgruppe
- [ ] Haendlerfinder unter `/service/haendlerfinder/` live mit Karte und PLZ-Suche
- [ ] "Wo kaufen?"-Button auf mindestens 20 Produktseiten
- [ ] Alle 301-Redirects aktiv (Stichprobe: 50 alte URLs pruefen)
- [ ] Google Search Console zeigt keine neuen 404-Fehler
- [ ] Newsletter-Anmeldung im Footer und auf Zielgruppen-Landingpages

---

## Phase 3 -- Neue Inhalte & Features (Woche 21--40)

**Ziel:** Die grossen Differenzierungsfeatures umsetzen, die KORODUR von Wettbewerbern abheben. Diese Phase erfordert am meisten fachlichen Input von KORODUR Produktmanagement und Vertrieb.

### 3.1 Scope

| # | Feature | Zielgruppe | Aufwand | Abhaengigkeit |
|---|---------|-----------|---------|---------------|
| 3.1 | **Planerbereich aufbauen** (`/planer/` + 6 Unterseiten) | Planer | HOCH | Fachlicher Content von KORODUR |
| 3.2 | **Ausschreibungstexte GAEB-Format** (Download pro Produkt) | Planer | HOCH | GAEB-Dateien erstellen (ORCA-Export aus Ausschreibungstexte-Projekt) |
| 3.3 | **Technische Daten als HTML auf Produktseiten** | Planer, Verarbeiter | HOCH | Produktdatenbank (Notion) als Quelle |
| 3.4 | **Anwendungsseiten erstellen** (`/anwendungen/` + 9 Unterseiten) | Verarbeiter, Planer | HOCH | Branchenspezifischer Content + Bilder von KORODUR |
| 3.5 | **Referenz-Produkt-Verknuepfung** | Planer | MITTEL | Referenz-DB (117 Eintraege) mit Produkten mappen |
| 3.6 | **Verbrauchsrechner** (kg/m2 x Flaeche) | Verarbeiter | MITTEL | Verbrauchswerte pro Produkt von KORODUR Technik |
| 3.7 | **Produktfinder nach Anwendung** (Entscheidungsbaum) | Planer, Verarbeiter | HOCH | Entscheidungslogik von KORODUR Technik |
| 3.8 | **Normen-Referenzseite** (`/planer/normen-zulassungen/`) | Planer | MITTEL | Normenliste von KORODUR QM |
| 3.9 | **Systemaufbauten** (Schichtaufbau-Diagramme) | Planer | MITTEL | Technische Zeichnungen von KORODUR |
| 3.10 | **Produktvergleichstabellen** (z.B. HE 3 vs. HE 65) | Alle | MITTEL | Produktdatenbank als Quelle |
| 3.11 | **Fachwissen-Blog starten** (2 Beitraege/Monat) | SEO, Alle | NIEDRIG (pro Beitrag) | Redaktionsplan + Fachautoren |

### 3.2 Abhaengigkeiten (KRITISCH -- Content von KORODUR)

| Von KORODUR benoetigt | Fuer Feature | Deadline | Anmerkung |
|-----------------------|-------------|----------|-----------|
| **GAEB-Dateien** (Top-20 Produkte) | 3.2 | Woche 22 | Koennen aus Ausschreibungstexte-Projekt (ORCA) exportiert werden |
| **Technische Datenblatt-Werte als strukturierte Daten** | 3.3 | Woche 22 | Produktdatenbank-Projekt liefert 28 Properties pro Produkt |
| **Branchenspezifische Inhalte** (Logistik, Automotive, Food etc.) | 3.4 | Woche 24 | Texte, Bilder, typische Anforderungen pro Branche |
| **Referenz-Produkt-Mapping** (welches Produkt in welcher Referenz?) | 3.5 | Woche 24 | Vertrieb/Technik muss 117 Referenzen zuordnen |
| **Verbrauchswerte** (kg/m2 pro Schichtdicke pro Produkt) | 3.6 | Woche 26 | Technik liefert Berechnungsformeln |
| **Entscheidungsbaum-Logik** (Anforderung → Produktempfehlung) | 3.7 | Woche 28 | Workshop mit Technik + Vertrieb notwendig |
| **Normenliste** mit Zuordnung zu Produkten | 3.8 | Woche 26 | QM-Abteilung |
| **Systemaufbau-Zeichnungen** (digital, pro Anwendung) | 3.9 | Woche 30 | Technik erstellt oder digitalisiert vorhandene Zeichnungen |

### 3.3 Synergie mit bestehenden Projekten

| Projekt | Liefert fuer Phase 3 | Repo |
|---------|---------------------|------|
| **Produktdatenbank** | 28 Properties pro Produkt → HTML-Produktdaten (3.3) | `C:\Users\stefa\Produktdatenbank` |
| **Ausschreibungstexte-Produkte** | 193 LV-Positionen → GAEB-Export (3.2) | `C:\Users\stefa\Ausschreibungstexte-Produkte` |
| **Korodur-Referenzen** | 117 Referenzen in Notion → Produkt-Verknuepfung (3.5) | `C:\Users\stefa\Korodur-Referenzen` |
| **KORODUR-Translation** | 572 Fachbegriffe DE/EN/FR → mehrsprachige Inhalte | `C:\Users\stefa\KORODUR-Translation` |

### 3.4 Geschaetzter Zeitrahmen

- **20 Wochen** (Woche 21--40)
- Sprint-Empfehlung:
  - Woche 21--24: Planerbereich Grundstruktur + Ausschreibungstexte
  - Woche 25--28: HTML-Produktdaten + Anwendungsseiten (erste 4 Branchen)
  - Woche 29--32: Verbrauchsrechner + Referenz-Produkt-Verknuepfung
  - Woche 33--36: Produktfinder + Systemaufbauten
  - Woche 37--40: Produktvergleiche, Normen-Seite, Blog-Start, Testing

### 3.5 Definition of Done

- [ ] Planerbereich unter `/planer/` live mit mindestens 4 Unterseiten
- [ ] GAEB-Downloads fuer Top-20 Produkte verfuegbar
- [ ] Technische Kerndaten (mindestens 5 Werte) als HTML auf allen Produktseiten
- [ ] Mindestens 4 Anwendungsseiten (Logistik, Automotive, Lebensmittel, Trinkwasser) live
- [ ] Referenzprojekte mit Produkten verknuepft (mindestens 50 von 117)
- [ ] Verbrauchsrechner funktional fuer mindestens 10 Produkte
- [ ] Produktfinder-Prototyp live (mindestens 2 Entscheidungspfade)
- [ ] Blog mit mindestens 4 Fachbeitraegen

---

## Phase 4 -- Langfristige Investitionen (ab Woche 41)

**Ziel:** Strategische Features, die KORODUR langfristig als digitalen Vorreiter in der Nische positionieren. Hoehere Investitionen, laengere Vorlaufzeiten, teilweise externe Partner notwendig.

### 4.1 Scope

| # | Feature | Zielgruppe | Aufwand | Externe Partner? |
|---|---------|-----------|---------|-----------------|
| 4.1 | **EPDs erstellen** fuer Kernprodukte (Top-10) | Planer | SEHR HOCH | Ja -- IBU-Akkreditierung, ~5.000--10.000 EUR/EPD |
| 4.2 | **BIM-Objekte** fuer Kernprodukte | Planer | SEHR HOCH | Ja -- BIM-Dienstleister |
| 4.3 | **Geschuetztes Haendlerportal** (Login, Preislisten, Konditionen, Marketing) | Handel | HOCH | Ggf. WP-Membership-Plugin oder Custom-Entwicklung |
| 4.4 | **PIM-System evaluieren** (crossbase, Akeneo, Pimcore) | Intern | HOCH (Evaluation) | Ja -- PIM-Anbieter |
| 4.5 | **Tech-Stack-Wechsel evaluieren** (Next.js/Astro + Headless CMS) | Intern | HOCH (Evaluation) | Ggf. Agentur |
| 4.6 | **Schulungs-/Webinar-Plattform** | Verarbeiter | MITTEL | Ggf. LMS-Plugin oder externe Plattform |
| 4.7 | **Mobile-First Redesign** (komplettes Frontend) | Alle | SEHR HOCH | Abhaengig von 4.5 |
| 4.8 | **Internationalisierung ausbauen** (weitere Sprachen, regionale Inhalte) | Alle | HOCH | Uebersetzer |

### 4.2 Entscheidungspunkte

| Entscheidung | Wann | Entscheidungstraeger | Kriterien |
|-------------|------|---------------------|-----------|
| EPD-Investition starten? | Woche 41 | GF + Produktmanagement | Nachfrage von Planern, DGNB-Pflicht-Entwicklung |
| BIM-Investition starten? | Woche 45 | GF + Vertrieb | Kundenanfragen, Wettbewerber-Druck |
| Haendlerportal Scope definieren | Woche 42 | GF + Vertrieb | Anzahl aktive Haendler, digitale Affinitaet |
| WordPress behalten oder wechseln? | Woche 48 | GF + Steffi | Performance-Daten, Wartungsaufwand, Feature-Anforderungen |
| PIM-System Ja/Nein? | Woche 50 | GF + Produktmanagement | Anzahl Produkte, Mehrsprachigkeit, Datenkonsistenz |

### 4.3 Geschaetzter Zeitrahmen

- **Fortlaufend ab Woche 41** (open-ended)
- EPDs: 6--12 Monate Vorlauf pro Produkt (IBU-Prozess)
- BIM: 3--6 Monate pro Produktgruppe
- Haendlerportal: 8--12 Wochen Entwicklung
- Tech-Stack-Wechsel: 6--12 Monate (wenn entschieden)

### 4.4 Definition of Done (pro Milestone)

- [ ] EPDs: Mindestens 3 EPDs fuer Kernprodukte veroeffentlicht (IBU/OEKOBAUDAT)
- [ ] BIM: Mindestens 5 BIM-Objekte auf BIMobject/eigener Website
- [ ] Haendlerportal: Login funktional, Preislisten abrufbar, mindestens 10 Haendler ongeboardet
- [ ] Tech-Stack-Entscheidung: Evaluierungsbericht mit Empfehlung liegt vor

---

## Risiken & Abhaengigkeiten

### Hohe Risiken

| # | Risiko | Wahrscheinlichkeit | Impact | Gegenmassnahme |
|---|--------|-------------------|--------|---------------|
| R1 | **SEO-Verlust bei URL-Umstellung** (Phase 2) | MITTEL | HOCH | Vollstaendige 301-Redirect-Map, 4 Wochen Monitoring nach Go-Live, Search Console ueberwachen |
| R2 | **Content-Lieferung durch KORODUR verzoegert sich** | HOCH | HOCH | Frueh einfordern, Deadlines klar kommunizieren, MVP-Ansatz (erst Top-10 Produkte, dann Rest) |
| R3 | **WordPress-Performance-Probleme** bei neuen Features | MITTEL | MITTEL | Caching optimieren, ggf. Features als externe Microservices (z.B. Haendlerfinder als iFrame) |
| R4 | **Kein GF-Buy-in fuer Investitionen** (Phase 3+4) | NIEDRIG | HOCH | Erfolge aus Phase 1+2 als Argument nutzen, KPIs praesentieren |
| R5 | **WooCommerce-Umbau bricht bestehende Funktionen** | MITTEL | HOCH | Staging-Umgebung nutzen, nie direkt auf Production arbeiten |

### Mittlere Risiken

| # | Risiko | Wahrscheinlichkeit | Impact | Gegenmassnahme |
|---|--------|-------------------|--------|---------------|
| R6 | **WPML-Konflikte bei Navigations-Aenderungen** | MITTEL | MITTEL | Aenderungen erst auf DE, dann EN/FR uebertragen. WPML-String-Translation pruefen |
| R7 | **Cloudflare-Caching verzoegert Aenderungen** | NIEDRIG | NIEDRIG | Cache-Purge-Routine nach jedem Deploy |
| R8 | **Elementor-Limitierungen bei Mega-Menue** | MITTEL | MITTEL | Elementor Pro Hat Mega-Menu-Feature; ggf. JetMenu als Alternative |
| R9 | **Haendler wollen nicht im Haendlerfinder gelistet werden** | NIEDRIG | MITTEL | Vorher Vertrieb einbinden, Haendler-Nutzen kommunizieren |

### Technische Risiken (WordPress-spezifisch)

| Bereich | Risiko | Empfehlung |
|---------|--------|-----------|
| **Plugin-Konflikte** | 14+ Plugins → Updates koennen Konflikte verursachen | Staging-Umgebung pflegen, Updates testen |
| **Performance** | 30+ JS-Dateien, jQuery-Overhead | WP-Optimize Config optimieren, unnoetige Plugins deaktivieren |
| **WooCommerce-Overhead** | Shop-Funktionen (Cart, Checkout) auf jeder Seite geladen | WooCommerce-Assets nur auf Produktseiten laden (via Plugin oder functions.php) |
| **Elementor-Abhaengigkeit** | Alle Seiten an Elementor gebunden → Wechsel teuer | Kurzfristig akzeptieren, in Phase 4 evaluieren |

---

## Stakeholder & Verantwortlichkeiten

### RACI-Matrix

| Aufgabe | Steffi (AI-Team) | KORODUR Produktmgmt | KORODUR Vertrieb | KORODUR Technik | GF |
|---------|------------------|--------------------|-----------------|-----------------|----|
| Analytics einrichten | **R/A** | I | I | -- | I |
| SEO-Bugfixes | **R/A** | -- | -- | -- | I |
| CTAs + Videos | **R/A** | C | C | -- | I |
| Neue Navigation | **R** | C | C | -- | **A** |
| Homepage-Redesign | **R** | C | C | -- | **A** |
| Download-Center | **R** | **C** (PDFs liefern) | -- | **C** (TDS pruefen) | I |
| Haendlerfinder | **R** | -- | **C** (Haendlerliste) | -- | **A** |
| Planerbereich | **R** | **C** (Normen, Systeme) | -- | **C** (Technik-Content) | **A** |
| GAEB-Dateien | **R** | **C** (Texte pruefen) | -- | **C** (Technik pruefen) | I |
| HTML-Produktdaten | **R** | **C** (Daten pruefen) | -- | **C** (Werte liefern) | I |
| Anwendungsseiten | **R** | **C** (Branchen-Content) | **C** (Kundenbeispiele) | **C** (Technik) | I |
| EPDs | C | **R** | -- | **C** | **A** |
| BIM-Objekte | C | **R** | -- | **C** | **A** |
| Tech-Stack-Entscheidung | **R** | I | I | I | **A** |

R = Responsible, A = Accountable, C = Consulted, I = Informed

### GF-Freigaben

| Was braucht GF-Freigabe? | Wann? | Empfohlenes Format |
|--------------------------|-------|-------------------|
| Analytics-Tool-Wahl (GA4 vs. Matomo) | Woche 1 | Kurz-Memo (1 Seite) |
| Neue Navigationsstruktur | Woche 9 | Praesentation mit ia_new.md |
| Homepage-Redesign | Woche 12 | Wireframe-Review (Staging-Link) |
| Haendlerfinder Go-Live | Woche 16 | Staging-Preview |
| Investitionsentscheidung EPDs | Woche 41 | Business Case (ROI-Rechnung) |
| Tech-Stack-Wechsel Ja/Nein | Woche 48 | Evaluierungsbericht |

---

## Meilensteine & KPIs

### Meilenstein-Uebersicht

| # | Meilenstein | Zieldatum | Review |
|---|-----------|----------|--------|
| M0 | **Analytics live** -- Baseline-Daten fliessen | Woche 2 | Steffi prueft GA4/Matomo Dashboard |
| M1 | **Quick Wins live** -- CTAs, Videos, Meta-Tags | Woche 8 | Steffi + GF: Vorher/Nachher-Screenshots |
| M2a | **Download-Center + Haendlerfinder live** | Woche 16 | Steffi + Vertrieb: Funktionstest |
| M2b | **Homepage-Relaunch + Neue Navigation** | Woche 20 | Steffi + GF: Staging-Review, dann Go-Live |
| M3a | **Planerbereich + GAEB live** | Woche 28 | Steffi + Produktmgmt: Content-Review |
| M3b | **HTML-Produktdaten + Anwendungsseiten live** | Woche 36 | Steffi + Technik: Daten-Validierung |
| M3c | **Verbrauchsrechner + Produktfinder live** | Woche 40 | Steffi + Technik: Berechnungs-Validierung |
| M4 | **Phase-4-Evaluierungsberichte** (EPD, BIM, PIM, Tech-Stack) | Woche 48 | GF-Praesentation mit Empfehlungen |

### KPIs pro Phase

#### Phase 0+1 Baseline & Quick Wins

| KPI | Messmethode | Zielwert (nach 3 Monaten) |
|-----|-----------|--------------------------|
| **Seitenaufrufe/Monat** | GA4/Matomo | Baseline ermitteln (Schaetzung: 5.000--15.000) |
| **Kontaktanfragen/Monat** | Formular-Tracking | +30% gegenueber Baseline |
| **Bounce Rate Homepage** | GA4/Matomo | Baseline ermitteln, Ziel: < 60% |
| **CTR aus Google Suche** | Search Console | +15% fuer Top-30 Seiten (durch bessere Meta-Tags) |
| **Verweildauer Produktseiten** | GA4/Matomo | +20% (durch Videos) |

#### Phase 2 Strukturelle Verbesserungen

| KPI | Messmethode | Zielwert (nach 3 Monaten) |
|-----|-----------|--------------------------|
| **Download-Center Downloads/Monat** | GA4 Event-Tracking | > 200 Downloads/Monat |
| **Haendlerfinder-Nutzungen/Monat** | GA4 Event-Tracking | > 50 Suchen/Monat |
| **Newsletter-Anmeldungen** | Newsletter-Tool | > 50 Anmeldungen in 3 Monaten |
| **Crawl-Errors (404)** | Google Search Console | < 10 neue 404er nach URL-Umstellung |
| **Indexierte Seiten** | Google Search Console | >= 90% der neuen URLs indexiert |

#### Phase 3 Neue Inhalte & Features

| KPI | Messmethode | Zielwert (nach 6 Monaten) |
|-----|-----------|--------------------------|
| **GAEB-Downloads/Monat** | GA4 Event-Tracking | > 50 Downloads/Monat |
| **Verbrauchsrechner-Nutzungen** | GA4 Event-Tracking | > 100 Berechnungen/Monat |
| **Planerbereich-Traffic** | GA4 | > 500 Seitenaufrufe/Monat |
| **Organischer Traffic (gesamt)** | GA4/Matomo | +40% gegenueber Phase-0-Baseline |
| **Kontaktanfragen (gesamt)** | Formular-Tracking | +100% gegenueber Phase-0-Baseline |
| **Referenz-Seiten mit Produktverknuepfung** | Content-Audit | > 80% aller Referenzen |

#### Phase 4 Langfristige Investitionen

| KPI | Messmethode | Zielwert |
|-----|-----------|---------|
| **EPD-Downloads** | GA4 Event-Tracking | > 30/Monat pro EPD |
| **BIM-Object-Downloads** | BIMobject-Analytics + GA4 | > 20/Monat |
| **Haendlerportal-Logins** | WP-Login-Tracking | > 50% der gelisteten Haendler aktiv |
| **Website-Performance** | Lighthouse Score | > 80 (Mobile), > 90 (Desktop) |

### Review-Rhythmus

| Frequenz | Was | Wer |
|----------|-----|-----|
| **Woechentlich** | Analytics-Check (Traffic, Downloads, Anfragen) | Steffi |
| **Alle 2 Wochen** | Sprint-Review (Fortschritt vs. Plan) | Steffi + involvierte KORODUR-Stakeholder |
| **Monatlich** | KPI-Report an GF (1 Seite, Highlights + Blocker) | Steffi → GF |
| **Pro Phasen-Ende** | Meilenstein-Review (Demo + KPI-Praesentation) | Steffi + GF + relevante Abteilungen |
| **Quartalsweise** | Strategie-Review (Roadmap anpassen, Prioritaeten) | GF + Steffi |

---

## Anhang: Zusammenfassung der Sofort-Aktionen

**Was muss DIESE WOCHE passieren:**

1. **GA4 oder Matomo installieren** -- ohne Daten kein messbarer Relaunch
2. **H1 auf Homepage setzen** -- 30 Sekunden Arbeit, gravierender SEO-Fix
3. **Schema.org "Maison"-Bug fixen** -- Yoast/WPML Breadcrumb-Spracheinstellung pruefen
4. **`/dattenblaetter/`-Redirect einrichten** -- Tippfehler mit 301 auf korrekte URL leiten
5. **EN-Homepage Title aendern** -- "Homepage -- korodur" ist inakzeptabel

**Geschaetzter Aufwand fuer alle 5 Punkte: ca. 4 Stunden.**

---

*Erstellt am 2026-03-24 als Teil des KORODUR Website Relaunch Projekts, Phase 3 -- Konzept.*
*Quellen: technical_audit.md (Phase 1), ia_new.md (Phase 3), zielgruppen.md (Phase 3), feature_matrix.md (Phase 2).*
