# Voorbeelden — Gebruikers

<!-- Fictief, geen klantgegevens. Opgesteld door Claude, akkoord Damon. -->

## Goed

> ### Aanvrager (inwoner)
> **Taken:** aanvraag bijzondere bijstand indienen; ontbrekende stukken aanleveren; besluit ontvangen.
> **Pijnpunten:** weet niet welke stukken nodig zijn; hoort weken niets over de status; moet bij elke aanvraag dezelfde gegevens opnieuw invullen.
> **Verwachte voordelen:** weet vooraf welke stukken nodig zijn; kan zelf zien hoe ver de aanvraag is; hoeft bekende gegevens niet opnieuw in te vullen.
>
> ### Consulent
> **Taken:** aanvraag beoordelen op volledigheid; recht op bijstand vaststellen; besluit opstellen.
> **Pijnpunten:** zoekt gegevens bij elkaar in drie systemen; geen overzicht van de eigen werkvoorraad.
> **Verwachte voordelen:** minder tijd kwijt aan zoeken; ziet in één oogopslag welke aanvragen het eerst moeten.
>
> ### Budgetcoach (ketenpartner)
> **Taken:** levert een budgetplan aan bij aanvragen met schulden.
> **Pijnpunten:** stuurt het plan per e-mail en weet niet of het is aangekomen.
> **Verwachte voordelen:** zekerheid dat het plan bij de juiste aanvraag terechtkomt.

**Verwachte bevindingen:**
- Criterium 1 (taken): pass voor alle profielen — citaat (aanvrager): "aanvraag bijzondere bijstand indienen".
- Criterium 2 (pijnpunten): pass voor alle profielen — citaat (consulent): "zoekt gegevens bij elkaar in drie systemen".
- Criterium 3 (verwachte voordelen): pass voor alle profielen — citaat (consulent): "minder tijd kwijt aan zoeken".
- Externe partijen zijn meegenomen (aanvrager, budgetcoach).

## Matig

> ### Consulent
> **Taken:** aanvragen afhandelen.
> **Pijnpunten:** veel handwerk.
> **Verwachte voordelen:** dashboard met werkvoorraad; koppeling met BRP.
>
> ### Teamleider
> **Taken:** werk verdelen; rapportages maken.
> **Pijnpunten:** geen overzicht van de bezetting.
> **Verwachte voordelen:** inzicht in de bezetting en de doorlooptijden.

**Verwachte bevindingen:**
- Criterium 1 (taken): twijfel bij consulent — citaat: "aanvragen afhandelen." Te globaal. Terugvraag: "Welke taken voert de consulent uit in het proces?" Pass bij teamleider.
- Criterium 2 (pijnpunten): twijfel bij consulent — citaat: "veel handwerk." Pass bij teamleider.
- Criterium 3 (verwachte voordelen): twijfel bij consulent — citaat: "dashboard met werkvoorraad; koppeling met BRP." Veelgemaakte fout: voordeel = functie. Terugvraag: "'Dashboard met werkvoorraad' is een functionaliteit. Wat levert die de consulent concreet op?" Pass bij teamleider.
- Veelgemaakte fout: externen vergeten — geen aanvrager of ketenpartner. Terugvraag: "Zijn er externe partijen die in het proces handelen, zoals de aanvrager of een ketenpartner?"

## Slecht

> ### Behandelaar
> Mag zaken aanmaken, documenten beheren en dossiers inzien.
>
> ### Raadpleger
> Mag dossiers alleen inzien.

**Verwachte bevindingen:**
- Criterium 1 (taken): fail — citaat: "Mag zaken aanmaken, documenten beheren en dossiers inzien." Veelgemaakte fout: systeemrollen. Terugvraag: "Dit beschrijft wat de behandelaar in het systeem mag. Welke taken voert de behandelaar uit in het proces?"
- Criterium 2 (pijnpunten): fail — niet aanwezig.
- Criterium 3 (verwachte voordelen): fail — niet aanwezig.
- Veelgemaakte fout: externen vergeten.

## Grensgeval (hoort bij externe-toegang)

> ### Inwoner
> Logt in op het klantportaal met DigiD en kan daar de aanvraag indienen.

**Verwachte bevindingen:**
- De review signaleert dat dit over de manier van toegang gaat (`discovery-externe-toegang`), niet over het gebruikersprofiel.
- Criterium 1 (taken): twijfel — citaat: "kan daar de aanvraag indienen."
- Criteria 2 en 3: fail — pijnpunten en verwachte voordelen ontbreken.
