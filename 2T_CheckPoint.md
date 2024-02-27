![](../x_res/tbz_logo.png)

# M141 - DB-Systeme in Betrieb nehmen


# ![](../x_res/CP.png) Checkpoint 2.Tag



## DB-Server und XAMPP

Bei den folgenden Fragen treffen eine oder mehrere Antworten zu.

1.  Wie kann der MySQL-Server gestartet werden?

    - [x] Start von `mysql.exe` im CMD-Fenster

    - [ ] Start von `mysqld.exe` im CMD-Fenster

    - [x] über MySQL-Workbench

    - [x] Eingabe von localhost als URL im Browser

    - [ ] `NET START mysql` (im CMD-Fenster)

    - [ ] mit dem Dienstmanager von Windows

2.  Welche Informationen erhalten Sie, wenn Sie im Konsolenfenster den Befehl *status* eingeben?

    - [ ] Version des Konsolenprogramms

    - [x] Betriebszeit des Servers

    - [x] Version des Servers

    - [ ] Betriebszeit des Monitors

3.  Welche Daten befinden sich im Verzeichnis datadir (z. B. C:…\\mysql\\data)?

    - [x] Protokoll-Dateien (Log-Files)

    - [x] Fehlerprotokolle

    - [ ] die ausführbaren MySQL-Programme, z.B. mysql.exe

    - [x] Datenbanken

4.  Wie prüfen Sie, ob der MySQL-Server läuft?

    - [ ] mit dem Dienst-Manager von Windows

    - [ ] mit dem GUI-Tool Administrator

    - [ ] durch Eingabe des Befehls `status` im CMD-Fenster

    - [x] mit dem Task-Manager von Windows (Prozess)

1.  Wie testen Sie die Installation des DB-Servers?

    Wenn ich drauf komme geht es. Man kann noch überprüfen wenn man drinn ist mit "SHOW status;"

1.  Wie überprüfen Sie die Laufzeit des DB-Servers?

    status

1.  Wozu verwenden Sie das Programm mysql.exe? Wie starten Sie es?

    Um auf den SQL Server zuzugreifen. Ich starte es mit XAMPP.

2.  Notieren Sie 3 Informationen des status-Befehls mit ihrer Bedeutung.

    Current User: Angemeldeter Benutzer
    Server: Die Server Art also MariaDB
    Uptime: Laufzeit des Servers

3.  Nennen Sie 2 wichtige Verzeichnisse der MySQL-Installation mit ihrem Inhalt.

    data hat die Logs und die Datenbanken und bin ist die installation.
    
4.  Was ist der Inhalt der `my.ini` – Datei?

    default-character-set=utf8mb4
    [mysqld]
    port=3306
    socket="C:/xampp2/mysql/mysql.sock"
    basedir="C:/xampp2/mysql"
    tmpdir="C:/xampp2/tmp"
    datadir="C:/xampp2/mysql/data"
    pid_file="mysql.pid"
    # enable-named-pipe
    key_buffer=16M
    max_allowed_packet=1M
    sort_buffer_size=512K
    net_buffer_length=8K
    read_buffer_size=256K
    read_rnd_buffer_size=512K
    myisam_sort_buffer_size=8M
    log_error="mysql_error.log"
    
    character-set-server=utf8mb4
    collation-server=utf8mb4_general_ci
    [mysqldump]
    max_allowed_packet=16M

    [isamchk]
    key_buffer=20M
    sort_buffer_size=20M
    read_buffer=2M
    write_buffer=2M

    [myisamchk]
    key_buffer=20M
    sort_buffer_size=20M
    read_buffer=2M
    write_buffer=2M

    [mysqlhotcopy]

## Codierung und Kollation

1.  Welche Aussagen treffen zum Thema Codierung zu?

    - [] Ein Datenbankserver erkennt die Codierung einer Datei automatisch

    - [x] Codierung ist eine Vereinbarung zwischen dem Nutzer und dem System.

    - [x] Die Codierung legt fest, welche binäre Bitkombination zu welchem Zeichen gehört.

    - [ ] ANSI- und ASCII-Codierung ist dasselbe

    - [ ] Der Unicode-Zeichensatz hat 32 Bit Codelänge

    - [x] `UTF` bedeutet Unicode Transformation Format

    - [ ] `UTF-8 ` hat nur 8 Bit lange Zeichen aus dem Unicode-Zeichensat

2.  Welche Aussagen treffen zum Thema Byte Order Mark zu?

    - [x] Ein BOM kann in Dateien jeglicher Art gesetzt werden.

    - [x] Wenn das UTF-8-BOM "ï»¿" bei einem Text-Editor sichtbar ist, erkennt er *es* nicht!

    - [ ] Bei UTF-8 nutzt ein BOM nichts, da es nur 8 Bits zur Codierung verwendet!

    - [x] UTF-8 und UTF-16 verwenden unterschiedliche BOMs.!

3.  Welche Aussagen treffen zum Thema Kollation zu?

    - [ ] ist die Standard-Einstellung bei MySQL.

    - [x] In der DIN-Normierung zur deutschen Kollation werden zwei Varianten zur Umlauthandhabung angeboten.

    - [ ] Die Endung "_ci" gibt an, dass die Sortierung die Gross-/Kleinschreibweise unterscheidet.

    - [x] Seit MySQL 5.5.3 sollte [utf8mb4](https://dev.mysql.com/doc/refman/5.5/en/charset-unicode-utf8mb4.html) anstelle von utf8 verwendet werden.

    - [x] In der Konfig-Datei (my.ini) kann die UFT8-Codierung als Standard angegeben werden.

    - [x] Eine Kollationseinstellung gilt für die ganze Tabelle (Entität).
    
    - [x] "Binärsortierung" ist die Sortierung anhand des binären Codes der verglichenen Zeichen.



## Daten importieren

1.  Mit welchem Befehl kontrollieren Sie die Struktur einer Tabelle?

    - [ ] SHOW DATABASES;

    - [ ] SHOW CREATE TABLE *tabellenname*;

    - [x] DESC *tabellenname*; 
    
    - [x] DESCRIBE *tabellenname*;

    - [ ] SELECT * FROM *tabellenname*;

    - [ ] SHOW TABLE *tabellenname*;