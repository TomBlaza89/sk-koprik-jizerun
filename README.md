# SK Kopřík na Jizerunu 2026

Plán štafety týmu **SK Kopřík** (Cýra, Irča, Klára, Tom, Mára) na závodě Jizerun 2026: 15 úseků, 164,3 km z Čelákovic do Smržovky.

Stránka `index.html` obsahuje:

- odhad doběhu do cíle podle startovního času,
- tabulku temp týmu (tempo po rovině + minuty navíc za stoupání),
- zjednodušenou mapu trasy,
- přehled úseků a kdo kolik běží,
- časovou osu závodu.

## Odkud jsou data

- **Délky a náročnost úseků:** [jizerun.cz/trasa](https://www.jizerun.cz/trasa/)
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
- Na GitHub Pages si každý mění tempa jen pro sebe a po obnovení stránky se vrátí výchozí hodnoty. Sdílené ukládání pro celý tým funguje jen ve verzi na claude.ai.
