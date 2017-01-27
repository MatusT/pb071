# Inštalácia {#intro}

1. V nastaveniach zvoľte **Update & Security**.

  ![](/images/ubuntu-on-bash/install_01.png)

2. Zapnite si **Developer mode** pre Windows 10.

  ![](/images/ubuntu-on-bash/install_02.png)

3. Cez vyhľadávanie nájdite a otvorte **Turn Windows features on or off**.

  ![](/images/ubuntu-on-bash/install_03.png)

4. Nájdite položku **Windows Subsystem for Linux (Beta)**, zaškrtnite ju a potvrďte. Následne **reštartujte **Windows.

  ![](/images/ubuntu-on-bash/install_04.png)

5. Po reštarte vyhľadajte program **bash** a spustite. 

  ![](/images/ubuntu-on-bash/install_05.png)
  
6. Nápište **y** a stlačte enter pre potvrdenie inštalácie. V ďalšom kroku vytvorte účet administrátora linuxového systému - tento účet sa nemusí zhodovať s Vaším Windows účtom.

  ![](/images/ubuntu-on-bash/install_06.png)

# Prvé kroky {#start}

Po úspešnom nainštalovaní môžete spúštať aplikáciu **Bash on Ubuntu on Windows**. Je to plnohodnotné Ubuntu a teda všetky linuxové príkazy v ňom budú fungovať.

![](/images/ubuntu-on-bash/install_07.png)

Na začiatok je odporúčané updatovať Ubuntu pomocou príkazu:
```
sudo apt update && sudo apt upgrade
```

# Prístup k súborom {#filesystem}



# Kam ďalej {#next}

Najdôležitejšia funkcionalita je pre Vás použitie programu Valgrind, ktorý inak na Windowse nespustíte. Pokračujte [návodom na jeho inštaláciu](../valgrind/installation_windows.md).
