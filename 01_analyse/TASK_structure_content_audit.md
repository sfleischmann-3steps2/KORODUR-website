# Task: Struktur- & Inhaltsaudit – korodur.de
**Version:** 1.0 | **Datum:** 2026-03-23 | **Phase:** 1 – Analyse
**Output-Dateien:** `01_analyse/structure_audit.md` + `01_analyse/content_audit.md`

---

## Ziel
Verstehen, wie die aktuelle Website strukturiert ist, welche Inhalte vorhanden sind –
und vor allem: **was fehlt** aus Sicht der drei Zielgruppen.

---

## Teil A: Strukturaudit

### 1. Navigationsstruktur rekonstruieren
Crawle alle erreichbaren Seiten von korodur.de und erstelle eine vollständige Sitemap:

```
Hauptnavigation:
├── [Menüpunkt 1]
│   ├── Unterseite 1.1
│   └── Unterseite 1.2
├── [Menüpunkt 2]
...

Footer-Navigation:
├── ...
```

### 2. Informationsarchitektur bewerten
- Wie viele Klicks braucht ein Planer, um ein relevantes Datenblatt zu finden?
- Wie viele Klicks braucht ein Verarbeiter, um Verarbeitungshinweise zu finden?
- Gibt es einen dedizierten Planerbereich / Ausschreibungsbereich?
- Gibt es einen Download-Bereich für TDS/SDS?
- Wie sind Referenzprojekte organisiert?
- Gibt es eine Händlersuche / Vertriebspartnersuche?

### 3. Zielgruppen-Navigation
- Werden Zielgruppen explizit adressiert? (z.B. "Für Planer", "Für Verarbeiter")
- Gibt es zielgruppenspezifische Einstiegspunkte?
- Wird zwischen Produktkategorien und Anwendungsbereichen unterschieden?

### 4. Mehrsprachige Konsistenz
- Sind alle DE-Seiten auch auf EN und FR vorhanden?
- Sind Inhalte identisch oder adaptiert?
- Welche Seiten existieren nur auf Deutsch?

---

## Teil B: Inhaltsaudit

### 1. Produktseiten inventarisieren
Für jede Produktseite notieren:
- Produktname & SKU
- Kategorie
- Beschreibungstiefe (1–5: oberflächlich bis technisch vollständig)
- TDS vorhanden? (Link oder Download)
- SDS vorhanden?
- Anwendungsbereiche beschrieben?
- Bilder vorhanden?
- Cross-Selling / verwandte Produkte?

### 2. Content-Qualitätsbewertung
| Content-Typ | Vorhanden? | Qualität | Zielgruppe adressiert? |
|-------------|-----------|----------|----------------------|
| Produktbeschreibungen | | 1–5 | |
| Technische Datenblätter (TDS) | | | |
| Sicherheitsdatenblätter (SDS) | | | |
| Verarbeitungshinweise | | | |
| Referenzprojekte | | | |
| Ausschreibungstexte / LV-Texte | | | |
| Zertifikate & Normen | | | |
| News / Aktuelles | | | |
| Nachhaltigkeitsinformationen | | | |
| Videocontent | | | |
| Händlersuche | | | |

### 3. CTA-Analyse (Call-to-Actions)
- Welche CTAs gibt es auf der Homepage?
- Welche CTAs gibt es auf Produktseiten?
- Gibt es Anfrage-/Kontaktformulare?
- Gibt es einen Konfigurator oder Produktfinder?
- Werden Telefonnummern/Kontaktpersonen sichtbar angezeigt?

### 4. Content-Gaps für Zielgruppen

**Planer & Architekten – was fehlt?**
- [ ] Ausschreibungstexte (GAEB, STLB-Bau-kompatibel)
- [ ] BIM-Objekte / CAD-Downloads
- [ ] Normennachweise (DIN 18560, EN 13813, etc.)
- [ ] DGNB/LEED-relevante Produktinformationen (EPD)
- [ ] Planerhotline / direkter Ansprechpartner
- [ ] Muster-Leistungsverzeichnisse

**Bauunternehmen & Verarbeiter – was fehlt?**
- [ ] Verarbeitungsvideos
- [ ] Schritt-für-Schritt Verarbeitungsanleitungen
- [ ] FAQ zu Produkten
- [ ] Produktrechner (Mengenberechnung)
- [ ] Technischer Support / Hotline prominent
- [ ] Schulungsangebote

**Handel & Distributoren – was fehlt?**
- [ ] Händlerportal / Login
- [ ] Produktkatalog als Download
- [ ] Preislisten (geschützt)
- [ ] Händlerfinder / Wo kaufen
- [ ] Neuheitenmeldungen / Newsletter

---

## Output-Format

```
01_analyse/structure_audit.md    ← Sitemap + IA-Bewertung
01_analyse/content_audit.md      ← Inventar + Gaps + Empfehlungen
```

---

## Hinweise für den Agenten
- Bei 403-Fehlern: Google-Cache, Wayback Machine, oder gespeicherte Suchergebnisse nutzen
- Content-Gaps sind mindestens genauso wichtig wie vorhandener Content
- Alles aus Sicht der Zielgruppen bewerten, nicht aus technischer Sicht
- Bewertung auf einer 1–5 Skala: 1=nicht vorhanden/mangelhaft, 5=exzellent
