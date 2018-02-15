# Inštalácia Qt na Windows {#intro}

Stiahnite si *Qt Open Source* na adrese [https://www.qt.io/download-open-source/](https://www.qt.io/download-open-source/). ([Priamy link](http://download.qt.io/official_releases/online_installers/qt-unified-windows-x86-online.exe))
Inštalácia by mala vyzerať tak, ako na priložených obrázkoch.

1. Na začiatku Vám inštalátor ponúkne registráciu, ktorá nie je povinná a je možné ju
preskočiť. V prípade, že sa rozhodnete túto možnosť využiť, účet Vám poslúži na prihlasovanie sa do [Qt Wiki](https://wiki.qt.io/Main) a [Qt Fóra](https://forum.qt.io/).
  
  ![](../images/qt-creator/windows_install_02.png)

2. Z komponentov na výber potrebujete:
  - Qt → Qt 5.10.1 → **MinGW 5.3.0 32 bit**
  - Tools → **MinGW 5.3.0**

3. Ak chcete aj podporu oficiálneho Microsoft kompilátora MSVC, môžete pridať aj nasledujúce komponenty:
  - Qt → Qt 5.10.1 → **msvc2017 64-bit**
  - Tools → **Qt Creator 4.5.1 CDB Debugger support**
     
    ![](../images/qt-creator/windows_install_03.png)

{% include "./installation-next.md" %}