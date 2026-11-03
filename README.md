# n8n Workflow Portfolio — Tim Hungerbach

Dieses Repository zeigt eine Auswahl meiner n8n-Workflows. Ich habe sie selbst gebaut und dokumentiert; zwei davon (SEO & GEO Audit, AI Recruiting Pipeline) basieren auf Vorlagen aus der n8n-Community, die ich für meine Zwecke angepasst habe.

## Über mich

Ich automatisiere seit Oktober 2025 Geschäftsprozesse mit n8n, KI-APIs und Low-Code-Tools. Bei der GOKIXX GmbH habe ich n8n als unternehmensweite Plattform eingeführt und 11 API-Schnittstellen angebunden. Parallel baue ich eigene Workflows für verschiedene Use Cases. Code-Bausteine (JavaScript) entwickle ich mit KI-Unterstützung.

**Tech-Stack:** n8n, OpenAI API, Anthropic API (Claude), OpenRouter, Google Workspace (Sheets, Calendar, Gmail), Slack, Salesforce, Pipedrive, Airtable, Apollo.io, JavaScript in Code-Nodes (KI-gestützt)

## Workflows

| # | Workflow | Nodes | Beschreibung |
|---|---------|-------|-------------|
| 01 | [SEO & GEO Audit](./01-seo-geo-audit/) | 14 | KI-gestützter Website-Audit mit 4 parallelen AI-Agents |
| 02 | [Scouting Kalender](./02-scouting-kalender/) | 40 | Automatischer Spielkalender aus Fussball.de → Google Calendar |
| 03 | [AI Recruiting Pipeline](./03-ai-recruiting-pipeline/) | 40 | Kandidatensuche, KI-Scoring und Outreach via Apollo & Airtable |
| 04 | [Office Belegung Tracker](./04-office-belegung-tracker/) | 30 | Slack-Nachrichten → Google Sheets + tägliche Zusammenfassung |
| 05 | [Transfer-News](./05-transfer-news/) | 18 | Web Scraping von Transfermarkt mit E-Mail-Report |

## Hinweis

Die Workflow-JSONs enthalten keine Credentials, API-Keys oder internen Daten. IDs von Google Sheets, Kalendern, Slack-Channels und Airtable sind durch Platzhalter wie `DEINE_GOOGLE_SHEET_ID` ersetzt. Zur Nutzung müssen eigene Zugangsdaten und IDs hinterlegt werden.

## Kontakt

Tim Hungerbach — [tim.hungerbach@icloud.com](mailto:tim.hungerbach@icloud.com)
