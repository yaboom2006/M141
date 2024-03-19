![](../x_res/tbz_logo.png)

# M141 - DB-Systeme in Betrieb nehmen


# ![](../x_res/CP.png) Checkpoint 5.Tag


# DB-Server im LAN

1.  Welcher Befehl testet die Verbindung zum Server-Rechner mit Adresse 139.79.124.97?

    - [ ] mysql -h 139.79.124.97

    - [ ] ipconfig

    - [ ] ping 139.79.124.97

    - [x] mysqladmin -h 139.79.124.97 -u root -p ping

2.  Wozu wird der Parameter -h bei MySQL verwendet?

    - [ ] bewirkt die Abfrage des Passworts

    - [ ] bewirkt die Verbindung als bestimmter Benutzer

    - [ ] Angabe der Adresse des Client-Rechners

    - [x] Angabe der Adresse des Server-Rechners

3.  Was bewirkt der Befehl 'mysqldump -h 139.79.124.97 hotel \> datei.txt'?

    - [ ] Backup der DB hotel in die Datei datei.txt auf Adresse 139.79.124.97

    - [x] Backup der angegebenen DB auf dem Server mit der IP-Adresse 139.79.124.97

    - [ ] Restore der Datenbank hotel auf dem Server mit der Adresse 139.79.124.97

    - [ ] Ausführen des SQL-Skripts datei.txt auf Adresse 139.79.124.97 auf die DB hotel

4.  Welche Aufgabe hat der ODBC-Driver?

    - [ ] passt die SQL-Befehle dem entsprechenden DB-Server an

    - [ ] ermöglicht das Erstellen und Konfigurieren von ODBC-Datenquellen (DSN)

    - [x] ermöglicht den einheitlichen Zugriff einer Applikation auf verschiedene Datenbanken

    - [ ] ermöglicht den Zugriff einer Applikation auf eine bestimmte DB

5.  Wie greifen Sie vom Konsolenfenster auf einen DB-Server mit Adresse 139.79.124.97 zu?

    - [ ] mysqladmin -h 139.79.124.97

    - [ ] mysql -h 139.79.124.97 hotel \< hotel.bkp

    - [x] mysql -h 139.79.124.97 -u root -p

    - [ ] ping 139.79.124.97

1.  Welche Aufgaben hat der DB-Server im Gegensatz zum DB-Client?

    Verwaltet die Datenbank sowie auch die Benutzer und Rechte.   
      

2.  Weshalb benutzt man MS Access z.B. zusammen mit einem MySQL-Server?

    Schöne grafische Oberfläche, benutzerfreundlich.   
      

3.  Wie bestimmen Sie die IP-Adresse des Server-Rechners?

    Mit einem IP Scanner.   
      

4.  Wie prüfen Sie, ob der DB-Server auf Adresse 139.79.124.97 läuft?
    ```mysql
    mysqladmin -h  139.79.124.97 ping
    ```

5.  Welcher Befehl führt das SQL-Skript xy.sql auf die DB hotel auf Adresse 139.79.124.97 aus?
    ```mysql
    mysql -h 139.79.124.97 -u [Benutzername] -p hotel < xy.sql
    ```
      

6.  Wozu wird ODBC verwendet?

    Um einen allgemeinen Zugriff auf Applikaitionen für Benutzer zu gewährleisten.   
      

7.  Was wird benötigt, um von Access mit ODBC z.B. auf einen DB2-Server zuzugreifen?

    Man muss den ODBC-Treiber zuerst auf dem Ziel Server installieren.   
      

8.  Was wird in der Java-Welt anstelle von ODBC verwendet?

    JDBC   
      

9.  Was sind eingebundene Access-Tabellen?

    Bei eingebundenen Access-Tabellen sind die eigentliche Tabellen extern bei Microsoft. Die Tabellen verweisen aber auf die Daten welche bei dir gespeichert sind. 
      
