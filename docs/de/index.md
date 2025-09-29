# SHModbus - Benutzerhandbuch

![SHModbus Anwendung](../shared-images/shmodbus-app.png)

## Überblick

SHModbus Client ist eine Anwendung zur Echtzeitüberwachung und Visualisierung von Industriedaten, die sich mit Modbus-Geräten verbindet und Live-Sensordaten, Gerätestatus und Systeminformationen über eine intuitive Weboberfläche anzeigt.

## Hauptfunktionen

### Echtzeitdatenüberwachung
- **Live-Datentabelle**: Echtzeitwerte von verbundenen Modbus-Geräten mit automatischen Updates anzeigen
- **Auto-Aktualisierung**: Daten werden automatisch alle paar Sekunden ohne manuelle Aktualisierung erneuert
- **Zeitstempel-Anzeige**: Sehen Sie genau, wann jeder Datenpunkt zuletzt aktualisiert wurde
- **Wertformatierung**: Alle numerischen Werte werden mit konsistenter 2-Dezimalstellen-Präzision angezeigt

### Datenvisualisierung
- **Interaktive Diagramme**: Visuelle Darstellung von Datentrends über die Zeit
- **Mehrere Diagrammtypen**: Liniendiagramme, Balkendiagramme und andere Visualisierungsoptionen
- **Historische Daten**: Vergangene Datentrends und Muster anzeigen
- **Zoomen und Schwenken**: Mit Diagrammen interagieren, um sich auf bestimmte Zeiträume zu konzentrieren

### Geräteverwaltung
- **Verbindungsstatus**: Echtzeitanzeige der Modbus-Gerätekonnektivität
- **Geräteinformationen**: Details über verbundene Ausrüstung und Sensoren anzeigen
- **Mehrgeräte-Unterstützung**: Mehrere Modbus-Geräte gleichzeitig überwachen
- **Verbindungsgesundheit**: Visuelle Indikatoren zeigen an, wenn Geräte online/offline sind

### Benutzeroberflächen-Funktionen
- **Responsives Design**: Funktioniert auf Desktop-Computern, Tablets und Mobilgeräten
- **Dunkles/Helles Theme**: Wählen Sie Ihr bevorzugtes visuelles Theme
- **Sortierbare Tabellen**: Klicken Sie auf Spaltenkopfzeilen, um Daten nach beliebigen Feldern zu sortieren
- **Suchen und Filtern**: Bestimmte Datenpunkte schnell finden
- **Export-Funktionen**: Daten in Dateien für externe Analyse speichern

### Echtzeitkommunikation
- **SignalR-Integration**: Sofortige Datenaktualisierungen ohne Seitenaktualisierungen
- **Live-Benachrichtigungen**: Sofortige Alarme bei Änderungen des Gerätestatus
- **Automatische Wiederverbindung**: Hält Verbindung auch während Netzwerkunterbrechungen aufrecht
- **Niedrige Latenz**: Minimale Verzögerung zwischen Geräteaktualisierungen und Anzeige

### Datenverwaltung
- **Zwischengespeicherte Daten**: Aktuelle Werte lokal für schnellen Zugriff gespeichert
- **Datenhistorie**: Zugriff auf historische Messwerte und Trends
- **Wertvalidierung**: Automatische Erkennung und Behandlung ungültiger Daten
- **Zeitzonenunterstützung**: Zeigt Zeiten in Ihrer lokalen Zeitzone an

## Industrielle Anwendungen

- **Prozessüberwachung**: Temperatur, Druck, Durchflussraten und andere Prozessvariablen verfolgen
- **Gerätestatus**: Motorgeschwindigkeiten, Ventilpositionen, Pumpenstatus überwachen
- **Alarmüberwachung**: Echtzeitalarme für Bedingungen außerhalb des Bereichs
- **Qualitätskontrolle**: Produktionsmetriken und Qualitätsparameter verfolgen
- **Energiemanagement**: Stromverbrauch und Effizienzmetriken überwachen

## Barrierefreiheitsfunktionen

- **Tastaturnavigation**: Vollständige Anwendungssteuerung nur mit der Tastatur
- **Screen Reader-Unterstützung**: Kompatibel mit Hilfstechnologien
- **Hohe Kontrastoptionen**: Verbesserte Sichtbarkeit für Benutzer mit Sehbehinderungen
- **Skalierbare Oberfläche**: Einstellbare Text- und Elementgrößen

## Leistungsoptimierung

- **Effiziente Updates**: Aktualisiert nur Daten, die sich tatsächlich geändert haben
- **Bandbreitenoptimierung**: Minimaler Netzwerkverbrauch für kontinuierliche Überwachung
- **Browser-Kompatibilität**: Funktioniert mit allen modernen Webbrowsern
- **Schnelles Laden**: Schneller Start und responsive Oberfläche

## Konfigurationsoptionen

- **Anpassbare Ansichten**: Datenanzeigen passend zu Ihrem Arbeitsablauf anordnen
- **Benutzereinstellungen**: Bevorzugte Einstellungen und Layouts speichern
- **Datenpunktauswahl**: Wählen Sie, welche Sensoren und Werte überwacht werden sollen
- **Update-Intervalle**: Anpassen, wie häufig Daten aktualisiert werden

## Sicherheitsfunktionen

- **Sichere Verbindungen**: Verschlüsselte Kommunikation mit Geräten und Servern
- **Benutzerauthentifizierung**: Zugriffskontrolle und Benutzerverwaltung
- **Datenintegrität**: Überprüfung, dass angezeigte Daten genau und unverändert sind
- **Audit-Trail**: Protokollierung von Benutzeraktionen und Systemereignissen

## Häufige Anwendungsfälle

- **Fertigung**: Produktionslinienausrüstung und Qualitätsmetriken überwachen
- **HVAC-Systeme**: Temperatur, Feuchtigkeit und Luftqualität verfolgen
- **Wasseraufbereitung**: Durchflussraten, Chemikalienlevels und Pumpenstatus überwachen
- **Energiesysteme**: Stromerzeugung, -verbrauch und -effizienz verfolgen
- **Gebäudeautomation**: Beleuchtung, Sicherheit und Umweltsysteme überwachen
- **Laborausrüstung**: Testbedingungen und Messergebnisse verfolgen

## Erste Schritte

1. Öffnen Sie die Anwendung in Ihrem Webbrowser
2. Warten Sie auf die Verbindungsherstellung mit Modbus-Geräten
3. Zeigen Sie Echtzeitdaten in der Live-Tabelle an
4. Erkunden Sie Diagramme und Visualisierungen für Trends
5. Passen Sie Ihre Ansicht durch Sortieren und Filtern von Daten an
6. Richten Sie Alarme und Überwachung für kritische Parameter ein

Die Anwendung behandelt automatisch alle technischen Details der Modbus-Kommunikation, Datenformatierung und Echtzeitaktualisierungen, so dass Sie sich auf die Überwachung Ihrer industriellen Prozesse und Ausrüstung konzentrieren können.