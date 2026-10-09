---
name: discovery-status
description: Genereert status.md — overzicht van wat volledig, half of nog niet is ingevuld per actief onderwerp, getoetst aan de Definition of Done, plus alle open punten. Gebruik niet voor het reviewen of schrijven van een onderwerp (dat doen de discovery-<onderwerp-id>-skills en discovery-write).
---

# Discovery: status

Vervangt de vroegere vervolgstappen-onderwerpen: één pagina waarop de uitvoerder ziet waar de discovery staat en wat er nog open ligt.

## Wanneer gebruiken

Op verzoek van de Uitvoerder Discovery, bijvoorbeeld aan het eind van een sessie of voor een overleg met de klant.

## Stappen

1. Lees `discovery.yaml` (`nieuwe-klant`, `pad`, `nieuwe-technische-koppeling`, `onderwerpen`) en `topics.yaml` (`applies_when`, `dod`, `decks`).
2. Bepaal per onderwerp of het actief is (`applies_when`). Staat een veld in `discovery.yaml` nog op `TODO`, meld dat bovenaan en behandel de afhankelijke onderwerpen als "onbekend".
3. Zet per actief onderwerp de status om:
   - `akkoord` → **volledig**
   - `in-behandeling`, `review` → **half**
   - `nog-niet-gestart` → **niet**
   - `overruled` → **overruled**, met de `reden`
4. Markeer:
   - een `verplicht` onderwerp dat niet volledig is → **blokkeert DoD**
   - een `sterke-voorkeur`-onderwerp dat niet volledig en niet overruled is → **stuur op**
5. Verzamel de open punten:
   - uit `reviews/<id>.md`: criteria met twijfel of fail die niet zijn overruled, met de bijbehorende terugvraag;
   - uit `open-punten.md`: alle punten die nog niet zijn afgevinkt.
6. Schrijf `status.md` volgens het outputformaat (overschrijf het vorige bestand; het is afgeleid, geen bron).

## Outputformaat (`status.md`)

```markdown
# Status discovery

Gegenereerd: <datum>. DoD: docs/definition-of-done.md

<waarschuwingen, bv. "nieuwe-technische-koppeling staat nog op TODO">

## DoD
<behaald / niet behaald — en welke onderwerpen blokkeren>

## Per onderwerp

| Deck | Onderwerp | DoD | Status | Actie |
|---|---|---|---|---|

## Open punten

### Uit reviews
- <onderwerp>: <criterium> (<twijfel|fail>) — <terugvraag>

### Uit open-punten.md
- <punt>

## Niet van toepassing
- <onderwerp> — <waarom, bv. pad == functionele-invulling of nieuwe-technische-koppeling == nee>
```

## Gebruik niet voor

Het beoordelen of aanvullen van inhoud. Deze skill telt en verzamelt alleen; hij past `discovery.yaml`, `reviews/` en `content/` nooit aan.

## Bronnen

- Status: `discovery.yaml`
- Register: `topics.yaml`
- DoD: `docs/definition-of-done.md`
- Open punten: `reviews/*.md`, `open-punten.md`
- Output: `status.md`
