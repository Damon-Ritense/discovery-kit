# Voorbeelden — Proces

<!-- Fictief, geen klantgegevens. Opgesteld door Claude, akkoord Damon. -->

## Goed

> **Procesmodel huidig:** zie `diagrams/bijzondere-bijstand-huidig.bpmn` (aangeleverd door de procesadviseur).
>
> **Procesmodel gewenst:** uitgewerkt in Valtimo Designer: <link>. Verschil met huidig: de volledigheidscheck is geautomatiseerd en de inkomenstoets haalt gegevens zelf op in plaats van ze op te vragen bij de inwoner.
>
> **Gebeurtenissen:**
>
> | Gebeurtenis | Intern/extern | Wie | Actie |
> |---|---|---|---|
> | Ontbrekende stukken | Extern | Aanvrager | Verzoek om aanvulling, zaak opschorten, na 14 dagen herinnering. |
> | Inwoner trekt aanvraag in | Extern | Aanvrager | Zaak afsluiten met resultaat "ingetrokken", bevestiging sturen. |
> | Spoedaanvraag (dreigende afsluiting energie) | Extern | Aanvrager | Zaak krijgt prioriteit, teamleider krijgt melding, besluit binnen 2 werkdagen. |

**Verwachte bevindingen:**
- Criterium 1 (huidig model): pass — citaat: "zie `diagrams/bijzondere-bijstand-huidig.bpmn`".
- Criterium 2 (gewenst model): pass — citaat: "uitgewerkt in Valtimo Designer".
- Criterium 3 (gebeurtenissen + wie + actie): pass — citaat: "Spoedaanvraag (dreigende afsluiting energie) | Extern | Aanvrager | Zaak krijgt prioriteit".

## Matig

> **Procesmodel huidig:** BPMN-model aangeleverd (bijlage).
>
> **Procesmodel gewenst:** gelijk aan het huidige proces, maar dan in Valtimo.
>
> **Gebeurtenissen:**
>
> | Gebeurtenis | Intern/extern | Wie | Actie |
> |---|---|---|---|
> | Bezwaar | Extern | Inwoner | |
> | Ziekte behandelaar | Intern | Teamleider | Werk herverdelen. |

**Verwachte bevindingen:**
- Criterium 1 (huidig model): pass — citaat: "BPMN-model aangeleverd (bijlage)."
- Criterium 2 (gewenst model): twijfel — citaat: "gelijk aan het huidige proces, maar dan in Valtimo." Veelgemaakte fout: huidig = gewenst. Terugvraag: "Het gewenste proces lijkt gelijk aan het huidige. Wat wordt er verbeterd?"
- Criterium 3 (gebeurtenissen + wie + actie): twijfel — citaat: "Bezwaar | Extern | Inwoner |" zonder actie. Terugvraag: "Wie is betrokken bij bezwaar, en welke actie volgt?"

## Slecht

> **Proces:** Aanvraag komt binnen → consulent beoordeelt → besluit → betaling.

**Verwachte bevindingen:**
- Criterium 1 (huidig model): fail — geen model of verwijzing. Terugvraag: "Is er een procesmodel van de huidige situatie, of waar staat het?"
- Criterium 2 (gewenst model): fail — niet uitgewerkt, geen link.
- Criterium 3 (gebeurtenissen): fail — niet aanwezig. Veelgemaakte fout: alleen happy flow. Terugvraag: "Wat gebeurt er als het niet volgens de standaardroute loopt, bijvoorbeeld als er stukken ontbreken?"

## Grensgeval (hoort bij event-storming)

> **Event: aanvraag volledig verklaard.** IST: consulent controleert handmatig, 30 minuten, 3 dagen wachttijd. SOLL: geautomatiseerde check met business rules. Pijnpunt: iedere consulent interpreteert "volledig" anders.

**Verwachte bevindingen:**
- De review signaleert dat dit de uitwerking van een event uit de sessie is (`discovery-event-storming`), niet het uitgewerkte proces.
- Criteria 1–3: fail — huidig model, gewenst model en gebeurtenissen ontbreken. Terugvraag: "Is de uitkomst van de Event Storming al vertaald naar het huidige en gewenste procesmodel?"
