# 🚀 KI-gestützte YouTube-Upload-Pipelines

Willkommen in meinem Projekt-Repository! Hier präsentiere ich zwei automatisierte Workflows, die ich mit **n8n** entwickelt habe, um den gesamten Prozess von der Cloud-Speicherung bis zum fertigen YouTube-Release inklusive SEO-Optimierung zu automatisieren. 

Diese Projekte demonstrieren meine Fähigkeiten in der Prozessautomatisierung, API-Integration und dem praktischen Einsatz von Large Language Models (LLMs).

---

## 1. Komplexe KI-Automatisierung & SEO-Pipeline (ThommyEight)

![KI Video Erstellung](Bild%20KI-basierte%20Video-Erstellung.png)

**Beschreibung:**
Entwicklung eines vollautomatisierten Workflows für den YouTube-Kanal „ThommyEight“. Das System erkennt neue Videodateien in einem spezifischen Google Drive-Ordner, lädt diese auf YouTube hoch und nutzt das Anthropic Claude-Modell für die dynamische Generierung von SEO-optimierten Titeln, Tags und Hashtags basierend auf dem rohen Dateinamen.

**✨ Besondere Features:**
* **Shorts-Erkennung:** Automatische Erkennung von YouTube-Shorts durch die Analyse der Video-Metadaten (Format-Prüfung `height > width`).
* **Datenbereinigung per Code:** Einsatz von benutzerdefiniertem JavaScript zur Strukturierung der KI-Ausgaben, Filterung von Sonderzeichen und strikten Einhaltung der YouTube-Zeichenlimits (max. 500 Zeichen für Tags).
* **Datenprotokollierung:** Automatische Übertragung der finalen Upload-Daten (URLs, Titel, Tags) in ein Google Sheets-Dokument für das weitere Social Media Management.

**🛠️ Angeignete Skills & Tech Stack:**
* **Automatisierung:** n8n, visuelles Workflow-Design, bedingte Logik (If-Statements)
* **APIs:** Google Drive API, YouTube Data API, Google Sheets API
* **KI / LLMs:** Prompt Engineering, Integration von Anthropic Claude (Langchain)
* **Programmierung:** JavaScript (Datenstrukturierung, Regex, Fehlervermeidung)

---

## 2. Automatisierter Cloud-to-YouTube Workflow (Nulty Little)

![YouTube Upload Automation](Bild%20YouTube-Upload-Automation.png)

**Beschreibung:**
Eine effiziente, ressourcenschonende End-to-End-Upload-Pipeline für den YouTube-Kanal „Nulty Little“. Dieser Workflow fokussiert sich auf automatisiertes Cloud-Management und nutzt Google Gemini als KI-Engine zur Textverarbeitung.

**✨ Besondere Features:**
* **Speichermanagement:** Selbstständige Löschung der massenspeicherintensiven Originaldateien im Google Drive nach erfolgreichem Upload auf YouTube und Ablauf einer Sicherheitsfrist.
* **Alternatives LLM:** Erfolgreiche Anbindung und Workflow-Integration des Google Gemini Modells, was Flexibilität im Umgang mit verschiedenen KI-Anbietern beweist.

**🛠️ Angeignete Skills & Tech Stack:**
* **Automatisierung:** n8n, Cloud-Ordner-Überwachung
* **APIs:** Google Drive API (inkl. destruktiver Datei-Operationen), YouTube Data API
* **KI / LLMs:** Integration der Google Gemini API
* **Effizienz:** Reduzierung manueller Routineaufgaben und intelligentes Ressourcenmanagement
