# Definition of Done — discovery

Een discovery is done wanneer alle verplichte onderdelen zijn ingevuld. Wat verplicht is, bepaalt grotendeels de uitvoerder van de discovery. Een paar standaarden gelden altijd.

## Niveaus

Per onderwerp staat het niveau in `topics.yaml` (veld `dod`).

| Niveau | Betekenis |
|---|---|
| `verplicht` | Moet ingevuld zijn. Kan niet worden overruled. |
| `sterke-voorkeur` | Hier wordt actief op gestuurd, maar de uitvoerder mag overrulen. Een overrule wordt vastgelegd in `discovery.yaml` (status `overruled` plus `reden`). |

## Standaarden

- **Privacy & AVG** (`privacy-avg`) moet ingevuld zijn: verplicht.
  - Nieuwe klant (`nieuwe-klant: ja`): de GDPR-checklist is volledig ingevuld.
  - Bestaande klant met bestaande afspraken (`nee`): een verwijzing naar de bestaande privacyovereenkomst is voldoende.
- **Beheerafspraken** (`beheer`) moeten altijd vastgelegd zijn: verplicht.
- **Organisatorische en functionele discovery:** sterke voorkeur om alle onderdelen in te vullen.
  - De losse functionele onderwerpen gelden altijd, ongeacht het gekozen pad. Bij Event Storming vult de uitkomst daarvan deze onderwerpen.
  - `event-storming` zelf telt alleen mee als daarvoor gekozen is (`pad` in `discovery.yaml`).
- **Technische discovery:**
  - Bij een nieuwe technische koppeling (`nieuwe-technische-koppeling: ja`): sterke voorkeur om het technische deel goed uit te werken.
  - Bij een bestaande klant met een bestaande omgeving waarin niets verandert (`nee`): het technische deel is niet nodig, behalve `beheer`.

## Alleen actieve onderwerpen tellen

Een onderwerp telt alleen mee als zijn `applies_when` in `topics.yaml` waar is voor deze discovery.

## Voortgang

De voortgang per onderwerp en de open punten staan in `status.md`, gegenereerd door de skill `discovery-status`.
