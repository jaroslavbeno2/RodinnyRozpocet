# SC-009 nastavenie mesačného limitu kategórie

**Aktér:** člen domácnosti 

**Ako** člen domácnosti **chcem** nastaviť mesačný limit pre konkrétnu kategóriu výdavkov **aby** som mal prehľad o mesačnom čerpaní v danej kategórii.

## Predpodmienky
- Používateľ je prihlásený a patrí do domácnosti.

## Hlavný tok
- Používateľ zvolí "Nastaviť mesačný limit kategórie".
- Zadá údaje:
```
kategória:
mesačný limit: 300
mesiac / obdobie: aktuálny mesiac (alebo platnosť od zvoleného mesiaca)
upozorniť: (voliteľne, napr. 80 %)
....
```
- Používateľ klikne na tlačidlo uložiť 
- Systém overí, či je zvolená kategória a či je mesačný limit platný (väčší ako 0).
- Používateľ uloží pravidlo.
- Systém uloží nastavený mesačný limit pre danú kategóriu domácnosti.
- Koniec scenáru

## Alternatívne / chybové toky
- Mesačný limit ≤ 0 → chybová hláška. Mesačný limit musí byť viac ako 0.
- Nevybratá kategória → chybová hláška. Kategória je povinná (prípadne sa dá dať aj na celkový rozpočet).
- Existujúci limit → systém ho umožní prepísať.

## Otvorené otázky
- Môže mesačné limity kategórií nastavovať a upravovať ktorýkoľvek člen domácnosti, alebo túto možnosť má iba správca / zakladateľ domácnosti?