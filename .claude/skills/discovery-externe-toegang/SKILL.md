---
name: discovery-externe-toegang
description: Review van de toegang tot de zaak voor externe gebruikers in een discovery (onderwerp externe-toegang, scope eindgebruikers) — wie, via portaal of externe klanttaak, met welk inlogmiddel, welke acties, en de broker. Gebruik niet voor wat externen in het systeem mogen — zie discovery-rollen-rechten.
---

# Discovery: Externe toegang

## Wanneer gebruiken

Externe toegang heeft sterke voorkeur (`docs/definition-of-done.md`) in de functionele discovery, ongeacht het gekozen pad. Bij Event Storming wordt dit onderwerp gevuld vanuit de uitkomst van de sessie.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op externe toegang:
  - Toets de input tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Gebruik `references/deck-voorbeeld.md` als illustratie.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/externe-toegang.md`.
- Schrijf zelf niets naar `content/externe-toegang.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/externe-toegang.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

Wat externen in het systeem mogen nadat ze zijn ingelogd — dat is `discovery-rollen-rechten`. Externe toegang gaat over wie van buiten toegang krijgt en hoe ze inloggen.

## Bronnen

- Register: `topics.yaml` (onderwerp `externe-toegang`)
- Template (structuur): `templates/externe-toegang.md`
- Content (na akkoord): `content/externe-toegang.md`
- Reviewuitkomst: `reviews/externe-toegang.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`, `references/deck-voorbeeld.md`
