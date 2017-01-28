# Inštalácia Qt na Linux {#intro}

Inštalácia na linuxe je závislá na konkrétnej distribúcii a kedže distribúcií je nespočetne mnoho, konkrétne postupy tu budú uvedené len pre najnovšie verzie najpopulárnejších linuxových distribúcií. Pokiaľ máte názvy balíkov pre svoju distribúciu a chcete ju zdieľať s ostatnými študentami, pridajte ju do komentárov a bude pridaná do tohoto návodu.

# Ukážkové distribúcie {#distributions}

V tejto časti sú uvedené príkazy inštalujúce všetky potrebné nástroje pre jednotlivé distribúcie.

## Ubuntu 16.10

```
sudo apt install make gcc g++ gdb qt5-default qtcreator
```

## Fedora 25

```
sudo dnf install make gcc g++ gdb qt5*-devel qt-creator
```

# Všeobecný postup - inštalátor {#installer}

V prípade, že nepoužívate žiadnu z vyššie uvedených distribúcií, je priložený aj všeobecný návod pre každú distribúciu.

Základne balíky **make, gcc, gdb** na kompiláciu musíte nainštalovať z balíčkovacieho správcu Vašej distribúcie - väčšinou sa tieto balíku volajú presne podľa názvov programov.

**Qt Creator** je možné nainštalovať pomocou inštalátora:

1. Stiahnite Qt Open Source Online Installer, napr. pomocou wget:
  ```
  # pre 32 bitovú verziu nahradťe x64 za x86
  wget http://download.qt.io/official_releases/online_installers/qt-unified-linux-x64-online.run
  ```
2. Nastavte inštalátoru práva na spúštanie
  ```
  ./chmod +x qt-*
  ```
3. Spustite
  ```
  ./qt*
  ```
4. Na začiatku Vám inštalátor ponúkne registráciu, ktorá nie je povinná a je možné ju
preskočiť. V prípade, že sa rozhodnete túto možnosť využiť, účet Vám poslúži na prihlasovanie sa do [Qt Wiki](https://wiki.qt.io/Main) a [Qt Fóra](https://forum.qt.io/).
  
  ![](/images/qt-creator/linux_install_01.png)
  
5. Z komponent potrebujete Qt 5.7 → **Desktop gcc 64-bit/32-bit**
  
  ![](/images/qt-creator/linux_install_03.png)


{% include "./installation-next.md" %}
