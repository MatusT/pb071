# Valgrind na Windows {#intro}

Najprv potrebujete program **Ubuntu on Windows**. Ak ho nemáte, začnite [tutoriálom na Ubuntu on Windows](../ubuntu-on-bash/README.md). Pokiaľ už máte Ubuntu nainštalované, spustite ho.

1. Najprv nainštalujte sadu nástrojov na kompiláciu:
  ```
  sudo apt install wget tar git gcc make
  ```
  
2. Stiahnite Valgrind 3.12.0 príkazom:
   ```
   wget http://valgrind.org/downloads/valgrind-3.12.0.tar.bz2
   ```
   
3. Extraktujte zdrojový kod príkazom:
   ```
   tar -xjf valgrind*
   ```
   Tento krok môže trvať pár minút.
   
4. Vstúpte do adresára valgrindu:
   ```
   cd valgrind*
   ```
   ![](/images/valgrind/install_09.png)
   
5. Spustite automatickú konfiguráciu príkazom:
   ```
   ./configure
   ```
   
6. Skompilujte a nainštalujte Valgrind:
   ```
   make && sudo make install
   ```
   
7. Reštartujte Ubuntu on Windows a overte, že valgrind je nainštalovaný:
   ```
   valgrind --version
   ```
   Výstupom by malo byť:
   ```
   valgrind-3.12.0
   ```
   

# Kam ďalej {#next}

