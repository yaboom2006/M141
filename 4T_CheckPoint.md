![](../x_res/tbz_logo.png)

# M141 - DB-Systeme in Betrieb nehmen


# ![](../x_res/CP.png) Checkpoint 4.Tag


# Datenbank-Sicherheit

1.  Was bedeutet der Begriff Authentifizierung im Zusammenhang mit einem DB-Server?

    - [ ] Prüfung der Privilegien des Benutzers

    - [x] Antwort auf die Frage Wer?

    - [x] Identitätsprüfung

    - [ ] Antwort auf die Frage Was?

2.  Wann werden Änderungen im Zugriffssystem von MySQL wirksam?

    - [ ] sofort nach Eingabe der Änderung

    - [x] nach dem Befehl FLUSH PRIVILEGES

    - [ ] nach dem Neustart des DB-Servers

    - [ ] nach dem Befehl GRANT

3.  Was bewirkt der SQL-Befehl GRANT ... ON ... TO ...;

    - [x] Privileg(ien) erteilen

    - [ ] Privileg(ien) wegnehmen

    - [ ] User erstellen, falls noch nicht vorhanden

    - [ ] User löschen

4.  Mit welchem Befehl werden Privilegien kontrolliert?

    - [ ] REVOKE ... ON ... FROM ;

    - [ ] SELECT user, host, password FROM user ;

    - [ ] SHOW TABLES;

    - [x] SHOW GRANTS FOR ... ;

5.  Welches sind die beiden wichtigsten DCL-Befehle (data control)?

    - [x] SELECT

    - [ ] REVOKE

    - [x] DELETE

    - [ ] GRANT
    
1.  Was ist nötig, dass Benutzer "meier" keinen Zugang mehr auf den DB-Server hat.

    - [x] in Systemtabelle user für diesen Benutzer jedes Privileg auf "N" setzen

    - [ ] mit DELETE FROM user WHERE user = 'meier'; und FLUSH PRIVILEGES;

    - [ ] in allen Systemtabellen für diesen Benutzer jedes Privileg auf "N" setzen

    - [ ] dem Benutzer das GRANT-Privileg (Grant_priv) wegnehmen

1.  Erklären Sie den Begriff "Autorisierung" im Zusammenhang mit einem DB-Server.

    Autorisierung ist wenn abgefragt wird was für Berechtigungen der Benutzer hat.  
      

2.  Wann wird das Schlüsselwort IDENTIFIED BY verwendet?

    Beim CREATE USER Command um dem Benutzer ein Passwort zuzuweisen.   
      

3.  Ergänzen Sie den Befehl REVOKE ... ON ... FROM ... ; mit eigenen Angaben.

    REVOKE privileg ON mysql.buchung FROM user@localhost;   
      
4.  Beschreiben Sie den Begriff der MySQL-Testdatenbank.

    Das ist die Datenbank von welcher sich mysql selbst verwaltet,   
      

5.  Mit welchem Befehl ändern Sie das Passwort von Benutzer Meier auf "abc123"?

    SET PASSWORD FOR meier@localhost = password('abc123')   
      

6.  Geben Sie eine Erklärung für folgende Fehlermeldung.  
    
    ```  
    GRANT USAGE ON \*.\* TO abc IDENTIFIED BY 'a12';  
    ERROR 1045: Access denied for user: '@127.0.0.1'
    ```
    
    Der Benutzer hat keine Berechtigung um auf den Server zuzugreifen.   
      

7.  Korrigieren Sie den folgenden Befehl:  
    
    ```  
    REVOKE ALL FROM ''@localhost;  
    ERROR 1064: You have an error
    ```
    
    REVOKE ALL PRIVILEGES ON *.* FROM ''@localhost;

