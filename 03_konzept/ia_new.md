# Informationsarchitektur NEU -- korodur.de
**Version:** 1.0 | **Datum:** 2026-03-24 | **Phase:** 3 -- Konzept
**Erstellt von:** Claude Code (Konzept-Agent)
**Basis:** structure_audit.md, technical_audit.md, content_audit.md, competitors.md, zielgruppenplattformen.md, feature_matrix.md

---

## Executive Summary

Die neue Informationsarchitektur fuer korodur.de loest die zentralen Probleme der bestehenden Seite:

1. **Doppelstruktur aufgeloest:** "Bereiche" und "Produkte" werden zu einer einzigen Produkt-Hierarchie zusammengefuehrt
2. **Zielgruppen-Einstiege eingefuehrt:** Planer, Verarbeiter und Haendler erhalten dedizierte Zugaenge
3. **Duale Produkt-Navigation:** Produkte sind sowohl nach Produktgruppe als auch nach Anwendung/Branche erreichbar
4. **Planerbereich neu:** Ausschreibungstexte, GAEB, Downloads, Normen an einem Ort
5. **Download-Center zentralisiert:** TDS, SDS, DoP, LV filterbar an einem Ort
6. **Haendlerfinder integriert:** Karte + PLZ-Suche
7. **URL-Struktur bereinigt:** Keine Doppelungen, konsistente Slugs, SEO-freundlich
8. **858 URLs auf ca. 320 konsolidiert** (plus Sprachvarianten)

**Leitprinzipien:**
- Maximal 3 Klicks zum Ziel fuer jede Zielgruppe
- WordPress-kompatibel (vorerst)
- Realistisch fuer einen Mittelstaendler
- Schrittweise umsetzbar

---

## 1. Neue Hauptnavigation (Top-Level)

### 1.1 Navigationsstruktur

```
[Logo KORODUR]    Produkte | Anwendungen | Fuer Planer | Service & Downloads | Unternehmen | Kontakt    [Suche] [DE|EN|FR]
```

**6 Hauptpunkte** (plus Utility: Suche, Sprachwechsel)

| # | Menuepunkt | Ziel | Primaere Zielgruppe | Sekundaere Zielgruppe |
|---|-----------|------|---------------------|----------------------|
| 1 | **Produkte** | Produktkatalog nach Produktgruppe | Alle | -- |
| 2 | **Anwendungen** | Produkte nach Anwendungsfeld/Branche | Verarbeiter, Planer | Handel |
| 3 | **Fuer Planer** | Dedizierter Planerbereich | Planer & Architekten | -- |
| 4 | **Service & Downloads** | Download-Center, Rechner, Haendlerfinder | Alle | -- |
| 5 | **Unternehmen** | Firmeninfos, Referenzen, Nachhaltigkeit, News | Alle | -- |
| 6 | **Kontakt** | Kontaktformular, Ansprechpartner, Standorte | Alle | -- |

### 1.2 Mega-Menue-Struktur

#### Produkte (Mega-Menue)
```
┌─────────────────────────────────────────────────────────────────────────┐
│  PRODUKTGRUPPEN              HIGHLIGHTS           SCHNELLEINSTIEG       │
│                                                                         │
│  Industrieboden              [Bild] NEODUR HE 3   → Alle Produkte      │
│  Sichtestrich                Green – unser         → Produktvergleich   │
│  Microtop                    nachhaltiger          → Neuheiten          │
│  Rapid Set                   Hartstoff                                  │
│  Schnellbetonsysteme                                                    │
│  Spezialbaustoffe            [Bild] Diamond        → Download TDS      │
│  3D Concrete Printing        Concrete – der        → Produktfinder     │
│  Katzenstreu (GoodCat)       Sichtestrich                              │
│                              der Zukunft                                │
└─────────────────────────────────────────────────────────────────────────┘
```

#### Anwendungen (Mega-Menue)
```
┌─────────────────────────────────────────────────────────────────────────┐
│  NACH BRANCHE                NACH ANFORDERUNG      SCHNELLEINSTIEG      │
│                                                                         │
│  Logistik & Distribution     Neubau                → Produktfinder      │
│  Automotive & Produktion     Sanierung              → Referenzprojekte  │
│  Lebensmittel & Pharma       Hochbelastbare Boeden  → Beratung anfragen │
│  Handel & Retail             Schnelle Nutzung                           │
│  Oeffentliche Gebaeude       Dekorative Boeden                          │
│  Trinkwasser                 Trinkwasserschutz                          │
│  Wohnen & Hospitality                                                   │
└─────────────────────────────────────────────────────────────────────────┘
```

#### Fuer Planer (Mega-Menue)
```
┌─────────────────────────────────────────────────────────────────────────┐
│  PLANUNGSHILFEN              DOKUMENTE              SERVICE              │
│                                                                         │
│  Ausschreibungstexte (LV)    Technische Datenblaetter  Objektberatung   │
│  GAEB-Downloads              Leistungserklaerungen     Planerhotline    │
│  Normen & Zulassungen        Sicherheitsdatenblaetter  Bemusterung      │
│  Systemaufbauten             EPDs (in Vorbereitung)                     │
│  Produktvergleiche                                                      │
│  Referenzprojekte            → Zum Download-Center                      │
└─────────────────────────────────────────────────────────────────────────┘
```

#### Service & Downloads (Mega-Menue)
```
┌─────────────────────────────────────────────────────────────────────────┐
│  DOWNLOADS                   TOOLS                  HAENDLER            │
│                                                                         │
│  Download-Center             Verbrauchsrechner      Haendlerfinder     │
│  (TDS, SDS, DoP, LV)        Produktfinder           Lieferprogramm     │
│  Lieferprogramm (PDF)        FAQ                    Anfrage stellen    │
│  Anwendungsempfehlungen                                                 │
│  Reinigungsempfehlungen      VERARBEITER                                │
│  Verarbeitungsvideos         Verarbeitungshinweise                      │
│                              Schulungen & Seminare                      │
│                              Sicherheitsunterweisung                    │
└─────────────────────────────────────────────────────────────────────────┘
```

#### Unternehmen (Mega-Menue)
```
┌─────────────────────────────────────────────────────────────────────────┐
│  UEBER UNS                   REFERENZEN             AKTUELLES           │
│                                                                         │
│  Geschichte (seit 1936)      Referenzprojekte       News & Presse       │
│  Standorte & Produktion      nach Branche           KORODUR Report      │
│  Nachhaltigkeit              nach Produkt           Veranstaltungen     │
│  Qualitaet & Zertifikate     nach Region                                │
│  Jobs & Karriere                                                        │
└─────────────────────────────────────────────────────────────────────────┘
```

#### Kontakt (kein Mega-Menue, direkte Links)
```
Kontaktformular | Ansprechpartner Deutschland | Ansprechpartner International | Standorte
```

---

## 2. Vollstaendige Sitemap (Baumstruktur)

```
korodur.de/
│
├── / .................................................. Homepage
│
├── /produkte/ ........................................ Produktuebersicht
│   ├── /produkte/industrieboden/ ..................... Produktgruppe: Industrieboden
│   │   ├── /produkte/industrieboden/hartstoffeinstreuung/ ... Unterkategorie
│   │   ├── /produkte/industrieboden/hartstoffschicht/ ....... Unterkategorie
│   │   ├── /produkte/industrieboden/schnellestrich/ ......... Unterkategorie
│   │   ├── /produkte/industrieboden/selbstverlaufend/ ....... Unterkategorie
│   │   ├── /produkte/industrieboden/sanierung/ .............. Unterkategorie
│   │   ├── /produkte/industrieboden/hartstoff-kunstharze/ ... Unterkategorie
│   │   └── /produkte/industrieboden/bauchemie/ .............. Unterkategorie
│   ├── /produkte/sichtestrich/ ....................... Produktgruppe: Sichtestrich
│   │   ├── /produkte/sichtestrich/geglaettet/ ............... Unterkategorie
│   │   ├── /produkte/sichtestrich/geschliffen/ .............. Unterkategorie
│   │   └── /produkte/sichtestrich/truazzo/ .................. Unterkategorie
│   ├── /produkte/microtop/ ........................... Produktgruppe: Microtop
│   ├── /produkte/rapid-set/ .......................... Produktgruppe: Rapid Set
│   ├── /produkte/schnellbetonsysteme/ ................ Produktgruppe: Schnellbetonsysteme
│   ├── /produkte/spezialbaustoffe/ ................... Produktgruppe: Spezialbaustoffe
│   │   ├── /produkte/spezialbaustoffe/betoninstandsetzung/ .. Unterkategorie
│   │   ├── /produkte/spezialbaustoffe/injektionssystem/ ..... Unterkategorie
│   │   └── /produkte/spezialbaustoffe/vergusssystem/ ........ Unterkategorie
│   ├── /produkte/3d-concrete-printing/ ............... Produktgruppe: 3D Concrete Printing
│   ├── /produkte/katzenstreu/ ........................ Produktgruppe: Katzenstreu (GoodCat)
│   ├── /produkte/vergleich/ .......................... Produktvergleich-Tool
│   └── /produkte/neuheiten/ .......................... Neuheiten
│
│   Einzelprodukte (Ebene 3, Beispiele):
│   ├── /produkte/industrieboden/neodur-he-3/ ......... Produktdetail
│   ├── /produkte/industrieboden/neodur-he-65/ ........ Produktdetail
│   ├── /produkte/sichtestrich/granidur/ .............. Produktdetail
│   ├── /produkte/microtop/microtop-tw-3/ ............. Produktdetail
│   ├── /produkte/rapid-set/cement-all/ ............... Produktdetail
│   └── /produkte/katzenstreu/goodcat-silver-classic/ . Produktdetail
│
├── /anwendungen/ ..................................... Anwendungsuebersicht
│   ├── /anwendungen/logistik/ ........................ Branche: Logistik & Distribution
│   ├── /anwendungen/automotive/ ...................... Branche: Automotive & Produktion
│   ├── /anwendungen/lebensmittel-pharma/ ............. Branche: Lebensmittel & Pharma
│   ├── /anwendungen/handel-retail/ ................... Branche: Handel & Retail
│   ├── /anwendungen/oeffentliche-gebaeude/ ........... Branche: Oeffentliche Gebaeude
│   ├── /anwendungen/trinkwasser/ ..................... Branche: Trinkwasserschutz
│   ├── /anwendungen/wohnen-hospitality/ .............. Branche: Wohnen & Hospitality
│   ├── /anwendungen/neubau/ .......................... Anforderung: Neubau
│   ├── /anwendungen/sanierung/ ....................... Anforderung: Sanierung
│   └── /anwendungen/produktfinder/ ................... Interaktiver Produktfinder
│
├── /planer/ .......................................... Planerbereich (Landing Page)
│   ├── /planer/ausschreibungstexte/ .................. Ausschreibungstexte (LV + GAEB)
│   ├── /planer/normen-zulassungen/ ................... Normen & Zulassungen
│   ├── /planer/systemaufbauten/ ...................... Systemaufbauten (Schichtaufbau-Diagramme)
│   ├── /planer/produktvergleiche/ .................... Produktvergleichstabellen
│   ├── /planer/objektberatung/ ....................... Objektberatung & Planerhotline
│   └── /planer/nachhaltigkeit/ ....................... EPDs, DGNB-Relevanz, Green Building
│
├── /service/ ......................................... Service-Uebersicht
│   ├── /service/downloads/ ........................... Download-Center (zentral, filterbar)
│   ├── /service/verbrauchsrechner/ ................... Verbrauchsrechner
│   ├── /service/produktfinder/ ....................... Redirect → /anwendungen/produktfinder/
│   ├── /service/haendlerfinder/ ...................... Haendlerfinder (Karte + PLZ)
│   ├── /service/verarbeitungshinweise/ ............... Verarbeitungshinweise & Videos
│   ├── /service/anwendungsempfehlungen/ .............. Anwendungsempfehlungen
│   ├── /service/reinigungsempfehlung/ ................ Reinigungsempfehlung
│   ├── /service/sicherheitsunterweisung/ ............. Sicherheitsunterweisung
│   ├── /service/schulungen/ .......................... Schulungen & Seminare
│   ├── /service/faq/ ................................. FAQ (alle Produktgruppen)
│   └── /service/lieferprogramm/ ...................... Lieferprogramm (PDF)
│
├── /unternehmen/ ..................................... Unternehmensuebersicht
│   ├── /unternehmen/geschichte/ ...................... Geschichte (seit 1936)
│   ├── /unternehmen/standorte/ ....................... Standorte & Produktion
│   ├── /unternehmen/nachhaltigkeit/ .................. Nachhaltigkeit
│   ├── /unternehmen/qualitaet/ ....................... Qualitaet & Zertifikate (ISO 9001 etc.)
│   ├── /unternehmen/karriere/ ........................ Jobs & Karriere
│   ├── /unternehmen/news/ ............................ News & Presse
│   │   └── /unternehmen/news/[slug]/ ................. Einzelner News-Beitrag
│   └── /unternehmen/korodur-report/ .................. KORODUR Report
│
├── /referenzen/ ...................................... Referenzprojekte (Uebersicht, filterbar)
│   └── /referenzen/[projekt-slug]/ ................... Einzelnes Referenzprojekt
│
├── /kontakt/ ......................................... Kontakt (Formular + Uebersicht)
│   ├── /kontakt/deutschland/ ......................... Ansprechpartner Deutschland
│   └── /kontakt/international/ ....................... Ansprechpartner International
│
├── /impressum/ ....................................... Impressum
├── /datenschutz/ ..................................... Datenschutzerklaerung
├── /agb/ ............................................. AGB
└── /hinweisgebersystem/ .............................. Hinweisgebersystem
```

### 2.1 Seitenanzahl-Schaetzung

| Bereich | Anzahl Seiten (DE) | Bemerkung |
|---------|-------------------|-----------|
| Homepage | 1 | -- |
| Produkte (Gruppen + Kategorien) | ~25 | 8 Gruppen + Unterkategorien |
| Produkte (Einzelseiten) | ~71 | Bestehender Katalog |
| Anwendungen | ~12 | 7 Branchen + 2 Anforderungen + Produktfinder + Uebersicht |
| Planer | ~7 | Neuer Bereich |
| Service | ~12 | Inkl. Download-Center, Haendlerfinder, Rechner |
| Unternehmen | ~8 | Inkl. News-Uebersicht |
| Referenzen | ~131 | Bestehend |
| Kontakt | ~3 | -- |
| Rechtliches | ~4 | -- |
| News-Beitraege | ~10+ | Wachsend |
| **Gesamt (DE)** | **~284** | Statt 858 URLs (inkl. Duplikate) |

Mit EN + FR: **~284 x 3 = ~852 URLs** (aber ohne Duplikate und WooCommerce-Overhead)

---

## 3. Zielgruppen-Einstiege & Klickpfade

### 3.1 Homepage-Struktur (Wireframe)

```
┌─────────────────────────────────────────────────────────────────────┐
│ [Hauptnavigation]                                                    │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  HERO: "Qualitaet fuer Generationen – seit 1936"                    │
│  [CTA: Produkte entdecken]  [CTA: Beratung anfragen]               │
│                                                                      │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐              │
│  │  FUR PLANER  │  │FUR VERARBEIT.│  │  FUR HANDEL  │              │
│  │  & ARCHIT.   │  │              │  │              │              │
│  │              │  │              │  │              │              │
│  │ Ausschreibung│  │ Verarbeitungs│  │ Haendler-    │              │
│  │ Downloads    │  │ hinweise     │  │ finder       │              │
│  │ Normen       │  │ Rechner      │  │ Lieferprogr. │              │
│  │              │  │ Videos       │  │ Anfrage      │              │
│  │ [Mehr →]     │  │ [Mehr →]     │  │ [Mehr →]     │              │
│  └──────────────┘  └──────────────┘  └──────────────┘              │
│                                                                      │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  PRODUKTBEREICHE (8 Kacheln mit Bild)                               │
│  Industrieboden | Sichtestrich | Microtop | Rapid Set | ...         │
│                                                                      │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  USP-SEKTION: "750 Mio. m2 verlegt | 90 Jahre Erfahrung | ISO 9001"│
│                                                                      │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  REFERENZ-HIGHLIGHTS (3-4 Projekte mit Bild)                        │
│  [Alle Referenzen →]                                                │
│                                                                      │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  NEWS-TEASER (2-3 aktuelle Beitraege)                               │
│  [Alle News →]                                                      │
│                                                                      │
├─────────────────────────────────────────────────────────────────────┤
│ [Footer: Kontakt | Links | Social | Rechtliches]                    │
└─────────────────────────────────────────────────────────────────────┘
```

### 3.2 Klickpfade pro Zielgruppe

#### Planer & Architekten

| Ziel | Pfad | Klicks |
|------|------|--------|
| Ausschreibungstext fuer Produkt X | Homepage → Fuer Planer → Ausschreibungstexte → Produkt waehlen | 3 |
| Ausschreibungstext (alternativ) | Homepage → Produkt → Produktdetail → Tab "Ausschreibung" | 3 |
| TDS herunterladen | Homepage → Service & Downloads → Download-Center → Filter | 3 |
| TDS herunterladen (alternativ) | Homepage → Produkt → Produktdetail → Download-Button | 3 |
| Normen-Info | Homepage → Fuer Planer → Normen & Zulassungen | 2 |
| Objektberatung anfragen | Homepage → Fuer Planer → Objektberatung | 2 |
| Referenzprojekt finden | Homepage → Referenz-Highlight klicken | 1 |
| Referenzprojekt nach Branche | Homepage → Unternehmen (Mega) → Referenzen nach Branche | 2 |
| Systemaufbau ansehen | Homepage → Fuer Planer → Systemaufbauten | 2 |
| Produktvergleich | Homepage → Fuer Planer → Produktvergleiche | 2 |

**Ergebnis: Alle Planer-Ziele in maximal 3 Klicks erreichbar.**

#### Bauunternehmen & Verarbeiter

| Ziel | Pfad | Klicks |
|------|------|--------|
| Produkt nach Anwendung finden | Homepage → Anwendungen → Branche → Produkt | 3 |
| Verarbeitungshinweis lesen | Homepage → Service → Verarbeitungshinweise → Produkt | 3 |
| Verarbeitungshinweis (alternativ) | Homepage → Produkt → Produktdetail → Tab "Verarbeitung" | 3 |
| Verarbeitungsvideo ansehen | Homepage → Service → Verarbeitungshinweise → Video | 3 |
| Verbrauchsrechner nutzen | Homepage → Service → Verbrauchsrechner | 2 |
| TDS auf der Baustelle oeffnen | Homepage → Produkt → Produktdetail → Download | 3 |
| FAQ lesen | Homepage → Service → FAQ | 2 |
| Technischen Support kontaktieren | Homepage → Kontakt (Header) | 1 |

**Ergebnis: Alle Verarbeiter-Ziele in maximal 3 Klicks erreichbar.**

#### Handel & Distributoren

| Ziel | Pfad | Klicks |
|------|------|--------|
| Haendlerfinder oeffnen | Homepage → "Fuer Handel"-Kachel → Haendlerfinder | 2 |
| Haendlerfinder (alternativ) | Homepage → Service → Haendlerfinder | 2 |
| Lieferprogramm herunterladen | Homepage → Service → Lieferprogramm | 2 |
| Produktuebersicht | Homepage → Produkte | 1 |
| Anfrage stellen | Homepage → Kontakt | 1 |
| Ansprechpartner finden | Homepage → Kontakt → Deutschland/International | 2 |

**Ergebnis: Alle Haendler-Ziele in maximal 2 Klicks erreichbar.**

---

## 4. URL-Schema

### 4.1 Konsistentes Sprachschema

| Sprache | Praefix | Beispiel |
|---------|---------|---------|
| Deutsch (Standard, x-default) | `/` | `korodur.de/produkte/industrieboden/` |
| Englisch | `/en/` | `korodur.de/en/products/industrial-floor/` |
| Franzoesisch | `/fr/` | `korodur.de/fr/produits/sols-industriels/` |

### 4.2 URL-Muster nach Seitentyp

| Seitentyp | DE | EN | FR |
|-----------|----|----|-----|
| Produkte (Uebersicht) | `/produkte/` | `/en/products/` | `/fr/produits/` |
| Produktgruppe | `/produkte/industrieboden/` | `/en/products/industrial-floor/` | `/fr/produits/sols-industriels/` |
| Produktdetail | `/produkte/industrieboden/neodur-he-3/` | `/en/products/industrial-floor/neodur-he-3/` | `/fr/produits/sols-industriels/neodur-he-3/` |
| Anwendungen | `/anwendungen/` | `/en/applications/` | `/fr/applications/` |
| Anwendung (Branche) | `/anwendungen/logistik/` | `/en/applications/logistics/` | `/fr/applications/logistique/` |
| Planer | `/planer/` | `/en/specifiers/` | `/fr/prescripteurs/` |
| Ausschreibungstexte | `/planer/ausschreibungstexte/` | `/en/specifiers/tender-specifications/` | `/fr/prescripteurs/cahier-des-charges/` |
| Service | `/service/` | `/en/service/` | `/fr/service/` |
| Downloads | `/service/downloads/` | `/en/service/downloads/` | `/fr/service/telechargements/` |
| Haendlerfinder | `/service/haendlerfinder/` | `/en/service/dealer-locator/` | `/fr/service/trouver-un-distributeur/` |
| Unternehmen | `/unternehmen/` | `/en/company/` | `/fr/entreprise/` |
| Referenzen | `/referenzen/` | `/en/references/` | `/fr/references/` |
| Referenz (Einzel) | `/referenzen/[slug]/` | `/en/references/[slug]/` | `/fr/references/[slug]/` |
| Kontakt | `/kontakt/` | `/en/contact/` | `/fr/contact/` |
| News | `/unternehmen/news/` | `/en/company/news/` | `/fr/entreprise/actualites/` |
| News (Einzel) | `/unternehmen/news/[slug]/` | `/en/company/news/[slug]/` | `/fr/entreprise/actualites/[slug]/` |

### 4.3 URL-Regeln

1. **Produktnamen bleiben sprachunabhaengig** -- Markennamen (NEODUR, GRANIDUR, MICROTOP, KORODUR) werden nicht uebersetzt (sind identisch in DE/EN/FR)
2. **Alle Slugs lowercase, Bindestrich-getrennt** -- keine Grossbuchstaben, keine Underscores
3. **Keine WooCommerce-Artefakte** -- kein `/shop/`, kein `/produkt/`, kein `/produkt-kategorie/`
4. **Keine Duplikate** -- jeder Inhalt hat genau eine kanonische URL pro Sprache
5. **Trailing Slashes konsistent** -- alle URLs mit abschliessendem `/`
6. **Hreflang im HTML-Head UND in Sitemap** -- nicht nur Sitemap wie bisher

### 4.4 Redirect-Empfehlungen (ALT → NEU)

Insgesamt muessen **858 bestehende URLs** via 301-Redirect umgeleitet werden. Nachfolgend die wichtigsten Muster:

#### Systematische Redirects

| Altes Muster | Neues Muster | Anzahl URLs (ca.) |
|-------------|-------------|-------------------|
| `/bereiche/[bereich]/` | `/produkte/[bereich]/` | ~25 (DE) + ~25 (EN) + ~25 (FR) |
| `/produkt-kategorie/[kategorie]/` | `/produkte/[kategorie]/` | ~45 (alle Sprachen) |
| `/produkt/[produktname]/` | `/produkte/[gruppe]/[produktname]/` | ~200 (alle Sprachen) |
| `/en/produkt/[name]/` | `/en/products/[group]/[name]/` | ~67 |
| `/fr/produkt/[name]/` | `/fr/produits/[group]/[name]/` | ~63 |
| `/en/areas/[area]/` | `/en/applications/[area]/` oder `/en/products/[group]/` | ~25 |
| `/fr/domaines/[domaine]/` | `/fr/applications/[domaine]/` oder `/fr/produits/[group]/` | ~25 |
| `/shop/` | `/produkte/` | 3 (DE/EN/FR) |
| `/en/shop/` | `/en/products/` | 1 |
| `/service/dattenblaetter/` | `/service/downloads/` | 1 (Tippfehler-Korrektur!) |
| `/service/datenblaetter/` | `/service/downloads/` | 1 |
| `/service/leistungsverzeichnisse/` | `/planer/ausschreibungstexte/` | 1 |
| `/service/leistungserklaerungen/` | `/service/downloads/?typ=dop` | 1 |
| `/service/sicherheitsdatenblaetter/` | `/service/downloads/?typ=sds` | 1 |
| `/aktuelles/` | `/unternehmen/news/` | 1 |
| `/unternehmen/presse/` | `/unternehmen/news/` | 1 |
| `/unternehmen/jobs-karriere/` | `/unternehmen/karriere/` | 1 |
| `/bauarbeiten-im-gange/` | `/` (410 Gone oder 301 zu Homepage) | 1 |
| Referenzen (Query-basiert) | `/referenzen/?branche=[slug]` | ~7 |

#### Spezielle Redirects

| Alte URL | Neue URL | Grund |
|----------|----------|-------|
| `/?page_id=1090` | `/unternehmen/korodur-report/` | KORODUR Report hatte page_id-URL |
| `/en/service/datenblaetter/` | `/en/service/downloads/` | Unuebersetzter DE-Slug |
| `/en/service/leistungserklaerungen/` | `/en/service/downloads/?type=dop` | Konsolidierung |
| `/en/service/sicherheitsdatenblaetter/` | `/en/service/downloads/?type=sds` | Konsolidierung |

**Wichtig:** Vollstaendige Redirect-Map als CSV erstellen vor Go-Live (alle 858 URLs einzeln mappen).

---

## 5. Navigation Mapping: ALT → NEU

### 5.1 Was wandert wohin?

#### Bestehende Bereiche-Seiten (Content-Seiten)

| Alte Seite | Neuer Ort | Aktion |
|-----------|-----------|--------|
| `/bereiche/industrieboden/` | `/produkte/industrieboden/` | **Zusammenfuehren** mit Produktkategorie. Content der Bereiche-Seite wird zur Kategorie-Einfuehrung. |
| `/bereiche/industrieboden/hartstoffschicht/` | `/produkte/industrieboden/hartstoffschicht/` | Umbenennung, Content bleibt |
| `/bereiche/industrieboden/hartstoffeinstreuung/` | `/produkte/industrieboden/hartstoffeinstreuung/` | Umbenennung, Content bleibt |
| `/bereiche/sichtestrich/` | `/produkte/sichtestrich/` | Zusammenfuehren |
| `/bereiche/microtop/` | `/produkte/microtop/` | Zusammenfuehren |
| `/bereiche/rapid-set/` | `/produkte/rapid-set/` | Zusammenfuehren |
| `/bereiche/schnellbetonsysteme/` | `/produkte/schnellbetonsysteme/` | Zusammenfuehren |
| `/bereiche/spezialbaustoffe/` | `/produkte/spezialbaustoffe/` | Zusammenfuehren |
| `/bereiche/3d-concrete-printing/` | `/produkte/3d-concrete-printing/` | Zusammenfuehren |
| `/bereiche/katzenstreu/` | `/produkte/katzenstreu/` | Zusammenfuehren |

**Prinzip:** Die erklaerenden Inhalte der "Bereiche"-Seiten werden zum Kopfbereich der neuen Produktgruppen-Seiten. So entsteht eine einzige Hierarchie statt zwei paralleler.

#### Bestehende Produkt-Kategorie-Seiten (WooCommerce)

| Alte Seite | Neuer Ort | Aktion |
|-----------|-----------|--------|
| `/produkt-kategorie/industrieboden/` | `/produkte/industrieboden/` | **Zusammenlegen** mit Bereiche-Content |
| `/produkt-kategorie/sichtestrich/` | `/produkte/sichtestrich/` | Zusammenlegen |
| ... (alle Kategorien analog) | ... | Zusammenlegen |

#### Bestehende Produktdetailseiten

| Alte Seite | Neuer Ort | Aktion |
|-----------|-----------|--------|
| `/produkt/neodur-he-3/` | `/produkte/industrieboden/neodur-he-3/` | **Umstrukturieren** -- Produkt erhaelt Gruppenkontext in der URL |
| `/produkt/cement-all/` | `/produkte/rapid-set/cement-all/` | Umstrukturieren |
| `/produkt/granidur/` | `/produkte/sichtestrich/granidur/` | Umstrukturieren |
| ... (alle ~71 Produkte analog) | ... | Umstrukturieren |

#### Bestehende Service-Seiten

| Alte Seite | Neuer Ort | Aktion |
|-----------|-----------|--------|
| `/service/` | `/service/` | Bleibt (neues Layout) |
| `/service/dattenblaetter/` | `/service/downloads/` | **Zusammenlegen** ins Download-Center |
| `/service/sicherheitsdatenblaetter/` | `/service/downloads/` | Zusammenlegen ins Download-Center |
| `/service/leistungserklaerungen/` | `/service/downloads/` | Zusammenlegen ins Download-Center |
| `/service/leistungsverzeichnisse/` | `/planer/ausschreibungstexte/` | **Verschieben** in Planerbereich |
| `/service/anwendungsempfehlungen/` | `/service/anwendungsempfehlungen/` | Bleibt |
| `/service/reinigungsempfehlung/` | `/service/reinigungsempfehlung/` | Bleibt (EN/FR hinzufuegen!) |
| `/service/lieferprogramm/` | `/service/lieferprogramm/` | Bleibt |
| `/aktuelles/` | `/unternehmen/news/` | Verschieben unter Unternehmen |

#### Bestehende Unternehmensseiten

| Alte Seite | Neuer Ort | Aktion |
|-----------|-----------|--------|
| `/unternehmen/` | `/unternehmen/` | Bleibt (neues Layout) |
| `/unternehmen/geschichte/` | `/unternehmen/geschichte/` | Bleibt |
| `/unternehmen/nachhaltigkeit/` | `/unternehmen/nachhaltigkeit/` | Bleibt (ausbauen!) |
| `/unternehmen/standorte/` | `/unternehmen/standorte/` | Bleibt |
| `/unternehmen/presse/` | `/unternehmen/news/` | **Zusammenlegen** mit Aktuelles |
| `/unternehmen/jobs-karriere/` | `/unternehmen/karriere/` | Slug-Bereinigung |

### 5.2 Was wird NEU erstellt?

| Neue Seite | Beschreibung | Prioritaet |
|-----------|--------------|-----------|
| `/anwendungen/` + 9 Unterseiten | Branchenspezifische Anwendungsseiten (Logistik, Automotive etc.) | Phase 1 |
| `/anwendungen/produktfinder/` | Interaktiver Produktfinder (Entscheidungsbaum) | Phase 2 |
| `/planer/` + 6 Unterseiten | Kompletter Planerbereich | Phase 1 |
| `/planer/ausschreibungstexte/` | Ausschreibungstexte mit GAEB-Download | Phase 1 |
| `/planer/normen-zulassungen/` | Normen-Referenzseite | Phase 1 |
| `/planer/systemaufbauten/` | Schichtaufbau-Diagramme pro System | Phase 2 |
| `/planer/produktvergleiche/` | Vergleichstabellen (z.B. HE 3 vs HE 65) | Phase 2 |
| `/planer/objektberatung/` | Objektberatung mit Kontaktformular | Phase 1 |
| `/planer/nachhaltigkeit/` | EPDs, DGNB-Relevanz (wenn verfuegbar) | Phase 2 |
| `/service/downloads/` | Zentrales Download-Center (filterbar) | Phase 1 |
| `/service/haendlerfinder/` | Haendlerfinder (Karte + PLZ) | Phase 1 |
| `/service/verbrauchsrechner/` | Verbrauchsrechner (kg/m2 x Flaeche) | Phase 2 |
| `/service/schulungen/` | Schulungen & Seminare | Phase 3 |
| `/service/faq/` | FAQ fuer alle Produktgruppen | Phase 2 |
| `/produkte/vergleich/` | Produktvergleich-Tool | Phase 2 |
| `/produkte/neuheiten/` | Neuheiten-Seite | Phase 2 |
| `/unternehmen/qualitaet/` | Qualitaet & Zertifikate (ISO 9001, TUeV) | Phase 1 |
| `/unternehmen/korodur-report/` | KORODUR Report (eigene URL statt page_id) | Phase 1 |

### 5.3 Was wird zusammengelegt?

| Zusammenlegung | Betroffene alte Seiten | Neue Seite |
|---------------|----------------------|-----------|
| Bereiche + Produktkategorien | `/bereiche/[x]/` + `/produkt-kategorie/[x]/` | `/produkte/[x]/` |
| Alle Download-Typen | `/service/dattenblaetter/` + `/service/sicherheitsdatenblaetter/` + `/service/leistungserklaerungen/` | `/service/downloads/` |
| News + Presse | `/aktuelles/` + `/unternehmen/presse/` | `/unternehmen/news/` |
| Shop + Produkte | `/shop/` + `/produkte/` | `/produkte/` |

### 5.4 Was faellt weg?

| Entfernt | Grund |
|---------|-------|
| `/shop/` | WooCommerce-Artefakt, kein E-Commerce aktiv |
| `/produkt-kategorie/` (alle) | Zusammengelegt mit `/produkte/` |
| `/bereiche/` (als separater Punkt) | Zusammengelegt mit `/produkte/` |
| `/bauarbeiten-im-gange/` | Platzhalterseite, nicht mehr noetig |
| Rapid-Set-Unterseiten als separate Bereiche-Seiten | Content wird in Produktgruppe integriert |
| WooCommerce-spezifische URLs (cart, checkout etc.) | Kein E-Commerce |

---

## 6. Vergleich ALT vs NEU

### 6.1 Hauptnavigation

| ALT | NEU | Aenderung |
|-----|-----|-----------|
| Korodur (Dropdown) | Unternehmen | Umbenannt, Referenzen hinzugefuegt |
| Bereiche | -- (entfaellt als eigenstaendiger Punkt) | Content wandert in Produkte |
| Produkte | Produkte | Bleibt, erhaelt Bereiche-Content + Unterkategorien |
| Referenzen | -- (wandert unter Unternehmen) | Bleibt erreichbar, aber nicht mehr Top-Level |
| Service | Service & Downloads | Erweitert um Download-Center, Haendlerfinder, Rechner |
| Kontakt | Kontakt | Bleibt |
| -- | **Anwendungen** (NEU) | Branchenspezifische Produktnavigation |
| -- | **Fuer Planer** (NEU) | Dedizierter Planerbereich |

### 6.2 Detailliertes Mapping

| Alter Menuepunkt | Neuer Ort | Status |
|-----------------|-----------|--------|
| Korodur → Unternehmen | Unternehmen | Umbenannt |
| Korodur → Geschichte | Unternehmen → Geschichte | Verschoben |
| Korodur → Nachhaltigkeit | Unternehmen → Nachhaltigkeit | Verschoben |
| Korodur → Standorte | Unternehmen → Standorte | Verschoben |
| Korodur → Presse | Unternehmen → News | Zusammengelegt mit Aktuelles |
| Korodur → Jobs & Karriere | Unternehmen → Karriere | Verschoben + Slug bereinigt |
| Bereiche → Industrieboden | Produkte → Industrieboden | Zusammengelegt |
| Bereiche → Sichtestrich | Produkte → Sichtestrich | Zusammengelegt |
| Bereiche → Microtop | Produkte → Microtop | Zusammengelegt |
| Bereiche → Rapid Set | Produkte → Rapid Set | Zusammengelegt |
| Bereiche → Schnellbetonsysteme | Produkte → Schnellbetonsysteme | Zusammengelegt |
| Bereiche → 3D Concrete Printing | Produkte → 3D Concrete Printing | Zusammengelegt |
| Bereiche → Spezialbaustoffe | Produkte → Spezialbaustoffe | Zusammengelegt |
| Bereiche → Katzenstreu | Produkte → Katzenstreu | Zusammengelegt |
| Produkte → [Kategorien] | Produkte → [Kategorien] | URL-Struktur bereinigt |
| Referenzen | Unternehmen (Mega) → Referenzen | Unter Unternehmen, weiterhin prominent |
| Service → Aktuelles | Unternehmen → News | Verschoben |
| Service → KORODUR Report | Unternehmen → KORODUR Report | Verschoben |
| Service → Lieferprogramm | Service → Lieferprogramm | Bleibt |
| Service → Leistungsverzeichnisse | **Planer → Ausschreibungstexte** | Verschoben + aufgewertet |
| Service → Leistungserklaerungen | **Service → Downloads** (Filter: DoP) | Konsolidiert |
| Service → Sicherheitsdatenblaetter | **Service → Downloads** (Filter: SDS) | Konsolidiert |
| Service → Reinigungsempfehlung | Service → Reinigungsempfehlung | Bleibt |
| Service → Anwendungsempfehlungen | Service → Anwendungsempfehlungen | Bleibt |
| Service → Datenblaetter | **Service → Downloads** (Filter: TDS) | Konsolidiert |
| Kontakt | Kontakt | Bleibt |
| -- | **Anwendungen (7 Branchen + 2 Anforderungen)** | NEU |
| -- | **Fuer Planer (6 Unterseiten)** | NEU |
| -- | **Service → Download-Center** | NEU (konsolidiert) |
| -- | **Service → Haendlerfinder** | NEU |
| -- | **Service → Verbrauchsrechner** | NEU |
| -- | **Service → FAQ** | NEU (erweitert) |
| -- | **Service → Schulungen** | NEU |
| -- | **Unternehmen → Qualitaet** | NEU |
| -- | **Produkte → Vergleich** | NEU |
| -- | **Produkte → Neuheiten** | NEU |

### 6.3 Zusammenfassung der Aenderungen

| Metrik | ALT | NEU |
|--------|-----|-----|
| Top-Level Menuepunkte | 7 (inkl. Bereiche als eigener Punkt) | 6 |
| Maximale Navigationstiefe | 5 Klicks | 3 Klicks |
| Zielgruppen-Einstiege | 0 | 3 (Planer, Verarbeiter, Haendler) |
| Download-Seiten (verstreut) | 5 separate Seiten | 1 zentrales Download-Center |
| Doppelte URL-Strukturen | Ja (Bereiche + Produktkategorien) | Nein |
| Haendlerfinder | Nicht vorhanden | Vorhanden |
| Planerbereich | Nicht vorhanden | 7 Seiten |
| Anwendungs-/Branchenseiten | Nicht vorhanden | 12 Seiten |
| CTAs pro Seite | 0 | Mindestens 1 |
| Tippfehler in URLs | Ja (/dattenblaetter/) | Nein |
| WooCommerce-URLs (/shop/, /produkt/) | Ja | Nein |
| Konsistente Slug-Uebersetzung | Nein (/en/produkt/) | Ja (/en/products/) |

---

## 7. Rollout-Plan (Schrittweiser Relaunch)

Die IA ist fuer einen schrittweisen Relaunch konzipiert. Jede Phase liefert sichtbare Ergebnisse, ohne die bestehende Seite komplett abzuschalten.

### Phase 1: Grundstruktur (Wochen 1-8)
**Ziel:** Neue Navigation, Planerbereich, Download-Center live

| Massnahme | Beschreibung |
|-----------|-------------|
| Neue Hauptnavigation | 6 Menuepunkte mit Mega-Menue |
| Homepage-Redesign | Zielgruppen-Kacheln, USP-Sektion, CTAs |
| Produkte-Zusammenfuehrung | Bereiche + Produktkategorien zusammenlegen |
| Planerbereich (Basis) | Landing Page + Ausschreibungstexte + Normen + Objektberatung |
| Download-Center | Zentral, filterbar (TDS, SDS, DoP, LV) |
| Redirect-Map | Alle 858 alten URLs → neue URLs (301) |
| Hreflang im HTML-Head | Ergaenzend zur Sitemap |
| Analytics einrichten | GA4 oder Matomo (Baseline!) |

### Phase 2: Anwendungen & Tools (Wochen 9-16)
**Ziel:** Anwendungsseiten, Haendlerfinder, erweiterte Produktseiten

| Massnahme | Beschreibung |
|-----------|-------------|
| Anwendungsseiten | 9 Branchenspezifische Seiten |
| Haendlerfinder | Karte + PLZ-Suche |
| Produktseiten anreichern | Technische Daten im HTML, Cross-Selling, Referenz-Links |
| Referenz-Produkt-Verknuepfung | Bidirektionale Verlinkung |
| Verbrauchsrechner | Einfacher kg/m2-Rechner |
| FAQ erweitern | Alle Produktgruppen |
| Produktvergleich | Vergleichstabellen fuer Hauptprodukte |

### Phase 3: Fortgeschrittene Features (Wochen 17-24)
**Ziel:** Produktfinder, Videos, Schulungen, Content-Hub

| Massnahme | Beschreibung |
|-----------|-------------|
| Interaktiver Produktfinder | Entscheidungsbaum nach Anwendung |
| Video-Integration | YouTube-Videos auf Produktseiten einbetten |
| Schulungen-Seite | Webinare, Seminare |
| Content-Hub / Blog | Fachwissen-Beitraege, Praxistipps |
| Systemaufbauten | Schichtaufbau-Visualisierung |
| Newsletter-Integration | Fuer Planer und Haendler |
| Geschuetzter Haendlerbereich | Login fuer Konditionen (optional) |

---

## 8. Technische Hinweise fuer WordPress-Umsetzung

### 8.1 Post Types

| Post Type | Verwendung | Bisherig |
|-----------|-----------|---------|
| `page` | Statische Seiten (Unternehmen, Planer, Service) | Wie bisher |
| `product` (Custom, NICHT WooCommerce) | Produktdetailseiten | War WooCommerce Product |
| `reference` (Custom) | Referenzprojekte | War Custom Post Type "referenzen" |
| `post` | News & Presse | Wie bisher |

### 8.2 Taxonomien

| Taxonomie | Verwendung |
|-----------|-----------|
| `product_group` | Industrieboden, Sichtestrich, Microtop, Rapid Set, ... |
| `product_subcategory` | Hartstoffeinstreuung, Hartstoffschicht, ... |
| `application_sector` | Logistik, Automotive, Lebensmittel, ... |
| `application_type` | Neubau, Sanierung |
| `reference_sector` | Logistik, Automotive, ... (gleich wie application_sector) |
| `reference_product` | Relation zu Produkten |
| `document_type` | TDS, SDS, DoP, LV, Anwendungsempfehlung |

### 8.3 Kritische Abhaengigkeiten

- **WooCommerce entfernen:** Alle Produkte auf Custom Post Type migrieren (oder WooCommerce-URLs per Rewrite umleiten)
- **WPML konfigurieren:** Neue URL-Slugs pro Sprache korrekt uebersetzen
- **Yoast konfigurieren:** Breadcrumbs, hreflang im Head, Schema.org korrigieren
- **Elementor evaluieren:** Mega-Menue ggf. ueber eigenes Widget oder Plugin (Max Mega Menu)

---

## 9. Offene Punkte & Empfehlungen

| # | Punkt | Empfehlung | Entscheidung noetig? |
|---|-------|-----------|---------------------|
| 1 | **Referenzen: Top-Level oder unter Unternehmen?** | Empfehlung: Unter Unternehmen im Mega-Menue, aber mit eigenem URL-Pfad `/referenzen/`. Prominent auf Homepage. Bei hohem Traffic evtl. als 7. Hauptpunkt. | Ja |
| 2 | **Katzenstreu: In Hauptnavigation?** | Empfehlung: Als Produktgruppe unter Produkte, aber keine eigene Anwendungsseite. Verweis auf goodcat.de im Footer beibehalten. | Nein |
| 3 | **3D Concrete Printing + Schnellbetonsysteme: Separate Gruppen?** | Empfehlung: Beibehalten als separate Gruppen, aber im Mega-Menue weniger prominent (unter "Weitere" oder 2. Spalte). | Nein |
| 4 | **INOTEC Pumptechnik:** | Empfehlung: Als Zubehoer unter Industrieboden listen, nicht als eigene Kategorie. | Nein |
| 5 | **Blog vs. News:** | Empfehlung: Vorerst als "News & Presse" unter Unternehmen. Spaeter (Phase 3) zu Content-Hub ausbauen. | Nein |
| 6 | **Login-Bereich fuer Haendler:** | Empfehlung: Phase 3. Erst Haendlerfinder (Phase 2), dann geschuetzter Bereich. | Ja (Timing) |
| 7 | **Tech-Stack-Wechsel:** | Empfehlung: IA ist WordPress-kompatibel konzipiert. Wenn Next.js/Headless angestrebt wird, muss die IA nicht angepasst werden -- nur die technische Umsetzung aendert sich. | Ja (spaeter) |

---

## Anhang A: Produktgruppen-Zuordnung (vollstaendig)

| Produktgruppe | Unterkategorie | Produkte (Auswahl) |
|---------------|---------------|-------------------|
| **Industrieboden** | Hartstoffeinstreuung | KORODUR 0-4, VS 0-5, PC, TXPK, WH Metallic, WH Special, EasyFinish, NanoFinish, HB 5, HB 5 Rapid |
| | Hartstoffschicht | NEODUR HE 2, HE 3, HE 3 Green, HE 3 Metallisch, HE 40, HE 40-8 |
| | | NEODUR HE 60 Rapid, HE 65, HE 65 Plus, HE 65 Metallisch |
| | | NEODUR HE 3 SVS 3, HE 3 SVS 15, HE 65 SVS 3, HE 65 SVS 15, HE 65 Plus SVS 3 |
| | Schnellestrich | KORODUR FScem, FScem Screed |
| | Selbstverlaufend | NEODUR Level, Level AU, SVM 03 |
| | Sanierung | NEODUR PFM 1K EasyFix, PFM ZE |
| | Hartstoff fuer Kunstharze | NEODUR MSM 3, MSM 5, MSB 8 |
| | Bauchemie | KOROMINERAL, KOROMINERAL Cure, KOROMINERAL LI, KOROCLEAN, KOROCURE, KOROCRETE, KOROTEX, UniPrimer, LEVELFLOR, DUROP |
| **Sichtestrich** | Geglaettet / Geschliffen / Truazzo | GRANIDUR, GRANIDUR Bianco Nero, Diamond Concrete, Copetti Floor (KCF), TRU PC, TRU Self-Leveling, TRU SP |
| **Microtop** | -- | MICROTOP TW 2, TW 3, TW 5, TW 8, TW BM, TW Mineral, TW NSM, TW VSM |
| **Rapid Set** | -- | Cement All, Mortar Mix, Concrete Mix, Concrete Pharmacy, DOT Europe, Rapid Set Concrete, Asphalt Repair Mix |
| **Schnellbetonsysteme** | -- | (Produkte aus Sitemap) |
| **Spezialbaustoffe** | Betoninstandsetzung | NEODUR Vergussmoertel Beton, VM Basic |
| | Injektionssystem | (Produkte aus Sortiment) |
| | Vergusssystem | (Produkte aus Sortiment) |
| **3D Concrete Printing** | -- | (Produkte aus Sortiment) |
| **Katzenstreu** | -- | GoodCat Silver Classic, GoodCat Golden Nature, GoodCat Organic Love |

---

## Anhang B: Anwendungsseiten -- Inhaltliche Zuordnung

| Anwendungsseite | Primaere Produktgruppen | Referenzbeispiele (bestehend) |
|----------------|------------------------|------------------------------|
| Logistik & Distribution | Industrieboden (HE 65, HE 3) | Amazon Bad Hersfeld, Zalando Bydgoszcz |
| Automotive & Produktion | Industrieboden (HE 65, HE 3, FScem) | BMW Wallersdorf, BMW Krefeld |
| Lebensmittel & Pharma | Industrieboden (HE 3 Green), Microtop | (zu recherchieren) |
| Handel & Retail | Sichtestrich (Diamond Concrete, Granidur) | Nike Kaunas, Balenciaga, Porsche Loerrach |
| Oeffentliche Gebaeude | Industrieboden, Sichtestrich | Olympiastadion Berlin |
| Trinkwasser | Microtop (TW-Serie) | Trinkwasserbehaelter Bad Nauheim, Puchheim |
| Wohnen & Hospitality | Sichtestrich, Truazzo | Moxy Hotels, Hotel Puro Krakow |
| Neubau (Anforderung) | Alle | (Querschnitt) |
| Sanierung (Anforderung) | Rapid Set, Spezialbaustoffe | (Querschnitt) |

---

*Erstellt am 2026-03-24 als Teil des KORODUR Website Relaunch Projekts, Phase 3 -- Konzept.*
