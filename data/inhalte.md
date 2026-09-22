# Inhalte — Rohdaten für die Portfolio-Datenbasis

Arbeitsdatei von Rayan. Hier sammle ich die Beschreibungen meiner Projekte,
bevor sie in die strukturierten JSON-Dateien überführt werden.

**Wichtig: nicht alles auf einmal.** Nur Projekte, die wirklich etwas zu zeigen
haben, brauchen eine ausgefüllte Karte. Module ohne Projekt bleiben einfach in der
Modulliste in `PROJECT_PROGRESS.md` stehen — das genügt als Kompetenznachweis.

Pro Projekt ca. 5 Minuten. Stichworte reichen, keine ganzen Sätze nötig.

---

## Vorlage zum Kopieren

```
### <Projektname>
- Modul / Semester:
- Aufgabe (1–2 Sätze):
- Mein Beitrag (2–3 Stichpunkte):
- Methoden & Werkzeuge:
- Vorzeigbar (Datei, Screenshot, Link, oder "nichts mehr vorhanden"):
```

---

## Priorität 1 — diese zuerst

### Cybersecurity — CTF-Wettbewerb
- Modul / Semester: Cybersecurity (3 ECTS), Frühlingssemester 2026, Semester 4
- Prüfungsform: Capture-the-Flag-Wettbewerb über das ganze Semester.
  Die gesammelten Punkte bestimmten die Modulnote.
- Drei Challenge-Typen:
  - **Quiz Challenges** — Multiple Choice, ab 75 % richtig gab es einen Flag
  - **Open Challenges** — offene Aufgaben, zu lösen mit Werkzeugen aus den Vorlesungen
  - **OWASP-Top-10-Challenges** — Ausnutzen von Schwachstellen an einer eigenen
    Instanz des OWASP Juice Shop, innerhalb eines begrenzten Zeitfensters
- Themen der Vorlesungen: Grundkonzepte, Security Policies und Design-Prinzipien,
  Web Application Vulnerabilities und Malware, Kryptografie, Security-Mythen,
  Supply-Chain-Angriffe

**Gelöste Challenge-Kategorien** (Angabe von Rayan)

| Kategorie | Schwachstellenklasse |
|---|---|
| SQL Injection | Injection |
| NoSQL Injection | Injection |
| Cross-Site Scripting (XSS) | Injection |
| XML External Entity (XXE) | Security Misconfiguration |
| Insecure Direct Object Reference (IDOR) | Broken Access Control |
| Path Traversal | Broken Access Control |
| JWT-Manipulation | Identification & Authentication Failures |
| TOTP-Bypass | Identification & Authentication Failures |
| RCE-nahe Exploits | Injection / Software Integrity |
| Steganografie | Forensik (Open Challenge) |

**Darstellung im Portfolio**

Das Vorgehen zu den einzelnen Challenges ist nicht mehr erinnerlich (Modul lag im
Frühlingssemester 2026). Die Kategorien werden deshalb als Rückblick auf das Modul
dargestellt, nicht als jederzeit abrufbare Routine. Formulierung sinngemäss:

> Im CTF des Cybersecurity-Moduls Challenges aus zehn Schwachstellenkategorien gelöst.

Keine Detailbeschreibungen einzelner Exploits, solange sie nicht belegbar sind.

**Optional, falls Zeit und Lust:**
Juice Shop läuft lokal in wenigen Minuten (`docker run -p 3000:3000 bkimminich/juice-shop`).
Eine Stunde damit würde ein bis zwei Vorgehensbeschreibungen wieder verfügbar machen —
nice to have, nicht eingeplant.

### Bärnway — nutzerzentriertes Mobilitätskonzept für den Modal Shift in Bern
- Modul / Semester: Projekt 2 — Business Case Study (WPR2 / BBCS), 6 ECTS,
  HS 2025, Gruppe 15
- Betreuung: Anja Habegger, BFH Departement Wirtschaft
- Team (5 Personen): Gabriel Raphael Schüpbach, Natasa Rogers, Jana Lynn Begert,
  Inesa Hamza (alle BBA Betriebsökonomie) und Rayan Somaï (BWI)
  → Rayan war der einzige Wirtschaftsinformatiker im Team und damit die technische Rolle
- Aufgabe: Digitale Anwendung, die Menschen zur häufigeren ÖV-Nutzung motiviert.
  Zielgruppe sind bewusst jene, die den ÖV aus Gewohnheit oder Unsicherheit meiden.

**Belegter eigener Beitrag** (im Bericht als Quelle ausgewiesen)
- **Figma-Prototyp** — „Quelle: Figma, Somaï, Rayan Zineddine, 2025"
- **Trello-Board** zur Projektsteuerung — „Quelle: Trello, Somaï, Rayan Zineddine, 2025"

**Technisches Konzept** (20 Seiten im Produktbericht)
- Zielarchitektur aus Präsentationsschicht, Strapi-Backend und geplantem Routing-Service
- Datenmodelle für Trips, Mobility Services und User; REST-Endpunkte inkl. JSON-Beispielen
- Geplante API-Anbindungen: Transport API / SBB, Bernmobil-Echtzeitdaten,
  Publibike, E-Trottinett-Anbieter, Mobility Carsharing, GTFS
- **Proof of Concept als Jupyter Notebook**: echte API-Abfrage, JSON-Verarbeitung,
  Distanzberechnung über die Haversine-Formel, CO₂-Vergleich Auto (0.171 kg/km)
  gegen ÖV (0.028 kg/km)
- Multikriterieller Routing-Algorithmus: gewichteter Gesamtscore aus Reisezeit,
  Umstiegen und CO₂-Ersparnis statt nur „schnellste Verbindung"
- Ehrliche Einordnung der Umsetzungstiefe nach High/Mid/Low Fidelity
- Benannte Limitationen: API-Rate-Limits, Authentifizierung, fehlende Echtzeit-Endpunkte,
  ungetestete Fehlerbehandlung und Caching

**Datenschutz als Designentscheidung**
Nach dem Interview mit Pascal Mainini (Dozent BFH Technik und Informatik) wurde
die Erfassungslogik neu ausgerichtet: **bewusst gegen automatische GPS-Überwachung**,
stattdessen eine manuelle, datensparsame Lösung ohne vollständige Bewegungsprofile.

**Methodik**
Vier Sprints, agiles Vorgehen, Personas, Customer Journey Mapping,
Segelboot-Retrospektive, 4L-Retrospektive, Figma, Trello.
Experteninterviews: Sabrina Stöckli (Professorin für Social Marketing, BFH),
Pascal Mainini (BFH Technik und Informatik), Yvonne Schönthal (Leiterin
Unternehmensentwicklung, Bernmobil).

**Vorzeigbar**
- **Figma-Prototyp, öffentlich erreichbar:** https://kit-adapt-81309158.figma.site/
  (von Rayan als öffentlich bestätigt, 22.09.2026 — im Portfolio verlinkbar)
- Schlussbericht und Produktbericht liegen als PDF vor

**Screenshots** (gesichert unter `assets/images/baernway/`)

| Datei | Screen | Belegt |
|---|---|---|
| `01-onboarding.webp` | Willkommen, SwissPass-Login oder Gastmodus | Niederschwelliger Einstieg, Gastmodus ohne Konto |
| `02-dashboard.webp` | Startscreen mit „Fahrt starten"-Slider, Schnellzugriff, letzte Fahrt | Start-Stopp-Kernidee, CO₂ pro Fahrt |
| `03-fahrtenuebersicht.webp` | Wochenstatistik (43.4 km, 12 Fahrten, 11.6 kg CO₂), Fahrtenliste | Aggregation, konsistentes Listen-Pattern |
| `04-trip-planner.webp` | Von/Nach, Datum und Zeit, häufige Routen | Smart Trip Planner |
| `05-karte.webp` | Regionale Mobilität mit Anbieterfiltern (ÖV, Velo, Trottinett) | Multimodalität, Publibike/Trottinett/Carsharing |

**Gestalterische Einordnung:** Bärnway nutzt Rot auf Weiss — die Farbwelt von
Bernmobil und der Stadt Bern. Das steht bewusst im Gegensatz zum dunklen
Glassmorphism von MysteryBox. Zwei Projekte, zwei völlig verschiedene Designsprachen,
jeweils passend zum Kontext statt zum persönlichen Geschmack.

Damit ist Bärnway das einzige Projekt mit begehbarem Live-Artefakt. Trotzdem
werden Screenshots im Repository abgelegt: Figma Sites lassen sich jederzeit
unveröffentlichen, das Portfolio soll davon nicht abhängen.

**Autorschaft** (von Rayan bestätigt, 22.09.2026)

Das Kapitel „Technisches Konzept" stammt von Rayan. Zusammen mit dem namentlich
belegten Figma-Prototyp und der Trello-Steuerung war er damit für die gesamte
technische Seite des Projekts verantwortlich: Architektur, Datenmodellierung,
API-Design, Proof of Concept und Prototyp.

Offen (nicht blockierend): Existiert das Jupyter Notebook noch als Datei?

### MysteryBox — Zufällige Lifehacks auf Knopfdruck
- Modul / Semester: Software Engineering (WSEG), Herbstsemester 2025, Semester 3
- Team: Rayan Somai (@somar1), Yasin Masrouhi (@masry1), Nico (@dinha1), Andy (@ruttn3)
- Aufgabe: Web-Applikation als Alternative zum ziellosen Scrollen — per Klick
  kurze, sofort anwendbare Lifehacks. MVP mit Authentifizierung und
  kontextabhängigen Inhalten.

**Technischer Stack**
- Frontend: Vue 3 (Composition API), TypeScript, Vite, Vue Router
- Backend: Strapi Headless CMS, REST API, users-permissions, JWT
- Infrastruktur: GitLab CI/CD, GitLab Pages, Bruno für API-Tests

**Externe API-Integrationen**
- ipapi.co — Standortermittlung
- Open-Meteo — Wetterdaten
- Daraus kontextabhängige Lifehacks („Es ist kalt bei dir — Heizkörper entlüften
  spart Energie.")

**Architektur & Qualität**
- Service-Layer trennt API-Zugriffe von den Views
- Qualitätskriterien nach arc42 / ISO 25010: Functional Suitability und
  Operability (Pflicht), Usability und Modularity (selbstgewählt)
- Single-Page-Application, dunkles UI mit Glassmorphism

**Zustand der Demo** (geprüft 22.09.2026 anhand von Screenshots)

Die Anwendung läuft und ist inhaltlich vollständig: Landing-Page mit Problem-/
Lösungsabschnitt, Feature-Übersicht, Live-API-Demos, Favoriten, Login/Logout.
Gamification ist funktionsfähig (Level 3, 150/200 XP, Badges) — im README noch
als „vorbereitet" beschrieben.

Bemerkenswert für die Darstellung: Bei verweigertem Standortzugriff zeigt die App
„Standortzugriff verweigert" und liefert einen allgemeinen Lifehack statt zu
scheitern. Sichtbare Fehlerbehandlung mit sinnvollem Rückfall — genau das, was
das Bewertungsraster unter „verständliche Fehlermeldungen" versteht.

**Screenshots** (gesichert unter `assets/images/mysterybox/`)

| Datei | Inhalt |
|---|---|
| `01-landing.webp` | Hero mit Gradient-Typografie |
| `02-problem-loesung.webp` | Problem- und Lösungsabschnitt |
| `03-features.webp` | Feature-Karten |
| `04-api-demo.webp` | Live-API-Demos, AI Lifehack Generator |
| `05-kontext-gamification.webp` | Kontext-Lifehack mit Fehlerfall, Fortschritt und Badges |

Browserleisten sind entfernt. Der eingeloggte Zustand („Logout" in der Navigation)
bleibt sichtbar — er belegt die Authentifizierung und ist deshalb erwünscht.
Die Screenshots sind unabhängig davon, ob das GitLab-Deployment bestehen bleibt.

**Links — nicht öffentlich** (geprüft 22.09.2026 im InPrivate-Fenster)

Sowohl das Repository als auch GitLab Pages leiten auf die BFH-Anmeldung um.
Pages Access Control ist auf Projektmitglieder beschränkt. **Keiner dieser Links
wird im Portfolio verlinkt** — ein Link auf eine Login-Maske wirkt schlechter als
gar kein Link.

- Repository (intern): https://gitlab.ti.bfh.ch/dsl-student-projects/wseg-25-hs/mysterybox
- Dokumentation (intern): https://dsl-student-projects.pages.ti.bfh.ch/wseg-25-hs/mysterybox/
- Demo (intern): https://dsl-student-projects.pages.ti.bfh.ch/wseg-25-hs/mysterybox/demo/

**Darstellung im Portfolio:** Screenshots plus Beschreibung des Stacks. Der Hinweis,
dass das Projekt auf der internen Infrastruktur der BFH liegt, ist nachvollziehbar
und muss nicht kaschiert werden.

**Optional für später** (nicht eingeplant, frühestens Oktober): eigene Kopie des
Frontends auf GitHub veröffentlichen und über Netlify oder Cloudflare Pages
deployen. Voraussetzungen: Zugangsdaten vorher aus dem Code und der Git-History
entfernen, Einverständnis des Teams einholen, und prüfen, ob das Frontend ohne das
Strapi-Backend lauffähig ist.

**Eigener Anteil**

Laut Rayan hat er praktisch die gesamte Umsetzung allein erbracht.

*Darstellung im Portfolio:* Es wird beschrieben, **was** Rayan gebaut hat — nicht,
was die anderen nicht beigetragen haben. Aussagen über die Untätigkeit von
Teammitgliedern gehören nicht in ein öffentliches Portfolio: sie sind für Aussenstehende
nicht überprüfbar und wirken auf Personalverantwortliche negativ. Eine konkrete
Aufzählung der eigenen Leistung ist stärker und belegbar.

*Noch zu konkretisieren* (aus der GitLab-Commit-Historie von `@somar1` ablesbar):
- Welche Bereiche stammen von dir? Vorschlag zur Gliederung:
  - Frontend-Architektur (Views, Router, Komponentenstruktur)
  - Service-Layer (`AuthService.ts`, `LifehackService.ts`, `ContextLifehack.ts`, `AiLifehack.ts`)
  - Strapi-Backend und Authentifizierung
  - CI/CD-Pipeline und GitLab Pages
  - Dokumentation (arc42-Qualitätskriterien, Blog)
- Anzahl eigener Commits im Verhältnis zum Team — belegt den Anteil sachlich,
  ohne jemanden zu beschuldigen

---

## Priorität 2 — danach

### SmartHealth
- Modul / Semester:
- Aufgabe: App-Konzept für KI-gestützte Arztterminbuchung
- Mein Beitrag:
- Methoden & Werkzeuge: Service Blueprint, IT-Architektur, Usability
- Vorzeigbar:

### Fahrgemeinschafts-App für Studierende
- Modul / Semester: **Requirements Engineering** (6 ECTS, Grundstudium)
- Dokument: „Systemanforderungen" — Spezifikation nach Hochschulvorlage
  (Template von Reto Schneider), 22 Tabellen, 106 Bearbeitungsstände
- Aufgabe: Hochschulspezifische Plattform, über die BFH-Studierende Fahrten zum
  Campus anbieten und finden können. Ziele: Kostenersparnis, weniger Verkehr und
  CO₂, Entlastung der Parkplatzsituation, soziale Kontakte

**Inhalt der Spezifikation**
- Situationsanalyse: Problemstellung, Mengen und Häufigkeiten, Datenbestände,
  Stärken-/Schwächen- und Ursachenanalyse
- Informationssicherheit und Datenschutz als eigenes Kapitel — ausgehend davon,
  dass die heutige Organisation über WhatsApp- und Facebook-Gruppen weder
  zugriffsbeschränkt noch datenschutzkonform ist
- Systemkontext mit Kontextdiagramm
- **Morphologischer Kasten** zur Lösungsfindung, daraus drei Varianten,
  bewertet nach Zielerreichung und Anforderungsabdeckung, mit begründeter Variantenwahl
- Design-Thinking-Prozess in mehreren Iterationen, MVP-Abgrenzung
- Use Cases mit Use-Case-Diagramm, Detailanforderungen per **Satzschablone** und
  **User-Story-Formular**, Qualitätsanforderungen
- UML: Klassen-, Sequenz-, Aktivitäts- und Zustandsdiagramm
- Anforderungen zu Betriebskonzept, Systemarchitektur, Migrationskonzept und
  ISDS-Konzept — die Struktur folgt **HERMES**, das im Glossar auch genannt wird

**Autorschaft** (von Rayan bestätigt, 22.09.2026)

Josias Odermatt zeichnet die 13 detaillierten Einträge: UC-01 bis UC-07,
US-01 bis US-03 und QA-01 bis QA-03, also Use Cases, User Stories,
Qualitätsanforderungen und das Use-Case-Diagramm.

**Alles Übrige stammt von Rayan:**
- Management Summary, Ausgangslage
- Situationsanalyse mit Mengengerüst, Datenbeständen, Stärken-/Schwächenanalyse
- Kapitel Informationssicherheit und Datenschutz
- Systemkontext und Kontextdiagramm
- Lösungsentwicklung: Business Model Canvas, morphologischer Kasten,
  drei Varianten samt Bewertung und begründeter Variantenwahl
- System- und Produktziele, Grobanforderungen, UI-Skizze
- Technische Spezifikation inklusive **UML-Klassendiagramm**

**Screenshots** (gesichert unter `assets/images/fahrgemeinschaft/`)

| Datei | Inhalt |
|---|---|
| `01-klassendiagramm.webp` | UML-Klassendiagramm: Nutzer, Fahrt, Mitfahranfrage, Bewertung, Chat — mit Attributen, Methoden, Multiplizitäten und Rollennamen |
| `02-business-model-canvas.webp` | Ausgefülltes Business Model Canvas |

Das Use-Case-Diagramm wurde **bewusst nicht** übernommen — es gehört zu Odermatts
Kapitel und darf nicht als eigene Leistung erscheinen.

**Anmerkung:** In einer Tabelle stehen noch Beispielinhalte aus der Vorlage
(„Jede Abteilung kann ihre Events selbständig organisieren"). Falls das Dokument
je gezeigt wird, vorher bereinigen.

**Vorzeigbar:** DOCX vorhanden. Kontextdiagramm, Use-Case-Diagramm und die
UML-Diagramme wären als Bild wertvoll.

### HypeWear — Plattform für virale Modetrends
- Modul / Semester: **Projekt 1 (WPR1)**, Kompetenznachweis 1, eingereicht 21.05.2025
- Experten: Prof. Dr. Anna Wiedemann, Olivier Marti
- Team: Alex Bongarzone, Nico Rüttimann, Yasin Masrouhi, Rayan Somaï
- Aufgabe: Projektauftrag für eine Plattform, die virale Modetrends aus TikTok,
  Instagram und Pinterest erkennt, passende Produkte empfiehlt und direkt kaufbar macht

**Art des Dokuments:** vollständiger Projektauftrag über 38 Seiten — kein Konzeptpapier,
sondern eine klassische Projektmanagement-Arbeit mit:
- Management Summary, Ausgangslage, Zielen und Leistungsumfang
- Projektstrukturplan mit beschriebenen Arbeitspaketen
- Ablauf-, Termin-, Ressourcen- und Kostenplanung
- Stakeholder- und Risikoanalyse
- Wirtschaftlichkeitsrechnung

**Konkrete Zahlen:** Budget 195'100 CHF (155'100 Personal, 40'000 Sachmittel),
Laufzeit 18 Monate, agil und phasenbasiert.

**Kompetenz daraus:** IT-Projektmanagement mit Projektstrukturplan, Aufwandschätzung,
Stakeholder- und Risikoanalyse — belegt den CV-Punkt „IT-Projektmanagement (Scrum, Agile)".

**Eigener Anteil** (von Rayan bestätigt, 22.09.2026): Die **Projektidee stammt von
ihm**, und er war an allen Arbeitspaketen beteiligt. Keine namentliche Kapitel-
zuordnung im Dokument — im Portfolio wird deshalb „Projektidee und Mitarbeit in
allen Arbeitspaketen" formuliert, nicht die alleinige Autorschaft einzelner Teile.

### MedFlow AI — Prozessoptimierung durch KI in einer Arztpraxis
- Modul / Semester: **Prozessmanagement (WPRO)**, Kompetenznachweis 1,
  eingereicht 01.12.2025
- Experten: Prof. Dr. Thiemo Wambsganss, Léane Wettstein
- Team: Rayan Somaï, Yasin Masrouhi (nur zu zweit)
- Aufgabe: Den Aufwand für die Erstellung von Operationsberichten in einer
  chirurgischen Arztpraxis mit KI-gestützter Spracherkennung senken

**Ausgangslage:** Nach jedem Eingriff diktiert der Arzt, die medizinische Assistenz
überträgt das Diktat manuell in Word. 15–20 Minuten pro Bericht, mehrfach täglich,
verteilt über Outlook, Word und Dateiablagen.

**Methodik**
- Stakeholder-Interviews mit vier Gruppen: Arzt, medizinische Assistenz,
  Administration, IT
- Prozesslandkarte und **BPMN-2.0-Modellierung** des IST-Prozesses mit vier Lanes
  (Arzt, medizinische Assistenz, IT-Systeme, Archivierung)
- Wertschöpfungsanalyse jedes Prozessschritts
- Anforderungsanalyse mit Basisanforderungen
- SOLL-Prozess, Machbarkeits- und Wirtschaftlichkeitsbetrachtung

**Regulatorik:** Schweizer Datenschutzgesetz (DSG) und medizinrechtliche
Anforderungen an die Verarbeitung von Gesundheitsdaten wurden als Rahmenbedingung
berücksichtigt.

**Ergebnis:** Geschätzte Zeitersparnis von 50–70 %. *Wichtig: eine Schätzung aus
dem Konzept, keine gemessene Grösse — im Portfolio entsprechend kennzeichnen.*

**Kompetenz daraus:** BPMN 2.0, IST/SOLL-Prozessanalyse, Stakeholder-Interviews,
Anforderungserhebung im regulierten Umfeld — belegt den CV-Punkt
„Prozessmodellierung (BPMN, UML)".

**⚠️ Datenschutz:** Die Präsentation nennt „Praxis Dr. med. Raphael Wirth – Bern"
namentlich. Die schriftliche Hausarbeit anonymisiert dagegen korrekt
(„eine Praxis mit fünf bis zehn Mitarbeitenden"). **Im Portfolio wird die
anonymisierte Variante verwendet** — eine reale Praxis samt Arztnamen gehört nicht
auf eine öffentliche Seite, schon gar nicht in Verbindung mit einer Analyse ihrer
internen Schwachstellen.

**Vorzeigbar:** Hausarbeit (DOCX) und Präsentation (PPTX) vorhanden.
Die BPMN-Diagramme wären als Bild wertvoll.

### Skribble AG — Nachhaltigkeitsanalyse
- Modul / Semester: Sustainable Business (3 ECTS), Gruppe C
- Gegenstand: Skribble AG, Schweizer TrustTech-Scale-up für rechtsgültige
  elektronische Signaturen (gegründet 2018, Zürich, rund 60 Mitarbeitende)
- Team: Yasin Masrouhi, Nico Janick Rüttimann, Danijel Marjanovic,
  Andy Minh Vu Dinh, Rayan Somaï

**Rayans Sektion: „Digital Artefacts" (Folien 26–31, namentlich ausgewiesen)**

Analyse der ökologischen Wirkung von Softwarearchitektur, jeweils mit Chancen
*und* Risiken:

| Thema | Chancen | Risiken |
|---|---|---|
| Energy-aware software design | weniger CPU-Zeit, Speicher und Netzverkehr pro Signatur; geringere Cloud-Kosten; bessere Performance | Refactoring-Aufwand; überoptimierter Code wird schwer wartbar; **Rebound-Effekt** — billigere Signaturen erhöhen das Gesamtvolumen und fressen die Einsparung auf |
| Sustainable data lifecycle | Retention und Kompression senken Speicherbedarf; weniger Kosten; geringeres Datenschutzrisiko durch Löschen | falsche Aufbewahrungsregeln löschen rechtlich nötige Nachweise; Migrationsrisiko; Governance-Aufwand |
| Open and modular architecture | längere Systemlebensdauer durch austauschbare Komponenten; keine Vendor-Lock-ins; Wiederverwendung | mehr Schnittstellen erhöhen Komplexität; **jede zusätzliche API ist Angriffsfläche**; Koordinationsaufwand |

Bemerkenswert: Die Analyse benennt durchgehend auch die Gegenseite — Rebound-Effekt,
Wartbarkeitsverlust durch Überoptimierung, Angriffsfläche durch Modularisierung.
Das ist Abwägung statt Nachhaltigkeits-Marketing.

**Kompetenz daraus:** Green IT und nachhaltige Softwarearchitektur.

**Anschluss ans eigene Portfolio:** Dieselbe Denkweise ist in diesem Projekt
bereits angewandt — kein Framework, optimierte Bilder (Portrait 205 KB → 33 KB),
statisches Hosting, GitHub-API-Caching statt wiederholter Requests. Könnte im
Portfolio als bewusste Entscheidung sichtbar gemacht werden.

**Vorzeigbar:** Präsentation als PPTX vorhanden.

### Business Gaming mit TOPSIM
- Modul / Semester:
- Aufgabe:
- Mein Beitrag:
- Ergebnis (Platzierung, Kennzahlen, Erkenntnis):
- Vorzeigbar:

---

## Priorität 3 — nur falls Zeit bleibt

Alles Übrige. Module ohne eigenes Projekt müssen hier nicht auftauchen.
