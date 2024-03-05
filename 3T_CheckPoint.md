![](../x_res/tbz_logo.png)

# M141 - DB-Systeme in Betrieb nehmen


# ![](../x_res/CP.png) Checkpoint 3.Tag


## Tabellentypen und Transaktionen
1.  Wie bezeichnet man die Ausführung mehrerer DB-Operationen in einem einzigen Schritt?

    - [x] Referentielle Integrität

    - [ ] Replikation

    - [ ] Transaktion

    - [ ] Storage Procedure

2.  Warum sollen Locks möglichst schnell freigegeben werden?

    - [ ] damit das DBMS nicht zu stark belastet wird

    - [x] damit andere DB-Anwender nicht lange warten müssen

    - [ ] damit niemand die Daten ändern kann

    - [x] damit möglichst viele Benutzer gleichzeitig auf die DB zugreifen können

3.  Welches ist das Standard-Tabellenformat von MySQL (MariaDB)?

    - [ ] InnoDB

    - [x] MyISAM

    - [ ] ARIA

    - [ ] ISAM

4.  Wann verwenden Sie das InnoDB-Tabellenformat?

    - [ ] wenn möglichst schnell auf die Daten zugegriffen werden muss

    - [x] wenn auf gar keinen Fall ein Datenverlust vorkommen darf

    - [x] wenn viele Benutzer gleichzeitig Daten ändern

    - [ ] wenn bei sehr vielen Daten nicht beliebig viel Speicherplatz vorhanden ist

5.  Was trifft auf den sog. Tablespace zu?

    - [ ] Datei, welche die Daten der entsprechenden Tabelle enthält (\*.MYD)

    - [ ] Datei, welche Beschreibung, Daten und Indexe einer Tabelle enthält

    - [x] Datei, welche alle InnoDB-Tabellen enthält (virtueller Speicher)

    - [x] wird nach Erreichen von x MB automatisch vergrössert (falls autoextend eingeschaltet)
    
6.  Mit welchen Befehlen werden Transaktionen gesteuert?

    - [ ] UNLOCK TABLES;

    - [ ] COMMIT; oder ROLLBACK;

    - [ ] ALTER TABLE ... TYPE= ...;

    - [x] BEGIN; oder START TRANSACTION;

7.  Was trifft auf das Locking bei Transaktionen auf InnoDB-Tabellen zu?

    - [ ] in Transaktionen kommt Table locking zur Anwendung

    - [x] es wird Row locking angewendet

    - [ ] es werden alle Datensätze der entsprechenden Tabelle(n) gesperrt

    - [ ] es werden nur die gerade bearbeiteten Datensätze gesperrt

8.  Welches sind Vorteile der InnoDB-Tabellen gegenüber MyISAM-Tabellen?

    InnoDB hat eine Transaktionunterstützung. Das Row-Level-Locking ist auch ein Vorteil da nur die gerade verwendeten Daten gesperrt werden und nicht der ganze Table. Ausserdem wird die Tabelle bei einem Crash, egal von was, automatisch mit ROLLBACK zurückgesetzt damit keine Daten verlohren gehen.
      
9.  In welchen Dateien wird die MyISAM-Tabelle KUNDEN gespeichert?

    In .FRM Dateien.
      
10.  Notieren Sie den SQL-Befehl, der die InnoDB-Tabelle BESTELLUNGEN erstellt.

    ```mysql
    CREATE TABLE bestellungen (id_k INT AUTO_INCREMENT, Name VARCHAR(30), Saldo DECIMAL(110,2), PRIMARY KEY (id_k)) ENGINE = InnoDB;   
    ```  
    Das ist nur ein Beispiel.

11.  Welche Locking-Art ist a) bei MyISAM-Tabellen b) bei InnoDB-Tabellen möglich?

    Bei MyISAM ist nur Table Locking möglich und bei InnoDB Row-Level-Locking   
      
12.  Beschreiben Sie den Begriff Datenbank-Transaktion!

    Eine Abfolge von mehreren Befehlen, welche zusammen einen Sinn ergeben.   
      
13.  Beschreiben Sie die Bedeutung von I in der Abkürzung ACID.

    Das I steht für Isolation, und bezeichnet das Locken der tabellen.   
      
14.  Wie stellen Transaktionen bei einem DB-Server-Crash die Datenkonsistenz sicher? (Schwierig)

    Mit einem automatischen ROLLBACK basierend auf den Logs.   
  
15. Mit welcher Locking-Art wartet ein SELECT-Befehl, bis alle Transaktionen auf die angeforderte Tabelle entsperrt sind? 

    Gar nicht, SELECT Anfragen werden trotzdem durgelassen.
   
16. Wie muss Autocommit gesetzt werden, damit jeder SQL-Befehl zu einer Transaktion gehört und damit explizit mit COMMIT abgeschlossen werden muss, damit er ausgeführt wird? 

    Der Autocommit Modus muss auf 0 gesetzt werden damit alles als einzelne Transaktion gilt. Das geht so:

    ```mysql
    SET AUTOCOMMIT=0;
    ```   
          