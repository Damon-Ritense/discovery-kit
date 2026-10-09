---
name: discovery-beheer
description: Review van de afspraken rond beheer in een discovery (onderwerp beheer, scope technisch). Gebruik niet voor de werkwijze tijdens het traject — zie discovery-werkwijze.
---

# Discovery: Beheer

## Wanneer gebruiken

Afspraken rond beheer moeten altijd vastgelegd worden (verplicht volgens `docs/definition-of-done.md`), ook bij een bestaande omgeving waarin technisch niets verandert.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op beheer:
  - Toets de input tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/beheer.md`.
- Schrijf zelf niets naar `content/beheer.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen van een criterium kan wel, als bewuste, expliciete keuze van de Uitvoerder Discovery. Leg dat vast in `reviews/beheer.md`: welk criterium, en waarom het voor deze implementatie minder relevant is. Het onderwerp als geheel kan niet worden overruled (verplicht).

## Gebruik niet voor

De werkwijze tijdens het traject (roadmap, betrokkenheid, verloop van een sprint) — dat is `discovery-werkwijze`. Beheer gaat over de afspraken na oplevering.

## Bronnen

- Register: `topics.yaml` (onderwerp `beheer`)
- Template (structuur): `templates/beheer.md`
- Content (na akkoord): `content/beheer.md`
- Reviewuitkomst: `reviews/beheer.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`
