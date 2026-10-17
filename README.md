# FardaIQ — Webanwendung für Kundenaufträge und Projekte

**[Website auf Deutsch öffnen](https://www.fardaiq.ir/de)** · **[Persische Version](https://www.fardaiq.ir/fa)** · **[Fallstudie](docs/case-study.md)**

FardaIQ verbindet eine mehrsprachige Dienstleistungswebsite mit einem Kundenportal und einer Verwaltung. Ein Auftrag kann von der ersten Anfrage über Angebot und Zahlungsprüfung bis zu Projektphasen, Nachrichten und Freigaben begleitet werden.

**Portfolio von Erfan Bonyani · Ausbildungsziel: Fachinformatiker für Anwendungsentwicklung.**

## In zwei Minuten

| Frage | Antwort |
| --- | --- |
| Welches Problem wird gelöst? | Anforderungen, Angebote und Projektfortschritt sollen für Kunde und Anbieter nachvollziehbar bleiben. |
| Was ist bereits in Betrieb? | Website, Anmeldung, E-Mail und Passwort-Wiederherstellung sowie Auftrags- und Projektabläufe. |
| Was zeigt die Anwendungsentwicklung? | Formularvalidierung, Geschäftsregeln, Rollen, relationale Daten, Zustandsübergänge und automatisierte Tests. |
| Kann ich den Quellcode hier prüfen? | Dieses Repository ist eine öffentliche Fallstudie; der vollständige Anwendungscode ist privat. |
| Wo gibt es ein kleines Codebeispiel? | [Eigenständige Python-Lernübung mit Tests](https://github.com/ErfanBonyani/ErfanBonyani/tree/main/examples/order-workflow). |

## Ein durchgängiger Ablauf

1. Der Kunde beschreibt sein Vorhaben in einem geführten Formular.
2. Der Administrator erstellt ein übersichtliches Angebot mit Umfang, Betrag, Währung und Terminen.
3. Der Kunde nimmt das Angebot an und übermittelt gegebenenfalls einen Überweisungsbeleg.
4. Der Administrator prüft den tatsächlichen Zahlungseingang und legt das Projekt an.
5. Beide Seiten verfolgen Phasen, Nachrichten, Dateien und Freigaben im jeweiligen Arbeitsbereich.

Persische und gregorianische Datumswahl, lesbare Beträge und eine optionale Empfänger-IBAN unterstützen den Ablauf. Ein Belegbild löst keine automatische Zahlungsbestätigung aus.

## Technischer Überblick

| Bereich | Aktueller Stand |
| --- | --- |
| Anwendung | TypeScript, React und Vinext/Vite mit Next.js-kompatibler Struktur |
| Server | Node.js hinter Nginx auf einem Linux-VPS, HTTPS und systemd |
| Daten | SQLite und versionierte SQL-Migrationen |
| Dateien | Geschützter Dateispeicher und serverseitige Zugriffsprüfung |
| Kommunikation | Transaktions-E-Mails und Passwort-Wiederherstellung über Resend |
| Sprachen | Persisch, Englisch, Deutsch, Arabisch und Türkisch; RTL/LTR und lokalisierte Metadaten |
| Qualität | Typprüfung, Linting, automatisierte Tests, CI und kontrollierte Veröffentlichung |
| Betrieb | Verschlüsselte Backups, lokale Überwachung und externe Erreichbarkeitsprüfung |

Die frühere Cloudflare-Workers/D1-Bereitstellung wurde durch den VPS-Betrieb ersetzt. GitHub speichert den Code und prüft Änderungen; ein Commit allein veröffentlicht keine neue Serverversion.

## Nachvollziehbare Prüfung

Für die am **17. Oktober 2026** veröffentlichte Korrektur der Rechtstexte wurden **125 Anwendungstests und 11 Laufzeittests** erfolgreich ausgeführt. Zusätzlich wurden alle **30 Rechtstext-Seiten** auf HTTP-Antwort, Sprache, Inhalt, canonical und hreflang geprüft; diese Seitenprüfung lief auch nach der Serverinstallation erfolgreich.

Diese Prüfungen ersetzen weder einen unabhängigen Sicherheitstest noch einen Lasttest oder eine vollständige Prüfung aller Oberflächen.

## Meine Rolle

Anforderungen, Kunden- und Verwaltungsabläufe, Abnahmetests, Fehlerreproduktion, Release-Prüfung und Inbetriebnahme. Für Implementierung, Tests und Dokumentation wurden KI-gestützte Werkzeuge genutzt. Ich baue meine Programmiergrundlagen weiter aus; das Projekt wird nicht als vollständig ohne Unterstützung programmierte Arbeit dargestellt.

## Grenzen und nächste Schritte

- Überweisungen werden manuell geprüft; ein Online-Zahlungsanbieter ist nicht angeschlossen.
- Ein SMS-Anbieter ist noch nicht eingerichtet.
- Eine vollständige Wiederherstellungsprobe des aktuellen Serverbackups in einer getrennten Umgebung steht noch aus.
- Die Akademie ist eine technische Grundlage; ein vollständig betriebener Kurskatalog wird hier nicht behauptet.
- Barrierefreiheit und Datenschutz werden berücksichtigt; eine externe Zertifizierung oder landesspezifische Rechtsprüfung wird nicht behauptet.

## Dokumentation und frühere Entwürfe

- [Fallstudie: Anforderungen, Entscheidungen und Lernerfahrungen](docs/case-study.md)
- [Aktuelle Architektur](docs/architecture-overview.md)
- [Sicherheit, Datenschutz und Barrierefreiheit](docs/security-privacy-accessibility.md)
- [Status und nächste Schritte](docs/status-and-roadmap.md)

Die Bilder unter `assets/screens/` sind **frühere Konzeptgrafiken und Wireframes**, keine aktuellen Produktionsscreenshots. Sie dokumentieren die Entwurfsphase; für den aktuellen Stand nutzen Sie die Live-Website und die obigen Dokumente.

## English summary

A live multilingual web application covering project enquiries, proposals, manual payment review and customer collaboration. The current runtime uses Node.js, Nginx and SQLite on a Linux VPS. This repository is a public case study, not an open-source distribution of the application.

## Kontakt und Rechte

**Erfan Bonyani** · [GitHub](https://github.com/ErfanBonyani) · [E-Mail](mailto:erfan.bonyaniapp@gmail.com)

Proprietäre Projektdokumentation. Siehe [LICENSE.md](LICENSE.md). Kundendaten, Zugangsdaten und Produktionskonfiguration sind nicht Bestandteil dieses Repositories.
