# Vývojárske nástroje

Všetky kompilačné nástroje môžete nainštalovať príkazom

```
sudo apt install git make cmake gcc g++ gdb doxygen ssh
```

# Valgrind

Valgrind je nutné si skompilovať.

1. Stiahnite zdrojové súbory  valgrindu
   ```
   wget http://valgrind.org/downloads/valgrind-3.12.0.tar.bz2
   ```
   
2. Rozbaľte ich
   ```
   tar xjf valgrind*
   ```
   
3. Vstúpte do foldera valgrindu
   ```
   cd valgrind*
   ```
   
4. Zavolajte postupne príkazy na kompiláciu (ich vykonanie môže chvíľu trvať)
   ```
   ./configure
   make
   sudo make install
   ```
   
5. Reštartujte *Ubuntu on Windows*

