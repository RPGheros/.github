Deutsch | [English](README.en.md)

# ShellRPG-server · v0.0.2

> **Status:** Reversion / normalized release
>
> **Governance-Layer:** SERVER-PRIVAT
>
> **Kurzfassung:** Neu versionierter und konsistent verpackter Stand, der den vorherigen Build auf v0.0.2 normalisiert.

## Zweck dieses Artefakts

Privater, serverautoritiver Kern. Berechnet Weltzustand, Kampf, Städte, Ökonomie, Tick-Logik, Sicht, Belagerungen und Integrität.

## Wozu dieses Artefakt gedacht ist

Dieses Artefakt ist **nicht isoliert** gedacht. Es ist Teil des vierteiligen ShellRPG-Verbunds und arbeitet mit den übrigen Artefakten zusammen:

- ShellRPG-client; ShellRPG-www; ShellRPG-wiki
- gemeinsamer Datenvertrag / gemeinsamer Spielzustand
- konsistente README-, Revisions- und Release-Logik

## Was in dieser Version enthalten ist

- Version normalisiert
- TOML-Dateien aktualisiert
- Packaging bereinigt
- Tests/Health geprüft

## Verknüpfung mit den anderen Artefakten

- **Server** bleibt immer die Wahrheitsquelle für kritische Simulation.
- **Client** und **WWW** sind zwei öffentliche Interaktionsschichten für denselben Kern.
- **Wiki** dokumentiert Spiel, Bedienung und Architektur redigiert.

## Typische Ordnerstruktur

- `src/shellrpg_server/`
- `docs-private/`
- `tests/`
- `pyproject.toml`
- `shellrpg.manifest.toml`

## Voraussetzungen

- Python 3.11 oder neuer für Python-Artefakte
- Browser für `ShellRPG-www`
- optional Git für lokale Repository-Arbeit
- unter Windows empfohlen: PowerShell oder CMD

## Build / Installation

```bash
python -m pip install -e .
python -m pip install build pytest
```

## Start / Ausführung

```bash
python -m shellrpg_server
```

## Tests / Validierung

```bash
pytest
```

## Empfohlene Startreihenfolge im Projektverbund

1. `ShellRPG-server` starten
2. danach `ShellRPG-client` **oder** `ShellRPG-www`
3. `ShellRPG-wiki` als Handbuch / redigierte Referenz verwenden

## Wichtige Bedienhinweise

- Diese Version ist als **Reversion / normalized release** zu lesen, nicht als finaler Gesamtstand.
- Änderungen an einem Artefakt müssen immer gegen Server, beide Clients und Wiki mitgedacht werden.
- Reine Build-/Bugfixes erhöhen gemäß Projektregel **nicht** automatisch die Versionsnummer.

## Google AdSense / Monetarisierung

Für dieses Artefakt gilt: Eine GitHub-`README.md` ist Dokumentation, **keine** geeignete AdSense-Auslieferungsfläche. Monetarisierung gehört – wenn überhaupt – in eine **separat gehostete Weboberfläche** oder Dokumentationsseite, nicht in die Projekt-README selbst.

Praktisch bedeutet das für ShellRPG:

- AdSense gehört eher in eine eigenständig gehostete Informations-/Projektseite oder in eine öffentliche Dokumentationsseite außerhalb von GitHub-README-Rendering.
- `ShellRPG-www` ist der sinnvollere technische Kandidat für eine spätere, sauber getrennte Monetarisierungsschicht.
- Der private Server und die redigierte Wiki-Doku müssen von Werbe- und Tracking-Entscheidungen getrennt betrachtet werden.

## Für wen diese README gedacht ist

- Owner / Entwickler
- Mitwirkende
- Tester
- GitHub-Besucher, die schnell verstehen müssen:
  - was dieses Artefakt tut
  - wozu es gedacht ist
  - wie es gebaut wird
  - wie es mit den anderen Artefakten zusammenspielt

## Release- und Revisionshinweise

- Zielstand: **v0.0.2**
- Deutsche Haupt-README: `README.md`
- Englische Fassung: `README.en.md`
- Zu jedem relevanten Release müssen README und Dokumentation mitgezogen werden
- ZIP-Artefakte werden je Artefakt getrennt ausgeliefert

## Troubleshooting

### Paket startet nicht
- Python-Version prüfen
- virtuelle Umgebung aktivieren
- `pip install -e .` erneut ausführen

### Server/Client sprechen nicht miteinander
- zuerst `ShellRPG-server` starten
- Host/Port prüfen
- lokale Firewall / Browser-Origin prüfen

### WWW zeigt nichts an
- statischen Webserver nutzen
- Browser-Konsole prüfen
- sicherstellen, dass der Server parallel läuft

### Wiki wirkt unvollständig
- das ist je nach Version normal, solange der Ausbaupfad dokumentiert ist
- redigierte Inhalte sind absichtlich nicht gleichbedeutend mit privater Serverdoku

## Abschluss

Diese README ist bewusst ausführlich, damit ein Besucher oder Mitwirkender ohne Vorwissen verstehen kann, **was ShellRPG-server ist, was es nicht ist und wie es in den ShellRPG-Verbund passt**.
