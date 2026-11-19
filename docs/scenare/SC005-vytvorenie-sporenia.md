# SC-005 Vytvorenie sporenia

**Aktér:** člen domácnosti 

**Ako** člen domácnosti **chcem** vytvoriť nové sporenie **aby** som si odkladal peniaze na zvolený cieľ.

## Predpodmienky
- Používateľ je prihlásený a patrí do domácnosti.

## Hlavný tok
- Používateľ zvolí "Vytvoriť sporenie"
- Zadá údaje:
```
názov sporenia: 
cieľová suma: 1000 (voliteľné)
aktuálna suma / počiatočný vklad: 0
cieľový dátum (voliteľné)
kategória / účet

```
- Používateľ klikne na tlačidlo uložiť 
- Systém overí, či sú vyplnené povinné údaje a či je cieľová suma platná, prípadne vypočíta mesačnú čiastku, ak máme cieľový dátum.
- Používateľ uloží pravidlo.
- Systém vytvorí a uloží nové sporenie do zoznamu sporení domácnosti.
- Koniec scenáru

## Alternatívne / chybové toky
- Suma ≤ 0 → chybová hláška. Suma musí byť viac ako 0.
- Nevyplnený názov sporenia → chybová hláška. Názov sporenia je povinný.

## Otvorené otázky
- Bude možné k sporeniu priradiť automatické mesačné príspevky alebo sa čiastky budú pridávať iba manuálne?