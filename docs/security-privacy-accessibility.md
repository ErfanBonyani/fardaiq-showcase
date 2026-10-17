# Sicherheit, Datenschutz und Barrierefreiheit

Stand: 17. Oktober 2026. Die folgenden Punkte beschreiben Funktionen und Prüfgrenzen, keine Zertifizierung.

## Anwendungssicherheit

- Serverseitige Rollen- und Datensatzprüfung für Kunden- und Verwaltungsaktionen.
- Sichere Sitzungen, CSRF-Schutz, Eingabevalidierung und Anfragebegrenzung.
- Zeitlich begrenzte, einmalig verwendbare Passwort-Wiederherstellung per E-Mail.
- Getrennte Sichtbarkeit interner Notizen und kundensichtbarer Nachrichten.
- Kontrollierter Zugriff auf private Dateien und dokumentierte Verwaltungsaktionen.
- Abhängigkeiten und Änderungen werden im GitHub-Workflow geprüft.

Dateiprüfungen durch Mitarbeiter ersetzen keinen automatisierten Virenscanner. Erfolgreiche Tests sind kein unabhängiger Penetrationstest.

## Datenschutz und Betrieb

Die aktuelle Anwendung verwendet SQLite und geschützten Dateispeicher auf einem Linux-VPS. Dienst-E-Mails und Wiederherstellungsnachrichten werden über Resend versendet. Tägliche Backups werden verschlüsselt und eine zusätzliche verschlüsselte Kopie wird an das festgelegte Betreiberpostfach gesendet. Der Entschlüsselungsschlüssel wird getrennt aufbewahrt.

Die Sicherung prüft Integrität und Inhalt ihrer Archive. Eine vollständige Wiederherstellungsprobe des aktuellen Produktionsbackups in einer getrennten Umgebung steht noch aus. Allgemeine automatische Löschung sämtlicher Konten, Verträge und Rechnungen ist nicht eingerichtet; Aufbewahrung und Löschanfragen müssen entsprechend bearbeitet werden.

Öffentliche Projektdokumentation enthält keine Kundeninformationen, Belege, Datenbanken, Schlüssel oder Serverkonfiguration.

## Barrierefreiheit

Semantische Struktur, Formularbeschriftungen, sichtbarer Fokus, Tastaturbedienung, RTL/LTR und reduzierte Bewegung sind Teil der Gestaltung. WCAG 2.2 AA ist ein Ziel, keine Bestätigung vollständiger Konformität. Zusätzliche Geräte- und assistive Tests bleiben erforderlich.

## Rechtlicher Rahmen

Übersetzte Datenschutz- und Servicetexte informieren über den aktuellen Betrieb. Sie sind kein Nachweis vollständiger Rechtskonformität in Deutschland oder anderen Ländern. Geschäftsbedingungen, Aufbewahrung und länderspezifische Pflichten benötigen eine geeignete fachliche Prüfung.
