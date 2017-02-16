# Valgrind použitie

Majme nasledovný ukážkový main súbor, obsahujúci jedinú alokáciu pamäte, ktorá nie je uvoľnená, a teda na tomto mieste dochádza k **memory leaku**.

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    printf("Hello, World!\n");
    int *leak = malloc(sizeof(int));	
    return 0;
}

```

Súbor main.c skompilujeme (pre potreby tejto ukážky môžeme niektoré flagy vynechať) s pridaným flagom **-g**, ktorý spôsobí, že výstup z valgrindu bude čitateľnejší.

Výslednú skompilovanú binárku **main** spustíme pod valgrindom s flagmi **--leak-check=full --show-reachable=yes**

V prípade, že by spustená binárka potrebovala k spusteniu ďaľšie argumenty, tieto argumenty budú umiestnené za **./main**

```terminal
gcc -std=c99 -g -o main main.c
valgrind --leak-check=full --show-reachable=yes ./main
```

Vo výstupe z valgrindu môžeme vidieť: 

* _Hello, World!_ hovorí, aký bol output spustenej binárky **main**

* _in use at exit: 4 bytes in 1 blocks_ hovorí, že sme neuvoľnili všetkú alokovanú pamäť.

* _4 bytes in 1 blocks are definitely lost in loss record 1 of 1_ spolu s _by 0x400581: main (main.c:7)_ nám následne hovorí, kde alokácia nastala. V našom prípade ide práve o alokáciu premennej **leak**


```terminal
==18901== Memcheck, a memory error detector
==18901== Copyright (C) 2002-2015, and GNU GPL'd, by Julian Seward et al.
==18901== Using Valgrind-3.11.0 and LibVEX; rerun with -h for copyright info
==18901== Command: ./main
==18901== 
Hello, World!
==18901== 
==18901== HEAP SUMMARY:
==18901==     in use at exit: 4 bytes in 1 blocks
==18901==   total heap usage: 2 allocs, 1 frees, 1,028 bytes allocated
==18901== 
==18901== 4 bytes in 1 blocks are definitely lost in loss record 1 of 1
==18901==    at 0x4C2DB8F: malloc (in /usr/lib/valgrind/vgpreload_memcheck-amd64-linux.so)
==18901==    by 0x400581: main (main.c:7)
==18901== 
==18901== LEAK SUMMARY:
==18901==    definitely lost: 4 bytes in 1 blocks
==18901==    indirectly lost: 0 bytes in 0 blocks
==18901==      possibly lost: 0 bytes in 0 blocks
==18901==    still reachable: 0 bytes in 0 blocks
==18901==         suppressed: 0 bytes in 0 blocks
==18901== 
==18901== For counts of detected and suppressed errors, rerun with: -v
==18901== ERROR SUMMARY: 1 errors from 1 contexts (suppressed: 0 from 0)

```