# ROADMAP — Beyond the Portfolio: My Interactive Developer Journey

> Diese Datei beschreibt den **geplanten** Entwicklungsverlauf des Projekts.
> Der **tatsächliche** Fortschritt wird separat in [`PROJECT_PROGRESS.md`](./PROJECT_PROGRESS.md) dokumentiert.
> Massgeblich für den echten Stand des Codes ist immer die Git-History.

**Zeitraum:** 22. September 2026 – 10. Januar 2027 (ca. 16 Wochen, 90–140 Stunden)
**Kontext:** Einzelarbeit im Modul Web Engineering, zusätzlich als Bewerbungsportfolio nutzbar.

## Projektvision

Drei miteinander verknüpfte Hauptfunktionen auf einer gemeinsamen Datenbasis:

1. **Interaktive Lebensreise** – animierte Timeline meiner persönlichen/beruflichen Entwicklung
2. **Interaktive Entwickler-Landkarte** – D3.js-Netzwerkvisualisierung von Technologien & Projekten
3. **Persönlicher KI-Assistent** – Chatbot, der Fragen anhand echter Portfolio-Daten beantwortet

Alle drei greifen auf dieselben JSON-Datenquellen (`data/profile.json`, `data/projects.json`, `data/timeline.json`) zu, damit ein neues Projekt nicht an drei Stellen im Code gepflegt werden muss.

## Technische Architektur (Entscheidungen aus der Vorbereitungsphase)

| Bereich | Entscheidung | Begründung |
|---|---|---|
| Frontend | Reines HTML5/CSS3/JS (ES-Module, kein Build-Zwang) | GitHub Pages ist statisch; ES-Module laufen direkt im Browser ohne Bundler |
| Animation | GSAP (+ ScrollTrigger) via CDN | Standard für performante Scroll-Animationen |
| Visualisierung | D3.js (Force-Directed Graph) via CDN | Flexibel genug für Netzwerkstruktur Technologien↔Projekte |
| Daten | Statische JSON-Dateien unter `data/` | Zentral pflegbar, von allen drei Hauptfunktionen nutzbar |
| GitHub-Repos | **Build-Time-Fetch** über GitHub Action statt Live-Client-Fetch | Vermeidet das 60-Requests/Stunde-Limit der unauthentifizierten GitHub-API pro Besucher; Ergebnis wird als `data/github-cache.json` committet und im Frontend nur gelesen |
| KI-Backend | Separater Serverless-Endpunkt (z. B. Cloudflare Worker) statt GitHub Pages | API-Schlüssel dürfen nie im Frontend liegen; GitHub Pages kann keinen Server ausführen |
| Tests | Vitest/Jest (Unit) + GitHub Actions (CI) | Deckt Datenverarbeitung, Filter, Chatbot-Logik ab |
| Fallback KI | Regelbasierte Antwortlogik bleibt immer aktiv | Funktioniert auch, falls die echte KI-Anbindung zeitlich nicht mehr passt |

### Identifizierte Risiken

- **GitHub-API-Limit:** clientseitige Live-Abfragen sind bei 60 Requests/h/IP für einen öffentlichen Portfolio-Besuch riskant → gelöst durch Build-Time-Caching (siehe oben).
- **KI-Anbindung & Geheimnisse:** GitHub Pages kann keine Secrets sicher halten → erfordert externen Backend-Dienst; muss früh genug (Woche 12) evaluiert werden, sonst bleibt Stufe 2 (regelbasiert) die Abgabeversion.
- **D3.js auf Mobilgeräten:** Force-Graphs sind touch- und performance-kritisch → alternative Listenansicht für kleine Screens ist von Anfang an eingeplant (nicht optional).
- **Zwei schwere Libraries (GSAP + D3):** Ladezeiten im Auge behalten, `defer`/`async` nutzen, Animationen bei `prefers-reduced-motion` reduzieren.

## Wochenplan

### Woche 1 — Projektstart und GitHub (22.–27. Sept)
- Projektanforderungen verstehen, Repository-Struktur anlegen
- README und Roadmap anlegen
- HTML-Grundgerüst entwickeln
- GitHub Pages einrichten, erste öffentliche Version veröffentlichen

### Woche 2 — Designsystem und Navigation (28. Sept – 4. Okt)
- Farbschema & Typografie als CSS-Tokens definieren
- Wiederverwendbare CSS-Komponenten
- Responsive Navigation + mobiles Menü

### Woche 3 — Startseite und Animationen (5.–11. Okt)
- Hero-Section, persönliche Vorstellung
- Erste Animationen, Scroll-Navigation
- Mobile Darstellung testen

### Woche 4 — Lebensreise: Grundstruktur (12.–18. Okt)
- Timeline-Datenmodell (`timeline.json`)
- Timeline-Layout, dynamisches Rendering

### Woche 5 — Lebensreise: Interaktivität (19.–25. Okt)
- Scroll-Animationen (GSAP), Detailansichten
- Projektverlinkung, Barrierefreiheit

### Woche 6 — Gemeinsame Projekt-Datenbasis (26. Okt – 1. Nov)
- `projects.json`, Projektübersicht, Filter, Detailansichten

### Woche 7 — Entwickler-Landkarte: Grundlagen (2.–8. Nov)
- D3.js-Integration, Knoten/Kanten aus echten Daten generieren

### Woche 8 — Entwickler-Landkarte: Interaktion (9.–15. Nov)
- Zoom/Pan, Technologie-Filter, mobile Bedienbarkeit

### Woche 9 — GitHub-API-Integration (16.–22. Nov)
- Build-Time-Fetch der Repos, Caching, Fehler-/Ladezustände
- Verknüpfung mit Portfolio-Projekten

### Woche 10 — KI-Assistent: Chatoberfläche (23.–29. Nov)
- Chatfenster, Nachrichteneingabe/-verlauf, vordefinierte Fragen

### Woche 11 — KI-Assistent: Antwortlogik (30. Nov – 6. Dez)
- Regelbasierte Wissensbasis aus Portfolio-Daten
- Navigation aus Chatantworten, Umgang mit unbekannten Fragen

### Woche 12 — Echte KI-Anbindung (7.–13. Dez)
- Auswahl KI-Dienst, sicherer Backend-Endpunkt
- Frontend-Backend-Verbindung, Rate-Limiting

### Woche 13 — Integration aller Hauptfunktionen (14.–20. Dez)
- Lebensreise ↔ Landkarte ↔ Assistent verknüpfen
- Gemeinsame Datenbasis konsolidieren, End-to-End-Flows testen

### Woche 14 — Responsive Design & Performance (21.–27. Dez)
- Mobile/Tablet-Feinschliff, Bild-/Animationsoptimierung

### Woche 15 — Automatisierte Tests (28. Dez – 3. Jan)
- Unit-Tests für Daten/Filter/Chatbot, GitHub Actions CI

### Woche 16 — Abschluss und Veröffentlichung (4.–10. Jan)
- Gesamttest, Dokumentation, finale Veröffentlichung, Abgabe

## Priorisierung bei Zeitdruck

1. Öffentlich erreichbare, funktionierende Grundversion (jederzeit Pflicht)
2. Lebensreise, Landkarte, KI-Assistent als **Grundfunktionen** vor Erweiterungen
3. Visuelle Erweiterungen und die echte KI-API-Anbindung sind die ersten Kandidaten für eine Verschiebung, falls die Zeit knapp wird — die regelbasierte Assistenten-Version bleibt in jedem Fall funktionsfähig
