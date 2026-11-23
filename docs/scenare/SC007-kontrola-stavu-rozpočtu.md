# SC-007 Kontrola stavu rozpočtu

**Aktér:** člen domácnosti 

**Ako** člen domácnosti **chcem** skontrolovať stav rozpočtu **aby** som mal prehľad o celkových príjmoch, výdavkoch a aktuálnom zostatku rodiny.

## Predpodmienky
- Používateľ je prihlásený a patrí do domácnosti.

## Hlavný tok
- Používateľ zvolí "Kontrola stavu rozpočtu".
- Zadá údaje:
```
obdobie: aktuálny mesiac (prípadne vlastné obdobie od - do)
kategória: všetky kategórie (alebo konkrétnu kategóriu)
člen domácnosti: celá domácnosť (alebo konkrétny člen)
```
- Používateľ klikne na tlačidlo uložiť 
- Systém načíta všetky príjmy a výdavky domácnosti pre zvolené obdobie a vypočíta celkový zostatok (príjmy mínus výdavky) a čerpanie limitov
- Systém zobrazí prehľadnú tabuľku a graf aktuálneho stavu rozpočtu
- Koniec scenáru

## Alternatívne / chybové toky
- Ak pre zvolené obdobie nie sú žiadne záznamy, v grafe budú nulové hodnoty.
- Dátum "od" je neskorší ako dátum "do" → chybová hláška.

## Otvorené otázky
- Budeme zobrazovať pri stave rozpočtu aj očakávane budúce platby alebo iba tie realizvané do daného dňa?