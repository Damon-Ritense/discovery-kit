# Plan: git-template voor discovery-repos

## Doel

Een template waaruit per discovery een eigen repo wordt aangemaakt, gebaseerd op de bestaande discovery-PowerPoints. Twee mechanismen:

1. **Review-skills** die de invulling van een onderwerp kritisch beoordelen op basis van de kennis die in de skill staat.
2. **Een write-skill** die goedgekeurde resultaten naar de juiste plek in de repo schrijft.

De repo is de bron van waarheid; de decks zijn een weergave daarvan.

## Uitgangspunten (besloten)

- Skills zijn ingedeeld **per onderwerp**, niet per deck of per hoofdstuk.
- Organisatiedoelen en eindgebruikersdoelen zijn **twee aparte onderwerpen** met elk een eigen skill (`doelen-organisatie`, `doelen-eindgebruikers`).
- De lijst met onderwerpen staat in `docs/deck-structuur.md` en is akkoord, onder voorbehoud van de punten bij "Te valideren".
- Damon bepaalt de inhoud van de skills. Claude bouwt de structuur.
- Review en schrijven zijn gescheiden stappen; er gaat niets de repo in zonder akkoord.
- Het gekozen pad (Event Storming óf Functionele invulling) staat in `discovery.yaml`.

## Architectuur

```
discovery-template/
├── CLAUDE.md
├── discovery.yaml              # klantnaam, proces, gekozen pad, status per onderwerp
├── topics.yaml                 # register: onderwerp → skill → contentbestand → template
├── content/                    # één bestand per onderwerp
├── templates/                  # template per onderwerp
├── reviews/                    # reviewuitkomst per onderwerp
├── diagrams/
├── docs/
│   ├── PLAN.md
│   ├── deck-structuur.md
│   └── bron/                   # de decks als referentie
└── .claude/skills/
    ├── discovery-<onderwerp-id>/
    │   ├── SKILL.md            # kort: wanneer, stappen, outputformaat
    │   └── references/         # criteria, veelgemaakte fouten, voorbeelden (goed/matig/slecht)
    ├── discovery-consistentie/ # onderwerp-overstijgend, later
    └── discovery-write/        # één generieke schrijf-skill
```

### `topics.yaml` (schema)

```yaml
- id: doelen-organisatie
  scope: organisatie            # organisatie | eindgebruikers | technisch, of een lijst voor een gedeeld onderwerp
  skill: discovery-doelen-organisatie
  content: content/doelen-organisatie.md
  template: templates/doelen-organisatie.md
  decks: [organisatie]
  applies_when: always          # of bv. pad == event-storming
```

Gedeelde onderwerpen (`context`, `privacy-avg`, `werkwijze`) staan als één rij met `scope` als lijst. `vervolgstappen` is gesplitst per deck (`vervolgstappen-organisatie`, `vervolgstappen-functioneel`, `vervolgstappen-technisch`) omdat de inhoud wezenlijk verschilt (vast vs. invulbaar).

Een nieuw onderwerp toevoegen = een skill-map plus een regel in dit register. De write-skill verandert niet.

## Ontwerpregels voor de skills

- `SKILL.md` blijft kort; de kennis staat in `references/` en wordt pas geladen als de skill draait.
- Gemeenschappelijk reviewformaat: per criterium pass / twijfel / fail, een letterlijk citaat uit de input, en terugvragen bij gaten.
- De review vult nooit zelf aan; bij een gat stelt de skill een vraag.
- Elke beschrijving bevat een "gebruik niet voor"-regel.
- Per onderwerp een set testinvoer (goed, matig, slecht) met de verwachte bevindingen, als regressietest bij wijzigingen in de kennis.

## Consistentie-skill (later)

Kijkt over onderwerpen heen, onder meer:
- elk eindgebruikersdoel draagt bij aan minstens één organisatiedoel
- een organisatiedoel zonder eindgebruikersdoel erachter wordt gesignaleerd
- elke functionaliteit verwijst naar een doel
- passen visie en doelen bij elkaar; dekken de gebruikersprofielen de rollen

Pas bouwen als meerdere onderwerpen bestaan.

## Fasering

| # | Fase | Status |
|---|---|---|
| 0 | Beslissingen uit "Open" nemen | [ ] |
| 1 | Bronmateriaal verzamelen (decks, Definition of Done, voorbeelden) | [ ] |
| 2 | Skelet: mappen, `discovery.yaml`, `topics.yaml`, templates per onderwerp | [x] |
| 3 | Slice 1: `doelen-organisatie` (review-skill + write-skill, getest) | [ ] |
| 4 | Slice 2: `doelen-eindgebruikers` | [ ] |
| 5 | Slice 3: `visie` (kwalitatief onderwerp) | [ ] |
| 6 | Uitrollen per deck: organisatie, functioneel, technisch | [ ] |
| 7 | Consistentie-skill | [ ] |
| 8 | Repo als template markeren, pilot op een echte discovery, evaluatie | [ ] |
| 9 | Optioneel: decks genereren uit de repo-content | [ ] |

## Beslissingen

### Open

1. Platform (GitHub, GitLab, Bitbucket): bepaalt de template-functie en eventuele CI.
2. Vertrouwelijkheid: moeten repos privé zijn, en wat mag er niet in (persoonsgegevens, klantnamen)? Tot besloten is geldt: geen persoonsgegevens of klantgevoelige gegevens.
3. Taal van content en skills. Voorstel: Nederlands.
4. Wie commit. Voorstel: Damon handmatig na diff-review in IntelliJ.

### Te valideren

Zie het kopje "Te valideren" in `docs/deck-structuur.md`. Beslist tijdens fase 2: gedeelde onderwerpen (per onderwerp verschillend, zie daar) en `rollen-rechten`/`externe-toegang` blijven apart. Nog open: het voorbeeld bij de business doelen in het functionele deck, overlap `nieuwe-plugins`/`functionaliteiten`.

## Werkwijze met Claude Code

- Open de repo in IntelliJ en draai Claude Code in de terminal.
- Begin elke sessie in plan mode met: *"Lees CLAUDE.md en docs/PLAN.md. Stel voor wat de volgende openstaande fase concreet inhoudt en welke bestanden je aanmaakt. Nog niets bouwen."*
- Commit per afgeronde stap; de voortgang staat in dit bestand, dus `/clear` tussen fasen kan zonder context te verliezen.

## Risico's

- **Te meegaande review:** een skill die alles goedkeurt is waardeloos. Voorkomen met citaatplicht, terugvragen in plaats van aanvullen, en testinvoer met bekende zwakke voorbeelden.
- **Kennis ontbreekt of is dun:** de skill is zo goed als de criteria die erin staan. Slice 1 dient om dat vroeg te zien.
- **Onderwerp-afbakening:** visie, doelen en context liggen dicht bij elkaar. Afbakening in de beschrijvingen en testinvoer die juist op de grens zit.
- **Drift tussen repo en decks:** zolang decks handmatig worden bijgewerkt, kunnen ze afwijken. Fase 9 lost dit structureel op.
- **Vertrouwelijkheid:** zie open beslissing 2.
