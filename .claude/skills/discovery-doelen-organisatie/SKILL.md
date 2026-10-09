---
name: discovery-doelen-organisatie
description: Review van de organisatiedoelen in een discovery (onderwerp doelen-organisatie, scope organisatie). Gebruik niet voor doelen van eindgebruikers — zie discovery-doelen-eindgebruikers.
---

# Discovery: Doelen — Organisatie

## Wanneer gebruiken

Doelen van de organisatie moeten altijd vastgelegd worden bij een discovery.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op organisatiedoelen:
  - Toets de input tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/doelen-organisatie.md`.
- Schrijf zelf niets naar `content/doelen-organisatie.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`, nog te bouwen).

## Outputformaat

Per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/doelen-organisatie.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

Doelen van eindgebruikers, dit is een andere skill (`discovery-doelen-eindgebruikers`).

## Bronnen

- Register: `topics.yaml` (onderwerp `doelen-organisatie`)
- Template (structuur): `templates/doelen-organisatie.md`
- Content (na akkoord): `content/doelen-organisatie.md`
- Reviewuitkomst: `reviews/doelen-organisatie.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`
