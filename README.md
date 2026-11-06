# Výsledkovo

Aplikácia na organizovanie amatérskych aj profesionálnych turnajov a líg a na živé zadávanie a zverejňovanie výsledkov. Spája organizátorov, rozhodcov, zapisovateľov, trénerov, hráčov, rodičov a fanúšikov – každý vidí a mení len to, na čo má právo.

Tento repozitár zatiaľ obsahuje len zadanie. **Podklady popisujú, ČO má aplikácia robiť, nie AKO** – technické riešenie navrhuje programátor.

## Funkčný podklad

Celý podklad je v dokumente [Výsledkovo – funkčný podklad](https://claude.ai/artifact/HbKDjXvCzsr5sz996uAEmP). Obsahuje záložky:

| Záložka | Čo v nej je |
| --- | --- |
| Vízia, rozsah a roly | MVP vs. neskôr, roly, matica práv, ochrana údajov maloletých, rozhodnutia a otvorené otázky |
| Hlavné toky | vytvorenie podujatia, registrácia tímu, rozpis, zápas, tabuľka a tresty, play-off |
| Pravidlá výpočtov | body, tabuľka, kritériá pri rovnosti bodov, štatistiky, tresty, postup do play-off; overené podľa predpisov SFZ |
| User stories | 50 stories v 8 moduloch s akceptačnými kritériami |
| GitHub issues – návrh | text, z ktorého vznikli issues v tomto repozitári |
| Poradie vývoja | 7 fáz a ich závislosti |
| Otázky pre právnika | GDPR a súhlasy maloletých |

## Rozsah MVP

- Slovenský trh, slovenčina, šport futbal a futsal (ďalšie športy neskôr).
- Formáty: jednodňový turnaj (skupiny + play-off), sezónna liga každý s každým, viac kategórií v jednom podujatí.
- Roly s vlastným účtom: organizátor, spoluorganizátor (nastaviteľné práva), rozhodca, zapisovateľ, tréner/vedúci tímu, hráč, rodič. Verejnosť bez prihlásenia.
- Výsledok platí hneď; opravuje len organizátor s dôvodom a históriou. Zadávanie funguje aj offline.
- Verejná stránka, režim pre TV v hale, katalóg turnajov, sledovanie tímu s upozorneniami.
- Maloletí hráči sú bez súhlasu verejne len v minimálnom režime (meno, iniciála priezviska, číslo dresu).
- MVP je bezplatné.

## Ako sú organizované issues

- **Epiky** M1–M8 (štítok `epic`) – každý obsahuje zoznam svojich issues.
- **Issues** US-Mx-yy – jedna user story s rozsahom a akceptačnými kritériami.
- **Míľniky** F1–F7 – poradie vývoja:

| Míľnik | Obsah | Výsledok |
| --- | --- | --- |
| F1 Základ | účty, pozvánky, podujatie, kategórie, ihriská | organizátor založí podujatie |
| F2 Tímy a súpisky | registrácia tímov, súpisky, oprávnenosť, minimálne zobrazenie maloletých | tímy so súpiskami |
| F3 Rozpis | skupiny, rozpis, rozhodcovia | zverejnený rozpis |
| F4 Zápas a tabuľka | zadávanie výsledkov, tabuľky, verejná stránka | **prvý použiteľný jednodňový turnaj** |
| F5 Play-off, tresty, štatistiky | pavúk, tresty podľa SFZ, štatistiky, zápis, offline | turnaj aj liga kompletne |
| F6 Súhlasy a GDPR | súhlasy rodičov a trénerov | začať až po stanovisku právnika |
| F7 Diváci a pohodlie | TV v hale, katalóg, upozornenia, spoluorganizátori, šablóny | MVP kompletné |

- **Štítky:** `mvp`, `modul:M1`–`modul:M8`, `gdpr` (údaje hráčov a súhlasy), `analýza` (issue obsahuje `[DOPLNIŤ]` – treba doriešiť pred alebo počas vývoja).

## Konvencie

- Všetko je po slovensky.
- `[DOPLNIŤ]` označuje neoverenú alebo nerozhodnutú vec – nevymýšľať, opýtať sa.
- Pravidlá súťaží vychádzajú zo [Súťažného poriadku futbalu SFZ (2025)](https://mediamanager.ws/media/pages/f/futbalsfz.sk/2025/06/sutazny-poriadok-futbalu-sfz-konsolidovane-znenie-2025-1.pdf) a [Disciplinárneho poriadku SFZ (2019)](https://mediamanager.sportnet.online/media/pages/f/futbalsfz.sk/2019/08/132b9cc6-d0f6-42a8-8d29-ac871ac401e9.pdf); organizátor ich v aplikácii môže upraviť.
- Inšpirácia: [Tournify](https://tournifyapp.com) – porovnávame len funkcie, dizajn ani texty nepreberáme.
