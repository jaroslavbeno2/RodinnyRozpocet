# SC-011 Pridanie člena domácnosti
**Aktér:** hlava rodiny

**Ako** hlava rodiny **chcem** pridať nového člena do domácnosti **aby** mohol spoločne evidovať príjmy, výdavky a sledovať rozpočet domácnosti.

## Predpodmienky
- Používateľ je prihlásený a v existujúcej domácnosti má rolu hlava rodiny.

## Hlavný tok
- Používateľ zvolí "Správa domácnosti".
- Zadá údaje:
```
e-mailová adresa (alebo používateľské meno pozývaného člena): 
poznámka / prezývka v domácnosti (voliteľne):
....
```
- Používateľ klikne na tlačidlo pridať člena.
- Systém overí, či je zadaný e-mail v správnom formáte a či používateľ už nie je členom tejto domácnosti.
- Systém odošle pozvánku na zadaný e-mail (alebo priradí existujúci účet do domácnosti po jej potvrdení).
- Pozvaný používateľ potvrdí pozvánku a stane sa členom domácnosti.
- Koniec scenáru

## Alternatívne / chybové toky
- Neplatný formát e-mailovej adresy → chybová hláška. Zadajte platnú e-mailovú adresu.
- Používateľ s daným e-mailom už je členom domácnosti → chybová hláška. Používateľ už patrí do tejto domácnosti.
- Pozvaný používateľ ešte nemá vytvorený účet v systéme → systém mu odošle registračný odkaz s pozvánkou do domácnosti.


## Otvorené otázky
- Môže mať domácnosť naraz viac ako jednu hlavu rodiny alebo je táto rola priradená len jednej osobe?
