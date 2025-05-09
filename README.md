# SQL kurs
En oversikt over kommandoene du trenger for å gjøre oppgavene til SQL kurset

## Lage og bruke en database
For å lage en database bruk koden under og erstatt *databasenavn* med navnet du vil gi til databasen.
```
CREATE DATABASE databasenavn;
```
For å bruke en database bruk koden under og erstatt *databasenavn* med navnet til databasen.
```
USE DATABASE databasenavn;
```

## Lage et table
for å lage et table bruk koden under og erstatt *tablenavn* med navnet du vil gi tablet, erstatt *kolonne1*, *kolonne2*, osv. med navnene du vil gi til kolonenene og erstatt *datatype* med datatypene du vil gi til kolonnen.
```
CREATE TABLE tablenavn (kolonne1 datatype, kolonne2 datatype, …);
```

## Datatyper
Det finnes mange datatyper i SQL her finner du en oversikt over de vanligeste.
- INT - heltall
- VARCHAR() - En tekst streng, put antall bokstaver du tilater inn i paranteset
- DATE - Dato, gitt ved året-måneden-datoen
- BOOLEAN/TINYINT(1) - true & false, 1 & 0

Les om flere datatyper [her](https://mariadb.com/kb/en/data-types/)

Du kan bruke kommadoen under for å se datatypene til kolonnene i et table.
```
DESCRIBE tablenavn;
```

## Putte inn data i et table
Bruk kommandoen under for å sett inn data i tablet ditt. Erstatt *tablenavn* med navnet navnet på tablet, erstatt kolonne1, kolonne2, osv. med de kolonnene du vil putte data inn i, erstatt verdi1 med den verdien du vil putte i kolonne1 erstatt verdi2 med den verdien du vil putte i kolonne2 osv.
```
INSERT INTO tablenavn (kolonne1, kolonne2, ...) VALUES(verdi1, verdi2, ...);
```
**HUSK!** å putte hermetegn (") rundt hver enkelt verdi

## Hente ut data fra et table
Bruk kommandoen under for å hente ut data fra et table. Erstatt *tablenavn* med navnet til tablet, erstatt *kolonne* med den kolonnen du vil ha dataen til. Hvis du vil ha dataen fra **flere** kolonner så kan du erstatte *kolonne* med *kolonne1, kolonne2, ...*. Hvis du vil har dataen i **alle** kolonnene så kan du erstatte *kolonne* med *.

```
SELECT kolonne FROM tablenavn;
```

## Slette et table
Bruk kommandoen under for å slette et table og erstatt *tablenavn* med navnet på tablet du vil slette.
```
DROP TABLE tablenavn;
```

## Andre ting
**HUSK!** å legge til et semikolon (;) på slutten av hver kommando.

### PRIMARY KEY
Primary key kan brukes for å referere til en rad i et table og kan også brukes for å skape referanser på tvers av tabler i en database. Legg til PRIMARY KEY når du deklarerer datatypen til en kolonne for å gjøre kolonnen til en primary key. Du kan også gjøre om kolonnen til en primary key med [ALTER TABLE](https://www.geeksforgeeks.org/alter-table-in-mariadb/)

### NOT NULL
NOT NULL kan brukes for å hindre at en kolonne ikke får noen verdi når man putter inn en ny rad i et table. Hvis brukeren har glemt å putte inn en verdi for en kolonne definert som NOT NULL så vil man få en feilmelding. Legg til NOT NULL når du deklarerer datatypen til en kolonne eller legg til NOT NULL med ALTER TABLE.

### AUTO_INCREMENT
AUTO_INCREMENT fyller automatisk ut en kolonne uten at en bruker trenger å skrive det inn når de putter inn en ny rad. På denne måten kan du få en index til radene i tablet. AUTO_INCREMENT må brukes sammen med KEY, men ikke nødvendigvis PRIMARY KEY. Legg til AUTO_INCREMENT når du deklarerer datatypen til en kolonne eller legg til AUTO_INCREMENT med ALTER TABLE.


