# Deck-structuur

Afgeleid uit de drie Ritense-decks en `Technische Discovery onderwerpen.docx` (referentie in `docs/bron/`).
Onderwerp-ID's en scope zijn een **voorstel** en moeten door Damon worden bevestigd.

De decks dienen als voorbeeld en referentie; ze zijn niet de manier waarop het eindresultaat wordt ingevuld. Wijzigingen in de onderwerpen hoeven dus niet in de decks te worden doorgevoerd.

Vervolgstappen zijn geen onderwerp meer: de voortgang en open punten staan in `status.md` (skill `discovery-status`). Welke onderwerpen verplicht zijn: `docs/definition-of-done.md`.

Onderwerpen zonder review (standaardinhoud): even voorstellen, doelstellingen discovery, dagindeling, Valtimo/GZAC-introductie.

## Deck 1 — Organisatie

| Hoofdstuk | Slides / inhoud | Onderwerp-ID | Scope |
|---|---|---|---|
| 01 Introductie | Even voorstellen, Doelstellingen discovery | — | — |
| 02 Context & Doelen | Context (Wie/Wat/Waarom/Wanneer/Hoeveel/Waar) | `context` | organisatie |
| | Strategische observaties | `strategische-observaties` | organisatie |
| | Doelen — Organisatie (Wat zijn de doelen / Welke outcomes / Hoe valideren/meten; korte, middellange, lange termijn) | `doelen-organisatie` | organisatie |
| | Visie | `visie` | organisatie |
| | Privacy & AVG: GDPR-checklist (nieuwe klant) of verwijzing naar bestaande privacyovereenkomst (bestaande klant). De zes vragen in het deck zijn gespreksstof, niet de structuur. Bron: `docs/bron/GDPR checklist.docx` | `privacy-avg` | organisatie |
| 03 Werkwijze | Roadmap, verwachte betrokkenheid per rol, verloop van een sprint | `werkwijze` | organisatie |
| 04 Vervolgstappen | Vervallen als onderwerp — zie `status.md` | — | — |

## Deck 2 — Functioneel

Het pad (Event Storming of Functionele invulling) bepaalt hoe hoofdstuk 3 wordt ingevuld, niet welke onderwerpen gelden. De onderwerpen van 03B gelden altijd; bij Event Storming vult de uitkomst daarvan deze onderwerpen. Alleen `event-storming` zelf is pad-afhankelijk.

| Hoofdstuk | Slides / inhoud | Onderwerp-ID | Scope |
|---|---|---|---|
| 01 Introductie & doelstelling | Dagindeling, voorstellen, Valtimo/GZAC, doelstellingen | — | — |
| 02 Businesscontext & doelen | Context | `context` | eindgebruikers |
| | Business doelen (zelfde 3-stappenlogica + voorbeeld met termijn en meetwijze) | `doelen-eindgebruikers` | eindgebruikers |
| 03A Event Storming (alleen bij pad Event Storming) | Waarom, de 8 kaarttypen, uitwerking van een event (IST/SOLL, pijnpunt, uitdaging) | `event-storming` | eindgebruikers |
| 03B Functionele invulling (altijd; bij Event Storming gevuld vanuit de uitkomst) | Gebruikers: samenhang van een bedrijfsproces, gebruikersprofielen | `gebruikers` | eindgebruikers |
| | Data: verloop, entiteiten, zaakdossiers | `data` | eindgebruikers |
| | Proces: procesmodel huidig/gewenst, gebeurtenissen, uitkomst (product/dienst) | `proces` | eindgebruikers |
| | Functionaliteiten: prioritering (risico/waarde), standaard, nieuwe | `functionaliteiten` | eindgebruikers |
| | Rollen & rechten | `rollen-rechten` | eindgebruikers |
| | Toegang tot zaak voor externe gebruikers | `externe-toegang` | eindgebruikers |
| (einde hoofdstuk 3) | Privacy & AVG (zie deck 1) | `privacy-avg` | eindgebruikers |
| 04 Werkwijze | Roadmap, verwachte betrokkenheid, verloop van een sprint | `werkwijze` | eindgebruikers |
| 05 Vervolgstappen | Vervallen als onderwerp — zie `status.md` | — | — |

## Deck 3 — Technisch

Bij een nieuwe technische koppeling (`nieuwe-technische-koppeling: ja`) gelden hoofdstuk 01–05. Bij een bestaande omgeving waarin niets verandert geldt alleen `beheer`.

Herzien op basis van `Technische Discovery onderwerpen.docx`: `hosting`, `componenten` en `architectuur-deployment` zijn vervallen; vervangen door vier diagram-onderwerpen in een vast format (Doel / Leidende vraag / Onderwerpen).

| Hoofdstuk | Slides / inhoud | Onderwerp-ID | Scope |
|---|---|---|---|
| 01 Context diagram | Doel: scope en externe dependencies bepalen. Leidende vraag: wie/wat praat met ons systeem? Onderwerpen: actoren, externe systemen, dataflows | `context-diagram` | technisch |
| 02 Applicatie architectuur diagram | Doel: intern design en verhouding externe componenten. Leidende vraag: hoe gaan we functionaliteit realiseren? Onderwerpen: verantwoordelijkheden per deel, hoe componenten met elkaar praten, identificatie van gebruikers | `applicatie-architectuur-diagram` | technisch |
| 03 Data architectuur diagram | Doel: gegevensmodel. Leidende vraag: wat slaan we op? Onderwerpen: entiteiten en attributen, identiteit van entiteiten, relaties | `data-architectuur` | technisch |
| 04 Infrastructuur diagram | Doel: deployment, operations, reliability. Leidende vraag: waar en hoe draait het? Onderwerpen: hardware componenten, netwerk connectiviteit, security | `infrastructuur-diagram` | technisch |
| 05 Nieuwe plug-ins & functionaliteiten | Tabel met omschrijving, business value, type, inschatting, risico/beperking | `nieuwe-plugins` | technisch |
| 06 Beheer | Afspraken rond beheer (altijd verplicht) | `beheer` | technisch |
| — Vervolgstappen | Vervallen als onderwerp — zie `status.md` | — | — |

## Te valideren (door Damon)

1. ~~**Gedeelde onderwerpen.**~~ Besloten (fase 2): `context`, `privacy-avg` en `werkwijze` zijn elk één gedeeld onderwerp (scope: organisatie + eindgebruikers). `vervolgstappen` is later (fase 1) vervallen als onderwerp en vervangen door `status.md`.
2. **Voorbeeld in het functionele deck.** De voorbeeldslide bij "Business doelen" toont doelen als "Verbeteren digitale dienstverlening" en "Efficiëntie interne processen". Die lezen als doelen op organisatieniveau. Moet die slide worden aangepast naar eindgebruikersniveau?
3. **Overlap `nieuwe-plugins` en `functionaliteiten`.** De technische tabel bouwt voort op de nieuwe functionaliteiten uit de functionele discovery. Is dat één keten (en dus een traceerbaarheidseis voor de consistentie-skill) of twee losse onderwerpen?
4. ~~**Samenvoegen.**~~ Besloten (fase 2): `rollen-rechten` en `externe-toegang` blijven apart.
