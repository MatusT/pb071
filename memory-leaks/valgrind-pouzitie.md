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




```
gcc -std=c99 -g -o main main.c
valgrind --leak-check=full --show-reachable=yes ./main
```


```
==18827== Memcheck, a memory error detector
==18827== Copyright (C) 2002-2015, and GNU GPL'd, by Julian Seward et al.
==18827== Using Valgrind-3.11.0 and LibVEX; rerun with -h for copyright info
==18827== Command: ./main
==18827== 
Hello, World!
==18827== 
==18827== HEAP SUMMARY:
==18827==     in use at exit: 4 bytes in 1 blocks
==18827==   total heap usage: 2 allocs, 1 frees, 1,028 bytes allocated
==18827== 
==18827== 4 bytes in 1 blocks are definitely lost in loss record 1 of 1
==18827==    at 0x4C2DB8F: malloc (in /usr/lib/valgrind/vgpreload_memcheck-amd64-linux.so)
==18827==    by 0x400581: main (in /home/kejsty/Skola/main)
==18827== 
==18827== LEAK SUMMARY:
==18827==    definitely lost: 4 bytes in 1 blocks
==18827==    indirectly lost: 0 bytes in 0 blocks
==18827==      possibly lost: 0 bytes in 0 blocks
==18827==    still reachable: 0 bytes in 0 blocks
==18827==         suppressed: 0 bytes in 0 blocks
==18827== 
==18827== For counts of detected and suppressed errors, rerun with: -v
==18827== ERROR SUMMARY: 1 errors from 1 contexts (suppressed: 0 from 0)
```