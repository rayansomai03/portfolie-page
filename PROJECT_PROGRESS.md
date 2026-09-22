# PROJECT PROGRESS

> Diese Datei dokumentiert den **tatsächlichen** Entwicklungsstand.
> Der geplante Verlauf steht in [`ROADMAP.md`](./ROADMAP.md).

**Letzte Aktualisierung:** 22. September 2026
**Aktuelle Entwicklungswoche:** Woche 1 von 12 (Projektstart)
**Abgabe:** 11. Dezember 2026 — bestätigt

## Abgeschlossene Funktionen

- _Noch keine._ Das Repository enthält bisher nur eine Platzhalter-`readme.md`
  (Commit `a022987`) sowie die Planungsdokumente.

## In Bearbeitung

- Aufbereitung der persönlichen Daten für die gemeinsame Datenbasis

## Verifizierte Inhaltsdaten

Quelle: Lebenslauf 2026 plus Korrekturen von Rayan (22.09.2026).
Nichts davon ist erfunden oder ergänzt.

**Person:** Rayan Somai, Student Wirtschaftsinformatik (BFH Bern)

**Öffentliche Kontaktdaten (freigegeben)**
- E-Mail: rayan.somai@hotmail.com
- GitHub: `rayansomai03`
- LinkedIn: vorhanden — URL ausstehend

Telefonnummer und Wohnadresse aus dem Lebenslauf werden **nicht** veröffentlicht.

**Bildung**
| Zeitraum | Abschluss | Institution |
|---|---|---|
| 09/2024 – 2027 | Bachelor Wirtschaftsinformatik | BFH Bern |
| 09/2023 – 2024 | Berufsmaturität Wirtschaft | BFB Biel |
| bis 06/2023 | Handelsmittelschule | ESC La Neuveville |

**Berufserfahrung**
- Wird im Portfolio nicht dargestellt (auf Wunsch von Rayan entfernt).

**Kompetenzen**
- Methodik & Analyse: Systemanalyse & Requirements Engineering, Prozessmodellierung
  (BPMN, UML), IT-Projektmanagement (Scrum, Agile), IT-Sicherheit & Compliance (ITIL)
- Technisch: Datenbankmanagement (R/SQL), Softwareentwicklung (Python)
- Web-Security: OWASP-Schwachstellen praktisch (Juice Shop)
- Neu ab diesem Projekt: HTML, CSS, JavaScript, Git/GitHub, D3.js, GSAP

**Sprachen:** Deutsch (Muttersprache), Französisch (Muttersprache), Englisch B2

**Projekte & Module**
| Projekt | Art | Inhalt |
|---|---|---|
| OWASP Juice Shop | Cybersecurity-Modul, praktisch | Ausnutzen von Schwachstellen einer bewusst verwundbaren Webanwendung |
| SmartHealth | Konzept & Analyse | App-Konzept für KI-gestützte Arztterminbuchung; Service Blueprint, IT-Architektur, Usability |
| HyperWear | Konzept & Planung | E-Commerce-Konzept, Projektplanung, Product Backlog |
| Fahrgemeinschafts-App | Analyse & Design | Systemanalyse und Lösungsdesign mit Fokus Datenschutz und Benutzerfreundlichkeit |
| Dieses Portfolio | Implementierung | Erste eigene Webanwendung — Teil der Lebensreise |

## Offene Fragen an Rayan

1. **LinkedIn-URL** — für den Kontaktbereich (Woche 3)
2. **ESC La Neuveville** — Startjahr? (Abschluss 06/2023 ist bekannt)
3. **OWASP Juice Shop** — an welcher Schule, in welchem Semester, und welche
   Schwachstellen hast du konkret gelöst? Gibt es eine Abgabe/Dokumentation dazu?
4. **Schulprojekte** — Rayan prüft, ob Dokumente oder Screenshots noch vorhanden sind
5. **Foto** — soll das Lebenslauf-Portrait auf die Seite?

Keine dieser Fragen blockiert Woche 1 oder 2.

## Bekannte Fehler

- Keine.

## Wichtige technische Entscheidungen

| Datum | Entscheidung | Begründung |
|---|---|---|
| 2026-09-22 | Vanilla HTML/CSS/JS mit ES-Modulen, kein Bundler | GitHub Pages ist statisch; Frameworks bringen laut Bewertungsraster keinen Vorteil |
| 2026-09-22 | GitHub-Repo-Daten per GitHub Action zur Build-Zeit cachen | Unauthentifizierte API erlaubt nur 60 Requests/h pro IP — im Schul-WLAN teilen sich alle eine IP |
| 2026-09-22 | KI-Assistent zweistufig, echte API nur als Stretch Goal | Keine Secrets im Frontend; bei 12 Wochen ohne Puffer nicht einplanbar |
| 2026-09-22 | Listenansicht der Landkarte als Pflichtbestandteil | Barrierefreiheit + Responsivität (15 Punkte) |
| 2026-09-22 | Abgabe 11.12.2026 bestätigt → feature-complete bis 06.12. | Letzte Woche bleibt echter Puffer |
| 2026-09-22 | Landkarte trennt Methodenkompetenz von Implementierungstechnologien | Bildet den realen Werdegang ehrlich ab |
| 2026-09-22 | Berufserfahrung wird nicht dargestellt | Entscheidung von Rayan; Portfolio fokussiert auf IT-Kompetenz |

## Durchgeführte Tests

- Keine. Testinfrastruktur folgt, sobald testbare Logik existiert (geplant ab Woche 4).

## Nächster geplanter Entwicklungsschritt

**Woche 1 (22.–27.09.2026):**
Ordnerstruktur anlegen, `README.md` mit echtem Inhalt, semantisches `index.html`,
minimales Basis-CSS im dunklen Theme, GitHub Pages aktivieren und öffentliche URL prüfen.

Die öffentliche URL ist K.-o.-Kriterium der Bewertung und hat Vorrang vor allen Features.
