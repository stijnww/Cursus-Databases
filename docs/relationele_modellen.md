# Relationele modellen

## Tabellen, rijen en kolommen

Een relationeel model is een manier om data te organiseren in tabellen. Elke tabel vertegenwoordigt een bepaald soort informatie, zoals klanten, producten of bestellingen.

Een tabel bestaat uit:

- kolommen: de eigenschappen van de gegevens;
- rijen: de individuele records;
- een duidelijke naam en structuur.

Voorbeeld:

```sql
CREATE TABLE klanten (
    klant_id INT,
    naam VARCHAR(100),
    email VARCHAR(100)
);
```

Hierbij is:

- `klant_id` een kolom;
- een specifieke klant een rij;
- `naam` en `email` eigenschappen van die klant.

Het grote voordeel van relationele modellen is dat gegevens logisch georganiseerd worden, waardoor ze beter te beheren, op te vragen en te koppelen zijn.

## Primaire sleutels

Een primaire sleutel is een kolom of combinatie van kolommen die elke rij in een tabel uniek maakt. Hiermee kun je elke record precies identificeren.

Voorbeeld:

```sql
CREATE TABLE klanten (
    klant_id INT PRIMARY KEY,
    naam VARCHAR(100),
    email VARCHAR(100)
);
```

Hier is `klant_id` de primaire sleutel. Geen twee klanten kunnen dezelfde `klant_id` hebben.

Waarom is dit belangrijk?

- Je kunt één record uniek terugvinden.
- Je voorkomt dubbele gegevens.
- Je kunt andere tabellen verwijzen naar dezelfde rij.

## Vreemde sleutels

Een vreemde sleutel is een kolom in een tabel die verwijst naar de primaire sleutel van een andere tabel. Hiermee leg je relaties tussen tabellen vast.

Voorbeeld:

```sql
CREATE TABLE bestellingen (
    bestel_id INT PRIMARY KEY,
    klant_id INT,
    totaal DECIMAL(10,2),
    FOREIGN KEY (klant_id) REFERENCES klanten(klant_id)
);
```

Hier verwijst `klant_id` in `bestellingen` naar `klant_id` in `klanten`. Dat betekent dat elke bestelling gekoppeld is aan een bestaande klant.

Vreemde sleutels helpen om:

- gegevensintegriteit te waarborgen;
- relaties tussen tabellen te modelleren;
- consistente en betrouwbare databases te bouwen.

> Een relationeel model werkt dus vooral door tabellen te koppelen aan elkaar via primaire en vreemde sleutels.

## In één oogopslag

Een relationeel model bestaat uit:

- tabellen;
- kolommen;
- rijen;
- primaire sleutels;
- vreemde sleutels;
- relaties tussen tabellen.

### Voorbeeld

| klanten |  |  |  | bestellingen |
|---|---|---|---|---|
| klant_id | naam | email |  | bestel_id | klant_id | totaal |
| 1 | Anna | anna@x.nl |  | 101 | 1 | 55.00 |
| 2 | Bob | bob@x.nl |  | 102 | 2 | 20.00 |

De kolom `klant_id` in `bestellingen` verwijst naar `klant_id` in `klanten`.

## Belangrijk om te onthouden

- Een primaire sleutel maakt een rij uniek.
- Een vreemde sleutel koppelt tabellen aan elkaar.
- Relaties houden de data consistent.

## Oefenopdrachten

1. Maak een eenvoudig relationeel model voor een bibliotheek met de tabellen `leden` en `uitleningen`. Bepaal welke kolommen en welke primaire sleutel je nodig hebt.
2. Leg uit waarom een `FOREIGN KEY` nodig is in een tabel als `uitleningen` verwijst naar `leden`. Wat gebeurt er als een lid wordt verwijderd?
