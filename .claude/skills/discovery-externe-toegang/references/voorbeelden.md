# Voorbeelden — Externe toegang

<!-- Fictief, geen klantgegevens. Opgesteld door Claude, akkoord Damon (kolommen aangepast). -->

## Goed

> | Externe gebruiker | Manier van toegang | Inlogmiddel | Acties |
> |---|---|---|---|
> | Inwoner | Portaal | DigiD | Aanvraag bijzondere bijstand indienen, stukken aanleveren, status volgen |
> | Bewindvoerder (namens inwoner) | Portaal | DigiD Machtigen | Aanvraag indienen en volgen namens de inwoner |
> | Budgetcoach (stichting) | Externe klanttaak | eHerkenning | Budgetplan uploaden bij een lopende aanvraag |
>
> **Broker:** de gemeente gebruikt een bestaande broker voor DigiD en eHerkenning, die ook voor het huidige e-loket wordt gebruikt. Bevestigd door de functioneel beheerder.

**Verwachte bevindingen:**
- Criterium 1 (externe gebruikers): pass — citaat: "Inwoner", "Bewindvoerder (namens inwoner)", "Budgetcoach (stichting)".
- Criterium 2 (inlogmiddel): pass — citaat: "DigiD Machtigen".
- Criterium 3 (acties): pass — citaat: "Budgetplan uploaden bij een lopende aanvraag".
- Criterium 4 (broker): pass — citaat: "een bestaande broker voor DigiD en eHerkenning … Bevestigd door de functioneel beheerder."

## Matig

> | Externe gebruiker | Manier van toegang | Inlogmiddel | Acties |
> |---|---|---|---|
> | Inwoner | Portaal | DigiD | Aanvraag indienen |
> | Budgetcoach | Externe klanttaak | | Stukken aanleveren |
>
> **Broker:** DigiD is al geregeld bij de gemeente.

**Verwachte bevindingen:**
- Criterium 1 (externe gebruikers): pass.
- Criterium 2 (inlogmiddel): fail bij Budgetcoach — leeg. Terugvraag: "Met welk inlogmiddel logt de budgetcoach in?"
- Criterium 3 (acties): pass.
- Criterium 4 (broker): twijfel — citaat: "DigiD is al geregeld bij de gemeente." Niet duidelijk welke broker, en eHerkenning ontbreekt. Veelgemaakte fout: broker niet geregeld. Terugvraag: "Is nagegaan of de broker er is, of is dat een aanname?"
- Veelgemaakte fout: machtigingen vergeten. Terugvraag: "Kan iemand namens een ander handelen, bijvoorbeeld via DigiD Machtigen of als bewindvoerder?"

## Slecht

> Inwoners loggen in met DigiD.

**Verwachte bevindingen:**
- Criterium 1 (externe gebruikers): twijfel — alleen inwoners. Terugvraag: "Welke externe partijen hebben toegang nodig?"
- Criterium 2 (inlogmiddel): pass — citaat: "DigiD".
- Criterium 3 (acties): fail — niet aangegeven.
- Criterium 4 (broker): fail — niet aanwezig. Veelgemaakte fout: broker niet geregeld.

## Grensgeval (hoort bij rollen-rechten)

> ### Inwoner
> **Rechten:** zaak aanmaken via verzoek, documenten aanleveren, lijstscherm inzien, procestaken uitvoeren.

**Verwachte bevindingen:**
- De review signaleert dat dit beschrijft wat de inwoner in het systeem mag (`discovery-rollen-rechten`), niet hoe de inwoner toegang krijgt.
- Criteria 2 en 4: fail — inlogmiddel en broker ontbreken.
