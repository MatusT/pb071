## GitLab
GitLab je webový manažer Git repozitářů, podobný známé službě GitHub. Kromě správy repozitářů (které se zde nazývají projekty) umí GitLab zejména také Wiki a Issue tracking.

### Přihlášení
Pokud máte na Fakultě informatiky aktivní účet můžete se přihlásit pomocí LDAP autentizace na následujícím URL:

```
https://gitlab.fi.muni.cz/
```

Zadejte svůj fakultní login a heslo, účet se po prvním přihlášení automaticky vytvoří. Po přihlášení se objeví hlavní přehled účtu, tzv. Dashboard.

Osoby bez fakultního účtu musí požádat o vytvoření externího účtu. Pošlete e-mail se žádostí a odůvodněním správcům. Pro přihlášení pak použijte Standard autentizaci.

#### Platnost účtu
Účet v GitLabu spojený s fakultním účtem je platný pouze pokud je fakultní účet aktivní a neblokovaný. Pokud dojde k zablokování nebo ukončení platnosti fakultního účtu, zablokuje se také přístup do GitLabu včetně SSH klíčů.

### Pravidla používání
* je zakázáno měnit své jméno i přesto, že to GitLab umožňuje
* je zakázano měnit cestu skupiny
* repozitáře nejsou určeny pro vkládání velmi velkých souborů
* limit na velikost repozitáře je 1,5 GB (velikost může snížit funkce Project → Settings → Housekeeping)
* dbejte na dodržování provozních pravidel

### SSH klíč
Pokud chcete pracovat s repozitářem ze svého počítače bez nutnosti pokaždé zadávat heslo, můžete si do svého profilu nahrát veřejný SSH klíč. Postupujte podle návodu, zde uvedeme pouze shrnutí pro UN*X systémy.

#### Vytvoření SSH klíče
Do terminálu napište:
```
mkdir -p ~/.ssh && cd ~/.ssh
ssh-keygen -t rsa -b 4096 -f id_gitlab -C "popis klíče"
```

Program pak požádá o zadání hesla pro privátní klíč. Toto heslo zadávat nemusíte, ale obecně je doporučeno klíče heslem chránit.

V adresáři vzniknou dva soubory, id_gitlab.pub (veřejný klíč) a id_gitlab (privátní klíč). Privátní klíč nikam nekopírujte a nezveřejňujte jej.

#### Vložení klíče do GitLabu
Z Dashboard na levém panelu vyberte Profile settings → SSH Keys. Zde do textového pole Key zkopírujte veřejný klíč (id_gitlab.pub). Pokud máte nainstalovaný program xclip, můžete použít příkaz
`xclip -selection c id_gitlab.pub`
Pole Title by se mělo vyplnit automaticky podle klíče, pokud se tak nestane, vyplňte jej sami. Poté klikněte na Add key.

#### Použití klíče
Otestovat funkčnost klíče můžete příkazem `ssh -i ~/.ssh/id_gitlab git@gitlab.fi.muni.cz`. Výstup příkazu by měl být podobný následujícímu:
```
Welcome to GitLab, (Jmeno, Prijmeni)
Connection to gitlab.fi.muni.cz closed.
Klíč bez hesla
```
Přidejte následující řádky do ~/.ssh/config (soubor nemusí dosud existovat):

```
Host gitlab gitlab.fi.muni.cz
    HostName gitlab.fi.muni.cz
    IdentityFile ~/.ssh/id_gitlab
```
Význam jednotlivých řádků viz ssh_config(5). Vyzkoušejte, že příkaz ssh git@gitlab má stejný výstup jako výše i bez explicitního uvedení klíče.

#### Klíč s heslem
Pokud jste privátní klíč vytvořili s heslem, můžete aplikovat stejný postup jako pro klíč bez hesla, ale heslo bude požadováno při každém použití klíče. S pomocí SSH agenta lze klíč odemknout pouze jednou a pak používat opakovaně:

```
ssh-agent $SHELL
ssh-add ~/.ssh/id_gitlab
```
První příkaz spustí agenta, který pak spustí nový shell z proměnné $SHELL. Pokud váš shell tuto proměnnou nenastavuje, zadejte místo ní cestu k programu (např. /bin/sh). Ukončením shellu se ukončí i agent.

Druhý příkaz odemkne klíč a předá jej agentovi. Klíč bude platný pouze do ukončení agenta. Platnost také můžete omezit přepínačem -t LIFETIME (viz ssh-add(1)).

Pozor, ve starší verzi této dokumentace a na různých diskuzních fórech lze najít postup, který používá příkaz eval $(ssh-agent -c) nebo jemu podobný. Nedoporučujeme tento postup používat, protože nezaručuje korektní ukončení agenta.

## Zřízení repozitáře
Projekt můžete vytvořit z hlavní stránky (Dashboard) nebo ze seznamu projektů kliknutím na New Project. Pak vyplňte informace o projektu:

* Project path (rozbalovací menu): umístnění projektu; pokud jste členem skupiny, pak zde můžete vytvořit projekt i v dané skupině,
* Project path (textové pole): cesta k projektu; bude součástí URL, proto volte ve tvaru nazev-projektu bez diakritiky a se spojovníky místo mezer,
* Description: nepovinný popis projektu; může obsahovat Markdown formátování,
* přístup k projektu; zvolte **Private**: přístupný pouze vám (nebo skupině, pokud je v ní projekt umístěn) a všem lidem, kterým k projektu explicitně povolíte přistup,
* pridelenie práva skupine *pb071*
* klikněte na Create Project

* Klonování a první commit
* Po vytvoření repozitáře se dostanete na stránku projektu. Pod názvem projektu naleznete URL pro přístup k projektu přes HTTPS (nebo SSH, pokud máte v účtu zaveden SSH klíč).

Zkuste z terminálu:
```
# bez SSH klíče
git clone "https://gitlab.fi.muni.cz/kde/repozitar.git"

# s SSH klíčem
git clone "git@gitlab.fi.muni.cz:kde/repozitar.git"
```
Tím vznikne adresář repozitar. Zkuste v něm vytvořit soubor README.md:

```
cd repozitar
cat > README.md &lt;&lt;EOL
# Readme k projektu

Tento soubor může používat **formátování** pomocí _Markdown_.
Viz také [manuál](http://doc.gitlab.com/ce/markdown/markdown.html).
EOF
```
Nový nebo změněný soubor připravte ke commitu, udělejte commit a pak push.

```
git add README.md
git commit -m "ZPRAVA"      # pokud chybí -m "ZPRAVA", otevře se editor
git push
```
Na GitLabu obnovte stránku, měli byste vidět soubor README.md a jeho obsah zobrazen pod popisem projektu. Zkuste jej nyní změnit: Files → README.md → Edit (vpravo). Přidejte libovolný text a klikněte na Commit Changes. Pak se vraťte na hlavní stránku projektu (levý panel Project) a uvidíte změněné README.md.

Upravenou verzi souboru stáhnete do svého repozitáře příkazem git pull.

Sdílení repozitáře
Pokud chcete zpřístupnit repozitář dalším lidem nad rámec "viditelnosti" projektu (Private, Internal nebo Public), můžete je nastavit jako členy (members) projektu.
z hlavní stránky projektu klikněte v levém panelu na Members,
do pole People zadejte jména uživatelů, kterým chcete přidat práva,
vyberte v Project Access oprávnění pro tyto osoby; přehled práv:
Guest: může vytvářet Issues nebo komentáře,
Reporter: může si projekt stáhnout pomocí git pull,
Developer: může do projektu přispívat pomocí git push,
Master: může přidávat a ubírat členy projektu a měnit nastavení,
Owner: může přesunout nebo smazat projekt
Celý seznam práv pro jednotlivé role viz manuál. Nikdy nedávejte jiným lidem právo Master ani Owner, pokud si nejste zcela jisti, co děláte!
Pokud chcete zpřístupnit privátní nebo interní projekt osobě bez fakultního účtu a dané osobě stačí pouze přístup pro stáhnutí projektu (tj. nepotřebuje přístup k Issues, Wiki atd.), můžete použít Deploy keys (v podstatě read-only přístup k projektu pomocí SSH klíče). Pokud se požaduje přístup k dalším službám nebo možnost do projektu přispívat, musí se projekt zveřejnit nebo se musí pro osobu vytvořit externí účet (žádejte u správců).
