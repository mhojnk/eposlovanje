# Terminko — lokalna spletna stran

Preprosta statična spletna stran brez gradnje ali zunanjih programskih paketov. Za lokalni ogled odpri `index.html` v brskalniku. Strani uporabljajo skupno datoteko `styles.css` in majhno skripto `script.js` za mobilno navigacijo.

## Strani

- `index.html` — domov
- `cenik.html` — možnosti in označbe za cene, ki jih je treba dopolniti
- `kontakt.html` — kontaktni podatki in še neaktivni obrazec

## Pred objavo

- Vnesi dejansko e-pošto in telefonsko številko v `kontakt.html` ter pravilna `mailto:` in `tel:` cilja.
- Poveži obrazec v `kontakt.html` s storitvijo za pošiljanje; šele nato odstrani obvestilo in omogoči gumb.
- Predstavljen okvirni cenik je 30 €/mesec za enega izvajalca, 50 €/mesec za več zaposlenih in začetna postavitev od 120 € enkratno. SMS-količina še ni določena; nova spletna stran se oceni posebej.
- Po želji dodaj URL spletne trgovine in druge končne kontaktne oziroma pravne podatke.
- Pisavi DM Sans in Manrope se trenutno nalagata iz Google Fonts. Če želiš popolnoma lokalno delovanje, ju zamenjaj s sistemskima pisavama ali dodaj lokalne datoteke pisav z ustrezno licenco.

## Lokalni predogled

V mapi projekta lahko zaženeš preprost lokalni strežnik:

```powershell
python -m http.server 8000
```

Nato obišči `http://localhost:8000`.

## Objavljanje prek GitHub in Cloudflare Pages

Ko bo lokalni videz potrjen:

1. Ustvari GitHub repozitorij in potisni te datoteke v vejo, ki jo želiš objavljati.
2. V Cloudflare Pages izberi **Create a project** in poveži GitHub repozitorij.
3. Izberi **None** kot prednastavitev ogrodja. Ukaz za gradnjo lahko pustiš prazen (če ga obrazec zahteva, uporabi `exit 0`), izhodni imenik pa nastavi na `.` — korensko mapo repozitorija, kjer so `index.html`, `cenik.html`, `kontakt.html`, `styles.css` in `script.js`. Root directory pusti prazen.
4. Shrani nastavitve in sproži prvo objavo. Pri naslednjih potiskih v povezano vejo bo Cloudflare Pages pripravil novo objavo.

Pred prvo objavo še enkrat preveri vse označbe za dopolnitev in delovanje kontaktnega obrazca.
