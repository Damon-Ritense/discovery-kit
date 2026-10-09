---
name: discovery-visie
description: Review van de visie in een discovery (onderwerp visie, scope organisatie) — toekomstgericht, richtinggevend, niet te gedetailleerd. Gebruik niet voor organisatiedoelen — zie discovery-doelen-organisatie.
---

# Discovery: Visie

## Wanneer gebruiken

De visie heeft sterke voorkeur (`docs/definition-of-done.md`) in de organisatorische discovery.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op de visie:
  - Toets de input tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Gebruik `references/deck-voorbeeld.md` om een overgenomen deckvisie te herkennen.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/visie.md`.
- Schrijf zelf niets naar `content/visie.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/visie.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

Organisatiedoelen — dat is `discovery-doelen-organisatie`. Doelen zijn concreet en meetbaar, met termijn en meetmethode; de visie is het kompas erachter.

## Bronnen

- Register: `topics.yaml` (onderwerp `visie`)
- Template (structuur): `templates/visie.md`
- Content (na akkoord): `content/visie.md`
- Reviewuitkomst: `reviews/visie.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`, `references/deck-voorbeeld.md`
