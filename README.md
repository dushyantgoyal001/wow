# wow
Spider Induction task-1



<!--EXPLANATION OF WHAT I DID-->


pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider
$ git status                                                                                                /*checking status*/
fatal: not a git repository (or any of the parent directories): .git

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider
$ git init                                                                                                  /*initializing git*/
Initialized empty Git repository in C:/Users/pc/Desktop/spider/.git/

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git config --global user.name "dushyant-goyal"                                                           /*introducing user to git*/

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git config --global user.email "dushyantgoyal2406@gmail.com"

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ touch initialcommit.txt                                                                             /*adding file*/

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git add .

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git commit -m "initial commit"                                                                     /*initial commit*/
[master (root-commit) efa085d] initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 initialcommit.txt

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git checkout -b develop                                                                                 /*new branch develop*/
Switched to a new branch 'develop'

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (develop)
$ touch commit2.txt                                                                                          /*adding new file*/

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (develop)
$ git add .

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (develop)
$ git commit -m "added file commit2.txt on develop"
[develop d29fa89] added file commit2.txt on develop
 1 file changed, 1 insertion(+)                                                                                    /*commit_2 on develop branch*/
 create mode 100644 commit2.txt

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (develop)
$ git checkout master
Switched to branch 'master'

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ touch commit3.txt                                                                                                /*commit_3 on master branch*/

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git add .

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git commit -m "added file on master branch"
[master 7df4a90] added file on master branch
 1 file changed, 1 insertion(+)
 create mode 100644 commit3.txt

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git checkout develop
Switched to branch 'develop'

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (develop)
$ touch commit4.txt                                                                                                   

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (develop)
$ git add .

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (develop)
$ git commit -m "added file on develop"
[develop 432976e] added file on develop
 1 file changed, 1 insertion(+)
 create mode 100644 commit4.txt                                                                                        /*commit-4 on develop branch*/

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (develop)
$ git checkout master
Switched to branch 'master'

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git merge develop
Merge made by the 'recursive' strategy.                                                                               /*MERGING develop to master*/
 commit2.txt | 1 +
 commit4.txt | 1 +
 2 files changed, 2 insertions(+)
 create mode 100644 commit2.txt
 create mode 100644 commit4.txt

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git checkout -b spider
Switched to a new branch 'spider'                                                                                 /*new branch spider*/

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (spider)
$ touch spider.txt

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (spider)
$ git status
On branch spider
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        spider.txt

nothing added to commit but untracked files present (use "git add" to track)

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (spider)
$ git add .

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (spider)
$ git commit -m "added file spider.txt"
[spider 6847611] added file spider.txt
 1 file changed, 1 insertion(+)                                                                                   /*first commit on spider*/
 create mode 100644 spider.txt

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (spider)
$ touch dushyant.txt

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (spider)
$ git add .

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (spider)
$ git commit -m "final file added"
[spider 69b0d2d] final file added                                                                               /*final commit on spider*/
 1 file changed, 1 insertion(+)
 create mode 100644 dushyant.txt

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (spider)
$ git status
On branch spider
nothing to commit, working tree clean

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (spider)
$ git branch
  develop
  master                                                                                                         /*showing all branches available*/
* spider

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (spider)
$ git checkout master
Switched to branch 'master'

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git merge spider
Updating 2198468..69b0d2d
Fast-forward
 dushyant.txt | 1 +                                                                                          /*MERGING SPIDER*/
 spider.txt   | 1 +
 2 files changed, 2 insertions(+)
 create mode 100644 dushyant.txt
 create mode 100644 spider.txt

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git status
On branch master
nothing to commit, working tree clean

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git branch -d spider                                                                                         /*deleting spider branch--no error*/
Deleted branch spider (was 69b0d2d).

pc@DUSHYANT-ROYAL MINGW64 ~/Desktop/spider (master)
$ git branch -d develop                                                                                            /*deleting develop branch--no error*/
Deleted branch develop (was 432976e).

