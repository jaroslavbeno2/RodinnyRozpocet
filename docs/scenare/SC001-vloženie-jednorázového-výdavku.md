# SC-001 Vloženie-jednorázového-výdavku

**Aktér:** člen domácnosti 

**Ako** člen domácnosti **chcem** nastaviť jednorázový výdavok **aby** sa pridal do výdavkov rodiny.

## Predpodmienky
- Používateľ je prihlásený a patrí do domácnosti.

## Hlavný tok
- Používateľ zvolí "Vložiť výdavok".
- Zadá údaje:
```
sumu: 50 
kategóriu: 
typ (výdavok/príjem)
druh (jednorázový, pravidelný)
dátum: aktuálny dátum (prípadne vlastný dátum)
popis / poznámka (voliteľne)
....
```
- Používateľ klikne na tlačidlo uložiť 
- Systém zistí, že ide o jednorázový výdavok ak je vybratý **typ: výdavok** a je nastavený **druh: jednorázový**
- Používateľ uloží pravidlo.
- Systém jednorázovo zapíše výdavok do výdavkov domácnosti pre zvolený dátum
- Koniec scenáru

## Alternatívne / chybové toky
- Suma ≤ 0 → chybová hláška. Suma musí byť viac ako 0.

## Otvorené otázky
- Dátum začiatku v minulosti → systém umožní zadať príjem s budúcim dátumom (napr. očakávaná výplata) alebo ho povolením obmedzí len na aktuálny/minulý dátum?