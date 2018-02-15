> Späť na [cecko.eu](www.cecko.eu).

# Úvod

Tieto tutoriály slúžia na to, aby ste si vedeli nastaviť a používať vývojárske nástroje, potrebné pre predmet PB071, na vlastnom počítači. Minimálne by ste mali prejsť všetkými tutoriálmi v kategórii _základných_ a to v poradí, akom sú usporiadané. V kategórii _doplňujúcich_ nájdete nepovinné tutoriály, ktoré sa Vám však môžu takisto hodiť.

## Špecifické pre Windows

### Linuxový systém

Pre Windows je hneď niekoľko vecí navyše. V prvom rade sa jedná o simuláciu linuxového prostredia. Linux je vo väčšine učební, používa ho väčšina cvičiacich a Kontr, nástroj na kontrolu úloh, beží takisto na linuxe. Z tohoto dôvodu je užitočné mať k dispozícii linuxový sýstém, ale aby ste si ho nemuseli inštalovať na svoj počítač a nemuseli behať na fakultu, ponúkame dve alternatívy:

1. [Virtuálny stroj](/virtual-machine/index.md) - pripravený spustiteľný linux so všetkými nástrojmi. Stačí keď ho spustíte a nemusíte nič inštalovať
2. [Ubuntu on Windows](/ubuntu-on-windows/index.md) - ak máte Windows 10 v 64 bitovej verzii, môžete aktivovať túto funkcionalitu, ktorá Vám dodá konzolovú verziu Ubuntu. Potom môžete postupovať v tutoriáloch linuxovou vetvou. Nevýhoda je, že máte k dispozícii len command line\(t.j žiadny Qt Creator a pod.\). Výhodou voči virtuálnemu stroju je omnoho vyššia rýchlosť a prístup k dátam Windowsu.

### [Visual Studio 2015](../visual-studio-2015/index.md)

Pre tých, ktorí preferujú natívne vývojové prostredie na Windowse od Microsoftu, je pripravený tutoriál aj na Visual Studio. Popísane je, ako dosiahnuť rovnakú kontrolu kódom, akú robí Kontr. Pozor, musíte si však vytvárať vlastné projekty, nakoľko dodaný je len cmake!

## Špecifické pre macOS

### [Homebrew](/qt-creator/homebrew-osx.md)

Inštalačný systém, vďaka ktorému môžete ľahšie nainštalovať niekoľko vývojarských nástrojov.

### [Xcode](/xcode/index.md)

Pokiaľ nechcete používať Qt Creator, je k dispozícii návod na natívne vývojové prostredie pre macOS, vyvíjané Applom.

# Rozcestník

## Základné

* [Git](git/index.md)
  * [Inštalácia](git/installation.md)
    * [Windows](git/installation-windows.md)
    * [Linux](git/installation-linux.md)
    * [Mac OS X](git/installation-macosx.md)
  * [Začiatok semestra](git/beginning-of-semester.md)
  * [Úloha hello](git/hello.md)
* [CMake](cmake/index.md)
  * [Inštalácia](cmake/installation.md)
    * [Windows](cmake/installation-windows.md)
    * [Linux](cmake/installation-linux.md)
    * [macOS](cmake/installation-macos.md)
  * [Použitie](cmake/use.md)
* [Qt Creator](qt-creator/index.md)
  * [Inštalácia](qt-creator/installation.md)
    * [Windows](qt-creator/installation-windows.md)
    * [Linux](qt-creator/installation-linux.md)
    * [Mac OS X](qt-creator/installation-macosx.md)
  * [Vytvorenie nového projektu](qt-creator/create.md)
  * [Kompilácia](qt-creator/compilation.md)
  * [Debugging](qt-creator/debug.md)
* [Valgrind a Dr. Memory](memory-leaks/index.md)
  * [Windows a Dr. Memory](memory-leaks/windows_drmemory.md)
  * [Linux a Valgrind](memory-leaks/linux_valgrind.md)
  * [macOS a Dr. Memory](memory-leaks/macos_drmemory.md)
  * [macOS a Valgrind](memory-leaks/mac-osx-valgrind.md)
  * [Valgrind - použitie](memory-leaks/valgrind-pouzitie.md)
* [Doxygen](doxygen/index.md)
  * [Inštalácia](doxygen/installation.md)
    * [Windows](doxygen/installation-windows.md)
    * [Linux](doxygen/installation-linux.md)
    * [macOS](doxygen/installation-mac.md)
  * [Písanie dokumentácie](doxygen/document.md)
  * [Generovanie dokumentácie](doxygen/generate.md)
* [AISA a Kontr](ssh/index.md)
  * [Windows](ssh/windows.md)
  * [Linux & macOS](ssh/linux.md)

## Doplňujúce

* [Homebrew for macOS](qt-creator/homebrew-osx.md)
* [Visual Studio 2015](visual-studio-2015/index.md)
  * [Inštalácia](visual-studio-2015/installation.md)
  * [Vytvorenie nového projektu](visual-studio-2015/create.md)
  * [Spustenie projektu](visual-studio-2015/run.md)
  * [Debugging](visual-studio-2015/debugging.md)
  * [Git](visual-studio-2015/git.md)
  * [Dr. Memory](visual-studio-2015/dr.-memory.md)
* [Xcode](xcode/index.md)
  * [Inštalácia](xcode/installation.md)
  * [Spustenie projektu](xcode/run.md)
  * [Nastavenie kompilačných parametrov](xcode/compilation.md)
  * [Pridanie súborov do projektu](xcode/create.md)
  * [Vytvorenie projektu z cmake](xcode/vytvorenie-projektu-z-cmake.md)
* [Ubuntu on Windows](ubuntu-on-windows/index.md)
  * [Inštalácia](ubuntu-on-windows/installation.md)
  * [Kompilačné nástroje](ubuntu-on-windows/kompilacne-nastroje.md)
  * [AISA](ubuntu-on-windows/aisa.md)
* [Virtuálny stroj](virtual-machine/index.md)



