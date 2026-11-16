# Homepage-Entwurf Queens 45 BC (Divi)

Entwurf einer neuen Startseite für queens45.de auf Basis des Divi-Themes. Texte, Farben, Schriften und Bilder stammen von der bestehenden Seite.

## Dateien

| Datei | Zweck |
|---|---|
| `index.html` | Eigenständige Vorschau zum Öffnen im Browser, mit Kopf, Fuß, SEO-Tags und JSON-LD. Bilder aus `bilder/`. |
| `divi-code-modul.html` | Nur der Seiteninhalt (8 Sektionen) plus `<style>`, zum Einfügen in ein Divi-Code-Modul. Bilder verweisen auf die bestehende Mediathek (`https://queens45.de/wp-content/uploads/2026/10/…`). |
| `bilder/` | Verkleinerte WebP-Fassungen der Fotos (50–150 KB statt 110–550 KB) und das Logo. |

Es gibt **keine Divi-Import-Datei (JSON)**. Das Exportformat von Divi 5 ließ sich nicht an echten Daten prüfen, deshalb wurde keine erzeugt.

## Weg A: Schnell einfügen (Code-Modul)

1. Seite in WordPress anlegen oder die Startseite duplizieren, mit dem Divi-Builder öffnen.
2. Eine Sektion anlegen, Innenabstand oben und unten auf `0`.
3. Darin eine Zeile mit einer Spalte: Breite `100 %`, maximale Breite `keine`, Innenabstand `0`.
4. Modul „Code“ einfügen und den gesamten Inhalt von `divi-code-modul.html` hineinkopieren.
5. Vorschau prüfen, dann veröffentlichen.

Nachteil: Der Inhalt lässt sich danach nur im HTML ändern, nicht per Klick im Builder.

## Weg B: Im Builder nachbauen (empfohlen)

Das HTML folgt der Divi-Struktur Sektion → Zeile → Spalte → Modul und nutzt die Klassen, die Divi 5.18 auf der Live-Seite ausgibt (`et_pb_section`, `et_pb_row`, `et_pb_column_1_2`, `et_pb_text`, `et_pb_heading`, `et_pb_button`, `et_pb_image`, `et_pb_blurb`). Über jeder Sektion steht ein Kommentar mit Modultypen und Spaltenlayout:

| Nr. | Sektion | Spalten | Module |
|---|---|---|---|
| 1 | Hero | 4_4 | Text, Überschrift (H1), Text, Button |
| 2 | Anlässe | 1_2 + 1_2 | Bild / Text, Überschrift, Text, Button |
| 3 | Hochzeit | 1_2 + 1_2 | Text, Überschrift, Text, Button / Bild |
| 4 | Räume | 4_4, dann 1_3 × 3, dann 4_4 | Überschrift / je Bild, Überschrift (H3), Text, Button / Text mit Tabelle |
| 5 | Ausstattung | 4_4, dann 1_2 + 1_2 | Überschrift / je Blurb, Button |
| 6 | Geschichte | 1_2 + 1_2 | Bild / Text, Überschrift, Text |
| 7 | Anfrage | 4_4 | Überschrift, Text, Button |
| 8 | Kontakt | 1_3 × 3 | je Blurb |

Das CSS aus dem `<style>`-Block gehört dann nach Divi → Theme-Optionen → Benutzerdefiniertes CSS. Alle Regeln beginnen mit `.q45`; diese Klasse der Seite oder den Sektionen als CSS-Klasse geben (Erweitert → CSS-ID & Klassen). Die eigenen Klassen (`q45-hero`, `q45-rahmen`, `q45-raum` …) an den jeweiligen Modulen eintragen.

## Farben und Schriften

Übernommen aus den Divi Global Colors und Button-Presets der Live-Seite:

| Rolle | Wert | Herkunft |
|---|---|---|
| Primär (Dunkelrot) | `#680909` | Divi Global Color „primary“ |
| Sekundär (Gold) | `#e09900` | Divi Global Color „secondary“ |
| Button | `#780000` | Button-Preset der Live-Seite |
| Button Hero | `#c1121f` | Button-Preset der Live-Seite |
| Dunkel | `#0e0c19` | Flächenton der Live-Seite |
| Text | `#0a0a0a` | Divi Global Color „heading“ |
| Heller Grund | `#f7f1f0` | aufgehellter Ton aus dem Logo (`#e6d4d3`) |

Schriften: Cormorant Garamond (Überschriften), Proza Libre (Text), beide bereits im Theme eingebunden.

## Wohin mit Title, Meta-Description, Open Graph und JSON-LD?

Diese Angaben stehen nur in `index.html`, nicht im Code-Modul.

- **Title und Meta-Description:** im SEO-Plugin (Rank Math oder Yoast) an der Startseite eintragen.
  - Title: `Eventlocation Berlin-Charlottenburg im 20er-Stil | Queens 45 BC`
  - Description: `Eventlocation in Berlin-Charlottenburg im Stil der Goldenen 20er: Ballsaal für bis zu 300 Gäste, Champagner-Bar & Salon. Jetzt unverbindlich anfragen.`
- **Open Graph:** erzeugt das SEO-Plugin automatisch; dort nur das Vorschaubild wählen.
- **JSON-LD (`EventVenue`):** entweder über das Schema-Modul des SEO-Plugins oder den `<script type="application/ld+json">`-Block aus `index.html` in Divi → Theme-Optionen → Integration → „Code in den `<head>` einfügen“ kopieren.

## Vor dem Livegang prüfen

- **Foto Champagner-Bar:** Das Bild mit den grünen Stühlen ist auf der Live-Seite der Champagner-Bar zugeordnet und wurde so übernommen. Es könnte den Grünen Salon zeigen. Bitte prüfen.
- **Fotonachweis:** Dasselbe Bild trägt das Wasserzeichen eines Hochzeitsfotografen. Nutzungsrecht klären.
- **Grüner Salon & Destille:** Kein Foto vorhanden, deshalb ein Platzhalter „Foto folgt“ (auf der Live-Seite fehlt es ebenfalls).
- **Großer Saal, Steh-Sitz-Kombination:** Auf der Website steht keine Zahl, in der Tabelle steht „auf Anfrage“.
- **Buttons:** Es gibt noch keine eigenen Raumseiten. „Großen Saal entdecken“ führt zur Hochzeitsseite, die übrigen Raum- und Ausstattungs-Buttons zum Anfrage-Bereich, die Anfrage-Buttons zur Kontaktseite.
- **Links:** Sie zeigen auf die heutigen Adressen (`?page_id=141`, `?page_id=183`, `?page_id=128`). Nach der Umstellung der Permalinks anpassen.
