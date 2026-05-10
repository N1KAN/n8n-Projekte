# 🚀 KI-gestützte Content- & Automatisierungs-Pipelines

Willkommen in meinem Projekt-Repository! Hier präsentiere ich zwei fortschrittliche Workflows, die ich mit **n8n** entwickelt habe. Sie demonstrieren meine Fähigkeiten in der Prozessautomatisierung, API-Integration und der Orchestrierung verschiedener KI-Modelle (LLMs & Text-to-Video) für das moderne Social Media Management.

---

## 1. YouTube Upload Automatisierung

![YouTube Upload Automation](Bild%20Youtube-Upload-Automation.png)

**Beschreibung:**
Ein vollautomatisierter Workflow, der den kompletten YouTube-Upload-Prozess von der Cloud bis zur Veröffentlichung steuert. Sobald eine Videodatei in Google Drive abgelegt wird, lädt das System diese auf YouTube hoch. Zeitgleich analysiert das **Anthropic Claude Sonnet 4.5** Modell den Dateinamen und generiert SEO-optimierte Titel, Tags und Beschreibungstexte.

**✨ Besondere Features:**
* **Shorts-Erkennung & Daten-Protokollierung:** Der Workflow erkennt automatisch, ob es sich um ein YouTube Short handelt (durch Prüfung der Auflösung `height > width` oder des Dateinamens). Shorts werden zur weiteren Verarbeitung (z.B. für Buffer/Zapier) in ein Google Sheet eingetragen.
* **Datenbereinigung per Code (JavaScript):** Ein benutzerdefiniertes Skript strukturiert die KI-Ausgaben, filtert Sonderzeichen und stellt sicher, dass das strenge YouTube-Zeichenlimit für Tags (max. 500 Zeichen) exakt eingehalten wird.
* **Cloud-Speichermanagement:** Nach erfolgreichem Upload und einer Sicherheitsfrist wird die Originaldatei automatisch aus Google Drive gelöscht, um Speicherplatz zu sparen.

**🛠️ Angeignete Skills & Tech Stack:**
* **Automatisierung:** n8n, bedingte Logik (If-Statements), automatisiertes Speichermanagement
* **APIs:** Google Drive, YouTube Data API, Google Sheets
* **KI / LLMs:** Prompt Engineering, Integration von Anthropic Claude 4.5
* **Programmierung:** JavaScript (Datenstrukturierung, Regex)

---

## 2. Vollautomatisierte KI-Video-Generierung & Social Media Distribution (Sora 2)

![KI Video Erstellung](Bild%20KI-basierte%20Video-Erstellung.png)

**Beschreibung:**
Eine autonome Content-Creation-Pipeline, die komplett selbstständig Kurzvideos erstellt und veröffentlicht. Ein zeitgesteuerter Trigger startet den Prozess. Eine KI (**Claude 3 Haiku**) generiert basierend auf einem Zufallsprinzip kreative, deutsche Video-Prompts. Diese werden über eine API an einen **Text-to-Video KI-Dienst (Sora 2)** gesendet. Nach der Generierung wird das fertige Video automatisch auf TikTok und mehreren Instagram-Accounts gepostet.

**✨ Besondere Features:**
* **Text-to-Video API-Integration:** Anbindung der Kie AI API zur Nutzung von Sora-2, inklusive asynchronem Polling (Wait-Nodes und Status-Abfragen), um auf das fertig gerenderte Video zu warten.
* **Structured Output Parsing:** Strikte Formatierung der KI-Antworten in JSON-Objekte, um eine fehlerfreie Übergabe von Titeln, Beschreibungen und Prompts an die nächsten Prozessschritte zu garantieren.
* **Multi-Channel Publishing:** Automatisiertes Cross-Posting der finalen Medieninhalte auf verschiedenen Plattformen (TikTok & Instagram) über die Blotato-Integration.

**🛠️ Angeignete Skills & Tech Stack:**
* **Automatisierung:** n8n, Cron-Jobs (Schedule Trigger), asynchrone API-Abfragen (Polling)
* **Generative KI:** Text-to-Video APIs (Sora 2), LLM Output Parsing (Langchain)
* **Social Media APIs:** Automatisierte Veröffentlichung auf TikTok und Instagram
* **Datenverarbeitung:** Handling komplexer JSON-Strukturen und HTTP-Requests
