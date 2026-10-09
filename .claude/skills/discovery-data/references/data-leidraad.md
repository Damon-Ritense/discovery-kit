# Gespreksleidraad — Data

<!-- Bron: functioneel deck, slides 23 en 24. -->

## Verloop (slide 23)

Het verwerken van een zaak brengt doorgaans drie grote aandachtspunten met zich mee op het gebied van data.

### 1. Verzoek

- Documenten?
- Data van een externe bron (DigiD, KvK)?
- Relationele data?
- Hoeveelheid data?
- Aanleiding: verzoek via de Objecten API, of handmatig via een startformulier?

### 2. Zaak

- Info van externe bronnen samenbrengen (KvK, BRP)?
- Nieuwe info vastgelegd bij de zaak?
- Relatie tot andere zaken?
- Hoeveelheid data?
- Hoeveel en welke zaaktypen?

### 3. Resultaat

- Wordt er een resultaat vastgelegd? Waar?
- Welke metadata?
- Documenten koppelen?
- Wat gebeurt er hierna met dit resultaat?

Doorlopend tijdens de zaakafhandeling: data wordt vastgelegd als zaakdetail en in de domeinregistratie, en wordt bijgewerkt terwijl de zaak wordt behandeld.

## Entiteiten (slide 24)

Door entiteiten en hun onderdelen in kaart te brengen, wordt de structuur van de informatie duidelijk.

Willen we een zaak starten voor een boom of voor een bos?
- Een boom, met attributen: bladeren, takken, hoogte.
- Een bos, met attributen: bomen, beren, boswachters.

Hoe later je er in een implementatie achter komt, hoe groter de benodigde herstelwerkzaamheden. Stel dus vooraf goed vast welke datastructuur wordt geaccepteerd en geïmplementeerd. Kleine aanpassingen (een attribuut of een nieuwe entiteit toevoegen) kunnen zonder veel impact worden doorgevoerd.
