## Kompilácia

Ak ste postupovali podľa [návodu](/qt-creator/installation.md) pri inštalácií, Qt Creator automaticky nájde všetky potrebné nástroje(kompilátor, debugger, qmake...) a vytvorí z nich použiteľné kit-y.

### Kit

Je termín, ktorý Qt Creator používa na označenie zoskupenia nástrojov slúžiacich na:
- otvorenie projektového súboru(**qmake** pre súbory **.pro**)
- kompiláciu projektu(**gcc**)
- debuggovanie(**gdb**)

V záložke Projects → Manage Kits môžete pridávať nové kity alebo upravovať existujúce. Po inštalácii by ste mali skontrolovať, že Qt Creator automaticky pripravil použiteľný kit s nástrojmi: qmake, gcc a gdb. 

![INSERT IMAGE]

> V prípade, že nebudete mať žiadny alebo chybný kit(ukazuje warning alebo error značku pri názve), skontrolujte si postup inštalácie podľa návodu a prípadne sa obrátte na cvičiaceho.

Priložené sú obrázky ukazujúce správnu konfiguráciu v jednotlivých systémoch Windows, Ubuntu, Mac OS.

![INSERT IMAGE]

### Otvorenie projektu

