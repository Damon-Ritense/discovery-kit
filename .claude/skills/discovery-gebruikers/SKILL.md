---
name: discovery-gebruikers
description: Review van de gebruikersprofielen in een discovery (onderwerp gebruikers, scope eindgebruikers) — per profiel taken, pijnpunten en verwachte voordelen. Gebruik niet voor rollen en rechten in het systeem of voor de toegang van externen — zie discovery-rollen-rechten en discovery-externe-toegang.
---

# Discovery: Gebruikers

## Wanneer gebruiken

Gebruikers hebben sterke voorkeur (`docs/definition-of-done.md`) in de functionele discovery, ongeacht het gekozen pad. Bij Event Storming wordt dit onderwerp gevuld vanuit de uitkomst van de sessie.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op gebruikers:
  - Toets elk profiel tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/gebruikers.md`.
- Schrijf zelf niets naar `content/gebruikers.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per profiel en per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/gebruikers.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

- Rollen en rechten in het systeem — dat is `discovery-rollen-rechten`. Gebruikersprofielen beschrijven wie wat doet in het proces; rollen en rechten wat iemand in het systeem mag.
- De toegang van externe gebruikers (DigiD, eHerkenning, portaal) — dat is `discovery-externe-toegang`.

## Bronnen

- Register: `topics.yaml` (onderwerp `gebruikers`)
- Template (structuur): `templates/gebruikers.md`
- Content (na akkoord): `content/gebruikers.md`
- Reviewuitkomst: `reviews/gebruikers.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`, `references/samenhang.md`
