# PROJECT PROGRESS

> Diese Datei dokumentiert den **tatsächlichen** Entwicklungsstand.
> Der geplante Verlauf steht in [`ROADMAP.md`](./ROADMAP.md).

**Letzte Aktualisierung:** 22. September 2026
**Aktuelle Entwicklungswoche:** Woche 1 (Projektstart) — Vorbereitungsphase

## Abgeschlossene Funktionen

- _Noch keine._ Das Repository enthält bisher nur eine Platzhalter-`readme.md` (Commit `a022987`).

## In Bearbeitung

- Analyse der Projektanforderungen und Festlegung der technischen Architektur
- Erstellung der Planungsdokumente (`ROADMAP.md`, `PROJECT_PROGRESS.md`)

## Offene Aufgaben (nächste Schritte, Woche 1)

- [ ] Ordnerstruktur anlegen (`css/`, `js/`, `data/`, `assets/`, `tests/`, `.github/workflows/`)
- [ ] `readme.md` → `README.md` umbenennen und mit echtem Projektinhalt füllen
- [ ] HTML-Grundgerüst (`index.html`) mit semantischen Sektionen erstellen
- [ ] Minimales Basis-CSS, damit die erste Version präsentabel ist
- [ ] GitHub Pages aktivieren und öffentliche URL prüfen
- [ ] Persönliche Daten sammeln (Werdegang, Projekte, Technologien) — wird von mir (Rayan) geliefert

## Bekannte Fehler

- Keine.

## Wichtige technische Entscheidungen

| Datum | Entscheidung | Begründung |
|---|---|---|
| 2026-09-22 | Vanilla HTML/CSS/JS mit ES-Modulen, kein Bundler | GitHub Pages ist statisch; hält die Lernkurve für Anfänger flach und den Code nachvollziehbar |
| 2026-09-22 | GitHub-Repo-Daten per GitHub Action zur Build-Zeit holen statt live im Browser | Unauthentifizierte GitHub-API erlaubt nur 60 Requests/Stunde pro Besucher-IP |
| 2026-09-22 | KI-Assistent zweistufig: regelbasiert zuerst, echte KI-API später über separates Backend | Keine Secrets im Frontend; Abgabe ist auch ohne KI-API vollständig funktionsfähig |
| 2026-09-22 | Listenansicht der Entwickler-Landkarte als fester Bestandteil, nicht als Option | Barrierefreiheit und Bedienbarkeit auf Smartphones |

## Durchgeführte Tests

- Keine. Testinfrastruktur folgt in Woche 15 (bzw. früher, sobald es testbare Logik gibt).

## Nächster geplanter Entwicklungsschritt

Woche 1: Projektstruktur anlegen, HTML-Grundgerüst erstellen und eine erste
öffentlich erreichbare Version über GitHub Pages veröffentlichen.
Die öffentliche URL ist Voraussetzung für die gesamte Bewertung — deshalb hat
sie höchste Priorität vor allen Features.
