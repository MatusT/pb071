## Debugging

Pred spustením debugovania sa uistite, že je projekt skompilovaný s informáciami potrebnými pre debugovanie. To spravíte kliknutím na ikonu výberu spôsobu kompilácie\(viď obrázok nižšie\) a zvolením _Debug_.

![](/images/qt-creator/debug_01.png)

Teraz môžete spustiť proces debugovania kliknutím na ikonu nachádzajúcu sa pod ikonou spustenia. Qt Creator sa prepne do módu debugovania, ktorý vyzerá ako na obrázku. Jednotlivé okná a prvky sú postupne popísané v tutoriály aj s návodom ako ich efektívne používať pre nájdenie chyby v programe.

![](/images/qt-creator/debug_02.png)

### Breakpoints

**Breakpoint** je bod v programe, určený podmienkou, na ktorom debugger zastaví počas behu programu. Podmienkou je najčastejsie riadok kódu v programe - takýto bod môžete určiť kliknutím vedľa čísla riadku v editore. Keď program v tomto bode zastaví, môžete:
- preskúmať stav programu v oknách [*Stacktrace*]() a [*Local variables and watches*]()
- postupovať po krokoch([over/into/out]())
- nechať program bežať dalej kliknutím na Continue(viď obrázok), až kým nenarazí na ďalší breakpoint

V okne *Breakpoints* je možné vidieť zoznam všetkých breakpointov, ktoré ste vytvorili. Dvojkliknutím do okna vytvoríte nový breakpoint, pravým kliknutím na existujúci breakpoint a zvolením **Edit Selected Breakpoints** upravíte podmienky zvoleného breakpointu.

Pokročilejšie nastavenia breakpointu su užitočné napríklad vtedy, keď chcete testovať cyklus a zastaviť sa až pri n-tej iterácii. To dosiahnete možnosťou *Ignore count*. Môžete taktiež určiť zastavenie na volaní konkrétnej funkcie a pod.

### Step over/into/out

Pomocou panelu, nachádzuceho sa nad oknom Stacktrace, je možné pohybovať sa v programe po krokoch:

- **Step over** - preskočí riadok kódu na ktorom sa nachádza a zastaví sa na nasledujúcom
- **Step into** - vstúpi do funkcie, ktorá je volaná na aktuálnom riadku
- **Step out** - vystúpi z funkcie v ktorej sa program náchadza

### Local variables and watches

V tomto okne sú automaticky zobrazené lokálne premenné na stacku s ich hodnotami v danom zastavenom stave programu. Dvojkliknutím do okna je možné pridať výraz

### Stacktrace

