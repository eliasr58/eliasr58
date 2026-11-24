# Elias Röhrner

KI-Workflows und Automatisierung mit n8n und Claude, selbst betrieben auf einem eigenen Server. Einzelunternehmer unter Röhrner Automation.

**Stack:** n8n · Claude (Anthropic-API, Claude Code, MCP) · Docker Compose · Postgres · Caddy · Hetzner

## Ausgewählte Projekte

| Projekt | Was es zeigt |
|---|---|
| [Mahnlauf](https://github.com/eliasr58/n8n-production/tree/main/workflows/mahnlauf) | Offene Rechnungen gegen den Kontoauszug abgleichen (CSV und CAMT.053), stufenweise nachfassen, Mahnung erst nach Freigabe. Der Zahlstand wird direkt vor jeder Mail neu gelesen. 225 Tests. |
| [Bewertungsantworten](https://github.com/eliasr58/n8n-production/tree/main/workflows/bewertungsantworten) | Claude entwirft Antworten auf Online-Bewertungen. Veröffentlicht wird nur freigegebener Text, den der Code vorher gegen Leitplanken prüft. 170 Tests. |
| [Wartungserinnerung](https://github.com/eliasr58/n8n-production/tree/main/workflows/wartungserinnerung) | Angebote vor der fälligen Wartung aus festen Textbausteinen. Claude ordnet Antworten nur ein, ein Widerspruch sperrt den Kunden sofort und dauerhaft. 160 Tests. |
| [Eigenbetrieb](https://github.com/eliasr58/n8n-production#betrieb) | Caddy vor n8n, getrennte Datenbankrollen, verschlüsseltes Backup mit geprobtem Restore, Löschfristen und Alarmweg. Das Kontaktformular von roehrner.eu läuft produktiv darauf, beschrieben in der [Case-Study](https://github.com/eliasr58/n8n-production/blob/main/docs/case-study-kontaktformular.md). |
| [Kontextleiste](https://github.com/eliasr58/claude-kontextleiste) | Plugin für Claude Code, das live zeigt, wie voll das Kontextfenster ist. |

Die drei Workflow-Projekte sind für erfundene Betriebe gebaut und vollständig getestet. Im veröffentlichten Stand ist der Versand an Kunden gesperrt.

## Wie ich arbeite

Den Ist-Zustand messen, statt ihn aus der Dokumentation abzuleiten. Als ich meine Absicherung einmal gegen den laufenden Server geprüft habe statt gegen meine Konfigurationsdatei, war sie vollständig umgehbar. Seitdem schließe ich jede Änderung mit einem Nachweis ab, der ohne sie fehlgeschlagen wäre.

Wo ein Modell beteiligt ist, wird seine Ausgabe geprüft, nicht geglaubt: Am Ende entscheidet Code oder ein Mensch, nie das Modell allein.

[roehrner.eu](https://roehrner.eu)
