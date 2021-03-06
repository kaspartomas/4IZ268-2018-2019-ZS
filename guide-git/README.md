## Použití verzovacího nástroje Git pro předmět 4IZ268
Tento návod Ti pomůže s použitím Gitu během předmětu 4IZ268. Hodně štěstí!



### Setup, Ready, Go!
1. Nainstaluj si Git v počítači, pokud ho ještě nemáš -- [https://git-scm.com/downloads](https://git-scm.com/downloads), všude dávej Next.
    - Potom si možná budeš muset přidat cestu k git.exe do PATH pro použití v **`příkazovém okně`**.
2. Registruj se na GitHub, pokud ještě nemáš účet -- [https://github.com/join](https://github.com/join). Zvol si nějaké jednoduché a dobře zapamatovatelné uživatelské jméno.
3. Otevři příkazové okno CMD nebo PowerShell v domovském adresáři, např. v **`C:\Users\User\Projects\`**, 
    - tj. otevřeš tuto složku, podržíš SHIFT, klikneš někam do prázdna pravou myškou a vybereš **Příkazové okno** nebo **PowerShell**. Tahle finta je hodně užitečná.
4. **Naklonuj** si tento repozitář, 
    - tj. spustíš příkaz **`git clone https://{XXXX}@github.com/nvbach91/4IZ268-{YYYY}-{YYYY}-{SS}.git`**, přitom: 
        - nahradíš **`{XXXX}`** svým **username** na github, např. **`nvbach91`**,
        - nahradíš **`{YYYY}-{YYYY}`** aktuálními roky, např. **`2018-2019`**,
        - nahradíš **`{SS}`** buď **`ZS`** nebo **`LS`**,
        - tedy celkem např. **`git clone https://nvbach91@github.com/nvbach91/4IZ268-2018-2019-ZS.git`**,
        - takhle dostaneš adresář s názvem **`4IZ268-2018-2019-ZS`**.
5. **Přesuň se** do tohoto adresáře, 
    - tj. spustíš příkaz **`cd 4IZ268-2018-2019-ZS`**.
6. Vytvořiš si **vlastní branch**, 
    - tj. spustíš příkaz **`git checkout -b student-{xname}`** (nahraď **`{xname}`** svým **xname**).
7. Zveřejníš tuto **branch** a přitom ji nastavíš jako **upstream** u sebe, 
    - tj. spustíš příkaz **`git push --set-upstream student-{xname}`** (nahraď **`{xname}`** svým **xname**).
8. Ve složce **`www`** si vytvoříš svou složku, kterou nazveš svým **xname**, 
    - např. **`C:\Users\User\Projects\4IZ268-2018-2019-ZS\www\nguv03\`**.
9. Sem vložíš své **HTML** soubory a jsi připraven.



### Vývojové prostředí a Git
Pokud sis zvolil nějaké slušné **vývojové prostředí**, např. [VS Code](https://code.visualstudio.com/download), udělal jsi dobře! **IDE** ti totiž bude ukazovat změny v kódu a také se postará o Git příkazy na dva kliky. Viz [https://github.com/nvbach91/4IZ268-2018-2019-ZS/blob/master/guide-uep](https://github.com/nvbach91/4IZ268-2018-2019-ZS/blob/master/guide-uep).



### Standardní proces schválení změn v kódu pomocí příkazů
1. Uděláš nějaké změny v kódu a chceš to uložit na GIT, tak spustíš CMD ve složce tvého projektu.
2. Podíváš se na vyznačené změny, 
    - tj. spustíš příkaz **`git diff`**. Z toho odejdeš pomocí klávesy **`Q`**.
3. Přidáš tyto změny do **fáze** (stage), 
    - tj. spustíš příkaz **`git add -A`**.
4. Potvrdíš tyto změny, 
    - tj. spustíš příkaz **`git commit -m "MESSAGE"`**. Tady místo **`MESSAGE`** napíšeš krátký popis těch změn nebo jejich účel.
5. Pošleš tyto změny na repozitář, 
    - tj. spustíš příkaz **`git push`**. Zadáš heslo a tvůj kód je v cloudu na tvé **branch**i.
6. **Pokud chceš zveřejnit svoje změny na produkci (Pull Request), pokračuj dál, jinak můžeš tady skončit.**
7. Teď mě požádáš o schválení tvých změn na produkci, 
    - tj. jdeš na GitHub repozitář pro tento projekt, najdeš si svou **branch** a uděláš **Pull Request**.
8. Já se na to pak podívám a schválím, 
    - tj. já udělám **review** a **merge** tvé **branch**e na **master branch** a do minuty se to projeví na webu.
9. Zkontroluješ si svůj nový web a budeš šťastný. (Odkaz na tvůj web ti sdělím na cvičení)



### Další postupy v gitu
Většinou budeš chtít synchronizovat svůj projekt, aby byl aktuální s tím, co je na GitHubu. V našem případě to není třeba, jelikož pracuješ pouze v rámci své složky/**branch**e, a to vždy sám. Ale pokud bylo potřeba, tak jsou na to následující příkazy.
- Aktualizace celého projektu nanečisto - **``git fetch``**. Tím se dozvíš, jak daleko jsou na tom tví spolužáci.
- Zjištění názvu **branch**e, na které právě jsi - **`git branch`**
- Aktualizace **branch**e, na které právě jsi - **`git pull`**
- Přechod na jinou existující **branch** - **`git checkout {BRANCH-NAME}`**, místo **{BRANCH-NAME}** dáš název **branch**e
- Aktualizace jiné **branch**e - **`git checkout {BRANCH-NAME}`**, a pak **`git pull`**
- Vytváření nové **branch**e a přechod na ni - **`git checkout -b {BRANCH-NAME}`** // tohle už jsi jednou dělal při prvním nastavení



### Poznámky
- Nemanipuluj se složkami svých spolužáků, jinak ti Pull Request neprojde :)
