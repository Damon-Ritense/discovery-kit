# Deck-structuur

Afgeleid uit de drie Ritense-decks en `Technische Discovery onderwerpen.docx` (referentie in `docs/bron/`).
Onderwerp-ID's en scope zijn een **voorstel** en moeten door Damon worden bevestigd.

Onderwerpen zonder review (standaardinhoud): even voorstellen, doelstellingen discovery, dagindeling, Valtimo/GZAC-introductie.

## Deck 1 — Organisatie (4 hoofdstukken)

| Hoofdstuk | Slides / inhoud | Onderwerp-ID | Scope |
|---|---|---|---|
| 01 Introductie | Even voorstellen, Doelstellingen discovery | — | — |
| 02 Context & Doelen | Context (Wie/Wat/Waarom/Wanneer/Hoeveel/Waar) | `context` | organisatie |
| | Strategische observaties | `strategische-observaties` | organisatie |
| | Doelen — Organisatie (Wat zijn de doelen / Welke outcomes / Hoe valideren/meten; korte, middellange, lange termijn) | `doelen-organisatie` | organisatie |
| | Visie | `visie` | organisatie |
| | Privacy & AVG (FAQ, vragen voor aparte privacysessie met FG) | `privacy-avg` | organisatie |
| 03 Werkwijze | Roadmap, verwachte betrokkenheid per rol, verloop van een sprint | `werkwijze` | organisatie |
| 04 Vervolgstappen | Functionele discovery, Technische discovery, GDPR-checklist | `vervolgstappen-organisatie` | organisatie |

## Deck 2 — Functioneel (5 hoofdstukken; hoofdstuk 3 is een keuze)

| Hoofdstuk | Slides / inhoud | Onderwerp-ID | Scope |
|---|---|---|---|
| 01 Introductie & doelstelling | Dagindeling, voorstellen, Valtimo/GZAC, doelstellingen | — | — |
| 02 Businesscontext & doelen | Context | `context` | eindgebruikers |
| | Business doelen (zelfde 3-stappenlogica + voorbeeld met termijn en meetwijze) | `doelen-eindgebruikers` | eindgebruikers |
| 03A Event Storming (pad A) | Waarom, de 8 kaarttypen, uitwerking van een event (IST/SOLL, pijnpunt, uitdaging) | `event-storming` | eindgebruikers |
| 03B Functionele invulling (pad B) | Gebruikers: samenhang van een bedrijfsproces, gebruikersprofielen | `gebruikers` | eindgebruikers |
| | Data: verloop, entiteiten, zaakdossiers | `data` | eindgebruikers |
| | Proces: procesmodel huidig/gewenst, gebeurtenissen, uitkomst (product/dienst) | `proces` | eindgebruikers |
| | Functionaliteiten: prioritering (risico/waarde), standaard, nieuwe | `functionaliteiten` | eindgebruikers |
| | Rollen & rechten | `rollen-rechten` | eindgebruikers |
| | Toegang tot zaak voor externe gebruikers | `externe-toegang` | eindgebruikers |
| (einde hoofdstuk 3, beide paden) | Privacy & AVG (FAQ) | `privacy-avg` | eindgebruikers |
| 04 Werkwijze | Roadmap, verwachte betrokkenheid, verloop van een sprint | `werkwijze` | eindgebruikers |
| 05 Vervolgstappen | Nader te onderzoeken | `vervolgstappen-functioneel` | eindgebruikers |

## Deck 3 — Technisch (6 hoofdstukken)

Herzien op basis van `Technische Discovery onderwerpen.docx`: `hosting`, `componenten` en `architectuur-deployment` zijn vervallen; vervangen door vier diagram-onderwerpen in een vast format (Doel / Leidende vraag / Onderwerpen).

| Hoofdstuk | Slides / inhoud | Onderwerp-ID | Scope |
|---|---|---|---|
| 01 Context diagram | Doel: scope en externe dependencies bepalen. Leidende vraag: wie/wat praat met ons systeem? Onderwerpen: actoren, externe systemen, dataflows | `context-diagram` | technisch |
| 02 Applicatie architectuur diagram | Doel: intern design en verhouding externe componenten. Leidende vraag: hoe gaan we functionaliteit realiseren? Onderwerpen: verantwoordelijkheden per deel, hoe componenten met elkaar praten, identificatie van gebruikers | `applicatie-architectuur-diagram` | technisch |
| 03 Data architectuur diagram | Doel: gegevensmodel. Leidende vraag: wat slaan we op? Onderwerpen: entiteiten en attributen, identiteit van entiteiten, relaties | `data-architectuur` | technisch |
| 04 Infrastructuur diagram | Doel: deployment, operations, reliability. Leidende vraag: waar en hoe draait het? Onderwerpen: hardware componenten, netwerk connectiviteit, security | `infrastructuur-diagram` | technisch |
| 05 Nieuwe plug-ins & functionaliteiten | Tabel met omschrijving, business value, type, inschatting, risico/beperking | `nieuwe-plugins` | technisch |
| 06 Vervolgstappen | Nader te onderzoeken | `vervolgstappen-technisch` | technisch |

## Te valideren (door Damon)

1. ~~**Gedeelde onderwerpen.**~~ Besloten (fase 2): `context`, `privacy-avg` en `werkwijze` zijn elk één gedeeld onderwerp (scope: organisatie + eindgebruikers). `vervolgstappen` is gesplitst in `vervolgstappen-organisatie`, `vervolgstappen-functioneel` en `vervolgstappen-technisch`, omdat de inhoud wezenlijk verschilt (vast vs. invulbaar).
2. **Voorbeeld in het functionele deck.** De voorbeeldslide bij "Business doelen" toont doelen als "Verbeteren digitale dienstverlening" en "Efficiëntie interne processen". Die lezen als doelen op organisatieniveau. Moet die slide worden aangepast naar eindgebruikersniveau?
3. **Overlap `nieuwe-plugins` en `functionaliteiten`.** De technische tabel bouwt voort op de nieuwe functionaliteiten uit de functionele discovery. Is dat één keten (en dus een traceerbaarheidseis voor de consistentie-skill) of twee losse onderwerpen?
4. ~~**Samenvoegen.**~~ Besloten (fase 2): `rollen-rechten` en `externe-toegang` blijven apart.
