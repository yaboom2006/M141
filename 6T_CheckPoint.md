![](../x_res/tbz_logo.png)

# M141 - DB-Systeme in Betrieb nehmen


# ![](../x_res/CP.png) Checkpoint 6.Tag


## Server konfigurieren 

1.  Auf welche Arten können Konfigurationsparameter definiert werden?

    - [ ] mit einem INSERT-Befehl

    - [ ] durch Eintrag auf der Kommandozeile

    - [ ] durch Eintrag in einer Konfigurationsdatei

    - [ ] durch Eintrag in einem Logfile

3.  Welcher Konfigurationsparameter legt fest, wo die Log-Dateien abgelegt werden?

    - [ ] basedir

    - [ ] datadir

    - [ ] log-bin

    - [ ] logdir

4.  Mit welchem Eintrag beginnen die Server-Parameter in der Konfigurationsdatei?

    - [ ] [mysql]

    - [ ] [WinMySQLadmin]

    - [ ] [mysqldump]

    - [ ] [mysqld]

5.  Wozu kann der DB-Client mysqlshow verwendet werden?

    - [ ] Backup erstellen

    - [ ] DB-Schema anzeigen

    - [ ] Verbindung zum DB-Server testen

    - [ ] Inhalt einer Protokolldatei anschauen

6.  Mit welchem Log-File bestimmen Sie den letzten Start des MySQL-Servers?

    - [ ] Error Log

    - [ ] Update Log

    - [ ] Query Log

	 - [ ] Transaction Log
	 
1.  Welcher Eintrag im Konfigurationsfile schaltet die Protokollierung aller User-Login ein?

    - [ ] log-bin

    - [ ] log-slow-queries

    - [ ] log

    - [ ] log-error=C:/log/err.log

2.  Wie restaurieren Sie nach einem Server-Ausfall eine DB vollständig?

    - [ ] Einlesen des letzten Backup

    - [ ] Verwenden der Option --opt beim Erstellen des Backup

    - [ ] Einlesen des Query-Log

    - [ ] Einlesen aller Update-Logs in der richtigen Reihenfolge (mit Hilfe von mysqlbinlog)


3.  Wie erreichen Sie, dass Änderungen in der Konfigurationsdatei wirksam werden?

    ___   
      

4.  Durch welche Daten wird der von einer DB benötigte Speicherplatz bestimmt?

    ___   
      

5.  Wozu wird das Logging (Protokollierung) verwendet?

    ___   
      

6.  In welcher Log-Datei finden Sie, den Anwender, der bestimmte Daten löschte?

    ___   
      

7.  Welche Informationen finden Sie im Slow Query Log?

    ___   
      

8.  Geben Sie für jede Protokolldatei an, wie Sie deren Inhalt kontrollieren.

    ___   
      

9.  Wie beeinflusst der Parameter --opt beim Erstellen eines Backup das Tabellenlocking?

    ___   
      

10. Beschreiben Sie das Vorgehen, um Daten von MySQL nach ORACLE zu migrieren.

    ___   
      

11. Beschreiben Sie eine praktische Anwendung für den READ-Lock.

    ___   
    
    
---



# Optimierung

1.  Welche Möglichkeiten können die Geschwindigkeit eines DB-Server verbessern?

    - [ ] Indexe möglichst vermeiden

    - [ ] Serverparameter einstellen

    - [ ] Transaktionen verwenden

    - [ ] Locks verwenden

2.  Wie werden Daten schneller in eine DB-Tabelle geladen?

    - [ ] durch Komprimieren der Daten vor der Übertragung

    - [ ] durch Verwenden des Parameters --opt beim Erstellen des Backup-Skripts

    - [ ] durch Importieren der Daten aus einer Textdatei

    - [ ] durch Verwenden von vielen INSERT-Befehlen

3.  Was trifft auf den Befehl OPTIMIZE TABLE zu?

    - [ ] entfernt nicht genutzten Speicherplatz aus MyISAM-Tabellendateien

    - [ ] ist auf MyISAM- und InnoDB-Tabellen anwendbar

    - [ ] wird angewendet bei Tabellen, die häufig abgefragt werden

    - [ ] defragmentiert DB-Dateien

4.  Wie finden Sie langsame DB-Abfragen?

    - [ ] mit EXPLAIN SELECT

    - [ ] im Query Log

    - [ ] im Slow Query Log

    - [ ] im Error Log

5.  Welche Aussagen betreffend DB-Optimierung sind korrekt?

    - [ ] Abfragen, die LIKE enthalten, können immer optimiert werden

    - [ ] Indexe beschleunigen Abfragen

    - [ ] Indexe werden allgemein auf Schlüsselattribute gelegt

    - [ ] durch Indexe werden DB-Einträge und -änderungen schneller
    
1.  Wann verwenden Sie den Befehl EXPLAIN?

    - [ ] um Daten schneller in die DB zu laden

    - [ ] immer im Zusammenhang mit SELECT

    - [ ] um langsame Abfragen zu finden

    - [ ] um zu erkennen, wie sich ein Index auf die Geschwindigkeit einer Abfrage auswirkt

1.  Welches sind Gründe für die Verwendung eines Index?

    - [ ] um das Eintragen von Daten in Tabellen bei Unique-Attributen zu beschleunigen

    - [ ] um DB-Abfragen zu beschleunigen

    - [ ] um das Ändern von Daten zu verlangsamen

    - [ ] um einmalige Werte zu gewährleisten
    
1.  Nennen Sie Ziele der DB-Optimierung?

    ___   
      

2.  Was wird optimiert, um die Geschwindigkeit eines DB-Servers zu verbessern?

    ___   
      

3.  Mit welchen 2 prinzipiellen Massnahmen werden DB-Abfragen beschleunigt?

    ___   
      

4.  Beschreiben Sie kurz, wie Sie den Befehl EXPLAIN verwenden.

    ___   
      

5.  Wozu wird der Befehl OPTIMIZE TABLE angewendet?

    ___   
      

6.  Wie werden SELECT-Befehle optimiert?

    ___   
      

7.  Wie viele DB-Tabellen können standardmässig gleichzeitig geöffnet sein?

    ___   
      

8.  Wie schalten Sie den Query Cache ein bzw. aus?

    ___   
      
