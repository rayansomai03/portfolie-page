# PROJECT PROGRESS

> Diese Datei dokumentiert den **tatsächlichen** Entwicklungsstand.
> Der geplante Verlauf steht in [`ROADMAP.md`](./ROADMAP.md).

**Letzte Aktualisierung:** 22. September 2026
**Aktuelle Entwicklungswoche:** Woche 1 (Projektstart) — Vorbereitungsphase

## Abgeschlossene Funktionen

- _Noch keine._ Das Repository enthält bisher nur eine Platzhalter-`readme.md` (Commit `a022987`)
  sowie die beiden Planungsdokumente.

## In Bearbeitung

- Analyse der Anforderungen aus der Moduleinführung und Festlegung der Architektur
- Aufbereitung der persönlichen Daten aus dem Lebenslauf

## Verifizierte Inhaltsdaten (Quelle: Lebenslauf, Stand 2026)

Diese Angaben stammen aus dem gelieferten Lebenslauf und werden für die Datenbasis verwendet.
Nichts davon wurde erfunden oder ergänzt.

**Person:** Rayan Somai, Student Wirtschaftsinformatik

**Bildung**
| Zeitraum | Abschluss | Institution |
|---|---|---|
| 2024–2027 | Bachelor Wirtschaftsinformatik | BFH Bern |
| 2023–2024 | Berufsmaturität Wirtschaft | BFB Biel |
| 2023–2024 | Handelsmittelschule | ESC La Neuveville |

**Berufserfahrung**
- Avec Shop Lyss — Tankstellenmitarbeiter, seit 05/2026
  (Kundenbetreuung, Kassenbetrieb, Warenbewirtschaftung, Tagesabschluss)

**Kompetenzen**
- Methodik/Analyse: Systemanalyse & Requirements Engineering, Prozessmodellierung (BPMN, UML),
  IT-Projektmanagement (Scrum, Agile), IT-Sicherheit & Compliance (ITIL)
- Technisch: Datenbankmanagement (R/SQL), Softwareentwicklung (Python)
- Neu ab diesem Projekt: HTML, CSS, JavaScript, Git/GitHub

**Sprachen:** Deutsch (Muttersprache), Französisch (Muttersprache), Englisch B2

**Schulprojekte** (Konzept- und Analysearbeiten, keine Code-Repositories)
| Projekt | Inhalt |
|---|---|
| SmartHealth | App-Konzept für KI-gestützte Arztterminbuchung; Service Blueprint, IT-Architektur, Usability |
| HyperWear | E-Commerce-Konzept, Projektplanung, Product Backlog |
| Fahrgemeinschafts-App | Systemanalyse & Lösungsdesign mit Fokus Datenschutz und Benutzerfreundlichkeit |

## Offene Fragen an Rayan (blockieren teilweise die Datenbasis)

1. **Abgabetermin** — Folien nennen 18.02.–29.05.2026 (vermutlich altes Semester),
   Unterricht endet 11.12.2026, Annahme war Januar 2027. Bitte beim Dozenten bestätigen lassen.
2. **Avec Shop Lyss** — Lebenslauf nennt „05/2026 – heute" und gleichzeitig „1 Jahre".
   Was stimmt?
3. **ESC La Neuveville / BFB Biel** — beide mit 2023–2024 angegeben. Überschneidung korrekt?
4. **Öffentliche Kontaktdaten** — welche E-Mail soll auf der Seite stehen
   (`rayan.somai@hotmail.com` oder `rayansomai03@gmail.com`)?
5. **GitHub-Benutzername** — ist `rayansomai03` korrekt? LinkedIn-Profil vorhanden?
6. **Schulprojekte** — existieren dazu Repositories, Dokumente oder Screenshots,
   die verlinkt werden dürfen?

### Datenschutz-Empfehlung

Telefonnummer (079 619 89 55) und Wohnadresse (Rosenweg 5, 2560 Nidau) stehen im Lebenslauf,
gehören aber **nicht** auf eine öffentlich indexierte Webseite. Empfehlung: nur E-Mail,
GitHub und optional LinkedIn veröffentlichen. Der vollständige Lebenslauf kann bei Bedarf
als PDF-Download angeboten werden.

## Bekannte Fehler

- Keine.

## Wichtige technische Entscheidungen

| Datum | Entscheidung | Begründung |
|---|---|---|
| 2026-09-22 | Vanilla HTML/CSS/JS mit ES-Modulen, kein Bundler | GitHub Pages ist statisch; Frameworks bringen laut Bewertungsraster keinen Vorteil |
| 2026-09-22 | GitHub-Repo-Daten per GitHub Action zur Build-Zeit cachen | Unauthentifizierte API erlaubt nur 60 Requests/h pro IP — im Schul-WLAN teilen sich alle eine IP |
| 2026-09-22 | KI-Assistent zweistufig: regelbasiert zuerst, echte API später über externes Backend | Keine Secrets im Frontend; Abgabe ist auch ohne KI-API vollständig |
| 2026-09-22 | Listenansicht der Landkarte als Pflichtbestandteil | Barrierefreiheit + Responsivität (15 Punkte) |
| 2026-09-22 | Planung auf abgabefähige Version per 11.12.2026 statt Januar 2027 | Abgabetermin widersprüchlich; frühere Planung ist in beiden Fällen sicher |
| 2026-09-22 | Landkarte trennt Methodenkompetenz von Implementierungstechnologien | Bildet den realen Lebenslauf ehrlich ab, statt Programmierprojekte zu behaupten |

## Durchgeführte Tests

- Keine. Testinfrastruktur folgt, sobald testbare Logik existiert (geplant ab Woche 4).

## Nächster geplanter Entwicklungsschritt

**Woche 1 (22.–27.09.2026):**
Ordnerstruktur anlegen, `README.md` mit echtem Inhalt, semantisches `index.html`,
minimales Basis-CSS im dunklen Theme, GitHub Pages aktivieren und öffentliche URL prüfen.

Die öffentliche URL ist K.-o.-Kriterium der Bewertung und hat Vorrang vor allen Features.
