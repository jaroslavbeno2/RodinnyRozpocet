# SC-004 Vytvorenie pravidelného príjmu

**Aktér:** člen domácnosti 

**Ako** člen domácnosti **chcem** nastaviť pravidelný príjem **aby** sa zapisoval do príjmov automaticky.

## Predpodmienky
- Používateľ je prihlásený a patrí do domácnosti.

## Hlavný tok
- Používateľ zvolí "Vložiť príjem".
- Zadá údaje:
```
názov: (voliteľné)
sumu: 50 
kategóriu(zoznam pre pravidelný príjem):** napr. Potraviny, Oblečenie, Drogéria, Reštaurácie / Kaviarne, Doprava / Pohonné hmoty, Zdravie / Lekáreň, Zábava / Voľný čas, Iné
druh (jednorázový, pravidelný)
frekvencia (denný, týždenný, mesačný, ročný)
ak pravidelný: dátum trvania od
ak pravidelný: dátum trvania do
....
```
- Používateľ klikne na tlačidlo uložiť 
- Systém zistí, že ide o pravidelný príjem ak je nastavený **druh: pravidelný**
- Používateľ uloží pravidlo.
- Systém automaticky zapíše príjem do príjmov domácnosti podľa pravidiel (dátum od do, frekvencia) a do vybranej kategórie
- Koniec scenáru

## Alternatívne / chybové toky
- Suma ≤ 0 → chybová hláška. Suma musí byť viac ako 0.
- Používateľ nevyberie kategóriu zo zoznamu → kategória "Iné"
- Systém umožní zadať príjem s budúcim dátumom alebo dátumom v minulosti (napr. očakávaný alebo zabudnutý príjem).

## Otvorené otázky