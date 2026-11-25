# SC-002 Vytvorenie pravidelného výdavku

**Aktér:** člen domácnosti 

**Ako** člen domácnosti **chcem** nastaviť pravidelný výdavok **aby** sa zapisoval do výdavkov automaticky.

## Predpodmienky
- Používateľ je prihlásený a patrí do domácnosti.

## Hlavný tok
- Používateľ zvolí "Vložiť výdavok".
- Zadá údaje:
```
názov: (voliteľné)
sumu: 50 
kategóriu(zoznam pre pravidelný výdavok):** napr. Potraviny, Oblečenie, Drogéria, Reštaurácie / Kaviarne, Doprava / Pohonné hmoty, Zdravie / Lekáreň, Zábava / Voľný čas, Iné
druh (jednorázový, pravidelný)
frekvencia (denný, týždenný, mesačný, ročný)
ak pravidelný: dátum trvania od
ak pravidelný: dátum trvania do
....
```
- Používateľ klikne na tlačidlo uložiť 
- Systém zistí, že ide o pravidelný výdavok ak je nastavený **druh: pravidelný**
- Používateľ uloží pravidlo.
- Systém automaticky zapíše výdavok do výdavkov domácnosti podľa pravidiel (dátum od do, frekvencia) a do vybranej kategórie
- Koniec scenáru

## Alternatívne / chybové toky
- Suma ≤ 0 → chybová hláška. Suma musí byť viac ako 0.
- Používateľ nevyberie kategóriu zo zoznamu → kategória "Iné"
- Systém umožní zadať výdavok s budúcim dátumom alebo dátumom v minulosti a dogeneruje (napr. očakávaný alebo zabudnutý výdavok).

## Otvorené otázky