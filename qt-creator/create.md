# Vytvorenie nového projektu {#intro}

1. Vyberte v menu **File -> new File or Project** alebo **+ New Project** v úvodnej obrazovke

  ![](/images/qt-creator/create_01.png)

2. Zvoľte typ projektu **Non-Qt Project -> Plain C Application**

  ![](/images/qt-creator/create_02.png)

3. Určite meno projektu, pre domáce úlohy používajte hw01-hw05. Pre projekt bude vytvorený folder s rovnakým názvom, aký ma projekt. Pokiaľ teda budete vytvárať hw0x projekt, ako cestu zvoľte repozitár úloh.

  ![](/images/qt-creator/create_03.png)

4. Build system nastavte na **qmake**

  ![](/images/qt-creator/create_04.png)

5. Ak ste postupovali správne podľa návodu, budete mat práve jeden kit s gcc/MinGW

  ![](/images/qt-creator/create_05.png)
  
6. Voľbu *Add to version control* vynechajte, zbytočne iba vytvorí .gitignore pre daný projekt - to je však zbytočné ak už jeden máte v repozitári.

  ![](/images/qt-creator/create_06.png)

7. Do konfiguračného súboru projektu(.pro) pridajte nastavenia pre kompilátor používané v tomto predmete:
   ```
   QMAKE_CFLAGS = -std=c99 -pedantic -Wall -Werror
   ```
   Jednotlivé nastavenia znamenajú nasledovné:
   - **std=c99** - nastaví štandard jazyka, podľa ktorého má kompilátor kontrolovať na C99(vyučovaná verzia v PB071)
   - **pedantic** - nastaví striktné dodržiavanie štandardu, kompilátorom neprejdu žiadne rozšírenia štandardu, zahlási všetky chyby vyžadované štandardom
   - **Wall** - skratka pre *Warnings All*, pri tomto nastavení bude kompilátor upozorňovať aj na možné chyby, ktoré nie sú vynucované štandardom
   - **Werror** - skratka pre *Warning as error*, každé upozornenie bude brané ako chyba
  
  ![](/images/qt-creator/create_07.png)

# Kam ďalej {#next}

