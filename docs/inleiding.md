# Inleiding

## Wat is een database?

Een database is een gestructureerde verzameling van gegevens die centraal wordt opgeslagen, beheerd en opgevraagd. In plaats van informatie verspreid over verschillende bestanden, Excel-sheets of papieren formulieren te bewaren, zet je die gegevens in een database. Zo kun je ze snel en betrouwbaar opzoeken, aanpassen en analyseren.

Bij een database worden gegevens meestal georganiseerd in tabellen. Elke tabel bestaat uit rijen en kolommen:

- Een rij is een record: één compleet gegevenselement, bijvoorbeeld één klant of één bestelling.
- Een kolom is een veld: een eigenschap zoals naam, e-mailadres of datum.
- Een primaire sleutel is een uniek identificatienummer of veld dat elke rij in een tabel onderscheidt.
- Een relatie beschrijft hoe verschillende tabellen aan elkaar gekoppeld zijn.

Een eenvoudig voorbeeld:

- Tabel: klanten
  - klant_id
  - naam
  - email
- Tabel: bestellingen
  - bestel_id
  - klant_id
  - datum
  - totaal

Hiermee kun je bijvoorbeeld zien welke klant een bepaalde bestelling heeft geplaatst. Dat is precies waar databases goed in zijn: verbanden tussen gegevens vastleggen en op een gecontroleerde manier beheren.

## Waarom gebruiken we databases?

Databases worden gebruikt omdat ze veel voordelen bieden boven het handmatig bewaren van gegevens in losse documenten of spreadsheets.

### Belangrijkste voordelen

- Snel zoeken en ophalen van gegevens
- Eenvoudig opslaan van grote hoeveelheden informatie
- Controle op consistentie en volledigheid van gegevens
- Meerdere gebruikers kunnen tegelijk toegang krijgen tot dezelfde gegevens
- Betere beveiliging en toegangscontrole
- Back-up en herstel van gegevens bij storingen
- Reproduceerbare en gecontroleerde manipulatie van data via queries

Stel je voor dat een winkel honderden klanten, producten en bestellingen heeft. Zonder database zou je al die informatie handmatig moeten bijhouden, met veel kans op fouten, duplicaten en onoverzichtelijkheid. Een database maakt dit veel efficiënter en betrouwbaarder.

Databases zijn dus niet alleen voor grote bedrijven. Ze worden ook gebruikt in scholen, ziekenhuizen, webshops, mobiele apps, boekhoudsystemen en veel andere toepassingen.

## Soorten databases

Er bestaan verschillende soorten databases, afhankelijk van het soort gegevens en het doel waarvoor ze gebruikt worden.

### 1. Relationele databases

Dit is het meest gebruikte type database in bedrijfstoepassingen. De gegevens worden opgeslagen in tabellen met duidelijke verbanden tussen elkaar.

Kenmerken:

- Structuur in tabellen en relaties
- Gebruikt SQL (Structured Query Language)
- Sterk geschikt voor gestructureerde gegevens
- Voorbeelden: MySQL, PostgreSQL, SQL Server, Oracle

Voorbeeld: een klantenbestand, voorraadbeheer of een boekhoudsysteem.

### 2. NoSQL-databases

NoSQL-databases zijn ontworpen voor grote hoeveelheden data en minder strikt gestructureerde informatie. Ze worden vaak gebruikt bij webservices, realtime apps en grote datameren.

Kenmerken:

- Flexibelere opslag van gegevens
- Niet noodzakelijk in tabellen zoals bij relationele databases
- Vaak gebruikt voor documenten, sleutel-waardeparen of grafieken
- Voorbeelden: MongoDB, Redis, Cassandra

### 3. Andere soorten databases

Er zijn ook databases die speciaal zijn gemaakt voor specifieke doelen, zoals:

- Objectgeoriënteerde databases
- Grafdatabases voor netwerken en relaties
- Tijdreeksdatabases voor metingen en logs
- In-memory databases voor zeer snelle verwerking

## Wat gaan we in deze cursus leren?

In deze cursus focussen we ons vooral op relationele databases en SQL. Je leert onder andere:

- hoe databases zijn opgebouwd;
- hoe je tabellen en relaties modelleert;
- hoe je gegevens opvraagt met SQL;
- hoe je data toevoegt, wijzigt en verwijdert;
- hoe je transacties, indexen en normalisatie begrijpt.

Databases vormen de basis van veel moderne softwareapplicaties. Als je begrijpt hoe gegevens worden opgeslagen en opgehaald, kun je beter werken met applicaties, rapportages, analyses en softwareontwikkeling in het algemeen.

> In deze cursus gaan we vooral dieper in op relationele databases, omdat deze het meest gebruikt worden in bedrijfssystemen en softwareontwikkeling.

## Leerdoel

Aan het einde van dit hoofdstuk kun je:

- uitleggen wat een database is;
- benoemen waarom databases belangrijk zijn;
- onderscheid maken tussen verschillende soorten databases;
- een eenvoudig voorbeeld van tabellen en relaties herkennen.

## Kernbegrippen

- Database: een georganiseerde verzameling van gegevens
- Tabel: een verzameling records met dezelfde structuur
- Rij: één record of één item
- Kolom: één eigenschap van een record
- Relatie: een verband tussen tabellen

## Belangrijk om te onthouden

- Gegevens moeten logisch opgeslagen worden.
- Herhaling van data kost ruimte en kan fouten veroorzaken.
- Relaties maken een database veel krachtiger dan losse bestanden.

## Oefenopdrachten

1. Noem drie redenen waarom een bedrijf een database gebruikt in plaats van gegevens in Excel of losse bestanden op te slaan.
2. Leg in je eigen woorden uit wat het verschil is tussen een tabel, een rij en een kolom. Geef daarbij een concreet voorbeeld met klanten en bestellingen.
