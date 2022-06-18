# HW2
#====

# Preparations

~$ mkdir cursor
~$ cd cursor
~/cursor$ git clone git@github.com:Ivan-Diulin/Python-basic---Deadshot-.git

Cloning into 'Python-basic---Deadshot-'...
remote: Enumerating objects: 65, done.
remote: Counting objects: 100% (65/65), done.
remote: Compressing objects: 100% (36/36), done.
remote: Total 65 (delta 5), reused 56 (delta 1), pack-reused 0
Receiving objects: 100% (65/65), 7.28 KiB | 1.21 MiB/s, done.
Resolving deltas: 100% (5/5), done.

~/cursor$ cd Python-basic---Deadshot-
~/cursor/Python-basic---Deadshot-$ cd homeworks
~/cursor/Python-basic---Deadshot-/homeworks$ cd git
~/cursor/Python-basic---Deadshot-/homeworks/git$ 

# Actual homework

#1
$ mkdir cursor_git_hw

#2
$ cd cursor_git_hw

#3
$ touch first.txt

#4
$ git add first.txt

#5
$ git commit -m 'Adding first.txt'

[master b7460b8] Adding first.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 homeworks/git/first.txt
 
#6
$ git log

commit b7460b85147ea8e9cf0fabc449d7e3925f25ecc9 (HEAD -> master)
Author: Ivan Diulinclear <ivan.diulin.ua@gmail.com>
Date:   Sat Jun 18 19:08:33 2022 +0300

    Adding first.txt

commit 6333816e1518db8123351e69047e95d2047dd207 (origin/master, origin/HEAD)
Author: Rostyslav Kitsylinskyy <rostyslav.kitsylinskyy@gmail.com>
Date:   Thu Jun 16 20:59:53 2022 +0300

    git homework

#7
$ touch second.txt

#8
$ git add second.txt

#9
$ git commit -m 'Adding second.txt'

[master 648b712] Adding second.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 homeworks/git/second.txt
 
#10
$ rm first.txt

#11
$ git add first.txt

#12
$ git commit -m 'Removing first.txt'

[master 56beb7d] Removing first.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 delete mode 100644 homeworks/git/first.txt
 
#13
$ git log

commit 56beb7da4cccf4e4e03d3df91b7be2b68087c7fe (HEAD -> master)
Author: Ivan Diulinclear <ivan.diulin.ua@gmail.com>
Date:   Sat Jun 18 19:17:30 2022 +0300

    Removing first.txt

commit 648b7120d4a1ccb3233a53d071bd1ce8216be503
Author: Ivan Diulinclear <ivan.diulin.ua@gmail.com>
Date:   Sat Jun 18 19:16:41 2022 +0300

    Adding second.txt

#14
$ git push

Enumerating objects: 19, done.
Counting objects: 100% (19/19), done.
Delta compression using up to 2 threads
Compressing objects: 100% (10/10), done.
Writing objects: 100% (16/16), 1.28 KiB | 436.00 KiB/s, done.
Total 16 (delta 0), reused 1 (delta 0), pack-reused 0
To github.com:Ivan-Diulin/Python-basic---Deadshot-.git
   6333816..56beb7d  master -> master

#15
$ git branch first

#16
$ git checkout -b second

Switched to a new branch 'second'

#17
$ echo 'Hello' > second.txt

#18
$ git stash

Saved working directory and index state WIP on second: 56beb7d Removing first.txt

$ git checkout first

Switched to branch 'first'

#19
$ git checkout second

Switched to branch 'second'

$ git stash pop
On branch second
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   second.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        ../.idea/

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (c81412abb4932b66736ca8d0ccb3b93cf3369c12)

#20
$ git add second.txt

#21
$ git commit -m 'Changing second.txt'

[second 8879f4e] Changing second.txt
 1 file changed, 1 insertion(+)

#22
$ git push --set-upstream origin second

Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (6/6), 466 bytes | 466.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'second' on GitHub by visiting:
remote:      https://github.com/Ivan-Diulin/Python-basic---Deadshot-/pull/new/second
remote: 
To github.com:Ivan-Diulin/Python-basic---Deadshot-.git
 * [new branch]      second -> second
branch 'second' set up to track 'origin/second'.

#23
$ git checkout first

Switched to branch 'first'

#24
$ echo 'Cursor' > second.txt

#25
$ git add second.txt

#26
$ git commit -m 'Changing second.txt'

[first 3eee7e3] Changing second.txt
 1 file changed, 1 insertion(+)

#27
$ git push --set-upstream origin first

Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (6/6), 470 bytes | 470.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'first' on GitHub by visiting:
remote:      https://github.com/Ivan-Diulin/Python-basic---Deadshot-/pull/new/first
remote: 
To github.com:Ivan-Diulin/Python-basic---Deadshot-.git
 * [new branch]      first -> first
branch 'first' set up to track 'origin/first'.

#28
$ git checkout master

Switched to branch 'master'
Your branch is up to date with 'origin/master'.

#29
$ git merge second

Updating 56beb7d..8879f4e
Fast-forward
 homeworks/git/second.txt | 1 +
 1 file changed, 1 insertion(+)

#30
$ git merge first

Auto-merging homeworks/git/second.txt
CONFLICT (content): Merge conflict in homeworks/git/second.txt
Automatic merge failed; fix conflicts and then commit the result.

#31 - Edited text in conflicting file second.txt in PyCharm to look like:
#Hello
#Cursor
#
#then run next commands:

$ git add second.txt

$ git commit -m 'Resolving conflict in second.txt from merging first and master branches'

[master 11f8c83] Resolving conflict in second.txt from merging first and master branches

$ git push

Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (6/6), 537 bytes | 537.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:Ivan-Diulin/Python-basic---Deadshot-.git
   56beb7d..11f8c83  master -> master

#================
# End Of Homework
