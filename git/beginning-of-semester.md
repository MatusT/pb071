## Začiatok semestra

Po inštalácii Git-u, je potrebné sa prihlásiť na fakultný GitLab.

Na odovzdávanie úloh si budete musieť vytvoriť repozitár `pb071` a v nastaveniach (ozubené koliesko vpravo hore) v `Members → Share project with other groups` nastaviť skupine `pb071` práva `Reportér`. 

Každá úloha bude pozostávať z adresáru s názvom úlohy (napr hw01 alebo hw02) a v ňom súbory ktoré budú popísané v zadaní.

```
pb071
├── hw01
│   ├── main.c
│   ├── main.h
│   ├── nieco.c
│   └── nieco.h
└── hw02
    ├── main.c
    ├── main.h
    ├── nic.c
    └── nic.h
```

**Nezabudnite ze projekt musí byť private.** V nastaveniach `Edit project → Project Visibility:private` https://gitlab.fi.muni.cz/xlogin/pb071/edit

Viac informácií o fakultnom gitlabe nájdete na stránke [https://gitlab.fi.muni.cz](https://gitlab.fi.muni.cz)

### (Dobrovoľné) vytvorenie SSH kľúča
[oficiálny návod](https://docs.gitlab.com/ce/ssh/README.html), po nastavení ssh kľúča, pri zmeách sa nebude od vás
vyžadovať xlogin a heslo (pri `git pull`, `git push`), ale na autentizaciu sa použije asymetrický kľúč.
