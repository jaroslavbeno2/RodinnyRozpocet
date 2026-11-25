# SC-001 Vloženie-jednorázového-výdavku

**Aktér:** člen domácnosti 

**Ako** člen domácnosti **chcem** nastaviť jednorázový výdavok **aby** sa pridal do výdavkov rodiny.

## Predpodmienky
- Používateľ je prihlásený a patrí do domácnosti.

## Hlavný tok
- Používateľ zvolí "Vložiť výdavok".
- Zadá údaje:
```
názov: (voliteľné)
sumu: 50 
kategóriu(zoznam pre jednorázový výdavok):** napr. Potraviny, Oblečenie, Drogéria, Reštaurácie / Kaviarne, Doprava / Pohonné hmoty, Zdravie / Lekáreň, Zábava / Voľný čas, Iné
druh (jednorázový, pravidelný)
dátum: aktuálny dátum (prípadne vlastný dátum)
popis / poznámka (voliteľne)
....
```
- Používateľ klikne na tlačidlo uložiť 
- Systém zistí, že ide o jednorázový výdavok ak je nastavený **druh: jednorázový**
- Používateľ uloží záznam
- Systém jednorázovo zapíše výdavok do výdavkov domácnosti pre zvolený dátum a vybranú kategóriu
- Koniec scenáru

## Alternatívne / chybové toky
- Suma ≤ 0 → chybová hláška. Suma musí byť viac ako 0.
- Používateľ nevyberie kategóriu zo zoznamu → kategória "Iné"
- Systém umožní zadať výdavok s budúcim dátumom alebo dátumom v minulosti (napr. očakávaný alebo zabudnutý výdavok).

## Otvorené otázky