## Inštalácia Qt na Linux

Inštalácia na linuxe je závislá na konkrétnej distribúcii a kedže distribúcií je nespočetne mnoho, konkrétne postupy tu budú uvedené len pre najnovšie verzie najpopulárnejších linuxových distribúcií. Pokiaľ máte názvy balíkov pre svoju distribúciu a chcete ju zdieľať s ostatnými študentami, pridajte ju do komentárov a bude pridaná do tohoto návodu.

Medzi základne balíky, ktoré sú potrebné pre kompiláciu, patria:
- make
- gcc - compiler
- gdb - debugger

Pre 

### Ubuntu 16.10

```
sudo apt install make gcc gdb qt5-default qtcreator
```

### Fedora 25

```
sudo dnf install make gcc gdb qt5*-devel qt-creator
```


## Kam ďalej

Po nainštalovaný môžete otvárať súbory, s príponopu **.pro**, definujúce projekt. Tieto projektové súbory sú dodané pre úlohy na cvičenia. Pokračujte v návode [otvrením a skompilovaním projektu](../qt-creator/compilation.md).

