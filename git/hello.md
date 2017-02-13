## Hello

na servery aisa alebo linuxovom stroji na FI:
```
# nový clone projektu s SSH
aisa:/home/{xlogin}>$ git clone {URL začínajúce git@}
# nový clone projektu https
aisa:/home/{xlogin}>$ git clone {URL začínajúce https://}
# vstúpenie do adresára s repozitárom
aisa:/home/{xlogin}>$ cd pb071
```

Samotná práca na úlohe

```
# vytvorenie (pod)adresára pre konkrétnu úlohu {hello, hw01, ...)
aisa:/home/{xlogin}/pb071>$ mkdir hello

# vstúpenie do nového adresára
aisa:/home/{xlogin}/pb071/hello>$ cd hello

# vytvorenie zdrojového kódu, (možné použiť aj klasický editor/IDE)
aisa:/home/{xlogin}/pb071/hello>$ nano main.c

# pridanie súboru "main.c" do fázy STAGE
aisa:/home/{xlogin}/pb071/hello>$ git add main.c
# alebo
aisa:/home/{xlogin}/pb071/hello>$ cd ..
aisa:/home/{xlogin}/pb071>$ git add hello/main.c

# výpis stavu lokálneho repozitára
aisa:/home/{xlogin}/pb071>$ git status

# vytvorenie commitu so správou
aisa:/home/{xlogin}/pb071>$ git commit -m "Úloha Hello"

# odoslanie nových commitov na origin (v tomto prípade gitlab) do vetvy master
aisa:/home/{xlogin}/pb071>$ git push -u origin master
```

Po posledom kroku sú zmeny viditeľné v gitlabe, a preto je možné odovzdať úlohu (cez kontr, viď [odovzdávanie](../ssh/linux.html))
