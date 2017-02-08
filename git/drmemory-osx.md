### DrMemory on OSX

Inštalačný súbor si stiahnite [TU](https://github.com/DynamoRIO/drmemory/wiki/Downloads).

Otvorte **Terminál**, a presunte sa do priečinku **Downloads**\[Stiahnuté\], prípadne priečinok, v ktorom sa nachádza stiahnutý instalačný súbor. Preveďte nasledujúcu postupnosť krokov.

```terminal
tar xzf DrMemory-MacOS-X.X.X-X.tar.gz
mv DrMemory-MacOS-X.X.X-X drmemory
sudo mv drmemory /usr/local/
```

Následne modifikujeme Shellovskú PATH, aby sa nám DrMemory lahšie spúšťal.

```terminal
cd
nano .bash_profile
```

Otvorí sa súbor .**bash\_profile** pripravený pre editovanie. Ak už tento súbor niečo obsahuje, nemažte to.   
Do súboru vložte nasledovný riadok \(stačí bežným skopírovaním\)

```terminal
export PATH="/usr/local/drmemory/bin/:$PATH"
```

Stlačte _ctrl + o, následne Enter,_ na potvrdenie uloženia zmien. Potom stlačte _ctrl+x_, čím opustíte súbor a jeho editovanie.

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

Predpokladajme program pozostávajúci z jediného súboru** main.c**. Prítomnosť memory leakov vo vašom programe otestujete nasledovne.

```terminal
gcc -m32 -g -fno-inline -fno-omit-frame-pointer main.c -o main
drmemory -- main
```

Za príkaz gcc môžete samozrejme pridať flagy ako -Wextra atď, pre zjednodušenie sa tam nenachádzajú. 

