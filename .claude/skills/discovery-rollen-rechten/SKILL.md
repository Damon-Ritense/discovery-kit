---
name: discovery-rollen-rechten
description: Review van de rollen en rechten in een discovery (onderwerp rollen-rechten, scope eindgebruikers) — per rol de toegang en de rechten in Valtimo/GZAC (PBAC). Gebruik niet voor gebruikersprofielen of de manier waarop externen inloggen — zie discovery-gebruikers en discovery-externe-toegang.
---

# Discovery: Rollen & rechten

## Wanneer gebruiken

Rollen & rechten hebben sterke voorkeur (`docs/definition-of-done.md`) in de functionele discovery, ongeacht het gekozen pad. Bij Event Storming wordt dit onderwerp gevuld vanuit de uitkomst van de sessie.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op rollen en rechten:
  - Toets elke rol tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Gebruik `references/deck-voorbeeld.md` als illustratie.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/rollen-rechten.md`.
- Schrijf zelf niets naar `content/rollen-rechten.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per rol en per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/rollen-rechten.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

- Gebruikersprofielen (wie wat doet in het proces, met taken, pijnpunten en voordelen) — dat is `discovery-gebruikers`.
- De manier waarop externen inloggen (DigiD, eHerkenning, broker) — dat is `discovery-externe-toegang`. Rollen & rechten bepaalt wat iemand daarna in het systeem mag.

## Bronnen

- Register: `topics.yaml` (onderwerp `rollen-rechten`)
- Template (structuur): `templates/rollen-rechten.md`
- Content (na akkoord): `content/rollen-rechten.md`
- Reviewuitkomst: `reviews/rollen-rechten.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`, `references/deck-voorbeeld.md`
