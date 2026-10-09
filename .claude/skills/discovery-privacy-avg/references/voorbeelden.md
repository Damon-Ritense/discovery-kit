# Voorbeelden — Privacy & AVG

<!-- Fictief, geen klantgegevens. Opgesteld door Claude, akkoord Damon. -->

## Goed (nieuwe klant)

> **Situatie:** Nieuwe klant, GDPR-checklist wordt ingevuld.
>
> **1a. Is het verkrijgen van toestemming duidelijk gecommuniceerd?** N.v.t.: de verwerking gebeurt op grond van een wettelijke taak van de gemeente (aanvragen bijzondere bijstand), niet op basis van toestemming.
>
> **#2. Is er sprake van bijzondere persoonsgegevens?** Ja: het BSN van de aanvrager wordt opgeslagen in het zaakdossier. Contact met de privacy officer van de gemeente is ingepland.
>
> **3g. Zijn er verwerkersovereenkomsten gesloten?** De verwerkersovereenkomst tussen de gemeente en Ritense is op 12 maart getekend en staat in het contractdossier van de gemeente. Met de hostingpartij loopt de overeenkomst nog; de projectleider van de gemeente bewaakt dit.
>
> **4a. Is er een register?** Ja, de gemeente houdt een register van verwerkingsactiviteiten bij; de verwerking voor bijzondere bijstand wordt daarin toegevoegd door de privacy officer.
>
> **5c. Hoe worden gegevens verwijderd?** Zaken worden na afloop van de bewaartermijn uit de selectielijst automatisch vernietigd via de archiefprocedure in het zaaksysteem.
>
> *(overige vragen op vergelijkbare wijze beantwoord)*

**Verwachte bevindingen:**
- Criterium 1 (situatie): pass — citaat: "Nieuwe klant, GDPR-checklist wordt ingevuld."
- Criterium 3 (elke vraag beantwoord): pass, mits de overige vragen ook beantwoord zijn.
- Criterium 4 (concreet): pass — citaat: "op 12 maart getekend en staat in het contractdossier van de gemeente".
- Criterium 5 (n.v.t. onderbouwd): pass — citaat: "N.v.t.: de verwerking gebeurt op grond van een wettelijke taak".
- Signaleren: bijzondere persoonsgegevens — citaat: "het BSN van de aanvrager wordt opgeslagen". Open punt: contact met specialist. Geen fail.

## Goed (bestaande klant)

> **Situatie:** Bestaande klant. De bestaande privacyovereenkomst met Ritense is van toepassing.

**Verwachte bevindingen:**
- Criterium 1 (situatie): pass — citaat: "Bestaande klant."
- Criterium 2 (bestaande overeenkomst vermeld): pass — citaat: "De bestaande privacyovereenkomst met Ritense is van toepassing."
- Criteria 3–5: niet van toepassing (geen checklist bij een bestaande klant).

## Matig (nieuwe klant)

> **Situatie:** Nieuwe klant.
>
> **1a. Is het verkrijgen van toestemming duidelijk gecommuniceerd?** N.v.t.
>
> **#2. Is er sprake van bijzondere persoonsgegevens?** Nee.
>
> **3g. Zijn er verwerkersovereenkomsten gesloten?** Is geregeld.
>
> **4a. Is er een register?** Ja, de gemeente heeft een register van verwerkingsactiviteiten.
>
> **5c. Hoe worden gegevens verwijderd?** *(leeg)*

**Verwachte bevindingen:**
- Criterium 1 (situatie): pass — citaat: "Nieuwe klant."
- Criterium 3 (elke vraag beantwoord): fail — 5c is leeg. Terugvraag: "Vraag 5c is nog niet beantwoord. Wat is het antwoord?"
- Criterium 4 (concreet): twijfel — citaat: "Is geregeld." Terugvraag: "Wat gebeurt er concreet? 'Is geregeld' zegt nog niet hoe het geregeld is." Veelgemaakte fout: aanname "geregeld". Terugvraag: "Is nagegaan dat de verwerkersovereenkomst er echt is, of is dat een aanname?"
- Criterium 5 (n.v.t. onderbouwd): fail — citaat: "N.v.t." Terugvraag: "Waarom is vraag 1a niet van toepassing?"

## Slecht

> **1a.** Ja.
>
> **3g.** Hebben we.
>
> **4a.** N.v.t.
>
> *(overige vragen leeg)*

**Verwachte bevindingen:**
- Criterium 1 (situatie): fail — niet vastgelegd. Terugvraag: "Gaat het om een nieuwe klant, of om een bestaande klant met een bestaande privacyovereenkomst?"
- Criterium 3 (elke vraag beantwoord): fail — de meeste vragen zijn leeg.
- Criterium 4 (concreet): fail — citaten: "Ja.", "Hebben we." Veelgemaakte fout: aanname "geregeld" bij "Hebben we."
- Criterium 5 (n.v.t. onderbouwd): fail — citaat: "N.v.t." bij 4a, zonder reden.

## Grensgeval (alleen beheerafspraken, geen checklist)

> **Privacy & AVG:** Ritense levert maandelijks een securityrapportage en patcht binnen 48 uur bij kritieke kwetsbaarheden. Incidenten worden gemeld bij de servicedesk.

**Verwachte bevindingen:**
- Overlap met beheer (bv. securitycontroles, vraag 3e) is toegestaan en wordt niet gesignaleerd. Het probleem is dat de checklist zelf ontbreekt.
- Criterium 1 (situatie): fail — niet vastgelegd.
- Criterium 3: fail — geen checklistvraag beantwoord. Terugvraag: "Gaat het om een nieuwe klant? Dan moeten de vragen uit de GDPR-checklist nog worden beantwoord."
