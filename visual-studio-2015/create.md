## Vytvorenie nového projektu {#visual-studio-new-project}

Visual Studio rozlišuje dva [koncepty](https://msdn.microsoft.com/en-us/library/b142f8e7.aspx): **solution** a **project.**

* **Project** - logický celok obsahujúci cesty k súborom, ktoré chcete skompilovať, a informáciu ako ich má Visual Studio skompilovať. Súčasť **solution**.
* **Solution** - kolekcia **projektov** s dodatočnými informáciami netýkajucími sa samotnej kompilácie ako nastavenia okien editora, nezdrojové súbory\(obrázky etc.\) a podobne.

V tomto predmete budete mať typicky niekoľko projektov na jednu úlohu:

* Niekoľko projektov bude obsahovať zdrojové súbory úlohy - to budú spúšťateľné aplikácie a najčastejšie aj samotné riešenia úlohy, ktoré máte odovzdať.
* Jeden bude bude mať súbory obsahujúce **testovací framework a testy** k úlohe.


1. V menu vyberte **File → New → Project**

   ![](/visual-studio-2015/images/project_create_1.png)

2. Z možných templatov vyberte Win32 Console Application a paremetre vyplňte nasledovne:

   * **Name** - názov projektu bude zodpovedať názvu folderu, kde bude uložený. Z tohoto dôvodu úlohy na odovzdanie Kontru pomenúvajte podľa vyžadovanej schémy\(hw0x\).
   * **Location** - zvoľte cestu k Vášmu git repozitáru.
   * **Solution** - ak chcete vytvoriť nový folder na riešenie novej úlohy tak _Create new solution_ čím vytvoríte už podľa názvu **solution** obsahujúci nový projekt. V prípade, že budete chcieť len pridať projekt pre testy, môžete zvoliť možnosť _Add to solution_.
   * **Create directory for solution** - nezaškrtávajte, nie je to potrebné a s najväčšou pravdepodobnosťou si iba vytvoríte zbytočne veľa folderov v ktorých Kontr nenájde súbory.
   * **Add to Source Control** - môžete zaškrtnúť, keď pridávate projekt/solution do git repozitára\(pozri [tutoriál na git](../git/README.md)\)

     ![](/visual-studio-2015/images/project_create_2.png)

3. Kliknite Next pre ďalšie nastavenia a zvolťe _Console application_ a zaškrtnite iba _Empty project_

   ![](/visual-studio-2015/images/project_create_5.png)

4. Na to aby ste dostávali rovnaké warningy a errory, aké produkuje **gcc**/**Kontr**, je nutné zvoliť v nastaveniach projektu platformu _Clang with Microsoft CodeGen_ a dodať **flag**y _-std=c99 -pedantic -Wall -Werror._  
   Kliknite na názov projektu v okne **Solution Explorer** a zvoľte **Properties**. Nastavte tieto hodnoty:

   * v záložke **General**: Platform toolset - _Clang with Microsoft CodeGen_ 
   * v záložke **C/C++ → Command Line** vyplňte do _Additional options_: **-std=c99 -pedantic -Wall -Werror**

     ![](/visual-studio-2015/images/project_options_1.png)  
     ![](/visual-studio-2015/images/project_options_2.png)  
     ![](/visual-studio-2015/images/project_options_3.png)

5. Vytvorte nové súbory

   * Kliknite na _Header_/_Source_ _Files_ podľa toho či chcete pridať hlavičkový alebo zdrojový súbor → Add → New Item…
   * Používajte striktne prípony **.h** a **.c**

     ![](/visual-studio-2015/images/new_item_1.png)  
     ![](/visual-studio-2015/images/new_item_2.png)



