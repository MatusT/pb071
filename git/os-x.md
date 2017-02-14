### Inštalácia Cmake na OS X

* #### Ak máte nainštalovaný Homebrew:

Otvorte terminál, a postupujte nasledovne

```termnal
brew install cmake
cd
```
Je pravdepodobné, že brew nepridal cmake do vašej PATH. Otvoríme teda súbor

```terminal
nano .bashr_profile
export PATH="/usr/local/Cellar/cmake/3.7.2/bin:$PATH"
```




Stiahnut [TU](https://cmake.org/download/).

