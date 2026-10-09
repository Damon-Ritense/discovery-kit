---
name: discovery-privacy-avg
description: Review van Privacy & AVG in een discovery (onderwerp privacy-avg, scope organisatie + eindgebruikers) — de GDPR-checklist bij een nieuwe klant, of de verwijzing naar een bestaande privacyovereenkomst. Gebruik niet voor de beheerafspraken als geheel — zie discovery-beheer.
---

# Discovery: Privacy & AVG

## Wanneer gebruiken

Privacy & AVG moet altijd vastgelegd worden (verplicht volgens `docs/definition-of-done.md`):
- nieuwe klant (`nieuwe-klant: ja` in `discovery.yaml`): de GDPR-checklist is volledig ingevuld;
- bestaande klant met bestaande afspraken (`nee`): een vermelding van de bestaande privacyovereenkomst is voldoende.

## Stappen

- Beoordeel de aangeleverde informatie op onderwerp.
- Indien het onderwerp aansluit op privacy & AVG:
  - Toets de input tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
  - Gebruik `references/gdpr-toelichting.md` om de checklistvragen en hun achtergrond te begrijpen.
  - Ga over op het outputformaat om de input te beoordelen.
- Leg de reviewuitkomst vast in `reviews/privacy-avg.md`.
- Schrijf zelf niets naar `content/privacy-avg.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

Per criterium uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat uit de input.
Bij een gat: een terugvraag uit `references/terugvragen.md` (of zelf geformuleerd in dezelfde geest) — nooit zelf aanvullen.
Bijzondere persoonsgegevens: opvallend signaleren met een open punt, geen fail (zie `references/criteria.md`).

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen van een criterium kan wel, als bewuste, expliciete keuze van de Uitvoerder Discovery. Leg dat vast in `reviews/privacy-avg.md`: welk criterium, en waarom het voor deze implementatie minder relevant is. Het onderwerp als geheel kan niet worden overruled (verplicht).

## Gebruik niet voor

De beheerafspraken als geheel — dat is `discovery-beheer`. Privacy & AVG gaat over de verwerking van persoonsgegevens: grondslag, bijzondere gegevens, verwerkersovereenkomsten en rechten van betrokkenen. Overlap met beheer (bv. securitycontroles en SLA bij vraag 3e) is toegestaan; de review signaleert die niet.

## Bronnen

- Register: `topics.yaml` (onderwerp `privacy-avg`)
- Template (structuur): `templates/privacy-avg.md`
- Content (na akkoord): `content/privacy-avg.md`
- Reviewuitkomst: `reviews/privacy-avg.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`, `references/gdpr-toelichting.md`
