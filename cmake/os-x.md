### Inštalácia Cmake na OS X

* #### Ak máte nainštalovaný Homebrew:

Otvorte terminál, a postupujte nasledovne

```termnal
brew install cmake
```
Je pravdepodobné, že brew nepridal cmake do vašej PATH. Otvoríme teda súbor _.bash_profile_ a pridáme cmake do vašej PATH.

```terminal
cd
nano .bash_profile
```


Otvorí sa súbor .**bash\_profile** pripravený pre editovanie. Ak už tento súbor niečo obsahuje, nemažte to.  
Do súboru vložte nasledovný riadok \(stačí bežným skopírovaním\).

```terminal
export PATH="/usr/local/Cellar/cmake/3.7.2/bin:$PATH"
```


Stlačte **ctrl + o**, následne **Enter**,  na potvrdenie uloženia zmien. Potom stlačte** ctrl+x**, čím opustíte súbor a jeho editovanie.

Pred použitím cmake otvorte nové \(tento krok je podstatný!\).  



TODO?
Stiahnut [TU](https://cmake.org/download/).
