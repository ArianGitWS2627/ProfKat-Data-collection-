
# ProfKat Datenaufarbeitung

Um den ProKat Datensatz für die weitere Analyse vorzubereiten, wird in diesem Repository eine grafische Benutzeroberfläche bereitgestellt. 
Diese dienen der Überprüfung, Bereinigung, und Transformation der Daten und zu ihrem Export im anvisierten Datenformat.

Da es sich bei diesem Datensatz um einen **personenbezogenen** Datensatz handelt, ist es wichtig, dass alle Datenverarbeitungsschritte lokal durchgeführt werden und keine sensiblen Informationen an externe Dienste weitergegeben werden. 
Hierzu zählt auch, dass der **Datensatz selbst nicht in diesem Repository** enthalten ist.
Zudem darf der Datensatz nicht durch Anwendungen von Drittanbietern, insbesondere durch KI-gestützte Tools, verarbeitet werden, da dies ein Risiko für die Privatsphäre der betroffenen Personen darstellen könnte.

Haupziel dieses Repository ist es, ein benutzerfreundliches Werkzeug bereitzustellen, das es ermöglicht, den ProKat Datensatz (oder Teile davon) effizient und sicher zu verarbeiten und in einem standardisierten Format für die weitere Analyse bereitzustellen.

## Erste Schritte

Bevor Sie mit der Datenaufarbeitung beginnen, müssen Sie erst ihre eigene Kopie des Repository erstellen und auf Ihren lokalen Rechner herunterladen.
Hierzu führen sie bitte die folgenden Schritte aus:

- Dies ist ein "Template Repository", das bedeutet, dass Sie zunächst eine eigene Kopie des Repositorys erstellen müssen.
  - Klicken Sie hierzu auf die Schaltfläche "Use this template" (oben rechts) und wählen Sie "Create a new repository".
  - Geben Sie einen Namen für Ihr neues Repository ein und klicken Sie auf "Create repository from template".
- Nun sollten sie in ihrem eigenen GitHub Account eine Kopie des Repositorys haben.
- Klonen Sie nun das (online) Repository auf ihren lokalen Rechner mit Hilfe von Visual Studio Code oder einem anderen Git-Client.
  - in VScode können Sie dies über die folgenden Schaltflächen tun:
    - Klicken Sie auf das Symbol "Source Control" (links in der Seitenleiste).
    - Klicken Sie auf die Schaltfläche "Clone Repository" und geben Sie die URL ihres Repositorys ein.
    - Wählen Sie einen lokalen Ordner aus, in dem das Repository geklont werden soll.


## Anforderungen

Die Anforderungen für die Umsetzung der Datenaufarbeitung sind in der Datei `task-description.md` dokumentiert. 

- Das ursprüngliche Datenformat ist in der Datei `import-data-format.md` beschrieben.
- Ein Beispieldatensatz ist in der Datei `import-data-example.txt` enthalten.
- Das anvisierte Zieldateiformat ist in der Datei `export-data-format.md` beschrieben.

## Lokale Ausführung

Da ein Webseiten-basiertes Interface zu erstellen ist, muss der Inhalt (die Webseite) des Repositorys lokal auf dem Rechner ausgeführt werden.
Hierzu kann ein lokaler Webserver verwendet werden, was am einfachsten mit Python realisiert werden kann.

### Schritt 1 - Clonen des Repositorys

Um die Webseite lokal auszuführen, muss das Repository zunächst auf den lokalen Rechner geklont werden.
Dies kann entweder via git oder durch Herunterladen der ZIP-Datei erfolgen.

### Schritt 2 - Lokaler Webserver mit Python

Damit die Webseite im vollen Funktionsumfang lokal ausgeführt werden kann, muss ein lokaler Webserver gestartet werden.
Hierzu kann Python verwendet werden, das auf den meisten Systemen bereits vorinstalliert ist oder leicht installiert werden kann.

Die Fähigkeit, einen lokalen Webserver zu starten, ist im Basispaket von Python 3 bereits integriert und benötigt keine zusätzlichen Pakete.

Um den lokalen Webserver zu starten, navigieren Sie in das Verzeichnis, in dem sich die geklonten Dateien befinden, und führen Sie den folgenden Befehl aus:

```bash
# Für Python 3.x
python -m http.server 8000
```

### Schritt 3 - Zugriff auf die Webseite

Nachdem der lokale Webserver gestartet wurde, können Sie die Webseite in Ihrem Webbrowser aufrufen, indem Sie die folgende URL eingeben/verwenden:

- [http://localhost:8000](http://localhost:8000)

Hiermit greift der Browser direkt auf den eigenen Rechner zu und kommuniziert mit dem gestarteten lokalen Webserver, wodurch die Webseite im vollen Funktionsumfang ausgeführt werden kann.

Ein *direktes Öffnen* der HTML-Dateien im Browser (z.B. durch Doppelklick auf die Datei) *ist nicht ausreichend*, da dies nicht die volle Funktionalität der Webseite gewährleistet.
In diesem Fall können nicht alle Dateien der Webseite korrekt geladen werden, sodass die Webseite nicht wie vorgesehen funktioniert.


### Schritt 4 - Beenden des lokalen Webservers

Um den lokalen Webserver zu beenden, können Sie im Terminal, in dem der Server gestartet wurde, die Tastenkombination `Strg + C` verwenden.

Alternativ können Sie das Terminal-Fenster schließen, in dem der Server läuft.


### Webseiten-Aktualisierung bei live Änderungen

Sie können während der Webserver-Ausführung Änderungen an den Dateien vornehmen und die Webseite im Browser aktualisieren, um die Änderungen zu sehen.
Hierzu ist *kein Neustart des Webservers erforderlich*. 
Dieser wird automatisch die Änderungen erkennen und die aktualisierten Dateien bereitstellen.

Hierzu müssen Sie lediglich die **Seite im Browser neu laden** (z.B. durch Drücken der Taste `F5` oder durch Klicken auf die Schaltfläche "Aktualisieren" im Browser).
Beachten sie dabei, dass die meisten Browser die Dateien zwischenspeichern (Caching), sodass Änderungen an den Dateien nicht sofort sichtbar sind.

Sie können das **Caching umgehen**, indem Sie die Seite mit der Tastenkombination `Strg + F5` (Windows) oder `Cmd + Shift + R` (Mac) neu laden.


