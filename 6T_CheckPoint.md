![](../x_res/tbz_logo.png)

# M141 - DB-Systeme in Betrieb nehmen


# ![](../x_res/CP.png) Checkpoint 6.Tag


## Server konfigurieren 

1.  Auf welche Arten können Konfigurationsparameter definiert werden?

    - [ ] mit einem INSERT-Befehl

    - [x] durch Eintrag auf der Kommandozeile

    - [x] durch Eintrag in einer Konfigurationsdatei

    - [ ] durch Eintrag in einem Logfile

3.  Welcher Konfigurationsparameter legt fest, wo die Log-Dateien abgelegt werden?

    - [x] basedir

    - [ ] datadir

    - [ ] log-bin

    - [ ] logdir

4.  Mit welchem Eintrag beginnen die Server-Parameter in der Konfigurationsdatei?

    - [ ] [mysql]

    - [ ] [WinMySQLadmin]

    - [ ] [mysqldump]

    - [x] [mysqld]

5.  Wozu kann der DB-Client mysqlshow verwendet werden?

    - [ ] Backup erstellen

    - [x] DB-Schema anzeigen

    - [ ] Verbindung zum DB-Server testen

    - [ ] Inhalt einer Protokolldatei anschauen

6.  Mit welchem Log-File bestimmen Sie den letzten Start des MySQL-Servers?

    - [x] Error Log

    - [ ] Update Log

    - [ ] Query Log

	- [ ] Transaction Log
	 
1.  Welcher Eintrag im Konfigurationsfile schaltet die Protokollierung aller User-Login ein?

    - [ ] log-bin

    - [ ] log-slow-queries

    - [x] log

    - [ ] log-error=C:/log/err.log

2.  Wie restaurieren Sie nach einem Server-Ausfall eine DB vollständig?

    - [x] Einlesen des letzten Backup

    - [ ] Verwenden der Option --opt beim Erstellen des Backup

    - [ ] Einlesen des Query-Log

    - [ ] Einlesen aller Update-Logs in der richtigen Reihenfolge (mit Hilfe von mysqlbinlog)


3.  Wie erreichen Sie, dass Änderungen in der Konfigurationsdatei wirksam werden?

    Den Server neustarten   
      

4.  Durch welche Daten wird der von einer DB benötigte Speicherplatz bestimmt?

     Benutzerdaten (Tabellendaten), Speicherplatz für Indexe (Indextabellen), Systemverwaltung (DB- und Tabellenbeschreibungen, Systemkatalog, User- und Zugriffsverwaltung)
      

5.  Wozu wird das Logging (Protokollierung) verwendet?

    Zur Protokollierung von Start, Shutdown und Fehlern. Ausserdem wer welche Daten verändert hat und auch wann.Zur Datenwiederherstellung und Aufzeichnung von aufwendigen DB-Abfragen. Logging des Master-Rechners für die DB-Synchronisierung. Durchführen von Transaktionen nach einem DB-Absturz
      

6.  In welcher Log-Datei finden Sie, den Anwender, der bestimmte Daten löschte?

    Im Query Log   
      

7.  Welche Informationen finden Sie im Slow Query Log?

    Dort werden Abfragen gezeigt, welche einen grossen Aufwand verursacht haben.   
      

8.  Geben Sie für jede Protokolldatei an, wie Sie deren Inhalt kontrollieren.

    Mit mysqlbinlog kann man die Binären Logs anschauen, sonst im ensprechenden Pfad.   
      

9.  Wie beeinflusst der Parameter --opt beim Erstellen eines Backup das Tabellenlocking?

    Es erhöht die geschwindigkeit, da es Tables sperrt.
      

10. Beschreiben Sie das Vorgehen, um Daten von MySQL nach ORACLE zu migrieren.

    Man exportiert die Daten in ein CSV File und importiert dieses.   
      

11. Beschreiben Sie eine praktische Anwendung für den READ-Lock.

    Es wird verwendet, das wenn jemand eine Datei liest, diese nicht verändert wird.
    
    
---



# Optimierung

1.  Welche Möglichkeiten können die Geschwindigkeit eines DB-Server verbessern?

    - [ ] Indexe möglichst vermeiden

    - [x] Serverparameter einstellen

    - [x] Transaktionen verwenden

    - [x] Locks verwenden

2.  Wie werden Daten schneller in eine DB-Tabelle geladen?

    - [ ] durch Komprimieren der Daten vor der Übertragung

    - [ ] durch Verwenden des Parameters --opt beim Erstellen des Backup-Skripts

    - [x] durch Importieren der Daten aus einer Textdatei

    - [ ] durch Verwenden von vielen INSERT-Befehlen

3.  Was trifft auf den Befehl OPTIMIZE TABLE zu?

    - [x] entfernt nicht genutzten Speicherplatz aus MyISAM-Tabellendateien

    - [ ] ist auf MyISAM- und InnoDB-Tabellen anwendbar

    - [ ] wird angewendet bei Tabellen, die häufig abgefragt werden

    - [x] defragmentiert DB-Dateien

4.  Wie finden Sie langsame DB-Abfragen?

    - [ ] mit EXPLAIN SELECT

    - [ ] im Query Log

    - [x] im Slow Query Log

    - [ ] im Error Log

5.  Welche Aussagen betreffend DB-Optimierung sind korrekt?

    - [ ] Abfragen, die LIKE enthalten, können immer optimiert werden

    - [x] Indexe beschleunigen Abfragen

    - [x] Indexe werden allgemein auf Schlüsselattribute gelegt

    - [ ] durch Indexe werden DB-Einträge und -änderungen schneller
    
1.  Wann verwenden Sie den Befehl EXPLAIN?

    - [ ] um Daten schneller in die DB zu laden

    - [x] immer im Zusammenhang mit SELECT

    - [x] um langsame Abfragen zu finden

    - [x] um zu erkennen, wie sich ein Index auf die Geschwindigkeit einer Abfrage auswirkt

1.  Welches sind Gründe für die Verwendung eines Index?

    - [ ] um das Eintragen von Daten in Tabellen bei Unique-Attributen zu beschleunigen

    - [x] um DB-Abfragen zu beschleunigen

    - [ ] um das Ändern von Daten zu verlangsamen

    - [x] um einmalige Werte zu gewährleisten
    
1.  Nennen Sie Ziele der DB-Optimierung?

    Um die Gechwindigkeit und nutzung zu erhöhen.
      

2.  Was wird optimiert, um die Geschwindigkeit eines DB-Servers zu verbessern?

    Der Index. 
      

3.  Mit welchen 2 prinzipiellen Massnahmen werden DB-Abfragen beschleunigt?

    Mit dem Index und schreiben von effizienten SQL Abfragen.
      

4.  Beschreiben Sie kurz, wie Sie den Befehl EXPLAIN verwenden.

    Mit der SELeCT Abfrage, somit wird der Befehl erklärt.   
      

5.  Wozu wird der Befehl OPTIMIZE TABLE angewendet?

    Es optimiert die Tabellen indem es z.B. Fragmentierung entfernt.   
      

6.  Wie werden SELECT-Befehle optimiert?

    Anstatt von * kann man die genau angeben was man braucht. Man kann auch LIMIT benutzen um eine optimierung zu erzielen.   
      

7.  Wie viele DB-Tabellen können standardmässig gleichzeitig geöffnet sein?

    Standardmässig gibt es keine Grenze, die kann aber konfiguriert werden.   
      

8.  Wie schalten Sie den Query Cache ein bzw. aus?

    Entweder mit SET GLOBAL query_cache_size = (Zahl in MB), oder indem man in der Konfigurationdatei query_cache_type auf 1 stellt.   
      
