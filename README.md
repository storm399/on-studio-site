# ON studio — coming soon

Tijdelijke landingspagina voor on-studio.nl.

- Eén statisch bestand: `index.html` (inline CSS, geen build, geen dependencies)
- Fonts self-hosted in `fonts/` (Syne variable + Space Mono) — bewust geen Google Fonts CDN,
  dat is in de EU een AVG-risico omdat de bezoeker-IP naar Google gaat
- Totaal ± 60 kB, geen externe requests

## Merk
Logo, kleuren en typografie komen uit het Figma-bestand van ON studio:
ON. in Syne SemiBold (letter-spacing .04em), punt in aan-groen `#19C37D`,
STUDIO in Syne Regular (letter-spacing .42em). Achtergrond inkt `#111111`.
Verhoudingen zijn 1-op-1 overgenomen: 160/34 px, basislijnafstand 65 px.

## Animatie
De punt is het aan-teken: die klikt als laatste aan en blijft daarna rustig branden.
`prefers-reduced-motion` toont direct de eindstand.

## Lokaal bekijken
    python3 -m http.server 4321

## Deploy
Render static site, root directory `.`, geen build command, publish directory `.`.
