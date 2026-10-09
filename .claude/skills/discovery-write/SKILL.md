---
name: discovery-write
description: Schrijft een goedgekeurde reviewuitkomst naar content/, generiek voor elk onderwerp uit topics.yaml. Gebruik niet voor het reviewen zelf (dat doen de discovery-<onderwerp-id>-skills) en nooit zonder expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie.
---

# Discovery: schrijven

Eén generieke skill voor alle onderwerpen. Bij een nieuw onderwerp verandert deze skill niet — alleen `topics.yaml` krijgt er een regel bij.

## Wanneer gebruiken

Alleen als losse, expliciete stap nadat de Uitvoerder Discovery in dezelfde sessie akkoord heeft gegeven op een reviewuitkomst. Dat akkoord mag gegeven worden ook als er nog twijfel- of fail-items open staan (overrulen is toegestaan) — deze skill controleert dat zelf niet, en vult ook nooit zelf inhoudelijk aan.

## Stappen

1. Zoek het onderwerp-id op in `topics.yaml` en haal het `content`-pad op.
2. Bestaat dat bestand al? Vul aan per sectie (merge op basis van de koppen uit het bijbehorende `template`-bestand) — overschrijf niet het hele bestand.
3. Bestaat het nog niet? Maak het aan, gestructureerd volgens het template.
4. Werk `discovery.yaml` bij: `onderwerpen.<id>` naar `akkoord`.

## Gebruik niet voor

Het reviewen van input — dat doen de `discovery-<onderwerp-id>`-skills, met het reviewformaat (pass/twijfel/fail + citaat) en de reviewuitkomst in `reviews/<id>.md`. Deze skill schrijft pas ná dat akkoord.

## Bronnen

- Register: `topics.yaml` (content-pad, template-pad per onderwerp-id)
- Status: `discovery.yaml` (`onderwerpen.<id>`)
