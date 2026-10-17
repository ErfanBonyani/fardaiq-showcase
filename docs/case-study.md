# Fallstudie: Von einer Anfrage zur betreuten Projektarbeit

## Ausgangslage

Eine Dienstleistungswebsite allein beantwortet nicht, was nach einer Kundenanfrage geschieht. Für FardaIQ sollten Anforderungen, Angebote, Zahlungsprüfung und Projektausführung in einem nachvollziehbaren Ablauf zusammenkommen. Die Oberfläche musste auch für einen Betreiber ohne Programmierkenntnisse verständlich bleiben.

## Anforderungen und Entscheidungen

| Anforderung | Umsetzung und Begründung |
| --- | --- |
| Anforderungen verständlich aufnehmen | Ein geführter, bedingter Projektfragebogen mit wiederaufnehmbaren Entwürfen |
| Angebote übersichtlich erfassen | Eigene Auftragsseite mit großen Eingabefeldern, Betrag, Währung, Umfang, Phasen und Terminen |
| Beträge und Termine lesbar machen | Gruppierte Betragseingaben, exakte Geldumrechnung sowie wählbarer persischer oder gregorianischer Kalender |
| Projektfortschritt sichtbar machen | Bearbeitbare Phasen, Status, Nachrichten, Dateien und Freigaben in Kunden- und Verwaltungsansicht |
| Kunden voneinander trennen | Serverseitige Prüfung von Anmeldung, Rolle und Datensatz-Zugehörigkeit |
| Zahlungen nachvollziehen | Manuelle Bankprüfung; ein hochgeladenes Belegbild gilt nicht als Zahlungsnachweis |
| Kontozugang wiederherstellen | Zeitlich begrenzte, einmalig verwendbare Links und Widerruf bestehender Sitzungen nach erfolgreichem Zurücksetzen |
| Änderungen kontrolliert veröffentlichen | Automatisierte Prüfungen, separate Release-Verzeichnisse, Backup vor der Umschaltung und anschließende HTTP-Prüfung |

## Ein konkretes Betriebsproblem

Vor dem Hostingwechsel meldete HTML teilweise HTTP 200, während die Übertragung einer benötigten CSS-Datei abbrach oder stark verzögert war. Ein erfolgreicher HTTP-Status allein erklärte deshalb nicht, ob die Seite für einen Besucher tatsächlich benutzbar war.

Nach einem direkten Verbindungstest wurde die Anwendung von Cloudflare Workers/D1 auf einen Linux-VPS mit Node.js, Nginx und SQLite umgestellt. Daten wurden exportiert, auf Integrität und Fremdschlüssel geprüft und vor dem Wechsel gesichert. Der Betreiber bestätigte anschließend eine schnelle Nutzung ohne VPN auf seiner Verbindung. Das ist ein konkretes Testergebnis, keine allgemeine Verfügbarkeitsgarantie und kein Nachweis eines universellen Cloudflare-Problems.

## Ein konkretes Inhaltsproblem

Google meldete mehrere Rechtstext-Seiten als Duplikate. Die Prüfung zeigte: Deutsche, arabische und türkische Routen erklärten sich jeweils als canonical, lieferten aber englischen Hauptinhalt. Die Korrektur übersetzte alle sechs Rechtstext-Seiten und aktualisierte veraltete Hostingangaben. Jede Sprachversion behält ihre eigene canonical-Adresse und verweist per hreflang auf die anderen Versionen.

Für diese Veröffentlichung liefen 125 Anwendungstests, 11 Laufzeittests und HTTP-Prüfungen für 30 Rechtstext-Seiten erfolgreich. Anschließend wurden die Seiten auch auf dem Server geprüft und eine erneute Google-Prüfung angefordert. Die spätere Indexierung wird getrennt vom technischen Testergebnis bewertet.

## Meine Rolle und Unterstützung

Ich habe Anforderungen und Benutzerabläufe festgelegt, praktische Tests durchgeführt, Fehlverhalten beschrieben, Änderungen nachprüfen lassen und Releases auf dem Server ausgeführt. Implementierung, Dokumentation und Tests entstanden mit KI-Unterstützung. Ich nutze die Projekte, um Anwendungscode, Datenmodelle, Debugging und Tests besser zu verstehen; sie werden nicht als vollständig selbstständig programmierte Prüfungsleistung dargestellt.

## Was ich in einer Ausbildung weiterlernen möchte

- Geschäftsregeln selbstständig in überschaubarem Code umsetzen.
- Änderungen mit passenden Tests absichern und im Code-Review erklären.
- Relationale Daten und Zustandsübergänge konsistent modellieren.
- Anforderungen, Entscheidungen und offene Grenzen verständlich dokumentieren.

## Noch offen

SMS und Online-Zahlungsanbieter sind nicht angeschlossen. Eine vollständige Wiederherstellungsprobe des aktuellen Serverbackups, unabhängige Sicherheits- und Lastprüfungen sowie weitere Geräteprüfungen stehen aus. Die Akademie-Funktionen sind als Grundlage vorhanden; ein vollständig betriebenes Lernangebot ist damit nicht nachgewiesen.
