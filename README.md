korodur-website – Projekt-README
Stand: 2026-03-23 | Verantwortlich: Steffi (Applied AI Manager, KORODUR)
---
Projektziel
Schrittweiser Relaunch von korodur.de – Bereich für Bereich, nicht von heute auf morgen.
Die neue Website soll die drei B2B-Zielgruppen (Planer, Verarbeiter, Handel) klar adressieren
und deutlich mehr Mehrwert bieten als die aktuelle Seite.
---
Schwesterprojekt: KORODUR-Sanierung_app
Repo: https://github.com/sfleischmann-3steps2/KORODUR-Sanierung_app
Live: https://sfleischmann-3steps2.github.io/KORODUR-Sanierung_app/de/

Die Sanierungs-App ist seit 2026-04-17 offiziell als **Keimzelle der neuen korodur.de**
eingeplant – nicht als eingebetteter Baustein in WordPress, sondern als technisches und
gestalterisches Fundament für den Relaunch.

**Rolle der App im Relaunch:**
- **Flow-Werkstatt** – neue UX-Flows (Produktfinder, Referenz-Navigation, Planerbereich,
  Download-Center) werden dort prototypisch geschärft, bevor sie in die neue Website wandern.
- **Stack-Vorbild** – Next.js Static Export + TypeScript + Tailwind, wie es die neue
  Website ebenfalls nutzen soll.
- **Content-Fundament** – 26 Referenzen, 16 Produkte, 4 Sprachen – migrierbar in das
  zukünftige Headless CMS (Favorit: Payload, Fallback: Sanity).

**Aktueller Stand (2026-04-17):**
- Sanierungs-App V2.3 live, 4 Sprachen (DE/EN/FR/PL)
- Strategie-Spec: `docs/superpowers/specs/2026-04-17-korodur-website-stack-strategie-design.md`
  (im Schwester-Repo)
- Vorgehen: Ansatz B – UX-Arbeit in der App + parallel Payload-CMS-Prototyp (4-Wochen-Timebox)
- Multi-Locale-Modell: 8 Startlocales (DACH + FR + PL + IT + NL + EN-international)

Die IA aus `03_konzept/ia_new.md` bleibt die Referenz für die neue Website und ist
CMS-agnostisch – sie trägt sowohl eine WP-Umsetzung als auch den geplanten Next.js + Headless-Stack.
---
Projektstruktur
```
korodur-website/
│
├── CLAUDE.md                          ← Projektkontext für alle Claude Code Sessions
├── README.md                          ← Diese Datei
│
├── 01_analyse/
│   ├── TASK_technical_audit.md        ✅ Task definiert → ausführen
│   ├── TASK_structure_content_audit.md ✅ Task definiert → ausführen
│   ├── technical_audit.md             ← [OUTPUT: noch nicht erstellt]
│   ├── structure_audit.md             ← [OUTPUT: noch nicht erstellt]
│   └── content_audit.md               ← [OUTPUT: noch nicht erstellt]
│
├── 02_benchmark/
│   ├── TASK_competitors.md            ✅ Task definiert → ausführen
│   ├── TASK_zielgruppenplattformen.md ✅ Task definiert → ausführen
│   ├── competitors.md                 ← [OUTPUT: noch nicht erstellt]
│   ├── zielgruppenplattformen.md      ← [OUTPUT: noch nicht erstellt]
│   └── feature_matrix.md              ← [OUTPUT: aus Benchmark generiert]
│
├── 03_konzept/
│   ├── zielgruppen.md                 ← Personas & User Journeys
│   ├── ia_new.md                      ← Neue Informationsarchitektur
│   ├── page_templates.md              ← Seitentypen & Wireframe-Beschreibungen
│   └── rollout_plan.md                ← Phase-für-Phase Umsetzungsplan
│
└── 04_umsetzung/
    ├── phase_01/                       ← z.B. neue Homepage
    ├── phase_02/                       ← z.B. Produktseiten
    └── phase_03/                       ← ...
```
---
Phasenstatus
Phase	Status	Nächster Schritt
1 – Analyse	🟡 Tasks definiert	Claude Code: TASK_technical_audit.md ausführen
2 – Benchmark	🟡 Tasks definiert	Nach Phase 1 starten
3 – Konzept	⬜ Noch nicht begonnen	Nach Phase 2
4 – Umsetzung	⬜ Noch nicht begonnen	Iterativ ab Phase 3
---
Wie man mit Claude Code arbeitet
Session starten
```bash
cd /path/to/korodur-website
claude  # Claude Code liest CLAUDE.md automatisch
```
Task ausführen
```
> Führe den Task in 01_analyse/TASK_technical_audit.md aus
  und schreibe das Ergebnis nach 01_analyse/technical_audit.md
```
Empfohlene Reihenfolge
`TASK_technical_audit.md` → schreibt `technical_audit.md`
`TASK_structure_content_audit.md` → schreibt `structure_audit.md` + `content_audit.md`
`TASK_competitors.md` → schreibt `competitors.md`
`TASK_zielgruppenplattformen.md` → schreibt `zielgruppenplattformen.md`
Aus 3+4: `feature_matrix.md` generieren lassen
Dann: Konzept-Dokumente in `03_konzept/`
---
Wichtige Entscheidungen (Log)
Datum	Entscheidung	Begründung
2026-03-23	Schrittweiser Relaunch (kein Big Bang)	Risikoreduzierung, frühe Sichtbarkeit
2026-03-23	WordPress bleibt vorerst als CMS	Migration zu komplex für Phase 1
2026-03-23	Drei Zielgruppen gleichwertig adressieren	Planer / Verarbeiter / Handel
2026-04-17	Sanierungs-App wird Keimzelle der neuen Website	Einheitlicher Stack, keine Iframe-Kompromisse
2026-04-17	Frontend-Stack: Next.js festgelegt	Produktiv bewährt in Sanierungs-App
2026-04-17	CMS-Kategorie: Headless + strukturierte Inhalte	Editor-UI + Agent-Workflow + Multi-Locale
2026-04-17	Konkretes CMS später (Payload-Favorit, Sanity-Fallback)	Evidenzbasierte Entscheidung via 4-Wochen-Prototyp
2026-04-17	Multi-Locale-Modell: 8 Startlocales	DACH + FR + PL + IT + NL + EN-international
---
Kontakt & Verantwortlichkeiten
Projektleitung & AI-Umsetzung: Steffi (KORODUR Applied AI Manager)
Fachlicher Content: KORODUR Produktmanagement / Vertrieb
Review & Freigabe: Geschäftsführung KORODUR
