# Git inštalácia - Windows

Stiahnite si inštalátor zo stránky [git-scm.com](https://git-scm.com/).

Pri inštalácii sa uistite, že ste si zvolili:
* Checkout Windows-style, commit Unix-style line endings

Po inštalácii si otvorte command line(PowerShell, Bash, ...) a nastavte si editor, ktorý bude slúžiť na editáciu commit správ, nasledujúcimi príkazmi:
```
git config --global core.editor notepad
# alebo 
git config --global core.editor {editor podľa vášho výberu}
```

Nastavenie zarovnania commit správy:
```
git config --global format.commitMessageColumns 80
```
