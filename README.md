# North Sun — solární kalkulačka

Veřejná kalkulačka pro klienty: zadají polohu a základní údaje o střeše,
dostanou orientační odhad výroby a odešlou poptávku.

- `index.html` — celá aplikace v jednom souboru (nepotřebuje server ani databázi)
- Interní část (ceny, kusovník, výkresy) v tomto souboru **není** a nejde z něj získat.

## Nasazení přes GitHub Pages
1. Nahrát `index.html` do repozitáře.
2. Settings → Pages → Source: *Deploy from a branch* → větev `main`, složka `/ (root)` → Save.
3. Za chvíli poběží na `https://<uživatel>.github.io/<repozitář>/`.

## Vložení do webu northsun-eu.com
```jsx
<iframe src="https://<adresa kalkulačky>" style={{width:"100%",height:"100vh",border:0}} title="Solární kalkulačka" />
```

## Kam chodí poptávky
Tlačítko „Odeslat poptávku" otevře e-mailového klienta s předvyplněnými podklady
na adresu `info@northsun-eu.com`. Na konci zprávy je kód poptávky — ten se vkládá
do interní aplikace (Projekt → *Načíst poptávku od klienta*).
