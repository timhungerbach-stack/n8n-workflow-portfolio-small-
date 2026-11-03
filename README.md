# n8n Workflow Portfolio — Tim Hungerbach

Dieses Repository zeigt eine Auswahl meiner n8n-Workflows. Alle drei habe ich während meines Praktikums bei der GOKIXX GmbH selbst konzipiert, gebaut und dokumentiert – für echte Abläufe im Team.

## Über mich

Ich automatisiere seit Oktober 2025 Geschäftsprozesse mit n8n, KI-APIs und Low-Code-Tools. Bei der GOKIXX GmbH habe ich n8n als unternehmensweite Plattform eingeführt und 11 API-Schnittstellen angebunden. Parallel baue ich eigene Workflows für verschiedene Use Cases. Code-Bausteine (JavaScript) entwickle ich mit KI-Unterstützung.

**Tech-Stack:** n8n, OpenAI API, Anthropic API (Claude), Google Workspace (Sheets, Calendar, Gmail), Slack, Salesforce, Pipedrive, JavaScript in Code-Nodes (KI-gestützt)

## Workflows

| # | Workflow | Nodes | Problem → Lösung |
|---|---------|-------|-------------|
| 01 | [Scouting Kalender](./01-scouting-kalender/) | 40 | Scouts mussten Spieltermine ihrer Spieler selbst suchen und eintragen → Spielpläne von Fussball.de landen automatisch im Google Calendar |
| 02 | [Office Belegung Tracker](./02-office-belegung-tracker/) | 30 | Mehr Mitarbeitende als Büroplätze → jeden Sonntagabend automatisch die Belegung der Woche im Slack-Channel, inkl. Warnung bei Überbelegung |
| 03 | [Transfer-News](./03-transfer-news/) | 18 | Transferseiten mehrerer Ligen manuell durchklicken → jeden Morgen ein fertiger U23-Transfer-Report per E-Mail |

## Hinweis

Die Workflow-JSONs enthalten keine Credentials, API-Keys oder internen Daten. IDs von Google Sheets, Kalendern, Slack-Channels und Airtable sind durch Platzhalter wie `DEINE_GOOGLE_SHEET_ID` ersetzt. Zur Nutzung müssen eigene Zugangsdaten und IDs hinterlegt werden.

## Kontakt

Tim Hungerbach — [tim.hungerbach@icloud.com](mailto:tim.hungerbach@icloud.com)
