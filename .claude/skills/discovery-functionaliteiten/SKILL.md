---
name: discovery-functionaliteiten
description: Review van de functionaliteiten in een discovery (onderwerp functionaliteiten, scope eindgebruikers) — standaard en nieuwe functionaliteiten met omschrijving, business waarde, inschatting en type. Gebruik niet voor de technische uitwerking van koppelingen — zie discovery-nieuwe-plugins.
---

# Discovery: Functionaliteiten

## Wanneer gebruiken

Functionaliteiten hebben sterke voorkeur (`docs/definition-of-done.md`) in de functionele discovery, ongeacht het gekozen pad. Bij Event Storming wordt dit onderwerp gevuld vanuit de uitkomst van de sessie.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op functionaliteiten:
  - Toets elke functionaliteit tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Gebruik `references/deck-voorbeeld.md` als illustratie.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/functionaliteiten.md`.
- Schrijf zelf niets naar `content/functionaliteiten.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per functionaliteit en per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/functionaliteiten.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

De technische uitwerking van koppelingen met andere systemen — dat is `discovery-nieuwe-plugins`. Een plug-in is nodig om te koppelen met een ander systeem; in functionaliteiten staat alleen de functionele behoefte (type "plug-in"). Een nieuwe functionaliteit die Valtimo/GZAC zelf aanpast (productaanpassing) vereist geen plug-in en hoort hier.

## Bronnen

- Register: `topics.yaml` (onderwerp `functionaliteiten`)
- Template (structuur): `templates/functionaliteiten.md`
- Content (na akkoord): `content/functionaliteiten.md`
- Reviewuitkomst: `reviews/functionaliteiten.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`, `references/deck-voorbeeld.md`
