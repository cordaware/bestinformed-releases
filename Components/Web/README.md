# best_web.exe Version´s

------------------

Changelog 6.0.150 (06.09.2018)

- Neu: Benutzerdefiniertes Menü - Gruppierung kann aktiviert werden (Standardwert: false)

------------------

Changelog 6.0.149 (04.09.2018)

- Testlizenz bis 31.12.2018

------------------

Changelog 6.0.148 (29.08.2018)

- Weitere Verbesserungen für das Auslesen der Domäne / LDAP
- Der Gruppenmanager zeigt nun für Benutzer & Computer die zugewiesenen Gruppen und OU´s.
- Der Gruppenmanager zeigt beim Aufklappen einer Gruppe die enthaltenen Mitglieder (Benutzer, Computer)

------------------

Changelog 6.0.147 (27.08.2018)

- Neu: System (global) - Alarm Icon bei keinem Computer einstellbar

------------------

Changelog 6.0.146 (23.08.2018)

- Weitere Performance Verbesserungen für das Auslesen der Domäne / LDAP

------------------

Changelog 6.0.145 (22.08.2018)

- Interne Optimierung beim Laden von statischen Dateien für die Weboberfläche
- Das Auslesen von Gruppen,Benutzer,OU,Computer über LDAP wurde verbessert
- In "Nachrichten,Berechtigungen" werden jetzt mehr Informationen bzgl. des Auslesen der Domäne aufgelistet
- Fixed: Anzeige des StatusQuo in der StatusInfo App
- Fixed: Client-Konfiguration speichern / editieren wurde verbessert

------------------

Changelog 6.0.144 - DEVELOP ONLY

------------------

Changelog 6.0.143 (03.08.2018)

- Gruppenmanager zeigt nun für die Benutzer die zugewiesenen Gruppen aus dem LDAP

------------------

Changelog 6.0.142 (02.08.2018)

- Weboberfläche für Internet Explorer 11 Kompatibilität verbessert

------------------

Changelog 6.0.141 - DEVELOP ONLY

------------------

Changelog 6.0.140 (23.07.2018)

- Fixed: Szenarien entwarnen
- (INTERNAL) Fixed: Childs stoppen im bi_connection_mgr des Clusters

------------------

Changelog 6.0.139 (20.07.2018) - DEVELOP ONLY
- Suche geändert in der Verbindungshistorie und Verbindungsübersicht
- Suche geändert für alle anderen Grids / Sucht nun nicht mehr nach dem eingegeben Anfangstext sondern jetzt global.

------------------

Changelog 6.0.138 (17.07.2018) - DEVELOP ONLY

- Neu: Audit-Ansicht eines Alarmes gibt nun detaillierte Informationen über den Auslöser aus
- Export als JSON für Empfangsübersicht (Empfangen, Gesendet, Response)
- Neu: Sencha Version 6.6.0.258

------------------

Changelog 6.0.137 (17.07.2018) - DEVELOP ONLY

- Neu: Der Alarmtyp "Info an Empfänger des Templates" kann nun mit Alarm-Variablen und Alarm-Rückmeldung genutzt werden
- Domänen Manager startet sich bei Verbindungsverlust zum LDAP erneut neu.

------------------

Changelog 6.0.136 (14.06.2018)

- Neu: Verbindungsübersicht zeigt die Anzahl der Passiven Verbindungen. Hierzu wird aus dem Serverboard der Eintrag [best_mqttc] uuid= verwendet oder aus den Cluster best_srv Datensätzen die UUID zur Ermittlung der passiven Verbindungen benötigt.
- Neu: Rolle hat eine neue Ressource (Infos - alle dynamisch)
- Neu: Infoübersicht - Ansicht kann für Alle Infos oder nur eigene Infos angepasst werden

------------------

Changelog 6.0.135 (13.06.2018)

- Fixed: M2I Schnittstelle bei Standard Lizenz

------------------

Changelog 6.0.134 (07.06.2018)

- Geändert: Verhalten für IniFile Infos kopieren geändert

------------------

Changelog 6.0.133 (15.05.2018)

- Neu: System (lokal) - Ausführung einer Datenbank Komprimierung
- Neu: System (lokal) - Datensätze eines Benutzers löschen (Angabe von Domäne, Benutzername)
- Neu: Es gibt neue Einträge um eine automatische Bereinigung der Empfangsübersicht, Verbindungshistorie einstellen zu können. Wird standardmäßig automatisch um 00:00 Uhr ausgeführt
* In der infoserver.ini gibt es die neuen Einträge:
* [best_web] last_clean_history =   <- speichert die letzte Ausführung für die Verbindungshistorie (Zeitstempel, z. B. 2018-05-15T00:00:00Z)
* [best_web] last_clean_client =   <- speichert die letzte Ausführung für die Empfangsübersicht (Response, Empfangen, Gesendet, Autoupdate Archiv) (Zeitstempel, z. B. 2018-05-15T00:00:00Z)
* [best_web] clean_history_after = 20160   (Angabe in Minuten, default 20160) - Bereinigt alles nach 2 Wochen standardmäßig für die Verbindungshistorie
* [best_web] clean_client_after = 20160   (Angabe in Minuten, default 20160) - Bereinigt alles in Empfangsübersicht (Response, Empfangen, Gesendet, Autoupdate Archiv) was älter als 2 Wochen ist (standardmäßig)


------------------

Changelog 6.0.132 (04.05.2018)

- Neu: Dienst wird gestoppt, wenn die Verbindung zur Datenbank abbricht
- Neu: infoserver.ini [couch] max_retries = 3 (default), nach 3 fehlerhaften Versuchen die Datenbank zu kontaktieren, stoppt sich der best_web Dienst
- Fixed: MailToInfo SMTP Authentifizierung
- Fixed: Rollen - Auswahlfeld für die Ressourcen Mitbenutzung
- Neu: Hilfesymbol für den schnellen Zugriff aus der Alarm App zu den entsprechenden Kapiteln im Hilfe Dokument
- Neu: Globale Alarm Einstellung für das Verhalten bei Rechner mit aktivem Bildschirmschoner / gesperrten Zustand
- Neu: Beim Alarm-Typ "Alarm an alle Infoclients" kann man nun optional den Alarm ebenfalls für den Auslöser anzeigen lassen
- Fix: Falls die Navigation durch Alarm App reduziert wurde und bisher keine Usersettings gesetzt wurden, änderten sich die Standardsettings bzgl. des Infoversands

------------------

Changelog 6.0.131 (20.04.2018)

- Fixed: Sicherheitsprüfung und Änderungen bzgl. Speichern von Templates als ADMIN, Rolle
- Fixed: Rollen können keine vererbten Template-Ressourcen vom ADMIN bearbeiten

------------------

Changelog 6.0.130 (18.04.2018)

- Fixed: Öffnen vom LDAP Import Fenster ohne Lizenz
- Neu: Alarm LDAP Zuordnungen können nun bei Installationen ohne Cluster-Betrieb automatisch synchron gehalten werden

------------------

Changelog 6.0.129 (16.04.2018)

- no changelog available, only development

------------------


Changelog 6.0.128 (16.04.2018)

- Fixed: Quickuser hinzufügen im Infoeditor, Client-Konfiguration
------------------

Changelog 6.0.127 (05.04.2018)

- Fixed: gelöschte Datensätze die bereits gelöscht sind und in der Oberfläche nochmal gelöscht werden
- Fixed: Infos die abgebrochen oder in der Historie sind und anschließend als Template gespeichert werden.

------------------

Changelog 6.0.126 (05.04.2018)

- Gelöschte Datensätze werden jetzt anders gespeichert in der Datenbank
- Geändert: Audit bei gelöschten Datensätzen

------------------

Changelog 6.0.125 (04.04.2018)
- Neu: Der Alarm Plan kann nun auch Computer-Raum Zuordnungen ausgeben
- Fixed: System (global) - bei Infoversand

------------------

Changelog 6.0.124 (22.03.2018)

- Fixed: Cluster Status für Infoserver
- Neu: Spalte "Geräte-Typ" in der Verbindungsübersicht. Bei Mobile wird die Zeile als hellgrün markiert
- Neu: Wenn in der Alarm App Räume umbenannt werden, bleiben Zuordnungen vorhanden
- Geändert: Kein Beep mehr beim Entwarnen von Alarmen

------------------

Changelog 6.0.123 (12.03.2018)

- Fixed: Cluster Status für Infoserver

------------------

Changelog 6.0.122 (07.03.2018)

- Fixed: Datenbank Änderungs Feed - Benachrichtungen innerhalb der Weboberfläche

------------------


Changelog 6.0.121 (05.03.2018)

- Cluster Standardwerte geändert
- Fixed: Contentverwaltung Dateinamen

------------------

Changelog 6.0.120 - not available

------------------

Changelog 6.0.119 (26.02.2018)

- Wichtig: Verbindungsübersicht verbessert
- (INTERNAL ONLY) code loader best_data optimized
- Anzeigeformat Zahl angepasst für Verbindungen, Empfangsübersicht

------------------

Changelog 6.0.118 (09.02.2018)

- Alarm Texte für Sprache Englisch geändert

------------------


Changelog 6.0.117 (07.02.2018)

- (INTERNAL ONLY) - changed service to restart onfail

------------------

Changelog 6.0.116 (07.02.2018)

- Zähler für Migration von Gruppen verbessert
- Migration 5to6: MemberOfNT.. unterstützt jetzt auch DOMÄNE\Gruppenname und wird zur Standarddomäne konvertiert.
- Migration 5to6: StatusInfo Migration verbessert
- (INTERNAL ONLY) - changed beam module for best_data

------------------


Changelog 6.0.116 (07.02.2018)

- Zähler für Migration von Gruppen verbessert
- Migration 5to6: MemberOfNT.. unterstützt jetzt auch DOMÄNE\Gruppenname und wird zur Standarddomäne konvertiert.
- Migration 5to6: StatusInfo Migration verbessert
- (INTERNAL ONLY) - changed beam module for best_data

------------------

Changelog 6.0.115 (02.02.2018)

- (INTERNAL ONLY) - hackney app new vsn

------------------


Changelog 6.0.114 (31.01.2018)

- Neu: Erlang 20.2

------------------

Changelog 6.0.113 (29.01.2018)

- Neu: Erweitere Anpassung der Eskalationsstufen im Alarm Visualizer
- Neu: Kopieren von Datensätzen in den folgenden Apps: Channel,ScriptVar,Template,Konfiguration,Domäne,Filter,Rolle
- Neu: Höhe für Navigation (links) reduziert

------------------

Changelog 6.0.112 (January 2018) - ONLY DEVELOP

- Fixed: Info / IniFile. Standardwert für quickusersadditional ist default true.

------------------

Changelog 6.0.111 (January 2018) - ONLY DEVELOP

- Fixed: Lademaske im Serverboard beim Hinzufügen von neuen Einträgen

------------------

Changelog 6.0.110 (January 2018) - - ONLY DEVELOP

- Fixed: Infoeditor bei Benutzer als Rolle angemeldet (ohne Recht: LDAP Gruppen erlauben)
- Fixed: Suche von LDAP-Gruppen ohne ausgefüllte Benutzersuche, zeigt nur den Zweig der Gruppen an
- Neu: Anzeige der ausgewählten Hintergrundfarbe für Infotext / Caption in der Infoübersicht - Einstellbar in [general] info_overview_background=true/false (default: true)
- Neu: Anzeige der zugewiesenen Domäne in der Verbindungsübersicht
- Neu: Quickusers im Infoeditor, die zugewiesene Domäne kann mit #cordaware300 adressiert werden. Normale Domäne des OS bleibt nach wie vor gleich.
- Neu: Alarm Visualizer ist nun direkt von der Hauptseite der Alarm App aufrufbar
- Neu: Erstellung von Alarmen mit nur einer Taste möglich
- Neu: Panikalarm (Auslösen eines Alarmes mit einer Anzahl von beliebigen Tasten)
- Neu: Optimierung des Ladens von externen Daten in der Alarm App
- Fix: Darstellungsfehler in der Übersicht der verfügbaren Räume in den Alarmierungskreisen

------------------

Changelog 6.0.109 (08.01.2018)

- Neue Testlizenz gültig bis 31.03.2018
- Fixed: E-Mail Validierung Formular
- Fixed: Login Hinweismeldung bzgl. Sencha Framework 6.5.2
- Neu: Filterung der Auslöseräume in der Übersicht der Alarm-Eskalationsstufen
- Fix: Behebung eines Fehlers beim Löschen von mehreren zugeordneten Räumen mit Kommas
- Fix: Erstellung und gleichzeitige Zuweisung von mehreren Räumen mit Kommas

------------------

Changelog 6.0.108 (21.12.2017)

- Aktualisiert auf Sencha Framework 6.5.2
- Beta: Clients -> Registriert als APP
Alarm:
- Neu: Hinweis auf doppelte Zuordnungen beim Öffnen der Alarm App
- Neu: Alarm ScriptVars und die Auslöser Rückmeldung ist nun beim "Alarm an alle" möglich
- Neu: Alarm Visualizer kann nun auf bestimmte Eskalationsstufen begrenzt werden
- Neu: Optimierung beim Versand von neuen Alarm Einstellungen

------------------

Changelog 6.0.107 (11.12.2017)

- Audit Modus kann im Serverboard bei [bi_audit] audit=true (type: boolean - default: true) an/aus geschaltet werden.
- Debug vom best_srv kann im Nachrichten-Panel im Serverboard mit [general] debugtoweb=true (type: boolean - default: true) an/aus geschaltet werden.
- Bei der Infoeditor Vorschau kann die ScriptVar Anzeige im Serverboard positioniert werden [best_web] dock_scriptvar_preview=bottom/top (default: bottom - or top allowed
- Fixed: Domänen App - Auswahlliste/TagField für weitere Domänen (weitere Einstellungen)
- Optimierungen für LDAP Gruppen im Infoeditor
- Fixed: Szenarien entwarnen mit ScriptVars
- Mehr Informationen / Details in den Infodetails hinzugefügt
- Neu: Löschen von mehreren Gruppen gleichzeitig
- Neu: Alarm Visualizer (Zeigt Zuordnung graphisch dar)
- Neu: Generierung einer PDF-Datei mit Alarm Zuordnungen
- Fixed: Falsche Alarm Anzeigenamen im Popup nach LDAP Usernamen Import

------------------

Changelog 6.0.106

- no changelog available, only development

------------------

Changelog 6.0.105 (28.11.2017)

- Neue Guardian Optionen unter System(global) zum Einschränken der Aktionen für Prozesse & Fenstertitel


------------------

Changelog 6.0.104 (24.11.2017)

- Fixed: Domänen / LDAP Monitor


------------------

Changelog 6.0.103 (23.11.2017)

- Fixed: Domänen / LDAP Monitor
- Fixed: 500er Internal Server Error - Crashes bei nicht verbundener Datenbank
- Neu: [general] keep_info_begin_end=true/false (default: true) -> Behält beim Kopieren von Infos bei noch aktiver Zeit den Beginn / Ende. Bei keep_info_begin_end=false ist immer Beginn / Ende auf leer gesetzt bei einer kopierten Info
- Neu: [general] init_scriptvar_copy=true/false (default: true) -> ScriptVar Werte werden beim Kopieren einer Info beibehalten.
- Neu: [general] init_scriptvar_allclear=true/false (default: true) -> ScriptVar Werte werden beim Entwarnen einer Info beibehalten.
- Verbesserungen: Schnellere Migration beim Alarm Konfigurationsmanager aus der Version 5

------------------

Changelog 6.0.102 (20.11.2017)

- Neu: Migration von Poweruser zu Rollen nach Version 6
- Neu: Migration von StatusInfos nach Version 6
- Neu: Lizenz (Demand) -> Konfiguration herunterladen (als JSON)
- Fixed: Umfragen - Bearbeiten / Ansicht von Umfragen
- Fixed: Rollen / Rechte Überprüfung für ac_guest (Gastanmeldungen) bei Umfrageteilnehmer

------------------

Changelog 6.0.101 (17.11.2017)

- Neu: Verbindung zum best_srv TLS/PSK
- Neu: Migration von AKM zur V6 Alarm App
- Neu: Optionale Anpassung der Navigation an die Alarm Funktionalität

------------------

Changelog 6.0.100 (16.11.2017)

- Neu: System (global) - "Für nicht bekannte Domänen in der Verbindungsübersicht wird die Standarddomäne (siehe oben) verwendet."
- Neu: Demo Lizenz hinzugefügt
- Fixed: Sencha Fieldset Text bei Mac OS Safari / iOS 11

------------------

Changelog 6.0.99 (08.11.2017)

- Fixed: Contentverwaltung Grid
- Geändert: On Demand Lizenz Prüfung

------------------

Changelog 6.0.98 (06.11.2017)

- Neu: Geänderte Namen von Ressourcen werden automatisch in den Zuordnungen übernommen
- Neu: Hinzufügen Buttons in der System Global App für Alarm Ressourcen hinzugefügt
- Fixed: Beispiel Basis Alarm bei Erstkonfiguration der Alarm App
- Fixed: Einige Textanpassungen in der Alarm App

------------------

Changelog 6.0.97 (27.10.2017)

- Performance Verbesserungen beim Laden von Datensätzen
- Neu: Im Migrationsassistenten können jetzt auch Logon Gruppen migriert werden (Achtung: Standardomäne muss zuvor gesetzt sein)
- Neu: Timeout beim Migrationsassistenten erhöht auf 30 Minuten
- Geändert: Ausgabe des Ergebnis im Migrationsassistenten
- Geändert: Infos (Ressourcen Mitbenutzung) - in der Infohistorie werden keine Infos vom ADMIN aufgelistet.
- Neue Filter Optionen: client.sessionusername, client.sessioncomputername, client.sessiondomain
- Einstellbares Format für {TIMESTAMP} in der E-Mail Umfrage Benachrichtigung im Serverboard unter [bi_survey] timestamp=d.m.Y (default: d.m.Y H:i:s)
- Fixed: Anmeldemaske für Sprache-Auswahlfeld
- Fixed: "Umfragen, initiierte Umfragen, Gruppenumfragen anhand von den Anmeldegruppen einschränken"
- Neu: In den Filter Scripten kann die Erlang Funktion integer_to_binary verwendet werden
- Neu: Alarm Einstellungen wurden stark erweitert wodurch nun mehr Anpassungmöglichkeiten gegeben sind
- Neu: Navigation durch die Alarm Auslöser- zu Empfängerzuordnungen per Tastatur
- Neu: Alarme werden nun in der aktuellen Sprache der Weboberfläche generiert
- Fixed: Groß- und Kleinschreibung bei Alarm Anzeigenamen LDAP Import wurden nicht beachtet
- Fixed: Darstellungsproblem beim Alarm LDAP Import von Räumen mit bestimmten Satzzeichen
- Fixed: Englische Alarm App öffnet sich nicht
- Fixed: Fehlerhaftes Scrolling in Alarm App bei Rechnern mit Touchscreen

------------------

Changelog 6.0.96 (19.10.2017)
- Geändert: Lizenz Compliance Umfragen
- Geändert: SMTP Benachrichtungen über die Weboberfläche (Umfragebenachrichtigungen oder SMTP Einstellungen testen) - für neuere SMTP Server kann man die TLS Versionen für den SMTP Verbindungsaufbau einstellen über das Serverboard in
[bi_smtp] tls_connect=['tlsv1', 'tlsv1.1', 'tlsv1.2']  <- (default)


------------------

Changelog 6.0.95 (18.10.2017)
- Neu: Setzen des "Benutzername", "Anmelden als" über http://localhost:8000/?name=BENUTZERNAME&logon=LOGONUSER
- Fixed: Filter testen als angemeldeter Domänenbenutzer. Achtung: Beachten der Rollen Ressourcen Filter/Gruppen/Gruppierungen!

------------------

Changelog 6.0.94 (16.10.2017)
- StatusInfo: Sprache bei Statusdetail in der Übersicht hinzugefügt

------------------

Changelog 6.0.93 (13.10.2017)
- Geändert: Guardians Script beim Anlegen von einem neuen Guardian
- Fixed: Standard Icons,Sounds,Images in der Contentverwaltung

------------------

Changelog 6.0.92 (12.10.2017)
- Neu: Guardians - Auswahl eines Prozess bei der Verwendung des Typ "Fenstertitel"
- Geändert: Beginn / Ende werden bei einer kopierten Info behalten, wenn die Info noch nicht abgelaufen ist.

------------------

Changelog 6.0.91 (09.10.2017)
- Verhalten geändert: bei [general] allclear_only=false wird der Tab "Empfänger" automatisch aktiviert. Im Infoeditor werden die Filter/Gruppen/Gruppierungen automatisch von der Ursprungs-Info übernommen

------------------

Changelog 6.0.90 (09.10.2017)
- Neue Optionen unter System -> System (global): Clientanmeldegruppe, Clientauthentizitätsgruppe.

------------------

Changelog 6.0.89 (06.10.2017)
- Neu: [general] info_source_edit=false (default: false) - Schaltet den Infoeditor standardmäßig in den HTML Source bearbeiten Modus
- Neu: [general] template_source_edit=false (default: false) - Schaltet den Infoeditor standardmäßig in den HTML Source bearbeiten Modus, wenn ein Template bearbeitet wird.
- (VERALTET!!!!) Neu: bei [general] allclear_only=false werden im Infoeditor die Filter/Gruppen/Gruppierungen (aber keine vom Typ "Infoclient") der Ursprungs-Info übernommen

------------------

Changelog 6.0.88 (05.10.2017)
- Neu: Cluster Optionen für Infoserver - UUID und Infoserver wird für Info2Mail verwendet
- Neu: Content - Upload von mehreren Dateien gleichzeitig möglich, Upload-Vorgang optimiert und schöner gestaltet
- Neu: System (global) - Alarm-Icon (wenig Computer), Alarm-Icon (genügend Computer)
- Fixed: StatusInfo HTMLEditor Synchronisation

------------------
Changelog 6.0.87 (28.09.2017)
- Lizenzen und Hinweismeldungen optimiert

------------------
Changelog 6.0.86 (27.09.2017)
- Lizenzoptionen / Hinweismeldungen wurden implementiert
- Fixed: Jumping beim Anklicken von Optionen in der Rollen App (Rechte, Ressourcen)
- Neu: Hinweis in der Rollen App bei den Ressourcen
- Neu: Neues Recht bei den Rollen für Neue Info "Mail2Info - Schnittstelle für Infoversand erlauben" in Verbindung mit "Erstellen von Infos erlauben", Benutzer können jetzt auch die Mail2Info-Schnittstelle verwenden. Authentifizierung der Benutzer erfolgt über LDAP.
- Fixed: Filter testen
- Geändert: Farbe für Filter Schaltflächen UND / ODER
- Neue Filter Operatoren (endet mit, endet nicht mit)
- Neu: [general] allclear_only=true (default: true) - Verhalten einstellbar für das Entwarnen von Infos, ob auch weitere Filter/Gruppen sofort ausgewählt werden können.
 
------------------
Changelog 6.0.85 (21.09.2017)
- Mehr Optionen in der Client-Konfiguration bei den Clienteinstellungen
- Verbesserungen beim Einspielen einer Lizenz

------------------
Changelog 6.0.84 (19.09.2017)
- Geändert: Lizenzserver

------------------
Changelog 6.0.83 (19.09.2017)
- Fixed: Infohistorie Status (beendet, abgebrochen)
- Fixed: Infohistorie Baum / Jahre und Monatsdarstellung
- Fixed: Benutzerdefiniertes Menü / Benutzereinstellungen
- Korrigiert numerierte -> nummerierte im WYSIWYG-Editor

------------------
Changelog 6.0.82 (18.09.2017)
- Fixed: Standardwerte beim Erstellen einer neuen Info aus der Guardian App / Verbindungsübersicht
- Fixed: Statistik App - Datenbank - Ausgabe der Größe in MB

------------------
Changelog 6.0.81 (15.09.2017)
- Kompatibilität für CouchDB 2.1 erweitert

------------------
Changelog 6.0.80 (13.09.2017)

- Neue Lizenzoptionen
- Fixed: Szenarien versenden wenn Änderungen am Infotext / Entwarnungen nicht erlaubt ist
- Fixed: Rechtezuweisung bei Guardians: Löschen von dynamischer Guradians -> Beschreibung war falsch
- Neu: Zusätzliche Alarm Empfänger, Notfall-Gruppe, Eskalationsgruppe in System (global)
- Neu: Automatischer Upload von Filegruppen, Intervall einstellbar im Serverboard [bi_filegroup] interval= (default: 60)
- Fixed: Sencha Tagfield reset of field
- Automatische Aktualisierung der Ressourcen / Rechte für angemeldete Benutzer
- Optimierungen für Benachrichtungen an die Weboberfläche über den Websocket
- Neu: Ressourcen Mitbenutzung von Infos
- Optimierte Anzeige der InfoclientValues, Channels, DynamicInfoclientValues in der Verbindungsübersicht
- Kompatibilität für CouchDB 2.1
- Neue Optionen in System (global) für Alarm: Zusätzliche Alarm-Empfänger, Notfallgruppe, Eskalationsgruppe
- In Scripten kann jetzt zusätzlich das Module "binary" verwendet werden, z. B. für binary:replace/3 etc.

------------------
Changelog 6.0.74 (21.07.2017)
- Geändert: Rollen Ressourcen Mitbenutzung
- Neu: Anzeige des angemeldeten Benutzers im Titel des Browsers

------------------
Changelog 6.0.73 (19.07.2017) 
- (INTERNAL ONLY) Erlang Mnesia Tabellen zuerst erzeugen lassen

------------------
Changelog 6.0.72 (17.07.2017) 
- Fixed: Zeichenkodierung bei Dateinamen beim Upload von Dateien (z. B. in der Contentverwaltung)
- Geändert: Temporäres Laden von Domänen verwendet jetzt Erlang ETS-Tabellen
- (INTERNAL ONLY) - Start Scripte für die Applikation angepasst

------------------
Changelog 6.0.55 (13.07.2017) 
- Interne Verbesserungen für die Verwaltung der Verbindungsübersicht
- (INTERNAL ONLY) Erlang Nodetool

------------------
Changelog 6.0.53 (10.07.2017) 
- Weitere Verbesserungen beim Starten der Erlang Datenbank Mnesia
- Erlang Tuning

------------------
Changelog 6.0.51 (07.07.2017) 
- (INTERNAL ONLY) In ranch.app there must be add ssl to applications!!!!!
- (INTERNAL ONLY) Erlang Supervisor angepasst für best_web, bi_auth, bi_interval, bi_kvs, bi_uuid 
- Verbesserungen beim Starten der Erlang Datenbank Mnesia
- Neue Start Scripte unter Windows für die Applikation best_web
- Wechsel zu Erlang Version 19.3 (8.3)
- Fixed: Abbrechen der Domänen Aktualisierung, wenn die Domäne gelöscht wird.
- Neu: Angabe von Alias in der Domäne, einzelne Domänen können in einer Komma-getrennten Liste angegeben werden
- Geändert: Beschreibung für den Namen der Domäne wurde in der App ausgetauscht
- (INTERNAL ONLY) Neu: best_domain_client ??? 

------------------
Changelog 6.0.48 (19.06.2017) - ONLY DEVELOPMENT VERSION
- Neu: Filter Operator : beginnt mit / beginnt nicht mit
- Geändert: Nur Filter können getestet werden vom Typ Infoclient / Logon
- Fixed: Filter Wizard
- Fixed: Gruppenmanager - schnelleres Laden der Infoserver-Gruppen
- Neu: Domänen Live-LDAP Synchronisation
- Neu: Unterstützung weiterer Domänen für eine Clientverbindung (Benutzername muss bei den Domänen identisch sein)

------------------
Changelog 6.0.47 (02.06.2017)
- Fixed: Gruppenmanager - Import von vorhandenen Gruppennamen
- Geändert: Gruppenmanager - Fehlermeldung bei vorhandenen Gruppennamen
- Fixed: Migration von Templates und beeinhaltenden Gruppen unter Windows OS
- Fixed: Migration von Templates mit Sound, Beginn/Ende, Vollbildschirm-Popup
- Geändert: Gruppenmanager zeigt nur Gruppen vom Typ Infoclient / Logon

------------------
Changelog 6.0.46 (01.06.2017)
- Fixed: Gruppenmitglieder auslesen per LDAP von Apache Directory
- Optimierungen für Gruppenmanager / schnelleres Laden
- Neu: Suche im Gruppenmanager bzw. LDAP-Gruppen im Infoeditor erlaubt jetzt Wildcards * oder ? für die Namenssuche
- Neu: Gruppenmanager - Anzeige der Mitglieder als DN-Syntax im Gruppenbaum
- Geändert: Infoeditor bei den LDAP-Gruppen zeigt jetzt keine OU´s mehr an
- Geändert: Contentverwaltung - Hochladen in die Ordner Icons/Images/Sounds ab jetzt erlaubt
- Neu: Migration - Anzeige eines Ergebnis bei der Durchführung der Migration (Es werden die Namen angezeigt und ein Status z. B. grüner Haken oder ein rotes Ausrufezeichen, bei Gruppen kann auch ein weiterer Zustand angezeigt werden, falls nicht alle Mitglieder einer Gruppe migriert werden konnten)
- Neu: Verbesserte Migration von Templates und deren Inhalte (Sprachen, Channels, Gruppen, Auschlussgruppen)

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