# SEO-Audit queens45.de

Stand: 16.11.2026 · Geprüft: Live-Seite (HTML, Header, Bilder, Sitemap, alle 4 Unterseiten)

**Datenlage:** Suchvolumen, Rankings und Backlinks fehlen, weil kein SEO-Tool (Ahrefs, Similarweb) verbunden war. Alle Angaben zu Keyword-Schwierigkeit und Wettbewerb sind Schätzungen.

## Zusammenfassung

- WordPress 7.1 mit Divi 5, PHP 8.4, nginx/Plesk. Neue Seite (Uploads von 10/2026).
- Umfang: Startseite, Hochzeitsseite, Kontakt, Impressum.
- Bei einer `site:queens45.de`-Suche erscheint keine Seite. Die Domain ist wahrscheinlich noch nicht indexiert; verbindlich klärt das die Google Search Console.
- **Stärke:** gute Texte mit konkreten Fakten (300 Gäste, 9,60 m Deckenhöhe, ca. 200 m², Charlottenburg).
- **Gesamturteil:** ordentliche Inhalte, technische Basis mit kritischen Fehlern.

**Top 3 Prioritäten**

1. Permalinks, robots.txt und Sitemap reparieren.
2. Startseite auf „Eventlocation Berlin“ ausrichten (Title, Meta-Description).
3. Eigene Seiten für Räume und Anlässe anlegen; die Buttons dafür haben derzeit kein Linkziel.

## Technische Checkliste

| Check | Status | Details |
|---|---|---|
| URL-Struktur | Fail | URLs wie `?page_id=141` statt `/hochzeitslocation-berlin/` |
| robots.txt | Fail | 404 (Plesk-Fehlerseite); nginx reicht die Anfrage nicht an WordPress weiter |
| XML-Sitemap | Warning | `/wp-sitemap.xml` liefert 404; Sitemap nur unter `/?sitemap=index` erreichbar |
| HTTPS / HSTS | Pass | Kein Mixed Content; `www` leitet per 301 um |
| Canonical | Pass | Überall gesetzt; doppelte Startseite (`page_id=149`) zeigt auf `/` |
| Indexierung | Warning | Kein `noindex`, aber vermutlich noch nicht im Index |
| Strukturierte Daten | Fail | Kein JSON-LD (`EventVenue`, `LocalBusiness`, `FAQPage` fehlen) |
| Open Graph | Fail | Fehlt komplett |
| Ladezeit | Warning | 1,4 s bis zum ersten Byte; JPEGs mit 220–550 KB statt WebP; 26 Scripts |
| Mobil | Warning | Zoomen verboten (`user-scalable=0`) |
| Sicherheit | Warning | `xmlrpc.php` offen erreichbar |

## On-Page-Probleme

| Seite | Problem | Schwere | Fix |
|---|---|---|---|
| Startseite | Meta-Description leer | Kritisch | „Eventlocation in Berlin-Charlottenburg im Stil der Goldenen 20er: Ballsaal für bis zu 300 Gäste, Champagner-Bar & Salon. Jetzt unverbindlich anfragen.“ |
| Startseite | Title „Feiern in den 20er Jahren \| Queens45“ ohne „Eventlocation“ und „Berlin“ | Hoch | „Eventlocation Berlin-Charlottenburg im 20er-Stil \| Queens 45 BC“ |
| Startseite | 3 Buttons ohne Link („Großen Saal entdecken“, „Champagner-Bar ansehen“, „Hochzeitslocation entdecken“) | Hoch | Links setzen, Raumseiten anlegen |
| Startseite | 5 von 6 Bildern ohne Alt-Text | Mittel | z. B. „Großer Saal mit Kronleuchtern, Queens 45 BC Berlin“ |
| Hochzeit | 2 H1 | Mittel | Eine zu H2 machen |
| Hochzeit | Meta-Description ist abgeschnittener Auszug (über 300 Zeichen) | Mittel | Eigene Beschreibung mit 150–160 Zeichen |
| Hochzeit | 3 von 4 Bildern ohne Alt-Text | Mittel | Alt-Texte ergänzen |
| Alle | Titles „X \| Feiern in den 20er Jahren“ ohne Markennamen | Mittel | Schema „Thema \| Queens 45 BC“ |
| Kontakt | Keine H1, 48 Wörter, duzt (Rest siezt) | Mittel | H1, Anfahrt, Adresse, Karte; einheitlich siezen |
| Impressum | Keine H1 | Niedrig | H1 setzen |

## Keyword-Chancen (geschätzt)

| Keyword | Schwierigkeit | Chance | Intent | Zielseite |
|---|---|---|---|---|
| eventlocation berlin charlottenburg | mittel | hoch | transaktional | Startseite |
| hochzeitslocation berlin charlottenburg | mittel | hoch | transaktional | Hochzeit |
| 20er jahre party location berlin | leicht | hoch | transaktional | neue Seite „Motto-Feiern“ |
| ballsaal mieten berlin | mittel | hoch | transaktional | Großer Saal |
| ballhaus berlin hochzeit | mittel | hoch | kommerziell | Hochzeit |
| weihnachtsfeier location berlin | schwer | hoch (saisonal) | transaktional | neue Seite „Firmenfeier“ |
| firmenfeier location berlin 300 personen | mittel | hoch | transaktional | Firmenfeier |
| location für 100 personen berlin | mittel | mittel | transaktional | Champagner-Bar |
| art deco location berlin | leicht | mittel | kommerziell | Champagner-Bar |
| tagungsraum berlin charlottenburg | mittel | mittel | transaktional | neue Seite „Tagung“ |
| geburtstag location berlin 50 personen | mittel | mittel | transaktional | Grüner Salon / Destille |
| great gatsby party berlin | leicht | mittel | informational | Motto-Feiern / Blog |
| hochzeitslocation berlin kosten | mittel | mittel | kommerziell | FAQ Hochzeitsseite |
| was kostet eine eventlocation in berlin | leicht | mittel | informational | Ratgeber |
| eventlocation berlin | sehr schwer | niedrig (kurzfristig) | transaktional | erst nach Linkaufbau |

## Inhaltslücken

| Thema | Format | Priorität | Aufwand |
|---|---|---|---|
| Eine Seite pro Raum (Großer Saal, Champagner-Bar, Grüner Salon & Destille) | Landingpage | hoch | je ½ Tag |
| Firmenfeier / Weihnachtsfeier | Landingpage | hoch | ½ Tag |
| Tagung & Konferenz | Landingpage | hoch | ½ Tag |
| Geburtstag / Motto-Party 20er Jahre | Landingpage | mittel | ½ Tag |
| Galerie mit gut benannten Bildern | Galerie | mittel | 2 h |
| Anfahrt, Parken, ÖPNV | Kontaktseite | mittel | 1 h |
| Preise / Pakete („ab“-Preise) | Seite oder FAQ | mittel | offen |

## Wettbewerb

Keine Daten ohne SEO-Tool. Vermutlich konkurrieren andere Berliner Ballhaus- und Eventlocations sowie Vermittlungsportale, die generische Suchen dominieren. Local SEO (Google-Unternehmensprofil, Bewertungen, Portaleinträge) ist deshalb wichtiger als der Kampf um große Suchbegriffe. Ein ProvenExpert-Profil „Queens 45 BC“ existiert: https://www.provenexpert.com/queens-45-bc/

## Maßnahmenplan

**Quick Wins (diese Woche)**

1. Permalinks auf „Beitragsname“ umstellen. In Plesk unter „Apache & nginx“ eintragen: `location / { try_files $uri $uri/ /index.php?$args; }`. Danach `/robots.txt` und `/wp-sitemap.xml` testen. (30 min, Wirkung hoch)
2. Google Search Console einrichten, Sitemap einreichen, Indexierung beantragen. (30 min, hoch)
3. SEO-Plugin (Rank Math oder Yoast): Title, Meta-Description, Open Graph, `LocalBusiness`-Schema. (2 h, hoch)
4. Tote Buttons verlinken, Alt-Texte ergänzen, doppelte H1 und `user-scalable=0` entfernen. (1 h, mittel)
5. Bilder nach WebP konvertieren, Caching-Plugin aktivieren. (1 h, mittel)

**Strategisch (dieses Quartal)**

1. Raum- und Anlass-Seiten aufbauen. (3–4 Tage, hoch; setzt Quick Win 1 voraus)
2. Google-Unternehmensprofil („Veranstaltungsort“), Fotos, Bewertungen. (laufend, hoch)
3. Einträge in Location- und Hochzeitsportalen mit identischem Namen, Adresse, Telefon. (1–2 Tage, hoch)
4. Weihnachtsfeier-Seite spätestens im Juli live stellen.
