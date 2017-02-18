# Ubuntu on Windows {#intro}

Je nový projekt od Microsoftu, ktorý je možné si nainštalovať vo Windows od verzie 10. Umožnuje spúšťať Ubuntu ako štandardnú aplikáciu. Táto funkcionalita je užitočná pre Vás z niekoľkých dôvodov:
- môžete používať nástroj **Valgrind**, ktorý je určený len pre Linux(a čiastočne Mac OS X)
- môžete sa učiť linuxovú príkazovú riadku z pohodlia domova na svojom vlastnom počítači bez potreby linux reálne inštalovať
- budete mať rovnaké podmienky za akých kompiluje a testuje Vaše úlohy **Kontr**

# Inštalácia {#installation}

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

Ubuntu on Windows má svoj vyhradený priestor oddelený od Windowsu. Pokiaľ chcete pristúpiť k dátam Windowsu, musíte sa presunúť v príkazovom riadku do adresára **/mnt/c/** pomocou príkazu:
```
cd /mnt/c/
```
V priečinku **/mnt/c/** sa nachádza partícia **C:/**. Pre vrátenie sa do domovského adresára Ubuntu použite:
```
cd ~
```

![](/images/ubuntu-on-bash/install_08.png)


# Kam ďalej {#next}

Najdôležitejšia funkcionalita je pre Vás použitie programu Valgrind, ktorý inak na Windowse nespustíte. Pokračujte [návodom na jeho inštaláciu](../valgrind/installation_windows.md).

