# Virtuálny stroj - Lubuntu 16.04 LTS

Kvôli prípadným problémom na vlastných strojoch, Vám dávame k dispozícii virtuálny stroj s prednastaveným Linuxom.

# Stiahnutie VirtualBox

* Stiahnite z: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
* Virtuálna verzia bola vyrobená na verzii _5.2.14_
* Nainštalujte si verziu pre svoj daný operačný systém.
* Pre viac informácii ako postupovať a ovládať virtual box:
  * [https://www.virtualbox.org/manual/ch01.html](https://www.virtualbox.org/manual/ch01.html)
  * návody na internete.

## Stiahnutie stroja

* Aktuálne na MEGA: 
  * [https://www.fi.muni.cz/pb071/download/ubuntu\_machine.zip](https://www.fi.muni.cz/pb071/download/ubuntu_machine.zip)
  * ide o zip archív, ktorý je potrebné rozbaliť. Vo vnútri sa nachádza súbor **VDI.**

## Nastavenie virtuálneho stroja - referenčné

* Processor: 2 jadrá \(staršie stroje kľudne jedno - budú ale pomalšie\)
* RAM: 2 GB
* Grafická pamäť: 64MB 
* Disk: Treba zadať cestu k stiahnutému VDI disku.

## Virtuálny stroj

* Užívateľ: _user \(Autologin\)_
* Heslo: _user_
* Root heslo: _toor _\(root naopak\)
* SSH port: 22

### Verzie nástrojov

* GCC - 5.4.0
* GDB - 7.11.1
* CLANG  - 3.8.0
* CMAKE - 3.5.1
* QtCreator - 3.5.1
* Valgrind - 0.6.7

## Obrázky

Takto nejak bez virtuálnych strojov by mal vyzerať váš virtual box.![](/images/virtual_machine/virtual_box_main_window.png)

Kliknete na na **New.**

![](/images/virtual_machine/NameOfTheMachine.png)

Pomenujte si nejak váš stroj.

![](/images/virtual_machine/MemorySize.png)

Pridelte mu pamäť - 2 GB je optimum.

![](/images/virtual_machine/SelectVirtualDrive.png)

Vyberte poslednú možnosť, kliknite na zložku a nájdite extrahovaný virtuálny disk. A kliknite na **Create**.

Následne otvorte **Settings** pre aktuálne vytvorený disk.

![](/images/virtual_machine/SystemProc.png)

Na karte **System** prideľte rozumné množstvo jadier.

![](/images/virtual_machine/DisplayMemory.png)

Na karte **Display** nastavte optimálne veľa **Video memory**, napríklad 64 MB.

A je to, stroj by mal byť nastavený a pripravený na spustenie.

