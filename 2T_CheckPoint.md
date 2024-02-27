![](../x_res/tbz_logo.png)

# M141 - DB-Systeme in Betrieb nehmen


# ![](../x_res/CP.png) Checkpoint 2.Tag



## DB-Server und XAMPP

Bei den folgenden Fragen treffen eine oder mehrere Antworten zu.

1.  Wie kann der MySQL-Server gestartet werden?

    - [ ] Start von `mysql.exe` im CMD-Fenster

    - [ ] Start von `mysqld.exe` im CMD-Fenster

    - [ ] über MySQL-Workbench

    - [ ] Eingabe von localhost als URL im Browser

    - [ ] `NET START mysql` (im CMD-Fenster)

    - [ ] mit dem Dienstmanager von Windows

2.  Welche Informationen erhalten Sie, wenn Sie im Konsolenfenster den Befehl *status* eingeben?

    - [ ] Version des Konsolenprogramms

    - [ ] Betriebszeit des Servers

    - [ ] Version des Servers

    - [ ] Betriebszeit des Monitors

3.  Welche Daten befinden sich im Verzeichnis datadir (z. B. C:…\\mysql\\data)?

    - [ ] Protokoll-Dateien (Log-Files)

    - [ ] Fehlerprotokolle

    - [ ] die ausführbaren MySQL-Programme, z.B. mysql.exe

    - [ ] Datenbanken

4.  Wie prüfen Sie, ob der MySQL-Server läuft?

    - [ ] mit dem Dienst-Manager von Windows

    - [ ] mit dem GUI-Tool Administrator

    - [ ] durch Eingabe des Befehls `status` im CMD-Fenster

    - [ ] mit dem Task-Manager von Windows (Prozess)

1.  Wie testen Sie die Installation des DB-Servers?

    ---

1.  Wie überprüfen Sie die Laufzeit des DB-Servers?

    ---

1.  Wozu verwenden Sie das Programm mysql.exe? Wie starten Sie es?

    ---

2.  Notieren Sie 3 Informationen des status-Befehls mit ihrer Bedeutung.

    ---

3.  Nennen Sie 2 wichtige Verzeichnisse der MySQL-Installation mit ihrem Inhalt.

    ---
    
4.  Was ist der Inhalt der `my.ini` – Datei?

    ---
    



## Codierung und Kollation

1.  Welche Aussagen treffen zum Thema Codierung zu?

    - [ ] Ein Datenbankserver erkennt die Codierung einer Datei automatisch

    - [ ] Codierung ist eine Vereinbarung zwischen dem Nutzer und dem System.

    - [ ] Die Codierung legt fest, welche binäre Bitkombination zu welchem Zeichen gehört.

    - [ ] ANSI- und ASCII-Codierung ist dasselbe

    - [ ] Der Unicode-Zeichensatz hat 32 Bit Codelänge

    - [ ] `UTF` bedeutet Unicode Transformation Format

    - [ ] `UTF-8 ` hat nur 8 Bit lange Zeichen aus dem Unicode-Zeichensat

2.  Welche Aussagen treffen zum Thema Byte Order Mark zu?

    - [ ] Ein BOM kann in Dateien jeglicher Art gesetzt werden.

    - [ ] Wenn das UTF-8-BOM "ï»¿" bei einem Text-Editor sichtbar ist, erkennt er *es* nicht!

    - [ ] Bei UTF-8 nutzt ein BOM nichts, da es nur 8 Bits zur Codierung verwendet!

    - [ ] UTF-8 und UTF-16 verwenden unterschiedliche BOMs.!

3.  Welche Aussagen treffen zum Thema Kollation zu?

    - [ ] ist die Standard-Einstellung bei MySQL.

    - [ ] In der DIN-Normierung zur deutschen Kollation werden zwei Varianten zur Umlauthandhabung angeboten.

    - [ ] Die Endung "_ci" gibt an, dass die Sortierung die Gross-/Kleinschreibweise unterscheidet.

    - [ ] Seit MySQL 5.5.3 sollte [utf8mb4](https://dev.mysql.com/doc/refman/5.5/en/charset-unicode-utf8mb4.html) anstelle von utf8 verwendet werden.

    - [ ] In der Konfig-Datei (my.ini) kann die UFT8-Codierung als Standard angegeben werden.

    - [ ] Eine Kollationseinstellung gilt für die ganze Tabelle (Entität).
    
    - [ ] "Binärsortierung" ist die Sortierung anhand des binären Codes der verglichenen Zeichen.



## Daten importieren

1.  Mit welchem Befehl kontrollieren Sie die Struktur einer Tabelle?

    - [ ] SHOW DATABASES;

    - [ ] SHOW CREATE TABLE *tabellenname*;

    - [ ] DESC *tabellenname*; 
    
    - [ ] DESCRIBE *tabellenname*;

    - [ ] SELECT * FROM *tabellenname*;

    - [ ] SHOW TABLE *tabellenname*;