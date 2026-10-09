---
name: discovery-doelen-eindgebruikers
description: Review van de eindgebruikersdoelen in een discovery (onderwerp doelen-eindgebruikers, scope eindgebruikers). Gebruik niet voor doelen van de organisatie — zie discovery-doelen-organisatie.
---

# Discovery: Doelen — Eindgebruikers

## Wanneer gebruiken

Doelen van de eindgebruikers moeten altijd vastgelegd worden bij een discovery.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op eindgebruikersdoelen:
  - Toets de input tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/doelen-eindgebruikers.md`.
- Schrijf zelf niets naar `content/doelen-eindgebruikers.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/doelen-eindgebruikers.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

Doelen van de organisatie, dit is een andere skill (`discovery-doelen-organisatie`). Het wezenlijke verschil: een eindgebruikersdoel draagt bij aan het vereenvoudigen of verbeteren van de dagelijkse werkzaamheden van de eindgebruiker zelf; een organisatiedoel gaat over sturing, efficiëntie of continuïteit op organisatieniveau. Zie `references/criteria.md`, criterium 5.

## Bronnen

- Register: `topics.yaml` (onderwerp `doelen-eindgebruikers`)
- Template (structuur): `templates/doelen-eindgebruikers.md`
- Content (na akkoord): `content/doelen-eindgebruikers.md`
- Reviewuitkomst: `reviews/doelen-eindgebruikers.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`
