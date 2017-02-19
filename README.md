> Späť na [cecko.eu](www.cecko.eu).

# Úvod

Tieto tutoriály slúžia na to, aby ste si vedeli nastaviť a požívať vývojárske nástroje, potrebné pre predmet PB071, na vlastnom počítači. Minimálne by ste mali prejsť všetkými tutoriálmi v kategórii *základných* a to v poradí, akom su usporiadané. V kategórii \*doplňujúcich\* nájdete nepovinné tutoriály, ktoré sa Vám však môžu takisto hodiť.

## Špecifické pre Windows

### Linuxový systém

Pre Windows je hneď niekoľko vecí navyše. V prvom rade sa jedná o simuláciu linuxového prostredia. Linux je vo väčšine učební, používa ho väčšina cvičiacich a Kontr, nástroj na kontrolu úloh, beží takisto na linuxe. Z tohoto dôvodu je užitočné mať k dispozícii linuxový sýstém, ale aby ste si ho nemuseli inštalovať na svoj počítač a nemuseli behať na fakultu, ponúkame dve alternatívy:

1. [Virtuálny stroj](../virtual-machine/README.md) - pripravený spustiteľný linux so všetkými nástrojmi. Stačí keď ho spustíte a nemusíte nič inštalovať
2. [Ubuntu on Windows](../ubuntu-on-windows/README.md) - ak máte Windows 10 v 64 bitovej verzii, môžete aktivovať túto funkcionalitu, ktorá Vám dodá konzolovú verziu Ubuntu. Potom môžete postupovať v tutoriáloch linuxovou vetvou. Nevýhoda je, že máte k dispozícii command line. Výhoda voči virtuálnemu stroju je omnoho vyššia rýchlosť a prístup k dátam Windowsu.

### [Visual Studio 2015](../visual-studio-2015/README.md)

Pre tých, ktorí preferujú natívne vývojové prostredie na Windowse od Microsoftu, je pripravený tutoriál aj na Visual Studio. Popísane je, ako dosiahnuť rovnakú kontrolu kódom, akú robí Kontr. Pozor, musíte si však vytvárať vlastné projekty, nakoľko dodaný je len cmake!

## Špecifické pre macOS

### [Homebrew](/qt-creator/homebrew-osx.md)

Inštalačný systém, vďaka ktorému môžete ľahšie nainštalovať niekoľko vývojarských nástrojov

### [Xcode](/xcode/README.md)

Pokiaľ nechcete používať Qt Creator, je k dispozícii návod na natívne vývojové prostredie pre macOS, vyvíjané Applom.

{% include "./SUMMARY.md" %}

