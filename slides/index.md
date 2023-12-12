
### Git workshop 

<img src="./img/DragonSec_logo.png" alt="logo" title="Logo" width="300"/> 

Ljubljana FRI, December 2023

---
### Kdo smo <!-- .element: style="text-align: left; font-size: 50px;" -->
<style>
.container{
    display: flex;
}
.col{
    flex: 1;
}
</style>

<div class="container">

<div class="col">

<div style="display: flex; align-items: center;"><img src="./img/github-light.png" alt="logo" title="Logo" width="50" style="margin-right: 10px;" /><b>DragonSec SI</b> </div>
<div style="display: flex; align-items: center;"><img src="./img/twitter-light.png" alt="logo" title="Logo" width="50" style="margin-right: 10px;" /><b>@DragonSec_SI</b> </div>
<div style="display: flex; align-items: center;"><img src="./img/mail-light.png" alt="logo" title="Logo" width="50" style="margin-right: 10px;" /><b>info@dragonsec.si</b> </div>


</div>
<!-- .element: style="width: 100%;" -->

<div class="col">

<img src="./img/about-us.jpg" alt="logo" title="Logo" width="400"/> 

</div>

---
### GIT

Kaj sploh je git?

<img src="./img/git-logo.png" alt="logo" title="Logo" width="300"/>

Note: Predstavljaj si, da gradiš stolp iz lego kock. Vsakič, ko dodaš novo kocko, stolp postane malo višji. 
Včasih pa morda dodaš kocko, ki ti ne ustreza ali pa celo zruši stolp. Kako bi bilo super, če bi lahko shranil, kako je stolp izgledal na vsaki stopnji, 
tako da bi se lahko vedno vrnil nazaj, če nekaj ne bi delovalo, kajne?

Git je kot čarobna škatla za shranjevanje vsake faze tvojega lego stolpa. 
Vsakič, ko dodaš pomembne kocke (ali spremembe) na svoj stolp (ki je tukaj tvoj projekt ali delo), lahko "shraniš" kako izgleda. 
To imenujemo "commit". Če kasneje nekaj gre narobe, lahko uporabiš Git, da se vrneš nazaj do ene od teh shranjenih točk, kjer je bilo vse v redu.

Poleg tega, če imaš prijatelje, ki ti pomagajo graditi stolp, lahko Git pokaže, kdo je dodal katere kocke in kdaj. 
To pomaga, da vsi vedo, kaj se dogaja z stolpom in kako raste.

Torej, Git je kot čarobna škatla, ki ti pomaga shraniti vsak korak pri gradnji tvojega lego projekta, 
in ti omogoča, da se vrneš nazaj, če nekaj gre narobe ali če želiš videti, kako je projekt izgledal v preteklosti.


---
### GIT vs. GITHUB

<img src="./img/git-github.png" alt="logo" title="Logo" width="1000"/>

Note: Git je sistem za nadzor različic, ki lokalno sledi spremembam v datotekah, običajno v kontekstu razvoja programske opreme. 
Omogoča razvijalcem, da ustvarijo "commits" ali zapiske o spremembah, ki so jih naredili v svojih datotekah. 
Prav tako omogoča povrnitev datotek na prejšnje stanje in ogled zgodovine, kdo je kdaj naredil kakšno spremembo. 
Git je orodje, ki se uporablja na lokalnem računalniku in je neodvisno od interneta ali centraliziranega strežnika.

GitHub pa je spletna platforma, ki gosti Git skladišča in dodaja funkcije za sodelovanje, kot so upravljanje nalog, 
zahteve za prevzem (pull requests), in pregledovanje kode. GitHub je kot socialno omrežje za razvijalce, 
kjer lahko shranjujejo svoje projekte (skladišča), sodelujejo z drugimi in delijo svojo kodo z javnostjo ali v privatnih skupinah. 
GitHub deluje v oblaku in je dostopen preko spleta.

Ključna razlika je torej ta, da je Git orodje, ki deluje lokalno in omogoča nadzor različic, 
medtem ko je GitHub spletna storitev, ki gradi na Gitu in dodaja funkcionalnosti za sodelovanje in gostovanje kode.

---
### Zakaj bi uporabljali Git?

<img src="./img/why-git.webp" alt="logo" title="Logo" width="600"/>

Note:

Git je napreden sistem za nadzor različic, ki omogoča razvijalcem učinkovito sledenje in upravljanje sprememb v kodi. 
V primerjavi z ročnim shranjevanjem različnih verzij v ločenih direktorijih, Git ponuja boljšo organizacijo, 
varčuje s prostorom z inteligentnim shranjevanjem sprememb, olajša združevanje sprememb iz različnih vej (branches) 
in omogoča enostavno povrnitev na prejšnje verzije

Medtem pa ce shranjujemo različne verzije v ločenih direktorijih, se lahko zgodi, da se izgubijo ali pa jih je težko najti.


---

<img src="./img/git-meme-ctlz.jpg" alt="logo" title="Logo" width="600"/>

---

<img src="./img/meme_1.jpg" alt="logo" title="Logo" width="400"/>

---
#### Kaj je Diff?

<style>
.container {
    display: flex;
    flex-wrap: wrap;
}
.col {
    flex: 50%; /* each column will take up half of the container width */
}
.full-width {
    width: 100%;
}
</style>

<div class="container">
   <div class="col">
   .
    <img src="./img/diff-a.png" alt="l1" title="l1" width="300"/>
   </div>

   <div class="col">
   .
    <img src="./img/diff-b.png" alt="l2" title="l2" width="300"/>
   </div>

   <div class="full-width">
    <img src="./img/diff-a-b.png" alt="l3" title="l3" width="300"/> 
   </div>
</div>

Note:
V kontekstu Git-a in razvoja programske opreme, "diff" je kratka oblika za "difference" (razlika). 
To orodje se uporablja za prikaz razlik med dvema datotekama ali nizoma datotek. 
Pogosto se uporablja za prikaz sprememb, ki so bile narejene v datoteki ali med različnimi verzijami datoteke v sistemu za nadzor različic, kot je Git.

Ko uporabljate Git, lahko z ukazom git diff vidite, 
kaj se je spremenilo v datotekah, ki še niso bile "committed" (to je, katerih spremembe še niso bile uradno zabeležene v Git zgodovini). 
Ta ukaz prikaže vrstice, ki so bile dodane, spremenjene ali odstranjene. 

1d0 - izbrisi vrstico 1 iz datoteke A
2a2 - dodaj vrstico 2 iz datoteke B na mesto 2 v datoteki A
4a5 - dodaj vrstico 4 iz datoteke B na mesto 5 v datoteki A
7d7 - izbrisi vrstico 7 iz datoteke A
8a9 - dodaj vrstico 8 iz datoteke B na mesto 9 v datoteki A

Basically recept kako priti iz datoteke A v datoteko B.

---
### Kako začeti z Gitom?

```bash
git init
```

```bash
λ ls -lah
drwxr-xr-x spagnologasper users 4.0 KB ... 2023 .
drwxr-xr-x spagnologasper users 4.0 KB ... 2023 ..
drwxr-xr-x spagnologasper users 4.0 KB ... 2023 .git
```

Note: Zacnemo z git init, tako ustvarimo nas lokalni repozitorij.

---
### Kaj se ustvari ob git init?

```
λ ls -lah .git
drwxr-xr-x spagnologasper users 4.0 KB ...  .
drwxr-xr-x spagnologasper users 4.0 KB ...  ..
drwxr-xr-x spagnologasper users 4.0 KB ...  branches
.rw-r--r-- spagnologasper users  92 B  ...  config
.rw-r--r-- spagnologasper users  73 B  ...  description
.rw-r--r-- spagnologasper users  23 B  ...  HEAD
drwxr-xr-x spagnologasper users 4.0 KB ...  hooks
drwxr-xr-x spagnologasper users 4.0 KB ...  info
drwxr-xr-x spagnologasper users 4.0 KB ...  objects
drwxr-xr-x spagnologasper users 4.0 KB ...  refs
```

---
### Config 

 To je datoteka konfiguracije za vaš Git repozitorij. 
 V njej so shranjene lokalne nastavitve za vaš repozitorij, 
 kot so informacije o uporabniku (ime in e-pošta), oddaljeni repozitoriji (remote repositories), 
 veje (branches), in druge nastavitve, specifične za vaš projekt.
 V to datoteko tudi pisejo git ukazi, ki jih izvajamo.

 ```
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
 ```


---
### Description

Vsebuje opis samega repozitorija.

```
λ cat description
Unnamed repository; 
edit this file 'description' to name the repository.
```

---
### HEAD
Datoteka HEAD vsebuje referenco na trenutno izbrano vejo. Pogosto kaže na datoteko znotraj refs/heads map

```
λ cat HEAD
ref: refs/heads/master
```

---
### OBJECTS
Direktorij objects je ključna komponenta Gitovega shranjevanja. 
Vsebuje vse podatkovne objekte (commits, drevesa, binarne datoteke), 
ki predstavljajo vsebino vašega repozitorija. Ti objekti so shranjeni v stisnjeni in binarni obliki

---
### REFS
V tem direktoriju so shranjene reference na veje (branches), oznake (tags) 
in oddaljene repozitorije (remotes). Vsaka od teh poddirektorijev vsebuje datoteke, 
ki kažejo na določene commite.

---
### LOGS
Direktorij logs vsebuje dnevniške datoteke, 
ki zapisujejo spremembe v različnih referencah, kot so veje. 
To omogoča sledenje zgodovini sprememb.

---
### HOOKS
Direktorij `hooks` vsebuje skripte, ki se lahko samodejno izvajajo ob določenih dogodkih v Git ciklu, 
kot je commit, push, in podobno. Privzeto so te skripte vzorci in niso aktivne.

---
### Kako dodamo oddaljeni repozitorij?

Recimo, da sedaj zelimo nas lokalni git povezati z nekim git streznikom, da bomo imeli backup nasega lokalnega repozitorija.

```bash
git remote add origin https://gitea.spanskiduh.dev/spanskiduh/test-repo.git
```

V datoteko `.git/config` se doda vrstica:
```
[remote "origin"]
        url = https://gitea.spanskiduh.dev/spanskiduh/test-repo.git
        fetch = +refs/heads/*:refs/remotes/origin/*
```

---
### Dodajanje nove datoteke

```bash
init on master
λ echo "#TO JE PRVA DATOTEKA" >> prva_datoteka.txt

init on master [?]
λ ls -lah
drwxr-xr-x spagnologasper users 4.0 KB ... .
drwxr-xr-x spagnologasper users 4.0 KB ... ..
drwxr-xr-x spagnologasper users 4.0 KB ... .git
.rw-r--r-- spagnologasper users  21 B  ... prva_datoteka.txt
```

---
### dodajanje nove datoteke

```
λ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        prva_datoteka.txt

nothing added to commit but untracked files present (use "git add" to track)
```

---
### dodajanje nove datoteke

```bash
git add prva_datoteka.txt
```

```bash
λ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   prva_datoteka.txt
```

---
### Uveljavljanje sprememb

<img src="./img/git-commit-message-meme.png" alt="logo" title="Logo" width="400"/>

```bash
git commit -m "Zelo deskriptivno sporocilo!"
```

---
### Sinhronizacija lokalnega repozitorija z oddaljenim

<img src="./img/master-main.jpg" alt="logo" title="Logo" width="400"/> 

```bash
git checkout -b main; git push -u origin main
```

---
### Sinhronizacija lokalnega repozitorija z oddaljenim

<img src="./img/pushed-to-git.png" alt="logo" title="Logo" width="600"/> 

---
#### Pregled zgodovine uveljavitev

<img src="./img/gitlog-meme.jpeg" alt="logo" title="Logo" width="160"/> 

---
#### Pregled zgodovine uveljavitev

```
git log
```
```bash
commit e44d7ef17a34fa9fa2d92ace8dd1296c06353d90 (HEAD -> main, origin/main, master)
Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
Date:   Tue Dec 12 22:02:03 2023 +0100

    Zelo deskriptivno sporocilo!
```
```
git log --oneline

```
```
e44d7ef (HEAD -> main, origin/main, master) Zelo deskriptivno sporocilo!
```


---
#### .Gitignore

Pomaga nam ignorirati datoteke, ki jih ne zelimo dodati v repozitorij.
Kot so npr. datoteke z gesli, datoteke z nastavitvami, datoteke z logi, baze itd.

```bash
λ echo "mojabaza.sqlite" >> .gitignore
λ ls
mojabaza.sqlite prva_datoteka.txt
```

```bash
λ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)
```

---
#### .Gitignore

<img src="./img/meme-gitignore-node-modules.png" alt="logo" title="Logo" width="600"/> 


---
### Branching

Zakaj?

<img src="./img/git-branches-merge.png" alt="logo" title="Logo" width="600"/>

---
### Reality

<img src="./img/branching-reallife.png" alt="logo" title="Logo" width="400"/>


---
### Ustvarjanje nove veje

```bash
λ git checkout -b feats1337
Switched to a new branch 'feats1337'
# -b pomeni, da ustvarimo novo vejo
```

Spremenino datoteko `prva_datoteka.txt`:

```bash
echo -n "\n 1337 feature" >> prva_datoteka.txt
```
Dodamo spremembe v repozitorij:

```bash
git add prva_datoteka.txt
```

---
### Ustvarjanje nove veje

Uveljavimo spremembe:

```bash
λ git commit -m "Dodaj vrstico v prvo datoteko"
```

```bash
λ git push -u origin feats1337

Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a new pull request for 'feats1337':
remote:   https://gitea.spanskiduh.dev/spanskiduh/test-repo/compare/main...feats1337
remote:
remote: . Processing 1 references
remote: Processed 1 references in total
To https://gitea.spanskiduh.dev/spanskiduh/test-repo.git
 * [new branch]      feats1337 -> feats1337
branch 'feats1337' set up to track 'origin/feats1337'.
```


---
### Pregled vej

Lokalno:
```bash
λ git branch 

* feats1337
  main
  master
```

Remote: 
```
λ git branch  -r 

  origin/feats1337
  origin/main
```

---
### Pregled vej

```bash
λ git log --graph --oneline --all

* commit 634d79a74c2f7347c0afb8fb8305b523ee16d05a (HEAD -> feats1337, origin/feats1337)
| Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
| Date:   Tue Dec 12 23:06:49 2023 +0100
|
|     Dodaj vrstico v prvo datoteko
|
* commit e44d7ef17a34fa9fa2d92ace8dd1296c06353d90 (origin/main, master, main)
  Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
  Date:   Tue Dec 12 22:02:03 2023 +0100

      Zelo deskriptivno sporocilo!
```


---
### Globje


```bash
* commit b62623b5451187faf463bf5f0e0a93ea0c1fbf45 (HEAD -> feats1337, origin/feats1337)
| Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
| Date:   Tue Dec 12 23:11:14 2023 +0100
|
|     Se ena vrstica
|
* commit e60b7db578566b1f4110e04d95580118a6a3160d
| Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
| Date:   Tue Dec 12 23:10:56 2023 +0100
|
|     Dodaj novo vrstico v datoteko
|
* commit 8a79fbcaefdd8f445f6ff1d4a5e693963f4772dc
| Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
| Date:   Tue Dec 12 23:10:23 2023 +0100
|
|     Uredi prvo datoteko se nekoliko
|
* commit 634d79a74c2f7347c0afb8fb8305b523ee16d05a
| Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
| Date:   Tue Dec 12 23:06:49 2023 +0100
|
|     Dodaj vrstico v prvo datoteko
|
* commit e44d7ef17a34fa9fa2d92ace8dd1296c06353d90 (origin/main, master, main)
  Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
  Date:   Tue Dec 12 22:02:03 2023 +0100

      Zelo deskriptivno sporocilo!
```


---
### Treunutno stanje

```
main: e44d7 --
            |
feats1337:  634d79 --  8a79f -- e60b7 -- b62623
```

---
### Združevanje vej

<img src="./img/merge-rebase.png" alt="logo" title="Logo" width="600"/> 

---
### Združevanje vej

Merge:
```
main: e44d7 -- M
                  |
feats1337:       634d79 --  8a79f -- e60b7 -- b62623
```

Rebase:
```
e44d7 -- [634d79 --  8a79f' -- e60b7' -- b62623']
```

---
### Rebase

```
git checkout feats1337
git rebase main
git checkout main
git merge feats1337
```

---
### Rebase

```bash
* commit b62623b5451187faf463bf5f0e0a93ea0c1fbf45 (HEAD -> main, origin/feats1337, feats1337)
| Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
| Date:   Tue Dec 12 23:11:14 2023 +0100
|
|     Se ena vrstica
|
* commit e60b7db578566b1f4110e04d95580118a6a3160d
| Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
| Date:   Tue Dec 12 23:10:56 2023 +0100
|
|     Dodaj novo vrstico v datoteko
|
* commit 8a79fbcaefdd8f445f6ff1d4a5e693963f4772dc
| Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
| Date:   Tue Dec 12 23:10:23 2023 +0100
|
|     Uredi prvo datoteko se nekoliko
|
* commit 634d79a74c2f7347c0afb8fb8305b523ee16d05a
| Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
| Date:   Tue Dec 12 23:06:49 2023 +0100
|
|     Dodaj vrstico v prvo datoteko
|
* commit e44d7ef17a34fa9fa2d92ace8dd1296c06353d90 (origin/main, master)
  Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
  Date:   Tue Dec 12 22:02:03 2023 +0100

      Zelo deskriptivno sporocilo!
```

---
### Merge

```
git checkout -b feats222
# Create some commits on feats222
git checkout main
git merge feats222
```

---
### Merge conflicts

<img src="./img/merge-conflict.png" alt="logo" title="Logo" width="600"/>

---
### Merge conflicts

<img src="./img/mc.webp" alt="logo" title="Logo" width="500"/>


---
### Primer merge conflicta

Najprej ustvarimo `example.txt` datoteko z neko vsebino:

```bash 
git checkout main
echo "Initial content" > example.txt
git add example.txt
git commit -m "Add example.txt with initial content"
```

---
### Primer merge conflicta

Ustvarimo novo vejo uin dodamo novo vrstico v datoteko:

```bash
git checkout -b feature-branch
echo "Content added in feature-branch" > example.txt
git add example.txt
git commit -m "Modify example.txt in feature-branch"
```

---
### Primer merge conflicta 

Se vrnemo nazaj na `main` in dodamo novo vrstico v datoteko:

```bash
git checkout main
echo "Conflicting content in main branch" > example.txt
git add example.txt
git commit -m "Modify example.txt in main with conflicting content"
```

---
### Primer merge conflicta 

Združimo obe veji:

```bash
git merge feature-branch
```
O ne!

```
λ git merge feature-branch
Auto-merging example.txt
CONFLICT (content): Merge conflict in example.txt
Automatic merge failed; fix conflicts and then commit the result.
```

---
### Primer merge conflicta

V tem primeru uredimo datoteko tako da obdrzimo
uveljavitev, ki jo zelimo obdrzati.

```bash
λ cat example.txt
<<<<<<< HEAD
Conflicting content in main branch
=======
Content added in feature-branch
>>>>>>> feature-branch
```

---
### Primer merge conflicta

Po popravku datoteke jo dodamo v repozitorij:

```
git add example.txt
```

Ter uveljavimo spremembe:

```
git commit -m "Fix merge conflict"
```

---
### Git Reset 

Recimo da se zelimo vrniti na stanje pred zdruzevanjem vej.
Uporabimo naso prelepo komando `git log` ter lociramo commit,
na katerega se zelimo vrniti.

```bash
commit a1af9a2ce1e46f336e2a904149ded1078eedd43e
Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
Date:   Wed Dec 13 00:09:41 2023 +0100

    Modify example.txt in main with conflicting content

commit 2f12b6c100b20a7e1fc0ce64a902a3109e6edaee (feature-branch)
Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
Date:   Wed Dec 13 00:09:24 2023 +0100

    Modify example.txt in feature-branch

commit 9fdd5980c45b35dcbe7d0b84d9a82fa3e3babeb6
Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
Date:   Wed Dec 13 00:08:53 2023 +0100

    Add example.txt with initial content

```

---
### Git Reset 

Po izboru se lahko vrnemo nazaj na stanje pred zdruzevanjem vej.

```bash
git reset --hard 9fdd5980c45b35dcbe7d0b84d9a82fa3e3babeb6
```

```
commit 9fdd5980c45b35dcbe7d0b84d9a82fa3e3babeb6 (HEAD -> main)
Author: Gašper Spagnolo <gasper.spagnolo@outlook.com>
Date:   Wed Dec 13 00:08:53 2023 +0100

    Add example.txt with initial content
```

In sedaj HEAD kaze na commit, ki smo ga izbrali.

---
### Git blame 

<img src="./img/git-blame-meme.jpg" alt="logo" title="Logo" width="1000"/>


---
### Hvala za pozornost <!-- .element: style="text-align: left; font-size: 50px;" -->
<style>
.container{
    display: flex;
}
.col{
    flex: 1;
}
</style>

<div class="container">
<div class="col">

<div style="display: flex; align-items: center;"><img src="./img/github-light.png" alt="logo" title="Logo" width="50" style="margin-right: 10px;" /><b>DragonSec SI</b> </div>
<div style="display: flex; align-items: center;"><img src="./img/twitter-light.png" alt="logo" title="Logo" width="50" style="margin-right: 10px;" /><b>@DragonSec_SI</b> </div>
<div style="display: flex; align-items: center;"><img src="./img/mail-light.png" alt="logo" title="Logo" width="50" style="margin-right: 10px;" /><b>info@dragonsec.si</b> </div>


</div>
<!-- .element: style="width: 100%;" -->

<div class="col">

<img src="./img/about-us.jpg" alt="logo" title="Logo" width="400"/> 

</div>
</div>
