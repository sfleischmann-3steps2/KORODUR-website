# Strukturaudit – korodur.de
**Version:** 1.0 | **Datum:** 2026-03-24 | **Phase:** 1 – Analyse
**Quelle:** Sitemap-Crawl + HTML-Analyse (Cloudflare-geschuetzt, Sitemaps + HTML per curl)

---

## 1. Navigationsstruktur (DE)

### Hauptnavigation (Desktop)

```
Korodur (Dropdown, kein eigener Link)
├── Unternehmen                     /unternehmen/
├── Geschichte                      /unternehmen/geschichte/
├── Nachhaltigkeit                  /unternehmen/nachhaltigkeit/
├── Standorte                       /unternehmen/standorte/
├── Presse                          /unternehmen/presse/
└── Jobs & Karriere                 /unternehmen/jobs-karriere/

Bereiche                            /bereiche/
├── Industrieboden                  /bereiche/industrieboden/
├── Sichtestrich                    /bereiche/sichtestrich/
├── Microtop                        /bereiche/microtop/
├── Rapid Set                       /bereiche/rapid-set/
├── Schnellbetonsysteme             /bereiche/schnellbetonsysteme/
├── 3D Concrete Printing            /bereiche/3d-concrete-printing/
├── Spezialbaustoffe                /bereiche/spezialbaustoffe/
└── Katzenstreu                     /bereiche/katzenstreu/

Produkte                            /produkte/
├── Industrieboden                  /produkt-kategorie/industrieboden
├── Sichtestrich                    /produkt-kategorie/sichtestrich
├── Microtop                        /produkt-kategorie/microtop/
├── Rapid Set                       /produkt-kategorie/rapid-set/
├── Schnellbetonsysteme             /produkt-kategorie/Schnellbetonsysteme
├── 3D Concrete Printing            /produkt-kategorie/concrete-printing-3d/
├── Spezialbaustoffe                /produkt-kategorie/spezialbaustoffe
└── Katzenstreu                     /produkt-kategorie/katzenstreu

Referenzen                          /referenzen/
├── 3D Concrete Printing            /referenzen/?...reference-categories:350
├── Industrieboden                  /referenzen/?...reference-categories:128
├── Sichtestrich                    /referenzen/?...reference-categories:129
├── Microtop                        /referenzen/?...reference-categories:130
├── Rapid Set                       /referenzen/?...reference-categories:131
├── Schnellbetonsysteme             /referenzen/?...reference-categories:132
└── Spezialbaustoffe                /referenzen/?...reference-categories:133

Service                             /service/
├── Aktuelles                       /aktuelles/
├── KORODUR Report                  /?page_id=1090
├── Lieferprogramm                  /service/lieferprogramm/
├── Leistungsverzeichnisse          /service/leistungsverzeichnisse/
├── Leistungserklaerungen           /service/leistungserklaerungen/
├── Sicherheitsdatenblaetter        /service/sicherheitsdatenblaetter/
├── Reinigungsempfehlung            /service/reinigungsempfehlung/
├── Anwendungsempfehlungen          /service/anwendungsempfehlungen/
└── Datenblaetter                   /service/dattenblaetter/  (Tippfehler im Slug!)

Kontakt                             /kontakt/
├── Kontaktformular                 /kontakt/
├── Ansprechpartner Deutschland     /kontakt/deutschland/
└── Ansprechpartner International   /kontakt/international/
```

### Utility-Navigation (Top Bar)
- **Sprachwechsler:** DE | FR | EN (WPML, horizontale Liste)
- **Suchfunktion:** Jet Ajax Search (sucht in: page, product, referenzen)

### Footer-Navigation

```
Kontakt:
├── KORODUR International GmbH
├── Wernher-von-Braun-Str. 4, D-92224 Amberg
├── Tel: +49 (0) 9621 47 59-0
├── Fax: +49 (0) 9621 32 341
└── E-Mail: [email protected] (Cloudflare-verschluesselt)

Wichtige Links:
├── www.goodcat.de (extern)
├── www.korodur-rapidset.com (extern)
├── www.3d-concrete-printing.com (extern)
├── Impressum                       /impressum
├── Datenschutz                     /datenschutz
├── Hinweisgebersystem              /hinweisgebersystem
└── AGB                             /agb

Social Media:
├── LinkedIn: linkedin.com/company/korodur-international-gmbh
└── YouTube: youtube.com/user/KORODUR

Logo + Copyright:
└── (c) Copyright 2023 by Korodur.  (VERALTET – 2023 statt 2026!)
```

---

## 2. Navigationsstruktur (EN)

Die englische Navigation spiegelt die DE-Struktur. Wichtige Abweichungen:

```
Korodur
├── Company                         /en/company/
├── History                         /en/company/history/
├── Sustainability                  /en/company/sustainability/
├── Locations                       /en/company/locations/
├── Press                           /en/company/press/
└── Special Projects                /en/company/special-projects/
    (kein "Jobs & Karriere" Aequivalent sichtbar!)

Areas                               /en/areas/
├── Industrial Floor                /en/areas/industrial-floor/
├── Decorative Screed               /en/areas/decorative-screed/
├── Microtop                        /en/areas/microtop/
├── Rapid Set                       /en/areas/rapid-set/
├── Rapid Concrete Systems          /en/areas/rapid-concrete-systems/
├── 3D Concrete Printing            /en/areas/3d-concrete-printing/
├── Special Mortars                 /en/areas/special-mortars/
└── Cat Litter                      /en/areas/cat-litter/

Products                            /en/products/
(gleiche Kategorien wie DE, englisch)

References                          /en/references/

Service                             /en/service/
├── Data Sheets                     /en/service/datenblaetter/
├── Tender Specifications           /en/service/tender-specifications/
├── Declarations of Performance     /en/service/leistungserklaerungen/
├── Safety Data Sheets              /en/service/sicherheitsdatenblaetter/
├── Delivery Programme              /en/service/lieferprogramm/
├── Maintenance Hints               /en/service/maintenance-hints/
└── Application Recommendation      /en/service/anwendungsempfehlungen/

Contact                             /en/contact/
├── Germany                         /en/contact/germany/
└── International                   /en/contact/international/
```

---

## 3. Bereiche-Unterseiten (Tiefenstruktur)

Die "Bereiche"-Seiten bilden umfangreiche Informationsseiten pro Geschaeftsfeld:

### Industrieboden
```
/bereiche/industrieboden/
├── Was sind KORODUR Industrieboeden?
├── Hartstoffschicht                    (= Hartstoff-Coulis)
├── Hartstoffeinstreuung                (= Dry-Shake)
├── Schnellestrich-Systeme
├── Selbstverlaufende Systeme
├── Industriebodensanierung
├── Hartstoff fuer Kunstharze
├── Bauchemische Produkte
└── INOTEC Pumptechnik
```

### Sichtestrich
```
/bereiche/sichtestrich/
├── Geglaetteter Sichtestrich
├── Geschliffener Sichtestrich
└── Truazzo
```

### Microtop
```
/bereiche/microtop/
├── Nassspritzverfahren
└── Trockenspritzverfahren
```

### Rapid Set
```
/bereiche/rapid-set/
├── Rapid Set Technologie
├── Einzigartige Rapid Set Produkte
├── Cement All
├── Mortar Mix
├── Concrete Mix
├── Flow Control
├── Fast Control
├── Set Control
├── Concrete Pharmacy
├── Haeufige Fragen (FAQ)
└── Prospekte in verschiedenen Sprachen
```

### Spezialbaustoffe
```
/bereiche/spezialbaustoffe/
├── Betoninstandsetzung
├── Anker-Injektionssystem
└── Montage- und Vergusssystem
```

### Katzenstreu
```
/bereiche/katzenstreu/
├── Was ist Bentonit?
├── Premium-Qualitaeten
├── Standard-Qualitaeten
├── Unsere Marken
├── Private Label
└── Nachhaltigkeit
```

---

## 4. Produktkategorien (aus product_cat-Sitemap)

| DE Kategorie | EN Kategorie | FR Kategorie | Dreisprachig? |
|---|---|---|---|
| Alle | All | Tous | Ja |
| Industrieboden | Industrial floor | Sols industriels | Ja |
| - Hartstoffschicht | - Hartstoffschicht-en | - Coulis | Ja |
| - Hartstoffeinstreuung | - Hard Aggregate Dry-Shake | - Saupoudrage | Ja |
| - Schnellestrich-Systeme | - Fast Setting Screed | - Chape rapide | Ja |
| - Selbstverlaufende Systeme | - Self-Leveling Flooring | - Revetement autonivelant | Ja |
| - Industriebodensanierung | - Industrial Floor Repair | - Renovation de sols industriels | Ja |
| - Hartstoff fuer Kunstharze | - Hard Aggregates for Synthetic Resins | - Durcisseurs pour resines | Ja |
| - Bauchemische Produkte | - Building Chemical Products | - Produits chimiques de construction | Ja |
| Sichtestrich | Decorative Screed | Sols decoratifs | Ja |
| Microtop | Microtop | Microtop | Ja |
| Rapid Set | Rapid Set | Rapid Set | Ja |
| Schnellbetonsysteme | Rapid Concrete Systems | Systemes de beton rapide | Ja |
| 3D Concrete Printing | Concrete Printing 3D | Concrete Printing 3D | Ja |
| Spezialbaustoffe | Special Mortars | Materiaux speciaux | Ja |
| Katzenstreu | Cat Litter | Litiere pour chats | Ja |

---

## 5. Produktliste (aus product-Sitemap, nur DE-Slugs, dedupliziert)

**Gesamt: ca. 71 Produkte (DE)** | ca. 67 (EN) | ca. 63 (FR)

### Industrieboden-Produkte
- NEODUR HE 2, HE 3, HE 3 Green, HE 3 Metallisch, HE 3 SVS 3, HE 3 SVS 15
- NEODUR HE 40 / HE 40-8
- NEODUR HE 60 Rapid
- NEODUR HE 65, HE 65 Plus, HE 65 Metallisch, HE 65 SVS 3, HE 65 SVS 15, HE 65 Plus SVS 3
- NEODUR Level, Level AU
- NEODUR PFM 1K EasyFix, PFM ZE
- NEODUR SVM 03
- NEODUR MSM 3 / MSM 5 / MSB 8
- NEODUR Vergussmoertel Beton, Vergussmoertel VM Basic
- KORODUR 0-4, VS 0-5, PC, TXPK
- KORODUR HB 5, HB 5 Rapid
- KORODUR Diamond Concrete
- KORODUR EasyFinish, NanoFinish
- KORODUR WH Metallic, WH Special
- KORODUR FScem, FScem Screed, Copetti Floor (KCF)
- KORODUR UniPrimer
- KOROMINERAL, KOROMINERAL Cure, KOROMINERAL LI
- KOROCLEAN, KOROCURE, KOROCRETE, KOROTEX
- LEVELFLOR
- DUROP
- KORODUR Silosystem

### Sichtestrich-Produkte
- GRANIDUR, GRANIDUR Bianco Nero
- TRU PC, TRU Self-Leveling, TRU SP

### Microtop-Produkte
- MICROTOP TW 2, TW 3, TW 5, TW 8
- MICROTOP TW BM, TW Mineral, TW NSM, TW VSM

### Rapid Set Produkte
- Cement All, Mortar Mix, Concrete Mix
- Concrete Pharmacy
- DOT Europe Concrete Mix
- Rapid Set Concrete
- Asphalt Repair Mix

### Katzenstreu
- GoodCat Silver Classic, GoodCat Golden Nature, GoodCat Organic Love

### WooCommerce-Shop
- `/shop/` existiert (WooCommerce-basiert)
- Produkte haben SKUs (z.B. 1220116S25KG fuer NEODUR HE 3)
- KEIN Warenkorb / Bestellfunktion sichtbar (cart_url zeigt auf Homepage)

---

## 6. Referenzprojekte (aus referenzen-Sitemap)

**Gesamt: ca. 130 Referenzen (DE)** | ca. 128 (EN) | ca. 126 (FR)

Filterbar nach Kategorien via JetSmartFilters:
- 3D Concrete Printing, Industrieboden, Sichtestrich, Microtop, Rapid Set, Schnellbetonsysteme, Spezialbaustoffe

Beispiel-Referenzen (Auswahl):
- Zalando Bydgoszcz, Amazon Logistikzentrum Bad Hersfeld/Wroclaw
- BMW Logistikzentrum Wallersdorf, BMW Ausstellungshalle Krefeld
- Olympiastadion Berlin, Airbus A-380 Hamburg
- Nike Store Kaunas/Szczecin, Balenciaga Flagship Store
- Porsche Showroom Loerrach, Leica Firmenzentrale Wetzlar
- Moxy Hotels, Hotel Puro Krakow
- Trinkwasserbehaelter Bad Nauheim/Puchheim/Haidberg/Raecknitz

---

## 7. News / Blog (aus post-Sitemap)

**Gesamt: 5 Posts**
- Aktuelles (Uebersichtsseite)
- KORODUR auf YouTube (DE/EN/FR)
- Neues Zalando Logistikzentrum setzt auf KORODUR (nur DE!)
- KORODUR goes green (DE/EN/FR)

**Bewertung: Extrem duenn.** Letzte Aktualisierung: November 2024. Nur 3 echte News-Beitraege.

---

## 8. Informationsarchitektur – Bewertung

### 8.1 Klick-Pfade

| Ziel | Pfad | Klicks | Bewertung |
|---|---|---|---|
| Planer → TDS (Datenblatt) | Home → Service → Datenblaetter | 3 | Akzeptabel |
| Planer → TDS via Produkt | Home → Produkte → Kategorie → Produkt → Tab "Downloads" | 5 | Zu viele Klicks |
| Planer → Ausschreibungstexte | Home → Service → Leistungsverzeichnisse | 3 | Akzeptabel |
| Planer → Ausschreibungstexte via Produkt | Produkt → Tab "Additional Info" → Tender Specs | 4+ | Umstaendlich |
| Verarbeiter → Anwendungsempfehlung | Home → Service → Anwendungsempfehlungen | 3 | Akzeptabel |
| Verarbeiter → Verarbeitungshinweise | Nur ueber Produkt-Tab erreichbar | 4-5 | Zu versteckt |
| Handel → Produktuebersicht | Home → Produkte | 2 | OK |
| Handel → Haendlersuche | NICHT VORHANDEN | - | Fehlt komplett |

### 8.2 Strukturelle Probleme

1. **Doppelte Hierarchie "Bereiche" vs "Produkte":**
   - "Bereiche" = Informationsseiten pro Geschaeftsfeld (Content-fokussiert)
   - "Produkte" = WooCommerce-Produktkatalog (Datenblatt-fokussiert)
   - Nutzer muessen verstehen, welcher Einstieg fuer sie relevant ist
   - **Empfehlung:** Zusammenfuehren oder klarer differenzieren

2. **Service als Sammelkategorie:**
   - Mischung aus News, Downloads, technischen Dokumenten
   - Kein klarer Zielgruppen-Bezug
   - "Dattenblaetter" statt "Datenblaetter" (Tippfehler im Slug)

3. **WooCommerce als CMS-Kruecke:**
   - Produkte laufen ueber WooCommerce mit /shop/, /produkt/, Warenkorb-Logik
   - Aber kein E-Commerce aktiv (keine Preise, kein Checkout)
   - Unnoetige Komplexitaet

4. **Copyright veraltet:** Footer zeigt "(c) Copyright 2023"

---

## 9. Zielgruppen-Navigation

### 9.1 Explizite Zielgruppen-Adressierung

| Kriterium | Vorhanden? | Bewertung |
|---|---|---|
| "Fuer Planer" Einstieg | Nein | 1/5 |
| "Fuer Verarbeiter" Einstieg | Nein | 1/5 |
| "Fuer Haendler" Einstieg | Nein | 1/5 |
| Zielgruppenspez. Landing Pages | Nein | 1/5 |
| Branchenseiten (Logistik, Automotive, ...) | Nein | 1/5 |

**Fazit: Keine explizite Zielgruppen-Navigation vorhanden.** Die Seite ist rein produkt-/bereichsorientiert strukturiert. Es fehlt jegliche "Was suchen Sie?"-Weichenstellung.

### 9.2 Zielgruppen-spezifische Einstiegspunkte

- **Planer:** Muessten sich durch Service-Unterpunkte klicken (LV, TDS, SDS)
- **Verarbeiter:** Finden Anwendungsempfehlungen nur unter Service
- **Handel:** Kein Haendlerportal, kein Login, keine Bestellmoeglichkeit

---

## 10. Mehrsprachige Konsistenz

### 10.1 Sprachen
- **DE** (Primaersprache, Standard/x-default)
- **EN** (vollstaendig uebersetzt)
- **FR** (weitgehend uebersetzt)

### 10.2 Stichproben-Vergleich

| Seite (DE) | EN vorhanden? | FR vorhanden? |
|---|---|---|
| / (Homepage) | Ja | Ja |
| /unternehmen/ | /en/company/ | /fr/entreprise/ |
| /unternehmen/jobs-karriere/ | NEIN (fehlt!) | NEIN (fehlt!) |
| /bereiche/industrieboden/ | /en/areas/industrial-floor/ | /fr/domaines/sols-industriels/ |
| /produkte/ | /en/products/ | /fr/produits/ |
| /referenzen/ | /en/references/ | /fr/references/ |
| /service/ | /en/service/ | /fr/service/ |
| /kontakt/ | /en/contact/ | /fr/contact/ |
| /unternehmen/spezialprojekte/ | /en/company/special-projects/ | /fr/entreprise/projets-speciaux/ |
| /bauarbeiten-im-gange/ | NEIN | NEIN |
| /service/sicherheitsunterweisung/ | NEIN (nur DE) | NEIN |
| /service/reinigungsempfehlung/ | NEIN (nur DE) | NEIN |

### 10.3 Produkt-Paritaet

| Sprache | Produkte in Sitemap |
|---|---|
| DE | ~71 |
| EN | ~67 |
| FR | ~63 |

**Einige Produkte fehlen auf EN/FR:**
- KORODUR Silosystem (nur DE)
- NEODUR Vergussmoertel VM Basic (nur DE)
- KCF / Copetti Floor (nur EN, nicht DE?)
- KOROCRETE (nur DE+EN, nicht FR)
- GoodCat-Produkte (nur DE)
- FR hat einige Zusatz-Varianten (z.B. NEODUR HE 60 Rapid Metallisch, SVS-Varianten nur FR)

### 10.4 News-Paritaet
- Zalando-Artikel: nur DE
- KORODUR goes green: DE/EN/FR
- YouTube-Seite: DE/EN/FR

### 10.5 URL-Muster
- DE: `/bereiche/`, `/produkt/`, `/referenzen/`, `/service/`
- EN: `/en/areas/`, `/en/produkt/` (NICHT /en/product/!), `/en/references/`, `/en/service/`
- FR: `/fr/domaines/`, `/fr/produkt/`, `/fr/references/`, `/fr/service/`

**Auffaellig:** Produkt-Slugs sind NICHT uebersetzt (z.B. `/en/produkt/neodur-he-3/` statt `/en/product/neodur-he-3/`)

---

## 11. Homepage-Content

### Hero-Slider (8 Slides)
1. "KORODUR – Qualitaet fuer Generationen" (Link zu Presse)
2. "KORODUR – Qualitaet fuer Generationen"
3. "KORODUR Sichtestrich – natuerlich. nachhaltig. anders."
4. "MICROTOP – Spritzmoertel fuer Trinkwasserbehaelter"
5. "Rapid Set – Reparaturmoertel"
6. "3D-Betondruck"
7. "Katzenstreu – aus 100% Naturmineral"
8. "KORODUR – Ihr verlaesslicher Partner"

### Sektionen auf Homepage
1. Hero-Slider
2. "HERZLICH WILLKOMMEN BEI KORODUR" / "QUALITAET FUER GENERATIONEN"
3. "BEREICHE" / "WAS WIR MACHEN" (4-Spalten-Grid mit Bereichskarten)
4. Produktkategorie-Carousel (WooCommerce-Kategorien als Karussell)
5. Footer

### Fehlende Homepage-Elemente
- Keine USP-Sektion
- Kein Trust-Bereich (Zertifikate, Awards, Zahlen)
- Keine Referenz-Highlights
- Keine News-Teaser
- Kein CTA ("Kontaktieren Sie uns", "Jetzt beraten lassen")
- Kein "750 Mio. m2 verlegt" trotz Meta-Description

---

## 12. Zusammenfassung – Strukturelle Staerken & Schwaechen

### Staerken
- Dreisprachige Struktur konsequent umgesetzt (DE/EN/FR)
- Vollstaendiger Produktkatalog mit SKUs
- ~130 Referenzprojekte mit Kategorie-Filtern
- Umfangreiche Bereiche-Seiten mit Tiefeninfo
- Service-Bereich mit TDS, SDS, LV, Anwendungsempfehlungen

### Schwaechen (priorisiert)
1. **Keine Zielgruppen-Navigation** – Planer, Verarbeiter, Handel werden nicht adressiert
2. **Doppelstruktur Bereiche/Produkte** verwirrt Nutzer
3. **Kein CTA auf der Homepage** – weder Kontakt noch Beratung noch Download
4. **WooCommerce ohne E-Commerce** – technischer Overhead, verwirrende /shop/-URLs
5. **News quasi tot** – 3 Beitraege, letzter von Nov 2024
6. **Kein Haendlerportal, kein Login, kein Produktfinder**
7. **Tippfehler in URLs** (/service/dattenblaetter/ statt /datenblaetter/)
8. **Copyright veraltet** (2023)
9. **Produkt-Slugs nicht uebersetzt** (/en/produkt/ statt /en/product/)
10. **Keine Suche-Ergebnisseite** (nur Ajax-Suche mit 5 Ergebnissen)
