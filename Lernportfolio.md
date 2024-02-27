# Lernportfolio M141

## Tag 1

![](Architekturen.png)

Desktop Datenbanken sind Datenbanken welche auf einem einzelnen PC laufen kann, und dafür da ist um kleinere Mengen an daten zu sichern.

Der DB-Client sind Clients die von den Diensten des Servers profitieren und die auch nutzen. Kurz gesagt griefen diese Geräte auf die Datenbank zu. Darum auch die Verbindung.
Der DB-Server ist die eigene Datenbank mit den Dateisystemen und den Daten.

Beim Tier-3 Modell ist es fast das gleiche wie beim Client/Server Modell, nur dass das Aufrufen der Datenbank und das Bearbeiten nicht auf der gleichen Schicht sind. Aufgerufen wird es per CLient und bearbeitet per Anwendungs-Server. Der DB Server ist wieder die Datenbank.


So kommt man per cmd auf die Datenbank:
cd C:/
cd xampp2
cd mysql
cd bin
.\mysql -u root -p


Hier die Vor- und Nachteile und Typische Anwendungsfällen.

![](Überblick-Datenbank.png)


## Tag 2

![](Verbose-mysqld.png)

![](Verbose-mysql.png)


So legt man die Kollation in SQL fest (Beispiel): <br>

```mysql
CREATE TABLE Personen (
    Nachname VARCHAR(100) CHARACTER SET utf8mb4 COLLATE utf8mb4_german2_ci
);
```

Um die Reihen zu sortieren kann man auf die Kollationen in der obersten Reihe klicken um die Spalten zu sortieren.

![](Sortierung.png)


Um Nachnamen einzufügen kann man folgendes Script benützen: <br>

```mysql
INSERT INTO Personen (Nachname) VALUES ('Müller'), ('Mueller'), ('Muller'), ('Straus'), ('Strauss'), ('Strauß'), ('Über'), ('Ueber'), ('Uber');
```

Um die Kollation in Workbench zu ändern kann man Alter Table benutzen: <br>

```mysql
ALTER TABLE Personen MODIFY Nachname VARCHAR(100) CHARACTER SET utf8mb4 COLLATE utf8mb4_german2_ci;
```

Im phpMyqdmin kann man auf dem Dashboard die Kollation auswählen: <br>

![](Kollation-myadmin.png)


| **Tätigkeit**                         | **SQL-Befehl**                                               | **Grp** | **![Achtung](../x_res/caution.png)** |
|---------------------------------------|--------------------------------------------------------------|---------|-------------------------------------|
| 1) alle Daten einer Tabelle anzeigen  | SELECT * FROM [Table Name]                                        | DML     | Der Befehl kann gefährlich werden wenn man mega viele Sachen hat in der Datenbank hat |
| 2) Datenbank auswählen                | USE [Database Name]                                               | DCL     | Ist nicht gefährlich |
| 3) eine neue Datenbank erstellen      | CREATE [Database Name]                                            | DDL     | Kann zu Verwechslungen führen wenn doppelte Einträge vorhanden sind |
| 4) eine neue Tabelle erstellen        | CREATE TABLE Personen (Nachname VARCHAR(100) CHARACTER SET utf8mb4 COLLATE utf8mb4_german2_ci) | DDL | Kann zu Verwechslungen führen wenn doppelte Einträge vorhanden sind |
| 5) eine Tabelle löschen               | DROP TABLE [Table Name]                                           | DDL     | Ist gefährlich, kann nicht rückgängig gemacht werden, ausser mit Rollback |
| 6) Tabellenstruktur **kontrollieren** | DESC [Tabellen Namen] | DDL | Nich gefährlich|
| 7) Datenbanken anzeigen               | SHOW DATABASES | DCL | Nicht gefährlich |
| 8) Tabellen einer DB anzeigen         | SHOW TABLES | DCL | Nichr gefährlich |
| 9) Daten in eine Tabelle eintragen    |INSERT INTO [Tabellen Namen] [Spalte1, Spalte2] VALUES [Wert1, Wert2] | DML | Kann sachen überschreiben |
| 10) Daten in einer Tabelle ändern     | UPDATE [Tabelle] SET [Spalte1] = '[neuer Wert]' WHERE ]Bedingung] | DML | Kann sachen überschreiben |
| 11) Daten in einer Tabelle löschen    | DELETE FROM [Tabellen Name] WHERE [Bedingung] | DML | Ist gefährlich, kann nicht rückgängig gemacht werden, ausser mit Rollback |
| 12) Spalte in einer Tabelle löschen   | ALTER TABLE [Tabellen Name] DROP COLUMN [Spalte] | DDL | Ist gefährlich, kann nicht rückgängig gemacht werden, ausser mit Rollback |


Um die Daten in die Tabelle einzufügen kann man phpmyadmin benutzen. Oben auf Import klicken und "CSV using LOAD DATA" auswählen:

![](Import.png)