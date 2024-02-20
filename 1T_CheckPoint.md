![](../x_res/tbz_logo.png)

# M141 - DB-Systeme in Betrieb nehmen


# ![](../x_res/CP.png) Checkpoint


# Einführung, DB-Engines, XAMPP, Workbench

Bei den folgenden Fragen treffen eine oder mehrere Antworten zu.

1.  Welches ist die heute am **häufigsten** verwendete Datenbank-Art?

    - [ ] Hierarchische Datenbank

    - [x] Relationale Datenbank

    - [ ] Objektorientierte Datenbank

    - [ ] Netzwerkförmige Datenbank

2.  Welche **Komponenten** sind in einem DB-Server enthalten?

    - [x] 1 oder mehrere Datenbanken

    - [x] 1 oder mehrere Datenbank-Anwendungen

    - [x] Datenbank-Management-System (DBMS)

    - [ ] Formulare, Reports und Abfragen

3.  Bei welchen der folgenden **Fabrikate** handelt es sich um eine relationale Datenbank?

    - [x] Oracle

    - [ ] Couch-DB

    - [x] MySQL

    - [x] MariaDB

    - [ ] Mongo-DB

    - [x] MS Access

    - [x] PostgrSQL °

4.  Welches sind Beispiele für **Aufgaben** eines DB-Clients?

    - [ ] speichert die eigentlichen Daten

    - [x] stellt dem Benutzer ein User-Interface für den Datenzugriff zur Verfügung

    - [ ] verwaltet Benutzer und Passworte und gewährleistet damit die Sicherheit der Datenbank

    - [x] leitet die Befehle des Benutzers an den DB-Server weiter

5.  Welches sind **Client-Komponenten** von MySQL?

    - [x] mysqld

    - [ ] my.ini

    - [x] mysql

    - [ ] phpMyAdmin
    
6.  Wie heisst die **Server-Komponente** von MySQL?

    - [ ] phpMyAdmin

    - [ ] Workbench °

    - [ ] mysql

    - [x] mysqld

7.  Beschreiben Sie den Begriff Client/Server-Modell.

    Das Client/Server-Modell ist eine Art von Anwendungsstruktur, bei der Aufgaben und Arbeit zwischen den Servern, die die Dienste bereitstellen, und den Clients, die diese Dienste nutzen, aufgeteilt werden.
      
8.  Welche Vorteile hat die Client/Server-Architektur gegenüber einer Desktop-DB?

    Die Vorteile sind bessere Anpassungsfähigkeit für wachsende Anforderungen, zentrale Kontrolle und Verwaltung sowie erhöhte Sicherheit.
      
9.  Wie werden die Daten in einer relationalen Datenbank abgespeichert?

    In relationalen Datenbanken werden Daten in Tabellen gespeichert. Diese Tabellen bestehen aus Zeilen und Spalten. Jede Zeile steht für einen Datensatz, und jede Spalte repräsentiert ein Merkmal oder Attribut dieses Datensatzes.  
      
10.  Was sind die Vorteile, wenn ein DB-Server die **referentielle Datenintegrität** unterstützt?

    Wenn ein DB-Server die referentielle Datenintegrität unterstützt, bringt dies Vorteile wie die Sicherstellung von konsistenten und genauen Daten sowie die Vermeidung von Datenanomalien.

11.  Welches sind die 4 Gruppen von **NoSQL**-Datenbanken, die zurzeit relevant sind?

    Dokumentenorientierte Datenbanken, Schlüssel-Wert-Datenbanken, Spaltenorientierte Datenbanken und Graphdatenbanken.
    
12.  Was bedeutet **DBaaS**? Erklären Sie anhand eines Beispiels. °

    DBaaS steht für "Database as a Service" und ist ein cloudbasierter Service, bei dem Nutzer auf eine Datenbank zugreifen können, ohne sich um die physische Infrastruktur oder die Verwaltung der Datenbank kümmern zu müssen. Amazon RDS ist ein Beispiel für einen solchen Dienst.
    
13.  Was sind die Vorteile eines RDBMS gegenüber anderen DB-Modellen? °

    Ein RDBMS hat gegenüber anderen Datenbankmodellen Vorteile, darunter die Unterstützung von ACID-Transaktionen, die Verwendung von SQL als standardisierte Abfragesprache und die Fähigkeit, komplexe Beziehungen zwischen Daten zu modellieren.
    
14.  DB-Server starten und stoppen

    Stoppen und starten Sie Ihren DB-Server auf die verschiedenen Arten. Kontrollieren Sie jeweils das Resultat mit dem Task-Manager:

	-   Über das XAMPP – Control-Panel
	-   Via Konsole (CMD / WPS)
	-   Über die MySQL-Workbench (nur wenn der als Service läuft) 
	
15. DB-Server prüfen

    Kontrollieren Sie, ob der MySQL-Server läuft mit dem

	-   Task-Manager von Windows: dort sollte ein Prozess mysqld.exe laufen.
	-   Dienst-Manager von Windows: der Dienst MySql sollte den Status Gestartet haben.
	-   Mit den drei Klienten mysql, Workbench und phpMyAdmin

