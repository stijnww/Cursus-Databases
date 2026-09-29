# ER-diagrammen

## Entiteiten en attributen

Een ER-diagram (Entity-Relationship diagram) is een visuele manier om een database te modelleren. Het laat zien welke soorten gegevens er zijn en hoe deze met elkaar samenhangen.

Belangrijkste begrippen:

- entiteit: een object of concept uit de werkelijkheid, zoals `klant`, `product` of `bestelling`;
- attribuut: een eigenschap van een entiteit, zoals `naam`, `email` of `prijs`;
- relatie: de verbinding tussen entiteiten.

Voorbeeld:

- Entiteit: `Klant`
  - klant_id
  - naam
  - email
- Entiteit: `Bestelling`
  - bestel_id
  - datum
  - totaal

Deze entiteiten zijn niet zomaar los van elkaar; ze hebben een betekenisvolle relatie: een klant plaatst een bestelling.

## Relaties tussen entiteiten

Relaties beschrijven hoe twee entiteiten met elkaar verbonden zijn. Hierbij kun je denken aan:

- één-op-veel;
- veel-op-veel;
- één-op-één.

Voorbeeld:

- één klant kan meerdere bestellingen plaatsen;
- elke bestelling hoort bij één klant.

Dus de relatie tussen `Klant` en `Bestelling` is een één-op-veel-relatie.

ER-diagrammen maken dit inzichtelijk zonder dat je meteen te maken hebt met SQL of technische details.

## Cardinaliteit

Cardinaliteit beschrijft hoeveel records van de ene entiteit kunnen samenhangen met hoeveel records van een andere entiteit.

Voorbeelden:

- één-op-één: één student heeft één studentnummer;
- één-op-veel: één docent geeft les aan meerdere studenten;
- veel-op-veel: meerdere studenten volgen meerdere cursussen.

Bij ER-modelleren wordt cardinaliteit vaak weergegeven met symbolen die aangeven hoeveel exemplaren er maximaal aan elkaar gekoppeld kunnen zijn.

Dit is belangrijk omdat de juiste relaties bepalen hoe je de tabellen in een database gaat structureren.

> Een ER-diagram is een blauwdruk voor de database: het laat zien wat de data betekent en hoe de verschillende delen van het model met elkaar verbonden zijn.

## In één oogopslag

- Entiteit = object of concept
- Attribuut = eigenschap van een entiteit
- Relatie = verband tussen entiteiten
- Cardinaliteit = hoeveel records ermee samenhangen

### Mini-voorbeeld

- Klant
  - klant_id
  - naam
  - email
- Bestelling
  - bestel_id
  - datum
  - totaal

Relatie: één klant kan meerdere bestellingen plaatsen.

## Visuele gedachtegang

Voordat je SQL schrijft, moet je eerst begrijpen wat de echte gegevens zijn en hoe ze samenhangen. Een ER-diagram helpt je dat te zien zonder direct in SQL te denken.

## Oefenopdrachten

1. Teken of beschrijf een ER-diagram voor een winkel met de entiteiten `klant`, `bestelling` en `product`. Geef aan welke relaties er zijn.
2. Wat is het verschil tussen een entiteit en een attribuut? Geef voor beide een voorbeeld uit een schooldatabase.
