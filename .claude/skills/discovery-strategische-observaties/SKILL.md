---
name: discovery-strategische-observaties
description: Review van de strategische observaties in een discovery (onderwerp strategische-observaties, scope organisatie) — per observatie de kans, het grootste risico en de mitigatie. Gebruik niet voor organisatiedoelen of de visie — zie discovery-doelen-organisatie en discovery-visie.
---

# Discovery: Strategische observaties

## Wanneer gebruiken

Strategische observaties hebben sterke voorkeur (`docs/definition-of-done.md`) in de organisatorische discovery.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op strategische observaties:
  - Toets elke observatie tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Gebruik `references/deck-voorbeeld.md` om overgenomen thema's of formuleringen te herkennen.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/strategische-observaties.md`.
- Schrijf zelf niets naar `content/strategische-observaties.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per observatie en per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/strategische-observaties.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

- Organisatiedoelen — dat is `discovery-doelen-organisatie`. Doelen beschrijven de gewenste uitkomst; observaties de kansen en risico's op weg daarheen.
- De visie — dat is `discovery-visie`. De visie is het kompas op lange termijn; observaties zijn concreet en traject-specifiek.

## Bronnen

- Register: `topics.yaml` (onderwerp `strategische-observaties`)
- Template (structuur): `templates/strategische-observaties.md`
- Content (na akkoord): `content/strategische-observaties.md`
- Reviewuitkomst: `reviews/strategische-observaties.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`, `references/deck-voorbeeld.md`
