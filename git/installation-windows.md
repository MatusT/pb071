# Git inštalácia - Windows

Stiahnite si inštalátor zo stránky [git-scm.com](https://git-scm.com/).

Pri inštalácii sa uistite, že ste si zvolili:
* Checkout Windows-style, commit Unix-style line endings

Po inštalácii v Power Shelle alebo Príkazovom riadku (alebo Git Bash) je dobré nastaviť si editor, ktorý Git otvorí pri chýbajúcej správe pri commitovaní:

```
git config --global core.editor notepad
git config --global format.commitMessageColumns 80
```
