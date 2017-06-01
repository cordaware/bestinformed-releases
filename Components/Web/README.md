# best_web.exe Version´s

All-In-One Download:
http://download.cordaware.com/support/v6/latest/bestinformed.exe

------------------
Changelog 6.0.46 (01.06.2017)
- Fixed: Gruppenmitglieder auslesen per LDAP von Apache Directory
- Optimierungen für Gruppenmanager / schnelleres Laden
- Neu: Suche im Gruppenmanager bzw. LDAP-Gruppen im Infoeditor erlaubt jetzt Wildcards * oder ? für die Namenssuche
- Neu: Gruppenmanager - Anzeige der Mitglieder als DN-Syntax im Gruppenbaum
- Geändert: Infoeditor bei den LDAP-Gruppen zeigt jetzt keine OU´s mehr an
- Geändert: Contentverwaltung - Hochladen in die Ordner Icons/Images/Sounds ab jetzt erlaubt
- Neu: Migration - Anzeige eines Ergebnis bei der Durchführung der Migration (Es werden die Namen angezeigt und ein Status z. B. grüner Haken oder ein rotes Kreuz, bei Gruppen kann auch ein weiterer Zustand angezeigt werden, falls nicht alle Mitglieder einer Gruppe migriert werden konnten)
- Neu: Verbesserte Migration von Templates und deren Inhalte (Sprachen, Channels, Gruppen, Auschlussgruppen)
- Neu: Unterstützung für weitere Filter-Möglichkeiten (Gruppen, OU´s mit LDAP-Attributen) 

------------------
Changelog 6.0.45 (16.05.2017)
* Neue Rechte in den Rollen für Empfangsübersicht 
* Fixed: Anzeige der richtigen ScriptVar Ressourcen im Infoeditor
* Geändert: Verbindungsübersicht -> Historie Schaltfläche nicht anzeigen wenn das Recht nicht gesetzt wurde
* Neues Recht in den Rollen für den Infoeditor „Info entwarnen erlauben“
* Geändert: Anzeige des Benutzername, Domäne in der Infoübersicht
* Neu: Infoübersicht Schaltflächen für Infohistorie, Info/Szenario entwarnen oder Empfangsübersicht anzeigen werden ausgeblendet, wenn der Benutzer nicht das Recht hierfür hat
* Spalten für Empfangsübersicht einschränken (Ausnahme: Gilt nicht für Response einer Info einsehen!)
* Fixed: Rollen -> Ressourcen Mitbenutzung umbenannt von Profilebene auf Rollenebene
* Neu: Domänen - neue Checkbox ob ein RootDSE verwendet werden soll oder nicht, um das LDAP zu lesen.

------------------
Changelog 6.0.44 (08.05.2017)
* Hilfe Dateien für Deutsch / Englisch ausgetauscht
* Geändert: Cluster "Die Secrets stimmen nicht überein"

------------------
Changelog 6.0.43 (21.04.2017)
* Neu: Anzeige des Hostname im Browsertitel (änderbar in der Sektion best_web unter hostname=SERVER123 im Serverboard)
* Fixed: Verbindungsübersicht der Clientverbindungen
* Fixed: Anzeige der Empfangsübersicht nur wenn die Verbindungsübersicht erlaubt ist
* Fixed: DICV Generator in der IniFile App
* Fixed: DICV Type Stores in der IniFile App
* Neu: Statistik App ist jetzt Responsive
* Geändert: Gruppenmanager - Es wird jetzt eine Fehlermeldung angezeigt, wenn Gruppen nicht importiert werden konnten. Es werden auch die Gruppennamen angezeigt, die nicht importiert werden konnten
* Fixed: Gruppenmanager - Die Anzahl der lokalen Infoserver Gruppen wurden falsch berechnet
* Fixed: Eingabe im Datum-Feld (Beginn/Ende) im Infoeditor (Synchronisation der Zeiten für Beginn und Ende)
* Neu: Angabe der Position für ein Popup im Infoeditor (Standardanzeige mittig) - mittig, links (oben), links (unten), rechts (oben), rechts (unten)
* Neu: Channel sind jetzt nach Namen sortiert
* Neu: Cluster sind jetzt nach Namen sortiert
* Neu: Cluster Status (Online, Offline, Waiting) - Der Status Waiting existiert nur beim Typ Datenbank, d.h. dieser Zustand tritt nur dann auf falls nicht alle 3 Datenbanken (bi_data,bi_client_info,bi_chat) nicht repliziert werden
* Neu: Cluster bei denen der Haken im Formular auf nicht aktiv gesetzt ist, werden in der Übersichtstabelle der entsprechenden Zeile grau markiert
* Geändert: Sicherheitsprüfung beim Template speichern für ADMIN Benutzer

------------------
Changelog 6.0.42 (04.04.2017)
* Fixed: Vererbte Gruppierungen als Ressourcen im Infoeditor
* Neu: ScriptVars als Mehrfachauswahl
* Neu: ScriptVars „Liste alphabetisch sortieren lassen“ möglich für die Typen Einzelauswahl und Mehrfachauswahl
* Geändert: Policies in der Navigation wurde umbenannt zu Team
* Geändert: Textdateien mit Typ „filegroup“ oder „text“
* Geändert: Cluster Typ Server -> umbenannt zu Infoserver
* Geändert: Hilfe Datei öffnen
* Geändert: Guardians Fenstertitel nur Aktionen möglich: „Nur Benachrichtigung“, „Fenster schließen“, „Fenster schließen und Prozess anhalten“
* Fixed: Synchronisation des Infoeditor wenn immer das gleiche Template nacheinander geladen wird
* Fixed: Statistik App auf Touchscreen-Monitore
* Neu: CouchDB Datenbank führt zwischen 23 Uhr - 4 Uhr eine Verkleinerung der Festplatte für die Datenbanken bi_data,bi_chat,bi_client_info durch wenn die Festplatte über 70% belegt ist
* Neu: Standard Content-Inhalte (Sounds, Images, Icons)
* Neu: Migration von Gruppen aus Version 5 nach Version 6 (aktuell nur Benutzername, Computername, IP-Adresse, MemberOFNTGroup, MemberOFNTComputerGroup)

Fixed Gruppenmanager:
* Import von kompletten Gruppen aus der Domäne (z. B. alle OUs)
* Typ Script wird jetzt angezeigt
* Anzeige der einzelnen Typen für die Filter im Baum
* Beim Ändern des Gruppen-Typ wird nun eine Warnmeldung angezeigt und danach bei Änderung die zugewiesenen Filter verworfen
* Filter und Gruppen vom Typ Logon können erstellt werden
* Bei Import von AD Gruppen in eine vorhandene Infoserver Gruppe werden die Filter mit dem jeweiligen Typ der Gruppe erstellt
* Die Anzahl der aktuell vorhandenen Gruppen im Infoserver wird nun angezeigt

------------------
Changelog 6.0.41 (20.03.2017)
* Geändert: Cluster App -  „Bitte das Secret eintragen"
* Geändert: Domänen App - RAM-Speichernutzung/Domain Handlers als Felder versteckt
* Geändert: Infoeditor -> Schaltfläche geändert „ScriptVars ersetzen und weiter zur Vorschau“
* Neu - ScriptVars - für die Typen Datum oder Zeit kann ein Format gesetzt werden z. B. d.m.Y für Datum oder H:i:s für Zeit
* Geändertes Verhalten: Im Dashboard oder Infoeditor kann in der Templategruppen / Templates Auswahlliste gesucht werden.

------------------
Changelog 6.0.40 (14.03.2017)
* Fixed: Quickusers in der IniFile-App
* Neu: Anzeige des Lizenzstatus im Browsertitel
* Fixed: Dashboard Laden der Templates,Templategruppen,Gruppen für den Easy Infoeditor beim Anmelden eines Benutzers
* Fixed: Beim Entwarnen einer Info werden die QuickUsers entfernt
* Fixed: Easy IE Infoeditor - Infos senden
* Fixed: Cluster Manager beim Editieren
* (INTERNAL ONLY) - Fixed: erlang code:is_loaded()
* (INTERNAL ONLY) - Optimize doc_vsn in CouchDB Documents for Cluster - Update only when current VNS is newer
* (INTERNAL ONLY) - Fixed: Infos erstellen mit best_srv Version 6.0.33
* NEU: best_data Version 6.1.6.3 mit CouchDB Secret
* NEU: Erlang Dienst geändert für Mnesia Datenbank für Erlang best_web@127.0.0.1 - Ordner in data\mnesia\best_web@127.0.0.1

------------------
Changelog 6.0.39 (10.03.2017)
* Fixed: Cluster Manager
* Geändert: Empfangsübersicht - Spalte Host
* Task App: Spaltenbreite optimiert, Tooltips, Darstellung eines Cluster Status

------------------
Changelog 6.0.38 (09.03.2017)
* Geändert: System(global) - TsHaltGroup nur Filter/Gruppen vom Typ Infoclient erlaubt
* Neu: Vorschau Periode zu einer Info
* Templates Funktionalität für Clients -> Konfiguration
* Fixed / Implementiert: Textdatei App mit HTML Quellcode oder weiterem Inhalt möglich als Inhalt.
* Geändertes Verhalten in Template App - Editieren eines Templates öffnet entweder den Infoeditor oder die Client-Konfiguration
* Neue Spalte in der Template App „Typ“ zeigt Info oder Konfiguration an
* Internal only: Sprachbausteine in bi-lang_7 (deutsch), bi-lang_9 (englisch) docs in der Datenbank
* Neue Script Operatoren für den Filter (script.is_alarm, script.is_allclear etc).
* Fixed: Setzen der korrekten Webseitensprache bei Session Timeout
* Hinweis geändert im Infoeditor: Kein Infotext für Alle Sprachen definiert
* Fixed: Checkbox „Alle Rollen“ bei Profile App
* Fixed: StatusInfo Bild vom Infoserver einfügen
* Rechtschreibung korrigiert Infoeditor -> Bitte wählen Sie hier die gewünschten Gruppierungen aus
* Korrigiert M2i Ansicht für username=admin
* Infoeditor: Generell alles mit LDAP-Gruppen verbessert
* Neu: LDAP-Gruppen per MailToInfo ansprechen
* Geänderte Darstellung in der Task App
* Cluster App: Weitere Optionen hinzugefügt für Datenbank
* Beta: Migrationsassistent Version 5 -> Version 6

------------------
Changelog 6.0.37 (22.02.2017)
* Fixed: Empfangsübersicht sortieren nach Empfangen am
* Neu: Infoeditor - IniFile - Speichern von Beginn / Ende als UTC
* Neu: Hinweismeldung im Infoeditor wenn Aktivzeit oder Beginn / Ende falsch sind
* M2I Schnittstelle mit begin,end oder begindate,enddate,begintime,endtime
* Autoupdate - Anzeige der durchgeführten Autoupdates
* Fixed: Templategruppen, Templates Auswahlliste im Dashboard und Infoeditor
* Optimierungen Infoeditor - Template laden / Standardtemplate / Zurücksetzen des Editors

------------------
Changelog 6.0.36 (17.02.2017)
* Fixed: Infoeditor zurücksetzen, wenn kein Standardtemplate gesetzt ist
* Fixed: Refresh Stores Dashboard, Standardtemplate, Templategruppen, Templates, Gruppen für EasyIE
* Geändert: Reihenfolge ScriptVars bei Szenarien
* Geändert: Verbindungsübersicht - Toolbar die Option Suche entfernt
* Geändert: Empfangsübersicht - Toolbar die Option Suche entfernt
* Intern: Verwaltung der aktuellen Verbindungsübersicht zum best_srv verbessert
* Fixed: Rolle - Ressourcen Haken bei Guardians (dynamisch - alle)
* Geändert: Vergabe von Rollen Ressourcen bei Rollen aktuell nicht notwendig - entfernt
* Neu: Anzeige der vererbten Guardians im Rollen Baum als Ressource
* Geändert: Rolle - Guardians Tagfield - Anzeige der Typen
* Fixed: Einstellung fulllogin im Serverboard
* Neu: Reboot des Webservers im Serverboard möglich

------------------
Changelog 6.0.35 (15.02.2017)
* Geändert: Guardians - Ziel ist jetzt ein Pflichtfeld
* Fixed: Guardians - Bei Fenstertitel schließen und sperren keine Zeitangabe möglich
* Fixed: Guardians - Checkbox Info Anzeigen
* Fixed: Szenarien und ScriptVar Werte beim Speichern
* Fixed: ScriptVar internal matching regular expression
* Fixed: ScriptVar Reihenfolge beim Auslesen berücksichtigen
* Fixed: Inifile mit QuickUsers
* Geändert: Intern M2I Schnittstelle anhand bi-info_default angepasst (nur für internen Gebrauch…)
* Fixed: Infoeditor Guardians Aufklappen der Auswahlliste mit einem Klick
* Neu: Benutzereinstellungen - Standardtemplate
* Geändert: Quickuser Eingabe bei einer Neuen Info + Client-Konfiguration setzt jetzt bei Benutzername ein *, wenn entweder nur Computername, IP-Adresse oder Domäne angegeben wird
* Neu: Rechte in Rollen für Guardians entfernt für Software + Archive hochladen
* Interne Änderungen bi-info_default, bi-template_default - Anpassungen der Models für Info und co.
* Neu: Anzeige von Popup: IE benutzen in den Infodetails zu einer Info

------------------
Changelog 6.0.34 (10.02.2017)
* System(global) - TsHaltGroup, SafetyGroup, DemandGroup Auswahl von Filter/Gruppen vom Typ Script nur
* Neues Dokument  bi-info_default : Stellt für die Felder einer Info die Datentypen dar (nur für internen Gebrauch…)
* Neues Dokument  bi-template_default : Template als Standard für den Ursprung jeder neuen Info, dieses Template "default" kann nicht vom ADMIN gelöscht worden und auch nur vom ADMIN angepasst werden.
* StatusInfo Gruppen: Nur Infoclient, Script, Info2Mail als Gruppen/ Filter Typ möglich
* M2I Ansicht
* Fixed: Infoeditor Hintergrundfarbe laden aus Template
* Replikations App entfernt
* Neue App: Cluster & Task
* Umbenannt im Infoeditor Guardians -> Guardian
* StatusInfo: StatusQuo Spalte zeigt jetzt „Bitte hier klicken, um den Status Quo zu ändern“
* Fixed: Optimierungen zum Info editieren, Info aus Template erzeugen, Info kopieren etc
* Fixed: Szenarien Formular Boolean Werte
* Fixed: Vererbung bei Rollen Ressourcen: Templategruppen, Szenarien, Guardians
* Fixed: Darstellung von vererbten Szenarien
* Neu: MinAlarmSendTo, MaxAlarmLoop, MinAlarmSendToTime in System(global)
* Neu: Erlang OTP 19.2


------------------
Changelog best_web 6.0.33 (01.02.2017)
* Guardians: Aktion entfernt - Prozess ausführen
* Filter, Gruppen, Gruppierungen - Neuer Typ „Script“
* Neue App: Knopfdruck
* StatusInfo Name kein _ erlaubt
* Fixed: bi_backup from database_dir
* Fixed: Info kopieren, wenn diese aus dem Easy Infoeditor erstellt worden ist
* Fixed: Overflow in der Infoübersicht (z. B. bei großen Texten)
* Fixed: Easy Infoeditor - Erweiterte Ansicht
* Fixed: Enable Info als angemeldete Rolle

------------------
- Changelog best_web 6.0.32 (25.01.2017)
* Fixed: M2I mit @@
* Geändert: Klickverhalten zum Einfügen von Bildern im Infoeditor / StatusInfodetails
* Sprachwechsel behoben
* Fixed: Autoupdate Checkbox als Boolean in System(global)
* Neu: Lizenzhinweis wenn keine gültige Lizenz gefunden wurde (erscheint als angemeldeter admin nur)
* Fixed: Duplicate Message wenn Datenbank nicht mehr erreichbar
* Anzeige des best_srv Host in der aktuellen Verbindungsübersicht + Historie


------------------
- Changelog best_web 6.0.31 (23.01.2017)
* Autoupdate
* StatusInfo: Statusdetails geändert
* Infoeditor: Fixed App Wechsel zu Guardian und Channel über die Plus Schaltfläche
* Client-Konfiguration: Address and Port ist nicht mehr emptyText und für weitere Felder wurde es ebenfalls geändert
* Infohistorie: Anzeige der Empfänger + Aufruf der Empfänger
* Guardians können aus der App als neue Info direkt verschickt werden
* Fixed: Statistik App HDD Speicherbelegung (Frei / Genutzt war vertauscht)
* Neu: Replikation App
* Infofelder werden jetzt im Infoeditor angezeigt
* Fixed: Dashboard Layout bei Fenstergröße ändern
* Geändert: StatusInfo Details (Felder für Channel, Typ)
* best_script: member_of_filegroup
* Suche und Sortierungen in der Empfangsübersicht für gesendete, empfangene Infos + Response
* Guardians: Neue Option beim Erstellen: Info anzeigen für Fenster / Prozesse

------------------
- Changelog best_web 6.0.30 (20.12.2016)
* Hilfedateien (deutsch & englisch)
* Lizenz: Compliance hinzugefügt

------------------
- Changelog best_web 6.0.29 (15.12.2016)
* Infoeditor Optimierungen
* Client-Konfiguration

------------------
- Changelog best_web 6.0.28 (12.12.2016)
* Neuer Infoeditor
* Templates exportieren / importieren
* uvm.

------------------
-Changelog best_web 6.0.27 (24.11.2016) - NOT FOR PUBLIC

* weitere Tooltip Konfiguration (benutzerdefiniert) über das Serverboard einstellbar
* Umfragen: Prüfung auf 100% / Bestätigen und Zurückweisen bietet die Möglichkeit zur Angabe eines Kommentars
* Umfragen: werden Umfragen über die Schaltfläche (Schließen und Benachrichtigen) geschlossen - so befindet sich anschließend die Umfrage aktuell in Prüfung, wenn ein Benutzer die Umfrage erneut öffnen möchte

------------------
-Changelog best_web 6.0.26 (15.11.2016)

* Standardmäßiges ADMIN-Passwort und für die M2I-Schnittstelle: bestinformed
* Neue Statistik für die durchschnittliche Anzahl der Clientverbindungen in den letzten 7 Tagen
* Neue Rechte für Umfragen in den Rollen (Benachrichtigungen für Umfragen erlauben, Anzeige der Gruppenumfragen, Ansicht für Umfragen / Initiierte Umfragen / Gruppenumfragen anhand der Anmeldegruppen-/filter einschränken)
* Geänderte Auswertung bei Anzeige der Umfrage Ergebnisse für Compliance Umfragen
* Hilfe für Deutsch / Englisch aktualisiert

------------------
-Changelog best_web 6.0.25 (09.11.2016)

Font Awesome:
* Neue Version -> 4.7
 
Clients -> Konfiguration:
* Verbesserung des Scrollverhaltens
* Optimierung des Empfänger-Tabs
 
Neue Info:
* Layoutanpassungen bei Schaltflächen
* Entwarnungs-ID kann jetzt verwendet werden
* Guardians -> Neue Elemente wurden nicht in der Auswahlbox synchronisiert
* Template laden ->Beschreibung wurde nicht in das Formular geladen
 
Templates:
* Löschen des Templates optimiert
* Workflow -> Template editieren und Template laden sind jetzt 2 getrennte Funktionen
 
EasyIE:
* Templategruppen implementiert
 
Concierge:
* App-Icon eingebaut

Allgemein:
* Auswahlfeldern erfodern bei bestimmten App´s eine Auswahl (keine manuelle Eingabe möglich)

Gruppenmanager:
* Erlang Funktion verbessert beim Importieren von Gruppen/Benutzer und co.

Channels:
* Verwendet immer Pascal Scripte (aktuell noch kein Erlang Script möglich)

------------------
-Changelog best_web 6.0.24 (03.11.2016)

* Scripteditor: Tooltip für Script in der Tabelle
* Umfragen: Sprache korrigiert für Englisch
* Umfragen: Benachrichtigung geändert zum Auslesen der E-Mail Adressen
* Filter: Regulärer Ausdruck hinzugefügt als Filter Operator

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