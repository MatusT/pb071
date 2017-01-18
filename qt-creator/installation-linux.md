## Inštalácia Qt na Linux

Inštalácia na linuxe je závislá na konkrétnej distribúcii a kedže distribúcií je nespočetne mnoho, konkrétne postupy tu budú uvedené len pre najnovšie verzie najpopulárnejších linuxových distribúcií. Pokiaľ máte názvy balíkov pre svoju distribúciu a chcete ju zdieľať s ostatnými študentami, pridajte ju do komentárov a bude pridaná do tohoto návodu.

Medzi základne balíky, ktoré sú potrebné pre kompiláciu, patria:
- make
- gcc - kompilátor
- gdb - debugger

Samotný Qt Creator nemusí byť vždy nainštalovaný aj s **qmake**, nástrojom na spracovávanie projektových súborov **pro**.

## Ukážkové distribúcie

V tejto časti sú uvedené príkazy inštalujúce všetky potrebné nástroje jediným príkazom.

### Ubuntu 16.10

```
sudo apt install make gcc gdb qt5-default qtcreator
```

### Fedora 25

```
sudo dnf install make gcc gdb qt5*-devel qt-creator
```

## Všeobecný postup - inštalátor

V prípade, že nepoužívate žiadnu z vyššie uvedených distribúcií, je priložený aj všeobecný návod pre každú distribúciu.

1. Základne balíky make, gcc, gdb na kompiláciu musíte nainštalovať z balíčkovacieho správcu Vašej distribúcie - väčšinou sa tieto balíku volajú presne podľa názvov programov.

2. Qt Creator je možné nainštalovať pomocou inštalátora:
  - [64 bit](http://download.qt.io/official_releases/online_installers/qt-unified-linux-x64-online.run) 
  - [32 bit](http://download.qt.io/official_releases/online_installers/qt-unified-linux-x86-online.run)

## Kam ďalej

Po nainštalovaný môžete otvárať súbory, s príponopu **.pro**, definujúce projekt. Tieto projektové súbory sú dodané pre úlohy na cvičenia. Pokračujte v návode [otvrením a skompilovaním projektu](../qt-creator/compilation.md).

