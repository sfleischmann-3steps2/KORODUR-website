# Technisches Audit -- korodur.de
**Stand:** 2026-03-24 | **Erstellt von:** Claude Code | **Version:** 1.0 | **Phase:** 1 -- Analyse

---

## Zusammenfassung & Kritische Findings

1. **Kein H1 auf der Homepage (DE + EN)** -- Die wichtigste Seite der Website hat keinen H1-Tag. Schwerwiegender SEO-Fehler.
2. **Keine hreflang-Tags im HTML-Head** -- Die dreisprachige Website (DE/EN/FR) setzt hreflang nur in der Sitemap, nicht im HTML `<head>`. Google empfiehlt beides.
3. **Schema.org Breadcrumb-Bug: "Maison" statt "Startseite"** -- Die DE-Homepage zeigt im JSON-LD Breadcrumb den franzoesischen Begriff "Maison" statt "Startseite". Klarer WPML/Yoast-Konfigurationsfehler.
4. **EN-Homepage: Generischer Title "Homepage -- korodur"** -- Kein beschreibender Title-Tag, keine Keywords. Verschenktes SEO-Potenzial fuer den internationalen Markt.
5. **WooCommerce als Produkt-Engine fuer Baustoffe** -- WooCommerce (Shop-System) wird fuer einen B2B-Produktkatalog verwendet. Erzeugt unnoetige Shop-Overhead (Warenkorb, Checkout, etc.) und suboptimale URL-Struktur (`/produkt/` statt semantischer Pfade).

---

## 1. Stack & Infrastruktur

### CMS & Versionen
| Komponente | Version | Quelle |
|---|---|---|
| WordPress | 6.9.4 | `<meta name="generator">` |
| PHP | 8.2.30 | HTTP-Header `x-powered-by` |
| WooCommerce | 10.6.1 | `<meta name="generator">` |
| Yoast SEO | 27.2 | HTML-Kommentar |
| WPML | 4.9.2 | `<meta name="generator">` |
| Elementor | 3.35.7 | `elementorFrontendConfig` JS |
| Elementor Pro | vorhanden | JS-Referenzen |
| Complianz GDPR | 7.4.5 | `complianz` JS-Config |
| Astra Theme | 4.12.5 | Body-Class `astra-4.12.5` |
| Astra Child Theme | aktiv | Pfad `themes/astra-child` |

### Erkannte Plugins (aus HTML-Quellcode)
| Plugin | Zweck |
|---|---|
| **Yoast SEO** | SEO-Management, Schema.org, Sitemaps |
| **WPML** + WooCommerce Multilingual | Mehrsprachigkeit (DE/EN/FR) |
| **Elementor** + Elementor Pro | Page Builder |
| **WooCommerce** + WooCommerce Multilingual | Produktkatalog (missbraucht als B2B-Katalog) |
| **WP-Optimize Premium** | Caching, Minification, Lazy Load |
| **Complianz GDPR** | Cookie-Consent |
| **Jet Engine** | Custom Post Types, Listings, Dynamic Content |
| **Jet Search** | AJAX-Suche |
| **Jet Smart Filters** | Filterbare Listings |
| **Premium Addons for Elementor** | Erweiterte Elementor-Widgets |
| **Simple Custom CSS and JS** | Individuelle Code-Snippets |
| **Pafe (Pro Addons for Elementor)** | Weitere Elementor-Erweiterungen |
| **Dynamic Conditions** | Bedingte Elementor-Anzeige |
| **ECS (Elementor Custom Skin)** | Custom Post Skin fuer Elementor |

### Hosting & Infrastruktur
| Aspekt | Detail |
|---|---|
| **Server** | Cloudflare (Reverse Proxy) |
| **Hosting-Backend** | Plesk-basiert (`x-powered-by: PleskLin`) |
| **CDN** | Cloudflare (inkl. Bot-Protection, Challenge-Mode) |
| **SSL** | HTTPS korrekt, Cloudflare-Zertifikat |
| **Caching** | WP-Optimize Premium (`wpo-cache-status`) -- Status "not cached" bei HEAD-Requests; Minified JS/CSS ueber `/wp-content/cache/wpo-minify/` |
| **Bot-Protection** | Cloudflare Challenge aktiv -- blockiert curl ohne Browser-UA mit 403 |
| **HTTP/2** | Ja (Cloudflare) |
| **Security-Headers** | Gut: `X-Content-Type-Options`, `X-Frame-Options`, `Referrer-Policy`, `Permissions-Policy`, `COEP`, `COOP`, `CORP` |
| **Speculation Rules** | Cloudflare Speculation Rules aktiv (`/cdn-cgi/speculation`) |

### robots.txt
```
User-agent: *
Disallow: /wp-content/uploads/wc-logs/
Disallow: /wp-content/uploads/woocommerce_transient_files/
Disallow: /wp-content/uploads/woocommerce_uploads/
Disallow: /*?add-to-cart=
Disallow: /*?*add-to-cart=
Disallow: /wp-admin/
Disallow: /wp-content/uploads/wpo/wpo-plugins-tables-list.json
Allow: /wp-admin/admin-ajax.php
Sitemap: https://www.korodur.de/sitemap_index.xml
```
**Bewertung:** Funktional, aber WooCommerce-spezifische Eintraege deuten auf Shop-Ueberreste hin.

### Sitemap-Struktur
| Sitemap | URLs | Letztes Update |
|---|---|---|
| `post-sitemap.xml` | ~10 | 2024-11-08 |
| `page-sitemap.xml` | 204 | 2026-03-23 |
| `product-sitemap.xml` | 203 | 2026-03-24 |
| `referenzen-sitemap.xml` | 396 | 2026-03-11 |
| `product_cat-sitemap.xml` | ~45 | 2026-03-24 |
| **Gesamt** | **~858** | |

**Auffaelligkeiten:**
- Referenzen-Sitemap ist mit 396 URLs die groesste -- deutet auf umfangreiche Referenzdatenbank hin
- Post-Sitemap hat nur ~10 Eintraege und wurde seit Nov 2024 nicht aktualisiert -- Blog/News offenbar vernachlaessigt
- Hreflang-Verweise in der Sitemap sind korrekt implementiert (de/en/fr + x-default)

---

## 2. Performance

### Bildoptimierung
| Aspekt | Status | Detail |
|---|---|---|
| **WebP** | Teilweise | Einige neuere Bilder (z.B. `Titelbilder-Homepage-KORODUR8-square.webp` von 2025/03) nutzen WebP |
| **AVIF** | Nicht vorhanden | Kein einziges AVIF-Bild gefunden |
| **PNG** | Haeufig | Viele Produktbilder und Kategoriebilder als PNG (z.B. 600x600px) |
| **JPG** | Haeufig | Referenzbilder als JPG, teils sehr gross (2560x1920px!) |
| **SVG** | Logo | Footer-Logo als SVG (`korodur-logo-white.svg`) |

**Kritisch:** Referenzbilder werden mit Originalaufloesungen bis 2560x2560px in srcsets ausgeliefert. Kein serverseitiges Resizing erkennbar.

### Lazy Loading
| Methode | Status |
|---|---|
| **WP-Optimize Lazy Load** | Aktiv -- Verwendet `data-src` / `data-srcset` mit Platzhalter-GIF (`R0lGODlhAQABAAAAACH5BAEK...`) |
| **Native `loading="lazy"`** | Inkonsistent -- Einige Bilder haben `loading="lazy"`, viele aber `loading="eager"` trotz data-src Pattern |
| **Elementor Lazy Background** | Aktiv (`e-lazyloaded` IntersectionObserver) |

**Problem:** Widerspruch zwischen `loading="eager"` und `data-src` Lazy-Load-Pattern bei den meisten Homepage-Bildern. Browser laden das Platzhalter-GIF sofort, dann muss JS das echte Bild nachladen -- doppelter Request-Overhead.

### JavaScript-Bundles
Erkannte JS-Dateien auf der Homepage (nicht vollstaendig):
- jQuery Core + jQuery Migrate (Legacy!)
- WP-Optimize Minified Bundles (6+ Dateien)
- Elementor Runtime + Frontend + Modules
- Elementor Pro Runtime + Frontend + Elements Handlers
- WooCommerce (add-to-cart, js-cookie, order-attribution, sourcebuster)
- Jet Engine + Jet Search + Jet Smart Filters
- Premium Addons for Elementor
- Pafe (Pro Addons) -- mind. 3 separate Bundles
- Complianz Cookie Banner
- Swiper.js + jQuery Numerator
- Slick Carousel (via Custom JS)
- Cloudflare Script Manager

**Schaetzung:** 30+ JavaScript-Dateien, auch nach Minification. jQuery-Abhaengigkeit in 2026 ist technische Schuld. WooCommerce-JS wird auf jeder Seite geladen, obwohl kein echtes Shopping stattfindet.

### CSS-Bundles
- WP-Optimize minifiziert CSS in 3+ Header-Dateien + 1 Footer-Datei
- Elementor generiert zusaetzliches Inline-CSS (WordPress Global Styles: ~500 Zeilen!)
- Simple Custom CSS and JS: mindestens 3 Custom-CSS-Bloecke inline

### Mobile
- Viewport korrekt: `<meta name="viewport" content="width=device-width, initial-scale=1">`
- Responsive Breakpoints via Elementor: Mobile (767px), Tablet (1024px)
- Astra Theme Breakpoint: 921px
- Custom CSS fuer < 767px und < 1385px vorhanden

### Cloudflare-Rocket-Loader
Script-Tags nutzen Cloudflare Rocket Loader (`type="34e5944399bf82310b984e75-text/javascript"` / `type="0bdcfac89a3ecfbc693637fe-text/javascript"`). Dieser modifiziert das Script-Loading-Verhalten.

---

## 3. SEO

### Homepage DE
| Tag | Inhalt | Bewertung |
|---|---|---|
| **Title** | "Bodenbelaege fuer Industrie und Gewerbe - Korodur" | OK, 52 Zeichen |
| **Meta Description** | "KORODUR ist der Spezialist fuer die Herstellung von Baustoffen fuer hochbelastbare Industrieboeden. In Neubau und Sanierung. Mit 90 Jahren und 750 Mio. Quadratmetern Erfahrung." | OK, 176 Zeichen (etwas lang) |
| **Canonical** | `https://www.korodur.de/` | Korrekt |
| **OG:Title** | Identisch mit Title | OK |
| **OG:Description** | Identisch mit Meta Description | OK |
| **OG:Image** | **FEHLT** | Schwerer Fehler -- Social Sharing ohne Vorschaubild |
| **OG:Locale** | `de_DE` | OK |
| **Twitter:Card** | `summary_large_image` | OK, aber kein Bild definiert |
| **H1** | **FEHLT** | Kritischer SEO-Fehler |
| **H2** | 5x `premium-title-header` (Inhalt nicht im HTML sichtbar -- JS-gerendert?) + Footer: "Kontakt", "Wichtige Links", "Social Media" | Schwach -- Footer-H2s verwässern Heading-Hierarchie |

### Homepage EN
| Tag | Inhalt | Bewertung |
|---|---|---|
| **Title** | "Homepage -- korodur" | SCHLECHT -- generischer WP-Fallback, kein SEO-Wert |
| **Meta Description** | Vorhanden, englisch uebersetzt | OK |
| **Canonical** | `https://www.korodur.de/en/` | OK |
| **OG:Image** | **FEHLT** | Wie DE |
| **H1** | **FEHLT** | Wie DE |

### Hreflang-Implementierung
| Methode | Status |
|---|---|
| **HTML `<link rel="alternate" hreflang="...">`** | NICHT VORHANDEN im `<head>` |
| **Sitemap hreflang** | Korrekt implementiert (de, en, fr, x-default) |
| **WPML Language Switcher** | Vorhanden als `<a hreflang="...">` im Body -- zaehlt NICHT als hreflang fuer Suchmaschinen |

**Problem:** Google akzeptiert Sitemap-hreflang, aber Best Practice ist die Implementierung im HTML-Head. Die fehlenden `<link>` Tags im Head sind ein Konfigurationsfehler in WPML/Yoast. Dies kann zu falscher Sprachzuordnung fuehren.

### Schema.org / Structured Data
Implementiert via Yoast SEO JSON-LD:
- `WebPage` -- korrekt
- `BreadcrumbList` -- **FEHLERHAFT**: Breadcrumb-Name ist "Maison" (franzoesisch!) auf der DE-Seite
- `WebSite` -- mit SearchAction (Sitelinks-Suchfeld)
- `Organization` -- Name "Korodur", Logo, sameAs (Facebook, X/Twitter)

**Fehlend:**
- Kein `Product`-Schema auf Produktseiten (WooCommerce sollte das liefern)
- Kein `LocalBusiness` oder `CorporateContact`
- Kein `FAQ`-Schema
- Kein `Review`/`AggregateRating`

### Stichprobe Unterseiten

| Seite | Title | H1 | Meta Description | Canonical |
|---|---|---|---|---|
| `/en/products/` | "Products -- korodur" | "PRODUCT CATEGORIES" | FEHLT | OK |
| `/shop/` | "Produkte Archive -- korodur" | Leer (`<h1>...</h1>` ohne Text) | FEHLT | OK |
| `/referenzen/` | "Referenzen Archive -- korodur" | "Referenzen" | FEHLT | OK |
| `/produkt/goodcat-silver-classic/` | `goodcat "silver classic" -- korodur` | Produktname | FEHLT | OK |

**Muster:** Meta Descriptions fehlen auf fast allen Unterseiten. Titles folgen dem schwachen "Seitenname -- korodur" Muster ohne Keywords.

### Interne Verlinkung
- **Produkte erreichbar ueber:** Hauptnavigation > Produkte > Kategorie > Produkt (3 Klicks)
- **Alternative:** Bereiche > Produktbereich > Produkte (3-4 Klicks)
- **Doppelstruktur:** `/bereiche/industrieboden/` (Content-Seite) vs. `/produkt-kategorie/industrieboden/` (WooCommerce-Kategorie) -- verwirrend fuer User und Suchmaschinen
- **Referenzen:** Direkt ueber Hauptnavigation oder Homepage-Listing

---

## 4. URL-Struktur & Mehrsprachigkeit

### Sprachpfade
| Sprache | Pfad | Beispiel |
|---|---|---|
| Deutsch (Standard) | `/` (kein Praefix) | `korodur.de/bereiche/industrieboden/` |
| Englisch | `/en/` | `korodur.de/en/areas/industrial-floor/` |
| Franzoesisch | `/fr/` | `korodur.de/fr/domaines/sols-industriels/` |

**x-default** zeigt auf DE (korrekt als Hauptsprache).

### URL-Muster nach Seitentyp
| Typ | DE | EN | FR |
|---|---|---|---|
| Bereiche | `/bereiche/` | `/en/areas/` | `/fr/domaines/` |
| Produkte (WC) | `/produkt/` | `/en/product/` | `/fr/produkt/` |
| Produktkategorien | `/produkt-kategorie/` | `/en/product-category/` | `/fr/categorie-produit/` |
| Referenzen | `/referenzen/` | `/en/references/` | `/fr/references/` |
| Unternehmen | `/unternehmen/` | `/en/company/` | `/fr/entreprise/` |
| Shop | `/shop/` | `/en/shop/` | `/fr/shop/` |
| Kontakt | `/kontakt/` | `/en/contact/` | `/fr/contact/` |
| News | `/aktuelles/` | `/en/news/` | `/fr/nouvelles/` |

### Auffaelligkeiten & Probleme
1. **Doppelte Produktstruktur:** `/bereiche/industrieboden/` (Content) und `/produkt-kategorie/industrieboden/` (WooCommerce) fuehren zu Kannibalisierung
2. **Inkonsistente EN-Slugs:** `/en/product-category/hartstoffschicht-en/` -- deutsche Begriffe mit `-en` Suffix statt Uebersetzung
3. **Inkonsistente FR-Slugs:** `/fr/produkt/` statt `/fr/produit/` bei einigen Produkten
4. **"shop" statt "produkte":** Der WooCommerce-Shop-Slug `/shop/` ist nicht markenueblich fuer einen B2B-Katalog
5. **Schnellestrich-Systeme-2:** URL-Slug `schnellestrich-systeme-2` deutet auf Duplikat/Neumigration hin
6. **"bauarbeiten-im-gange":** Offenbar eine Platzhalter-Seite ("Bauarbeiten im Gange"), die in der Sitemap indexiert ist
7. **News-Inkonsistenz:** DE `/aktuelles/` vs. DE-Hreflang in Sitemap `/news/` -- verschiedene URLs fuer gleichen Inhalt
8. **"dattenblaetter":** Tippfehler im URL-Slug `/service/dattenblaetter/` (statt "datenblaetter")

---

## 5. Seitentypen-Inventar

| Seitentyp | Beispiel-URL (DE) | Geschaetzte Anzahl | Mehrsprachig |
|---|---|---|---|
| **Homepage** | `/` | 1 | DE/EN/FR |
| **Bereichsuebersicht** | `/bereiche/` | 1 | DE/EN/FR |
| **Bereichsseiten** | `/bereiche/industrieboden/` | ~8 | DE/EN/FR |
| **Bereich-Unterseiten** | `/bereiche/industrieboden/hartstoffschicht/` | ~25 | Teilweise |
| **Produktuebersicht** | `/produkte/` bzw. `/shop/` | 2 (Duplikat!) | DE/EN/FR |
| **Produktkategorien** | `/produkt-kategorie/industrieboden/` | ~15 | DE/EN/FR |
| **Produktdetailseiten** | `/produkt/goodcat-silver-classic/` | ~70 | Teilweise |
| **Referenzen-Uebersicht** | `/referenzen/` | 1 | DE/EN/FR |
| **Referenz-Einzelseiten** | `/referenzen/produktionsstaette-fiorini/` | ~130 | Teilweise |
| **Unternehmensseiten** | `/unternehmen/`, `/unternehmen/geschichte/` | ~6 | DE/EN/FR |
| **Service-Seiten** | `/service/`, `/service/leistungserklaerungen/` | ~8 | Teilweise |
| **Kontaktseiten** | `/kontakt/`, `/kontakt/deutschland/` | ~3 | DE/EN/FR |
| **News/Blog** | `/aktuelles/`, `/korodur-goes-green/` | ~5 | Teilweise |
| **Rechtliches** | `/impressum/`, `/datenschutz/`, `/agb/` | 3 | Teilweise |
| **Sonstige** | `/hinweisgebersystem/`, `/bauarbeiten-im-gange/` | ~3 | Nein |

**Gesamt geschaetzt:** ~280 einzigartige Inhaltsseiten (ohne Sprachvarianten), ~858 URLs inkl. Sprachvarianten.

### Zielgruppen-Relevanz der Seitentypen

| Seitentyp | Planer/Architekten | Verarbeiter | Handel |
|---|---|---|---|
| Produktdetailseiten | Hoch (TDS, Normen) | Hoch (Verarbeitung) | Hoch (Sortiment) |
| Bereichsseiten | Hoch (Loesungsfindung) | Mittel | Mittel |
| Referenzen | Hoch (Nachweise) | Hoch (Anwendungen) | Mittel |
| Service (LV, TDS, DoP) | Sehr hoch | Hoch | Niedrig |
| Kontakt | Mittel | Mittel | Hoch |

---

## 6. Datenschutz & Tracking

### Cookie-Consent
- **Tool:** Complianz GDPR v7.4.5
- **Modus:** Opt-in (EU-Konfiguration, DSGVO-konform)
- **Kategorien:** Functional (immer aktiv), Preferences, Statistics, Marketing
- **Banner:** Deutsch ("Akzeptieren", "Ablehnen", "Einstellungen anzeigen")
- **Links:** Cookie-Richtlinie -> `/datenschutz/`, Impressum -> `/impressum/`
- **TCF:** Referenz vorhanden (`tcf cookie-statement`), Status unklar

### Analytics & Tracking
| Tool | Status | Integration |
|---|---|---|
| **Google Analytics / GA4** | NICHT ERKANNT | Kein `gtag.js`, kein `analytics.js`, kein `gtm.js` im HTML |
| **Google Tag Manager** | NICHT ERKANNT | Kein GTM-Container gefunden |
| **Matomo** | NICHT ERKANNT | |
| **Pressebox Tracking** | AKTIV | Custom Script via Simple Custom CSS/JS, Kategorie "statistics", Service "pressebox-de" |
| **WooCommerce Order Attribution** | AKTIV | Sourcebuster.js + Order Attribution (UTM-Tracking, Session-Tracking) |

**Kritisch:** Es scheint KEIN Standard-Analytics-Tool (GA4, Matomo o.ae.) aktiv zu sein. Lediglich Pressebox-Tracking und WooCommerce-internes Tracking. Das bedeutet: **Es gibt wahrscheinlich keine belastbaren Traffic-Daten** fuer die aktuelle Website, die als Baseline fuer den Relaunch dienen koennten.

### DSGVO-Einschaetzung
| Aspekt | Status |
|---|---|
| Cookie-Consent | OK (Complianz, Opt-in) |
| Impressum vorhanden | Ja |
| Datenschutzerklaerung vorhanden | Ja |
| Hinweisgebersystem | Ja (`/hinweisgebersystem/`) -- HinSchG-konform |
| Analytics-Consent | OK (Pressebox hinter Consent) |
| Drittanbieter-Einbindungen | Cloudflare (CDN) -- DSGVO-relevant, aber ueblich |

---

## Bewertungsmatrix

| Bereich | Status | Prioritaet | Kommentar |
|---|---|---|---|
| **Server & Hosting** | Gelb | Mittel | Cloudflare gut, aber Plesk-Backend und fehlende Cache-Strategie |
| **CMS-Stack** | Rot | Hoch | 14+ Plugins, WooCommerce-Overhead, jQuery-Abhaengigkeit |
| **Performance** | Rot | Hoch | 30+ JS-Dateien, inkonsistentes Lazy Loading, grosse Bilder |
| **SEO: Meta-Tags** | Rot | Hoch | Fehlende H1s, schwache Titles, keine Meta Descriptions auf Unterseiten |
| **SEO: Hreflang** | Gelb | Hoch | Sitemap OK, HTML-Head fehlt |
| **SEO: Schema.org** | Gelb | Mittel | Basis vorhanden, Breadcrumb-Bug, kein Product-Schema |
| **URL-Struktur** | Rot | Hoch | Doppelstruktur, inkonsistente Slugs, Tippfehler |
| **Mehrsprachigkeit** | Gelb | Mittel | WPML funktional, aber inkonsistente Uebersetzung der Slugs |
| **Bildoptimierung** | Gelb | Mittel | WebP teilweise, kein AVIF, grosse Originalbilder |
| **Content** | Gelb | Mittel | Blog vernachlaessigt, H2-Texte teils nur per JS sichtbar |
| **Datenschutz** | Gruen | Niedrig | Complianz korrekt konfiguriert |
| **Analytics** | Rot | Hoch | Kein Standard-Analytics -- keine Daten fuer Relaunch-Baseline |

---

## Empfehlungen fuer Phase 3 (Konzept)

### Prio 1 -- Muss beim Neuaufbau adressiert werden

1. **Analytics sofort einrichten** (noch vor Relaunch-Beginn)
   - GA4 oder Matomo auf der bestehenden Seite installieren
   - Mindestens 3 Monate Baseline-Daten sammeln
   - Ohne Traffic-Daten ist keine datengetriebene Priorisierung der neuen Seiten moeglich

2. **Informationsarchitektur vereinfachen**
   - Doppelstruktur `/bereiche/` vs. `/produkt-kategorie/` aufloesen
   - Klare Hierarchie: Produktbereich > Produktkategorie > Produkt
   - Zielgruppenspezifische Einstiege (Planer, Verarbeiter, Handel)

3. **SEO-Grundlagen bei Migration sicherstellen**
   - H1 auf jeder Seite (genau einer)
   - Individuelle Meta Descriptions fuer alle Seiten
   - Hreflang im HTML-Head UND in der Sitemap
   - 301-Redirects fuer alle alten URLs planen (858 URLs!)

4. **Tech-Stack entschlacken**
   - WooCommerce durch leichtgewichtigen Custom Post Type ersetzen (oder headless CMS)
   - jQuery-Abhaengigkeit eliminieren
   - Elementor durch performanteres System ersetzen (oder Gutenberg nutzen)
   - Ziel: unter 10 JS-Dateien, unter 500 KB Total JS

### Prio 2 -- Sollte beim Neuaufbau adressiert werden

5. **Bildstrategie definieren**
   - WebP als Standard, AVIF als Progressive Enhancement
   - Maximale Bildgroesse definieren (z.B. 1200px breit fuer Content)
   - Responsive Images mit korrekten `sizes`-Attributen
   - Konsistente Lazy-Loading-Strategie

6. **URL-Slugs bereinigen**
   - Alle Sprachen konsistent uebersetzen
   - Tippfehler korrigieren
   - Sprechende, keyword-relevante URLs

7. **Schema.org erweitern**
   - Product-Schema auf Produktseiten
   - Organization mit vollstaendigen Kontaktdaten
   - FAQ-Schema wo sinnvoll
   - BreadcrumbList korrekt in allen Sprachen

8. **Service-Bereich fuer Planer/Verarbeiter ausbauen**
   - Ausschreibungstexte leicht auffindbar
   - Technische Datenblaetter als strukturierte Downloads
   - Leistungserklaerungen (DoP) systematisch verlinkt

### Prio 3 -- Nice-to-have

9. **Content-Strategie fuer Blog/News**
   - Regelmaessige Veroeffentlichung (Referenzen, Fachbeitraege)
   - Integration in Hauptnavigation

10. **Suche verbessern**
    - Produktfilter nach technischen Eigenschaften
    - Facettierte Suche fuer den Produktkatalog

---

## Anhang: Technische Details

### Pressebox-Tracking-Code
```javascript
// Via Simple Custom CSS/JS, data-service="pressebox-de", data-category="statistics"
// Token: a6158fed-bfae-564b-9f75-bfa2239c8262
```

### Schema.org Breadcrumb-Bug (Homepage DE)
```json
{
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Maison"  // <-- Franzoesisch statt Deutsch!
    }
  ]
}
```

### Elementor-Version & Features
```
Version: 3.35.7
Active Features: theme_builder_v2, global_classes, e_variables, cloud-library,
                 e_components, e_interactions, e_editor_one, import-export-customization
Breakpoints: Mobile (767px), Tablet (1024px)
```

### WooCommerce-Konfiguration
```
Shop-URL: /shop/ (DE) | /en/shop/ (EN) | /fr/shop/ (FR)
Cart-Redirect: Nein
WC-AJAX: /?wc-ajax=%%endpoint%%
Sprach-Cookie: wp-wpml_current_language
```
