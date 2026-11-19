# SC-004 Vytvorenie pravidelného príjmu

**Aktér:** člen domácnosti 

**Ako** člen domácnosti **chcem** nastaviť pravidelný príjem **aby** sa zapisoval do príjmov automaticky.

## Predpodmienky
- Používateľ je prihlásený a patrí do domácnosti.

## Hlavný tok
- Používateľ zvolí "Vložiť príjem".
- Zadá údaje:
```
sumu: 50 
kategóriu: 
typ (výdavok/príjem)
druh (jednorázový, pravidelný)
frekvencia (denný, týždenný, mesačný, ročný)
ak pravidelný: dátum trvania od
ak pravidelný: dátum trvania do
....
```
- Používateľ klikne na tlačidlo uložiť 
- Systém zistí, že ide o pravidelný príjem ak je vybratý **typ: náklad** a je nastavený **druh: pravidelný**
- Používateľ uloží pravidlo.
- Systém automaticky zapíše príjem do príjmov domácnosti podľa pravidiel (dátum od do, frekvencia)
- Koniec scenáru

## Alternatívne / chybové toky
- Suma ≤ 0 → chybová hláška. Suma musí byť viac ako 0.

## Otvorené otázky
- Dátum začiatku v minulosti → systém dogeneruje zmeškané príjmy alebo dá chybovú hlášku?