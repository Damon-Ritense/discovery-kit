---
name: discovery-event-storming
description: Review van de Event Storming-plaat in een discovery (onderwerp event-storming, scope eindgebruikers) — leest een foto of export van het bord, stelt de kleurlegenda vast en controleert per kaarttype of de inhoud van de post-its bij hun kleur past. Gebruik niet voor de functionele invulling zelf — Event Storming is een hulpmiddel; de uitkomst wordt uitgewerkt in de functionele onderwerpen.
---

# Discovery: Event Storming

## Wanneer gebruiken

Alleen als in `discovery.yaml` `pad: event-storming` staat. Event Storming heeft dan sterke voorkeur (`docs/definition-of-done.md`). Het is een hulpmiddel om tot de functionele invulling te komen.

## Stappen

- Lees de plaat in (foto of export in `diagrams/`, zie de verwijzing in de content of input).
- Stel de kleurlegenda vast:
  - Staat er een legenda in de input, controleer dan of die klopt met de kleuren op de plaat.
  - Ontbreekt de legenda of klopt hij niet, vraag hem dan terug bij de uitvoerder. Gebruik tot die tijd de deckkleuren uit `references/kaarttypen.md` en vermeld dat expliciet.
- Ga per kaarttype na wat er op de plaat te zien is, en toets tegen `references/criteria.md`, met `references/veelgemaakte-fouten.md` als aandachtspunten.
- Leg de reviewuitkomst vast in `reviews/event-storming.md`.
- Schrijf zelf niets naar `content/event-storming.md` — dat is een aparte stap (spelregel 2 in CLAUDE.md): pas na expliciet akkoord van de Uitvoerder Discovery in dezelfde sessie, door de schrijf-skill (`discovery-write`).

## Outputformaat

1. **Kleurlegenda:** zoals vastgesteld, met de bron (input, deck of terug te vragen).
2. **Per kaarttype:** wat er op de plaat te zien is, met de letterlijke tekst van de post-its.
3. **Per criterium** uit `references/criteria.md`: pass / twijfel / fail, met een letterlijk citaat (tekst van de post-it).
4. **Terugvragen** bij gaten, onleesbare post-its of een kleur die niet bij de inhoud past — uit `references/terugvragen.md` of in dezelfde geest. Nooit zelf aanvullen of raden wat er op een onleesbare post-it staat.

## Oordeel vs. overrulen

Het oordeel (pass/twijfel/fail) verandert alleen op basis van nieuwe input uit de Uitvoerder Discovery — niet doordat die aandringt op een hoger oordeel zonder iets nieuws aan te dragen. Geen nieuwe informatie, dan blijft het oordeel staan.

Overrulen kan wel — bijvoorbeeld omdat een criterium voor deze specifieke implementatie minder relevant is — maar dat is een bewuste, expliciete keuze van de Uitvoerder Discovery, geen bijstelling van het oordeel zelf. Leg bij zo'n overrule in `reviews/event-storming.md` vast: welk criterium, en waarom het voor deze implementatie minder relevant is.

## Gebruik niet voor

De functionele invulling zelf. Event Storming is een hulpmiddel; de uitkomst wordt uitgewerkt en gereviewd in `gebruikers`, `data`, `proces`, `functionaliteiten`, `rollen-rechten` en `externe-toegang`. Of die doorvertaling is gebeurd, toetst de consistentie-skill (fase 7).

## Bronnen

- Register: `topics.yaml` (onderwerp `event-storming`)
- Template (structuur): `templates/event-storming.md`
- Content (na akkoord): `content/event-storming.md`
- Reviewuitkomst: `reviews/event-storming.md`
- Kennis: `references/criteria.md`, `references/veelgemaakte-fouten.md`, `references/terugvragen.md`, `references/voorbeelden.md`, `references/kaarttypen.md`
