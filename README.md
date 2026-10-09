# discovery-kit

Template voor een nieuwe discovery. Koppel er een agent (Claude Code) aan om de skills te gebruiken en input te verwerken tot discovery-documenten die met de klant gedeeld kunnen worden.

De repo is de bron van waarheid voor de inhoud van een discovery. De PowerPoint-decks in `docs/bron/` dienen als voorbeeld. Werkafspraken staan in `CLAUDE.md`, het plan en de beslissingen in `docs/PLAN.md`.

## Nieuwe discovery-repo aanmaken

Een discovery-repo bevat klantgegevens en wordt **altijd privé** aangemaakt.

Via GitHub:

1. Klik op **Use this template** → **Create a new repository**.
2. Kies bij de zichtbaarheid **Private**.

Via de CLI:

```sh
gh repo create <naam> --template Damon-Ritense/discovery-kit --private --clone
```

Vul daarna in `discovery.yaml` de klant, het bedrijfsproces en het gekozen pad in.

In dit templaterepo zelf komen geen klantgegevens.
