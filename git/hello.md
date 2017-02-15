## Hello

Na servery aisa alebo linuxovom stroji na FI:
```
# nový clone projektu s SSH
aisa:/home/{xlogin}>$ git clone {URL začínajúce git@}
# nový clone projektu https
aisa:/home/{xlogin}>$ git clone {URL začínajúce https://}
# vstúpenie do adresára s repozitárom
aisa:/home/{xlogin}>$ cd pb071
```
Príkazmi ste si spravili lokálnu verziu repozitára.


Samotná práca na úlohe
```
# vytvorenie (pod)adresára pre konkrétnu úlohu {hello, hw01, ...)
# a vstúpenie do nového adresára
aisa:/home/{xlogin}/pb071>$ mkdir hello
aisa:/home/{xlogin}/pb071>$ cd hello

# vytvorenie zdrojového kódu, (možné použiť aj klasický editor/IDE)
aisa:/home/{xlogin}/pb071/hello>$ nano main.c

# pridanie súboru "main.c" do fázy STAGE
aisa:/home/{xlogin}/pb071/hello>$ git add main.c
# alebo
aisa:/home/{xlogin}/pb071/hello>$ cd ..
aisa:/home/{xlogin}/pb071>$ git add hello/main.c

# výpis stavu lokálneho repozitára
aisa:/home/{xlogin}/pb071>$ git status

# vytvorenie commitu, "vytvorenie bodu aktuálne pridaných súborov"
# (ak nezadáte -m "správa", otvorí sa vám editor kde treba napísať správu a súbor uložit a editor ukončiť)
aisa:/home/{xlogin}/pb071>$ git commit -m "Úloha Hello"

# odoslanie nových commitov na remote (v tomto prípade gitlab) do vetvy master
aisa:/home/{xlogin}/pb071>$ git push -u origin master
```

Po posledom kroku sú zmeny viditeľné v gitlabe, a preto je možné odovzdať úlohu (cez kontr, viď [odovzdávanie](../ssh/linux.html))

### Ak pokračujete stále na tom istom PC (resp, na fakultných PC, stále s rovnakým OS), stačí držať sa týchto krokov:
* programovať, testovať,
* po dokončení nejakej časti, `git add`, `git commit` s rozumnou správou, nakoniec `git push`.


### Ak pracujete na rôznych PC:
* pred začatím, stiahnuť si zmeny z GitLab-u, pomocou `git pull`
* programovať, testovať,
* po dokončení nejakej časti, `git add`, `git commit` s rozumnou správou, nakoniec `git push`.


