# best_web.exe Version´s

> Current best_web.exe 6.0.23 - http://download.cordaware.com/support/v6/web/6023/best_web.exe


EN: Webinterface for bestinformed Version 6 can be downloaded here:

http://download.cordaware.com/support/v6/web/

DE: Weboberfläche zu bestinformed Version 6 hier herunterladen:

http://download.cordaware.com/support/v6/web/


------------------
-Changelog best_web 6.0.23 (28.10.2016)
* Dashboard Laden optimiert
* neue Hilfe-Version 6.0.23
* Guardians: Upload der Archive wurde verbessert
* Channels: Programmiersprache immer Pascal

------------------
-Changelog best_web 6.0.22 (28.10.2016)
                
* Das Dashboard wird anhand vorhandener Rechte erstellt / bei keinem Ergebnis erscheint das bestinformed Logo                
* Erlang Sandbox unterstützt für Erlang Scriptfilter das Module best_script
* Domäne: weitere Fehlermeldungen beim Verbindungsaufbau (Einstellungen testen)
* Infofelder: Formular geändert, Verbesserungen beim Speichern & Editieren
* Sprachwechsel innerhalb der Weboberfläche geändert (Parameter in der URL)
* Geänderter Installer für best_web.exe (korrigierte vm.args), etc\infoserver.ini und etc\ssl\* werden bei der Deinstallation nicht gelöscht

Infoeditor:
* Infofelder konnten mehrfach hinzugefügt werden
* Periode -> Bei Zahlenfeldern ist die Eingabe einer 0 nicht mehr möglich
* Periode -> Leere Fehlermeldung bei der Zeitüberschreitung der Anforderung verbessert
* Zeitberechnung beim Erstellen der Info mit einer numerischen Beginn/Endzeit verbessert
 
StatusInfo/Neue Info:
* Contentverwaltung -> Workaround für IE11 auf Windows 10 eingebaut
 
EasyIE:
* Leere Info konnte zum Versand freigegeben werden
                
- Umfragen: Draw2d Optimierungen beim Wechsel des Benutzers
- Umfragen: Fixed: Prozentanzeige bei Gruppenumfrage geändert, wenn eine Umfrage ohne Fragen erstellt wurde

------------------
-Changelog best_web 6.0.21 (27.10.2016)

Channel:
* Optimierungen für den Scripteditor

Domänen:
* Einstellungen testen zeigen weitere Fehlermeldungen

Neue Info:
* Templates versenden -> startWith wurde durch indexOf wegen Kompatibilität zu IE ersetzt
* Doppelte Schlüssel beim Laden der Templates wurden entfernt

Infoübersicht:
* Scrollverhalten beim Laden des Stores verbessert
                         
------------------

-Changelog best_web 6.0.20 (26.10.2016)
* ETAG Header in Cowboy-Server bei statischen Dateien (generell für CSS, gesamte Weboberfläche usw.)
* Szenario speichern und editieren verbessert
* Performance Verbesserungen Webseite laden
* EmptyText im Grid bei Textdateien App hinzugefügt

Verbesserungen bei Templates
* Doppelte Infos beim Versenden der Info, welche zuvor als Template gespeichert wurde.
 
Neue Info:
* ScriptVar in M2I Ansicht wurde abgeschnitten
* Anpassung des Layouts/Sprachbausteine an die kleinere Auflösungen
* Overflows, Scrollbalken, Wordwraps
* Scrollverhalten beim Editor verbessert
* Zurück-Button führte in bestimmten Fällen zu Templates
* 2. Toolbar im HTML-Editor verschwinden jetzt keine Elemente mehr
 
Infoübersicht:
* Keine Detailansicht war bei einer periodischen Info möglich
* Fehlermeldung bei fehlenden Entwarnung beim Entwarnen des Szenarios verbessert
* Entwarnungsinfo konnte nicht kopiert und entwarnt werden
 
Guardians:
* Formulare bei Zielen haben sich nicht geleert
* Ziele wurden nicht aktualisiert, wenn ein neues Ziel hinzugefügt wurde

------------------

-Changelog best_web 6.0.19 (21.10.2016)
* Berichte: Layout in der App geändert
* Erlang Cowboy Webserver zu N20 -  ?REQ (request) verbessert
* Umfragen: Formulare geändert beim Erstellen von neuen Umfragen, neuen Fragen
* Umfragen: Schaltfläche zu Prüfung auf 100% nur bei Compliance Umfragen möglich
* Umfragen Ergebnisse: Ausgefüllter Zustand optimiert für normale Umfragen
* Umfragen durchführen: weiter Schaltfläche geändert
* Umfragen initiieren: Beschriftung für die Felder (fieldLabel´s) werden dynamisch errechnet pro Fragenseite
* Alle Links aus der Oberfläche werden in einem neuen Fenster geöffnet
* Dashboard Hilfe -> Einträge angepasst/ausgeblendet
* Guardians: Layout Anpassung bei der Wahl der Aktion -> Auswahlbox statt Radiobuttons
* Guardians: Upload der Archive wurde optimiert

Neue Info:         
* Periode wurde verbessert
* Kleine Verbesserungen beim Erstellen einer Info
* Templates: Fehlende Inhalte beim Speichern und Laden von Templates hinzugefügt
* Templates: Kommunikation zwischen Neue Info und Infoübersicht verbessert
* Templates: Speichern des Templates unter anderen Namen ist jetzt möglich
* Layout der Template Card bei Neue Info geändert
* Verbesserung der Contentverwaltung
* Sound konnte nicht mehr hinzugefügt werden
* Sprachbausteine verbessert
* Zweite Toolbar des Editors hat sich nicht deaktiviert beim Source editieren
* Negative Werte können nicht mehr bei Nummerfeldern eingegeben werden

Weiteres:
* StatusInfos: kleine Verbesserungen beim Erstellen des StatusDetails
* Scriptvar: AuswahlBox warf Fehler beim Leeren des Wertes
* Infoübersicht: Info/Szenarien entwarnen und/oder abbrechen verbessert
* Überschriften bei Neue Info bei Aktionen aus Infoübersicht richtig gesetzt

------------------

-Changelog best_web 6.0.18 (20.10.2016)
* Durchführung von anonymisierten Umfragen
* Umfragen: Fragen editieren Formular (diverse Felder sind jetzt versteckt für den Benutzer)
* Session-Timeout bei anonymisierten Umfragen sind immer 8 Std.

------------------

-Changelog best_web 6.0.17 (19.10.2016)
* Webbenutzer laden beim Aktivieren der App
* Fixed: Rollen App - alle Rechte im Container selektieren / deselektieren
* Ausgabe von verbesserten Fehlermeldungen innerhalb der Weboberfläche
* Umfragen: Teilnahme an anonymisierten Umfragen ohne Benutzeranmeldung

------------------

-Changelog best_web 6.0.16 (18.10.2016)

* Sprachbausteine hinzugefügt für Webbenutzer, AKM, Infoeditor, Guardians
* Sprachbausteine optimiert
* Geändert: Webbenutzer für admin zeigt keine Domäne mehr an
* Upgrade: couchbeam lib zu Version 1.3.1
* Neu: Statistik App
* Fixed: Schriftfarbe setzen im HTMLEditor unter Firefox, Opera
* Neue Version für Alarmierung App implementiert
* Fixed & Geändert: Info an Benutzerschnellauswahl. Einträge können in der Tabelle mit einem Klick nachträglich editiert werden
* Fixed: Templategruppen erstellen, löschen, editieren, Optimierungen, Berechtigungen hinzugefügt für Template speichern, löschen, Templategruppe speichern, löschen
* Fixed: emptyText bei Infofeldern im Baum, wenn keine Daten vorhanden sind
* Fixed: Benutzereinstellungen - Tagfield für Benutzerdefiniertes Menü
* Fixed: Benutzereinstellungen - Sprachauswahl
* Geändert: Beschreibung im Infoeditor für Benutzerliste geändert
* Geändert: Beschreibung für Entwarnungs-ID im Infoeditor
* Neu: Berichte Beispiele - Letzten 10 aktive Nachrichten, Jahresübersicht Nachrichten aus der Historie
* Benachrichtigungen für den Status zum Laden der Domäne befindet sich jetzt in den Nachrichten
* Verbesserte Fehlermeldungen bei der Benutzeranmeldung für diverse Konstellationen
* Zusätzliche Prüfung eingebaut, wenn der Alias eines Profil der gleiche ist wie das eingetragene Standardprofil in den System (global) Einstellungen
* Geändertes Verhalten für die Ressourcen Mitbenutzung auf Profilebene
* Mimetypes für Web Font´s hinzugefügt
* Möglichkeit zum Filter testen für Domänen Filter hinzugefügt
* Fixed: Benutzersession optimiert (kein doppeltes anmelden mehr)
* Geändertes Datenbank Backup per Replikation oder auf HDD (stündlich)
* Aktualisieren Button in orange für die aktuelle Verbindungsübersicht, wenn neue Infoclients etc. verbunden werden.

Umfragen:
* Spalten verkleinert beim Anzeigen der Umfrageergebnisse (Fortschritt, Anzahl / Summe)
* Prozentanzeige bei Kommentaren geändert
* Umfrage Benachrichtigungen können kopiert werden
* Prüfung auf 100% optimiert, wenn Umfrage bereits beendet ist. Der Titel und der Prüfung Button werden angepasst / versteckt je nach Konstellation der Umfrage bei der Anzeige des Ergebnis
* Neue Benachrichtigungsoptionen für Umfrage wurde zurückgewiesen, Umfrage wurde vollständig ausgefüllt
* Ergebnisanzeige zeigt den ausgefüllten Status mit einem Häkchen (grün) oder X (rot) an…. (Prozentanzeige ist ausgeblendet)
* Abfrage für Prüfung auf 100% geändert: Schaltflächen geändert zu Bestätigen, Zurückweisen, Abbrechen
* Aufklappen einer Instanz einer Gruppenumfrage zeigt nun auch gleich die initiierten Umfragen
* Neue Auswertung Option bei Umfragen: Vollständige Ergebnisansicht mit allen Fragen und Antworten
* Ergebnisse sind bei der Auswertung alle aufgeklappt standardmäßig
* Neue Option bei Umfragen: Schließen und benachrichtigen. Fügt auf der letzten Seite der initiierten Umfrage eine weitere Benachrichtigung ein, wenn die Umfrage vollständig ausgefüllt wurde
* Unterstützung für mehrfache Filter bei der Umfrage Benachrichtigung hinzugefügt
* Fragenbaum Navigation mit zusätzlicher Prüfung auf geänderte Antworten
* Gruppenumfragen Ansicht zeigt keine beendeten Umfragen mehr bei einer erstellten Instanz
* Auswertungen bei einer Compliance Umfrage die noch nicht vollständig ausgefüllt ist, zeigt die weiteren kommenden & offenen Fragen mit einem roten X



---

-Changelog best_web 6.0.15 (04.10.2016)
* Fixed: Info an Benutzerschnellauswahl
* Fixed: Templates speichern, editieren
* Geändert: Tooltips bei Umfragen Ergebnisbaum
* Geändert: Gruppenumfrage Aktualisierung
* Geändert: Installationsroutine Struktur: etc/infoserver.ini etc/ssl/*, Mnesia Ordner direkt im Installationspfad


---
-Changelog best_web 6.0.14 (28.09.2016)
* Fixed: Suchen der LDAP-Gruppen nicht mehr limitiert auf 10 Zeichen
* Fixed: Aufrufen der Gruppenumfragen und Umfragen
* Fixed: Multi Search Grid
* Fixed: Gruppenumfrage Intervalle zur Initiierung