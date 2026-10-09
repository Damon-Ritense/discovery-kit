# Plan: git-template voor discovery-repos

## Doel

Een template waaruit per discovery een eigen repo wordt aangemaakt, gebaseerd op de bestaande discovery-PowerPoints. Twee mechanismen:

1. **Review-skills** die de invulling van een onderwerp kritisch beoordelen op basis van de kennis die in de skill staat.
2. **Een write-skill** die goedgekeurde resultaten naar de juiste plek in de repo schrijft.

De repo is de bron van waarheid en het eindresultaat. De bestaande decks dienen als voorbeeld; optioneel kan later een deck uit de repo-content worden gegenereerd (fase 9).

## Uitgangspunten (besloten)

- Skills zijn ingedeeld **per onderwerp**, niet per deck of per hoofdstuk.
- Organisatiedoelen en eindgebruikersdoelen zijn **twee aparte onderwerpen** met elk een eigen skill (`doelen-organisatie`, `doelen-eindgebruikers`).
- De lijst met onderwerpen staat in `docs/deck-structuur.md` en is akkoord, onder voorbehoud van de punten bij "Te valideren".
- Damon bepaalt de inhoud van de skills. Claude bouwt de structuur.
- Review en schrijven zijn gescheiden stappen; er gaat niets de repo in zonder akkoord.
- Het gekozen pad (Event Storming of Functionele invulling) staat in `discovery.yaml`. Het bepaalt hoe deel 2 wordt ingevuld, niet welke onderwerpen gelden; alleen `event-storming` is pad-afhankelijk.
- Of het om een nieuwe technische koppeling gaat staat in `discovery.yaml` (`nieuwe-technische-koppeling`). Zo niet, dan geldt van deel 3 alleen `beheer`.
- Definition of Done: `docs/definition-of-done.md`. Niveau per onderwerp (`verplicht` / `sterke-voorkeur`) in `topics.yaml`.
- Vervolgstappen zijn geen onderwerp; voortgang en open punten staan in `status.md` (skill `discovery-status`), met eigen notities in `open-punten.md`.
- De decks zijn voorbeeld en referentie, niet de manier om het eindresultaat in te vullen; ze hoeven niet mee te veranderen met de onderwerpen.

## Architectuur

```
discovery-template/
├── CLAUDE.md
├── discovery.yaml              # klantnaam, proces, gekozen pad, nieuwe technische koppeling, status per onderwerp
├── topics.yaml                 # register: onderwerp → skill → contentbestand → template → DoD-niveau
├── status.md                   # gegenereerd door discovery-status: voortgang en open punten
├── open-punten.md              # logboek van de uitvoerder
├── content/                    # één bestand per onderwerp
├── templates/                  # template per onderwerp
├── reviews/                    # reviewuitkomst per onderwerp
├── diagrams/
├── docs/
│   ├── PLAN.md
│   ├── deck-structuur.md
│   ├── definition-of-done.md
│   └── bron/                   # de decks als referentie
└── .claude/skills/
    ├── discovery-<onderwerp-id>/
    │   ├── SKILL.md            # kort: wanneer, stappen, outputformaat
    │   └── references/         # criteria, veelgemaakte fouten, voorbeelden (goed/matig/slecht)
    ├── discovery-consistentie/ # onderwerp-overstijgend, later
    ├── discovery-status/       # genereert status.md
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
  applies_when: always          # of "pad == event-storming" / "nieuwe-technische-koppeling == ja"
  dod: sterke-voorkeur          # verplicht | sterke-voorkeur
```

Gedeelde onderwerpen (`context`, `privacy-avg`, `werkwijze`) staan als één rij met `scope` als lijst. `vervolgstappen` is vervallen als onderwerp en vervangen door `status.md`.

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
- bij pad Event Storming: zijn de uitkomsten doorgezet naar de losse functionele onderwerpen

Pas bouwen als meerdere onderwerpen bestaan.

## Fasering

| # | Fase | Status |
|---|---|---|
| 0 | Beslissingen uit "Open" nemen | [x] |
| 1 | Bronmateriaal verzamelen (decks, Definition of Done, voorbeelden) | [ ] binnen: decks, DoD, GDPR-checklist, voorbeelden per gebouwd onderwerp. Open: echte event storming-plaat, bronmateriaal beheer, context technisch deel |
| 2 | Skelet: mappen, `discovery.yaml`, `topics.yaml`, templates per onderwerp | [x] |
| 3 | Slice 1: `doelen-organisatie` (review-skill + write-skill, getest) | [ ] |
| 4 | Slice 2: `doelen-eindgebruikers` | [ ] |
| 5 | Slice 3: `visie` (kwalitatief onderwerp) | [ ] |
| 6 | Uitrollen per deck: organisatie, functioneel, technisch | [ ] |
| 7 | Consistentie-skill | [ ] |
| 8 | Repo als template markeren, privé-zijn borgen (Actions-check of org-instelling die publieke repos blokkeert), pilot op een echte discovery, evaluatie | [ ] |
| 9 | Optioneel: decks genereren uit de repo-content | [ ] |

### Status per onderwerp

Werkwijze per onderwerp: template → kennis (Damon) → voorbeelden (concept door Claude, akkoord Damon) → skill bouwen → testen.

| Onderwerp | Deck | Status |
|---|---|---|
| `context` | organisatie, functioneel | gebouwd, niet getest |
| `privacy-avg` | organisatie, functioneel | gebouwd, niet getest |
| `werkwijze` | organisatie, functioneel | gebouwd, niet getest |
| `strategische-observaties` | organisatie | gebouwd, niet getest |
| `doelen-organisatie` | organisatie | gebouwd, niet getest |
| `visie` | organisatie | gebouwd, niet getest |
| `doelen-eindgebruikers` | functioneel | gebouwd, niet getest |
| `gebruikers` | functioneel | gebouwd, niet getest |
| `data` | functioneel | gebouwd, niet getest |
| `proces` | functioneel | gebouwd, niet getest |
| `functionaliteiten` | functioneel | gebouwd, niet getest |
| `rollen-rechten` | functioneel | gebouwd, niet getest |
| `externe-toegang` | functioneel | gebouwd, niet getest |
| `event-storming` | functioneel | gebouwd, niet getest (voorbeelden in tekst; echte plaat volgt) |
| `beheer` | technisch | skelet, kennis TODO (Damon) |
| `context-diagram`, `applicatie-architectuur-diagram`, `data-architectuur`, `infrastructuur-diagram`, `nieuwe-plugins` | technisch | geparkeerd: wacht op context van Damon |

## Beslissingen

### Besloten

1. Platform: GitHub (template-repo via "Use this template", CI via GitHub Actions).
2. Vertrouwelijkheid: discovery-repos zijn altijd privé met beperkte toegang. Klantgegevens mogen erin, ook namen van contactpersonen. In dit templaterepo zelf komen geen klantgegevens.
3. Taal: Nederlands, voor content en skills.
4. Commit: Damon handmatig na diff-review in IntelliJ. Claude commit nooit.

### Open

Geen.

### Te valideren

Zie het kopje "Te valideren" in `docs/deck-structuur.md`. Beslist tijdens fase 2: gedeelde onderwerpen (per onderwerp verschillend, zie daar) en `rollen-rechten`/`externe-toegang` blijven apart. Ook besloten: `nieuwe-plugins` en `functionaliteiten` zijn aparte onderwerpen (zie daar). Ook besloten: de voorbeeldslide bij de business doelen in het functionele deck wordt niet aangepast. Er staan geen punten meer open.

## Nieuwe discovery-repo aanmaken

Een discovery-repo wordt altijd **privé** aangemaakt (besluit 2).

- Via GitHub: **Use this template** en bij de zichtbaarheid **Private** kiezen.
- Via de CLI: `gh repo create <naam> --template Damon-Ritense/discovery-kit --private --clone`
- Daarna `discovery.yaml` invullen: klant, bedrijfsproces en pad.

## Werkwijze met Claude Code

- Open de repo in IntelliJ en draai Claude Code in de terminal.
- Begin elke sessie in plan mode met: *"Lees CLAUDE.md en docs/PLAN.md. Stel voor wat de volgende openstaande fase concreet inhoudt en welke bestanden je aanmaakt. Nog niets bouwen."*
- Commit per afgeronde stap; de voortgang staat in dit bestand, dus `/clear` tussen fasen kan zonder context te verliezen.

## Risico's

- **Te meegaande review:** een skill die alles goedkeurt is waardeloos. Voorkomen met citaatplicht, terugvragen in plaats van aanvullen, en testinvoer met bekende zwakke voorbeelden.
- **Kennis ontbreekt of is dun:** de skill is zo goed als de criteria die erin staan. Slice 1 dient om dat vroeg te zien.
- **Onderwerp-afbakening:** visie, doelen en context liggen dicht bij elkaar. Afbakening in de beschrijvingen en testinvoer die juist op de grens zit.
- **Drift tussen repo en decks:** de decks zijn voorbeeld en hoeven niet mee te veranderen. Wordt een deck voor de klant gemaakt, dan voorkomt genereren uit de repo (fase 9) afwijkingen.
- **Vertrouwelijkheid:** discovery-repos bevatten klantgegevens (zie besluit 2). De toegang tot elke discovery-repo moet daarom beperkt blijven.
