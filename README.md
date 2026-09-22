# Beyond the Portfolio — My Interactive Developer Journey

Interaktives Portfolio von **Rayan Somai**, Student der Wirtschaftsinformatik an der
Berner Fachhochschule. Einzelarbeit im Modul *Web Engineering* (HS 2026).

🔗 **Live:** _wird nach Aktivierung von GitHub Pages ergänzt_

## Über das Projekt

Statt einer klassischen Portfolio-Seite entsteht eine Webanwendung aus drei
Funktionen, die auf **einer gemeinsamen Datenbasis** aufbauen:

| Funktion | Beschreibung | Status |
|---|---|---|
| **Interaktive Lebensreise** | Animierte Timeline von Ausbildung und Projekten | geplant (Woche 5–6) |
| **Entwickler-Landkarte** | Kompetenzen und Projekte als D3.js-Netzwerk | geplant (Woche 7–8) |
| **KI-Assistent** | Chatbot, der aus den Portfolio-Daten antwortet | geplant (Woche 10–11) |

Weil alle drei dieselben JSON-Quellen lesen, wird ein neues Projekt nur an einer
Stelle gepflegt und erscheint überall.

## Technischer Stack

- **HTML5, CSS3, JavaScript (ES-Module)** — ohne Framework und ohne Build-Schritt
- **D3.js** für die Netzwerkvisualisierung
- **GSAP** für Scroll-Animationen
- **GitHub REST API**, per GitHub Action zur Build-Zeit gecacht
- **GitHub Pages** als Hosting

Bewusst kein Framework: Die Seite ist statisch, und das Bewertungsraster des Moduls
bewertet Frameworks neutral. Vanilla JS hält den Code nachvollziehbar.

## Projektstruktur

```
portfolie-page/
├── index.html              Einstiegsseite
├── css/
│   └── main.css            Design-Tokens, Basis- und Komponenten-Styles
├── assets/
│   └── images/             Bilder
├── ROADMAP.md              Geplanter Verlauf, Architektur, Risiken
└── PROJECT_PROGRESS.md     Tatsächlicher Stand, Entscheidungen, offene Punkte
```

Ordner für `js/`, `data/` und `tests/` entstehen, sobald sie gebraucht werden.

## Lokal starten

Die Seite braucht keinen Build-Schritt. Für lokales Testen genügt ein einfacher Webserver:

```bash
npx http-server .
```

Alternativ die Erweiterung *Live Server* in Visual Studio Code verwenden.
Ein direktes Öffnen der Datei über `file://` funktioniert für die Startseite,
scheitert aber später am Laden der JSON-Daten.

## Dokumentation

- [`ROADMAP.md`](./ROADMAP.md) — was geplant ist, inklusive Architekturentscheidungen und Risiken
- [`PROJECT_PROGRESS.md`](./PROJECT_PROGRESS.md) — was tatsächlich umgesetzt ist

## Arbeitsweise und KI-Einsatz

Dieses Projekt entsteht mit Unterstützung von Claude Code als Programmiermentor.
Der Einsatz wird offen dokumentiert statt verborgen:

- Commits, an denen die KI beteiligt war, tragen eine `Co-Authored-By`-Zeile.
  Commits ohne diese Zeile stammen ausschliesslich von mir.
- Komplexe Themen wie die D3.js-Visualisierung entstehen mit Unterstützung und
  ausführlicher Erklärung; einfachere Teile schreibe ich selbst.
- Alle **inhaltlichen** Angaben stammen aus meinem Lebenslauf und meinen echten
  Projekten. Es werden keine Technologien, Projekte oder Erfahrungen erfunden.
- Technische Entscheidungen und ihre Begründungen sind in
  [`PROJECT_PROGRESS.md`](./PROJECT_PROGRESS.md) festgehalten — inklusive der
  Abwägungen, die zu ihnen geführt haben.

Ziel ist nicht, möglichst schnell ein Ergebnis zu erhalten, sondern die
eingesetzten Techniken zu verstehen und begründen zu können.

## Kontakt

- E-Mail: rayan.somai@hotmail.com
- GitHub: [@rayansomai03](https://github.com/rayansomai03)
- LinkedIn: [rayansomai](https://www.linkedin.com/in/rayansomai/)
