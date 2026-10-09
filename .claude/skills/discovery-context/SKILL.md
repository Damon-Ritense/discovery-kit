---
name: discovery-context
description: Review van de context van een discovery (onderwerp context, scope organisatie + eindgebruikers — Wie/Wat/Waarom/Wanneer/Hoeveel/Waar). Gebruik niet voor doelen — zie discovery-doelen-organisatie en discovery-doelen-eindgebruikers.
---

# Discovery: Context

## Wanneer gebruiken

De context van de discovery moet altijd vastgelegd worden, ongeacht of het om de organisatie- of de functionele discovery gaat.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op context:
  - Toets de input tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/context.md`.
- Schrijf zelf niets naar `content/context.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/context.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

Doelen van de organisatie of de eindgebruiker — dat zijn andere skills (`discovery-doelen-organisatie`, `discovery-doelen-eindgebruikers`). Context beschrijft de situatie (wie, wat, waarom, wanneer, hoeveel, waar); doelen beschrijven de gewenste uitkomst. Een geformuleerd doel dat als context wordt aangeleverd hoort daar, niet hier.

## Bronnen

- Register: `topics.yaml` (onderwerp `context`)
- Template (structuur): `templates/context.md`
- Content (na akkoord): `content/context.md`
- Reviewuitkomst: `reviews/context.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`
