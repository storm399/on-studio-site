# ON studio — coming soon

Tijdelijke landingspagina voor on-studio.nl.

- Eén statisch bestand: `index.html` (inline CSS, geen build, geen dependencies)
- Fonts self-hosted in `fonts/` (Syne variable + Space Mono) — bewust geen Google Fonts CDN,
  dat is in de EU een AVG-risico omdat de bezoeker-IP naar Google gaat
- Totaal ± 60 kB, geen externe requests

## Merk
Logo, kleuren en typografie komen uit het Figma-bestand van ON studio:
ON in Syne SemiBold (letter-spacing .04em) met de aan-streep door de O in
`#19C37D`, STUDIO in Syne Regular. Achtergrond inkt `#111111`.
Corps 160/34 px en basislijnafstand 65 px zijn 1-op-1 uit de bron.

De streep is opgemeten op de letter, niet geschat: Syne SemiBold heeft een
cap-hoogte van .66em, zijstok .12em en boven/onder-stok .105em. De streep is
.11em dik, steekt .10em boven de O uit en eindigt op 50% van de cap-hoogte.
De inkeping is geen echte uitsparing maar een baan in inktkleur achter de
streep — dat werkt alleen op een egale achtergrond. Komt er ooit een foto of
verloop achter, dan moet het logo een SVG worden.

STUDIO wordt met `space-between` over de merkbreedte verdeeld in plaats van
met een vaste letter-spacing, zodat het links en rechts exact aansluit bij
elk schermformaat — ook als het merk van breedte verandert.

`punt.html` bewaart de eerdere variant met de punt als aan-teken.

## Animatie
De streep is het aan-teken: die groeit als laatste omhoog uit de O, klikt aan
op groen en blijft daarna rustig branden. `prefers-reduced-motion` en
`<noscript>` tonen direct de eindstand.

## Lokaal bekijken
    python3 -m http.server 4321

## Deploy
Render static site, root directory `.`, geen build command, publish directory `.`.
