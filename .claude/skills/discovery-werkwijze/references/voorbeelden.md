# Voorbeelden — Werkwijze

<!-- Fictief, geen klantgegevens. Opgesteld door Claude, akkoord Damon. -->

## Goed

> **MVP:** Inwoners kunnen een aanvraag bijzondere bijstand digitaal indienen; behandelaars handelen de aanvraag af in het zaaksysteem tot en met het besluit. Koppelingen met het financiële systeem volgen na de MVP.
>
> **Sprintvariant:** A, testen na de sprint.
>
> **Betrokkenheid:** besproken met de klant en akkoord: ja.
>
> | Rol | Uren per sprint |
> |---|---|
> | Interne project owner | 4 |
> | Subject Matter Experts | 6 |
> | Eindgebruikers | 2 |
> | Functioneel beheerder | 3 |

**Verwachte bevindingen:**
- Criterium 1 (MVP): pass — citaat: "Inwoners kunnen een aanvraag bijzondere bijstand digitaal indienen".
- Criterium 2 (sprintvariant): pass — citaat: "A, testen na de sprint."
- Criterium 3 (uren + akkoord): pass — citaat: "besproken met de klant en akkoord: ja", alle vier de rollen hebben uren.

## Matig

> **MVP:** Het volledige proces bijzondere bijstand, inclusief koppeling met het financiële systeem, rapportages en het klantportaal.
>
> **Sprintvariant:** B.
>
> **Betrokkenheid:** besproken met de klant en akkoord: *(leeg)*
>
> | Rol | Uren per sprint |
> |---|---|
> | Interne project owner | 2–4 |
> | Subject Matter Experts | 4–8 |
> | Eindgebruikers | 1–3 |
> | Functioneel beheerder | 2–4 |

**Verwachte bevindingen:**
- Criterium 1 (MVP): twijfel — citaat: "Het volledige proces bijzondere bijstand, inclusief koppeling met het financiële systeem, rapportages en het klantportaal." Veelgemaakte fout: te ruime MVP. Terugvraag: "Wat is de kleinste versie die al waarde oplevert?"
- Criterium 2 (sprintvariant): pass — citaat: "B."
- Criterium 3 (uren + akkoord): fail — uren zijn de bandbreedtes uit de standaard en akkoord is niet ingevuld. Veelgemaakte fout: uren niet besproken. Terugvraag: "Zijn deze uren met de klant besproken, en is de klant akkoord?"

## Slecht

> **MVP:** Nog te bepalen.
>
> **Sprintvariant:** A of B, afhankelijk van de beschikbaarheid van testers.
>
> | Rol | Uren per sprint |
> |---|---|
> | Interne project owner | onbekend |
> | Subject Matter Experts | |

**Verwachte bevindingen:**
- Criterium 1 (MVP): fail — citaat: "Nog te bepalen." Terugvraag: "Wat zit er in de MVP?"
- Criterium 2 (sprintvariant): fail — citaat: "A of B, afhankelijk van de beschikbaarheid van testers." Terugvraag: "Welke sprintvariant is gekozen?"
- Criterium 3 (uren + akkoord): fail — citaat: "onbekend"; eindgebruikers en functioneel beheerder ontbreken; geen akkoord. Veelgemaakte fout: rollen niet belegd. Terugvraag: "Wie vult aan klantzijde de rol interne project owner in?"

## Grensgeval (hoort bij beheer)

> **Werkwijze:** Na livegang meldt de functioneel beheerder incidenten bij de Ritense-servicedesk; releases worden maandelijks uitgerold.

**Verwachte bevindingen:**
- De review signaleert dat dit over afspraken na oplevering gaat (`discovery-beheer`), niet over de werkwijze tijdens het traject.
- Criteria 1–3: fail — MVP, sprintvariant en uren ontbreken.
