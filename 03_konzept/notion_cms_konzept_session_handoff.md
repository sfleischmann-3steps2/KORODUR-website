# Session Handoff: Notion als CMS & Wissens-Backbone

**Datum:** 2026-04-17
**Version:** 0.1 (Konzept-Entwurf, vor Notion-MCP-Anbindung)
**Status:** Handoff-Dokument für Folgesession mit aktivem Notion MCP
**Autor:** Konzept-Session Claude Code
**Ablage:** `/03_konzept/`

---

## 1. Ausgangslage

Wir befinden uns in **Phase 1 (Analyse)** des KORODUR-Website-Relaunches.
Parallel zur Analyse entstehen bereits einzelne Landingpages (z. B. microTOP,
Sanierungs-Applikation). Damit diese Einzelmaßnahmen nicht als Silos stehen
bleiben, soll eine **gemeinsame inhaltliche Infrastruktur** geschaffen werden,
aus der alle zukünftigen Seiten gespeist werden.

## 2. Zielbild (grobe Architektur-Idee)

- **Notion = Single Source of Truth** für alle inhaltlichen Kern-Entitäten
  (Produkte, technische Werte, Referenzen, Medien, Anwendungen, FAQ, Glossar etc.)
- **Sync-Pipeline** zieht Inhalte aus Notion in den Website-Build:
  - Trigger-basiert bei Änderung (Webhook)
  - Zeitgesteuert (täglich) als Safety-Net
- **Seitentypen als Templates**, die sich dynamisch aus Notion-Feldern
  zusammensetzen (Produkt-Template, Anwendungs-Landingpage,
  Sanierungs-Konfigurator …)
- **Jede Landingpage** (microTOP, Sanierung etc.) ist keine Insel mehr,
  sondern nutzt dieselben Kern-Entitäten → konsistente Daten, Wiederverwendung,
  skalierbar

**Vorteil:** Fachabteilungen pflegen in gewohnter Notion-Umgebung; Marketing
baut Seiten aus Bausteinen zusammen.

**Tradeoffs, die wir im Blick behalten müssen:**
- Notion ist kein echtes headless CMS (Rate-Limits, keine nativen Workflows,
  begrenzte Feldtypen bei strukturierter Rich-Content-Pflege, keine native
  Versionierung).
- Properties sind bei Textlänge limitiert – Pages/Subpages dagegen nicht.
  → **Konsequenz: page-zentrisch denken, nicht property-zentrisch.**

## 3. Wichtigste strategische Entscheidungen dieser Session

### 3.1 Notion-Struktur ist eigenständiges Thema – nicht nur Website-Zulieferung

Die Notion-Datenbanken sind primär ein **Wissensmanagement-Asset** für das
Unternehmen (Inhaber-Arbeit, Technik, Vertrieb, Marketing). Die Website ist nur
ein **Consumer** dieses Assets. Das heißt: Wir modellieren die Struktur zuerst
aus Unternehmens-/Prozesssicht, nicht aus Website-Sicht.

### 3.2 Trennung nach Daten-Charakter, nicht nach Produktgruppe

Die bestehende Produktdatenbank ist zu groß und vermischt unterschiedliche
Daten-Charaktere. Statt sie nach Produktgruppen (Hartstoffe, microTOP etc.)
aufzuteilen, trennen wir nach **Art der Information / Ownership**:

| DB | Ownership | Inhalt (Daten-Charakter) |
|---|---|---|
| **DB 1 – Produkt-Technik** | Technik (in Zusammenarbeit mit Vertrieb) | Was ist das Produkt? Was kann es? Was muss bei der Verarbeitung beachtet werden? Technische Werte, Messverfahren, Verarbeitungshinweise, Normenkonformität |
| **DB 2 – Produkt-Marketing** | Strategisches & operatives Marketing (in Zusammenarbeit mit Vertrieb) | Positionierung, Nutzenversprechen, Zielgruppen-Anspra­che, Medien (Bilder, Videos), Referenzprojekte, Sets, Kampagnen, Content-Bausteine |

Beide DBs teilen sich dieselben Produkte (über Relation oder gemeinsame
ID/Master), pflegen aber jeweils den Ausschnitt, der in ihrer Verantwortung
liegt. Keine der beiden Abteilungen arbeitet allein, aber jede hat klare
Hoheit über ihre Felder.

### 3.3 Einstieg: bewusst auf 2 DBs beschränken

Wir starten **bewusst reduziert** mit den beiden oben genannten DBs. Weitere
Datenbanken (Referenzen, Medien-Library, Anwendungen, Glossar, FAQ,
Normen/Standards, Märkte/Regionen …) werden **erst ergänzt, wenn sich aus der
Arbeit mit den zwei Kern-DBs ein konkreter Bedarf ergibt**. Vorab prüfen:
Welche dieser DBs existieren schon im Notion-Workspace?

## 4. Offene Fragen für die nächste Session (mit aktivem Notion MCP)

1. **Ist-Aufnahme:** Welche Properties hat die aktuelle Produktdatenbank
   heute? Welche sind technisch, welche Marketing, welche Meta/Organisation?
2. **Bestehende DBs:** Welche weiteren relevanten Datenbanken existieren
   bereits im Workspace (Referenzen, Bilder, Videos, Kunden, Projekte …)?
3. **Beziehungen:** Wie sind bestehende DBs heute miteinander verknüpft
   (Relations, Rollups)? Wo gibt es redundante / widersprüchliche Pflege?
4. **Mehrsprachigkeit:** Wie wird DE/EN/FR heute in Notion abgebildet?
   (Eine Seite mit Sprachfeldern? Getrennte Datensätze? Getrennte DBs?)
5. **Page-Content:** Welche Produkte haben heute schon strukturierte
   Subpages/Inhalte innerhalb ihrer Notion-Seite, die wir als Rich Content
   in die Website übernehmen wollen?

## 5. Geplante Arbeitsschritte der Folgesession

**Voraussetzung:** Notion MCP ist in der Claude-Code-Konfiguration aktiv und
hat Lese- (mindestens) bzw. Schreibzugriff auf die relevanten KORODUR-DBs.

### Schritt 1 – Inventur (nur lesen)
- Alle relevanten DBs inspizieren: Name, Property-Liste, Property-Typen,
  Anzahl Datensätze, Beispieleinträge
- Ergebnis: `/03_konzept/notion_inventur.md`

### Schritt 2 – Ziel-Schema entwerfen
- Property-Liste für **DB 1 (Produkt-Technik)** und **DB 2 (Produkt-Marketing)**
- Definition Relation-Anker (wie werden beide DBs am Produkt verknüpft?)
- Vorschlag für page-interne Struktur (Subpages / Rich Content)
- Ergebnis: `/03_konzept/notion_zielschema.md`

### Schritt 3 – Migrationspfad
- Wie überführen wir die bestehende Produktdatenbank in die neue Struktur,
  ohne Wissen zu verlieren?
- Wer macht was (Technik / Marketing / Vertrieb)?
- Meilensteine & Sequenz
- Ergebnis: `/03_konzept/notion_migration.md`

### Schritt 4 – Sync-Architektur (später, nach stabiler DB-Struktur)
- Webhook-Trigger + täglicher Cron
- Ziel-Stack Website (Astro/Next.js + statische Builds?)
- Template-Mapping: Welche Seitentypen ziehen welche Felder?
- Ergebnis: `/03_konzept/website_sync_architektur.md`

## 6. Prompt-Vorlage zum Wiedereinstieg in neue Session

> Wir arbeiten am Konzept, **Notion als CMS & Wissens-Backbone** für die neue
> KORODUR-Website aufzusetzen. Kontext und strategische Entscheidungen stehen
> in `/03_konzept/notion_cms_konzept_session_handoff.md` – bitte zuerst lesen.
>
> Notion MCP ist jetzt angebunden. Starte bitte mit **Schritt 1 – Inventur**:
> Liste mir alle erreichbaren Datenbanken aus unserem Notion-Workspace auf
> (Name, Anzahl Datensätze, grobe Einordnung) und frage mich dann, welche
> davon für das Konzept relevant sind. Erst danach in die Property-Tiefe
> gehen. Ergebnis in `/03_konzept/notion_inventur.md` dokumentieren.

## 7. Wichtige Rahmenbedingungen (aus CLAUDE.md)

- Interne Dokumente: **Deutsch**
- Code-Kommentare: **Englisch**
- Keine produktiven Deployments ohne Freigabe
- Keine Änderungen an der Live-Website
- Keine API-Keys / Zugangsdaten in Dateien ablegen
- Keine Datei überschreiben ohne expliziten Hinweis
- Alle Markdown-Dokumente mit Datum und Version im Header

---

**Nächste Aktion für den Menschen (Stefan):**
1. Notion Integration Token erzeugen und Zugriff auf relevante DBs gewähren
2. Notion MCP in Claude-Code-Konfiguration eintragen
3. Neue Session mit dem Prompt aus Abschnitt 6 starten
