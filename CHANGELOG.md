# Changelog

Alle nennenswerten Änderungen an Regex-Werkstatt. Die Einträge beschreiben, was das Projekt
danach kann bzw. was sich für den Nutzer ändert – kein Commit-Protokoll.

**Regel:** Jeder Commit bekommt seinen Eintrag, im selben Commit. Neues kommt oben unter
„Unveröffentlicht“ dazu; beim Release wird daraus ein Abschnitt mit Versionsnummer und Datum.

Kategorien: **Neu** (neue Funktionen), **Verbessert** (bestehendes Verhalten), **Behoben**
(Fehler), **Intern** (Struktur, Tooling, nicht sichtbar).

## Unveröffentlicht

### Neu
- Erste Version: 46 Einträge in 11 Kapiteln (Werkstatt, Grundlagen, Quantoren, Gruppen & Ersetzen, Lookarounds, Flags, Regex in JavaScript, Unicode & Umlaute, Rezepte, Fallen & Performance, Übungen),
  auf Deutsch und Englisch, mit Suche, hellem und dunklem Design, breiter Ansicht und
  App-Symbol.
- Tester im Web Worker: Gematcht wird in einem Worker mit 1,5 s Zeitlimit. Ein katastrophales Muster friert so nur den Worker ein, nicht die Seite.
- Erklärer: Ein eigener Parser zerlegt das Muster in Bausteine (Klassen, Quantoren, Gruppen, Lookarounds, Unicode-Eigenschaften) und beschreibt jeden einzeln.
- Schritt-Modus: Eine kleine Backtracking-Engine protokolliert jeden Versuch – so sieht man, warum `<.+>` zu viel nimmt und `(a+)+b` explodiert.
- Übungen: 17 Aufgaben in drei Stufen; gelöste Aufgaben merkt sich der Browser.
