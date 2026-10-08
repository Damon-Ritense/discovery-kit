# Discovery-template — werkafspraken

Dit is het templaterepo waaruit per discovery een eigen repo wordt aangemaakt.
De repo is de bron van waarheid voor de inhoud van een discovery; de PowerPoint-decks zijn een weergave daarvan.

Plan, beslissingen en open punten: @docs/PLAN.md
Onderwerpen per deck (lees bij behoefte): docs/deck-structuur.md

## Rolverdeling

- **Damon bepaalt de inhoud van de skills**: criteria, veelgemaakte fouten, terugvragen, voorbeelden.
- **Claude bouwt de structuur**: mappen, templates, registers, skill-skeletten met lege secties.
- Verzin nooit criteria, kwaliteitsnormen of voorbeelden. Ontbreekt kennis, laat de sectie leeg met `TODO (Damon)` en meld dat.

## Spelregels

1. Commit nooit zelf. Damon bekijkt de diff in IntelliJ en commit zelf.
2. Schrijf niets naar `content/` zonder een review-uitkomst én expliciet akkoord van Damon in dezelfde sessie.
3. Zijn er open beslissingen in `docs/PLAN.md` onder "Open", vraag ze dan voordat je erop vooruitloopt.
4. Eén stap tegelijk. Begin in plan mode, stel voor wat er verandert, bouw pas na akkoord.
5. Zet geen persoonsgegevens of klantgevoelige gegevens in de repo zolang de beslissing over vertrouwelijkheid open staat.
6. Werk na elke afgeronde stap de status in `docs/PLAN.md` bij.

## Conventies

- Taal: Nederlands (content, skills, commit-berichten).
- Onderwerp-ID's in kebab-case; ze zijn de sleutel in `topics.yaml`, bestandsnamen en skillnamen.
- Skills: map `.claude/skills/discovery-<onderwerp-id>/`, met een korte `SKILL.md` en de kennis in `references/`.
- Elke skill-beschrijving bevat een regel "gebruik niet voor ..." om verwarring tussen aangrenzende onderwerpen te voorkomen.
- Reviewformaat voor alle onderwerp-skills: per criterium pass / twijfel / fail, een letterlijk citaat uit de input, en terugvragen bij gaten. Een review vult nooit zelf aan.
- Scope per onderwerp: `organisatie`, `eindgebruikers` of `technisch`. Het onderscheid tussen organisatie- en eindgebruikersdoelen is wezenlijk; behandel ze nooit als hetzelfde onderwerp.
- Het gekozen pad (Event Storming óf Functionele invulling) staat in `discovery.yaml`; onderwerpen van het andere pad zijn niet actief.
