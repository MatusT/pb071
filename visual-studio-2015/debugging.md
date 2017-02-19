# Debugging

Pre vysvetlenie konceptov je dobré si pozrieť [Debugging v Qt Creatore](../qt-creator/debugging.md). Tu už iba zhrnieme možnosti.

Spustením programu cez možnosť **Local Windows Debugger** sa program spustí v móde na debuggovanie. **Breakpoint*y môžete pridávať kliknutím vedľa čísla riadku kódu.

V dolnej časti sa objavia dva panely. V prvom sa dá prepináť medzi:
- **Autos** - premenné, ktorých hodnotu automaticky VS zachytilo a môže sa Vám hodiť
- **Locals** - premenné, ktoré su len v lokálnom rozmedzí - napríklad ak breakpoint je vo funkcii, uvidíte v tomto okne len premenné, ktoré su na stacku v tejto funkcii
- **Watch** - v tomto okne môžete napísať názvy premenných, ktorých hodnotu chcete vedieť počas celej doby debuggovania

V druhom okne sa nachádza:
- **Call Stack** - zoznam volaní, ktoré boli vykonané aby sa program dostal do zastaveného bodu
- **Breakpoints** - zoznam všetkých breakpointov v programe. Tu môžete pridávať aj breakpointy so zložitejšími podmienkami(viď [Debugging v Qt Creatore](../qt-creator/debugging.md))

![](/images/visual-studio-2015/debugging.png)