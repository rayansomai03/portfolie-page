# PROJECT PROGRESS

> Diese Datei dokumentiert den **tatsächlichen** Entwicklungsstand.
> Der geplante Verlauf steht in [`ROADMAP.md`](./ROADMAP.md).

**Letzte Aktualisierung:** 22. September 2026
**Aktuelle Entwicklungswoche:** Woche 1 von 12
**Abgabe:** 11. Dezember 2026 — bestätigt

## Abgeschlossene Funktionen

**Woche 1 — Projektstart**
- Projektstruktur angelegt (`css/`, `assets/images/`)
- `index.html`: semantisches Grundgerüst mit Navigation, Hero, Über mich,
  drei Funktions-Sektionen als Platzhalter, Kontakt und Footer
- `css/main.css`: Design-Tokens (Farben, Abstände, Radien), Basis-Styles,
  dunkles Theme, Komponenten für Buttons, Karten und Kontaktlinks
- Portrait aus dem Lebenslauf extrahiert und als JPEG optimiert (205 KB → 33 KB)
- `README.md` mit echtem Projektinhalt ersetzt die Platzhalter-`readme.md`
- Barrierefreiheit von Beginn an: Skip-Link, sichtbarer Fokusrahmen,
  `prefers-reduced-motion`

**Noch offen in Woche 1:** GitHub Pages aktivieren (muss Rayan im Repository tun).

## In Bearbeitung

- Veröffentlichung über GitHub Pages

## Verifizierte Inhaltsdaten

Quelle: Lebenslauf 2026 plus Korrekturen von Rayan (22.09.2026).
Nichts davon ist erfunden oder ergänzt.

**Person:** Rayan Somai, Student Wirtschaftsinformatik (BFH Bern)

**Öffentliche Kontaktdaten (freigegeben)**
- E-Mail: rayan.somai@hotmail.com
- GitHub: [@rayansomai03](https://github.com/rayansomai03)
- LinkedIn: https://www.linkedin.com/in/rayansomai/
- Portrait aus dem Lebenslauf: freigegeben

Telefonnummer und Wohnadresse aus dem Lebenslauf werden **nicht** veröffentlicht.

**Bildung**
| Zeitraum | Abschluss | Institution |
|---|---|---|
| 09/2024 – 2027 | Bachelor Wirtschaftsinformatik | BFH Bern |
| 09/2023 – 2024 | Berufsmaturität Wirtschaft | BFB Biel |
| 2020 – 06/2023 | Handelsmittelschule | ESC La Neuveville |

**Berufserfahrung**
- Wird im Portfolio nicht dargestellt (Entscheidung von Rayan).

**Kompetenzen**
- Methodik & Analyse: Systemanalyse & Requirements Engineering, Prozessmodellierung
  (BPMN, UML), IT-Projektmanagement (Scrum, Agile), IT-Sicherheit & Compliance (ITIL)
- Technisch: Datenbankmanagement (R/SQL), Softwareentwicklung (Python)
- Web-Security: OWASP-Schwachstellen praktisch (Juice Shop)
- Neu ab diesem Projekt: HTML, CSS, JavaScript, Git/GitHub, D3.js, GSAP

**Sprachen:** Deutsch (Muttersprache), Französisch (Muttersprache), Englisch B2

**Projekte & Module**
| Projekt | Art | Kontext | Inhalt |
|---|---|---|---|
| OWASP Juice Shop | Praktisch | BFH, Semester 4 | Ausnutzen von Schwachstellen einer bewusst verwundbaren Webanwendung |
| SmartHealth | Konzept & Analyse | Schulprojekt | App-Konzept für KI-gestützte Arztterminbuchung; Service Blueprint, IT-Architektur, Usability |
| HyperWear | Konzept & Planung | Schulprojekt | E-Commerce-Konzept, Projektplanung, Product Backlog |
| Fahrgemeinschafts-App | Analyse & Design | Schulprojekt | Systemanalyse und Lösungsdesign mit Fokus Datenschutz und Benutzerfreundlichkeit |
| Dieses Portfolio | Implementierung | Web Engineering, HS 2026 | Erste eigene Webanwendung |

## Offene Fragen an Rayan

1. **OWASP Juice Shop** — welche Schwachstellen hast du konkret gelöst?
   (Für die Projektdetailansicht in Woche 4. Ohne Angaben bleibt es bei der
   allgemeinen Beschreibung — es wird nichts dazuerfunden.)
2. **Schulprojekte** — Rayan prüft, ob Dokumente oder Screenshots noch vorhanden sind
3. **Portrait in höherer Auflösung** — die Version aus dem PDF hat nur 330×630 px
   und wirkt auf hochauflösenden Displays leicht unscharf. Original vorhanden?

Keine dieser Fragen blockiert Woche 2.

## Bekannte Fehler

- Kein Favicon vorhanden (Browser fragt `/favicon.ico` an, erhält 404). Kosmetisch,
  wird im Designsystem in Woche 2 ergänzt.

## Wichtige technische Entscheidungen

| Datum | Entscheidung | Begründung |
|---|---|---|
| 2026-09-22 | Vanilla HTML/CSS/JS mit ES-Modulen, kein Bundler | GitHub Pages ist statisch; Frameworks bringen laut Bewertungsraster keinen Vorteil |
| 2026-09-22 | GitHub-Repo-Daten per GitHub Action zur Build-Zeit cachen | Unauthentifizierte API erlaubt nur 60 Requests/h pro IP — im Schul-WLAN teilen sich alle eine IP |
| 2026-09-22 | KI-Assistent zweistufig, echte API nur als Stretch Goal | Keine Secrets im Frontend; bei 12 Wochen ohne Puffer nicht einplanbar |
| 2026-09-22 | Listenansicht der Landkarte als Pflichtbestandteil | Barrierefreiheit + Responsivität (15 Punkte) |
| 2026-09-22 | Abgabe 11.12.2026 bestätigt → feature-complete bis 06.12. | Letzte Woche bleibt echter Puffer |
| 2026-09-22 | Landkarte trennt Methodenkompetenz von Implementierungstechnologien | Bildet den realen Werdegang ehrlich ab |
| 2026-09-22 | Berufserfahrung wird nicht dargestellt | Entscheidung von Rayan; Fokus auf IT-Kompetenz |
| 2026-09-22 | Woche 1 ohne JavaScript, Navigation rein mit CSS | Kein defektes Zwischenstadium; echtes Mobilmenü folgt geplant in Woche 2 |
| 2026-09-22 | Platzhalter-Sektionen zeigen offen die geplante Woche | Ehrlicher als leere Bereiche und macht den Fortschritt für Besucher sichtbar |
| 2026-09-22 | Commit-Autorschaft auf Rayan korrigiert, Claude bleibt Co-Author | Die ersten vier Commits liefen versehentlich auf Claude; die Historie soll den eigenen Fortschritt belegen |
| 2026-09-22 | Arbeitsweise ab Woche 2: gemischt nach Schwierigkeit | Einfachere Teile schreibt Rayan selbst, komplexe Teile entstehen mit Erklärung — Verständnis vor Tempo |

## Durchgeführte Tests

**22.09.2026 — Responsivitätstest (Chromium via Playwright)**

| Viewport | Horizontale Scrollbar | Überlaufende Elemente | JS-Fehler |
|---|---|---|---|
| 375 × 812 (Mobile) | nein | keine | keine |
| 768 × 1024 (Tablet) | nein | keine | keine |
| 1440 × 900 (Desktop) | nein | keine | keine |

Zusätzlich geprüft: `index.html`, `css/main.css` und das Portrait werden alle mit
HTTP 200 ausgeliefert.

## Nächster geplanter Entwicklungsschritt

1. **GitHub Pages aktivieren** — K.-o.-Kriterium, muss Rayan im Repository vornehmen
2. **Woche 2 (28.09.–04.10.):** Designsystem ausbauen (Favicon, Typografie festlegen),
   Navigation mit echtem Mobilmenü inklusive JavaScript, CSS in wiederverwendbare
   Komponenten aufteilen
