# Voorstel: Sanne Traint 🚴‍♀️🏃‍♀️

Een simpele, vrolijke trainingsapp voor Sanne (24) — fietsen en hardlopen,
zonder prestatiedruk. Zelfde technische opzet als de eigen trainingsapp
(`ryanifa/Training`) maar veel compacter: één self-contained `index.html` op
GitHub Pages, opslag in een GitHub Gist met localStorage als cache.

**Besluiten (14 aug):** looptrainingen ± 45–60 min, fietsritten ± 2–4 uur,
look & feel speels en kleurrijk. v1 is gebouwd.

## Wat Sanne ziet en doet

### Weekoverzicht
Zeven dagen in beeld, per dag een kaartje: 🚴 fietsen, 🏃 lopen of 😴 rust.
Vandaag springt eruit. Tikken op een dag opent het dagschema.

### Dagschema
Opgebouwd als echte training, in gewone-mensentaal:

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

## Trainingsbibliotheek (in v1)
- **Fietsen (2–4 uur)**: rustige duurrit, duurrit met tempoblokken, intervalrit,
  klim & kracht, souplesse-rit, ontdekkingsrit, koffierit
- **Lopen (45–60 min)**: rustige duurloop, intervallen, fartlek, tempoloop,
  climaxloop, playlist-run

## Techniek (zoals de eigen trainingsapp)
- Eén self-contained `index.html`, vanilla JS, geen build-stap
- GitHub Pages deploy via GitHub Actions bij push
- PWA: manifest + iconen, zodat Sanne 'm op haar beginscherm zet
- Opslag gelaagd: **localStorage primair** (snel, offline) + **GitHub Gist sync**
  - PAT met alléén `gist`-scope, blijft in de browser (localStorage)
  - Gist ID invoeren op tweede apparaat → zelfde data op jouw telefoon én die van Sanne
- `APP_VERSION` bumpen bij elke wijziging, Nederlandse commits

## Status
**v1 gebouwd** — weekoverzicht, dagschema's, instellingen (aantallen, niveau,
type, trainingsdagen), weekgenerator met husselknop, afvinken met smiley,
streaks & medailles, confetti, en gist-sync.

Ideeën voor later: notities per training, weekterugblik, meer sessies in de
bibliotheek, seizoensvariatie (winter = korter).
