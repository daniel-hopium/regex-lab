# Regex-Werkstatt – Reguläre Ausdrücke zum Anfassen

Reguläre Ausdrücke Baustein für Baustein: Jedes Muster läuft live gegen echten Text, Treffer und Gruppen werden markiert, jeder Baustein wird in Worten erklärt. Ein Schritt-Modus zeigt, wie die Backtracking-Engine sucht und zurückgeht. Dazu Übungen mit sofortiger Prüfung, Rezepte für den Alltag und die Fallen, die in Produktion wehtun.

46 Einträge in 11 Kapiteln, auf Deutsch und Englisch.

Online: https://daniel-hopium.github.io/regex-lab/

## Starten

`index.html` im Browser öffnen, per Doppelklick. Kein Build, kein Server, keine
Abhängigkeiten. Internet braucht es nur für die Google-Schriften.

## Inhalt

| Kapitel | Einträge |
|---|---|
| Werkstatt | Spielwiese & Spickzettel, Wie die Engine sucht |
| Grundlagen | Text und Sonderzeichen, Der Punkt, Zeichenklassen, Kurzschreibweisen, Anker, Alternativen |
| Quantoren | Wie oft?, Gierig oder genügsam, Gruppen wiederholen |
| Gruppen & Ersetzen | Gruppen herausziehen, Benannte Gruppen, Gruppen ohne Speichern, Rückverweise, Ersetzen mit Mustern |
| Lookarounds | Lookahead, Lookbehind, Mehrere Bedingungen, Tausenderpunkte |
| Flags | Alle Flags im Vergleich, Die lastIndex-Falle, Sticky: Schritt für Schritt lesen, Positionen der Gruppen |
| Regex in JavaScript | Die Methoden, replace mit Funktion, split, Regex aus Nutzereingaben |
| Unicode & Umlaute | Umlaute und andere Schriften, Emojis und das u-Flag, Groß, klein und ß |
| Rezepte | E-Mail-Adresse, Datum, Zahlen im deutschen Format, IBAN, PLZ, Telefon, Links aus Text ziehen, Logzeilen zerlegen, Text aufräumen, Regex in Angular-Formularen, CSV mit Anführungszeichen |
| Fallen & Performance | Katastrophales Backtracking, HTML mit Regex parsen, Wann keine Regex? |
| Übungen | Einsteiger, Fortgeschritten, Profi |

Jeder Eintrag hat eine eigene Adresse (`#kapitel/eintrag`), die meisten eine Stolperfalle
oder einen Merksatz und Links zu MDN oder der passenden Doku. Der Überblick hat eine
durchsuchbare Tabelle aller Einträge.

## So funktioniert es

- **Tester im Web Worker:** Gematcht wird in einem Worker mit 1,5 s Zeitlimit. Ein katastrophales Muster friert so nur den Worker ein, nicht die Seite.
- **Erklärer:** Ein eigener Parser zerlegt das Muster in Bausteine (Klassen, Quantoren, Gruppen, Lookarounds, Unicode-Eigenschaften) und beschreibt jeden einzeln.
- **Schritt-Modus:** Eine kleine Backtracking-Engine protokolliert jeden Versuch – so sieht man, warum `<.+>` zu viel nimmt und `(a+)+b` explodiert.
- **Übungen:** 17 Aufgaben in drei Stufen; gelöste Aufgaben merkt sich der Browser.

## Bedienung

- **Sprache:** Der Link oben rechts („English“ / „Deutsch“) wechselt die Sprache. Sie steht
  als `?lang=en` in der Adresse (teilbar), wird im `localStorage` gemerkt und folgt sonst der
  Browsersprache.
- `Strg+K` (Mac: `Cmd+K`) springt in die Suche der Seitenleiste.
- Hell und dunkel folgen der Systemeinstellung; der Sonne/Mond-Knopf überschreibt sie.
- Ab 1280px Breite schaltet der Breite-Knopf die breite Ansicht ein; dort lässt sich die
  Lektion am Griff rechts schmaler oder breiter ziehen.

## Aufbau

Alles steckt in einer Datei, `index.html`:

- **Hülle:** Kopfleiste, Seitenleiste mit Suche, Router, Sprache, Theme und Breite – dieselbe
  wie in den Schwester-Apps.
- **`CATS` und `ENTRIES`:** die Kapitel und ein Objekt pro Eintrag mit Text (`desc`, `tip`,
  `rule`, `links`) und einer Demo-Art (`kind`): `run` (echter Code mit Konsole), `trace`
  (Schritt-für-Schritt-Zustände), `sim` (Regler → Ergebnis) oder `custom` (eigene Demo mit
  `html()` und `init()`, die eine Aufräumfunktion zurückgibt).
- **Zweisprachig:** `tx('Deutsch','English')` steht direkt neben jedem Text.
- **Icons:** `tools/make_icons.py` erzeugt `favicon.svg`, `favicon.ico` und
  `apple-touch-icon.png` aus einer Geometrie (braucht Pillow).

## Schwester-Apps

[UI-Atlas](https://daniel-hopium.github.io/ui-atlas/), [CSS-Atlas](https://daniel-hopium.github.io/css-atlas/), [HTML-Atlas](https://daniel-hopium.github.io/html-atlas/), [ARIA-Kompass](https://daniel-hopium.github.io/aria-compass/), [Angular-Patterns](https://daniel-hopium.github.io/angular-patterns/), [Rechte-Kompass](https://daniel-hopium.github.io/access-compass/), [JS-Laufzeit](https://daniel-hopium.github.io/js-runtime/), [HTTP-Atlas](https://daniel-hopium.github.io/http-atlas/), [Sicherheits-Labor](https://daniel-hopium.github.io/security-lab/), [Performance-Atlas](https://daniel-hopium.github.io/perf-atlas/), [Algorithmen-Visualizer](https://daniel-hopium.github.io/algo-visualizer/).
