# SK Kopřík na Jizerunu 2026

Plán štafety týmu **SK Kopřík** (Cýra, Irča, Klára, Tom, Mára) na závodě Jizerun 2026: 15 úseků, 164,3 km z Čelákovic do Smržovky.

Stránka `index.html` obsahuje:

- odhad doběhu do cíle podle startovního času,
- tabulku temp týmu (tempo po rovině + minuty navíc za stoupání),
- zjednodušenou mapu trasy,
- přehled úseků a kdo kolik běží, u každého úseku s odkazem na doporučenou cestu autem (mapy.com),
- časovou osu závodu,
- panel **Cesty autem a zastávky**: mapku cesty autem pro každý úsek s benzinkami, hospodami, restauracemi a obchody do 150 m od silnice, pruh podle kilometrů a seznam s odkazy na Google Mapy.

## Odkud jsou data

- **Délky a náročnost úseků:** [jizerun.cz/trasa](https://www.jizerun.cz/trasa/)
- **Cesty autem:** odkazy „Cesta autem na mapy.com“ ze stránek jednotlivých úseků na jizerun.cz
- **Geometrie cest autem:** výchozí a cílové body z odkazů jizerun.cz, trasa dopočtená přes OSRM (OpenStreetMap), může se mírně lišit od mapy.com
- **Zastávky:** OpenStreetMap (Overpass), stav 10/2026; zdrojová data jsou v `auto-trasy.json`
- **Převýšení úseků:** tabulka `Jizerun_komplet.xlsx`, u úseku 4 podle Tomovy trasy na [Mapy.com](https://mapy.com/s/kefecudobe)
- **Výchozí tempa:** odhady z tréninků v Garminu a Stravě (srpen–říjen 2026)

## Jak se počítá čas

Pro každý úsek:

```
čas = délka × tempo po rovině
    + (stoupání / 100 m) × minuty navíc daného běžce
    − (klesání / 100 m) × společný odpočet za klesání (výchozí 2 min)
```

Čas úseku nikdy neklesne pod 3:00/km. Úseky jdou za sebou od startovního času (výchozí 4:30), předávky jsou započítané v tempu. Převýšení se dá vypnout přepínačem.

## Poznámky

- Mapa je orientační: úseky vedou přímkou mezi stanovišti.
- Stránka vždy začíná od odhadovaných temp. Každý si je může upravit a zkoušet, ale úpravy se nikam neukládají. Po novém otevření stránky (nebo tlačítkem „Vrátit odhady“) se vrátí výchozí hodnoty.
- Stránka je responzivní a funguje na počítači, tabletu i mobilu.

## Ikona na ploše

Při přidání na plochu iPhonu (Sdílet → Přidat na plochu) se použije logo z `apple-touch-icon.png`, v prohlížeči `favicon.png`.

## Offline režim

Stránka má service worker (`sw.js`). Po prvním otevření se uloží do telefonu a z ikony na ploše se otevře i bez signálu. Když je signál, stáhne se vždy aktuální verze (při slabém signálu se po 4 s použije uložená). Odkazy na Google Mapy a mapy.com offline nefungují.
