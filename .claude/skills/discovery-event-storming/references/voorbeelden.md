# Voorbeelden — Event Storming

<!-- Fictief, geen klantgegevens. Opgesteld door Claude, akkoord Damon.
     Een echte review werkt op een foto of export van het bord. Deze voorbeelden beschrijven wat er op de plaat te zien is,
     zodat ze ook zonder afbeelding als testinvoer bruikbaar zijn. Vervang ze door echte (geanonimiseerde) platen zodra die er zijn. -->

## Goed

> **Plaat:** `diagrams/event-storming-bijzondere-bijstand.png`
>
> **Kleurlegenda:** taak blauw, betrokkene geel, systeem roze, data groen, doorloop/wachttijd oranje, pijnpunt paars, uitdaging rood, resultaat donkerblauw.
>
> **Op de plaat, bij event "Aanvraag ontvangen":**
> - blauw: "Aanvraag registreren"
> - geel: "Medewerker intake"
> - roze: "E-mail + Excel"
> - groen: "In: aanvraagformulier en bijlagen / Uit: geregistreerde aanvraag"
> - oranje: "10 min / 2 dagen wacht"
> - paars: "Bijlagen komen los binnen, worden niet gekoppeld"
>
> **Events:** aanvraag ontvangen, aanvraag volledig verklaard, recht vastgesteld, besluit verzonden.

**Verwachte bevindingen:**
- Criterium 1 (kleurlegenda): pass — citaat: "pijnpunt paars" (afwijkend van het deck, maar vastgelegd).
- Criterium 2 (inhoud past bij kleur): pass — per kaarttype gezien: taak "Aanvraag registreren", betrokkene "Medewerker intake", systeem "E-mail + Excel", data "In: aanvraagformulier en bijlagen", doorloop "10 min / 2 dagen wacht", pijnpunt "Bijlagen komen los binnen". Alles past bij het kaarttype van de kleur.

## Matig

> **Plaat:** `diagrams/event-storming-bijzondere-bijstand.png`
>
> **Kleurlegenda:** *(niet ingevuld)*
>
> **Op de plaat, bij event "Recht vastgesteld":**
> - blauw: "Inkomen toetsen"
> - blauw: "Duurt te lang, inkomensgegevens moeten worden opgevraagd"
> - geel: "Consulent"
> - groen: "Suite"

**Verwachte bevindingen:**
- Criterium 1 (kleurlegenda): fail — niet ingevuld. Terugvraag: "Welke kleur post-it hoort bij welk kaarttype in deze sessie?"
- Criterium 2 (inhoud past bij kleur), uitgaande van de deckkleuren tot de legenda is bevestigd:
  - twijfel — citaat: "Duurt te lang, inkomensgegevens moeten worden opgevraagd" staat op blauw (taak), maar leest als pijnpunt. Terugvraag: "De post-it 'Duurt te lang…' is blauw (taak), maar de inhoud lijkt een pijnpunt. Klopt de kleur?"
  - twijfel — citaat: "Suite" staat op groen (data), maar leest als systeem. Terugvraag: "De post-it 'Suite' is groen (data), maar de inhoud lijkt een systeem. Klopt de kleur?"

## Slecht

> **Plaat:** foto van het bord, onscherp; de helft van de post-its is niet leesbaar.
>
> **Kleurlegenda:** *(niet ingevuld)*
>
> **Events:** *(niet ingevuld)*

**Verwachte bevindingen:**
- Criterium 1 (kleurlegenda): fail. Terugvraag: "Welke kleur post-it hoort bij welk kaarttype in deze sessie?"
- Criterium 2 (inhoud past bij kleur): fail — niet te beoordelen. Terugvraag: "De post-its bij <event> zijn niet leesbaar op de plaat. Wat staat erop?"

## SOLL = IST

> **Bij event "Besluit verzonden":**
> - IST, blauw: "Besluit printen en per post versturen"
> - SOLL, blauw: "Besluit printen en per post versturen vanuit Valtimo"

**Verwachte bevindingen:**
- Criterium 2: pass — beide post-its passen bij taak.
- Veelgemaakte fout: SOLL = IST. Terugvraag: "Het voorstel bij 'Besluit verzonden' lijkt gelijk aan de huidige situatie. Wat verandert er?"
