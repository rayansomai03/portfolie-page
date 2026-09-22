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
- Modul / Semester: Business Case Study (WPR2 / BBCS), HS 2025, Gruppe 15
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

**Vorzeigbar:** Schlussbericht und Produktbericht liegen als PDF vor.

**Noch von Rayan zu bestätigen:**
- Stammt das Kapitel „Technisches Konzept" von dir? Als einziger WI im Team liegt
  das nahe, aber es steht nicht namentlich im Bericht.
- Hast du das Jupyter Notebook geschrieben? Existiert es noch?
- Gibt es Screenshots oder einen Exportlink des Figma-Prototyps?

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

### Fahrgemeinschafts-App
- Modul / Semester:
- Aufgabe: Systemanalyse und Lösungsdesign
- Mein Beitrag:
- Methoden & Werkzeuge: Fokus Datenschutz und Benutzerfreundlichkeit
- Vorzeigbar:

### HyperWear
- Modul / Semester:
- Aufgabe: E-Commerce-Konzept
- Mein Beitrag:
- Methoden & Werkzeuge: Projektplanung, Product Backlog
- Vorzeigbar:

### Business Gaming mit TOPSIM
- Modul / Semester:
- Aufgabe:
- Mein Beitrag:
- Ergebnis (Platzierung, Kennzahlen, Erkenntnis):
- Vorzeigbar:

---

## Priorität 3 — nur falls Zeit bleibt

Alles Übrige. Module ohne eigenes Projekt müssen hier nicht auftauchen.
