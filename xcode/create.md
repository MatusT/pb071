## Pridanie súborov do projektu

Nie vždy bude stačiť vytvoriť len jeden súbor, obsahujúci všetkú funkcionalitu. Preto funkcie rozdelujeme do viacerých súborov. 

V jazyku C platí, že vytvárame vždy hneď dva súbory, jeden s príponou .h, druhý s príponou .c. Súbor s príponou .h označujeme ako hlavičkový a obsahuje deklarácie funkcií, ktoré sú následne v súbore s príponou .c implementované.

Do samotného programu potom includneme už len hlavičkový súbor, napríklad** &lt;stdio.h&gt;**



Na vytvorenie nového súboru kliknite na priečinok, v ktorom chcete súbor vytvoriť a vyberte _New File.._.

![](/assets/Xcode_create0.jpg)

Z ponúknutých možností vyberte _C File._ Kliknite na_ Next._

![](/assets/Xcode_create1.jpg)

Definujte meno pre súbor \(1\). Zaškrtnite, že chcete vytvorit aj hlavičkový súbor \(2\).  
\(Vo väčšine prípadov ho budete chcieť vytvoriť.\) Kliknite na _Next_.

![](/assets/Xcode_create2.jpg)

Vo vami vybranom priečinku by sa mali objaviť novovytvorené súbory. Všimnite si, že hlavičkový súbor obsahuje   
\`\`\`c

\#ifndef example\_h  
\#define example\_h

...

\#endif/\* example\_h \*/

\`\`\`

![](/assets/Xcode_create3.png)

