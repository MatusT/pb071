# Dr. Memory on macOS

Inštalačný súbor si stiahnite [https://github.com/DynamoRIO/drmemory/wiki/Downloads](https://github.com/DynamoRIO/drmemory/wiki/Downloads). ([Priamy link](https://github.com/DynamoRIO/drmemory/releases/download/release_1.11.0/DrMemory-MacOS-1.11.0-2.tar.gz))

Ovorte **terminál**. Ten nájdete v časti **Launchpad &gt; Others** alebo pomocou rýchleho vyhladávania: stlačte **⌘+Space **a napíšte Terminal.

![](/assets/OSX_terminal.png)

Presuňte sa do priečinku **Downloads**, prípadne do priečinku, v ktorom sa nachádza stiahnutý inštalačný súbor \(Pomocou príkazov cd {directory}\).
Preveďte nasledujúcu postupnosť krokov:
>**Pozor**! X.X.X-X bude nahradené vašou aktuálne stiahnutou verziou.

```terminal
tar xzf DrMemory-MacOS-X.X.X-X.tar.gz
mv DrMemory-MacOS-X.X.X-X drmemory
sudo mv drmemory /usr/local/
```

Následne modifikujeme shellovskú **PATH**, aby sa nám Dr. Memory lahšie spúšťal.

```terminal
cd
nano .bash_profile
```

Otvorí sa súbor .**bash\_profile** pripravený pre editovanie. Ak už tento súbor niečo obsahuje, nemažte to.  
Do súboru vložte nasledovný riadok \(stačí bežným skopírovaním\):

```terminal
export PATH="/usr/local/drmemory/bin/:$PATH"
```

Stlačte **ctrl+o**_, následne _**Enter**_,_ na potvrdenie uloženia zmien. Potom stlačte** ctrl+x**, čím opustíte súbor a jeho editovanie.

Zavrite toto terminálove okno a otvorte nové \(tento krok je podstatný!\).  
Napíšte do terminálu

```termi
drmemory
```

Mali by ste obdržať správu nasledujúceho formátu:

```terminal
WARNING: this version of Mac OSX is not officially supported by Dr. Memory.

ERROR: no app specified

Usage: drmemory [options] -- <app and args to run>
Run with -help for full option list.
See http://drmemory.org/docs/ for more information.
```

#### Použitie DrMemory

Predpokladajme program pozostávajúci z jediného súboru** main.c**. Prítomnosť memory leakov vo vašom programe otestujete nasledovne. Flagy** -m32 -g -fno-inline -fno-omit-frame-pointer **sú pre kompiláciu potrebné a binárka skompilovaná bez nich nemusí byť validným vstupom pre aplikáciu Dr. Memory.

```terminal
gcc -m32 -g -fno-inline -fno-omit-frame-pointer main.c -o main
drmemory -- main
```

Za príkaz gcc môžete samozrejme pridať flagy ako -Wextra atď., pre zjednodušenie sa tam nenachádzajú.

