# SC-010 Vytvorenie finančného plánu
**Aktér:** člen domácnosti 

**Ako** člen domácnosti **chcem** vytvoriť finančný plán domácnosti na zvolené obdobie **aby** som mohol vopred rozdeliť očakávané príjmy medzi plánované výdavky, limity kategórií a sporenia

## Predpodmienky
- Používateľ je prihlásený a patrí do domácnosti.

## Hlavný tok
- Používateľ zvolí "Finančný plán".
- Zadá údaje:
```
názov plánu: 
obdobie: od - do (mesačný, kvartálny, ročný alebo vlastné obdobie)
očakávané celkové príjmy: 2500
plánované výdavky podľa kategórií (napr. Bývanie: 800, Potraviny: 500, Doprava: 200)
plánovaná suma na sporenie: 400
nezaradené prostriedky: (automaticky vygenerovane - zvyšok príjmov)
....
```
- Používateľ klikne na tlačidlo uložiť 
- Systém overí, či sú vyplnené povinné údaje a či súčet plánovaných výdavkov a sporení nepresahuje očakávané príjmy.
- Systém uloží finančný plán domácnosti pre zvolené obdobie a sprístupní ho na sledovanie plnenia.
- Koniec scenáru

## Alternatívne / chybové toky
- Nevyplnený názov plánu alebo obdobie → chybová hláška. Názov plánu a obdobie sú povinné.
- Súčet plánovaných výdavkov a sporení je vyšší ako očakávané príjmy → systém zobrazí varovanie o deficitnom (zápornom) finančnom pláne a požiada o úpravu alebo potvrdenie.
- Pre zvolené obdobie už existuje aktívny finančný plán → systém ponúkne úpravu existujúceho plánu alebo jeho nahradenie novým.


## Otvorené otázky
- Môže finančný plán vytvárať a upravovať ktorýkoľvek člen domácnosti, alebo iba správca domácnosti?
- Má vytvorenie finančného plánu automaticky nastaviť alebo prepísať mesačné limity pre jednotlivé kategórie výdavkov?