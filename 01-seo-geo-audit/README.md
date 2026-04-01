# SEO & GEO Audit

Automatisierter Website-Audit, der eine URL entgegennimmt und über 4 parallele KI-Agents einen vollständigen SEO- und GEO-Report erstellt.

## Was macht der Workflow?

1. **Input:** Nutzer gibt eine Landing-Page-URL über ein Webformular ein
2. **Scraping:** Die Seite wird per HTTP Request abgerufen
3. **Analyse:** 4 KI-Agents laufen parallel und analysieren die Seite aus unterschiedlichen Blickwinkeln:
   - Technical Audit SEO
   - Content Audit SEO
   - Technical Audit GEO (Generative Engine Optimization)
   - Content Audit GEO
4. **Aggregation:** Die Ergebnisse werden zusammengeführt und in Markdown konvertiert
5. **Output:** Der fertige Report wird per Gmail als E-Mail versendet

## Genutzte Nodes & Integrationen

- **Form Trigger** — Eingabeformular für die URL
- **HTTP Request** — Website-Scraping
- **AI Agent (4x)** — LangChain-Agents über OpenRouter (LLM)
- **Merge + Aggregate** — Zusammenführung der 4 Audit-Ergebnisse
- **Markdown** — Konvertierung in lesbares Format
- **Gmail** — Versand des fertigen Reports

## Besonderheiten

- 4 AI-Agents arbeiten parallel, nicht sequenziell → schnellere Ergebnisse
- Trennung von SEO und GEO zeigt, dass der Workflow zukunftsorientiert aufgebaut ist (GEO = Optimierung für KI-Suchmaschinen wie Perplexity, ChatGPT Search etc.)
- Komplett formularbasiert — kann von jedem im Team ohne n8n-Kenntnisse genutzt werden

## Nodes

14 (davon 4 AI-Agents, 4 LLM-Modelle)
