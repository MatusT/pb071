# Použitie {#intro}

Najprv musíte skompilovať program bez optimalizácií a s informáciami na debugovanie, aby Valgrind vedel určiť riadky kódu, kde sa chyba nachádza. Ak už máte program skompilovaný, napríklad cez Qt Creator, a je to debug build, môžete preskočiť na [Spustenie Valgrindu]().

> Pozor! Ak máte Windows a používate *Bash on Ubuntu on Windows*, program musíte skompilovať v príkazovej riadke Ubuntu, výstup z Qt Creatora nebude platný.

## Kompilácia programu {#compilation}

### Priamo pomocou gcc {#gcc}

Aby ste mohli spustiť Valgrind nad Vaším programom, je potrebné ho skompilovať pomocou gcc. To spravíte príkazom:
```
# všeobecná forma: gcc -g -std=c99 -pedantic -Wall -Werror [zoznam_suborov] -o nazov_programu 
# ako príklad je uvedená kompilácia hw01
gcc -g -std=c99 -pedantic -Wall -Werror main.c -o hwo01
```
- **-std=c99 -pedantic -Wall -Werror** nastavenia boli spomenuté už v predošlých návodoch
- **-g** vloží informácie potrebné na debugovanie do výsledného binárneho súboru, potrebné pre valgrind
- **-o** je nepovinná možnosť, určuje názov výsledného súboru. Ak túto možnosť vynecháte, výsledný súbor sa bude volať a.o

Následne môžete program spustiť:
```
# ./nazov_programu
./hw01
```

### Qt projekty typu .pro {#qmake}

> Windows: v *Bash on Ubuntu on Windows* použite príkaz: sudo apt install qt5-default
> na inštaláciu Qt nástrojov


Ak máte *.pro* súbor na projekt, pridajte doň riadok
```
CONFIG += debug
```

A môžete projekt pre Valgrind skompilovať príkazom:
```
# všeobecná forma: -o Makefile nazov_projektu.pro
# ako príklad je uvedená kompilácia hw01
qmake -o Makefile hw01.pro && make
```

Následne môžete program spustiť:
```
# ./nazov_programu
./hw01
```

## Spustenie Valgrindu {#valgrind}
 
Keď už máte program skompilovaný, stačí spustiť Valgrind príkazom:
```
# všeobecná forma: valgrind --leak-check=full ./nazov_programu
# ako príklad je uvedená kompilácia hw01
valgrind --leak-check=full ./hw01
```

Príklad vystupu:
```
==14168== Memcheck, a memory error detector
==14168== Copyright (C) 2002-2015, and GNU GPL'd, by Julian Seward et al.
==14168== Using Valgrind-3.11.0 and LibVEX; rerun with -h for copyright info
==14168== Command: ./hw01
==14168==
Hello World!
==14168==
==14168== HEAP SUMMARY:
==14168==     in use at exit: 0 bytes in 0 blocks
==14168==   total heap usage: 1 allocs, 1 frees, 4,096 bytes allocated
==14168==
==14168== All heap blocks were freed -- no leaks are possible
==14168==
==14168== For counts of detected and suppressed errors, rerun with: -v
```

# Kam ďalej {#next}

Po odchytení všetkých chýb programu, je potrebné program:
- zdokumentovať programom [Doxygen](../doxygen/README.md)
- ak je úlohou na odovzdanie, [odovzdať cez Kontr](../ssh/README.md)