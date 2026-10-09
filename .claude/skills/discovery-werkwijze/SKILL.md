---
name: discovery-werkwijze
description: Review van de werkwijze in een discovery (onderwerp werkwijze, scope organisatie + eindgebruikers) — MVP, sprintvariant en afgesproken inzet per rol tijdens het traject. Gebruik niet voor afspraken na oplevering — zie discovery-beheer.
---

# Discovery: Werkwijze

## Wanneer gebruiken

De werkwijze heeft sterke voorkeur (`docs/definition-of-done.md`), in zowel de organisatorische als de functionele discovery. De vaste Ritense-werkwijze staat in `references/werkwijze-standaard.md`; de review toetst alleen de keuzes voor deze discovery.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op werkwijze:
  - Toets de input tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Gebruik `references/werkwijze-standaard.md` om afwijkingen van de standaard en overgenomen standaardwaarden te herkennen.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/werkwijze.md`.
- Schrijf zelf niets naar `content/werkwijze.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/werkwijze.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

Afspraken na oplevering, zoals incidentafhandeling en releases — dat is `discovery-beheer`. Werkwijze gaat over de samenwerking tijdens het traject.

## Bronnen

- Register: `topics.yaml` (onderwerp `werkwijze`)
- Template (structuur): `templates/werkwijze.md`
- Content (na akkoord): `content/werkwijze.md`
- Reviewuitkomst: `reviews/werkwijze.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`, `references/werkwijze-standaard.md`
