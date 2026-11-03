# Transfer-News

Täglicher Transfer-Report für die Scouting-Redaktion: Der Workflow ruft die Transferseiten ausgewählter Ligen bei Transfermarkt ab, filtert auf U23-Spieler und verschickt jeden Morgen eine fertig formatierte E-Mail.

## Was macht der Workflow?

1. **Trigger:** Startet automatisch jeden Tag um 08:15 Uhr (alternativ manuell)
2. **Ligen laden:** Die zu überwachenden Ligen samt Transfermarkt-Link kommen aus einem Google Sheet
3. **Loop:** Jede Liga wird einzeln verarbeitet
4. **Scraping:** Die Transferseite der Liga wird per HTTP Request abgerufen (mit Browser-User-Agent)
5. **Extraktion:** Die Transfer-Tabelle wird aus dem HTML herausgelöst
6. **Parsing:** Spieler, Alter, abgebender und aufnehmender Verein, Liga und Datum werden ausgelesen
7. **Formatierung:** Jeder Transfer wird als lesbarer Satz aufbereitet
8. **Filter & Aggregation:** Nur Spieler bis 23 Jahre, gruppiert nach Liga
9. **Output:** Versand als HTML-E-Mail per Gmail, Betreff „Transfernews U23 TT.MM.JJJJ“

## Genutzte Nodes & Integrationen

- **Schedule Trigger** — tägliche Ausführung
- **Google Sheets** — Liste der überwachten Ligen
- **Split In Batches** — Verarbeitung Liga für Liga
- **HTTP Request** — Abruf der Transfermarkt-Seiten
- **HTML** — Extraktion der Transfer-Tabelle
- **Code (3x)** — Parsing, Formatierung, U23-Filter und Aufbau der E-Mail
- **Gmail** — Versand des Reports

## Besonderheiten

- Neue Ligen lassen sich ohne Änderung am Workflow ergänzen: einfach eine Zeile im Google Sheet hinzufügen
- Ersetzt das manuelle Durchklicken mehrerer Transferseiten jeden Morgen
- Ausführliche Notizen direkt im Workflow erklären jeden Schritt

## Nodes

18 (davon 3 Code-Nodes, 9 Notizen zur Dokumentation)
