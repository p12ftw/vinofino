# Vinofino

Veckans vinlådor ur Systembolagets tillfälliga sortiment. Statisk sida som publiceras med GitHub Pages.

## Filer

- `index.html` – själva sidan (design och logik, ändras sällan)
- `releases.json` – alla släpp och lådor, en post per släppdatum (`YYYY-MM-DD`)
- `favicon.svg`, `og-image.png` – ikon och delningsbild

## Uppdatera ett släpp

Lägg till eller ändra en post i `releases.json`. Ett färdigt släpp har `boxes` och `specials`;
ett kommande släpp utan lådor har bara `highlights` och visas som "Kommer snart".
Sätt `monthBest: true` på högst ett släpp per månad.

Sidan läser `releases.json` vid varje besök, så en push räcker för att uppdatera.
