# vangoghslogs.damonia.com

De productpagina van Van Gogh's Logs: startpagina, privacybeleid en supportpagina, in het
Nederlands en het Engels. Statisch: HTML, één stylesheet en het app-icoon. Geen scripts,
geen trackers, geen cookies.

Apple vraagt bij het inzenden om:

- `https://vangoghslogs.damonia.com/privacy.html`
- `https://vangoghslogs.damonia.com/support.html`

## Publiceren

GitHub is de bron, Plesk haalt op. Bij elke push naar `main` roept GitHub een webhook van
Plesk aan; Plesk doet een `git pull` in de map van het subdomein. Zelfde opzet als
netwerk.damonia.com.

```
git add -A && git commit -m "…" && git push
```

## Let op

- Plesk zet de hele repo in de webmap; dit bestand is dus ook openbaar.
- Verandert er iets in wat de app met gegevens doet (een nieuwe toestemming, een
  netwerkverzoek), pas dan `privacy.html` én `privacy-en.html` aan, met nieuwe datum.
- Zodra de app in de winkel staat: een downloadknop op de startpagina met de echte link.
