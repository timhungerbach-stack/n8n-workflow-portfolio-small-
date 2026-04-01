# Office Belegung Tracker

Automatisierte Bürobelegungsübersicht: Liest Slack-Nachrichten aus Team- und Praktikanten-Channels, parst die Anwesenheitsmeldungen und postet eine tägliche Zusammenfassung zurück in Slack + Google Sheets.

## Was macht der Workflow?

1. **Trigger:** 3 Schedule Trigger für unterschiedliche Zeitpunkte (z.B. Wochentage)
2. **Reset:** Google Sheet wird zu Beginn geleert
3. **Slack auslesen:** Channel-History wird aus zwei Slack-Channels gelesen (Team + Praktikanten)
4. **User-Info:** Slack-User-IDs werden mit Klarnamen aufgelöst
5. **Zusammenführung:** Nachrichten und User-Infos werden gemerged
6. **Parsing:** JavaScript-Code parst die Nachrichten und erkennt, wer im Office ist, wer remote arbeitet, wer nicht da ist
7. **Google Sheets:** Die Ergebnisse werden in ein Tracking-Sheet geschrieben
8. **Zusammenfassung:** Eine formatierte Übersicht wird erstellt
9. **Slack-Post:** Die Zusammenfassung wird in zwei Channels gepostet (Team + Praktikanten)

## Genutzte Nodes & Integrationen

- **Schedule Trigger (3x)** — Zeitgesteuert an verschiedenen Wochentagen
- **Slack (5x)** — Channel History lesen, User-Info abrufen, Zusammenfassung posten
- **Google Sheets (2x)** — Sheet leeren + Ergebnisse schreiben
- **Merge (3x)** — Nachrichten mit User-Infos zusammenführen
- **Code (2x)** — Nachrichtenparser + Zusammenfassung formatieren

## Besonderheiten

- Zwei getrennte Channel-Pipelines (Team + Praktikanten) die am Ende zusammenlaufen
- Automatische Namensauflösung von Slack-User-IDs
- Tägliche Übersicht ohne manuellen Aufwand
- Output in zwei Formaten: Google Sheets (Archiv) + Slack (sofortige Sichtbarkeit)

## Nodes

30 (davon 5 Slack-Nodes, 3 Merge-Nodes, 2 Code-Nodes)
