# Joins

## INNER JOIN

Een `INNER JOIN` retourneert alleen de records die aan beide tabellen voldoen. Met andere woorden: je krijgt alleen de combinaties die bestaan in beide tabellen.

Voorbeeld:

```sql
SELECT klanten.naam, bestellingen.bestel_id
FROM klanten
INNER JOIN bestellingen ON klanten.klant_id = bestellingen.klant_id;
```

Deze query laat alleen klanten zien die daadwerkelijk een bestelling hebben geplaatst.

## LEFT JOIN

Een `LEFT JOIN` geeft alle records uit de linker tabel terug, zelfs als er geen overeenkomst in de rechter tabel bestaat. De rechter waarden zijn dan `NULL`.

Voorbeeld:

```sql
SELECT klanten.naam, bestellingen.bestel_id
FROM klanten
LEFT JOIN bestellingen ON klanten.klant_id = bestellingen.klant_id;
```

Hier zie je alle klanten, ook die nog geen bestelling hebben gedaan.

## RIGHT JOIN

Een `RIGHT JOIN` werkt precies andersom: alle records uit de rechter tabel worden getoond, zelfs als er geen overeenkomst in de linker tabel is.

Voorbeeld:

```sql
SELECT klanten.naam, bestellingen.bestel_id
FROM klanten
RIGHT JOIN bestellingen ON klanten.klant_id = bestellingen.klant_id;
```

Deze query toont alle bestellingen, zelfs als er geen klantrecord gekoppeld is.

## Wanneer gebruik je welke join?

- `INNER JOIN`: alleen overeenkomende gegevens
- `LEFT JOIN`: alles uit de linker tabel + overeenkomende gegevens uit de rechter tabel
- `RIGHT JOIN`: alles uit de rechter tabel + overeenkomende gegevens uit de linker tabel

> Joins zijn essentieel in relationele databases, omdat ze gegevens uit verschillende tabellen combineren op basis van hun relatie.

## Snel vergelijken

| Join-type | Wat krijg je terug? |
|---|---|
| `INNER JOIN` | Alleen records die in beide tabellen voorkomen |
| `LEFT JOIN` | Alle records uit de linker tabel, ook zonder match |
| `RIGHT JOIN` | Alle records uit de rechter tabel, ook zonder match |

## Denk aan het voorbeeld

- `klanten` is de linker tabel
- `bestellingen` is de rechter tabel
- de join gebeurt op `klant_id`

Als je wilt weten welke klanten bestellingen hebben, gebruik je meestal een `LEFT JOIN` of `INNER JOIN`.

## Oefenopdrachten

1. Schrijf een query met een `INNER JOIN` die alle klanten toont samen met hun bestellingen.
2. Geef aan welk type join je gebruikt als je alle klanten wilt tonen, ook als ze nog geen bestelling hebben gemaakt. Waarom is dat handig?
