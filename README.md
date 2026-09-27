Elias Röhrner

Ich automatisiere Abläufe für Handwerksbetriebe und kleine Unternehmen in Niederbayern — als Einzelunternehmer unter dem Namen Röhrner Automation.

Mein Werkzeug ist n8n auf einem eigenen Hetzner-Server: Docker Compose, Postgres, Caddy als Reverse Proxy, alles selbst aufgesetzt und im Betrieb. Gebaut wird mit Claude Code und MCP.

Was ich dabei gelernt habe und für wichtiger halte als jede Technologieliste: Den Ist-Zustand messen, statt ihn aus der Dokumentation abzuleiten. Als ich meine Absicherung einmal gegen den laufenden Server geprüft habe statt gegen meine Konfigurationsdatei, war sie vollständig umgehbar. Seitdem schließe ich jede Änderung mit einem Nachweis ab, der ohne sie fehlgeschlagen wäre.

n8n-production — meine produktiven Workflows, die Serverkonfiguration und die Betriebsdokumentation dazu. Bereinigt um Zugangsdaten, sonst unverändert.

Dort liegt auch der Mahnlauf, gebaut für einen erfundenen Betrieb mit erfundenen Kunden: Er gleicht jeden Werktag die offenen Rechnungen mit dem letzten Kontoauszug ab und erinnert, wer noch nicht gezahlt hat. Eine Mahnung an jemanden, der längst überwiesen hat, kostet mehr Vertrauen als eine zu spät verschickte. Deshalb liest er unmittelbar vor jeder Mail den Zahlstand neu, verschickt nur feste Textbausteine, eine Mahnung erst nach Freigabe, und meldet, was er nicht sicher zuordnen kann, statt es zu entscheiden. Im veröffentlichten Stand ist der Versand an Kunden gesperrt; vorgesehen ist, dass er zuerst einige Wochen nur berichtet, was er verschickt hätte: [workflows/mahnlauf](https://github.com/eliasr58/n8n-production/tree/main/workflows/mahnlauf).

Daneben die Wartungserinnerung, ebenfalls für einen erfundenen Betrieb: Sie schreibt Bestandskunden vor der fälligen Wartung ein Angebot aus festen Textbausteinen und lässt Antworten von Claude nur einordnen — ein Widerspruch sperrt den Kunden sofort und dauerhaft, im Zweifel wird gesperrt, und die KI schreibt nie an Kunden: [workflows/wartungserinnerung](https://github.com/eliasr58/n8n-production/tree/main/workflows/wartungserinnerung).

Erreichbar unter roehrner.eu.
