# Transacties

## Wat is een transactie?

Een transactie is een reeks databasebewerkingen die als één geheel uitgevoerd worden. Als één onderdeel van de transactie mislukt, dan worden de andere wijzigingen vaak ook teruggedraaid.

Voorbeeld:

```sql
BEGIN;

UPDATE rekeningen SET saldo = saldo - 100 WHERE klant_id = 1;
UPDATE rekeningen SET saldo = saldo + 100 WHERE klant_id = 2;

COMMIT;
```

Als deze twee updates succesvol uitgevoerd worden, is de transactie afgerond. Als er iets fout gaat, kun je in plaats daarvan `ROLLBACK` gebruiken om alles terug te draaien.

Transacties zijn belangrijk in situaties waar gegevens altijd consistent moeten blijven, bijvoorbeeld bij banktransacties of orderverwerking.

## ACID-eigenschappen

ACID staat voor:

- Atomicity: een transactie is volledig of helemaal niet.
- Consistency: de database blijft in een geldige toestand.
- Isolation: transacties kunnen gelijktijdig plaatsvinden zonder elkaar te verstoren.
- Durability: als een transactie is bevestigd, blijft deze ook bij een storing behouden.

### Uitleg

- Atomicity: als een opdracht in de transactie faalt, wordt alles teruggedraaid.
- Consistency: de gegevensregels blijven geldig, zoals primaire sleutels en vreemde sleutels.
- Isolation: een andere transactie ziet de wijzigingen niet half afgerond.
- Durability: na `COMMIT` blijven de wijzigingen bewaard, zelfs bij crash of stroomuitval.

> ACID is een belangrijk concept in relationele databases omdat het zorgt voor betrouwbaarheid en veiligheid bij het verwerken van data.

## ACID in één oogopslag

- Atomicity: alles of niets
- Consistency: database blijft geldig
- Isolation: transacties zijn gescheiden
- Durability: bevestigde wijzigingen blijven staan

## Praktisch voorbeeld

```sql
BEGIN;
UPDATE rekeningen SET saldo = saldo - 100 WHERE klant_id = 1;
UPDATE rekeningen SET saldo = saldo + 100 WHERE klant_id = 2;
COMMIT;
```

Als één update mislukt, gebruik je `ROLLBACK` om beide wijzigingen terug te draaien.

## Oefenopdrachten

1. Leg uit waarom een banktransactie als een transactie in SQL moet worden uitgevoerd. Wat gebeurt er als één van de twee updates faalt?
2. Noem de vier ACID-eigenschappen en geef voor elk een kort voorbeeld uit de praktijk.
