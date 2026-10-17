# Aktuelle Architektur

Stand: 17. Oktober 2026. Diese Übersicht beschreibt den VPS-Betrieb. Die frühere Architektur-Grafik im Bilderordner gehört zur Entwurfsphase und ist keine Beschreibung der aktuellen Infrastruktur.

| Schicht | Verantwortung |
| --- | --- |
| Oberfläche | Mehrsprachige öffentliche Seiten, Anfragen, Kundenportal und Verwaltung; React und TypeScript |
| Webserver | Nginx nimmt HTTPS-Anfragen entgegen und leitet sie an die Node.js-Anwendung weiter |
| Anwendung | Vinext/Vite, serverseitige Sitzungen, Rollenprüfung, Eingabevalidierung und Geschäftsregeln |
| Daten | SQLite für Konten, Aufträge, Angebote, Projekte, Zahlungen und weitere Anwendungsdaten; versionierte Migrationen |
| Dateien | Geschützter Speicher für private Projektdateien mit kontrolliertem Zugriff; Zahlungsbelege in der Datenbank |
| Integrationen | Resend für Dienst-E-Mails und Kontowiederherstellung; optionale Dienste nur nach Konfiguration |
| Betrieb | systemd, HTTPS-Erneuerung, verschlüsselte Backups und Erreichbarkeitsüberwachung |

## Wichtige Grenzen

- Ein sichtbarer oder ausgeblendeter Button ist keine Berechtigungsprüfung. Der Server prüft Rolle und Zugehörigkeit zum Datensatz.
- Ein Zahlungsbeleg ist eine Eingabe zur Prüfung, keine bestätigte Buchung.
- Nachrichten für Mitarbeiter und Nachrichten für Kunden haben unterschiedliche Sichtbarkeit.
- Datenbank und private Dateien liegen außerhalb des austauschbaren Anwendungscodes.
- E-Mail-Versand, Sicherung und Überwachung sind eigene betriebliche Aufgaben.

## Änderungen veröffentlichen

Änderungen werden über GitHub mit Typprüfung, Linting, Tests und Build geprüft. Die Serverinstallation erfolgt separat: neue Version in einem eigenen Verzeichnis bauen, Backup erstellen, Code umschalten und HTTP-Prüfungen ausführen. Bei fehlgeschlagener Prüfung kann der vorherige Code wiederhergestellt werden.

Die ursprüngliche Workers/D1-Lösung ist nicht mehr der aktuelle Hostingpfad. Cloudflare bleibt für DNS und konfigurierte E-Mail-Weiterleitung relevant.

Diese Dokumentation enthält keine Serveradressen, Zugangsdaten, privaten API-Verträge oder Kundeninformationen.
