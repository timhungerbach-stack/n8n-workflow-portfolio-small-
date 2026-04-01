# AI Recruiting Pipeline

KI-gestützte Recruiting-Pipeline: Von der Jobbeschreibung über die Kandidatensuche bis zum fertigen Outreach — automatisiert mit Apollo, OpenAI, Anthropic und Airtable.

## Was macht der Workflow?

1. **Input:** Jobbeschreibung wird über ein Webformular eingegeben
2. **Job anlegen:** Der Job wird in Airtable gespeichert
3. **Titel-Varianten:** OpenAI generiert Varianten des Jobtitels für eine breitere Suche
4. **Kandidatensuche:** Apollo People Search findet passende Kandidaten pro Titel-Variante
5. **Deduplizierung:** Doppelte Kandidaten werden entfernt
6. **KI-Scoring:** GPT-4.1-mini bewertet und priorisiert die Kandidaten anhand der Jobanforderungen
7. **Datenstrukturierung:** Die Ergebnisse werden durch einen Structured Output Parser in ein einheitliches Format gebracht
8. **LinkedIn-Anreicherung:** Kandidatenprofile werden mit LinkedIn-Daten ergänzt
9. **Assessment:** Ein detailliertes Candidate Assessment wird per KI erstellt
10. **Outreach-Nachrichten:** Anthropic (Claude) generiert personalisierte Anschreiben pro Kandidat
11. **Output:** Alle Kandidaten mit Scoring, Assessment und Nachricht werden in Airtable gespeichert

## Genutzte Nodes & Integrationen

- **Form Trigger** — Jobeingabe
- **Airtable (2x)** — Job + Kandidaten speichern
- **OpenAI (5x)** — Titel-Generierung, Scoring, Datenstrukturierung, Assessment
- **Anthropic Claude** — Personalisierte Outreach-Nachrichten
- **Apollo API** — Kandidatensuche
- **HTTP Request** — LinkedIn-Profil-Anreicherung
- **Structured Output Parser + Auto-fixing Parser** — Zuverlässige JSON-Ausgaben aus LLM-Responses
- **LangChain Chains (3x)** — Scoring, Assessment, Message Generation

## Besonderheiten

- Multi-Model-Ansatz: OpenAI für Scoring + Strukturierung, Anthropic für Nachrichten
- Auto-fixing Output Parser sorgt dafür, dass fehlerhafte LLM-Outputs automatisch korrigiert werden
- Vollständige Pipeline vom Job-Post bis zum fertigen Outreach in einem Workflow
- Airtable als zentrales CRM für Jobs und Kandidaten

## Nodes

40 (davon 6 LLM-Nodes, 3 LangChain Chains, 3 Output Parser)
