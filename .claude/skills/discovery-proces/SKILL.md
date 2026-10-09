---
name: discovery-proces
description: Review van het proces in een discovery (onderwerp proces, scope eindgebruikers) — procesmodel huidig en gewenst, en de gebeurtenissen met wie en actie. Gebruik niet voor de Event Storming-sessie zelf — zie discovery-event-storming.
---

# Discovery: Proces

## Wanneer gebruiken

Proces heeft sterke voorkeur (`docs/definition-of-done.md`) in de functionele discovery, ongeacht het gekozen pad. Bij Event Storming wordt dit onderwerp gevuld vanuit de uitkomst van de sessie.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op proces:
  - Toets de input tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Gebruik `references/deck-voorbeeld.md` als illustratie van gebeurtenissen.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/proces.md`.
- Schrijf zelf niets naar `content/proces.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/proces.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

De Event Storming-sessie zelf (kaarttypen, IST/SOLL per event) — dat is `discovery-event-storming`. Proces is het uitgewerkte resultaat: het huidige en gewenste procesmodel en de gebeurtenissen.

## Bronnen

- Register: `topics.yaml` (onderwerp `proces`)
- Template (structuur): `templates/proces.md`
- Content (na akkoord): `content/proces.md`
- Reviewuitkomst: `reviews/proces.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`, `references/deck-voorbeeld.md`
