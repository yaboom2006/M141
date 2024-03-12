![](../x_res/tbz_logo.png)

# M141 - DB-Systeme in Betrieb nehmen


# ![](../x_res/CP.png) Checkpoint 4.Tag


# Datenbank-Sicherheit

1.  Was bedeutet der Begriff Authentifizierung im Zusammenhang mit einem DB-Server?

    - [ ] Prüfung der Privilegien des Benutzers

    - [ ] Antwort auf die Frage Wer?

    - [ ] Identitätsprüfung

    - [ ] Antwort auf die Frage Was?

2.  Wann werden Änderungen im Zugriffssystem von MySQL wirksam?

    - [ ] sofort nach Eingabe der Änderung

    - [ ] nach dem Befehl FLUSH PRIVILEGES

    - [ ] nach dem Neustart des DB-Servers

    - [ ] nach dem Befehl GRANT

3.  Was bewirkt der SQL-Befehl GRANT ... ON ... TO ...;

    - [ ] Privileg(ien) erteilen

    - [ ] Privileg(ien) wegnehmen

    - [ ] User erstellen, falls noch nicht vorhanden

    - [ ] User löschen

4.  Mit welchem Befehl werden Privilegien kontrolliert?

    - [ ] REVOKE ... ON ... FROM ;

    - [ ] SELECT user, host, password FROM user ;

    - [ ] SHOW TABLES;

    - [ ] SHOW GRANTS FOR ... ;

5.  Welches sind die beiden wichtigsten DCL-Befehle (data control)?

    - [ ] SELECT

    - [ ] REVOKE

    - [ ] DELETE

    - [ ] GRANT
    
1.  Was ist nötig, dass Benutzer "meier" keinen Zugang mehr auf den DB-Server hat.

    - [ ] in Systemtabelle user für diesen Benutzer jedes Privileg auf "N" setzen

    - [ ] mit DELETE FROM user WHERE user = 'meier'; und FLUSH PRIVILEGES;

    - [ ] in allen Systemtabellen für diesen Benutzer jedes Privileg auf "N" setzen

    - [ ] dem Benutzer das GRANT-Privileg (Grant_priv) wegnehmen

1.  Erklären Sie den Begriff "Autorisierung" im Zusammenhang mit einem DB-Server.

    __   
      

2.  Wann wird das Schlüsselwort IDENTIFIED BY verwendet?

    __   
      

3.  Ergänzen Sie den Befehl REVOKE ... ON ... FROM ... ; mit eigenen Angaben.

    __   
      
4.  Beschreiben Sie den Begriff der MySQL-Testdatenbank.

    __   
      

5.  Mit welchem Befehl ändern Sie das Passwort von Benutzer Meier auf "abc123"?

    __   
      

6.  Geben Sie eine Erklärung für folgende Fehlermeldung.  
    
    ```  
    GRANT USAGE ON \*.\* TO abc IDENTIFIED BY 'a12';  
    ERROR 1045: Access denied for user: '@127.0.0.1'
    ```
    
    __   
      

7.  Korrigieren Sie den folgenden Befehl:  
    
    ```  
    REVOKE ALL FROM ''@localhost;  
    ERROR 1064: You have an error
    ```
    
    __

