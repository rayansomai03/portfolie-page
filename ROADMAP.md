# ROADMAP — Beyond the Portfolio: My Interactive Developer Journey

> Diese Datei beschreibt den **geplanten** Entwicklungsverlauf.
> Der **tatsächliche** Fortschritt steht in [`PROJECT_PROGRESS.md`](./PROJECT_PROGRESS.md).
> Massgeblich für den echten Codestand ist immer die Git-History.

**Modul:** Web Engineering, BFH Bern (Dozent: Syrian Hadad)
**Gewichtung:** Einzelarbeit 60 % der Modulnote, Moodle-Prüfung 40 %
**Entwicklungsstart:** 22. September 2026

## ⚠️ Terminrisiko (offen, muss geklärt werden)

Die Moduleinführung enthält widersprüchliche Angaben:

| Quelle | Angabe |
|---|---|
| Folie „Informationen zu den Prüfungen" | Einzelarbeit **18.02.2026 – 29.05.2026** |
| Folie „Termine" | Unterricht **18.09.2026 – 11.12.2026** (letzte Session: „Testautomatisierungen und Abschluss") |
| Ursprüngliche Annahme | Abgabe Januar 2027 |

Der Zeitraum 18.02.–29.05.2026 stammt vermutlich aus dem Frühlingssemester und wurde
in den Folien nicht aktualisiert. Belegt ist nur, dass der Unterricht am **11.12.2026** endet.
Eine Abgabe im Januar 2027 ist damit **nicht bestätigt**.

**Konsequenz für die Planung:** Wir planen so, dass am **11. Dezember 2026** eine
vollständig abgabefähige Version existiert. Der Zeitraum danach bis Januar ist Puffer
für Feinschliff und die optionale echte KI-Anbindung — nicht für Kernfunktionen.
Diese Planung ist in beiden Fällen sicher.

**To-do:** Abgabetermin bei Syrian Hadad (syrian.hadad@bfh.ch) oder auf Moodle bestätigen lassen.

## Bewertungskriterien (aus der Moduleinführung)

| # | Kriterium | Punkte | Wie unser Konzept das adressiert |
|---|---|---|---|
| 1 | **Erreichbarkeit** auf GitHub Pages | **K.-o.** | Live-Version bereits in Woche 1, danach durchgehend erreichbar |
| 2 | Responsivität | 15 | Mobile-First-CSS, Media Queries, Listenansicht der Landkarte, keine horizontalen Scrollbars |
| 3 | Codequalität & Komplexität | 20 | ES-Module, Trennung HTML/CSS/JS, D3.js, GitHub-API mit Caching, dynamisches Rendering aus JSON |
| 4 | Commit-History | 10 | Regelmässige Conventional Commits über die gesamte Projektdauer ab 22.09. |
| 5 | Gestaltung & Funktionalität | 15 | Konsistentes Designsystem, klare Navigation, drei sinnvoll integrierte Hauptfunktionen |
| | **Total** | **60** | |

Für die vollen 20 Punkte bei Kriterium 3 nennt die Bewertung explizit:
*„Komplexe API-Integrationen: Datenkombination", „Effiziente Datenverarbeitung: Caching,
Pagination", „Komplexe Third-Party-Integrationen: z. B. D3.js für Diagramme"*.
Genau diese drei Punkte sind der Kern unseres Konzepts.

Für die vollen 10 Punkte bei Kriterium 4 gilt: *„Gleichmässig über die gesamte
Projektdauer verteilt"* — Commits ab heute, nicht gebündelt am Ende.

## Projektvision

Drei verknüpfte Hauptfunktionen auf **einer** gemeinsamen Datenbasis:

1. **Interaktive Lebensreise** — animierte Timeline des Werdegangs
2. **Interaktive Entwickler-Landkarte** — D3.js-Netzwerk aus Kompetenzen & Projekten
3. **Persönlicher KI-Assistent** — Chatbot, der aus den echten Portfolio-Daten antwortet

Gemeinsame Quellen: `data/profile.json`, `data/projects.json`, `data/timeline.json`.
Ein neues Projekt wird an *einer* Stelle gepflegt und erscheint in allen drei Funktionen.

### Inhaltliche Leitlinie: Ehrlichkeit als Stärke

Der Lebenslauf zeigt Schwerpunkte in **Analyse, Konzeption und Datenbanken**
(Requirements Engineering, BPMN/UML, R/SQL, Python, Scrum/ITIL) — nicht in Webentwicklung.
Die drei Schulprojekte (SmartHealth, HyperWear, Fahrgemeinschafts-App) sind
Konzept- und Analysearbeiten, keine Code-Repositories.

Die Landkarte unterscheidet deshalb sauber zwischen:

- **Methoden- & Analysekompetenz** (Requirements Engineering, BPMN, UML, Scrum, ITIL)
- **Technische Umsetzung** (Python, R, SQL — und ab jetzt HTML, CSS, JavaScript, Git)

Dieses Portfolio ist das erste echte Webentwicklungsprojekt. Das ist keine Schwäche,
sondern die Erzählung: Die Lebensreise endet dort, wo die Seite selbst entsteht.
Es werden keine Projekte, Technologien oder Erfahrungen erfunden.

## Technische Architektur

| Bereich | Entscheidung | Begründung |
|---|---|---|
| Frontend | Vanilla HTML5/CSS3/JS mit ES-Modulen, kein Bundler | GitHub Pages ist statisch; Frameworks bringen laut Bewertung keinen Vorteil |
| Animation | GSAP + ScrollTrigger (CDN) | Performante Scroll-Animationen |
| Visualisierung | D3.js Force-Directed Graph (CDN) | In der Bewertung namentlich als Beispiel für 20 Punkte genannt |
| Daten | Statische JSON-Dateien unter `data/` | Zentral pflegbar, von allen drei Funktionen genutzt |
| GitHub-Repos | **Build-Time-Fetch** per GitHub Action → `data/github-cache.json` | Unauthentifizierte GitHub-API: nur 60 Requests/h pro IP. In einem Schul-WLAN teilen sich alle eine IP — Live-Fetch wäre bei der Bewertung leer |
| KI-Backend | Separater Serverless-Endpunkt (z. B. Cloudflare Worker) | GitHub Pages kann keine Secrets halten; API-Keys gehören nie ins Frontend |
| Tests | Vitest + GitHub Actions | Datenverarbeitung, Filter, Chatbot-Logik |
| Fallback | Regelbasierte Assistenten-Logik bleibt dauerhaft aktiv | Abgabe funktioniert auch ohne echte KI-API |

### Risiken

| Risiko | Schweregrad | Gegenmassnahme |
|---|---|---|
| Abgabetermin unklar (siehe oben) | **Hoch** | Abgabefähig ab 11.12.2026 planen; Termin beim Dozenten klären |
| GitHub-API-Limit (60/h/IP) | Mittel | Build-Time-Caching statt Client-Fetch |
| API-Keys im Frontend | **Hoch** (Sicherheit) | KI nur über externes Backend; Stufe 2 bleibt Fallback |
| D3-Graph auf Touchscreens | Mittel | Listenansicht als Pflichtbestandteil, nicht als Option |
| GSAP + D3 Ladezeit | Niedrig | `defer`, CDN, `prefers-reduced-motion` respektieren |
| Zeitdruck durch Nebenjob/Studium | Mittel | Kernfunktionen zuerst, Erweiterungen strikt danach |

## Wochenplan (Kernphase bis 11.12.2026)

Die Unterrichtstermine sind eingetragen — mehrere Themen werden im Unterricht
behandelt, kurz bevor wir sie brauchen.

| Woche | Zeitraum | Ziel |
|---|---|---|
| **1** | 22.–27.09 | Projektstruktur, HTML-Grundgerüst, **GitHub Pages live** |
| **2** | 28.09.–04.10 | Designsystem (Farben, Typografie, Tokens), responsive Navigation *(Unterricht 02.10.)* |
| **3** | 05.–11.10 | Hero-Section, Über-mich, Datenbasis `profile.json` |
| **4** | 12.–18.10 | Projektübersicht dynamisch aus `projects.json`, Filter *(Unterricht 16.10.: Web-Design & UX)* |
| **5** | 19.–25.10 | Lebensreise: Datenmodell, Timeline-Layout, Rendering |
| **6** | 26.10.–01.11 | Lebensreise: GSAP-Scroll-Animationen, Detailansichten, Barrierefreiheit *(Unterricht 30.10.: Architektur & APIs)* |
| **7** | 02.–08.11 | Entwickler-Landkarte: D3-Integration, Graph aus echten Daten |
| **8** | 09.–15.11 | Landkarte: Zoom/Pan, Filter, **Listenansicht** für Mobile *(Unterricht 13.11.: Sicherheit, asynchron)* |
| **9** | 16.–22.11 | GitHub-API: Action, Caching, Lade-/Fehlerzustände, Verknüpfung mit Projekten |
| **10** | 23.–29.11 | KI-Assistent: Chatoberfläche, Nachrichten, vordefinierte Fragen *(Unterricht 27.11.: APIs Hands-On)* |
| **11** | 30.11.–06.12 | KI-Assistent: regelbasierte Antwortlogik aus Portfolio-Daten, Navigation aus Antworten |
| **12** | 07.–11.12 | Integration aller drei Funktionen, Responsive-Feinschliff, Tests, **abgabefähige Version** *(Unterricht 11.12.: Testautomatisierung & Abschluss)* |

## Pufferphase (12.12.2026 – 10.01.2027)

Nur falls der Abgabetermin tatsächlich im Januar liegt — sonst entfällt dieser Teil.

- Echte KI-Anbindung (Stufe 3) über sicheres Backend
- Testabdeckung ausbauen, CI-Workflow verfeinern
- Performance-Optimierung, Lighthouse-Durchlauf
- README und technische Dokumentation abschliessen

## Priorisierung bei Zeitdruck

1. **Öffentlich erreichbare Seite** — K.-o.-Kriterium, hat immer Vorrang
2. Responsivität und saubere Codestruktur — 35 der 60 Punkte
3. Grundfunktionen der drei Hauptfeatures
4. Erweiterungen, Animationsdetails, echte KI-API — zuerst streichbar

Die regelbasierte Assistenten-Version bleibt in jedem Szenario funktionsfähig.
