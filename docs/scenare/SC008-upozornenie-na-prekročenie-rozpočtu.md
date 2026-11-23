# SC-008 upozornenie na prekročenie rozpočtu

**Aktér:** člen domácnosti 

**Ako** člen domácnosti **chcem** dostať upozornenie pri prekročení stanoveného rozpočtu **aby** som mal prehľad o nadmerných výdavkoch a mohol včas obmedziť ďalšie míňanie

## Predpodmienky
- Používateľ je prihlásený a patrí do domácnosti.
- Pre konkrétnu domácnosť alebo kategóriu je nastavený finančný limit na dané obdobie.

## Hlavný tok
- Používateľ zaeviduje nový výdavok v systéme.
- Systém automaticky porovná aktuálny súčet výdavkov s nastaveným limitom pre danú kategóriu alebo celkový rozpočet domácnosti:


- Systém zistí, že celkové výdavky presiahli stanovený limit (100 % rozpočtu).
- Systém vygeneruje a zobrazí upozornenie (notifikáciu) o prekročení rozpočtu členom domácnosti.
- Koniec scenáru

## Alternatívne / chybové toky
- Pre danú kategóriu alebo domácnosť nie je nastavený žiadny limit rozpočtu → upozornenie sa nevygeneruje.
- Výdavok sa blíži k limitu (80 % rozpočtu), ale ešte ho neprekročil → systém zobrazí len informatívne varovanie o blížiacom sa vyčerpaní rozpočtu.

## Otvorené otázky
- Ako bude upozornie vyzerať? Zobrazí sa len ako hláška v aplikácií alebo dostanú členovia domácnosti notifikáciu?