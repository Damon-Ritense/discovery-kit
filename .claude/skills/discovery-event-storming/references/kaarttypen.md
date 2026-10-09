# Event Storming — uitleg en kaarttypen

<!-- Bron: functioneel deck, slides 17–19. -->

## Waarom Event Storming? (slide 17)

Met Event Storming kunnen we op een interactieve wijze een groot aantal onderwerpen in één keer in kaart brengen: gebruikers, processen, data, systemen, pijnpunten en meer. Het doel van de sessie is het in beeld krijgen van de huidige situatie, zodat we op basis van kennis en ervaring uit de praktijk de verbeteringen kunnen vinden voor een efficiënter en gestroomlijnder proces.

Een belangrijk aspect is het interactieve karakter: de deelnemers komen zelf met de invulling van de events en alle gerelateerde aspecten. Dit zorgt ervoor dat de huidige situatie zo realistisch mogelijk wordt afgebeeld, waardoor de kansen voor verbeteringen beter naar voren komen.

## De 8 kaarttypen (slide 18)

| Kaarttype | Betekenis | Kleur in het deck |
|---|---|---|
| Taak | De activiteit die wordt uitgevoerd (IST); herontworpen versie door de BPE. | blauw |
| Betrokkene | Wie de taak nu uitvoert of daarvoor verantwoordelijk is. | geel |
| Systeem | Het systeem of de plug-in die nu bij deze taak hoort. | roze |
| Data (in/uit) | Gegevens nodig om te starten, en gegevens die daarna beschikbaar zijn. | groen |
| Doorloop/wachttijd | Bewerkingstijd van de taak plus de wachttijd die erna optreedt. | oranje |
| Pijnpunt | Wat hier niet goed gaat. | donkergrijs |
| Uitdaging | BPE-oplossing bestaat nog niet als standaard Valtimo/GZAC-functionaliteit. | rood |
| Resultaat | De uitkomst van de gehele flow. | donkerblauw |

**Let op:** de kleuren in de sessie kunnen verschillen van het deck, afhankelijk van de beschikbare post-its. Gebruik de kleurlegenda van de sessie (in de content), en valideer die met de uitvoerder als hij ontbreekt of niet klopt met de plaat.

## Uitwerking van een event (slide 19, VOORBEELD)

**Event:** aanvraag volledig verklaard.

**Pijnpunt:** iedere medewerker hanteert een eigen interpretatie van "volledig"; dit leidt tot inconsistente beoordeling en onnodige retourzendingen.

| Kaarttype | Huidige situatie (IST) | Voorstel (SOLL) |
|---|---|---|
| Taak | Aanvraag handmatig controleren op volledigheid | Geautomatiseerde volledigheidscheck op basis van vastgelegde business rules |
| Betrokkene | Intake-medewerker | — (ongewijzigd) |
| Systeem | E-mail / papieren checklist | Valtimo business rule task (DMN) + Formio-validatie |
| Data (in/uit) | In: ingevulde aanvraag — Uit: volledig/onvolledig-oordeel | In: ingevulde aanvraag — Uit: automatisch oordeel + evt. aanvullingsverzoek |
| Doorloop/wachttijd | 30 min proces / 3 dagen wacht | 2 min proces / 0 dagen wacht |
