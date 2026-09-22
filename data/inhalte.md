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

### Projekt 2
- Modul / Semester: Projekt 2 (6 ECTS)
- Aufgabe:
- Mein Beitrag:
- Methoden & Werkzeuge:
- Vorzeigbar:

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

**Links** (vor Verlinkung im Portfolio auf öffentliche Erreichbarkeit prüfen)
- Repository: https://gitlab.ti.bfh.ch/dsl-student-projects/wseg-25-hs/mysterybox
- Dokumentation: https://dsl-student-projects.pages.ti.bfh.ch/wseg-25-hs/mysterybox/
- Live-Demo: https://dsl-student-projects.pages.ti.bfh.ch/wseg-25-hs/mysterybox/demo/

**Noch von Rayan auszufüllen:**
- **Was war dein Anteil im Viererteam?** Welche Dateien, Features oder Bereiche
  hast du übernommen? Das ist die einzige offene Frage — ohne sie beschreibt das
  Portfolio nur das Teamprojekt, nicht deinen Beitrag daran.

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
