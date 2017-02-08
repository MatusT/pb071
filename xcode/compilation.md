## Nastavenie kompilačných parametrov {#xcode-compilation}

Aby ste dostávali rovnaké warningy a errory, aké produkuje **gcc**/**Kontr**, je nutné pridať pridať k vašej kompilácii rovnaké _warning options, ako sú nastavené v **Kontr**. V tomto predmete budeme používať nasledovné_ warning options : **-std=c99 -pedantic -Wall -Werror.**

V bočnom menu projektu kliknite na súbor example, reprezentujúci aplikáciu \(1. krok\). Vyberte záložku _Build Settings_\(2.\), a do panelu pre hladanie napíšte _flags_\(3.\). V nájdených výsledkoch nájdite možnosť _Other C Flags_\(4.\), dvojklikom otvorte okno na vloženie, a vložte vyššie spomínané _options: _**-std=c99 -pedantic -Wall -Werror**

![](/assets/Xcode_build1.jpg)

Ako test, že ste _options nastavili správne, otvorte súbor _**main.c**_ a do funcie main_ pridajte nasledovný riadok:

```c
int variable = 0;
```

Je jedno, či bude tento riadok vložený pred, alebo po funcii _printf_. Kliknite na ikonku pre Run. Vaša aplikácia by mala zahlásiť  
_Build failed_, a vysvietiť sa pridaný riadok s informácii o vytvorení nepoužitej premennej.

![](/assets/Xcode_build2.jpg)

