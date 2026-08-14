# Sanne Traint 🚴🏃

Speelse trainingsapp voor Sanne: weekplanning voor fietsen (2–4 uur) en
hardlopen (45–60 min). Sanne stelt zelf in hoe vaak, hoe zwaar en wat voor
soort trainingen; de app genereert elke week een gevarieerd schema.

Eén self-contained `index.html` — geen build-stap, geen dependencies.

## Lokaal bekijken

Open `index.html` in je browser, of serveer de map:

```bash
python3 -m http.server 8000
```

## Opslag & sync

- localStorage is de primaire opslag (werkt dus ook offline)
- Optioneel: sync via een privé GitHub Gist (☁️-knop in de app).
  Token met alléén `gist`-scope; op een tweede apparaat het Gist ID plakken.

## Deployment

Automatisch naar GitHub Pages bij elke push naar `main` via
`.github/workflows/deploy.yml`.

Activeren in de repo: **Settings → Pages → Source: GitHub Actions**.
