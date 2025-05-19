# DeeperSQL Software Detaillierte Anleitung
## Sprache ändern
[English](README.md)

## Inhalt der Anleitung
* 1. Software-Einführung
* 2. Installation & Start
* 3. Hauptfunktionen
* 4. Bedienschritte
* 5. FAQ
* 6. Kontakt & Support

## 1. Software-Einführung
DeeperSQL ist ein multifunktionales Werkzeug, das intelligente Excel-Interaktion, Wissensgraphen-Erstellung, KI-Q&A, Datenvisualisierung und mehr integriert. Es eignet sich für Datenbearbeitung und -analyse, Wissensmanagement, intelligente Q&A und verschiedene andere Szenarien.
* Nach dem Importieren von Excel-Dateien können Sie diese in natürlicher Sprache verarbeiten und exportieren.
* Integrierte Diagrammkomponenten für die Datenvisualisierungsanalyse
* Wissensgraphen können über große Sprachmodelle für intelligente Q&A erstellt werden
* Plattformübergreifende Unterstützung (Windows/macOS)

## 2. Installation & Start
### 2.1 Systemanforderungen
* Betriebssystem: Windows 10/11 oder macOS
* Abhängigkeiten: .NET 8.0 oder höher
### 2.2 Installationsschritte
1. Laden Sie das neueste Installationspaket herunter.
2. Stellen Sie die .NET-Komponentenunterstützung sicher, mit Online-/Offline-Großmodell- und Embedded-Modell-Unterstützung.
3. Führen Sie das Hauptprogramm `DeeperSQL` aus.
### 2.3 Starten der Software
1. Doppelklicken Sie auf die ausführbare Datei.
2. Konfigurieren Sie beim ersten Start die Einstellungen des großen Sprachmodells, um einen ordnungsgemäßen Betrieb sicherzustellen.

## 3. Hauptfunktionen
### 3.1 Intelligente Excel-Interaktion
Nach dem Importieren von Excel-Dateien können Sie diese in einer Datenbank speichern und in natürlicher Sprache verarbeiten, analysieren und exportieren.
### 3.2 Wissensgraph
Unterstützt die automatische Generierung, Anzeige und Abfrage von Wissensgraph-Knoten, -Beziehungen und -Gemeinschaften. Die Software generiert automatisch Wissensgraphen mithilfe großer Sprachmodelle.
### 3.3 KI-Q&A
Das KI-Q&A-Modul unterstützt die Integration mit verschiedenen großen Sprachmodellen. Benutzer können Fragen in natürlicher Sprache stellen und generierte Wissensgraphen für Q&A auswählen.
### 3.4 Datenanalyse
Importierte Excel-Dateien können nach dem Speichern in der Datenbank analysiert und visualisiert werden.
### 3.5 API-Dienst
Bietet API-Dienste für die intelligente SQL-Interaktion.

## 4. Bedienschritte
### 4.1 Einstellungen
1. Klicken Sie in der Hauptoberfläche auf Einstellungen und wählen Sie dann "Setting".
2. Nachdem die Einstellungsoberfläche angezeigt wird, klicken Sie auf die Registerkarte LLM, wählen Sie einen gängigen Modellanbieter, geben Sie die API-Adresse ein, geben Sie bei Bedarf den API-Schlüssel ein und wählen Sie das entsprechende Modell aus.
3. Geben Sie geeignete Grenzwerte für API-Aufrufe pro Minute und Token-Grenzwerte ein. Online-APIs haben normalerweise niedrigere Grenzwerte (10-30), und Token-Grenzwerte sollten mindestens 4096, aber im Allgemeinen weniger als 10240 betragen (je nach tatsächlichen Bedingungen anpassen).
4. Geben Sie dann die API-Adresse und den API-Schlüssel des eingebetteten Modells ein und wählen Sie das entsprechende Modell aus. Wenn localhost bei lokalen Modellen nicht funktioniert, versuchen Sie es mit 127.0.0.1.
5. Wenn beim Laden des Modells Probleme auftreten, wird ein Popup angezeigt. Stellen Sie sicher, dass das Modell korrekt geladen wird.
6. Wenn Sie "Beispieldaten für SQL-Anfragen verwenden" aktivieren, wird die erste Datenzeile in der Datenbanktabelle als Beispieldaten verwendet. Wenn Datenschutz oder Vertraulichkeit ein Anliegen sind, verwenden Sie ein lokales LLM oder deaktivieren Sie diese Option.
7. Wenn Sie "Originaltextindizierung verwenden" aktivieren, erhöht dies die Token-Nutzung, verbessert aber die Abrufgenauigkeit.
### 4.2 Erstellen von Wissensgraphen
1. Klicken Sie in der Hauptoberfläche auf Wissensdatenbank und wählen Sie dann das Unterelement Wissensdatenbank aus.
2. Wählen Sie in der Wissensdatenbank-Oberfläche einen Knoten im Baumsteuerelement auf der linken Seite aus und klicken Sie mit der rechten Maustaste.
3. Nachdem das Auswahlfeld angezeigt wird, klicken Sie auf Gruppe hinzufügen, geben Sie den Gruppennamen ein und klicken Sie auf Bestätigen.
4. Klicken Sie nach dem Hinzufügen im Eigenschaftensteuerelement auf die Gruppe und klicken Sie in der oberen Menüleiste auf Hinzufügen. Wählen Sie dann die hinzuzufügenden Dateien aus.
5. Warten Sie geduldig, bis die Generierung des Wissensgraphen abgeschlossen ist. Wenn keine Fehler auftreten, war die Erstellung erfolgreich.
6. Wählen Sie in der Wissensdatenbank-Oberfläche einen Knoten im Baumsteuerelement auf der linken Seite aus, klicken Sie mit der rechten Maustaste, und nachdem das Auswahlfeld angezeigt wird, klicken Sie auf Gruppe importieren oder Gruppe exportieren.
### 4.3 Verwalten von Wissensgraphen
1. Klicken Sie in der Hauptoberfläche auf Wissensdatenbank und wählen Sie dann das Unterelement Wissensdatenbank aus.
2. Wählen Sie in der Wissensdatenbank-Oberfläche einen Knoten im Baumsteuerelement auf der linken Seite aus und klicken Sie mit der rechten Maustaste.
3. Nachdem das Auswahlfeld angezeigt wird, klicken Sie auf Gruppe löschen, Gruppe importieren oder Gruppe exportieren, um diese Funktionen auszuführen.
4. Wählen Sie den Standardknoten aus, klicken Sie in der Menüleiste auf "Vorlage", um die "Gefällt mir"-Datenbank zu exportieren, oder klicken Sie auf "Importieren", um sie zu importieren. Klicken Sie auf Bearbeiten oder Löschen, um bestimmte "Gefällt mir"-Inhalte zu ändern oder zu entfernen.
### 4.4 Anzeigen von Wissensgraphen
1. Wählen Sie in der Wissensgraphen-Verwaltungsoberfläche eine Wissensdatenbank aus und klicken Sie auf die Schaltfläche "Wissensgraph".
2. Nachdem Sie die Wissensgraphen-Anzeigeoberfläche aufgerufen haben, klicken Sie auf die entsprechenden Knoten oder Kanten und dann auf die Schaltfläche Anzeigen, um die entsprechenden Daten anzuzeigen.
3. Geben Sie Suchinhalte ein, drücken Sie die Eingabetaste, und die entsprechenden Suchergebnisse werden angezeigt.
### 4.5 Hinzufügen von Excel-Dateien
1. Wählen Sie das Menü "Dateien", klicken Sie auf "Öffnen" und wählen Sie eine Excel-Datei aus.
2. Klicken Sie nach erfolgreichem Import auf Datenbank, geben Sie einen Datenbanknamen ein und klicken Sie auf Speichern. (Hinweis: Die erste Zeile des Excel-Blatts wird automatisch als Feldnamen der Datenbanktabelle erkannt.)
3. Klicken Sie auf die gerade gespeicherte Datenbank und dann auf Laden, um die Datenbank in die aktuelle Tabelle zu laden.
### 4.6 Bearbeiten von Datenbanktabellen
1. Nachdem Sie eine Excel-Datei geöffnet oder eine Datenbank geladen haben, können Sie im Menü "Bearbeiten" Funktionen wie "Kopieren, Einfügen, Rückgängig, Wiederherstellen, Spalte hinzufügen, Zeile hinzufügen" auswählen.
2. Klicken Sie auf die Tabelle und klicken Sie mit der rechten Maustaste, um entsprechende Funktionen auszuwählen.
3. Klicken Sie in der Menüleiste auf Tabellenelemente (z. B. sheet1), um Datenbanktabellenelemente zu erstellen, zu löschen oder umzubenennen.
### 4.7 Statistische Analyse
1. Klicken Sie nach dem Laden einer Datenbank in der Hauptoberfläche auf die Schaltfläche "Statistiken", um zur Seite "Datenbankstatistiken" zu gelangen.
2. Wählen Sie die Datenbank und Tabelle aus, die Sie analysieren möchten.
3. Wählen Sie die zu analysierenden Felder aus, klicken Sie auf die Schaltfläche Analysieren und zeigen Sie die Analyseergebnisse an. Klicken Sie auf Exportieren, um die Analyseergebnisse zu exportieren.
### 4.8 Intelligente Excel-Interaktion
1. Laden Sie nach dem Hinzufügen einer Excel-Datei und dem Speichern der Datenbank diese Datenbank.
2. Geben Sie unten rechts in der Hauptoberfläche eine Frage in natürlicher Sprache ein und klicken Sie auf die Schaltfläche "Generieren".
3. Nach der LLM-Verarbeitung wird automatisch ein Dialogfeld angezeigt. Bestätigen Sie, dass die generierte SQL-Anweisung durchführbar ist, und klicken Sie dann auf Ausführen, um Ergebnisse zu generieren. (Unterstützt die Erstellung mehrerer Ergebnisse, z. B. die Generierung von zwölf Ergebnissen nach Monat)
4. Klicken Sie auf Exportieren und wählen Sie einen Ordner aus, um die Ergebnisse als Excel-Tabelle zu exportieren. Klicken Sie auf die Schaltfläche "Gefällt mir", um Feedback an die lokale Datenbank zu geben (Daten werden nicht hochgeladen), damit die Software genauere Ergebnisse generieren kann.
### 4.9 KI-Konversation
1. Wählen Sie das Menü "Wissensdatenbank" und klicken Sie dann auf "Chat".
2. Ohne auf den Wissensdatenbankbaum auf der linken Seite zu klicken, geben Sie eine Frage in das Eingabefeld ein, klicken Sie auf die Schaltfläche "Chat starten" und warten Sie, bis die Ergebnisse generiert werden.
3. Klicken Sie auf den Wissensdatenbankbaum auf der linken Seite, um die entsprechende Wissensdatenbank zu laden, geben Sie eine Frage in das Eingabefeld ein, klicken Sie auf "Chat starten" und warten Sie auf die Ergebnisse. Nachdem die Ergebnisse generiert wurden, klicken Sie auf Referenzen oder Verlauf, um verwandte Inhalte anzuzeigen.
### 4.10 API-Dienst
* /api/SQL/List Datenbankliste abrufen
* /api/SQL/Tables Tabellenliste der angegebenen Datenbank abrufen Parameter: dbname
* /api/SQL/TableInfo Tabellenstruktur und Zeilenanzahl abrufen Parameter: dbname, tablename
* /api/SQL/Get Tabellendaten seitenweise abrufen Parameter: dbname, tablename, start, num
* /api/SQL/Chat Intelligente SQL-Q&A Parameter: dbname, content
* /api/SQL/Do SQL-Anweisung ausführen Parameter: dbname, content
* /api/status Dienststatus

## 5. FAQ
### F1: Was soll ich tun, wenn beim Start ein Fehler auftritt?
**A1:** Bitte überprüfen Sie, ob die .NET-Umgebung installiert ist, oder sehen Sie sich die Protokolldatei für detaillierte Fehlerinformationen an.
### F2: Was soll ich tun, wenn beim Importieren von Excel-Dateien oder beim Erstellen einer Datenbank ein Fehler auftritt?
**A2:** Bitte stellen Sie sicher, dass die erste Zeile der Excel-Datei die Datenbankfeldnamen enthält und dass das Excel-Datenformat korrekt ist. Beispielsweise sollten Datumsfelder in der Datenbanktabelle das Format "2025-12-30" haben.
### F3: Was soll ich tun, wenn beim Laden des Modells ein Fehler auftritt?
**A3:** Bestätigen Sie zunächst, ob die Modelladresse korrekt ist. Wenn ein API-Schlüssel erforderlich ist, stellen Sie sicher, dass Sie den richtigen API-Schlüssel eingegeben haben. Überprüfen Sie, ob die http/https-Präfixe korrekt sind, ob das Netzwerk normal ist usw. Starten Sie nach dem Ändern der Adresse die Software zum Testen neu.
### F4: Was soll ich tun, wenn bei der KI-Konversation ein Fehler auftritt?
**A4:**
1. Stellen Sie sicher, dass die Modelladresse, der API-Schlüssel usw. korrekt sind.
2. Stellen Sie sicher, dass das Netzwerk normal ist.
3. Stellen Sie bei lokalen Modellen sicher, dass der Modelldienst ordnungsgemäß ausgeführt wird.
4. Stellen Sie bei Online-Modellen sicher, dass der API-Schlüssel korrekt ist.
5. Stellen Sie sicher, dass die Token-Grenzwerte, API-Aufrufgrenzwerte pro Minute usw. korrekt sind – weder zu hoch noch zu niedrig.

## 6. Kontakt & Support
Bei Fragen oder Anregungen wenden Sie sich bitte an das Entwicklungsteam:
* E-Mail: deepersql@hotmail.com
