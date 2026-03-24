# KORODUR Website Relaunch – Projektkontext für Claude Code

## Unternehmen
**KORODUR International GmbH**, Amberg (Bayern)
- Spezialist für mineralische Hartstoffe & zementäre Industrieböden seit 1936
- Produktlinien: Hartstoff-Estriche, Reparaturmörtel, Spezialputze, Trinkwasserschutz, Katzenstreu
- Produktionsstandorte: Amberg, Bochum-Wattenscheid, Freihung/Bayern, Hannover-Misburg
- ISO 9001:2015 zertifiziert (TÜV Süd)
- Internationaler Vertrieb (DACH + Export)
- Website: https://www.korodur.de (WordPress, mehrsprachig: DE/EN/FR)

## Primäre Zielgruppen der neuen Website
1. **Planer & Architekten** – suchen Ausschreibungstexte, TDS, Normenkonformität, DGNB-Relevanz
2. **Bauunternehmen & Verarbeiter** – suchen Verarbeitungshinweise, technische Datenblätter, Referenzprojekte
3. **Handel & Distributoren** – suchen Produktübersichten, Bestellinformationen, Händlerportal

## Projektstrategie: Schrittweiser Ersatz (kein Big-Bang-Relaunch)
- Die alte Website (korodur.de) wird **Bereich für Bereich** durch neue Seiten ersetzt
- Parallel laufen alt und neu → keine 100%-Umstellung von heute auf morgen
- Jede Phase liefert sichtbare, öffentliche Ergebnisse
- Reihenfolge orientiert sich an Traffic-Priorität & strategischer Relevanz

## Projektphasen
```
Phase 1 – Analyse      → bestehende Website vollständig verstehen
Phase 2 – Benchmark    → Wettbewerber & zielgruppenrelevante Plattformen
Phase 3 – Konzept      → IA, Zielgruppen-Journeys, Seitentypen, Rollout-Plan
Phase 4 – Umsetzung    → Seite für Seite, iterativ
```

## Aktuelle Phase
**Phase 1 – Analyse** (aktiv)

## Sprachkonventionen
- Interne Dokumente: Deutsch
- Code-Kommentare: Englisch
- Website-Inhalte: Primär Deutsch (mit EN/FR als Sekundärsprachen)

## Technischer Kontext
- CMS: WordPress (bestehend, Struktur bleibt vorerst)
- Ziel-Stack für Neuentwicklung: TBD (ggf. Astro/Next.js + headless CMS)
- Repo: github.com/korodur/korodur-website (oder analog)
- Branching: `main` = stabil, `phase-X/feature-name` = Entwicklung

## Subagenten-Regeln
- Jede Analyse-Session schreibt in `/01_analyse/`
- Jede Benchmark-Session schreibt in `/02_benchmark/`
- Konzept-Dokumente gehen in `/03_konzept/`
- Umsetzung pro Phase in `/04_umsetzung/phase_XX/`
- Keine Datei überschreiben ohne expliziten Hinweis
- Alle Markdown-Dokumente mit Datum und Version im Header

## Wichtige URLs & Ressourcen
- Aktuelle Website: https://www.korodur.de
- EN-Version: https://www.korodur.de/en/
- Produkte: https://www.korodur.de/en/products/
- Unternehmen: https://www.korodur.de/en/company/
- Nachhaltigkeit: https://www.korodur.de/en/company/sustainability/

## Do not
- Keine produktiven Deployments ohne Freigabe
- Keine Änderungen an der Live-Website
- Keine API-Keys oder Zugangsdaten in Dateien ablegen
