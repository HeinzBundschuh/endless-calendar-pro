# Endless Calendar Pro

Ein vollständiger Kalender in **einer einzigen HTML-Datei**. Keine Installation, kein Konto, kein Server: Datei im Browser öffnen und loslegen – offline, unter Windows, Linux, macOS und Android. Deine Termine bleiben in deinem Browser.

🇬🇧 [English version](README.md)

![Monatsansicht](docs/screenshots/monat.png)

## Benutzen

1. `endless_calendar_pro_V3_1.html` aus den [Releases](../../releases) (oder aus diesem Repository) herunterladen.
2. Im Browser öffnen (Firefox, Chrome, Edge …). Das ist alles.

Die Termine liegen im lokalen Speicher des Browsers für diese Datei. Sichere regelmäßig über **ICS ↕ → JSON Backup** eine Sicherungsdatei; damit ziehst du den Kalender auch in einen anderen Browser oder auf ein anderes Gerät um. Der Kalender erinnert in der Info-Leiste, wenn das letzte Backup länger her ist.

## Überblick

- Fünf Ansichten: Jahr, Monat, Woche, Tag, Liste
- Bedienung mit der Maus: ziehen, kopieren, zusammenführen, Rechtsklick-Menü
- Serientermine mit vielen Regeln und Ausnahmen für einzelne Vorkommen
- Kategorien mit Farbe und Emoji, Geburtstage und Gedenktage
- Österreichische Feiertage und besondere Tage
- Suche, Aus- und Einblenden, Konfliktwarnung
- Rückgängig, Sicherungspunkte, ICS- und JSON-Import/-Export, Duplikatbereinigung
- Dunkelmodus, Vollbild, Desktop- und Mobil-Layout

## Ansichten und Navigation

- **Jahr:** zwölf Monate mit Kalenderwochen; Tage mit Terminen sind markiert.
- **Monat:** Raster mit Termin-Chips, darunter die Terminliste des Monats. Passt nicht alles in einen Tag, führt „+N mehr“ zur Tagesansicht.
- **Woche** und **Tag:** Termine mit Uhrzeit; Termine über Mitternacht zeigen an den Folgetagen ihr Startdatum.
- **Liste:** alle Termine eines Jahres; mehrtägige Termine als ein Eintrag mit Zeitraum.
- **Seitenleiste:** Mini-Kalender und „Demnächst“ mit dem jeweils nächsten Vorkommen.
- **Info-Leiste:** heutiges Datum, Kalenderwoche, Tag des Jahres, Termine von heute.
- **Blättern:** Pfeile ◀ ▶, Knopf **Heute**, Mausrad über dem Kalender (Monate, Jahre, Wochen, Tage), Wischen am Touchscreen.

![Jahresansicht](docs/screenshots/jahr.png)

## Bedienung mit der Maus

**Ziehen und Ablegen (Monatsansicht)**

| Aktion | Wirkung |
|---|---|
| Termin auf einen anderen Tag ziehen | Termin verschieben |
| Mit **Strg** oder **Umschalt** ziehen | Termin kopieren, das Original bleibt |
| Termin auf einen anderen Termin ablegen | beide zu einem Termin zusammenführen (Titel mit „+“, Notizen bleiben erhalten) |

Bei Serien betrifft das Ziehen nur das angefasste Vorkommen. Entsteht eine Zeitüberschneidung, zeigt die Bestätigung eine Warnung – mit **Rückgängig** direkt daneben.

**Rechtsklick auf einen Termin** (Monat, Woche, Tag, Liste, „Demnächst“)

- 📄 Termin kopieren
- ✏️ Bearbeiten
- ↔ Verschieben auf ein Zieldatum (bei Serien nur dieses Vorkommen)
- 📍 Springe zu Termin (öffnet die Tagesansicht)
- 🙈 Termin oder ganze Kategorie ausblenden
- 🗑 Löschen

**Rechtsklick auf einen Tag**

- 📋 Neuer Termin
- 📅 Tag ansehen
- 📥 Einfügen des kopierten Termins – beliebig oft, auch in anderen Monaten

Am Handy ersetzt langes Drücken den Rechtsklick.

## Termine

- Titel, Kategorie, Datum, Uhrzeit von–bis, Notizen.
- **Mehrtägig** über „Ende am“; **über Mitternacht** (z. B. 22:00–01:00) mit Rückfrage beim Speichern.
- **Erinnerung:** 1, 2 oder 3 Tage oder 1 Woche vorher. Mit eingeschalteter Glocke 🔔 kommen Erinnerungen als Browser-Benachrichtigung, solange die Seite offen ist.
- **Farbe je Termin:** Kategoriefarbe, eine von acht Pastellfarben oder eine eigene Farbe; wahlweise eigene Schriftfarbe. Die Schriftfarbe wird sonst automatisch nach Kontrast gewählt.
- **Darstellung je Termin** in der Monatsansicht: mit Farbhintergrund, nur farbiger Rand oder nur Text.
- **Termintyp:** Termin, Feiertag, privater Termin oder versteckter Termin (nur in der Liste sichtbar).
- **Eingabeprüfung:** Enddatum vor Beginn, Endzeit ohne Anfangszeit und ähnliche Fehler werden beim Speichern abgefangen.
- **Konfliktwarnung ⚠️:** Überschneidungen werden beim Speichern und in der Tagesansicht angezeigt, auch für Serien und mehrtägige Termine.

## Serientermine

- **Einfach:** wöchentlich, monatlich, jährlich.
- **Freies Intervall:** alle *n* Stunden, Tage, Wochen, Monate oder Jahre; bei Stunden auch als `HH:MM` (z. B. alle 02:30 Stunden).
- **Wochentag im Monat:** z. B. „erster Montag im Mai“ oder „letzter Freitag jedes Monats“.
- **Bewegliche Termine:** relativ zu Ostern oder zum 1. Advent.
- **Zusatzbedingungen:** Häkchen für Wochentage und Monate, z. B. „Freitag der 13.“ oder „nur werktags im Sommer“.
- **Ende:** nie, nach *n* Terminen oder an einem Datum; wahlweise Feiertage auslassen.
- **Ausnahmen:** ein einzelnes Vorkommen löschen oder verschieben, ohne die Serie zu ändern.
- Jährliche Termine zeigen die Jahre seit dem Start in Klammern (Geburtstag: Alter, Hochzeitstag: Jahre).

## Kategorien

- Fünf Kategorien sind vorgegeben: Termin, Geburtstag, Feiertag, Privater Termin, Sonstiges.
- Unter **Kategorien** legst du eigene an und änderst Name, Farbe und Emoji.
- Neue Termine übernehmen die Farbe ihrer Kategorie und folgen späteren Farbänderungen.
- Jede Kategorie lässt sich mit einem Schalter **aus- und einblenden**.
- Neue Termine in Geburtstags-, Gedenk- und Jahrestags-Kategorien starten mit „Jährlich“.

## Geburtstage und Gedenktage

- Geburtstage zeigen das Alter: „Anna (41)“.
- Mit einem optionalen Sterbedatum läuft der Geburtstag weiter als „Name (wäre 94 geworden)“, und am Sterbetag erscheint jährlich ein Gedenktag „✝ Name (13)“.
- Geburtstage lassen sich aus einer `birthday.dat` (Ewiger Kalender) importieren.

## Feiertage und besondere Tage

Die österreichischen Feiertage und besondere Tage werden für jedes Jahr berechnet, darunter die von Ostern abhängigen Tage (Gründonnerstag bis Pfingsten), Advent, Zeitumstellung, Faschingsdienstag, Martini und Heiliger Abend. Sie erscheinen in einer einheitlichen Farbe und werden von der Suche gefunden.

## Suche

Die Lupe 🔍 durchsucht Titel, Notizen und Kategorien aller Termine. Sie findet auch Feiertage und besondere Tage (aktuelles Jahr ± 2 Jahre). Jeder Treffer hat einen Knopf **Springe zu Termin**.

## Aus- und Einblenden

- Einzelne Termine oder ganze Kategorien lassen sich ausblenden. Das ist reine Anzeige: Daten, Backups und Erinnerungen bleiben unverändert.
- In der Terminliste unter der Monatsansicht und in der Listenansicht bleiben ausgeblendete Termine gedimmt sichtbar und lassen sich mit 👁 wieder einblenden.
- Eine Hinweisleiste zeigt, was ausgeblendet ist, mit dem Knopf **Alles einblenden**.

## Rückgängig und Sicherheit

- **Rückgängig:** die letzten 30 Änderungen, über den Knopf **↩ Rückgängig** in der Kopfleiste oder mit **Strg+Z**. Der Tooltip nennt die Aktion, die zurückgenommen wird.
- **Sicherungspunkt:** Vor jedem Import und vor der Duplikatbereinigung wird der Stand gespeichert und lässt sich unter **ICS ↕ → Wartung** wiederherstellen.
- **Löschen:** Die Knöpfe sagen genau, was gelöscht wird („Nur dieses Vorkommen“, „Serie“, „Gesamten Zeitraum“). Die Rückfrage nennt Termin, Umfang und Zeitraum.
- **Löschabfrage abschalten:** In den Einstellungen ⚙ gibt es „Beim Löschen einzelner Termine nicht nachfragen“. Serien und Zeiträume fragen zur Sicherheit weiter nach; Rückgängig bleibt immer möglich.
- **Mehrere Tabs:** Änderungen aus einem anderen Tab werden erkannt; Rückgängig wird dann gesperrt, statt fremde Daten zu überschreiben.

## Import, Export und Wartung (Knopf „ICS ↕“)

- **ICS-Export** als Datei oder Text, standardkonform für Google Kalender, Outlook, Thunderbird und andere.
- **ICS-Import mit Vorschau:** Zuerst wird nur eingelesen und geprüft. Du siehst, was neu, doppelt oder fehlerhaft ist, wählst aus und übernimmst erst dann.
- **birthday.dat** importieren.
- **JSON-Backup** als Datei oder Text. Beim Laden wählst du **Zusammenführen** (empfohlen) oder **Ersetzen**.
- **Wartung – Duplikate entfernen:** findet exakte Duplikate, ähnliche Paare (gleicher Name und gleiches Datum) und deckungsgleiche Serien mit unterschiedlichem Startdatum. Vor dem Entfernen zeigt eine Vorschau alle geplanten Änderungen; bei Abbruch bleibt alles unverändert.
- **Wartung – Sicherungspunkt wiederherstellen.**

## Einstellungen und Darstellung (⚙)

- **Hell** oder **Dunkel**, mit wählbarer Akzentfarbe (Vorgaben oder freie Farbe).
- Termin-Chips mit Farbhintergrund, mit farbigem Rand oder beides.
- Löschabfrage für einzelne Termine ein oder aus.
- **Vollbild** über den Knopf ⛶ in der Kopfleiste.

## Desktop und Mobil

| | Desktop | Handy und Tablet |
|---|---|---|
| Menü | Rechtsklick | langes Drücken |
| Blättern | Mausrad, Pfeile | Wischen, Pfeile |
| Verschieben | Ziehen und Ablegen | Menü „↔ Verschieben“ |
| Tastatur | Strg+Z, Esc schließt Dialoge | – |
| Layout | Seitenleiste neben dem Kalender | einspaltig, kompakte Kopfleiste |

Tipp für Android: Im Browser-Menü „Zum Startbildschirm hinzufügen“ wählen. Zusammen mit dem Vollbild-Knopf startet der Kalender dann wie eine App.

## Funktionsweise

Alles – HTML, CSS und JavaScript – steckt in einer Datei, ohne fremde Bibliotheken und ohne Netzwerkzugriffe. Die Versionsgeschichte steht am Anfang der Datei.

Die Daten liegen im `localStorage` (Schlüssel `ecpro_v1`). Sie gehören zum Browserprofil und zum Ort, von dem die Datei geöffnet wird. Wer die Browserdaten löscht, löscht auch die Termine – deshalb Backups anlegen.

## Mitmachen

Fehlermeldungen und Ideen sind willkommen – bitte ein [Issue](../../issues) anlegen.

## Datenschutz

Die Datei sendet keine Daten. Kein Tracking, keine Statistik, keine Werbung.

## Lizenz

[MIT](LICENSE) © 2026 Heinz Bundschuh
