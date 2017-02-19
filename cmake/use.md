# Použitie

V PB071 sa odporúča používať Qt Creator, kde typicky len otvoríte dodaný súbor CMakeLists.txt. Pre pokročilých/zvedavých je však priložený návod aj pre command line.

## Qt Creator

Pokračujte návodom na [Qt Creator](../qt-creator/README.md).

## Command line

1. Spustite command line(PowerShell, Bash, ...)
2. Vytvorte folder príkazom **mkdir**, kde sa bude program kompilovať:
   - folder, kde je zdrojový kód nesmie byť rovnaký ako folder, kde sa bude program kompilovať,
   - folder so zdrojovým kódom musí obsahovať CMakeLists.txt .
   
   Typicky sa volí vedľa foldera s kódom, napríklad pre hw01 to bude vyzerať približne takto:

   ```
   PS C:\Users\MatusT\Documents\Projects\pb071-homeworks> mkdir hw01-build
   PS C:\Users\MatusT\Documents\Projects\pb071-homeworks> dir
   Mode                LastWriteTime         Length Name
   ----                -------------         ------ ----
   d-----        2/17/2017  12:39 PM                hw01
   d-----        2/17/2017   1:30 PM                hw01-build
   ```

3. Pomocou príkazu **cd** sa presuňte tam, kde chcete program skompilovať (napr. hw01-build):

   ```
   PS C:\Users\MatusT\Documents\Projects\pb071-homeworks> cd hw01-build
   PS C:\Users\MatusT\Documents\Projects\pb071-homeworks\hw01-build>
   ```

4. Zavolajte príkaz **cmake** s parametrom cesty k zdrojovému kódu (napr. cmake ../hw01/). Výstup by mal byť podobný, ako tu uvedený:

   ```
   PS C:\Users\MatusT\Documents\Projects\pb071-homeworks\hw01-build> cmake ../hw01/
   ...
   -- Build files have been written to: C:/Users/MatusT/Documents/Projects/pb071-homeworks/hw01-build
   ```

5. Zavolajte príkaz **make** na Linuxe/macOS. Na Windows otvorte vygenerovaný .sln súbor 
vo Visual Studio.

# Kam ďalej

Pokračujte návodom na [Qt Creator](../qt-creator/README.md), alebo ak ste zvládli kompiláciu cez command line a nechcete používať IDE, preskočte na [Valgrind a Dr. Memory](../memory-leaks/README.md).