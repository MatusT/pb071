## Vytvorenie nového projektu

Visual Studio rozlišuje dva [koncepty](https://msdn.microsoft.com/en-us/library/b142f8e7.aspx): **solution** a **project.**

- **Project** - logický celok obsahujúci cesty k súborom, ktoré chcete skompilovať, a informáciu ako ich má Visual Studio skompilovať. Súčasť **solution**.
- **Solution** - kolekcia **projektov** s dodatočnými informáciami netýkajucími sa samotnej kompilácie ako nastavenia okien editora, nezdrojové súbory(obrázky etc.) a podobne.

V tomto predmete si vystačíte s najviac **2 projektami** v jednom solution na úlohu:

- Typicky bude prvý obsahovať zdrojové súbory úlohy a **main.c** - to bude spúšťateľná aplikácia a najčastejšie aj samotné riešenie úlohy, ktoré máte odovzdať(občas budete mať ako zadanie napísať/opraviť testy namiesto písania aplikácie).
- Druhý bude zdieľať s prvým zdrojové súbory, ale namiesto main.c bude mať súbory obsahujúce **testovací framework a testy** k úlohe.


1. V menu vyberte File → New → Project
![](/visual-studio-2015/images/project_create_01.png)

2. Z možných templatov vyberte Win32 Console Application a paremetre vyplňte nasledovne:
  - **Name** - názov projektu bude zodpovedať názvu folderu, kde bude uložený. Z tohoto dôvodu úlohy na odovzdanie Kontru pomenúvajte podľa vyžadovanej schémy(hw0x).
  - **Location** - zvoľte cestu k Vášmu git repozitáru.
  - **Solution** - ak chcete vytvoriť nový folder na riešenie novej úlohy tak *Create new solution* čím vytvoríte už podľa názvu **solution** obsahujúci nový projekt. V prípade, že budete chcieť len pridať projekt pre testy, môžete zvoliť možnosť *Add to solution*.
  - **Create directory for solution** - nezaškrtávajte, nie je to potrebné a s najväčšou pravdepodobnosťou si iba vytvoríte zbytočne veľa folderov v ktorých Kontr nenájde súbory.
![](/visual-studio-2015/images/project_create_02.png)

3. Zvolťe *Console application* a zaškrtnite iba *Empty project*
![](/visual-studio-2015/images/project_create_03.png)

4. Na to aby ste dostávali rovnaké warningy a errory, aké produkuje **gcc**/**Kontr**, je nutné zvoliť v nastaveniach projektu platformu *Clang with Microsoft CodeGen* a dodať **flag**y *-std=c99 -pedantic -Wall -Werror.*
  Kliknite na názov projektu v okne **Solution Explorer** a zvoľte **Properties**. Nastavte tieto hodnoty: 
  - v záložke **General**: Platform toolset - *Clang with Microsoft CodeGen* 
  - v záložke **C/C++ → Command Line** vyplňte do *Additional options*: **-std=c99 -pedantic -Wall -Werror** 
![](/visual-studio-2015/images/project_options_1.png)
![](/visual-studio-2015/images/project_options_2.png)
![](/visual-studio-2015/images/project_options_3.png)

5. Vytvorte nové súbory
  - Kliknite na *Header*/*Source* *Files* podľa toho či chcete pridať hlavičkový alebo zdrojový súbor → Add → New Item…
  - Používajte striktne prípony **.h** a **.c**
https://d2mxuefqeaa7sj.cloudfront.net/s_0F8597AFE97FB791FCCE3ADC2525C4BD7286EDD519DCC92C8988386EA14F90FD_1484346178869_2017-01-13+25.png
https://d2mxuefqeaa7sj.cloudfront.net/s_0F8597AFE97FB791FCCE3ADC2525C4BD7286EDD519DCC92C8988386EA14F90FD_1484346178856_2017-01-13+26.png


