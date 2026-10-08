# Winewine

Veckans vinlådor ur Systembolagets tillfälliga sortiment. Statisk sida som publiceras med GitHub Pages.

## Filer

- `index.html` – själva sidan (design och logik, ändras sällan)
- `releases.json` – alla släpp och lådor, en post per släppdatum (`YYYY-MM-DD`)
- `andra-slapp.json` – släpp utanför Systembolaget (t.ex. Caviste): säljare under `sellers`, släpp under `drops`
- `favicon.svg`, `og-image.png` – ikon och delningsbild

## Släpp utanför Systembolaget

Varje post i `drops` har `seller`, `name`, `launch` (`YYYY-MM-DDTHH:MM`, svensk tid), `url` och `intro`.
När innehållet är känt fylls `producer`, `region`, `boxPrice`, `bottles` och `wines`
(`name`, `region`, `qty`, `price`) i. Sätt `soldOut: true` när lådan är slut.
Ett kommande släpp visas tills det släppts; därefter bara i den vecka det släpptes.

## Uppdatera ett släpp

Lägg till eller ändra en post i `releases.json`. Ett färdigt släpp har `boxes` och `specials`;
ett kommande släpp utan lådor har bara `highlights` och visas som "Kommer snart".
Sätt `monthBest: true` på högst ett släpp per månad.

`wines` är hela släppet, ett objekt per vin: `artnr`, `producer`, `name`, `cat`
(Rött/Vitt/Rosé/Mousserande/Sött/Starkvin), `country`, `region`, `price`, `score`, `value`,
`bottles` och vid behov `cl`. Vilka viner som ligger i en låda räknas ut från artikelnumren.

Sidan läser `releases.json` vid varje besök, så en push räcker för att uppdatera.
