# best_web.exe Version´s


-------------

Changelog 6.1.8.8 (07.02.2022) 

- Fixed: bestzero Initialisierung wenn SMTP Passwort und Benutzername leer sind
- INTERNAL ONLY - Upgrade to OTP-23.3.4.11

---------------

Changelog 6.1.8.3 (24.01.2022) 

- bestzero Logo für best_web

---------------

Changelog 6.1.8.2 (21.01.2022) 

- Neu: Alarme in der Berichte App werden nun mit UTC Zeit angezeigt
- Behoben: Anzeige von Alarm Daten nach AKM Import in der Berichte App
- Behoben: Session ID wird anders erzeugt und interne Pfade beim Laden von Dateien angepasst
- Passwörter in der infoserver.ini für die Weboberfläche und MailToInfo Schnittstelle werden automatisch in das neue Format pbkdf2 umgewandelt
- Passwörter für Admin und MailToInfo-Schnittstelle können nicht über das Serverboard geändert werden -> siehe System (lokal)
- INTERN - bestzero Registrierungs-Mail

---------------

Changelog 6.1.8.1 (05.11.2021) 
- Neu: Erlang 23
- Neu: Neues Recht bei den Rollen für den Infoeditor: "Infoversand nur an ausgewählte Empfänger möglich (kein Versand an Alle)"
- Neu: Umfragen können in der Historie per Mehrfachauswahl gelöscht werden
- Neu: Der automatische Import des Alarm Standortmanagers kann nun auch manuell gestartet werden
- Behoben: Alarm Zuordnungen beim Verwenden des automatischen Alarm Standortmanager Imports
- Behoben: Serverfehler beim automatischen Import von Geräten ohne vorhandene Organisation oder Alarmeinheit
- Geändert: Beim Löschen von Alarmeinheiten können Geräte aus der Einheit nun in der Alarm App neu zugewiesen werden
- Geändert: Texte und Beispiele beim Alarm Standortmanager Import / Export

-------------

Changelog 6.1.8.0 (05.11.2021) - DEVELOP ONLY
- Intern zum Testen

-------------

Changelog 6.1.7.3 (27.07.2021) 
- In der infoserver.ini können weitere Header in dieser Einstellung gesetzt werden: <br><br>[best_web]<br>
 headers = [{"Strict-Transport-Security", "max-age=<expire-time>"}, {"X-Frame-Options", "DENY"}, {"X-Content-Type-Options", "nosniff"}]

    Quelle: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security
    * max-age=<expire-time>
    The time, in seconds, that the browser should remember that a site is only to be accessed using HTTPS.

- Geändert: Fehlermeldungen bei der Authentifzierung können mit der folgenden Option eingestellt werden:
    * [general]<br>
        auth_messages=true/false (boolean, default: true)


- Fixed: Download infoserver.zip:
Es ist nun nur noch ein Download gleichzeitig möglich bis die Logfiles als Download bereitgestellt worden sind, so dass das System nicht ausgelastet wird.

- Geändert: Stacktraces in Fehlermeldungen<br><br>
[general]<br>
stacktrace =true/false (boolean, default: false)

- Verschiedene Anpassungen bezüglich der Zugriffskontrolle wurden optimiert

- Neu: weitere Cookie Optionen können mit der folgenden Option eingestellt werden<br><br>
[best_web] <br>
cookies = secure<br><br>
siehe, https://developer.mozilla.org/en-US/docs/Web/API/Document/cookie

- Behoben: iFrame werden als sandbox eingebunden

- Behoben: Browser Caching 

-------------

Changelog 6.1.7.2 (21.07.2021) 
- Neues Recht für Rollen: Info als offenes Ende versenden
- Fixed: SMTP MailToInfo Schnittstelle - Anpassungen bei nicht gefundenden Datensätze (z. B. Filter,Channel,Gruppen etc.)

-------------

Changelog 6.1.7.0 (04.05.2021) 
- Neu: Änderungen bei Alarm App Alarmierungskreisen müssen nicht mehr explizit bestätigt werden
- Neu: Info2Mail Filter kann nun einfach als Eskalationsscript unter System (Global) für ASM Alarme hinterlegt werden
- Neu: Änderungen bei ASM Alarmierungskreisen müssen nicht mehr explizit bestätigt werden

-------------

Changelog 6.1.6.9 (22.04.2021) 
- Eingetragene Reihenfolge der conn_keys in der infoserver.ini behalten für die Spalten der Verbindungsübersicht 

-------------

Changelog 6.1.6.8 (16.04.2021) 
- Neu: System (global) Gäste-Gruppe

-------------

Changelog 6.1.6.7 (18.03.2021) 
- Neu: ODER-Verknüpfung mit Empfängergruppen im Infoeditor bei LDAP-Gruppen

-------------

Changelog 6.1.6.6 (16.03.2021) 
- Anpassungen zu besthome

-------------

Changelog 6.1.6.5 
- INTERNAL ONLY ERLANG 23

-------------


Changelog 6.1.6.4 (05.03.2021) 
- Neues Recht bei Rollen: Filter löschen (von anderen Benutzern) erlauben
- Fixed: Umfrage Anmeldung,Benachrichtung,Ansichtsgruppe als ADMIN editieren

-------------

Changelog 6.1.6.2 (17.02.2021) 
- Fixed: Entwarnung einer Info versenden

-------------


Changelog 6.1.6.1 
- INTERNAL

-------------


Changelog 6.1.6.0 (14.01.2021) 
- Fixed: Darstellung der Socks Client in Übersicht Socks

-------------

Changelog 6.1.5.9 (12.01.2021) 
- Neu: Anzeige der Details (Type, Beschreibungen) beim Tagfield (z. B. bei Neue Info, Filter, Gruppen, Gruppierungen) [general]  tagfield_details=true/false (boolean, default: true)
- Neu: Neue App für Socks / Übersicht Socks Client für best_tele
-------------

Changelog 6.1.5.8 (23.11.2020) 
- Neu: Tooltips für Alarm Computer / Raum und weitere Ansichten in der Alarm App
- Behoben: Entwarnung des Typ "Alarm an alle anderen Räume" erscheint bei Clients, welche eigentlichen Alarm nicht erhalten haben
- Entfernt: Abhängigkeiten der Serverboard Alarm Einstellung "computer_to_upper" mit Raumnamen
- Behoben: ASM Entwarnung erscheint bei Clients, welche eigentlichen Alarm nicht erhalten haben
- Neu: Bei den Infofeldern kann jetzt eine Breite eingestellt werden
- Neue App - Externe registriert

-------------

Changelog 6.1.5.7 (10.11.2020) 
- Cluster Status geändert

-------------

Changelog 6.1.5.6 (06.11.2020) 
- Neu: Formatierte Gruppenliste bei einer neuen Info im Benutzer Tab
- Fixed: Safari Browser Scrollprobleme in der Rollen App

-------------

Changelog 6.1.5.5 (30.10.2020) 
- Fixed: Auslesen der E-Mail Adressen bei einer Umfrage Benachrichtigung verbessert

-------------

Changelog 6.1.5.4 (19.10.2020) 
- Geändert: E-Mails bei einer Umfrage Benachrichtung werden nacheinander erst versandt (vorher: gleichzeitig)

-------------

Changelog 6.1.5.3 (13.10.2020) 
- Fixed: Umfrage Benachrichtungen editieren und neu anlegen
- Fixed: Umfragen Auswahlliste - Bereinigung \r\n oder \n beim Initiieren von einer Umfrage
- Fixed: SMTP App - erzwinge SMTP Authentifzierung bei Angabe von Benutzername und Passwort

-------------

Changelog 6.1.5.2 (02.10.2020) 
- Geändert: Umfragen können aus der Historie gelöscht werden, hierbei werden die E-Mail Empfänger gelöscht und die Antworten/Ergebnisse zur der Umfrage aus der Datenbank.
- Geändert: Beschreibung von initierten Umfragen wird angezeigt
- Fixed: Scrollen in der Umfragen Historie wurde behoben
- Fixed: Automatischen Export berücksichtigen bei nicht beendeten Umfragen
- Fixed: Umfragenantworten von einem Benutzer zurücksetzen
- Fixed: Implementierung anderer Message-ID´s beim Versand von E-Mails
- Neu: Retries zu SMTP Server können in der SMTP-App eingestellt werden, wie oft die E-Mail versucht wird zu senden. Standardmäßig ist der Wert 3
- Neu: Übersicht der E-Mail Empfänger zur initiierten Umfrage
- Fixed: Wiederaufnehmen von Umfragen
- Fixed: Beenden von Umfragen
- Neu: Ordner können für Umfragen angelegt werden. Bei Umfragen (existierende und neue) kann der Ordner angegeben werden.

------------------

Changelog 6.1.5.1 (01.10.2020) 
- Neu: Export API Schaltfläche im Infoeditor

------------------

Changelog 6.1.5.0 (25.09.2020) 
- Neu: Export von Alarm Raum + Benutzer Zuordnungen in der Alarm App
- Neu: System -> System (global) - Einstellungen für API
- Fixed: Editieren von Infos eines anderen Benutzers
- Fixed: commatext2text for darwin-macosx64

------------------

Changelog 6.1.4.9 (19.08.2020) 
- Neue SSL-Einstellungen bei Domäne für den Verbindungsaufbau per LDAPs

------------------

Changelog 6.1.4.8 (17.08.2020) 
- Neu: System -> Events

------------------

Changelog 6.1.4.7 (31.07.2020) 
- Geändert: Maximale Werte geändert für Zufallsgenerator im Infoeditor

------------------

Changelog 6.1.4.6 (24.07.2020) 
- Neu: Neues Recht bei der Rolle für Zufallsgenerator erlauben im Infoeditor
- Fixed: Kalender Einträge im Infoeditor erstellen
- Neue Alarm + ASM Serverboard Einträge zur Anpassung des "Einmalig" Verhaltens der INI Konfigurationen.

    [alarm]
    ini_onetime=false
    
    [asm]
    ini_onetime=false

    default ist immer true

------------------

Changelog 6.1.4.5 (23.07.2020) 
- Neu: Versand von Kalender Einträgen über den Infoeditor
- Fixed: Fehler beim Laden der gesamten Infoübersicht
- Neu: Zufallsgenerator im Infoeditor im Reiter "Benutzer"

------------------

Changelog 6.1.4.4 (25.06.2020) 

- Neu: Umfrage Benachrichtigungen lassen sich in der Rolle über das Ressourcen-Mitbenutzung teilen und innerhalb der gleichen Rolle editieren.

------------------


Changelog 6.1.4.3 (23.03.2020) 

- Fixed: Infoübersicht und Infodetails, Anzeige der Channels, Dynamische Adressierung, Gruppen, Ausschlussgruppen, Filter, Ausschlussfilter, Gruppierungen, Ausschlussgruppierungen wenn diese gelöscht worden sind
- Fixed: Anpassungen beim Intervall-Server (Beginn und Ende einer Umfrage)
- Neu: Pro Umfrage kann der automatische Export der Ergebnisse auch bei nicht beendeter Umfrage eingestellt werden.
- Neu: Der Dateiname des automatischen Export der Umfragenergebnisse besteht aus Name der Umfrage + ID.
- Neu: in der infoserver.ini kann unter [bi_survey] start_at = 12:00 die Uhrzeit für den Start des automatischen Export der Umfragenergebnisse eingestellt werden.
- Neu: Beim Initiieren einer Umfrage wird eine rote Hinweismeldung von oben eingefolgen, wenn z. B. der Beginn oder das Ende einer Umfrage bereits in der Vergangenheit liegt.

------------------

Changelog 6.1.4.2 (19.06.2020) 

- Anpassungen in der Umfragen App für den Intervall-Server (Beginn und Ende einer Umfrage)
- Co-Design vor Umfragen geändert, der Titel der Umfrage wird nun mittig dargestellt und ohne blauen Balken.

------------------

Changelog 6.1.4.1 (18.06.2020) 

- Neu: In der Umfrage Benachrichtigung kann für den Typ "Neue Umfrage initiiert" ein Beginn und Ende einer Umfrage gesetzt werden. Die Uhrzeit ist jeweils automatisch auf 00:00 Uhr gesetzt.

------------------

Changelog 6.1.4.0 (17.06.2020) 

- Fixed: Umfrage Schwebendatensätze, bei der letzten Seite der Umfrage wird dem Datensatz das Feld finished: true hinzugefügt zur Identifizierung der vollständigen Antworten
- Fixed: Bei der Umfrage Auswertung werden nur Antworten berücksichtigt die finished: true enthalten
- Fixed: Co-Design und Anzeige des Umfragetitels bei Durchführung einer Umfrage

------------------

Changelog 6.1.3.9 (29.05.2020) 

- Fixed: Automatischen Survey Export Mechanismus

------------------

Changelog 6.1.3.8 (18.05.2020) 

- Geändert: Corporate-Design von Umfragen
- Neu: Automatischer Export von Umfrageergebnissen bei abgeschlossenen Umfragen:
  [bi_survey]
  automatic_export = true
  interval = 1440 ( default: 1440 in minutes)
  
  
  Ordner in dem exportiert wird:
  
  best_web\etc\survey

------------------

Changelog 6.1.3.7 (29.04.2020) 

- Neu: Infodetails zeigt nun den Zeitstempel an, wann die Info abgebrochen wurde

------------------

Changelog 6.1.3.6 (28.04.2020) 

- Fixed: Standortmanager wurden in der Manager PDF Ausgabe nicht angezeigt

------------------

Changelog 6.1.3.5 (24.04.2020) 

- Neu: Neues Rollen Recht im Infoeditor "Empfänger Optionen als ODER-Verknüpfungen erlauben"
- Neu: Neues Rollen Recht im Infoeditor "Erweiterte Empfängereinstellungen erlauben"
- Geändert: Abstände im Infoeditor für Schaltflächen, Live-Vorschau, zurücksetzen, abbrechen + Tooltips hinzugefügt
- Geändert: Infoeditor - Benutzerdesktop + Winlogondesktop -> "Vorschau" in "Vorschau-Info" umbennant.

------------------

Changelog 6.1.3.4 (22.04.2020)

- Verbessert: Info als Live-Vorschau zeigt nur bei enthaltenen ScriptVars ein "Popup" Fenster zur Eingabe. Ansonsten ist immer eine Live-Vorschau möglich, sofern ein Text für Alle Sprachen hinterlegt ist.
- Neu: Im Infoeditor können im Reiter "Empfänger" als Optionen eine ODER-Verknüpfung zwischen Filter, Gruppen, Ausschlussfilter, Ausschlussgruppen, Gruppierungen und Ausschlussgruppierungen erstellt werden
- Neu: Im Infoeditor können im Reiter "Empfänger" bei Erweitere Empfängereinstellungen verschiedene UND / ODER  zwischen Filter, Gruppen, Ausschlussfilter, Ausschlussgruppen, Gruppierungen und Ausschlussgruppierungen erstellt werden
- Neu: Alarmstandort Manager und Wächter können nun als PDF ausgegeben werden.
- Neu: Im Filter vom Typ Logon kann nun auch für die Anmeldung in der best_web (Weboberfläche) das best_script für die Script Funktionen (load_from_file/1, member_of_filegroup/1, member_of_filegroup/2) verwendet werden.

------------------

Changelog 6.1.3.3 (03.04.2020)

- Fixed: Datensätze eines Benutzers umziehen 
    * Verbesserte Fehlermeldungen
    * Falsche ID beim Migrieren im Standardprofil behoben

------------------

Changelog 6.1.3.2 (01.04.2020)

- Geändert: System -> System (global) - Info als Live-Vorschau nur Auswahl von Filtern möglich, + Button zeigt zur Filter App
- Geändert: Die Live-Vorschau speichert beim Versand kein Empfangen/Gesendet in die Datenbank bi_client_info
- Fixed: Infoeditor -> Vorschau mit ScriptVars erlaubt erst dann eine Live-Vorschau wenn die ScriptVar gesetzt wurde
- Geändert: Der HTML Editor unter Umfragen > Benachrichtigungen ist jetzt höher.

- Neu: System(lokal) -> Datensätze umziehen
    * Domäne & Benutzer (Alt): Der Benutzer dessen Daten umgezogen werden sollen
    * Benutzer (Neu): Der Loginname des neuen Benutzers. (oder admin für Administrator)
    * Domäne (Neu): Die neue Domäne der Datensätze. Wenn leer selbe wie alte. Wird ignoriert falls Ziel-Benutzer admin ist.
    * Profilname: Den Namen des Profils in den die Datensätze übertragen werden sollen. Wenn leer wird das Standardprofil genutzt. Wird ignoriert falls Ziel-Benutzer admin ist.

------------------

Changelog 6.1.3.1 (30.03.2020)

- Fixed: Info als Live-Preview als ADMIN geht nicht mehr an Alle
- Fixed: Info als Live-Preview als Benutzer / Domäne geht nun an die zugewiesene Domäne
- Anpassungen und Änderungen an der Live-Preview (kein Beginn / Ende / offenes Ende / Periodisch / UTC möglich)
- Fixed: Dynamisches Laden im Infoeditor der Ausschlussfilter / -Gruppen / - Gruppierungen
- Fixed: Cluster Status Zähler

------------------

Changelog 6.1.3.0 (27.03.2020)

- Neu: Infos können nun als Live-Preview direkt an den eigenen Client gesendet werden
    * hierzu gibt es im Infoeditor unten rechts eine neue Schaltfläche mit "Live-Vorschau"
    * in den Rollen gibt es ein neues Recht unterhalb von Infos  - "Erlaubt eine Live-Vorschau (an den Infoclient) an den eigenen Benutzer zur Kontrolle der Nachricht"
    * als ADMIN gibt es eine Einstellung unter System -> System (global) "Info als Live-Preview (ADMIN)", dort kann für den ADMIN ein Filter gesetzt werden an dem die Live-Preview gesendet wird.
    * als Benutzer / Domäne wird die Live-Preview an den eigenen verbunden Client aus der Kombination des angemeldeten Benutzername und Domäne aus der Weboberfläche verwendet
    * unter System -> System (global) kann die Aktivzeit und Anzeigedauer bei "Live-Preview (Minuten)" im Bereich von 1 bis 1440 Minuten eingestellt werden.

- Neu: Cluster Status kann unter System -> System (global) über die Option "Cluster Status - Anzeige des Cluster-Status im Dashboard der Weboberfläche" aktiviert / deaktiviert werden.
- Fixed: Cluster Status und der Verbindungszähler
- Neu: Erlang OTP 22.3
- Geändert: Anzeige einer Fehlermeldung bei einer falsch hochgeladenen Datei in Autoupdate -> Autoupdate Archiv

------------------

Changelog 6.1.2.9 (.0.2020)

NACHTRAGEN

------------------

Changelog 6.1.2.8 (.2020)

NACHTRAGEN

------------------

Changelog 6.1.2.7 (17.02.2020)

- Neu: Verbessertes Zusammenspiel der Alarm App mit Rollen
- Neu: Alarm Serverboard Einstellung "computer_to_upper" true / false, um die optische Darstellung von Computernamen anzupassen
- Geändert: Alarm App Listenimport zeigt nun die wirkliche Anzahl an neuen Datensätzen an

------------------

Changelog 6.1.2.6 (24.01.2020)

- Neuerungen in der Umfrage App:
    * Neu: Es können nun mehrere Umfragen sowie initiierte Umfragen auf einmal gelöscht werden.
    * Neu: Beendete Umfragen werden in der Übersicht nun klar hervorgehoben.
    * Neu: Vorschau Button für einzelne Fragen.
    * Neu: Umfrageergebnisse können nun für einzelne Benutzer zurückgesetzt werden.
    * Neu: Es können zu Umfragen „Ansichtsgruppen“ hinzugefügt werden, um einen Benutzerkreis via Filter lesenden Zugriff auf eine Umfrage zu gestatten.
    * Änderung: Einige Punkte wurden zur Vereinfachung des Interfaces ausgeblendet.
    * Änderung: Die Breite der Antwortfelder ist nun pro Frage definierbar, nicht mehr pro Textfeld. Ebenfalls ist sie nicht mehr von der Fragetextlänge abhängig.
    * Änderung: Admin sieht nun alle Umfragen und kann diese bearbeiten.
    * Optimierung: Generelle Verbesserung der UX durch verschiedene Interface Optimierungen.
    * Behoben: Diverse Anzeige- und Rechtschreibfehler korrigiert.
    * Behoben: Ein seltener Fehler beim Kopieren von Umfragen wurde behoben.
    * Behoben: HTML-Code im Umfragetitel wird nun dargestellt.
    * Behoben: Umfragetext wird nun auch gespeichert, wenn man sich zum Zeitpunkt des Speicherns im HTML-Editor Modus befindet.
    * Behoben: Die Listenpunkte werden im Umfragetext nicht immer Linksbündig angezeigt, sondern folgen dem Text.

------------------

Changelog 6.1.2.5 (23.01.2020)

- DEVELOP ONLY

------------------

Changelog 6.1.2.4 (23.01.2020)

- DEVELOP ONLY

------------------

Changelog 6.1.2.3 (20.01.2020)

- Bugfixes im ASM

------------------

Changelog 6.1.2.0 (16.01.2020)

- Neu: Mehrfache Standard ASM Favoriten und Gruppen können nun entfernt werden
- Neu: ASM Standortabfrage kann nun optional nur nach IP-Wechsel angezeigt werden

------------------

Changelog 6.1.1.9 (13.01.2020)

- Neu (internal): hackney_v1.15.2.1 
- Fixed: Cluster Status im Dashboard
- Neu: Beim Löschen von ASM Alarmen werden nun Anpassungen ebenfalls entfernt
- Geändert: Einige Texte und kleinere Workflow Aspekte in der ASM App

------------------

Changelog 6.1.1.8 (09.01.2020)

- Client Konfiguration Hilfe Hyperlink angepasst
- Neu: Additional Colors im Infoeditor / StatusInfos
Zeigt die Standardfarben oder eigene definierte Farben an. Die einzelnen Werte lassen sich über das Serverboard einstellen.

Sektion: general
Schlüssel: additionalcolorsonly
Wert: false/true (boolean, default: false)

Sektion: general
Schlüssel: additionalcolors
Wert: Liste als Beispiel unten:

[{<<"#ACD819">>, <<"All clear">>},{<<"#009EE0">>, <<"Info">>},{<<"#FFC000">>, <<"Warning">>},{<<"#FF0000">>, <<"Alert">>}]

Liste aus Hexadezimal, mit anzeigbaren Text in der Liste

------------------

Changelog 6.1.1.7 (19.12.2019)

- Neu: Über die ASM Alarmplan Funktion können sich nun separat alle mobilen Geräte ausgegeben werden
- Neu: Beim ASM Geräte Alarmplan werden nun mobile Geräte extra markiert


------------------

Changelog 6.1.1.6 (16.12.2019)

- Kompatibilität mit CouchDB Version 2.3.x

------------------

Changelog 6.1.1.5 (13.12.2019)

- Verbesserungen bezüglich der Verbindungsübersicht und Anzeige

------------------

Changelog 6.1.1.4 (12.12.2019)

- Neu: Upgrade auf Erlang OTP 22.2

------------------

Changelog 6.1.1.3 (10.12.2019)

- Neu: Bereinigung alter Räume in Alarm App Alarmierungskreisen
- Neu: Kleinere Verbesserungen an der Alarm App Oberfläche

------------------

Changelog 6.1.1.2 (06.12.2019)

- Fixed: Rollen und die Verwendung von Filtern, Empfängerfilter beim Versand von Infos

------------------

Changelog 6.1.1.1 (05.12.2019)

- Neu: In der Infohistorie wird jetzt die Caption als Spalte aufgelistet
- Neu: Tooltips in der Infohistorie für die Spalte: Info, Caption

------------------

Changelog 6.1.1.0 (28.11.2019)

- Performance Optimierungen bei der Nutzung von Filtern

------------------

Changelog 6.1.0.9 (27.11.2019)

- Fixed - Info in die Historie verschieben (manuell)
- Neu: Demandwebsite vom ASM zeigt nun initial alle Standorte an, wenn keine Favoriten vorhanden sind
- Neu: Mehrere ASM Demand Favoriten können nun auf einmal entfernt werden
- Neu: BSMs und Alarmkreise werden nun beim Löschen von ASM Einheiten ebenfalls entfernt
- Neu: Kleinere optische und technische Verbesserungen in der ASM App
- Behoben: Zeitstempel nach ASM Demand Änderungen

------------------

Changelog 6.1.0.8 (27.11.2019)

- Fixed - Info in die Historie verschieben um 24 Uhr

------------------

Changelog 6.1.0.7 (26.11.2019)

- Optimierungen bei der Nutzung der Rollen Ressourcen / Filter und co.

------------------

Changelog 6.1.0.6 (06.11.2019)

- Fixed: Aus der Historie gelöschte Infos wurden immernoch in der Infoübersicht in anderen offenen Tabs aufgelistet.
- Fixed: Ausblenden der Rechte für Offline Infos, Bricht alle laufenden Infos ab
- Fixed: StatusInfo Contentlink einfügen Icon
- Fixed: Verschiedene Icon´s wurden angepasst
- Neu: Bei nicht vererbten Infofeldern über die Rolle/n wird im Infoeditor der Tab "Infofelder" automatisch ausgeblendet.

------------------

Changelog 6.1.0.5

- Fixed: Empfangsübersicht und Verbindungsübersicht mit den Rollen Empfängerfiltern

------------------

Changelog 6.1.0.4

- Neu: Empfängerfilter können nun in den Rollen gesetzt werden
- Neu: Anzeige von weiteren Details in der Infoübersicht (aufklappbar / einklappbar)

------------------

Changelog 6.1.0.3 (.10.2019)

- Neu: Erlang 22.1.1
- Neu: Sencha 7.0.0 als JavaScript Framework
- Fixed: Lademaske für das Speichern des Routings einer Umfrage
- Fixed: Bug "Leere Info" wird nach abbrechen einer Info oder über "In die Historie verschieben" erstellt


------------------

NEW Major Version .....

------------------

Changelog 6.0.186 (.09.2019)


------------------

Changelog 6.0.185 (25.09.2019)

- Geändert: Suche nach Benutzern (z. b. user_100) in den LDAP-Gruppen im Infoeditor, werden als "[user_100] Gruppenname" aufgelistet.

------------------

Changelog 6.0.184 (24.09.2019)

- Fixed: Anmeldung an einer Domäne, wenn zusätzliche Domänen ausgewählt wurden
- Neu: System - Serverboard [general] info_preview_time = true (default: false) zeigt die Zeiteinstellung bei der Vorschau einer Info
- Geändert: Die Auswahl von LDAP-Gruppen ist jetzt mit einer Mehrfachauswahl möglich


------------------

Changelog 6.0.182 (17.09.2019)

- Performance Verbesserungen bei der Nutzung von Filter-Logiken

------------------

Changelog 6.0.181 (11.09.2019)

- Fixed: Client Konfiguration / als personalisierte Infoclient.ini versenden

------------------

Changelog 6.0.180 (10.09.2019)

- Version only, ähnlich wie 6.0.174

------------------

Changelog 6.0.174 (02.09.2019)

- Die Höhe und Breite eines Popups kann nun in % angegeben werden
- Eine Info mit der Option „Bricht alle laufenden Infos ab" kann nun als Silent Info versendet werden (somit unsichtbar)
- Neuer Infoclient.ini Eintrag: PlayMasterInfoAllowed=True/False (Default=False)
- PlayMasterInfoAllowed legt fest, ob der Benutzer eine erstelle Info mit der Option "Option „Bricht alle laufenden Infos ab“  über das Infogitter erneut starten kann oder nicht.
- Eine Info kann nun für eine bestimmte Zeit X in Minuten als nicht schließbar markiert werden. Nach Ablauf dieser Zeit kann die Info wieder vom Benutzer geschlossen werden.
- StatusInfos können nun für eine bestimmte Zeit X in Sekunden als nicht schließbar markiert werden. Nach Ablauf dieser Zeit kann die Info wieder vom Benutzer geschlossen werden.

------------------

Changelog 6.0.173 (26.07.2019)

- Template Beschreibung lässt sich in der Template App editieren
- Fixed: Ein http-request für Infos in die Historie verschieben oder wenn Infos abgebrochen werden

------------------

Changelog 6.0.172 (01.07.2019)
- Hilfe Willkommensfenster geändert

------------------

Changelog 6.0.171 (12.04.2019)

- Neu: Alarm Standortmanager App Version 3.0 mit folgenden Features:
* Drastische Erhöhung der Versandgeschwindigkeit von Alarmen in großen Umgebungen
* Bereitstellung von Alarmierung für einzelne Benutzer (Terminalserver)
* Filter App mit Manager, Wächter und der Mobile Gruppe verwendbar
* Filterung des Alarm Planes nach Alarmeinheiten
* Anpassung des gesamten Alarm Standortmanager Templatetextes
* Deaktivierbarer Audit: [asm] audit=false

------------------

Changelog 6.0.170 (29.03.2019)

- Neue Optionen in der Domänen App für "zusätzliche Filter" bei sehr großen LDAP-Strukturen:
* {active_n,"once"}. % once,true,N > 0
* {min_bin_vheap_size,"10240"}. % number > 233, only on large system
* {min_heap_size,"10240"}. %% number > 4555, only on large system in best_domain

------------------

Changelog 6.0.169 (22.03.2019)

- Optimierungen in der Domänen App für das Laden von OU´s

------------------

Changelog 6.0.168 (14.03.2019)

- Neu: Testlizenz bis 30.06.2019
- In der App für das Testen von Filtern wurde ein Hinweis eingebaut: "Es können ausschließlich Filter getestet werden, welche Objekte einer Domäne filtern, z. B.: die das Attribut domain. im Filter enthalten! Die Domänen App muss hierzu in der Lizenz enthalten sein."

------------------

Changelog 6.0.167 (12.03.2019)

- Neue Optionen für das Laden von rekursiven Gruppen in der Domänen App
- In der Client-Konfiguration App können nun personalisierte Infoclient.ini Einträge versendet werden
- Fixed: Anmeldegruppen bei Umfragen

------------------

Changelog 6.0.166 (11.02.2019)

- Starter App für Lizenz korrigiert
- Laden der Weboberfläche bei geänderten Lizenz-Demand Einstellungen
- Neu: Die MailToInfo-Schnittstelle unterstützt jetzt im Mailbody das JSON-Format

------------------

Changelog 6.0.165 (19.12.2018)

- Testlizenz bis 31.03.2019
- Neu: Gruppierung der Navigation wird beibehalten, falls "Navigation reduzieren" bei Alarm App Erstkonfiguration gewählt wird
- Fix: Ladeproblem des Alarm Plans beim Verwenden des Mandantenkonzepts
- Fix: LDAP Import von verbotenen Zeichen in die Alarm App
- Fix: Anzeigenamen ScriptVar Problem bei bestimmten Einträgen in der Alarm App
- Geändert: "Raum" Modus in Alarm App wurde zu "Alarmierungskreise"
- Geändert: Ein paar Fehler- / Infomeldungen in der Alarm App wurden konkretisiert

------------------

Changelog 6.0.163 (07.11.2018)

- Neu: Alarm AD Import ändert nur noch selbst erstellte Ressourcen und Zuordnungen
- Geändert: In der Alarm App wird kein "undefined" Raum mehr für Computer ohne Zuordnung erstellt

------------------

Changelog 6.0.162 (07.11.2018) - special ASM Beta Version

- Neu: Hinweis, dass kein Alarm ohne entsprechende Lizenz versendet werden kann
- Neu: Gruppierung für die Manager Ansicht im ASM
- Neu: ASM Manager Filter werden nun entfernt, falls diese von keinem Manager mehr benötigt werden

------------------

Changelog 6.0.161 (23.10.2018) - special ASM Beta Version

- Fixed: Demand Webseite für Alarm Standortmanager
- Verschiedene Anpassungen und Bugfixes in der Alarm Standortmanager App
- Geändert: Systemgenerierte Filter sind nicht mehr kopierbar
- Geändert: In der Gruppen App werden nun systemgenerierte Einträge entsprechend markiert und als nicht editierbar behandelt

------------------

Changelog 6.0.160 (16.10.2018)

- Neu: Response-Ansicht in der Empfangsübersicht ist nun sortier- & filterbar
- Neu: System(global): Einstellung für das Verhalten von LDAP Gruppen (neue Info): Nur Benutzer adressieren, nur Computer adressieren, Benutzer oder Computer adressieren
- Neu: Warnung beim Versand von Infos in Kombination von QuickUser und Ausschlussfilter
- Geändert: Ausgabe der LDAP-Gruppen für M2I-Schnittstelle in lowercase
- (INTERNAL) - Demo Registrierung implementiert, so dass man sich mit einer E-Mail Adresse registrieren kann

------------------

Changelog 6.0.159 (16.10.2018)
 - Development version only

------------------

Changelog 6.0.158 (16.10.2018)
 - Development version only

------------------

Changelog 6.0.157 (12.10.2018)
 - Development version only

------------------

Changelog 6.0.156 (28.09.2018)

- Neu: Token Lebensdauer (Minuten) in System(global) für externe Clients einstellbar
- Neu: Anzeige aller vollständigen LDAP Attribute beim Filter testen
- Weitere Optionen für die Migration von V5 nach V6 in den Gruppen implementiert
- System Bereinigung verbessert

------------------

Changelog 6.0.155 (17.09.2018)

- Verbesserte IE 11 Kompatibilität

------------------

Changelog 6.0.154 (11.09.2018)

- Geändert: Gruppenmanager zeigt Benutzer, Computer die OU´s

------------------

Changelog 6.0.153 (11.09.2018)

- Geändert: Einschränkung in der Contentverwaltung für die Ordner-Ansicht anhand der berechtigten Rollen, Ressourcen Mitbenutzung

------------------

Changelog 6.0.152 (10.09.2018)

- Option in der infoserver.ini wurde entfernt [alarm] ldap_delete_everything_before_import
- Neu: Domäne "Protokollierung - LDAP Protokollierung aktivieren" -> schreibt in best_web/log/error.log

------------------

Changelog 6.0.151  - VERSION ONLY

------------------

Changelog 6.0.150 (06.09.2018)

- Neu: Benutzerdefiniertes Menü - Gruppierung kann aktiviert werden (Standardwert: false)
- Neu: Alarm-Typ "Info an Alarm-Auslöser" - Sendet eine Info an den Auslöser des Alarms (Alarmfunktionstest)
- Change: Recht für das Öffnen der Alarm App wird automatisch vergeben, falls andere Alarm-Berechtigung vorhanden
- Fix: Nur "Computer verwalten" Recht für die Alarm App funktioniert nun wieder

------------------

Changelog 6.0.149 (04.09.2018)

- Testlizenz bis 31.12.2018

------------------

Changelog 6.0.148 (29.08.2018)

- Weitere Verbesserungen für das Auslesen der Domäne / LDAP
- Der Gruppenmanager zeigt nun für Benutzer & Computer die zugewiesenen Gruppen und OU´s.
- Der Gruppenmanager zeigt beim Aufklappen einer Gruppe die enthaltenen Mitglieder (Benutzer, Computer)
- Neu: Die Alarm Ampel besitzt nun einen dritten Status für die Anzeige von keinen Empfängern- Neu: Die Alarm Ampel besitzt nun einen dritten Status für die Anzeige von keinen Empfängern

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