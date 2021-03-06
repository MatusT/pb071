### Vytvorenie Xcode projektu pomocou cmake

Na začiatok si nainštalujte [cmake](/git/cmake-os-x.md).

Stiahnite si priečinok s domácou úlohou, v prípade potreby ho odzipujte. Pre ukážky tutoriálu predpokladám výskyt domácej úlohy v priečinku _/Users/Kejsty/Downloads/hw01/_, a chcem rozbaliť úlohu do priečinku _/Users/Kejsty/Documents/Skola/PB071/hw01_

```terminal
cd Documents/Skola/PB071/
mkdir hw01
cd hw01
cmake -G Xcode . -- CMAKE_SOURCE_DIR = /Users/Kejsty/Downloads/hw01/,   CMAKE_BINARY_DIR = /Users/Kejsty/Downloads/hw01/
```

![](../assets/CmakeProjectXcode.png)

V priloženom obrázku je vidieť, že príkaz vygeneroval súbor s príponou _.xcodeproj_. Tento súbor je náš novovygenerovaný Xcode projekt. Otvoríme teda aplikáciu Xcode a vyberieme možnosť **Open another project**.

![](../assets/CmakeProjectXcode2.png)

V otvorenom okne nájdeme náš vygenerovaný projekt a vyberieme ho.

![](../assets/CmakeProjectXcode3.png)

Projekty vygenerované pomocou CMake majú o niečo zložitejšiu štruktúru, avšak narába sa s nimi pomerne jednoducho. Otvorte **Sources**. Pre každú spustiteľnú binárku vygeneroval CMake osobitný súbor. Pre binárku spustiteľnú ako **hw01_pow** nájdeme potrebné priečinky v súbore **Sources &gt hw01_pow &gt Source Files **, prípadne Header Files.

![](../assets/CmakeProjectXcode4.png)

Na spustenie binárky **hw01_pow** rozbalte menu pre výber vpravo hore (viď obrázok) a vyberte **hw01_pow**.

![](../assets/CmakeProjectXcode5.png)

Po vybratí stlačte **Run** (ikonka play). Rovnakým spôsobom spustíte aj ostatné binárky.

![](../assets/CmakeProjectXcode6.png)



