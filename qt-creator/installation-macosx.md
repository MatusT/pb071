## Inštalácia Qt na Mac OS X

Inštalačný súbor si stiahnite na [tejto](https://www.qt.io/download-open-source/) stránke. Kliknite na **Download Now**.

![](/assets/OSX_install0.jpg)

Otvorte stiahnuty súbor dvojklikom.

![](/assets/OSX_install1.jpg)

Dvojklikom na zelenú ikonku _Qt_ otvorte aplikáciu pre inštaláciu Qt creatoru \(1\). Kliknutím na _Open_ potvrďte jej otvorenie \(2\).

![](/assets/OSX_install2.jpg)

Otvoril sa vám sprievodca inštaláciou. Kliknite na **Continiue**.

![](/assets/OSX_install3.jpg)

Inštalátor vám v ďaľšom kroku ponúkne registráciu, ktorá nie je povinná a je možné ju preskočiť. V prípade, že sa rozhodnete túto možnosť využiť, účet Vám poslúži na prihlasovanie sa do [Qt Wiki](https://www.gitbook.com/book/matust/pb071-tutorials/edit#) a [Qt Fóra](https://www.gitbook.com/book/matust/pb071-tutorials/edit#).

![](/assets/OSX_install4.jpg)

Pokračujte dalej inštaláciou \(výber súboru pre inštaláciu, ..\), až kým sa nedostanete k časti výberu komponent, ktoré sa majú nainštalovať, viď obrázok nižšie. Rozbalte **Qt 5.8** a vyberte jedinú možnosť a to macOS**. **Pokračujte ďalej.

![](/assets/OSX_install5.png)

Počkajte, kým sa stiahnú potrebné súbory pre inštaláciu. Táto časť môže zabrať dlhší čas. Po dokončení inštalácie môžete spustiť vaše novo nainštalované IDE.

![](/assets/OSX_install6.jpg)

{% include "./installation-next.md" %}

## Pridanie Cmake do Qt

Najprv sa uistite, že máte nainštalovaný cmake, napríklad pomocou toho, že do terminálu napíšete:

```terminal
which cmake
```
Ak nie, cmake si nainštalujte napríklad podľa [návodu](/cmake/installation-macos.md).

Otvorte aplikáciu. V hornom menu vyberte možnosť **Qt Creator &gt Preferences... &gt Build & Run &gt CMake** a vyberte možnosť **Add**.

Ako meno zvolte ľubovoľný identifikátor pre CMake, pokojne nechajte pôvodný. Do path vložte cestu, ktorú vám povie terminál po zadaní 

```terminal
which cmake
```

![](/assets/CmakeQtOsx3.jpg)


## Pridanie Kompilátoru do Qt

V tomto predmete budeme používať kompilátor gcc. Uistite sa preto najprv, že tento kompilátor máte, napríklad napíšte do terminálu:

```terminal
which gcc
```
V opačom prípade si ho nainštalujte.

Otvorte aplikáciu. V hornom menu vyberte možnosť **Qt Creator &gt Preferences... &gt Build & Run &gt Compilers** a skontrolujte, že vo výbere sa GCC nachádza.

![](/assets/CmakeQtOsx2.jpg)

Následne otvorte záložku Kits a skontrolujte, že váš Kit má ako defaultný kompilátor pre C práve GCC.

Ak nie, odporúčam vytvoriť nový Kit. V záložke Kits kliknite na **Add** a novo pridaný Kit vyplnte nasledovne.

![](/assets/CmakeQtOsx4.jpg)


