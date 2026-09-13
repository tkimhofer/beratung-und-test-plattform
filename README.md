# Beratung und Test Plattform

Digitale Plattform für pseudonyme Gesundheitsangebote.

Eine integrierte Plattform zur Verwaltung pseudonymer Gesundheitsangebote, die derzeit für die HIV/STI-Prävention und -Diagnostik konzipiert ist. Sie verbindet zielgruppengerichtete Gesundheitskampagnen mit Terminbuchung, Beratung, Laborprozessen, sicherer Online-Ergebnismitteilung und der Evaluation von Angeboten.

Die Plattform verbindet eine interne Desktop-Anwendung für Beratung, Fragebogenerfassung sowie Labor- und Ergebnismanagement mit webbasierten Anwendungen für Terminbuchung, Terminverwaltung und Ergebnismitteilung. Alle Komponenten greifen auf ein gemeinsames Backend zu und bilden dadurch einen durchgängigen digitalen Ablauf von der Ansprache bis zum Ergebnis.

# Beratung und Test Plattform

## Überblick

Eine integrierte Plattform zur Verwaltung pseudonymer Gesundheitsangebote, die derzeit für die HIV/STI-Prävention und -Diagnostik konzipiert ist. Sie verbindet zielgruppengerichtete Gesundheitskampagnen mit Terminbuchung, Beratung, Laborprozessen, sicherer Online-Ergebnismitteilung und der Evaluation von Angeboten.

<p align="center">
  <img src="screenshots/onlinebesucher_angebote.png" alt="Angebot" width="48%">
  <img src="screenshots/onlineangebot_klinikinfo.png" alt="Besucherprozess" width="48%">
</p>


## Die Plattform

Die Plattform bildet den gesamten Klinikprozess ab, ausgehend von Testangeboten im Rahmen von Gesundheitskampagnen:

1. Online Terminbuchung und Terminmanagement
2. Beratung und Laborprobenentnahme
3. Management und Freigabe von Labortestergebnissen
4. Sichere Online Ergebnismitteilung
5. Evaluation und Statistik


## Komponenten

### Web-Anwendung
Terminbuchung, Terminverwaltung, E-Mail-Kommunikation,
Online-Ergebnismitteilung

### Desktop-App
Beratung, Fragebogen, Labor, Befunde, Statistik

### Gemeinsames Backend
API, Datenhaltung, Autorisierung, Pseudonymisierung,
Workflow-Logik

## Kampagnen und Evaluation

Um Angebote möglichst gut an den Menschen auszurichten, die sie benötigen, werden Kampagneninfomrmationen den URL-Links hinzugefügt. Dazu können beim Aufruf der Website übermittelte Kampagneninformationen (UTM-Parameter), die verweisende Website sowie die aufgerufene Einstiegsseite verarbeitet werden.

Beispiel: Besucher scannen einen QR-Code und gelangen dadurch auf die Buchungswebsite. Der QR code enthält zusätzliche Informationen (UTM Parameter), welche Auskunf über das entsprechende Gesundheitsangebot liefert. So kann messbar gemacht werden, wie gut eine Gesundheitskampagne angenommen wird.

Die Auswertung von Kampagneninformationen erfolgt unabhängig von der IP-Adresse der buchenden Person. Die gewonnenen Erkenntnisse werden verwendet, um Angebote und Zugangswege bedarfsgerecht weiterzuentwickeln.

## Datenschutz und Pseudonymisierung

Jedem Besucher wird ein zufällig ausgewähltes Mnemonic zugewiesen, welches ab Online-Terminierung, bis zur Beratung und Ergebnismitteilung den Besucher eindeutig yugeordente ist, sodass keine weiteren persönlichen Informationen notwendig sind. 

Termine und Ergebnisse können unabhängig von der Email-Addresse über eine persönliche ULR (256 bit, high-entropy) verwaltet und eingesehen werden. Zur Einsicht von Online-Ergebnisse wird ein Pin vergeben.

Online Administration Login nutzt Mutli-Faktor-Authentifizierung (Passwort und TOTP).

Die Destktop App nutzt ein Rollen-basierte Authentifizierung und Authorisierung (Bearer Token).


## Architektur

<p align="center">
  <img src="assets/architektur.png" alt="Architektur" width="60%">
</p>


## Technologien

React · TypeScript · Tauri · FastAPI · PostgreSQL · Docker  · nginx

## Screenshots

<p align="center">
  <img src="screenshots/onlinebesucher_terminauswahl.png" alt="Terminauswahl" width="48%">
  <img src="screenshots/onlinebesucher_kontakt.png" alt="Kontakt" width="48%">
</p>

<p align="center">
  <!-- <img src="onlineadmin_übersicht.png" alt="Adminansicht: Angebote und Buchungen" width="32%"> -->
  <img src="screenshots/onlinebesucher_buchungen_übersicht.png" alt="Adminansicht: Buchungen" width="48%">
  <img src="screenshots/onlineadmin_buchung_detailansicht.png" alt="Adminansicht: Buchung Detailansicht" width="48%">
</p>

<p align="center">
  <img src="screenshots/desktopapp_laborergebnis_management.png" alt="Laborergebnisse" width="48%">
  <img src="screenshots/desktopapp_management_ergebniszugang.png" alt="Management Laborergebnis-Zugang" width="48%">
</p>

<p align="center">
  <img src="screenshots/onlinebesucher_laborergebnisse.png" alt="Besucherergebnisse" width="48%">
   <img src="screenshots/desktopapp_statistik.png" alt="Fragebogenstatistik" width="48%">
</p>

→ [Weitere Screenshots](https://github.com/tkimhofer/beratung-und-test-plattform/edit/master/screenshots/readme.md)


## Hinweis

Dieses Repository dient der Dokumentation und Präsentation
des Projekts. Der Quellcode wird nicht öffentlich bereitgestellt.
