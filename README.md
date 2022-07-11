# dbtech_procedure

## 4. Übungsblatt: Anwendungslogik in PL/SQL

Laden Sie für das 4. Übungsblatt die Dateikschr-04-sp.zipherunter und impor-tieren Sie das darin befindliche Projekt. 
Die Testklasse für dieses Übungsblatt heißtCoolingServicePlSqlTest.


### Aufgabe 1: (10 Punkte)


In dieser Aufgabe sollen Sie denselben Service wie im 3. 
Übungsblatt implementieren,diesmal aber in PL/SQL. Dazu ist folgende Paketspezifikation vorgegeben, 
die sich inder Dateipkg.txtim Verzeichnis db befindet.


    create or replace package cooling_service as

        exc_data exception;
        
        pragma exception_init(exc_data, -20001);

        exc_cooling_system exception;

        pragma exception_init(exc_cooling_system, -20002);

    procedure transfer_sample(

        p_sample_id sample.sampleid%type,

        p_diameter_in_cm tray.diameterincm%type);

    end cooling_service;


Legen Sie dieses PL/SQL-Paket mit dem sqldeveloper in der Datenbank an.

Damit Ihr Code im Zusammenspiel mit den Java-Aufrufen funktioniert, müssen Sie anden richtigen Stellen folgende Ausnahme auslösen.

    raise exc_cooling_system;


Des Weiteren finden Sie in der Dateipkg-body.txtim Verzeichnisdbeine (leere) Pake-timplementierung, die folgendermaßen aussieht.


    create or replace package body cooling_service as

        procedure transfer_sample(

            p_sample_id sample.sampleid%type,
 
            p_diameter_in_cm tray.diameterincm%type

        ) as

        begin

            null;

        end transfer_sample;

    end cooling_service;


Legen Sie diese Paketimplementierung ebenfalls mit dem sqldeveloper in der Datenbank an.

Beachten Sie, dass Ihr Code nur in der gegebenen Paketimplementierung eingefügt wird.Das Eclipse-Projekt wird nur zum Testen Ihres PL/SQL-Codes verwendet. 
In dem Eclipse-Projekt selbst wird nicht implementiert.


### Zusatzaufgabe: (2 Bonuspunkte)

Präsentieren und erklären Sie Ihre erarbeitete Lösung in der nächsten Übung.


### Abgabe

Bitte geben Sie nur die Dateipkg-body.txtab, die den PL/SQL-Code enhält. 
VergessenSie nicht, die Namen Ihrer Gruppenmitglieder als Kommentar in die Datei einzutragen.
