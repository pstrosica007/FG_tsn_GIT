# Úvod
Poďme pokecať o git repositorz. Prečo ho naozaj potrebujeme, prečo tu a prečo teraz. 
Rýchle vhľad do tejto problematiky a (nielen) základov gitovania.

## Ciele
1. pokecať tak technicky bez pracovného stresu z nedokončenej práce..tá na chvíľku počká
2. presvedčiť (snáď aspoň niekoho) o kráse a doležitosti gitu a prípadne k ďalšiemu učeniu na udemy či youtube atd.
3. ako sa hovorí sharing is caring...sdieľanie teraz už vtipných príbehov 

## Štruktúra FG workshopu

## Prečo GIT? 
**_GIT definícia_**

GIT je svetovo najpopulárnejším distribuovaným systémom na správu verzií.

_Version control = tracking and managing changes to files over time_

**_plusy & mínusy ... sloboda alebo anarchia??_**

PLUS:  jednoduchý = nemá pravidlá (proces sa dohodne v týme/organizácii)

PLUS: nekomplikovaný = súbory, ktoré nechcem verzovať proste zadám názvami do jedného súboru .gitignore a viac neriešim

PLUS: flexibilný = verzujeme a porovnávame zmeny medzi verziami, rýchle vrátenie zmien = paralelná práca na róznych oddelených vetvách 
(branches)

PLUS: (ne)sdieľanie s týmom

PLUS: nevyhnutný = veľa súborov vs. veľa programátorov

![Snímek obrazovky 2023-07-27 v 22 59 03](https://github.com/pstrosica007/FG_tsn_GIT/assets/89271768/1fbcd339-a6b5-4dbe-81cf-25bdb343854e)


PLUS: decentralizovaný = každá kópia repository je jeho klonom (teda plnohodnotným repository) a može kedykoľvek nahradiť povodné repo = 
práve sme vylúčili single point of failure :)

PLUS: rýchlosť = možnosť práce v local repository

PLUS: rozmanitost použitia = malé i velké projekty

PLUS: gitshell & web app / unix, win, mac

MÍNUS: naozaj jednoduchý?

Flexibila používania GIT verzovacieho systému dáva priestor ľudovej tvorivosti. Veľa možností a kombinácií postupov umožňuje až nechcenú kreativitu. Nebudem ani počítať koľkokrát som prišla o kód (často svojou hlúposťou samozrejme ale aj ignoráciou kolegov v týme). 
Je dóležité vzdelávať sa aj v tak jednoduchom jazyku ako je gitshell, v týme si dohodnúť pravidlá a v najlepšom prípade sa pri niektorých krokoch dvakrát zamyslieť. Využívať pomocné pluginy v tooloch ako je napríklad PyCharm (neskor upresním), čistit pravidelne branche(verzie) lokálne aj remote a písať jasné krátke komentáre pri sdieľaní zmien do repa.

MÍNUS: naozaj zadarmo?

Na stránkach GIT doc https://git-scm.com/about/free-and-open-source sa píše zadarmo. GIT teda bude zadarmo, ale v organizácii vačšinou máte server (unix), ktorý niečo stojí. Potom ten server potrebuje software, ktorý možno niečo stojí (CENTOS, REDHAT - licencia?). V neposlednej rade potrebujete niekoho, kto sa postará o HW a SW. Prípadne vyrieši zálohovanie. Okrem ľudí potrebujete aj proces a monitoring. Server potrebujete mať v sieti. Potrebujete splňovať security požiadavky (pravdpodobne udržujete doležité firemné informácie). Potrebujete aktualizovať GIT a starať sa o správu aplikácie. Takže mať/používať verzovací systém reálne vždy niečo stojí. Je ale fajn, že samotný GIT je open source.

MÍNUS: a prečo GIT?
A prečo uprednostniť GIT? Popravde nemám skúsenosť s iným verzovacím systémom. V žiadnej firme som sa  ničím iným nestretla a ani to neočakávam. Je to podobné ako používať confluence pre dokumentáciu ak už máte JIRU. V dnešnom IT svete je repo nevyhnutnosť a preto je veľmi pravdepodobné, že stretnete na pohovoroch do týmu ľudí, ktorý sa s ním stretli. A keď náhodou nie, tak je jednoduché ich to naučiť. Prípadne návrat na výčet PLUSov by mohol pomocť.

GITLAB vs. GITHUB : https://www.geeksforgeeks.org/difference-between-gitlab-and-github/

![Snímek obrazovky 2023-07-27 v 21 56 19](https://github.com/pstrosica007/FG_tsn_GIT/assets/89271768/a341aa42-64b5-45e8-b410-a4496c7e0fea)


### Ako sa pracuje s GITom / procesy

![Snímek obrazovky 2023-07-27 v 22 56 58](https://github.com/pstrosica007/FG_tsn_GIT/assets/89271768/09cc2f4f-cbda-4396-b141-6e5554c1a7e7)

```
LOKAL REPO DEV: 
# Vytvorime si branch "featur z aktualnej master branch na doplnenie/fix kodu
$ git checkout master
$ git checkout -b feature1
$ git add private/*
$ git commit -m "conf feature1"
$ git push

LOKAL REPO TESTER:
# Vytvorime si branch "test1" na otestovanie feature1
$ git checkout feature1
$ git checkout -b test1
# ... Pracujeme, testujeme, klejeme

LOKAL REPO DEV:
# chyby predáme na dev, ktory opravi feature1
$ git checkout feature1
$ git add private/server_xfr_network_setup

# ulozenie opravy do repo
$ git commit -m "fix ssh-key setup server xfr"
$ git push

LOKAL REPO TESTER:
# stiahneme si update feature1 .. mozny postup 1
$ git pull
$ git checkout test1
$ git rebase origin/feature1
$ git push origin HEAD --force
# ... Pracujeme, testujeme, klejeme

# Vytvorime si branch "test2" na otestovanie feature1 .. mozny postup 2
$ git pull
$ git checkout feature1
$ git checkout -b test2
# ... Pracujeme, testujeme, klejeme

# DEV - PROD 
$ git checkout master
$ git merge feature1
$ git push origin master 
```
### GIT basics
### GIT specialities
### some hints (still not the end)
### some curiosities
### and some talk (this is the end)




