# SC-002 Vytvorenie pravidelného výdavku

**Aktér:** člen domácnosti 

**Ako** člen domácnosti **chcem** nastaviť pravidelný výdavok **aby** sa zapisoval do výdavkov automaticky.

## Predpodmienky
- Používateľ je prihlásený a patrí do domácnosti.

## Hlavný tok
- Používateľ zvolí "Vložiť výdavok".
- Zadá údaje:
```
sumu: 50 
kategóriu: 
typ (náklad/príjem)
druh (jednorázový, pravidelný)
frekvencia (denný, týždenný, mesačný, ročný)
ak pravidelný: dátum trvania od
ak pravidelný: dátum trvania do
....
```
- Používateľ klikne na tlačidlo uložiť 
- Systém zistí, že ide o pravidelný náklad ak je vybratý **typ: náklad** a je nastavený **druh: pravidelný**
- Používateľ uloží pravidlo.
- Systém automaticky zapíše výdavok do výdavkov domácnosti podľa pravidiel (dátum od do, frekvencia)
- Koniec scenáru

## Alternatívne / chybové toky
- Suma ≤ 0 → chybová hláška. Suma musí byť viac ako 0.

## Otvorené otázky
- Dátum začiatku v minulosti → systém dogeneruje zmeškané výdavky alebo dá chybovú hlášku?