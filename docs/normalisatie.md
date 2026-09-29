# Normalisatie

## Waarom normaliseren?

Normalisatie is het organiseren van gegevens in een database zodat redundantie wordt verminderd en de consistentie wordt verbeterd. Met andere woorden: je wilt voorkomen dat dezelfde informatie meerdere keren in verschillende tabellen verschijnt.

Een ongeorganiseerde database kan leiden tot:

- dubbele informatie;
- inconsistenties;
- meer onderhoud nodig bij wijzigingen;
- moeilijkere queries en analyses.

Door normalisatie te gebruiken, verdeel je gegevens logisch over passende tabellen. Daardoor wordt de database overzichtelijker en beter te onderhouden.

## Eerste normaalvorm (1NF)

Een tabel is in de eerste normaalvorm als:

- elke kolom een enkelvoudige waarde bevat;
- er geen herhaalde groepen aanwezig zijn;
- elke rij uniek identificeerbaar is.

Voorbeeld van een tabel die niet voldoet aan 1NF:

| klant_id | naam | hobby's |
|---------|------|---------|
| 1 | Anna | tennis, zwemmen |

Hier staat meerdere informatie in één veld (`hobby's`). In 1NF zou je dit opsplitsen in meerdere records of een aparte tabel.

## Tweede normaalvorm (2NF)

Een tabel is in de tweede normaalvorm als:

- deze voldoet aan 1NF;
- alle niet-sleutelvelden volledig afhankelijk zijn van de primaire sleutel.

Dit is vooral relevant als een tabel een samengestelde sleutel heeft. Als een veld alleen afhankelijk is van een deel van die sleutel, is er sprake van overbodige gegevens.

Voorbeeld:

Een orderregel tabel bevat `order_id`, `product_id`, `product_naam` en `prijs`. Hier hangt `product_naam` alleen af van `product_id`, niet van `order_id`. Dat is een teken dat de structuur nog niet optimaal is.

## Derde normaalvorm (3NF)

Een tabel is in de derde normaalvorm als:

- deze voldoet aan 2NF;
- geen niet-sleutelveld afhankelijk is van een ander niet-sleutelveld.

Met andere woorden: je mag geen informatie opslaan die eigenlijk al ergens anders in de database staat en afgeleid kan worden uit andere velden.

Voorbeeld:

Als je in een klantenbestand zowel `stad` als `postcode` opslaat, en `stad` af te leiden is uit `postcode`, dan is dat geen goede normalisatie. Je bewaart dan informatie die niet onafhankelijk is.

## Samenvatting

Normalisatie helpt bij:

- minder redundantie;
- betere data-integriteit;
- eenvoudigere onderhoudbaarheid;
- duidelijkere structuur.

> De kernidee is dat elke informatie op één logische plaats wordt opgeslagen, in plaats van meerdere keren in de database te herhalen.

## Snel overzicht

| Normaalvorm | Doel | Denk aan |
|---|---|---|
| 1NF | Geen herhaalde groepen | Eén waarde per veld |
| 2NF | Geen afhankelijkheid van een deel van een samengestelde sleutel | Logische onderverdeling |
| 3NF | Geen afhankelijke niet-sleutelvelden | Geen overbodige informatie |

## Tip

Normalisatie is niet bedoeld om de database ingewikkelder te maken, maar om de data juist en logisch te houden.

## Oefenopdrachten

1. Noem twee redenen waarom normalisatie belangrijk is bij het ontwerpen van een database. Geef een voorbeeld van een probleem dat ontstaat zonder normalisatie.
2. Bekijk een tabel met `klant_id`, `klant_naam`, `postcode` en `stad`. Leg uit waarom deze tabel mogelijk niet voldoet aan de derde normaalvorm.
