# best_web.exe Version´s

> Current best_web.exe 6.0.16 - http://download.cordaware.com/support/v6/web/6016/best_web.exe


EN: Webinterface for bestinformed Version 6 can be downloaded here:

http://download.cordaware.com/support/v6/web/

DE: Weboberfläche zu bestinformed Version 6 hier herunterladen:

http://download.cordaware.com/support/v6/web/


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