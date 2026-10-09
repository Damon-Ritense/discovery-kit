# Voorbeelden — Functionaliteiten

<!-- Fictief, geen klantgegevens. Opgesteld door Claude, akkoord Damon. -->

## Goed

> **Standaard functionaliteiten**
>
> | Functionaliteit | Omschrijving | Business waarde | Inschatting |
> |---|---|---|---|
> | Lijstscherm aanvragen | Consulent ziet openstaande aanvragen, te filteren op status en ontvangstdatum | Must have | S |
> | Taakformulier beoordeling | Formulier waarin de consulent de toets op recht en het bedrag vastlegt | Must have | M |
> | Dashboard doorlooptijden | Teamleider ziet per week het aantal aanvragen en de gemiddelde doorlooptijd | Could have | M |
>
> **Nieuwe functionaliteiten**
>
> | Functionaliteit | Omschrijving | Business waarde | Type | Inschatting |
> |---|---|---|---|---|
> | Koppeling BRP | Gezinssamenstelling automatisch ophalen bij de start van de zaak | Must have | Plug-in | M |
> | Berekening draagkracht | Draagkracht automatisch berekenen volgens de gemeentelijke beleidsregels | Should have | Productaanpassing | L |

**Verwachte bevindingen:**
- Criterium 1 (omschrijving): pass — citaat: "Gezinssamenstelling automatisch ophalen bij de start van de zaak".
- Criterium 2 (inschatting): pass — alle rijen hebben S, M of L.
- Criterium 3 (business waarde): pass — gespreid over must, should en could.
- Criterium 4 (type, nieuw): pass — citaten: "Plug-in", "Productaanpassing".

## Matig

> **Standaard functionaliteiten**
>
> | Functionaliteit | Omschrijving | Business waarde | Inschatting |
> |---|---|---|---|
> | Lijstscherm | | Must have | S |
> | Taakformulieren | Formulieren voor de consulent | Must have | |
>
> **Nieuwe functionaliteiten**
>
> | Functionaliteit | Omschrijving | Business waarde | Type | Inschatting |
> |---|---|---|---|---|
> | Rapportages | Managementrapportages | Must have | | L |

**Verwachte bevindingen:**
- Criterium 1 (omschrijving): fail bij Lijstscherm — leeg. Terugvraag: "Wat doet het lijstscherm?" Twijfel bij Rapportages — citaat: "Managementrapportages" herhaalt alleen de naam.
- Criterium 2 (inschatting): fail bij Taakformulieren — leeg. Terugvraag: "Wat is de inschatting voor taakformulieren?"
- Criterium 3 (business waarde): twijfel — alles must have. Veelgemaakte fout: alles must have. Terugvraag: "Welke kunnen wachten als de tijd of het budget op is?"
- Criterium 4 (type, nieuw): fail bij Rapportages — leeg. Terugvraag: "Is rapportages een plug-in, een productaanpassing of configuratie?"

## Slecht

> Functionaliteiten: zaaksysteem, formulieren, koppelingen, rapportages.

**Verwachte bevindingen:**
- Criterium 1 (omschrijving): fail — alleen namen, geen omschrijving.
- Criterium 2 (inschatting): fail — niet aanwezig.
- Criterium 3 (business waarde): fail — niet aanwezig.
- Criterium 4 (type): fail — geen onderscheid tussen standaard en nieuw, geen type.
- Veelgemaakte fout: geen link met doel. Terugvraag: "Aan welk doel draagt elke functionaliteit bij?"

## Grensgeval (hoort bij nieuwe-plugins)

> | Functionaliteit | Omschrijving | Business waarde | Type | Inschatting |
> |---|---|---|---|---|
> | Koppeling BRP | Via de Haal Centraal BRP API, OAuth2 client credentials, mapping naar het domeinobject Huishouden, retry bij timeouts | Must have | Plug-in | M |

**Verwachte bevindingen:**
- Criteria 1–4: pass.
- De review signaleert dat de technische uitwerking van de koppeling (API, authenticatie, mapping, foutafhandeling) bij `discovery-nieuwe-plugins` hoort. Hier volstaat de functionele behoefte.
