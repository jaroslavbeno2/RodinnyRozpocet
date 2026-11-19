# SC-006 Čerpanie zo sporenia

**Aktér:** člen domácnosti 

**Ako** člen domácnosti **chcem** vybrať peniaze zo sporenia **aby** som ich mohol použiť na pokrytie výdavkov.

## Predpodmienky
- Používateľ je prihlásený a patrí do domácnosti.
- Existuje aspoň jedno aktívne sporenie s nenulovým zostatkom.

## Hlavný tok
- Používateľ zvolí "Čerpať zo sporenia"
- Zadá údaje:
```
výber zo sporenia (výber cieľa/účtu): 
sumu: 50 
dátum: aktuálny dátum (prípadne vlastný dátum)
popis / poznámka (voliteľne)

```
- Používateľ klikne na tlačidlo uložiť 
- Systém overí, či je zadaná suma menšia alebo rovná aktuálnemu zostatku vo zvolenom sporení.
- Používateľ uloží transakciu.
- Systém zníži aktuálnu sumu vo zvolenom sporení o zadanú sumu a zaznamená čerpanie.
- Koniec scenáru

## Alternatívne / chybové toky
- Suma ≤ 0 → chybová hláška. Suma musí byť viac ako 0.
- Vybraná suma je vyššia ako aktuálny zostatok v sporení → chybová hláška. Nedostatočné prostriedky na sporení.

## Otvorené otázky
- Bude sa vybratá suma automaticky prevádzať do bežného rozpočtu rodiny ako príjem, alebo ide len o interný prevod zo sporenia bez vplyvu na bežné príjmy?