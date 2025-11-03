# Esercizio di risoluzione di un merge conflict

**Il tempo massimo in laboratorio per questo esercizio è di _20 minuti_.
Se superato, sospendere l'esercizio e riprenderlo per ultimo!**

Si visiti https://github.com/APICe-at-DISI/OOP-git-merge-conflict-test.
Questo repository contiene due branch: `master` e `feature`

Per ognuna delle seguenti istruzioni, si annoti l'output ottenuto.
Prima di eseguire ogni operazione sul worktree o sul repository,
si verifichi lo stato del repository con `git status`.

1. Si cloni localmente il repository

Cloning into '61-git-remotes-merge-conflict/dir'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 12 (delta 1), reused 1 (delta 1), pack-reused 8 (from 1)
Receiving objects: 100% (12/12), done.
Resolving deltas: 100% (2/2), done.


2. Ci si assicuri di avere localmente entrambi i branch remoti

git log --all --graph
* commit bed943fbdd6ba94e64197448e4754a529d984e88 (origin/feature)
| Author: Danilo Pianini <danilo.pianini@gmail.com>
| Date:   Thu Oct 27 17:21:22 2016 +0200
|
|     Print author information
|
| * commit 8e0f29c12e060f3bdc62540343eff3e473616d61 (HEAD -> master, origin/master, origin/HEAD)
|/  Author: Danilo Pianini <danilo.pianini@gmail.com>
|   Date:   Thu Oct 27 17:19:05 2016 +0200
|
|       Change HelloWorld to print the number of available processors
|
* commit d956df66aeb0829f23b7b3d0d9a1c002c390f87f
| Author: Danilo Pianini <danilo.pianini@gmail.com>
| Date:   Thu Oct 27 17:17:43 2016 +0200
|
|     Create .gitignore
|
* commit 700ee0b669f6cd75384abb9af51ca5c2adefe917
  Author: Danilo Pianini <danilo.pianini@gmail.com>
  Date:   Thu Oct 27 17:15:10 2016 +0200

      Create HelloWorld


3. Si faccia il merge di `feature` dentro `master`, ossia: si posizioni la `HEAD` su `master`
   e da qui si esegua il merge di `feature`
4. Si noti che viene generato un **merge conflict**!
5. Si risolva il merge conflict come segue:
   - Il programma Java risultante deve stampare sia il numero di processori disponibili
     (funzionalità presente su `master`)
     che il nome dell'autore del file
     (funzionalità presente su `feature`)
6. Si crei un nuovo repository nel proprio github personale
7. Si aggiunga il nuovo repository creato come **remote** e si elenchino i remote

origin  https://github.com/APICe-at-DISI/OOP-git-merge-conflict-test.git (fetch)
origin  https://github.com/APICe-at-DISI/OOP-git-merge-conflict-test.git (push)
remote  https://github.com/MansourChabraoui/lab06-61.git (fetch)
remote  https://github.com/MansourChabraoui/lab06-61.git (push)


8. Si faccia push del branch `master` sul proprio repository

git push remote master
Enumerating objects: 15, done.
Counting objects: 100% (15/15), done.
Delta compression using up to 12 threads
Compressing objects: 100% (11/11), done.
Writing objects: 100% (15/15), 1.57 KiB | 537.00 KiB/s, done.
Total 15 (delta 4), reused 10 (delta 2), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), done.
To https://github.com/MansourChabraoui/lab06-61.git
 * [new branch]      master -> master


9. Si setti il branch remoto `master` del nuovo repository come *upstream* per il proprio branch `master` locale

git push -u remote remote/master
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/MansourChabraoui/lab06-61.git
 * [new reference]   remote/master -> remote/master