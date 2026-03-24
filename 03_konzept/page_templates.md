# Seitentypen & Wireframe-Beschreibungen -- korodur.de
**Version:** 1.0 | **Datum:** 2026-03-24 | **Phase:** 3 -- Konzept
**Erstellt von:** Claude Code (Konzept-Agent)
**Basis:** ia_new.md, zielgruppen.md, feature_matrix.md, content_audit.md

---

## Globale Elemente (auf allen Seitentypen)

### Header/Navigation
```
┌─────────────────────────────────────────────────────────────────────────────┐
│ [Logo KORODUR]  Produkte | Anwendungen | Fuer Planer | Service & Downloads │
│                 | Unternehmen | Kontakt          [Suche] [DE|EN|FR] [Tel]  │
└─────────────────────────────────────────────────────────────────────────────┘
```
- Sticky Header (Desktop + Mobile)
- Mega-Menues fuer Produkte, Anwendungen, Fuer Planer, Service & Downloads, Unternehmen
- Telefonnummer sichtbar im Header (nicht nur Footer!)
- Sprachwechsel DE/EN/FR als Dropdown
- Mobile: Hamburger-Menue mit Akkordeon-Unternavigation

### Footer
```
┌─────────────────────────────────────────────────────────────────────────────┐
│  PRODUKTE        SERVICE          UNTERNEHMEN      KONTAKT                 │
│  Industrieboden  Download-Center  Geschichte       Tel: +49 9621 4759-0    │
│  Sichtestrich    Haendlerfinder   Nachhaltigkeit   E-Mail: info@korodur.de│
│  Microtop        Verbrauchsrechner Referenzen      Standorte               │
│  Rapid Set       FAQ              News             Kontaktformular         │
│  ...             Schulungen       Karriere                                 │
│                                                                            │
│  [Newsletter-Anmeldung: E-Mail-Feld + Button]                             │
│                                                                            │
│  [LinkedIn] [YouTube]    ISO 9001 Badge    (c) KORODUR International GmbH │
│  Impressum | Datenschutz | AGB | Hinweisgebersystem                       │
└─────────────────────────────────────────────────────────────────────────────┘
```

### CTA-Sticky-Bar (Mobile)
- Fixierte Leiste am unteren Bildschirmrand auf Smartphones
- Buttons: "Anrufen" | "Anfragen" | "Downloads"
- Erscheint auf allen Seiten ausser Homepage und Kontakt

---

## 1. Homepage

### A) Zweck & Zielgruppe
Die Homepage ist das Schaufenster und der zentrale Verteiler. Sie muss in 5 Sekunden vermitteln, wer KORODUR ist, und alle drei Zielgruppen (Planer, Verarbeiter, Handel) in ihre jeweiligen Bereiche leiten. Groesster Schwachpunkt bisher: Null CTAs, keine Zielgruppen-Einstiege, toter Hero-Slider.

**Primaere Zielgruppe:** Alle (Erstbesucher und Wiederkehrende)

### B) Content-Elemente

1. **Hero-Bereich**
   - Vollbreites Hintergrundbild (Industrieboden in Aktion, z.B. Logistikhalle)
   - Headline: "Qualitaet fuer Generationen -- mineralische Industrieboeden seit 1936"
   - Sub-Headline: 1 Satz Value Proposition
   - 2 CTAs: "Produkte entdecken" (primaer) | "Beratung anfragen" (sekundaer)
   - Kein Auto-Slider -- statisches Hero oder max. 2 Slides mit Pause-Button

2. **Zielgruppen-Einstiege (3 Kacheln)**
   - "Fuer Planer & Architekten" -- Ausschreibungstexte, Downloads, Normen → `/planer/`
   - "Fuer Verarbeiter" -- Verarbeitungshinweise, Rechner, Videos → `/service/verarbeitungshinweise/`
   - "Fuer Handel & Distributoren" -- Haendlerfinder, Lieferprogramm, Anfrage → `/service/haendlerfinder/`
   - Jede Kachel: Icon + 3 Stichpunkte + Link "Mehr erfahren"

3. **Produktbereiche (8 Kacheln mit Bild)**
   - Industrieboden, Sichtestrich, Microtop, Rapid Set, Schnellbetonsysteme, Spezialbaustoffe, 3D Concrete Printing, Katzenstreu (GoodCat)
   - Bild + Name + 1-Zeiler + Link zur Produktgruppe
   - Responsive: 4 Spalten Desktop, 2 Spalten Tablet, 1 Spalte Mobile

4. **USP-Leiste (Trust-Sektion)**
   - "750 Mio. m2 verlegt" | "Seit 1936" | "ISO 9001 zertifiziert" | "4 Produktionsstandorte"
   - Animierte Zaehler (optional, WordPress-Plugin moeglich)
   - Heller Hintergrund, Icons + Zahlen

5. **Referenz-Highlights (3-4 Projekte)**
   - Bildkacheln mit Overlay: Projektname, Branche, Standort
   - CTA: "Alle Referenzen ansehen" → `/referenzen/`

6. **News-Teaser (2-3 aktuelle Beitraege)**
   - Datum + Titel + Anreisser (2 Zeilen) + "Weiterlesen"
   - CTA: "Alle News" → `/unternehmen/news/`

7. **Kontakt-CTA-Leiste (volle Breite)**
   - "Sie haben ein Projekt? Wir beraten Sie gerne."
   - Buttons: "Kontakt aufnehmen" | "Objektberatung" | "+49 9621 4759-0"

### C) Wireframe-Beschreibung
```
┌─────────────────────────────────────────────────────────────┐
│                     Header / Navigation                      │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│          HERO: Vollbild + Headline + 2 CTAs                 │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐      │
│  │  FUR PLANER  │  │FUR VERARBEIT.│  │  FUR HANDEL  │      │
│  │  Icon + 3 SP │  │  Icon + 3 SP │  │  Icon + 3 SP │      │
│  │  [Mehr →]    │  │  [Mehr →]    │  │  [Mehr →]    │      │
│  └──────────────┘  └──────────────┘  └──────────────┘      │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  PRODUKTBEREICHE (8 Kacheln, je Bild + Name + 1-Zeiler)    │
│  ┌────┐ ┌────┐ ┌────┐ ┌────┐                               │
│  │Ind.│ │Sich│ │Micr│ │Rapi│                               │
│  └────┘ └────┘ └────┘ └────┘                               │
│  ┌────┐ ┌────┐ ┌────┐ ┌────┐                               │
│  │Schn│ │Spez│ │3D  │ │Katz│                               │
│  └────┘ └────┘ └────┘ └────┘                               │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│  USP-LEISTE: 750 Mio m2 | Seit 1936 | ISO 9001 | 4 Werke  │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  REFERENZ-HIGHLIGHTS (3-4 Projekte mit Bild)                │
│  [Alle Referenzen →]                                        │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  NEWS-TEASER (2-3 aktuelle Beitraege)                       │
│  [Alle News →]                                              │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│  KONTAKT-CTA: "Projekt? Wir beraten Sie."                  │
│  [Kontakt] [Objektberatung] [Telefon]                       │
├─────────────────────────────────────────────────────────────┤
│                        Footer                                │
└─────────────────────────────────────────────────────────────┘
```

### D) Dynamische Elemente
- Referenz-Highlights: 3-4 Projekte per WP-Query (Custom Post Type "Referenz", sortiert nach Datum oder manuell kuratiert)
- News-Teaser: 2-3 neueste Posts aus Kategorie "News"
- Produktbereiche: Kacheln per Custom Fields oder manuell (8 Stueck, selten geaendert)

### E) SEO-Anforderungen
- **Title:** "KORODUR -- Mineralische Industrieboeden & Hartstoffe seit 1936"
- **Meta-Description:** "Industrieboeden, Hartstoffe, Sichtestrich und Schnellreparatur-Moertel von KORODUR. Seit 1936. Fuer Planer, Verarbeiter und den Fachhandel."
- **Schema.org:** Organization + WebSite + SearchAction
- **H1:** "Mineralische Industrieboeden & Hartstoffe" (1x, im Hero)

### F) Besonderheiten fuer Mehrsprachigkeit
- Hero-Headline, Zielgruppen-Kacheln, USPs: vollstaendig uebersetzen
- Produktnamen (NEODUR, GRANIDUR etc.) bleiben sprachunabhaengig
- Referenz-Highlights: gleiche Projekte oder ggf. laenderspezifisch
- EN Title: "KORODUR -- Mineral Industrial Floors & Hardeners since 1936" (NICHT "Homepage -- korodur")

### G) Verknuepfungen
→ Produktgruppen-Seiten, Planerbereich, Verarbeiter-Service, Haendlerfinder, Referenzprojekte, News, Kontakt

---

## 2. Produktuebersicht (Kategorie)

### A) Zweck & Zielgruppe
Zeigt alle Produkte einer Produktgruppe (z.B. Industrieboden) mit filtern/sortieren. Dient als Einstieg in den Produktkatalog. Loesung fuer die alte Doppelstruktur: Bereiche-Content + WooCommerce-Kategorien werden hier zusammengefuehrt.

**Primaere Zielgruppe:** Alle (Planer suchen nach Produktgruppe, Verarbeiter nach Anwendung, Handel nach Sortiment)

### B) Content-Elemente

1. **Breadcrumb**
   - Home > Produkte > Industrieboden

2. **Kategorie-Header**
   - Ueberschrift (H1): "Industrieboden"
   - Einfuehrungstext (2-3 Absaetze): bisheriger "Bereiche"-Content, erklaerend, informativ
   - Optional: Hero-Bild der Kategorie
   - CTA: "Beratung anfragen" + "Download Lieferprogramm"

3. **Unterkategorien-Navigation** (wenn vorhanden)
   - Kacheln oder Tabs: Hartstoffeinstreuung | Hartstoffschicht | Schnellestrich | Selbstverlaufend | Sanierung | Bauchemie | Hartstoff fuer Kunstharze
   - Nur bei Industrieboden, Sichtestrich, Spezialbaustoffe (die Unterkategorien haben)

4. **Produktliste**
   - Grid-Ansicht (Standard) oder Listenansicht (umschaltbar)
   - Pro Produkt: Bild + Produktname + Kurzbeschreibung (1 Satz) + 2-3 Kerndaten (Verschleissklasse, Anwendung) + "Details ansehen"-Link
   - Filter-Sidebar (Desktop) / Filter-Akkordeon (Mobile):
     - Nach Anwendung (Neubau/Sanierung)
     - Nach Eigenschaft (Verschleissklasse, Druckfestigkeit)
     - Nach Norm (DIN 18560, DIN EN 13813)

5. **Verwandte Anwendungen**
   - "Diese Produkte finden Sie auch unter:" → Links zu Anwendungsseiten (z.B. Logistik, Automotive)

6. **CTA-Leiste**
   - "Nicht sicher, welches Produkt?" → Produktfinder / Beratung anfragen

### C) Wireframe-Beschreibung
```
┌─────────────────────────────────────────────────────────────┐
│                     Header / Navigation                      │
├─────────────────────────────────────────────────────────────┤
│  Breadcrumb: Home > Produkte > Industrieboden               │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  H1: Industrieboden                                         │
│  [Einfuehrungstext 2-3 Absaetze]                            │
│  [CTA: Beratung anfragen]                                   │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│  Unterkategorien: [Hartstoffeinstr.] [Hartstoffschicht] ... │
├──────────────┬──────────────────────────────────────────────┤
│  FILTER      │  PRODUKTLISTE (Grid)                         │
│              │  ┌─────┐ ┌─────┐ ┌─────┐                    │
│  Anwendung   │  │Prod1│ │Prod2│ │Prod3│                    │
│  □ Neubau    │  │Bild │ │Bild │ │Bild │                    │
│  □ Sanierung │  │Name │ │Name │ │Name │                    │
│              │  │1 Satz│ │1 Satz│ │1 Satz│                  │
│  Eigenschaft │  │[→]  │ │[→]  │ │[→]  │                    │
│  □ AR 0.5   │  └─────┘ └─────┘ └─────┘                    │
│  □ AR 1     │                                               │
│              │  ┌─────┐ ┌─────┐ ┌─────┐                    │
│  Norm        │  │Prod4│ │Prod5│ │Prod6│                    │
│  □ DIN 18560│  └─────┘ └─────┘ └─────┘                    │
│              │                                               │
├──────────────┴──────────────────────────────────────────────┤
│  Verwandte Anwendungen: Logistik | Automotive | ...         │
├─────────────────────────────────────────────────────────────┤
│  CTA: "Nicht sicher? → Produktfinder | Beratung anfragen"  │
├─────────────────────────────────────────────────────────────┤
│                        Footer                                │
└─────────────────────────────────────────────────────────────┘
```

### D) Dynamische Elemente
- Produktliste: WP Query (Custom Post Type "Produkt") gefiltert nach Taxonomie "Produktgruppe"
- Filter: Ajax-basiert (kein Seitenneuladen), WP + Custom Taxonomies oder Elementor Pro Posts Widget
- Unterkategorien: Child Terms der Taxonomie
- Einfuehrungstext: ACF-Feld auf der Taxonomie-Term-Seite (oder WP-Kategoriebeschreibung)

### E) SEO-Anforderungen
- **Title-Schema:** "[Produktgruppe] -- KORODUR Industrieboeden" z.B. "Hartstoffeinstreuung -- KORODUR Industrieboeden"
- **Meta-Description-Schema:** "KORODUR [Produktgruppe]: [2-3 Kerneigenschaften]. [Anzahl] Produkte fuer [Anwendung]. TDS-Download, Ausschreibungstexte, Beratung."
- **Schema.org:** CollectionPage + BreadcrumbList
- **H1:** Kategoriename (1x)
- **Interne Verlinkung:** Jedes Produkt, verwandte Anwendungsseiten, Planerbereich

### F) Besonderheiten fuer Mehrsprachigkeit
- Kategorie-Slugs uebersetzen: `/produkte/industrieboden/` → `/en/products/industrial-floor/` → `/fr/produits/sols-industriels/`
- Einfuehrungstext pro Sprache pflegen
- Filter-Labels uebersetzen
- Produktnamen (Markennamen) bleiben identisch

### G) Verknuepfungen
→ Produktdetailseiten, Anwendungsseiten, Produktfinder, Planerbereich, Download-Center

---

## 3. Produktdetailseite

### A) Zweck & Zielgruppe
Die zentrale Informationsseite pro Produkt. Muss drei fundamental verschiedene Beduerfnisse erfuellen: Planer brauchen technische Daten + Ausschreibungstexte, Verarbeiter brauchen Verarbeitungsdaten + Videos + SDS, Handel braucht Uebersicht + "Wo kaufen?". **Groesste Baustelle der alten Website:** Keine CTAs, keine tech. Daten im HTML, keine Cross-Links, keine Referenzverknuepfung.

**Primaere Zielgruppe:** Planer (Evaluation), Verarbeiter (Praxis), Handel (Sortiment)

### B) Content-Elemente

1. **Breadcrumb**
   - Home > Produkte > Industrieboden > NEODUR HE 3

2. **Produkt-Header**
   - Produktbild(er): Hauptbild + Galerie (3-5 Bilder: Produkt, Anwendung, Ergebnis)
   - H1: Produktname ("NEODUR HE 3")
   - Untertitel/Claim: "Mineralischer Hartstoff fuer hochbelastbare Industrieboeden"
   - Produktgruppe (verlinkt): Industrieboden > Hartstoffeinstreuung
   - Kerndaten-Box (immer sichtbar):
     - Verschleissklasse / Druckfestigkeit / Schichtdicke / Normen
   - **CTA-Cluster** (prominent, rechtsseitig oder unter Kerndaten):
     - "TDS herunterladen" (primaer)
     - "Ausschreibungstext (GAEB)" (primaer)
     - "Beratung anfragen" (sekundaer)
     - "Wo kaufen?" (sekundaer) → Haendlerfinder

3. **Tab-Navigation** (oder Akkordeon auf Mobile)
   - **Tab 1: Beschreibung** -- Ausfuehrliche Produktbeschreibung, Anwendungsgebiete, Vorteile, Systemkomponenten
   - **Tab 2: Technische Daten** -- HTML-Tabelle (!) mit allen Kennwerten aus dem TDS (Druckfestigkeit, Biegezugfestigkeit, Verschleissklasse, Verarbeitungstemperatur, Mischverhaeltnis, Schichtdicke etc.). NICHT nur als PDF!
   - **Tab 3: Verarbeitung** -- Verarbeitungshinweise (Text), Systemaufbau-Diagramm, eingebettetes YouTube-Video (wenn vorhanden)
   - **Tab 4: Downloads** -- TDS (DE/EN/FR), SDS (DE/EN/FR), DoP, Ausschreibungstext (PDF + GAEB), Anwendungsempfehlung, Farbkarte (wenn relevant)
   - **Tab 5: Normen & Zertifikate** -- Erfuellte Normen (DIN 18560, DIN EN 13813 etc.), Zulassungen, DoP-Verweis

4. **Referenzprojekte mit diesem Produkt**
   - 3-4 Referenzen als Kacheln (Bild + Projektname + Branche + Standort)
   - CTA: "Alle Referenzen mit NEODUR HE 3" → gefilterte Referenzuebersicht

5. **Verwandte Produkte**
   - "Fuer aehnliche Anwendungen:" -- 3-4 Alternativprodukte (z.B. HE 65, HE 65 Plus)
   - "Systemkomponenten:" -- Primer, Nachbehandlung etc.

6. **CTA-Leiste (volle Breite)**
   - "Interesse an NEODUR HE 3? Wir beraten Sie persoenlich."
   - Buttons: "Objektberatung anfragen" | "Technische Hotline: +49 9621 4759-XX"

### C) Wireframe-Beschreibung
```
┌─────────────────────────────────────────────────────────────┐
│                     Header / Navigation                      │
├─────────────────────────────────────────────────────────────┤
│  Breadcrumb: Home > Produkte > Industrieboden > NEODUR HE 3│
├──────────────────────────┬──────────────────────────────────┤
│                          │                                   │
│  [Produktbild]           │  H1: NEODUR HE 3                │
│  [Galerie 3-5 Bilder]   │  "Mineralischer Hartstoff ..."   │
│                          │  Produktgruppe: Industrieboden   │
│                          │                                   │
│                          │  KERNDATEN-BOX                   │
│                          │  Verschleissklasse: AR 0.5       │
│                          │  Druckfestigkeit: > 90 N/mm2    │
│                          │  Schichtdicke: 5-8 mm            │
│                          │  Norm: DIN 18560, EN 13813       │
│                          │                                   │
│                          │  [TDS ↓] [GAEB ↓]              │
│                          │  [Beratung] [Wo kaufen?]         │
│                          │                                   │
├──────────────────────────┴──────────────────────────────────┤
│  [Beschreibung] [Techn. Daten] [Verarbeitung] [Downloads]  │
│  [Normen]                                                    │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  TAB-INHALT (z.B. Technische Daten):                        │
│  ┌──────────────────────┬──────────────────────┐            │
│  │ Eigenschaft          │ Wert                 │            │
│  ├──────────────────────┼──────────────────────┤            │
│  │ Druckfestigkeit      │ > 90 N/mm2           │            │
│  │ Biegezugfestigkeit   │ > 12 N/mm2           │            │
│  │ Verschleissklasse    │ AR 0.5 (DIN 18560)   │            │
│  │ Verarbeitungstempe.  │ 5-30 °C              │            │
│  │ Mischverhaeltnis     │ 1:4 (Wasser:Pulver)  │            │
│  │ Verbrauch            │ ca. 5 kg/m2           │            │
│  └──────────────────────┴──────────────────────┘            │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│  REFERENZPROJEKTE MIT DIESEM PRODUKT                        │
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌─────┐                          │
│  │Ref1 │ │Ref2 │ │Ref3 │ │Ref4 │                          │
│  └─────┘ └─────┘ └─────┘ └─────┘                          │
│  [Alle Referenzen mit NEODUR HE 3 →]                       │
├─────────────────────────────────────────────────────────────┤
│  VERWANDTE PRODUKTE            SYSTEMKOMPONENTEN            │
│  ┌─────┐ ┌─────┐ ┌─────┐     ┌─────┐ ┌─────┐             │
│  │HE 65│ │HE65+│ │Green│     │Prim.│ │Nachb│             │
│  └─────┘ └─────┘ └─────┘     └─────┘ └─────┘             │
├─────────────────────────────────────────────────────────────┤
│  CTA: "Interesse? Wir beraten Sie."                        │
│  [Objektberatung] [Hotline +49 9621 4759-XX]               │
├─────────────────────────────────────────────────────────────┤
│                        Footer                                │
└─────────────────────────────────────────────────────────────┘
```

### D) Dynamische Elemente
- Produktdaten: ACF-Felder (Custom Fields) auf Custom Post Type "Produkt"
- Technische Daten (HTML-Tabelle): ACF Repeater Field oder aus Notion-DB synchronisiert (Produktdatenbank-Projekt)
- Downloads: ACF File Fields (TDS, SDS, DoP, GAEB, LV-PDF) pro Sprache
- Referenzen: WP Relationship Field (Produkt ↔ Referenz, bidirektional)
- Verwandte Produkte: Manuell kuratiert (ACF Relationship) oder automatisch (gleiche Kategorie)
- Video: ACF oEmbed Field (YouTube-URL)

### E) SEO-Anforderungen
- **Title-Schema:** "[Produktname] -- [Produktgruppe] | KORODUR" z.B. "NEODUR HE 3 -- Hartstoffeinstreuung | KORODUR"
- **Meta-Description-Schema:** "[Produktname]: [Haupteigenschaft]. Verschleissklasse [X], Druckfestigkeit [X]. TDS-Download, Ausschreibungstext, Referenzen. KORODUR seit 1936."
- **Schema.org:** Product (name, description, brand, offers.priceCurrency, sku, image) + BreadcrumbList
- **H1:** Produktname (1x)
- **Technische Daten im HTML** = SEO-Goldgrube (indexierbar, Rich Snippets moeglich)

### F) Besonderheiten fuer Mehrsprachigkeit
- Produktnamen bleiben identisch (NEODUR, GRANIDUR etc.)
- Beschreibungstexte, Tab-Labels, Kerndaten-Labels uebersetzen
- Downloads: TDS/SDS pro Sprache verlinken (DE-TDS, EN-TDS, FR-TDS)
- Hreflang-Tags: `/produkte/industrieboden/neodur-he-3/` ↔ `/en/products/industrial-floor/neodur-he-3/` ↔ `/fr/produits/sols-industriels/neodur-he-3/`

### G) Verknuepfungen
→ Produktgruppe (Breadcrumb), Referenzprojekte (gefiltert), Verwandte Produkte, Systemkomponenten, Anwendungsseiten, Haendlerfinder, Download-Center, Planerbereich (Ausschreibungstexte, Normen), Kontakt

---

## 4. Anwendungsseite (z.B. "Industrieboden fuer Logistik")

### A) Zweck & Zielgruppe
Branchenspezifische Einstiegsseite, die Produkte nach Anwendungskontext praesentiert statt nach Produktgruppe. Beantwortet die Frage: "Welchen KORODUR-Boden brauche ich fuer meine Logistikhalle?" -- der fehlende Produktfinder-Einstieg.

**Primaere Zielgruppe:** Planer (Thomas -- sucht nach Anwendung), Verarbeiter (Markus -- braucht Empfehlung)

### B) Content-Elemente

1. **Hero-Bereich**
   - Branchenbild (z.B. Logistikhalle mit Staplerverkehr)
   - H1: "Industrieboeden fuer Logistik & Distribution"
   - Sub-Headline: "Hochbelastbare Hartstoffboeden fuer 24/7-Betrieb mit Schwerlastverkehr"
   - CTA: "Passende Produkte ansehen" | "Beratung anfragen"

2. **Anforderungsprofil**
   - Ueberschrift: "Typische Anforderungen in der Logistik"
   - Liste mit Icons: Abriebfestigkeit, Staplertauglichkeit, schnelle Nutzbarkeit, Chemikalienbestaendigkeit etc.

3. **Empfohlene Produkte**
   - 3-5 Produkte mit Bild + Kerndaten + "Warum dieses Produkt fuer Logistik?"
   - Sortiert nach Relevanz (bestes Produkt zuerst)
   - CTA pro Produkt: "Details ansehen" → Produktdetailseite

4. **Referenzprojekte in dieser Branche**
   - 3-4 Referenzen (Logistik) mit Bild + Name + Flaeche
   - CTA: "Alle Logistik-Referenzen"

5. **Systemaufbau-Diagramm** (optional)
   - Schichtaufbau-Grafik: Untergrund → Grundierung → Hartstoff → Nachbehandlung

6. **Download-Bereich**
   - Relevante TDS der empfohlenen Produkte
   - Branchenspezifische Anwendungsempfehlung (PDF)

7. **CTA-Leiste**
   - "Sie planen ein Logistikprojekt? Unsere Objektberatung hilft."
   - [Beratung anfragen] [Hotline]

### C) Wireframe-Beschreibung
```
┌─────────────────────────────────────────────────────────────┐
│                     Header / Navigation                      │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  HERO: Logistikhalle-Bild                                   │
│  H1: "Industrieboeden fuer Logistik & Distribution"         │
│  [Produkte ansehen] [Beratung anfragen]                     │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  ANFORDERUNGSPROFIL                                         │
│  ✓ Abriebfest  ✓ Staplertauglich  ✓ Schnelle Nutzung      │
│  ✓ Chemikalienbest.  ✓ Langlebig                           │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  EMPFOHLENE PRODUKTE                                        │
│  ┌──────────────────────────────────────────────┐           │
│  │ [Bild] NEODUR HE 65 Plus                     │           │
│  │ Verschleissklasse AR 0.5 | 5-8 mm            │           │
│  │ "Ideal fuer Schwerlastverkehr in 24/7-..."    │           │
│  │ [Details →]                                   │           │
│  └──────────────────────────────────────────────┘           │
│  ┌──────────────────────────────────────────────┐           │
│  │ [Bild] NEODUR HE 3                           │           │
│  │ ...                                           │           │
│  └──────────────────────────────────────────────┘           │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│  REFERENZEN (LOGISTIK)                                      │
│  ┌─────┐ ┌─────┐ ┌─────┐                                   │
│  │Ref1 │ │Ref2 │ │Ref3 │                                   │
│  └─────┘ └─────┘ └─────┘                                   │
│  [Alle Logistik-Referenzen →]                               │
├─────────────────────────────────────────────────────────────┤
│  SYSTEMAUFBAU-DIAGRAMM (Schichten-Grafik)                   │
├─────────────────────────────────────────────────────────────┤
│  DOWNLOADS: TDS HE 65 Plus | TDS HE 3 | Anwendungsempf.   │
├─────────────────────────────────────────────────────────────┤
│  CTA: "Logistikprojekt? Objektberatung."                   │
│  [Beratung anfragen] [Hotline]                              │
├─────────────────────────────────────────────────────────────┤
│                        Footer                                │
└─────────────────────────────────────────────────────────────┘
```

### D) Dynamische Elemente
- Empfohlene Produkte: ACF Relationship Field (manuell kuratiert pro Anwendung)
- Referenzprojekte: WP Query gefiltert nach Taxonomie "Branche" = Logistik
- Systemaufbau: ACF Image/SVG oder Elementor-Widget
- Downloads: Automatisch aus verknuepften Produkten gezogen

### E) SEO-Anforderungen
- **Title-Schema:** "Industrieboden fuer [Branche] -- KORODUR" z.B. "Industrieboden fuer Logistik -- KORODUR"
- **Meta-Description-Schema:** "KORODUR Industrieboeden fuer [Branche]: [Kerneigenschaften]. Produkte, Referenzen, Ausschreibungstexte. Beratung anfragen."
- **Schema.org:** WebPage + BreadcrumbList
- **H1:** "Industrieboeden fuer [Branche]" (1x)
- **Long-Tail-Keywords:** "Industrieboden Logistikhalle", "Hartstoff Staplerverkehr", "Bodenbeschichtung Lagerhalle"

### F) Besonderheiten fuer Mehrsprachigkeit
- Branchennamen uebersetzen: Logistik → Logistics → Logistique
- URL-Slugs: `/anwendungen/logistik/` → `/en/applications/logistics/` → `/fr/applications/logistique/`
- Anforderungsprofile und Texte pro Sprache pflegen

### G) Verknuepfungen
→ Produktdetailseiten (empfohlene Produkte), Referenzprojekte (gefiltert), Produktgruppen, Planerbereich, Download-Center, Kontakt

---

## 5. Planerbereich (Landingpage)

### A) Zweck & Zielgruppe
Dedizierter Einstieg fuer Planer & Architekten -- der aktuell komplett fehlende Bereich. Buendelt alles, was ein Planer braucht: Ausschreibungstexte, Normen, Downloads, Objektberatung. Orientierung an Mapei PRO und Knauf Planner Suite.

**Primaere Zielgruppe:** Persona A (Thomas Berger, technischer Planer) und Persona B (Dr. Lisa Novak, Architektin)

### B) Content-Elemente

1. **Hero-Bereich**
   - H1: "Fuer Planer & Architekten"
   - Sub-Headline: "Ausschreibungstexte, technische Daten und Objektberatung fuer Ihre Projekte"
   - Vertrauenselement: "Seit 1936 | ISO 9001 | DIN EN 13813 konform"
   - CTA: "Ausschreibungstexte finden" | "Objektberatung anfragen"

2. **Schnellzugriff-Kacheln (6 Stueck)**
   - Ausschreibungstexte (LV + GAEB) → `/planer/ausschreibungstexte/`
   - Normen & Zulassungen → `/planer/normen-zulassungen/`
   - Systemaufbauten → `/planer/systemaufbauten/`
   - Produktvergleiche → `/planer/produktvergleiche/`
   - Objektberatung → `/planer/objektberatung/`
   - Nachhaltigkeit / EPDs → `/planer/nachhaltigkeit/`

3. **Meistgesuchte Downloads**
   - Top-5-Downloads direkt auf der Landing Page (z.B. TDS NEODUR HE 3, Lieferprogramm, Ausschreibungstext Hartstoffeinstreuung)
   - CTA: "Zum Download-Center" → `/service/downloads/`

4. **Referenzprojekte fuer Planer**
   - 3-4 Vorzeigeprojekte (grosse Industrieobjekte, bekannte Betreiber)
   - CTA: "Alle Referenzen"

5. **Objektberatung-CTA (prominent)**
   - Foto eines Beraters + Name + Direktkontakt
   - "Wir unterstuetzen Sie bei der Planung und Ausschreibung."
   - Formular-Felder: Projekt, Flaeche, Anwendung, Terminwunsch
   - Telefon: Planerhotline

6. **Normen-Quicklinks**
   - DIN 18560, DIN EN 13813, DIN 18557, DWA-A 141 -- je mit Erklaerung und Produktverweis

### C) Wireframe-Beschreibung
```
┌─────────────────────────────────────────────────────────────┐
│                     Header / Navigation                      │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  HERO: "Fuer Planer & Architekten"                          │
│  "Ausschreibungstexte, technische Daten, Objektberatung"    │
│  Seit 1936 | ISO 9001 | DIN EN 13813                        │
│  [Ausschreibungstexte] [Objektberatung]                     │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  SCHNELLZUGRIFF (6 Kacheln)                                 │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐                    │
│  │Ausschr.- │ │Normen &  │ │System-   │                    │
│  │texte     │ │Zulassung.│ │aufbauten │                    │
│  └──────────┘ └──────────┘ └──────────┘                    │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐                    │
│  │Produkt-  │ │Objekt-   │ │Nachhaltig│                    │
│  │vergleiche│ │beratung  │ │keit/EPDs │                    │
│  └──────────┘ └──────────┘ └──────────┘                    │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│  MEISTGESUCHTE DOWNLOADS                                    │
│  📄 TDS NEODUR HE 3    📄 LV Hartstoffeinstreuung (GAEB)  │
│  📄 TDS GRANIDUR        📄 Lieferprogramm                  │
│  [→ Zum Download-Center]                                    │
├─────────────────────────────────────────────────────────────┤
│  REFERENZEN (3-4 Vorzeigeprojekte)                          │
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌─────┐                          │
│  └─────┘ └─────┘ └─────┘ └─────┘                          │
│  [Alle Referenzen →]                                        │
├─────────────────────────────────────────────────────────────┤
│  OBJEKTBERATUNG                                             │
│  [Foto Berater]  "Wir unterstuetzen Sie."                   │
│  Planerhotline: +49 9621 4759-XX                            │
│  [Formular: Projekt / Flaeche / Anwendung / Termin]        │
│  [Anfrage absenden]                                         │
├─────────────────────────────────────────────────────────────┤
│  NORMEN-QUICKLINKS                                          │
│  DIN 18560 | DIN EN 13813 | DIN 18557 | DWA-A 141          │
├─────────────────────────────────────────────────────────────┤
│                        Footer                                │
└─────────────────────────────────────────────────────────────┘
```

### D) Dynamische Elemente
- Meistgesuchte Downloads: Manuell kuratiert (ACF Repeater) oder per Download-Tracking automatisch
- Referenzen: WP Query (Top-Referenzen, manuell kuratiert)
- Objektberatungs-Formular: Contact Form 7 oder Gravity Forms (Submission → E-Mail an Objektberatung)

### E) SEO-Anforderungen
- **Title:** "Fuer Planer & Architekten -- Ausschreibungstexte, Normen, Beratung | KORODUR"
- **Meta-Description:** "KORODUR Planerbereich: Ausschreibungstexte (GAEB), technische Datenblaetter, Normenkonformitaet, Objektberatung. Fuer Ihre Industrieboden-Projekte."
- **Schema.org:** WebPage + BreadcrumbList
- **Keywords:** "Ausschreibungstext Industrieboden", "GAEB Hartstoff", "DIN 18560 Hartstoffestrich"

### F) Besonderheiten fuer Mehrsprachigkeit
- `/planer/` → `/en/specifiers/` → `/fr/prescripteurs/`
- Normenbezeichnungen bleiben identisch (DIN/EN-Normen sind international)
- Ausschreibungstexte: GAEB nur fuer DE relevant, EN/FR erhalten PDF-Texte

### G) Verknuepfungen
→ Ausschreibungstexte, Normen-Seite, Systemaufbauten, Produktvergleiche, Objektberatung, Download-Center, Referenzen, Produktdetailseiten, Kontakt

---

## 6. Download-Center

### A) Zweck & Zielgruppe
Zentraler, filterbarer Ort fuer alle Dokumente. Loest das aktuell gravierende Problem: TDS, SDS, DoP, LV sind auf verschiedene Service-Unterseiten verteilt und nicht pro Produkt gebuendelt. Vorbild: Rockwool, Schoeck.

**Primaere Zielgruppe:** Alle (Planer: TDS + LV + DoP; Verarbeiter: TDS + SDS; Handel: Lieferprogramm + TDS)

### B) Content-Elemente

1. **Seitenheader**
   - H1: "Download-Center"
   - Intro-Text: "Alle technischen Dokumente an einem Ort -- ohne Login."
   - Suchfeld (Volltextsuche ueber Dokumentnamen)

2. **Filterleiste (prominent)**
   - **Dokumenttyp:** TDS | SDS | DoP | Ausschreibungstexte (LV) | EPD | Anwendungsempfehlungen | Farbkarten | Lieferprogramm
   - **Produktgruppe:** Industrieboden | Sichtestrich | Microtop | Rapid Set | ...
   - **Einzelprodukt:** Dropdown oder Autocomplete
   - **Sprache:** DE | EN | FR
   - Aktive Filter als Chips anzeigen, "Alle Filter zuruecksetzen"

3. **Ergebnisliste**
   - Tabelle oder Karten-Ansicht
   - Pro Dokument: Dokumenttyp-Icon | Dokumentname | Produkt | Sprache | Dateigroesse | Download-Button
   - Sortierung: nach Name, Typ, Produkt, Datum
   - "Alle ausgewaehlten herunterladen" (ZIP) -- optional

4. **Ohne Login!** (klar kommuniziert)
   - Hinweis: "Alle technischen Dokumente sind frei verfuegbar."

5. **CTA unten**
   - "Dokument nicht gefunden? Kontaktieren Sie uns."
   - [Kontakt] [Hotline]

### C) Wireframe-Beschreibung
```
┌─────────────────────────────────────────────────────────────┐
│                     Header / Navigation                      │
├─────────────────────────────────────────────────────────────┤
│  Breadcrumb: Home > Service > Download-Center               │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  H1: Download-Center                                        │
│  "Alle technischen Dokumente -- ohne Login."                │
│                                                              │
│  [Suchfeld: Dokumentname oder Produktname eingeben]         │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│  FILTER:                                                     │
│  Dokumenttyp: [TDS] [SDS] [DoP] [LV] [EPD] [Sonst.]       │
│  Produktgruppe: [Dropdown]                                   │
│  Produkt: [Autocomplete]                                     │
│  Sprache: [DE] [EN] [FR]                                    │
│                                                              │
│  Aktive Filter: [TDS ×] [Industrieboden ×]  [Zuruecksetzen]│
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  ERGEBNISSE (42 Dokumente)                                  │
│  ┌────────────────────────────────────────────────────────┐ │
│  │ 📄 TDS | NEODUR HE 3 | DE | 1.2 MB | [Download ↓]   │ │
│  │ 📄 TDS | NEODUR HE 3 | EN | 1.1 MB | [Download ↓]   │ │
│  │ 📄 SDS | NEODUR HE 3 | DE | 0.4 MB | [Download ↓]   │ │
│  │ 📄 LV  | Hartstoffeinstr. | DE | 0.1 MB | [Download] │ │
│  │ ...                                                    │ │
│  └────────────────────────────────────────────────────────┘ │
│                                                              │
│  [Seite 1] [2] [3] ... [→]                                 │
├─────────────────────────────────────────────────────────────┤
│  CTA: "Dokument nicht gefunden? → Kontakt"                  │
├─────────────────────────────────────────────────────────────┤
│                        Footer                                │
└─────────────────────────────────────────────────────────────┘
```

### D) Dynamische Elemente
- Dokumente: Custom Post Type "Download" mit Taxonomies (Dokumenttyp, Produktgruppe, Sprache) + ACF File Field
- Filter: Ajax-basiert, ohne Seiten-Neuladen (FacetWP-Plugin oder Custom Ajax)
- Suche: durchsucht Dokumentname + verknuepftes Produkt
- Alternativ: Download-Daten aus Notion-DB per API synchronisiert (Produktdatenbank-Projekt)
- URL-Parameter fuer Deep-Links: `/service/downloads/?typ=tds&gruppe=industrieboden`

### E) SEO-Anforderungen
- **Title:** "Download-Center -- Technische Datenblaetter, SDS, DoP | KORODUR"
- **Meta-Description:** "KORODUR Download-Center: TDS, Sicherheitsdatenblaetter, Leistungserklaerungen, Ausschreibungstexte. Alle Dokumente frei verfuegbar, ohne Login."
- **Schema.org:** CollectionPage + BreadcrumbList
- **Filterbare URLs:** `/service/downloads/?typ=sds` fuer Deeplinks (aber Canonical auf Hauptseite)

### F) Besonderheiten fuer Mehrsprachigkeit
- Filter-Labels uebersetzen (Dokumenttyp → Document type → Type de document)
- Sprach-Filter ermoeglicht gezielten Zugriff auf EN- oder FR-Dokumente
- URL: `/service/downloads/` → `/en/service/downloads/` → `/fr/service/telechargements/`

### G) Verknuepfungen
→ Produktdetailseiten (rueckwaerts: Produkt hat Download-Buttons), Planerbereich, Kontakt

---

## 7. Referenzprojekt-Uebersicht

### A) Zweck & Zielgruppe
Zeigt alle ~130 Referenzprojekte filterbar. Beweist Kompetenz und Erfahrung. Planer nutzen Referenzen zur Produkt-Evaluation ("Wer hat das schon verbaut?"), Verarbeiter zur Argumentation gegenueber Auftraggebern, Handel als Verkaufsargument.

**Primaere Zielgruppe:** Planer (Thomas -- prueft Eignung), Verarbeiter (Stefan -- Nachweis), Handel (Jens -- Verkaufsargument)

### B) Content-Elemente

1. **Seitenheader**
   - H1: "Referenzprojekte"
   - Intro: "Ueber 750 Millionen Quadratmeter weltweit verlegt. Hier eine Auswahl unserer Projekte."

2. **Filterleiste**
   - **Branche:** Logistik | Automotive | Lebensmittel | Handel | Oeffentlich | Trinkwasser | Wohnen
   - **Produktgruppe:** Industrieboden | Sichtestrich | Microtop | Rapid Set | ...
   - **Region:** Deutschland | Europa | International
   - **Produkt:** Einzelprodukt-Filter (NEU -- ermoeglicht Produkt-Referenz-Verknuepfung)

3. **Ergebnis-Grid**
   - Kacheln: Grosses Bild + Projektname + Branche + Standort + Baujahr
   - Hover: Kurzbeschreibung einblenden
   - Responsive: 3 Spalten Desktop, 2 Tablet, 1 Mobile

4. **Kartenansicht** (optional, Phase 2)
   - Weltkarte mit Pins, klickbar

5. **CTA unten**
   - "Ihr Projekt koennte das naechste sein."
   - [Beratung anfragen] [Objektberatung]

### C) Wireframe-Beschreibung
```
┌─────────────────────────────────────────────────────────────┐
│                     Header / Navigation                      │
├─────────────────────────────────────────────────────────────┤
│  Breadcrumb: Home > Referenzen                              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  H1: Referenzprojekte                                       │
│  "750 Mio. m2 verlegt. Eine Auswahl unserer Projekte."     │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│  FILTER:                                                     │
│  Branche: [Alle] [Logistik] [Automotive] [Lebensmittel] ...│
│  Produktgruppe: [Alle] [Industrieboden] [Sichtestrich] ... │
│  Region: [Alle] [Deutschland] [Europa] [International]     │
│  Produkt: [Autocomplete]                                     │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  ERGEBNISSE (87 Projekte)                                   │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐                       │
│  │ [Bild]  │ │ [Bild]  │ │ [Bild]  │                       │
│  │ Amazon  │ │ BMW     │ │ Edeka   │                       │
│  │ Leipzig │ │ Muenchen│ │ Minden  │                       │
│  │ Logistik│ │ Autom.  │ │ Handel  │                       │
│  │ 2024    │ │ 2023    │ │ 2022    │                       │
│  └─────────┘ └─────────┘ └─────────┘                       │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐                       │
│  │ ...     │ │ ...     │ │ ...     │                       │
│  └─────────┘ └─────────┘ └─────────┘                       │
│                                                              │
│  [Mehr laden] oder Pagination                                │
├─────────────────────────────────────────────────────────────┤
│  CTA: "Ihr Projekt koennte das naechste sein."              │
│  [Beratung anfragen] [Objektberatung]                       │
├─────────────────────────────────────────────────────────────┤
│                        Footer                                │
└─────────────────────────────────────────────────────────────┘
```

### D) Dynamische Elemente
- Referenzen: Custom Post Type "Referenz" mit Taxonomies (Branche, Region) + ACF Relationship (Produkt)
- Filter: Ajax-basiert (FacetWP oder Custom)
- "Mehr laden": Infinite Scroll oder Load-More-Button (nicht klassische Pagination)
- Referenz-Daten aus Notion-DB synchronisiert (KORODUR-Referenzen-Projekt, DB-ID: 2e7670e1...)

### E) SEO-Anforderungen
- **Title:** "Referenzprojekte -- Industrieboeden weltweit | KORODUR"
- **Meta-Description:** "KORODUR Referenzprojekte: Ueber 130 Industrieboden-Projekte weltweit. Logistik, Automotive, Lebensmittel. Bilder, Details, verwendete Produkte."
- **Schema.org:** CollectionPage + BreadcrumbList
- **Interne Verlinkung:** Jede Referenz-Kachel → Referenz-Detail, Filter-URLs fuer Branche

### F) Besonderheiten fuer Mehrsprachigkeit
- Filter-Labels uebersetzen
- Referenz-Titel und -Beschreibungen pro Sprache
- Branchennamen uebersetzen (Logistik → Logistics → Logistique)
- Format Referenz-Titel: "Betreiber, Ort (Baujahr)" -- Ortsnamen bleiben in Originalsprache

### G) Verknuepfungen
→ Referenz-Detailseiten, Produktdetailseiten (ueber Produkt-Filter), Anwendungsseiten, Kontakt

---

## 8. Referenzprojekt-Detail

### A) Zweck & Zielgruppe
Einzelnes Referenzprojekt ausfuehrlich darstellen. Verbindet Projekt mit verwendeten Produkten -- die aktuell fehlende Verknuepfung. Ueberzeugt Planer und Verarbeiter durch Praxisnachweis.

**Primaere Zielgruppe:** Planer (Thomas -- "Wer nutzt das schon?"), Verarbeiter (Stefan -- "Kann ich meinem Auftraggeber zeigen")

### B) Content-Elemente

1. **Breadcrumb**
   - Home > Referenzen > [Projektname]

2. **Projekt-Header**
   - Grosses Headerbild (volle Breite)
   - H1: Projektname (Format: "Betreiber, Ort (Baujahr)")
   - Meta-Infos: Branche | Standort | Baujahr | Flaeche (m2)

3. **Bildergalerie**
   - 4-8 Bilder: Baustelle, Verarbeitung, Endergebnis
   - Lightbox-Funktion

4. **Projektbeschreibung**
   - Aufgabenstellung, Anforderungen, Loesung, Ergebnis
   - 3-5 Absaetze

5. **Projektsteckbrief (Sidebar oder Box)**
   - Betreiber/Bauherr
   - Standort (Stadt, Land)
   - Baujahr
   - Flaeche (m2)
   - Verwendete Produkte (verlinkt!)
   - Verarbeiter (optional)
   - Architekt/Planer (optional)

6. **Verwendete Produkte** (NEU -- zentrale Verknuepfung!)
   - Pro Produkt: Bild + Name + Kurzbeschreibung + Link zur Produktdetailseite
   - "Dieses Produkt anzeigen" → Produktdetailseite

7. **Weitere Referenzen in dieser Branche**
   - 3 aehnliche Projekte als Kacheln

8. **CTA-Leiste**
   - "Aehnliches Projekt geplant?"
   - [Beratung anfragen] [Produktinfo anfordern]

### C) Wireframe-Beschreibung
```
┌─────────────────────────────────────────────────────────────┐
│                     Header / Navigation                      │
├─────────────────────────────────────────────────────────────┤
│  Breadcrumb: Home > Referenzen > Amazon Leipzig             │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  [GROSSES HEADERBILD -- volle Breite]                       │
│                                                              │
├──────────────────────────┬──────────────────────────────────┤
│                          │  PROJEKTSTECKBRIEF               │
│  H1: Amazon, Leipzig    │                                   │
│  (2024)                  │  Betreiber: Amazon               │
│                          │  Standort: Leipzig               │
│  [BILDERGALERIE]         │  Baujahr: 2024                   │
│  [Bild1] [Bild2] [Bild3]│  Flaeche: 42.000 m2             │
│                          │  Produkte:                       │
│  PROJEKTBESCHREIBUNG     │  → NEODUR HE 65 Plus            │
│  Aufgabe: ...            │  → KORODUR Primer Plus           │
│  Anforderungen: ...      │                                   │
│  Loesung: ...            │  Verarbeiter: Estrich GmbH       │
│  Ergebnis: ...           │                                   │
│                          │  [Produkte anzeigen]             │
│                          │  [Beratung anfragen]             │
├──────────────────────────┴──────────────────────────────────┤
│  VERWENDETE PRODUKTE                                        │
│  ┌─────────────────┐ ┌─────────────────┐                    │
│  │[Bild] NEODUR    │ │[Bild] KORODUR   │                    │
│  │HE 65 Plus       │ │Primer Plus      │                    │
│  │"Hartstoff fuer  │ │"Grundierung..." │                    │
│  │ Schwerlast..."  │ │                 │                    │
│  │[Details →]      │ │[Details →]      │                    │
│  └─────────────────┘ └─────────────────┘                    │
├─────────────────────────────────────────────────────────────┤
│  WEITERE REFERENZEN (LOGISTIK)                              │
│  ┌─────┐ ┌─────┐ ┌─────┐                                   │
│  │Ref2 │ │Ref3 │ │Ref4 │                                   │
│  └─────┘ └─────┘ └─────┘                                   │
├─────────────────────────────────────────────────────────────┤
│  CTA: "Aehnliches Projekt? Wir beraten Sie."               │
│  [Beratung] [Produktinfo]                                   │
├─────────────────────────────────────────────────────────────┤
│                        Footer                                │
└─────────────────────────────────────────────────────────────┘
```

### D) Dynamische Elemente
- Referenzdaten: Custom Post Type "Referenz" mit ACF-Feldern (Betreiber, Standort, Baujahr, Flaeche, Beschreibung)
- Produkt-Verknuepfung: ACF Relationship (Referenz → Produkt, bidirektional)
- Bildergalerie: ACF Gallery Field
- Weitere Referenzen: WP Query (gleiche Branche, ohne aktuelles Projekt)
- Daten-Sync aus Notion-DB (KORODUR-Referenzen-Projekt)

### E) SEO-Anforderungen
- **Title-Schema:** "[Betreiber], [Ort] -- Referenzprojekt | KORODUR" z.B. "Amazon, Leipzig -- Referenzprojekt | KORODUR"
- **Meta-Description-Schema:** "KORODUR Referenzprojekt: [Betreiber], [Ort]. [Flaeche] m2 [Branche]. Verwendete Produkte: [Produkt1], [Produkt2]. Seit 1936."
- **Schema.org:** Article + BreadcrumbList (oder CreativeWork)
- **Alt-Tags:** "[Betreiber] [Ort] -- KORODUR Industrieboden"

### F) Besonderheiten fuer Mehrsprachigkeit
- Projektbeschreibung pro Sprache
- Steckbrief-Labels uebersetzen (Betreiber → Client → Client)
- Ortsnamen: Originalsprache beibehalten
- Produktnamen: identisch in allen Sprachen

### G) Verknuepfungen
→ Produktdetailseiten (verwendete Produkte), Referenz-Uebersicht, Anwendungsseiten (gleiche Branche), Kontakt

---

## 9. Haendlerfinder

### A) Zweck & Zielgruppe
Komplett neue Seite (aktuell nicht vorhanden!). Ermoeglicht Endkunden und Verarbeitern, KORODUR-Produkte bei einem Haendler in ihrer Naehe zu kaufen. Fuer Haendler selbst: Sichtbarkeit und Kundenzufuehrung. Vorbild: Raab Karcher Standortsuche.

**Primaere Zielgruppe:** Persona E (Andrea -- will sichtbar sein), Persona F (Jens -- zeigt Kunden), Verarbeiter (Markus -- "Wo kann ich bestellen?")

### B) Content-Elemente

1. **Seitenheader**
   - H1: "Haendler & Bezugsquellen finden"
   - Intro: "KORODUR-Produkte erhalten Sie ueber den qualifizierten Baustoff-Fachhandel."

2. **Suchleiste (prominent)**
   - Eingabefeld: PLZ, Ort oder "Meinen Standort verwenden" (Geolocation)
   - Umkreis-Slider: 25 km / 50 km / 100 km / 200 km
   - Optional: Produkt-Filter ("Wer fuehrt NEODUR HE 3?")

3. **Karte + Liste**
   - Linke Seite (Desktop): Interaktive Karte (Google Maps oder OpenStreetMap/Leaflet)
   - Rechte Seite: Haendlerliste mit:
     - Firmenname
     - Adresse
     - Telefon + E-Mail
     - Entfernung
     - "Route planen" (Google Maps Link)
     - Optional: "Dieser Haendler fuehrt: [Produkte]"
   - Mobile: Karte oben, Liste unten (oder Toggle)

4. **Kontakt-CTA**
   - "Kein Haendler in Ihrer Naehe? Bestellen Sie direkt bei uns."
   - [Anfrage stellen] [Hotline]

5. **Haendler werden**
   - "Sie sind Baustoff-Fachhaendler und moechten KORODUR ins Sortiment aufnehmen?"
   - [Kontakt Vertrieb]

### C) Wireframe-Beschreibung
```
┌─────────────────────────────────────────────────────────────┐
│                     Header / Navigation                      │
├─────────────────────────────────────────────────────────────┤
│  Breadcrumb: Home > Service > Haendlerfinder                │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  H1: Haendler & Bezugsquellen finden                        │
│  "KORODUR-Produkte ueber den Baustoff-Fachhandel."         │
│                                                              │
│  SUCHE: [PLZ oder Ort eingeben] [📍 Standort] [Suchen]    │
│  Umkreis: [25km] [50km] [100km] [200km]                    │
│                                                              │
├──────────────────────────┬──────────────────────────────────┤
│                          │                                   │
│  ┌────────────────────┐  │  HAENDLERLISTE                   │
│  │                    │  │                                   │
│  │   INTERAKTIVE      │  │  1. Baustoff Mueller GmbH        │
│  │   KARTE            │  │     97070 Wuerzburg              │
│  │                    │  │     Tel: 0931 ...                 │
│  │   [Pins]           │  │     12 km entfernt               │
│  │                    │  │     [Route] [Anrufen]             │
│  │                    │  │                                   │
│  │                    │  │  2. Raab Karcher Nuernberg        │
│  │                    │  │     90441 Nuernberg               │
│  │                    │  │     Tel: 0911 ...                 │
│  │                    │  │     45 km entfernt               │
│  │                    │  │     [Route] [Anrufen]             │
│  │                    │  │                                   │
│  └────────────────────┘  │  3. ...                           │
│                          │                                   │
├──────────────────────────┴──────────────────────────────────┤
│  CTA: "Kein Haendler? Direkt anfragen."                     │
│  [Anfrage] [Hotline]                                        │
├─────────────────────────────────────────────────────────────┤
│  "Haendler werden? → Kontakt Vertrieb"                      │
├─────────────────────────────────────────────────────────────┤
│                        Footer                                │
└─────────────────────────────────────────────────────────────┘
```

### D) Dynamische Elemente
- Haendlerdaten: Custom Post Type "Haendler" mit ACF-Feldern (Adresse, Geokoordinaten, Telefon, E-Mail, Sortiment)
- Karte: Google Maps API oder Leaflet.js + OpenStreetMap (kostenlos)
- PLZ-Suche: Geocoding API (PLZ → Koordinaten → Umkreissuche)
- "Wo kaufen?" auf Produktseiten: Link zum Haendlerfinder mit Produkt-Parameter
- Datenpflege: Manuell ueber WP-Backend oder per CSV-Import

### E) SEO-Anforderungen
- **Title:** "Haendlerfinder -- KORODUR Bezugsquellen in Ihrer Naehe"
- **Meta-Description:** "Finden Sie einen KORODUR-Fachhaendler in Ihrer Naehe. PLZ-Suche, Karte, Kontaktdaten. Industrieboeden, Hartstoffe, Sichtestrich."
- **Schema.org:** WebPage + BreadcrumbList (Haendler-Eintraege: LocalBusiness)
- **Kein Index fuer Suchergebnis-URLs** (nur Hauptseite indexieren)

### F) Besonderheiten fuer Mehrsprachigkeit
- `/service/haendlerfinder/` → `/en/service/dealer-locator/` → `/fr/service/trouver-un-distributeur/`
- Haendlerdaten: Adressen in Originalsprache, Labels uebersetzen
- Fuer EN/FR-Version: ggf. internationale Distributoren anzeigen

### G) Verknuepfungen
→ Produktdetailseiten ("Wo kaufen?"-CTA), Kontakt (Direktanfrage), Homepage (Haendler-Einstieg)

---

## 10. Unternehmensseite

### A) Zweck & Zielgruppe
Stellt KORODUR als Unternehmen vor. Schafft Vertrauen durch Geschichte, Kompetenz und Qualitaetsnachweise. Dient als Verteiler zu Unterseiten (Geschichte, Standorte, Nachhaltigkeit, Qualitaet, Karriere, News).

**Primaere Zielgruppe:** Alle (Erstbesucher -- "Wer ist KORODUR?"), Planer (ISO-Zertifikate pruefen), potenzielle Mitarbeiter (Karriere)

### B) Content-Elemente

1. **Hero-Bereich**
   - Bild: Firmenzentrale Amberg oder Produktionshalle
   - H1: "KORODUR International GmbH"
   - Sub-Headline: "Mineralische Hartstoffe & Industrieboeden -- seit 1936"

2. **Kurzprofil**
   - 3-4 Absaetze: Wer ist KORODUR? Was machen wir? Wo sind wir aktiv?
   - Fact-Box: Gruendungsjahr | Mitarbeiter | Standorte | Laender

3. **Bereichs-Kacheln (5-6 Stueck)**
   - Geschichte (seit 1936) → `/unternehmen/geschichte/`
   - Standorte & Produktion → `/unternehmen/standorte/`
   - Nachhaltigkeit → `/unternehmen/nachhaltigkeit/`
   - Qualitaet & Zertifikate → `/unternehmen/qualitaet/`
   - News & Presse → `/unternehmen/news/`
   - Karriere → `/unternehmen/karriere/`

4. **Zertifikate-Leiste**
   - ISO 9001 Badge | TUeV Sued | Weitere Zertifikate als Logos

5. **Referenz-Teaser**
   - "Ueber 750 Mio. m2 weltweit verlegt"
   - 2-3 Highlight-Referenzen
   - [Alle Referenzen →]

6. **CTA-Leiste**
   - "Lernen Sie uns kennen -- persoenlich."
   - [Kontakt aufnehmen] [Standorte ansehen]

### C) Wireframe-Beschreibung
```
┌─────────────────────────────────────────────────────────────┐
│                     Header / Navigation                      │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  HERO: Firmenzentrale Amberg                                │
│  H1: "KORODUR International GmbH"                           │
│  "Mineralische Hartstoffe seit 1936"                        │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  KURZPROFIL (3-4 Absaetze)                                  │
│  Fact-Box: 1936 | XX MA | 4 Standorte | XX Laender          │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  BEREICHE (5-6 Kacheln)                                     │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐                    │
│  │Geschichte│ │Standorte │ │Nachhaltig│                    │
│  └──────────┘ └──────────┘ └──────────┘                    │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐                    │
│  │Qualitaet │ │News      │ │Karriere  │                    │
│  └──────────┘ └──────────┘ └──────────┘                    │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│  ZERTIFIKATE: [ISO 9001] [TUeV] [...]                       │
├─────────────────────────────────────────────────────────────┤
│  REFERENZ-HIGHLIGHTS (2-3 Projekte)                         │
│  [Alle Referenzen →]                                        │
├─────────────────────────────────────────────────────────────┤
│  CTA: "Lernen Sie uns kennen."                              │
│  [Kontakt] [Standorte]                                      │
├─────────────────────────────────────────────────────────────┤
│                        Footer                                │
└─────────────────────────────────────────────────────────────┘
```

### D) Dynamische Elemente
- Bereichs-Kacheln: Statisch (selten geaendert)
- Referenz-Highlights: WP Query (manuell kuratiert oder neueste)
- News-Teaser: WP Query (neueste 2-3 Posts)
- Zertifikate: ACF Gallery oder manuell

### E) SEO-Anforderungen
- **Title:** "Ueber KORODUR -- Mineralische Industrieboeden seit 1936"
- **Meta-Description:** "KORODUR International GmbH: Spezialist fuer mineralische Hartstoffe und Industrieboeden seit 1936. 4 Standorte, ISO 9001 zertifiziert, international taetig."
- **Schema.org:** Organization (name, founding, address, logo, sameAs) + BreadcrumbList
- **H1:** "KORODUR International GmbH" (1x)

### F) Besonderheiten fuer Mehrsprachigkeit
- `/unternehmen/` → `/en/company/` → `/fr/entreprise/`
- Unterseiten-Slugs uebersetzen (Geschichte → History → Histoire)
- Inhalte vollstaendig pro Sprache pflegen

### G) Verknuepfungen
→ Geschichte, Standorte, Nachhaltigkeit, Qualitaet, Karriere, News, Referenzen, Kontakt

---

## 11. Kontaktseite

### A) Zweck & Zielgruppe
Zentrale Kontaktseite mit Formular, Ansprechpartnern und Standorten. Muss die aktuellen Defizite beheben: Keine zielgruppenspezifischen Kontaktwege, Telefonnummer nur im Footer, kein Objektberatungs-Formular.

**Primaere Zielgruppe:** Alle (jeder, der Kontakt aufnehmen will -- Planer fuer Objektberatung, Verarbeiter fuer technische Hilfe, Handel fuer Konditionen)

### B) Content-Elemente

1. **Seitenheader**
   - H1: "Kontakt"
   - Intro: "Wir sind fuer Sie da -- per Telefon, E-Mail oder Formular."
   - Prominente Telefonnummer: "+49 9621 4759-0" (gross, klickbar)
   - E-Mail: info@korodur.de

2. **Zielgruppen-Kontaktwege (3 Spalten)**
   - **Planer & Architekten:** Objektberatung, Planerhotline, Ausschreibungs-Support → Ansprechpartner + Formular
   - **Verarbeiter & Bauunternehmen:** Technische Hotline, Verarbeitungsberatung → Ansprechpartner + Formular
   - **Handel & Distributoren:** Vertrieb, Konditionen, Listung → Ansprechpartner + Formular

3. **Kontaktformular**
   - Felder: Anrede, Name, Unternehmen, E-Mail, Telefon, **Betreff-Dropdown** (Objektberatung / Technische Frage / Haendleranfrage / Allgemein / Karriere), Nachricht, Datenschutz-Checkbox
   - Routet automatisch an richtigen Ansprechpartner basierend auf Betreff
   - Pflichtfelder: Name, E-Mail, Betreff, Nachricht, Datenschutz

4. **Ansprechpartner**
   - Link/Tab: "Deutschland" | "International"
   - Pro Ansprechpartner: Foto + Name + Rolle + Telefon + E-Mail + Region (bei International)

5. **Standorte** (Karte + Adressen)
   - 4 Standorte: Amberg (Zentrale), Bochum-Wattenscheid, Freihung, Hannover-Misburg
   - Google Maps Embed oder Leaflet
   - Pro Standort: Adresse, Telefon, "Route planen"

### C) Wireframe-Beschreibung
```
┌─────────────────────────────────────────────────────────────┐
│                     Header / Navigation                      │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  H1: Kontakt                                                │
│  "Wir sind fuer Sie da."                                    │
│  TEL: +49 9621 4759-0  |  info@korodur.de                  │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐        │
│  │ FUR PLANER   │ │FUR VERARBEIT.│ │ FUR HANDEL   │        │
│  │ Objektberat. │ │ Techn. Hotl. │ │ Vertrieb     │        │
│  │ Hr. [Name]   │ │ Hr. [Name]   │ │ Fr. [Name]   │        │
│  │ +49 9621 ... │ │ +49 9621 ... │ │ +49 9621 ... │        │
│  │ [E-Mail]     │ │ [E-Mail]     │ │ [E-Mail]     │        │
│  └──────────────┘ └──────────────┘ └──────────────┘        │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  KONTAKTFORMULAR                                            │
│  Anrede: [Herr/Frau]  Name: [________]                      │
│  Unternehmen: [________]  E-Mail: [________]                │
│  Telefon: [________]                                         │
│  Betreff: [Objektberatung ▾]                                │
│  Nachricht: [________________________]                       │
│  □ Datenschutz gelesen und akzeptiert                        │
│  [Nachricht senden]                                          │
│                                                              │
├─────────────────────────────────────────────────────────────┤
│  ANSPRECHPARTNER: [Deutschland] [International]              │
│  ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐                       │
│  │[Foto]│ │[Foto]│ │[Foto]│ │[Foto]│                       │
│  │Name  │ │Name  │ │Name  │ │Name  │                       │
│  │Rolle │ │Rolle │ │Rolle │ │Rolle │                       │
│  │Tel   │ │Tel   │ │Tel   │ │Tel   │                       │
│  └──────┘ └──────┘ └──────┘ └──────┘                       │
├─────────────────────────────────────────────────────────────┤
│  STANDORTE                                                   │
│  [Karte mit 4 Pins]                                         │
│  Amberg (Zentrale) | Bochum | Freihung | Hannover           │
├─────────────────────────────────────────────────────────────┤
│                        Footer                                │
└─────────────────────────────────────────────────────────────┘
```

### D) Dynamische Elemente
- Kontaktformular: Contact Form 7 oder Gravity Forms mit bedingtem Routing (Betreff → E-Mail-Empfaenger)
- Ansprechpartner: ACF Repeater auf der Kontaktseite oder eigener Custom Post Type "Ansprechpartner"
- Karte: Google Maps Embed (4 Standorte) oder Leaflet
- Formular-Submission: E-Mail + optional CRM-Anbindung (Salesforce, wenn vorhanden)

### E) SEO-Anforderungen
- **Title:** "Kontakt -- KORODUR International GmbH"
- **Meta-Description:** "Kontaktieren Sie KORODUR: Telefon +49 9621 4759-0, Kontaktformular, Ansprechpartner Deutschland und International. Objektberatung, technischer Support, Haendleranfragen."
- **Schema.org:** ContactPage + Organization (contactPoint: telephone, email, contactType) + BreadcrumbList
- **H1:** "Kontakt" (1x)

### F) Besonderheiten fuer Mehrsprachigkeit
- `/kontakt/` → `/en/contact/` → `/fr/contact/`
- Formular-Labels und Betreff-Optionen uebersetzen
- Ansprechpartner "International" in EN/FR staerker hervorheben
- Datenschutz-Checkbox: Link zur jeweiligen Sprachversion der Datenschutzerklaerung

### G) Verknuepfungen
→ Ansprechpartner Deutschland, Ansprechpartner International, Standorte, Datenschutzerklaerung, Planerbereich (Objektberatung)

---

## 12. Blog/News-Beitrag

### A) Zweck & Zielgruppe
Einzelner News-/Blog-Beitrag. Aktuell quasi tot (3 Beitraege, letzter Nov 2024). Muss reaktiviert werden mit mindestens monatlichem Content: neue Projekte, Produktneuheiten, Messen, Branchennews. Optional auch Fachbeitraege (Fachwissen-Blog).

**Primaere Zielgruppe:** Alle (Planer: Normen-Updates, neue Produkte; Verarbeiter: Praxistipps, Projekte; Handel: Neuheiten, Aktionen)

### B) Content-Elemente

1. **Artikel-Header**
   - Breadcrumb: Home > Unternehmen > News > [Titel]
   - H1: Artikeltitel
   - Meta: Datum | Autor | Kategorie (Tags)
   - Hero-Bild (volle Breite oder 2/3)

2. **Artikelinhalt**
   - Fliesstext mit Zwischenueberschriften (H2, H3)
   - Bilder/Galerie inline
   - YouTube-Embeds (wenn relevant)
   - Zitate/Highlights als Pull-Quotes

3. **Sidebar (Desktop) oder nach Artikel (Mobile)**
   - Kategorien: Produktneuheiten | Referenzprojekte | Messen & Events | Nachhaltigkeit | Praxistipps
   - "Aktuelle News" (5 neueste)
   - Newsletter-Anmeldung (Sidebar-Widget)
   - CTA: "Beratung anfragen"

4. **Verwandte Produkte** (wenn im Artikel referenziert)
   - 2-3 Produktkacheln

5. **Verwandte Referenzen** (wenn im Artikel referenziert)
   - 1-2 Referenzkacheln

6. **Social-Sharing-Buttons**
   - LinkedIn (B2B-primaer), E-Mail, Link kopieren

7. **Naechster/Vorheriger Beitrag**
   - Navigation zwischen Beitraegen

8. **CTA-Leiste**
   - "Bleiben Sie informiert."
   - [Newsletter abonnieren] [Alle News ansehen]

### C) Wireframe-Beschreibung
```
┌─────────────────────────────────────────────────────────────┐
│                     Header / Navigation                      │
├─────────────────────────────────────────────────────────────┤
│  Breadcrumb: Home > Unternehmen > News > Artikeltitel       │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  [HERO-BILD]                                                │
│                                                              │
│  H1: Artikeltitel                                           │
│  24.03.2026 | Redaktion | Produktneuheit                    │
│                                                              │
├──────────────────────────┬──────────────────────────────────┤
│                          │  SIDEBAR                          │
│  ARTIKELINHALT           │                                   │
│                          │  KATEGORIEN                       │
│  Text...                 │  Produktneuheiten                │
│                          │  Referenzprojekte                │
│  [Bild]                  │  Messen & Events                 │
│                          │  ...                              │
│  Text...                 │                                   │
│                          │  AKTUELLE NEWS                    │
│  H2: Zwischenueberschr. │  → Beitrag 1                     │
│                          │  → Beitrag 2                     │
│  Text...                 │  → Beitrag 3                     │
│                          │                                   │
│  [YouTube-Embed]         │  NEWSLETTER                      │
│                          │  [E-Mail] [Anmelden]             │
│  Text...                 │                                   │
│                          │  CTA                             │
│  [LinkedIn] [E-Mail]     │  [Beratung anfragen]             │
│  [Link kopieren]         │                                   │
│                          │                                   │
├──────────────────────────┴──────────────────────────────────┤
│  VERWANDTE PRODUKTE                                         │
│  ┌─────┐ ┌─────┐ ┌─────┐                                   │
│  └─────┘ └─────┘ └─────┘                                   │
├─────────────────────────────────────────────────────────────┤
│  [← Vorheriger Beitrag]        [Naechster Beitrag →]       │
├─────────────────────────────────────────────────────────────┤
│  CTA: "Bleiben Sie informiert."                             │
│  [Newsletter] [Alle News]                                   │
├─────────────────────────────────────────────────────────────┤
│                        Footer                                │
└─────────────────────────────────────────────────────────────┘
```

### D) Dynamische Elemente
- Artikel: Standard-WP-Post mit Kategorien und Tags
- Sidebar: WP-Widgets (Kategorien, Aktuelle Beitraege, Newsletter)
- Verwandte Produkte: ACF Relationship Field (Beitrag → Produkt)
- Social Sharing: Leichtes Plugin (z.B. Scriptless Social Sharing)
- Newsletter: Mailchimp/Brevo-Integration oder WP-Plugin

### E) SEO-Anforderungen
- **Title-Schema:** "[Artikeltitel] | KORODUR News"
- **Meta-Description-Schema:** Manuell pro Beitrag (Yoast SEO) oder automatisch: Ersten 160 Zeichen des Artikels
- **Schema.org:** Article (headline, datePublished, author, image, publisher) + BreadcrumbList
- **H1:** Artikeltitel (1x)
- **Open Graph:** og:title, og:description, og:image fuer LinkedIn-Sharing

### F) Besonderheiten fuer Mehrsprachigkeit
- `/unternehmen/news/[slug]/` → `/en/company/news/[slug]/` → `/fr/entreprise/actualites/[slug]/`
- Entscheidung: Alle Beitraege uebersetzen oder nur ausgewaehlte?
- Empfehlung: Wichtige Beitraege (Produktneuheiten, grosse Referenzen) in EN/FR; kleinere News nur DE
- Hreflang nur wenn Uebersetzung existiert, sonst x-default auf DE

### G) Verknuepfungen
→ Produktdetailseiten (verwandte Produkte), Referenzprojekte, News-Uebersicht, Newsletter-Anmeldung, Kontakt

---

## Zusammenfassung: Seitentypen und WordPress-Umsetzung

| # | Seitentyp | WordPress-Umsetzung | Custom Post Type | Anzahl Seiten (DE) |
|---|-----------|--------------------|-----------------|--------------------|
| 1 | Homepage | Statische Seite (Page) | -- | 1 |
| 2 | Produktuebersicht | Taxonomie-Archiv-Template | CPT "Produkt" + Tax. "Produktgruppe" | ~25 |
| 3 | Produktdetailseite | Single-Template fuer CPT | CPT "Produkt" + ACF Fields | ~71 |
| 4 | Anwendungsseite | Statische Seiten (Pages) mit ACF | -- (Pages mit Template) | ~12 |
| 5 | Planerbereich | Statische Seite + Unterseiten | -- (Pages mit Template) | ~7 |
| 6 | Download-Center | Statische Seite mit Ajax-Filter | CPT "Download" + Tax. "Dokumenttyp" | 1 (+Eintraege) |
| 7 | Referenz-Uebersicht | Taxonomie-Archiv-Template | CPT "Referenz" + Tax. "Branche" | 1 |
| 8 | Referenz-Detail | Single-Template fuer CPT | CPT "Referenz" + ACF Fields | ~131 |
| 9 | Haendlerfinder | Statische Seite mit JS-App | CPT "Haendler" | 1 (+Eintraege) |
| 10 | Unternehmensseite | Statische Seite (Page) | -- | ~8 |
| 11 | Kontaktseite | Statische Seite mit Formular | -- | ~3 |
| 12 | Blog/News | Standard-WP-Post | WP Posts + Kategorien | ~10+ |

**Benoetigte Custom Post Types:** Produkt, Referenz, Download, Haendler
**Benoetigte Custom Taxonomies:** Produktgruppe, Branche, Region, Dokumenttyp
**Benoetigte Plugins:** ACF Pro (Custom Fields), FacetWP oder SearchWP (Filter), Contact Form 7 / Gravity Forms, Yoast SEO, WPML oder Polylang (Mehrsprachigkeit)

---

## CTA-Strategie (seitenuebergreifend)

Der groesste Schwachpunkt der alten Website war das **komplette Fehlen von CTAs**. Die neue Website muss auf JEDER Seite mindestens 2 CTAs haben:

| CTA-Typ | Wo | Primaere Aktion | Sekundaere Aktion |
|---------|----|-----------------|--------------------|
| **Header-CTA** | Alle Seiten (Header) | Telefon sichtbar | "Kontakt" Button |
| **Hero-CTA** | Homepage, Anwendung, Planer | "Produkte entdecken" | "Beratung anfragen" |
| **Produkt-CTA** | Produktdetail | "TDS herunterladen" + "GAEB" | "Beratung" + "Wo kaufen?" |
| **Abschluss-CTA** | Alle Seiten (vor Footer) | "Kontakt aufnehmen" | "Hotline anrufen" |
| **Sticky-CTA** | Mobile (alle Seiten) | "Anrufen" | "Anfragen" |
| **Inline-CTA** | Blog, Referenz | "Produkt ansehen" | "Newsletter" |

---

*Erstellt am 2026-03-24 auf Basis von: ia_new.md (v1.0), zielgruppen.md (v1.0), feature_matrix.md (v1.0), content_audit.md (v1.0)*
