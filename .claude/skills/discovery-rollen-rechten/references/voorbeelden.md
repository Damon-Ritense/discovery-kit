# Voorbeelden — Rollen & rechten

<!-- Fictief, geen klantgegevens. Opgesteld door Claude, akkoord Damon. -->

## Goed

> ### Aanvrager
> **Toegang:** via klantportaal
> **Rechten:** aanvraag indienen; aanvullende stukken uploaden; status van de eigen aanvragen inzien.
>
> ### Consulent
> **Toegang:** in GZAC
> **Rechten:** aanvragen behandelen; documenten beheren; beoordeling en besluit vastleggen; notities toevoegen.
>
> ### Teamleider
> **Toegang:** in GZAC
> **Rechten:** alle rechten van de consulent; zaken toewijzen aan consulenten; dashboard doorlooptijden gebruiken.
>
> ### Functioneel beheerder
> **Toegang:** in GZAC
> **Rechten:** admin.

**Verwachte bevindingen:**
- Criterium 1 (toegang): pass voor alle rollen — citaat: "via klantportaal", "in GZAC".
- Criterium 2 (rechten): pass voor alle rollen — citaat (teamleider): "zaken toewijzen aan consulenten".

## Matig

> ### Consulent team Noord
> **Toegang:** in GZAC
> **Rechten:** aanvragen behandelen, documenten beheren.
>
> ### Consulent team Zuid
> **Toegang:** in GZAC
> **Rechten:** aanvragen behandelen, documenten beheren.
>
> ### Teamleider
> **Rechten:** zaken toewijzen.

**Verwachte bevindingen:**
- Criterium 1 (toegang): fail bij Teamleider — niet aangegeven. Terugvraag: "Waar krijgt de teamleider toegang: via het klantportaal of in GZAC?" Pass bij beide consulentrollen.
- Criterium 2 (rechten): pass — citaat: "aanvragen behandelen, documenten beheren".
- Veelgemaakte fout: te veel rollen — "Consulent team Noord" en "Consulent team Zuid" hebben dezelfde rechten. Terugvraag: "Verschillen de rechten van consulent team Noord en consulent team Zuid? Zo niet, kunnen ze één rol worden?"

## Slecht

> - Jan (teamleider): alles
> - Fatima: behandelen
> - Afdeling Financiën: inzien

**Verwachte bevindingen:**
- Criterium 1 (toegang): fail — bij geen enkele rol aangegeven.
- Criterium 2 (rechten): twijfel — citaten: "alles", "behandelen", "inzien" zijn te globaal.
- Veelgemaakte fout: rol = persoon — citaten: "Jan (teamleider)", "Fatima". Terugvraag: "'Jan (teamleider)' is een persoon. Wat doet deze rol in het systeem?"

## Grensgeval (hoort bij gebruikers)

> ### Consulent
> Beoordeelt aanvragen en stelt besluiten op. Pijnpunt: zoekt gegevens bij elkaar in drie systemen. Voordeel: minder zoekwerk.

**Verwachte bevindingen:**
- De review signaleert dat dit een gebruikersprofiel is (taken, pijnpunten, voordelen — `discovery-gebruikers`), geen beschrijving van rechten in het systeem.
- Criterium 1 (toegang): fail — niet aangegeven.
- Criterium 2 (rechten): fail — er staat wat de consulent doet, niet wat de rol in het systeem mag.
