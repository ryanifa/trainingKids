# Voorstel: Sanne Traint 🚴‍♀️🏃‍♀️

Een simpele, vrolijke trainingsapp voor Sanne — fietsen en hardlopen, zonder
prestatiedruk. Zelfde technische opzet als de eigen trainingsapp (`ryanifa/Training`):
één self-contained `index.html` op GitHub Pages, opslag in een GitHub Gist met
localStorage als cache.

## Wat Sanne ziet en doet

### Weekoverzicht
Zeven dagen in beeld, per dag een kaartje: 🚴 fietsen, 🏃 lopen of 😴 rust.
Vandaag springt eruit. Tikken op een dag opent het dagschema.

### Dagschema
Opgebouwd als echte training, maar in kindertaal:

> **Warming-up** — 10 min rustig infietsen
> **Kern** — 4× 1 minuut zo hard je kan, met 2 min rust ertussen
> **Uitfietsen** — 10 min rustig naar huis

Duur in minuten, geen tempo's of hartslagzones. Niveau sturen we op duur en
gevoel ("je moet nog kunnen praten").

### Zelf instellen
Dit is Sanne's programma, dus zij kiest:
- hoe vaak per week fietsen en lopen (bijv. 2× fietsen, 1× lopen)
- niveau: rustig / gemiddeld / pittig
- type training: duur, interval, techniek/behendigheid, of "verrassing"
- op welke dagen ze wil trainen

### Weekgenerator
Op basis van de instellingen stelt de app elke week een schema samen uit een
trainingsbibliotheek, met variatie. Bevalt een training niet → husselknop voor
een alternatief.

### Afvinken & belonen
Na de training afvinken + een smiley (hoe voelde het?). Volle week = medaille
op een trofeeënpagina, plus streak-teller. Geen druk: een gemiste training is
gewoon een lege dag, geen "mislukt".

## Ideeën voor de trainingsbibliotheek
- **Fietsbingo** — kaart met opdrachtjes (door een plas, heuvel op, slalom)
- **Lantaarnpaal-interval** — sprint naar de ene paal, rustig naar de volgende
- **Ontdekkingsrit** — fiets een route die je nog nooit gereden hebt
- **Muziek-loop** — hardlopen op een liedje, wandelen bij het volgende

## Techniek (zoals de eigen trainingsapp)
- Eén self-contained `index.html`, vanilla JS, geen build-stap
- GitHub Pages deploy via GitHub Actions bij push
- PWA: manifest + iconen, zodat Sanne 'm op haar beginscherm zet
- Opslag gelaagd: **localStorage primair** (snel, offline) + **GitHub Gist sync**
  - PAT met alléén `gist`-scope, blijft in de browser (localStorage)
  - Gist ID invoeren op tweede apparaat → zelfde data op jouw telefoon én die van Sanne
- `APP_VERSION` bumpen bij elke wijziging, Nederlandse commits

## Bouwvolgorde
1. **v1** — weekoverzicht + dagschema's + afvinken + gist-sync
2. **v2** — instellingen + weekgenerator met trainingsbibliotheek
3. **v3** — medailles, streaks, smiley-log, PWA-polish

## Open vragen
1. Hoe oud is Sanne? Bepaalt toon en trainingsduur (~8 jaar → 20–30 min, ~12 jaar → tot 45 min).
2. Mag ik dezelfde look & feel als jouw app aanhouden, of juist iets speelsers/kleurrijkers voor haar?
3. Moet er een "ouder-stand" komen (bibliotheek aanpassen), of houden we alles in één simpele weergave?
