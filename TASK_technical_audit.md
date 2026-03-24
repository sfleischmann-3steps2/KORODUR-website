# Task: Technisches Audit – korodur.de
**Version:** 1.0 | **Datum:** 2026-03-23 | **Phase:** 1 – Analyse
**Output-Datei:** `01_analyse/technical_audit.md`

---

## Ziel
Vollständige technische Bestandsaufnahme der aktuellen Website korodur.de.
Ergebnis ist ein strukturiertes Dokument, das als Grundlage für alle weiteren Entscheidungen dient.

---

## Aufgaben für Claude Code

### 1. Stack & Infrastruktur identifizieren
- CMS erkennen (WordPress-Version, Theme, bekannte Plugins)
- Hosting/Server-Technologie (via HTTP-Header, Wappalyzer-ähnliche Analyse)
- CDN / Caching-Layer vorhanden?
- SSL-Zertifikat & HTTPS-Konfiguration
- robots.txt & sitemap.xml abrufen und analysieren

```bash
# Beispiel-Befehle für den Agenten:
curl -I https://www.korodur.de
curl https://www.korodur.de/robots.txt
curl https://www.korodur.de/sitemap.xml
curl https://www.korodur.de/sitemap_index.xml
```

### 2. Performance-Analyse
- Core Web Vitals abschätzen (via PageSpeed Insights API oder Lighthouse CLI)
- Ladezeit der Homepage messen
- Bildoptimierung: Werden WebP/AVIF verwendet? Lazy Loading?
- JavaScript-Bundle-Größe einschätzen
- Mobile Performance gesondert betrachten

```bash
# Lighthouse CLI (falls verfügbar):
npx lighthouse https://www.korodur.de --output json --output-path ./lighthouse_report.json
```

### 3. SEO-Grundstruktur
- Meta-Tags der Homepage (title, description, OG-Tags)
- Heading-Hierarchie (H1–H3)
- Canonical-Tags vorhanden?
- Hreflang-Tags für DE/EN/FR korrekt gesetzt?
- Schema.org-Markup vorhanden?
- Interne Verlinkungsstruktur (wie tief sind Produkte verlinkt?)

### 4. URL-Struktur & Mehrsprachigkeit
- Sprachpfade dokumentieren (/de/, /en/, /fr/ oder Subdomains?)
- Konsistenz der URL-Struktur über Sprachen hinweg
- Legacy-URLs identifizieren (z.B. .html-Endungen)
- Weiterleitungs-Kette bei alten URLs?

### 5. Seitentypen-Inventar
Welche Seitentypen existieren aktuell?
- [ ] Homepage
- [ ] Produktkategorie-Seiten
- [ ] Produktdetailseiten
- [ ] Referenzseiten
- [ ] Unternehmensseiten
- [ ] Kontaktseiten
- [ ] Downloads/Dokumente
- [ ] Blog/News
- [ ] Sonstige

### 6. Cookie & Datenschutz
- Welches Consent-Tool wird verwendet?
- DSGVO-konform?
- Analytics-Tools (Google Analytics, Matomo, etc.)?

---

## Output-Format
Das fertige Audit wird als strukturiertes Markdown gespeichert:

```
01_analyse/technical_audit.md
```

### Struktur des Output-Dokuments:
```markdown
# Technisches Audit – korodur.de
**Stand:** DATUM | **Erstellt von:** Claude Code

## Zusammenfassung & Kritische Findings
[Top 5 wichtigste Erkenntnisse]

## 1. Stack & Infrastruktur
...

## 2. Performance
...

## 3. SEO
...

## 4. URL-Struktur
...

## 5. Seitentypen-Inventar
...

## 6. Datenschutz & Tracking
...

## Bewertungsmatrix
| Bereich | Status | Priorität |
|---------|--------|-----------|
| Performance | 🔴/🟡/🟢 | Hoch/Mittel/Niedrig |
...

## Empfehlungen für Phase 3 (Konzept)
[Was muss beim Neuaufbau unbedingt adressiert werden?]
```

---

## Hinweise für den Agenten
- Manche Seiten geben 403 zurück – dann via Google Cache oder Wayback Machine arbeiten
- Fokus auf Findings, die für die Zielgruppen (Planer, Verarbeiter, Handel) relevant sind
- Technische Schulden explizit benennen, nicht beschönigen
