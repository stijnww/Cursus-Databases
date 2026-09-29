# SQL basis

## SELECT

`SELECT` wordt gebruikt om gegevens uit een database op te halen. Het is waarschijnlijk het meest gebruikte SQL-commando.

Basisvoorbeeld:

```sql
SELECT *
FROM klanten;
```

Deze query geeft alle kolommen en alle rijen uit de tabel `klanten` terug.

Als je alleen bepaalde kolommen wilt zien:

```sql
SELECT naam, email
FROM klanten;
```

Je kunt ook voorwaarden toevoegen met `WHERE`:

```sql
SELECT naam, email
FROM klanten
WHERE klant_id = 1;
```

Met `ORDER BY` kun je resultaten sorteren:

```sql
SELECT naam, email
FROM klanten
ORDER BY naam ASC;
```

## INSERT

`INSERT` wordt gebruikt om nieuwe records aan een tabel toe te voegen.

Basisvoorbeeld:

```sql
INSERT INTO klanten (naam, email)
VALUES ('Anna', 'anna@example.com');
```

Je kunt meerdere records tegelijk invoegen:

```sql
INSERT INTO klanten (naam, email)
VALUES
    ('Bob', 'bob@example.com'),
    ('Celine', 'celine@example.com');
```

## UPDATE

`UPDATE` wordt gebruikt om bestaande gegevens te wijzigen.

Voorbeeld:

```sql
UPDATE klanten
SET email = 'nieuw@email.com'
WHERE klant_id = 1;
```

Hierbij wordt alleen de klant met `klant_id = 1` aangepast. Zonder `WHERE` zouden alle records worden gewijzigd.

## DELETE

`DELETE` wordt gebruikt om records uit een tabel te verwijderen.

Voorbeeld:

```sql
DELETE FROM klanten
WHERE klant_id = 1;
```

Let op: ook hier is `WHERE` belangrijk. Zonder `WHERE` zouden alle gegevens uit de tabel worden verwijderd.

## Samenvatting

De basisbewerkingen in SQL zijn:

- `SELECT`: gegevens lezen
- `INSERT`: gegevens toevoegen
- `UPDATE`: gegevens aanpassen
- `DELETE`: gegevens verwijderen

Deze vier opdrachten vormen de kern van het werken met relationele databases.

## In één oogopslag

- `SELECT` = lees gegevens
- `INSERT` = voeg gegevens toe
- `UPDATE` = wijzig gegevens
- `DELETE` = verwijder gegevens

## Snel overzicht

| Commando | Doel | Voorbeeld |
|---|---|---|
| `SELECT` | Gegevens ophalen | `SELECT * FROM klanten;` |
| `INSERT` | Nieuwe gegevens toevoegen | `INSERT INTO klanten ...` |
| `UPDATE` | Bestaande gegevens aanpassen | `UPDATE klanten SET ...` |
| `DELETE` | Gegevens verwijderen | `DELETE FROM klanten WHERE ...` |

## Oefenopdrachten

1. Schrijf een query die van alle klanten alleen de naam en e-mailadres toont, gesorteerd op naam van A tot Z.
2. Voeg twee nieuwe klanten toe aan de tabel `klanten` en wijzig daarna het e-mailadres van één van die klanten. Verwijder daarna de klant die je als tweede hebt toegevoegd.
