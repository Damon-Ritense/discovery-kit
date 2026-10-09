# Voorbeelden — Data

<!-- Fictief, geen klantgegevens. Opgesteld door Claude, akkoord Damon. -->

## Goed

> **Verzoek:** De inwoner dient de aanvraag in via een webformulier; die komt binnen via de Objecten API. Bijlagen: bankafschriften van de laatste drie maanden en de factuur van de kosten. Naam, adres en BSN komen via DigiD.
>
> **Zaak:** Bij de start worden de gezinssamenstelling uit de BRP en het inkomen uit het eigen bijstandssysteem opgehaald. De consulent legt de beoordeling en het vastgestelde bedrag vast bij de zaak. Eén zaaktype: aanvraag bijzondere bijstand. Een nieuwe aanvraag van hetzelfde huishouden wordt gekoppeld aan eerdere zaken.
>
> **Resultaat:** Het besluit (toekenning of afwijzing, bedrag) wordt vastgelegd bij de zaak en als document gearchiveerd. Bij toekenning gaat de betaalopdracht naar het financiële systeem.
>
> **Entiteiten:**
>
> | Entiteit | Attributen |
> |---|---|
> | Aanvraag | datum, soort kosten, gevraagd bedrag, bijlagen |
> | Huishouden | leden, inkomen, adres |
> | Besluit | uitkomst, toegekend bedrag, motivering |
>
> Een zaak wordt gestart per aanvraag, niet per huishouden; het huishouden is gekoppeld aan de aanvraag.

**Verwachte bevindingen:**
- Criterium 1 (verzoek): pass — citaat: "die komt binnen via de Objecten API. Bijlagen: bankafschriften van de laatste drie maanden en de factuur van de kosten."
- Criterium 2 (zaak): pass — citaat: "de gezinssamenstelling uit de BRP en het inkomen uit het eigen bijstandssysteem opgehaald" en "Eén zaaktype: aanvraag bijzondere bijstand."
- Criterium 3 (resultaat): pass — citaat: "Het besluit (toekenning of afwijzing, bedrag) wordt vastgelegd bij de zaak en als document gearchiveerd. Bij toekenning gaat de betaalopdracht naar het financiële systeem."
- Criterium 4 (entiteiten + attributen): pass — tabel aanwezig; citaat: "Een zaak wordt gestart per aanvraag, niet per huishouden".

## Matig

> **Verzoek:** Aanvraagformulier met bijlagen.
>
> **Zaak:** De consulent beoordeelt de aanvraag en legt het besluit vast.
>
> **Resultaat:** *(leeg)*
>
> **Entiteiten:**
>
> | Entiteit | Attributen |
> |---|---|
> | Aanvraag | datum, bedrag |
> | Persoon | naam, adres |

**Verwachte bevindingen:**
- Criterium 1 (verzoek): twijfel — citaat: "Aanvraagformulier met bijlagen." Welke bijlagen en welk kanaal is niet duidelijk. Terugvraag: "Welke gegevens en documenten komen binnen bij het verzoek, en via welk kanaal?"
- Criterium 2 (zaak): twijfel — citaat: "De consulent beoordeelt de aanvraag en legt het besluit vast." Zaaktypen en opgehaalde gegevens ontbreken. Veelgemaakte fout: externe bronnen vergeten. Terugvraag: "Welke gegevens komen uit externe bronnen, zoals BRP, KvK of BAG?"
- Criterium 3 (resultaat): fail — leeg. Veelgemaakte fout: resultaat vergeten. Terugvraag: "Wat wordt er als resultaat vastgelegd, waar, en wat gebeurt er daarna mee?"
- Criterium 4 (entiteiten + attributen): twijfel — tabel aanwezig, maar niet vastgesteld op welk niveau een zaak start. Veelgemaakte fout: boom/bos open. Terugvraag: "Op welk niveau wordt een zaak gestart: per aanvraag of per persoon?"

## Slecht

> **Entiteiten:** tabel `aanvraag` (id UUID PK, bedrag DECIMAL(10,2), status VARCHAR(20), persoon_id FK).

**Verwachte bevindingen:**
- Criterium 1 (verzoek): fail — niet aanwezig.
- Criterium 2 (zaak): fail — niet aanwezig.
- Criterium 3 (resultaat): fail — niet aanwezig.
- Criterium 4 (entiteiten + attributen): twijfel — citaat: "id UUID PK, bedrag DECIMAL(10,2)". Veelgemaakte fout: te technisch. Terugvraag: "'DECIMAL(10,2)' is een technisch detail. Wat betekent het functioneel: welke gegevens zijn er nodig, en waarvoor?"

## Grensgeval (hoort bij data-architectuur)

> Aanvraag en Huishouden zijn aparte entiteiten met een eigen identificatie; een aanvraag verwijst naar precies één huishouden, een huishouden kan meerdere aanvragen hebben. Opslag in de domeinregistratie via de Objecten API.

**Verwachte bevindingen:**
- De review signaleert dat identiteit, kardinaliteit en opslag bij `discovery-data-architectuur` horen.
- Criterium 4 (entiteiten + attributen): twijfel — entiteiten genoemd, attributen ontbreken.
- Criteria 1–3: fail — verzoek, zaak en resultaat ontbreken.
