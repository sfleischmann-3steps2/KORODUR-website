# Inhaltsaudit – korodur.de
**Version:** 1.0 | **Datum:** 2026-03-24 | **Phase:** 1 – Analyse
**Quelle:** Sitemap-Crawl + HTML-Analyse von Produktseiten, Service-Seiten, Homepage

---

## 1. Produktseiten – Inventar

### 1.1 Produktseiten-Anatomie (Standardaufbau)

Analysierte Beispiele: NEODUR HE 3, Cement All, KORODUR Diamond Concrete, MICROTOP TW 3, KORODUR HB 5

**Standardstruktur einer Produktseite:**
```
┌─ Breadcrumb (Home > Products > Category > Product)
├─ Produktbild (Hauptbild + Galerie, 2-4 Bilder)
├─ Produktname (H1)
├─ Kurzbeschreibung (1-2 Saetze)
├─ SKU
├─ Kategorien (verlinkt)
├─ Tabs:
│   ├─ Description (Langtext, Anwendung, Systemkomponenten)
│   ├─ Downloads (TDS-PDF, Broschuere, Farbkarte, Pflegesysteme)
│   └─ Additional Information (Links zu LV, Pflegehinweise, Anwendungsempf.)
└─ (kein Cross-Selling, kein "Verwandte Produkte"-Block)
```

### 1.2 Stichproben-Bewertung (5 Produkte detailliert)

| Kriterium | NEODUR HE 3 | Cement All | Diamond Concrete | MICROTOP TW 3 | KORODUR HB 5 |
|---|---|---|---|---|---|
| Beschreibungstiefe | 3/5 | 3/5 | 2/5 | 3/5 | 2/5 |
| TDS vorhanden? | Ja (PDF) | Ja (PDF) | Ja (PDF) | Ja (PDF) | Ja (PDF) |
| SDS vorhanden? | Nein (auf Seite) | Nein (auf Seite) | Nein (auf Seite) | Nein (auf Seite) | Nein (auf Seite) |
| Bilder | 4 (Produkt + 3 Referenz) | 1 | 1-2 | 1-2 | 1 |
| SKU | Ja | Ja | Ja | Ja | Ja |
| Anwendungsgebiete | Ja (Text) | Ja (kurz) | Minimal | Ja | Minimal |
| Cross-Selling | Systemkomponenten-Links | Nein | Nein | Nein | Nein |
| LV-Verweis | Ja (Tab) | Nein | Nein | Nein | Nein |
| Normen-Angaben | DIN 18557, DIN EN 13813 | Teilweise | Nein | DWA-A 141 | Nein |
| Technische Daten im Text | Nein (nur PDF) | Nein (nur PDF) | Nein (nur PDF) | Nein (nur PDF) | Nein (nur PDF) |

### 1.3 Produktkatalog nach Kategorie

| Kategorie (DE) | Anzahl Produkte (ca.) | TDS verfuegbar? | Bewertung |
|---|---|---|---|
| Industrieboden gesamt | ~45 | Ja (Download-Tab) | 3/5 |
| - Hartstoffeinstreuung | ~12 | Ja | 3/5 |
| - Hartstoffschicht | ~6 | Ja | 3/5 |
| - Schnellestrich-Systeme | ~4 | Ja | 3/5 |
| - Selbstverlaufende Systeme | ~3 | Ja | 3/5 |
| - Industriebodensanierung | ~5 | Ja | 2/5 |
| - Bauchemische Produkte | ~8 | Ja | 2/5 |
| - Hartstoff fuer Kunstharze | ~3 | Ja | 2/5 |
| Sichtestrich | ~5 | Ja | 3/5 |
| Microtop | ~8 | Ja | 3/5 |
| Rapid Set | ~7 | Ja | 3/5 |
| Schnellbetonsysteme | ~1 | Ja | 2/5 |
| Spezialbaustoffe | ~3 | Ja | 2/5 |
| Katzenstreu | ~3 | Unklar | 2/5 |

---

## 2. Content-Qualitaetsbewertung

| Content-Typ | Vorhanden? | Qualitaet (1-5) | Zielgruppe adressiert? | Kommentar |
|---|---|---|---|---|
| **Produktbeschreibungen** | Ja | 2/5 | Gemischt | Kurz, oft nur 2-3 Saetze. Technische Details nur im PDF-TDS, nicht im HTML. Keine Verarbeitungsanleitungen inline. |
| **Technische Datenblaetter (TDS)** | Ja | 4/5 | Planer/Verarbeiter | Als PDF-Downloads pro Produkt. Umfassend, professionell. Aber: Nicht im HTML indexierbar. |
| **Sicherheitsdatenblaetter (SDS)** | Ja (separat) | 3/5 | Verarbeiter | Eigene Service-Unterseite, nicht pro Produkt verlinkt. Nutzer muss wissen, wo er suchen muss. |
| **Verarbeitungshinweise** | Teilweise | 2/5 | Verarbeiter | "Anwendungsempfehlungen" unter Service. Nicht pro Produkt direkt verlinkt. Keine Videos. |
| **Referenzprojekte** | Ja | 3/5 | Planer/Verarbeiter | ~130 Referenzen, filterbar. Pro Referenz: Bild + Text. Aber: Keine klare Verlinkung zu Produkten. |
| **Ausschreibungstexte / LV** | Ja | 3/5 | Planer | Eigene Service-Unterseite "Leistungsverzeichnisse". Einige Produkte verlinken direkt. Kein GAEB-Format. |
| **Leistungserklaerungen (DoP)** | Ja | 3/5 | Planer | Eigene Service-Unterseite. PDF-Downloads. |
| **Zertifikate & Normen** | Teilweise | 2/5 | Planer | Normen werden in Produktbeschreibungen erwaehnt (DIN 18557, EN 13813), aber keine dedizierte Normen-/Zertifikatsseite. ISO 9001 nicht prominent. |
| **News / Aktuelles** | Minimal | 1/5 | Alle | Nur 3 Beitraege. Letzter: Nov 2024. Quasi tot. |
| **Nachhaltigkeitsinformationen** | Ja | 3/5 | Planer/Alle | Eigene Unterseite unter Unternehmen. "KORODUR goes green" als News. Aber: Keine EPDs, keine DGNB-Infos. |
| **Videocontent** | Minimal | 1/5 | Verarbeiter | "KORODUR auf YouTube" als Seite verlinkt. Kein eingebetteter Content auf der Website selbst. |
| **Haendlersuche** | Nein | 0/5 | Handel | NICHT VORHANDEN. Kein Haendlerfinder, keine Partner-Karte. |
| **Lieferprogramm** | Ja | 3/5 | Handel | Als PDF-Download unter Service. |
| **Reinigungsempfehlung** | Ja (nur DE) | 3/5 | Verarbeiter | Eigene Service-Unterseite. Nur auf Deutsch. |
| **KORODUR Report** | Ja | 2/5 | Alle | Interne Publikation, als eigener Menuepunkt. Unklar wie aktuell. |
| **Sicherheitsunterweisung** | Ja (nur DE) | 2/5 | Verarbeiter | Nur auf Deutsch verfuegbar. |

---

## 3. CTA-Analyse (Call-to-Actions)

### 3.1 CTAs auf der Homepage

| CTA | Vorhanden? | Position | Bewertung |
|---|---|---|---|
| "Kontaktieren Sie uns" | Nein | - | Fehlt komplett |
| "Jetzt beraten lassen" | Nein | - | Fehlt komplett |
| "Produkte entdecken" | Nein | - | Fehlt komplett |
| "Katalog anfordern" | Nein | - | Fehlt komplett |
| Slider-CTAs | Nein (1 Slide linkt zu Presse) | Hero | 1/5 |
| Suchfeld | Ja | Header | OK |
| Bereiche-Kacheln | Ja (klickbar) | Mitte | 2/5 (kein expliziter CTA-Text) |

**Bewertung Homepage-CTAs: 1/5** – Die Homepage hat KEINE aktiven Call-to-Actions. Der Hero-Slider hat bei 8 Slides nur 1 Link (zu Presse). Es gibt keinen Button "Kontakt", "Beratung", "Download".

### 3.2 CTAs auf Produktseiten

| CTA | Vorhanden? | Position | Bewertung |
|---|---|---|---|
| "TDS herunterladen" | Ja (im Tab) | Downloads-Tab | 3/5 (versteckt im Tab) |
| "Jetzt anfragen" | Nein | - | Fehlt komplett |
| "Beratung anfordern" | Nein | - | Fehlt komplett |
| "Muster bestellen" | Nein | - | Fehlt komplett |
| "Haendler finden" | Nein | - | Fehlt komplett |
| "In den Warenkorb" | Nein (WooCommerce deaktiviert) | - | - |
| Verwandte Produkte | Nein | - | Fehlt |
| Referenzen zu Produkt | Nein | - | Fehlt |

**Bewertung Produkt-CTAs: 1/5** – Produktseiten sind reine Informationsseiten ohne Conversion-Elemente. Kein einziger aktiver CTA.

### 3.3 Kontaktmittel

| Kontaktweg | Vorhanden? | Auffindbarkeit | Bewertung |
|---|---|---|---|
| Kontaktformular | Ja | Unter Kontakt | 3/5 |
| Telefonnummer | Ja | Nur im Footer | 2/5 (nicht prominent) |
| E-Mail | Ja | Nur im Footer (verschluesselt) | 2/5 |
| Ansprechpartner DE | Ja | Kontakt-Unterseite | 3/5 |
| Ansprechpartner INT | Ja | Kontakt-Unterseite | 3/5 |
| Live-Chat | Nein | - | 0/5 |
| WhatsApp | Nein | - | 0/5 |
| Produktfinder / Konfigurator | Nein | - | 0/5 |
| Mengenrechner | Nein | - | 0/5 |

**Bewertung Kontaktmittel: 2/5** – Basale Kontaktmoeglichkeiten vorhanden, aber nirgends prominent platziert. Telefonnummer nur im Footer, nicht auf Produktseiten oder Header.

---

## 4. Content-Gaps fuer Zielgruppen

### 4.1 Planer & Architekten – Was fehlt?

| Content-Element | Status | Prioritaet | Kommentar |
|---|---|---|---|
| Ausschreibungstexte (GAEB-Format) | Nur als HTML/PDF, kein GAEB | HOCH | LV-Texte vorhanden, aber nicht im Branchenstandard-Format (GAEB, STLB-Bau) |
| BIM-Objekte / CAD-Downloads | NICHT VORHANDEN | HOCH | Kein einziges BIM-Objekt, kein Revit/IFC/dwg |
| EPDs (Environmental Product Declarations) | NICHT VORHANDEN | HOCH | Fuer DGNB/LEED-Zertifizierung essenziell |
| DGNB/LEED-relevante Infos | NICHT VORHANDEN | HOCH | Weder Credits-Zuordnung noch Punkte-Berechnungen |
| Normennachweise gebundelt | Teilweise (in TDS) | MITTEL | DIN 18557, EN 13813 erwaehnt, aber keine zentrale Normen-Seite |
| Muster-Leistungsverzeichnisse | Teilweise | MITTEL | Service-Unterseite vorhanden, aber nicht pro Produkt |
| Planerhotline / Technische Beratung | NICHT VORHANDEN | HOCH | Kein dedizierter Ansprechpartner fuer Planer sichtbar |
| Objektberatung | NICHT VORHANDEN | HOCH | Kein Hinweis auf Planungsunterstuetzung |
| Referenzfilter nach Anwendung | Teilweise | MITTEL | Filter nach Bereich, aber nicht nach Anwendungstyp (z.B. "Logistik", "Automotive") |
| Technische Daten im HTML | NICHT VORHANDEN | MITTEL | Alle techn. Daten nur als PDF, nicht SEO-indexierbar |
| Vergleichstabellen | NICHT VORHANDEN | MITTEL | Kein Produkt-Vergleich moeglich (z.B. HE 3 vs HE 65) |

**Gesamt-Bewertung Planer-Content: 2/5**

### 4.2 Bauunternehmen & Verarbeiter – Was fehlt?

| Content-Element | Status | Prioritaet | Kommentar |
|---|---|---|---|
| Verarbeitungsvideos | NICHT VORHANDEN | HOCH | Weder auf Website eingebettet noch verlinkt. YouTube-Kanal existiert, aber Inhalte nicht integriert. |
| Schritt-fuer-Schritt Anleitungen | NICHT VORHANDEN | HOCH | Anwendungsempfehlungen nur als PDF unter Service |
| FAQ zu Produkten | Nur fuer Rapid Set | MITTEL | "Haeufige Fragen" existiert nur fuer Rapid Set, nicht fuer Industrieboden/Microtop |
| Mengenrechner / Produktrechner | NICHT VORHANDEN | HOCH | Kein Verbrauchsrechner, kein Mischungsverhaeltnis-Tool |
| Technischer Support prominent | NICHT VORHANDEN | HOCH | Keine Hotline, keine technische Notfall-Nummer sichtbar |
| Schulungsangebote | NICHT VORHANDEN | MITTEL | Keine Seminare, keine Webinare, keine Zertifizierungen |
| Verarbeiterbewertungen | NICHT VORHANDEN | NIEDRIG | Keine Testimonials oder Bewertungen |
| Fehlervermeidung / Troubleshooting | NICHT VORHANDEN | MITTEL | Keine "Haeufige Fehler"-Guides |
| Mobile Verarbeiter-App | NICHT VORHANDEN | NIEDRIG | Kein QR-Code-auf-Sack-System |
| Reinigungsempfehlung (EN/FR) | Nur DE | MITTEL | Reinigungsempfehlung existiert nur auf Deutsch |
| Sicherheitsunterweisung (EN/FR) | Nur DE | MITTEL | Nur auf Deutsch verfuegbar |

**Gesamt-Bewertung Verarbeiter-Content: 1.5/5**

### 4.3 Handel & Distributoren – Was fehlt?

| Content-Element | Status | Prioritaet | Kommentar |
|---|---|---|---|
| Haendlerportal / Login | NICHT VORHANDEN | HOCH | Kein geschuetzter Bereich, kein Partnerportal |
| Haendlerfinder / "Wo kaufen?" | NICHT VORHANDEN | HOCH | Keine Karte, keine PLZ-Suche |
| Produktkatalog (PDF gesamt) | Teilweise (Lieferprogramm) | MITTEL | Lieferprogramm als PDF, aber kein vollstaendiger Katalog |
| Preislisten (geschuetzt) | NICHT VORHANDEN | HOCH | Keine Preisinfos sichtbar |
| Newsletter-Anmeldung | NICHT VORHANDEN | MITTEL | Kein Newsletter, kein Opt-in |
| Neuheitenmeldungen | NICHT VORHANDEN | MITTEL | News-Bereich praktisch tot |
| Bestell-/Anfragemoeglichkeit | NICHT VORHANDEN | HOCH | WooCommerce deaktiviert, kein Bestellformular |
| Marketing-Materialien fuer Haendler | NICHT VORHANDEN | MITTEL | Keine Logos, Bilder, Texte zum Download fuer Weiterverkauf |
| Konditionsanfrage | NICHT VORHANDEN | HOCH | Kein Formular fuer Haendler-Konditionen |

**Gesamt-Bewertung Handel-Content: 0.5/5**

---

## 5. SEO-relevante Content-Beobachtungen

| Aspekt | Befund | Bewertung |
|---|---|---|
| Meta-Title Homepage (DE) | "Bodenbelaege fuer Industrie und Gewerbe - Korodur" | 3/5 (ok, aber generisch) |
| Meta-Title Homepage (EN) | "Homepage – korodur" | 1/5 (voellig nichtssagend!) |
| Meta-Description | Vorhanden und gut | 4/5 |
| H1-Struktur Produktseiten | Produktname als H1 | 3/5 |
| Schema.org | Organization + WebSite + BreadcrumbList | 3/5 |
| Product Schema | Nicht sichtbar (WooCommerce sollte es liefern) | 2/5 |
| Technische Daten als HTML | Nicht vorhanden (nur PDF) | 1/5 |
| Bilder-Alt-Tags | Vorhanden (z.B. "NEODUR HE 3") | 3/5 |
| Interne Verlinkung | Schwach (wenig Cross-Links zwischen Produkten) | 2/5 |
| Blog/Content-Marketing | Praktisch nicht vorhanden | 1/5 |

---

## 6. Bereichs-Content ("Bereiche"-Seiten)

Die "Bereiche"-Seiten bilden das eigentliche Content-Rueckgrat der Website. Sie sind informativ, erklaerend und gut strukturiert – im Gegensatz zu den eher kargen Produktseiten.

### Inhaltliche Tiefe pro Bereich

| Bereich | Unterseiten | Inhaltliche Tiefe | Bewertung |
|---|---|---|---|
| Industrieboden | 9 Unterseiten | Gut – inkl. "Was sind KORODUR Industrieboeden?" | 3.5/5 |
| Sichtestrich | 3 Unterseiten | OK – Geglaettet, Geschliffen, Truazzo | 3/5 |
| Microtop | 2 Unterseiten | OK – Nass-/Trockenspritzverfahren | 3/5 |
| Rapid Set | 10 Unterseiten | Sehr gut – inkl. FAQ, Technologie, Einzelprodukte | 4/5 |
| Schnellbetonsysteme | 1 Seite | Duenn | 2/5 |
| 3D Concrete Printing | 1 Seite | Duenn | 2/5 |
| Spezialbaustoffe | 3 Unterseiten | OK | 3/5 |
| Katzenstreu | 6 Unterseiten | Gut – inkl. Bentonit-Erklaerung, Marken, PL | 3.5/5 |

---

## 7. Presse-Content

Die Presse-Seite hat eigene Unterkategorien:
```
/unternehmen/presse/
├── 3D Concrete Printing
├── Industrieboden
├── Katzenstreu
├── KORODUR ueber uns
├── Microtop
├── Nachhaltigkeit
├── Rapid Set
└── Sichtestrich
```

**Bewertung: 2/5** – Struktur ist da, aber unklar ob Inhalte aktuell sind. Keine Pressemitteilungen in den Sitemaps sichtbar (als Posts).

---

## 8. Zusammenfassung – Content-Staerken & -Schwaechen

### Staerken
1. **TDS/Datenblaetter** als PDF-Downloads konsistent vorhanden (4/5)
2. **Bereiche-Seiten** bieten gute Erklaerungen zu Produktgruppen (3.5/5)
3. **Referenzprojekte** umfangreich mit ~130 Projekten weltweit (3/5)
4. **Dreisprachigkeit** weitgehend konsistent (3/5)
5. **Service-Bereich** mit LV, DoP, SDS, Anwendungsempfehlungen (3/5)

### Schwaechen (priorisiert)
1. **KEINE CTAs** – weder Homepage noch Produktseiten haben Conversion-Elemente (1/5)
2. **Keine Zielgruppen-Inhalte** – Content ist produktzentriert, nicht nutzerzentriert (1/5)
3. **Kein Video-Content** integriert – YouTube vorhanden aber nicht eingebettet (1/5)
4. **Keine BIM/EPD/DGNB-Inhalte** – fuer Planer essenziell (0/5)
5. **Kein Haendlerbereich** – nulltes Angebot fuer Distributoren (0/5)
6. **News tot** – 3 Beitraege, letzter Nov 2024 (1/5)
7. **Kein Newsletter, kein Konfigurator, kein Rechner** (0/5)
8. **Technische Daten nur als PDF** – nicht SEO-indexierbar (1/5)
9. **Produktseiten duenn** – kurze Beschreibungen, kaum Cross-Selling (2/5)
10. **Meta-Title EN Homepage** nichtssagend: "Homepage – korodur" (1/5)

### Content-Gesamtbewertung nach Zielgruppe

| Zielgruppe | Bewertung | Kernproblem |
|---|---|---|
| Planer & Architekten | **2/5** | Keine BIM, keine EPD, kein GAEB, kein Planerbereich |
| Bauunternehmen & Verarbeiter | **2/5** | Keine Videos, keine Anleitungen, kein Rechner, kein Support |
| Handel & Distributoren | **0.5/5** | Komplett unbesetzt – kein Portal, kein Finder, keine Konditionen |

---

## 9. Empfehlungen (Top 10, priorisiert)

1. **CTA-Strategie entwickeln** – Jede Seite braucht mindestens 1 klaren CTA (Kontakt, Download, Beratung)
2. **Zielgruppen-Einstiegspunkte** auf Homepage – "Fuer Planer", "Fuer Verarbeiter", "Fuer Handel"
3. **BIM-Objekte & EPDs** erstellen/bereitstellen – Marktzugang fuer Planer
4. **Video-Content** von YouTube einbetten – Verarbeiter brauchen Anleitungen
5. **Technische Daten ins HTML** ueberfuehren – SEO und Usability
6. **Haendlerfinder** implementieren – Karte + PLZ-Suche
7. **Produktseiten anreichern** – Vergleichstabellen, verwandte Produkte, Referenz-Links
8. **News-Strategie** – Mindestens monatlich Content (Projekte, Produkte, Events)
9. **Meta-Titles optimieren** – EN Homepage, Produktseiten
10. **WooCommerce evaluieren** – Entweder E-Commerce aktivieren oder auf Custom Post Types migrieren
