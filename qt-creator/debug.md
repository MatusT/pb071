# Debugging {#intro}

Pred spustením debugovania sa uistite, že je projekt skompilovaný s informáciami potrebnými pre debugovanie. To spravíte kliknutím na ikonu výberu spôsobu kompilácie\(viď obrázok nižšie\) a zvolením _Debug_.

![](/images/qt-creator/debug_01.png)

Teraz môžete spustiť proces debugovania kliknutím na ikonu nachádzajúcu sa pod ikonou spustenia. Qt Creator sa prepne do módu debugovania, ktorý vyzerá ako na obrázku. Jednotlivé okná a prvky sú postupne popísané v tutoriály aj s návodom, ako ich efektívne používať pre nájdenie chyby v programe.

![](/images/qt-creator/debug_02.png)

## Breakpoints {#breakpoints}

**Breakpoint** je bod v programe, určený podmienkou, na ktorom debugger zastaví počas behu programu. Podmienkou je najčastejsie riadok kódu v programe - takýto bod môžete určiť kliknutím vedľa čísla riadku v editore. Keď program v tomto bode zastaví, môžete:
- preskúmať stav programu v oknách [Stacktrace](#stacktrace) a [Local variables and watches](#locals),
- postupovať po krokoch([Step over/into/out](#step)),
- nechať program bežať dalej kliknutím na Continue(viď obrázok), až kým nenarazí na ďalší breakpoint.

V okne *Breakpoints* je možné vidieť zoznam všetkých breakpointov, ktoré ste vytvorili. Dvojkliknutím do okna vytvoríte nový breakpoint, pravým kliknutím na existujúci breakpoint a zvolením **Edit Selected Breakpoints** upravíte podmienky zvoleného breakpointu.

Pokročilejšie nastavenia breakpointu su užitočné napríklad vtedy, keď chcete testovať cyklus a zastaviť sa až pri n-tej iterácii. To dosiahnete možnosťou *Ignore count*. Môžete taktiež určiť zastavenie na volaní konkrétnej funkcie a pod.

## Step over/into/out {#step}

Pomocou panelu, nachádzajúceho sa nad oknom _Stacktrace_, je možné pohybovať sa v programe po krokoch:

- **Step over** - preskočí riadok kódu, na ktorom sa nachádza a zastaví sa na nasledujúcom,
- **Step into** - vstúpi do funkcie, ktorá je volaná na aktuálnom riadku,
- **Step out** - vystúpi z funkcie, v ktorej sa program náchadza.

## Local variables and watches {#locals}

V tomto okne sú automaticky zobrazené lokálne premenné na stacku s ich hodnotami v danom zastavenom stave programu. Dvojkliknutím do okna je možné pridať výraz, ktorý bude vyhodnocovaný pri zmene stavu. Výraz môže pozostávať aj z názvu iba jedinej premennej - takýmto spôsobom je možné sledovať premennú, ktorá nie je práve vo funkcii, kde sa chod programu nachádza.

## Stacktrace {#stacktrace}

Zobrazuje zoznam funkcií, ktoré boli zavolané aby sa program dostal do zastaveného bodu. Stacktracom sa dá prezerať história behu programu, pre každý bod sú zapamätané _local variables and watches_.


# Kam ďalej {#next}

Ak ste sa dostali až sem, tak ste prešli všetky potrebné tutoriály na vývoj. Ďalej by ste mali pokračovať:
- hľadaním a odchytávaním chýb spojených s pamäťou pomocou nástroja [Valgrind alebo Dr. Memory](/memory-leaks/README.md),
- dokumentovaním kódu pomocou nástroja [Doxygen](/doxygen/README.md),
- odovzdaním úlohy na [AISE](/ssh/README.md).