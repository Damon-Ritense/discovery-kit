---
name: discovery-data
description: Review van de data in een discovery (onderwerp data, scope eindgebruikers) — verloop van verzoek, zaak en resultaat, en de entiteiten met attributen. Gebruik niet voor het technische gegevensmodel — zie discovery-data-architectuur.
---

# Discovery: Data

## Wanneer gebruiken

Data heeft sterke voorkeur (`docs/definition-of-done.md`) in de functionele discovery, ongeacht het gekozen pad. Bij Event Storming wordt dit onderwerp gevuld vanuit de uitkomst van de sessie.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op data:
  - Toets de input tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Gebruik `references/data-leidraad.md` voor de vragen per onderdeel (verzoek, zaak, resultaat, entiteiten).
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/data.md`.
- Schrijf zelf niets naar `content/data.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/data.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

Het technische gegevensmodel (identiteit van entiteiten, relaties, opslag) — dat is `discovery-data-architectuur`. Data beschrijft functioneel welke gegevens er zijn en hoe ze door de zaak lopen.

## Bronnen

- Register: `topics.yaml` (onderwerp `data`)
- Template (structuur): `templates/data.md`
- Content (na akkoord): `content/data.md`
- Reviewuitkomst: `reviews/data.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`, `references/data-leidraad.md`
