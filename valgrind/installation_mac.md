# Valgrind na Mac OS X {#intro}



Máte dve možnosti

* Ak ste si nainštalovali alebo nainštalujete [Homebrew](/qt-creator/homebrew-for-os-x.md), otvorte terminál a napíšte:

```terminal
brew install valgrind
```

Pozor! Ak máte nainštalovanú najnovšiu nerziu OS X Sierra, je možné, že brew zlyhá s hláškou 

```terminal
versions newer than El Capitan due to an upstream incompatibility.
Error: An unsatisfied requirement failed this build.
```

V tomto prípade použite druhú možnosť inštalácie.

* Ak Homebrew nemáte, stiahnite si inštalačnú binárku pre [Vallgrind](http://valgrind.org/downloads/).

Pozor! limited support for 10.11 and 10.12

Otvorte stiahnutý súbor a dekomprimujte ho.

![](/assets/OSX_valgrind1.png)

Na vzniknutý priečinok kliknite pravým klikom a vyberte možnosť_ Get Info._

![](/assets/OSX_valgrind2.png)

V otvorenom okne zistíte, kde máte súbor uložený. 

![](/assets/OSX_valgrind3.jpg)

Otvorte terminál.



V príklade je cesta k priečinku : **/Users/Kejsty/Downloads/valgrind/**  
a názov priečinku **valgrind-3.12.0**

Napíšte: 

```terminal
cd /Users/Kejsty/Downloads/valgrind/valgrind-3.12.0
./configure
make
```

A dúfajte, všetko prebehne v poriadku.

Možné errory, na ktoré som narazila ja:

1.

```terminal
No rule to make target `/usr/include/mach/mach_vm.defs', needed by `m_mach/mach_vmUser.c'
```

riešenie:

```terminal
xcode-select --install
```



2.

```
Undefined symbols for architecture x86_64: 
 
   "___bzero", referenced from:
       _hijack_thread_state in libcoregrind-amd64-darwin.a(libcoregrind_amd64_darwin_a-syswrap-amd64-darwin.o)  
       _RRegUniverse__init in libvex-amd64-darwin.a(libvex_amd64_darwin_a-host_generic_regs.o) 
```

riešenie:

V priečinku s binárkami valgrindu otvorte **coregrind/m\_main.c **a za všetky include vložte:

```C
#if defined(VGO_darwin) && DARWIN_VERS >= DARWIN_10_10 

/* This might also be needed for > DARWIN_10_10, but I have no way 
    to test for that.  Hence '==' rather than '>=' in the version 
    test above. */ 
void __bzero ( void* s, UWord n ); 
void __bzero ( void* s, UWord n ) 
{ 
    (void) VG_(memset)( s, 0, n ); 
} 

#endif 
```

Obecná rada: googlite.

