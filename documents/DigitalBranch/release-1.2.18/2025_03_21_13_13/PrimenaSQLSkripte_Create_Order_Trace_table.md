# Primena sql skripte Create Trace table

Izraz CREATE TABLE se koristi za kreiranje nove tabele u bazi podataka.

Sintaksa

`CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
   ....
);`

Parametri kolone određuju imena kolona tabele.

**Datatype** parametar specificira tip podataka koje kolona može da sadrži (npr. varchar, integer, date, itd).

**Savet**: Za pregled dostupnih tipova podataka, idite na našu kompletnu referencu tipova podataka.

SQL KREIRAJ TABELU Primer

Sledeći primer stvara tabelu pod nazivom "Persons" koja sadrži pet kolona: PersonID, LastName, LastName, Address i City:

Primer

`CREATE TABLE Persons (
    PersonID int,
    LastName varchar(255),
    LastName varchar(255),
    Address varchar(255),
    City varchar(255)
);`