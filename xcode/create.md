## Pridanie súborov do projektu

Nie vždy bude stačiť vytvoriť len jeden súbor, obsahujúci všetkú funkcionalitu. Preto funkcie rozdelujeme do viacerých súborov.

V jazyku C platí, že vytvárame vždy hneď dva súbory, jeden s príponou .h, druhý s príponou .c.   
Súbor s príponou .h označujeme ako hlavičkový a obsahuje deklarácie funkcií, ktoré sú v súbore s príponou .c implementované.

Do samotného programu potom includneme už len hlavičkový súbor, napríklad hlavičkový súbor stdio.h includneme pomocou formule **\#include &lt;stdio.h&gt;.**

Na vytvorenie nového súboru kliknite na priečinok, v ktorom chcete súbor vytvoriť a vyberte **New File...**

![](/assets/Xcode_create0.jpg)

Z ponúknutých možností vyberte** C File.** Kliknite na_ _**Next**_._

![](/assets/Xcode_create1.jpg)

Definujte meno pre súbor \(1\). Zaškrtnite, že chcete vytvorit aj hlavičkový súbor \(2\).  
\(Vo väčšine prípadov ho budete chcieť vytvoriť.\) Kliknite na **Next**.

![](/assets/Xcode_create2.jpg)

Vo vami vybranom priečinku by sa mali objaviť novovytvorené súbory. Všimnite si, že hlavičkový súbor obsahuje

```c
#ifndef example_h
#define example_h
...
#endif/* example_h */
```

Tieto riadky majú svoj význam, tak ich prosím nemažte.

![](/assets/Xcode_create3.png)

