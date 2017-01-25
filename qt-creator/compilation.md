## Kompilácia {#intro}

Ak ste postupovali podľa [návodu](/qt-creator/installation.md) pri inštalácií, Qt Creator automaticky nájde všetky potrebné nástroje(kompilátor, debugger, qmake...) a vytvorí z nich použiteľné kit-y.

### Kit {#kit}

Je termín, ktorý Qt Creator používa na označenie zoskupenia nástrojov slúžiacich na:
- otvorenie projektového súboru(**qmake** pre súbory **.pro**)
- kompiláciu projektu(**gcc/MinGW**)
- debuggovanie(**gdb**)

V menu **Tools → Options → Build & Run** môžete pridávať nové kit-y alebo upravovať existujúce. Po inštalácii by ste mali skontrolovať, že Qt Creator automaticky pripravil použiteľný kit s nástrojmi: gcc/MinGW a gdb. 

![](/images/qt-creator/setup_01.png)

> V prípade, že nebudete mať žiadny alebo chybný kit(ukazuje warning alebo error značku pri názve), skontrolujte si postup inštalácie podľa návodu a prípadne sa obráťte na cvičiaceho.

Priložené sú obrázky ukazujúce správnu konfiguráciu v jednotlivých systémoch Windows, Ubuntu, Mac OS.

![](/images/qt-creator/setup_02.png)

### Otvorenie projektu {#open}

Ak ste nechali v inštalácii zaškrtnutú možnosť *Associate common file types with Qt Creator*(odporúčana možnosť v návode), stačí kliknúť na **.pro** súbor pre otvorenie. V opačnom prípade sa dá použiť **File → Open Project...**. Po otvorení je projekt nájditeľný aj vo *Welcome* obrazovke Qt Creatora v kategórii *Recent Projects*. 

![](/images/qt-creator/open_01.png)

Pri otváraní sa Qt Creator opýta, ktoré kit-y chcete použiť na prácu. Vystačíte si s jediným vyššie spomenutým.

![](/images/qt-creator/open_02.png)

### Spustenie {#run}

Pred spustením si skontrolujte nastavenie *Run in terminal* v **Projects → Run**. Toto nastavenie je vhodné na testovanie aplikácie, tak ako sa reálne mimo editora spustí. Spúšťanie v editore je niekedy neprehľadné a nepraktické, hlavne pri zadávaní vstupu.

![](/images/qt-creator/open_03.png)

Následne stačí kliknúť na ikonku spustenia/kompilácie. Pri spustení sa automaticky skompilujú zmeny prevedené od poslednej kompilácie. Ak nastanú pri kompilácii chyby, budú zobrazené v okne **4 Compile Output**. Pri dvojitom kliknuti na jednotlivé chybové hlášky budete presmerovaný na súbor a riadok, kde kompilačná chyba nastala.

![](/images/qt-creator/compile_01.png)

## Kam ďalej {#next}

Po úspešnom prejdení tohoto návodu pokračujte [debuggovaním aplikácie](/qt-creator/debug.md) a [vytvorením nového projektu](/qt-creator.create.md) pre hw0x.