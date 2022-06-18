ivn@ivn-u22:~/Projects/cursor-py/HW2$ mkdir cursor_git_hw

ivn@ivn-u22:~/Projects/cursor-py/HW2$ cd cursor_git_hw

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ touch first.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git add first.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git commit -m 'adding first.txt'

[main (root-commit) fd6380f] adding first.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 cursor_git_hw/first.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git log

commit fd6380f76a0d00121cfeeb95e42065563585cf7a (HEAD -> main)
Author: Ivan Diulinclear <ivan.diulin.ua@gmail.com>
Date:   Sat Jun 18 17:33:58 2022 +0300
    adding first.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ touch second.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git add second.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git commit -m 'adding second.txt'

[main 5f1b25d] adding second.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 cursor_git_hw/second.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ rm first.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git add first.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git commit -m 'removing first.txt'

[main 2ac5816] removing first.txt

 1 file changed, 0 insertions(+), 0 deletions(-)

 delete mode 100644 cursor_git_hw/first.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git log

commit 2ac58164361898048fe67d1e6d8489dcb691caed (HEAD -> main)

Author: Ivan Diulinclear <ivan.diulin.ua@gmail.com>

Date:   Sat Jun 18 17:36:57 2022 +0300



    removing first.txt



commit 5f1b25d06df40b6d8b57bb629be26faf5517f53f

Author: Ivan Diulinclear <ivan.diulin.ua@gmail.com>

Date:   Sat Jun 18 17:35:53 2022 +0300



    adding second.txt



commit fd6380f76a0d00121cfeeb95e42065563585cf7a

Author: Ivan Diulinclear <ivan.diulin.ua@gmail.com>

Date:   Sat Jun 18 17:33:58 2022 +0300



    adding first.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git push

Enumerating objects: 10, done.

Counting objects: 100% (10/10), done.

Delta compression using up to 2 threads

Compressing objects: 100% (4/4), done.

Writing objects: 100% (10/10), 811 bytes | 405.00 KiB/s, done.

Total 10 (delta 0), reused 0 (delta 0), pack-reused 0

To github.com:Ivan-Diulin/HW2.git

 * [new branch]      main -> main

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git branch first

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git branch second

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ echo "Hello" > second.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git branch

  first

* main

  second

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git branch -d second

Deleted branch second (was 2ac5816).

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git checkout -d second

fatal: git checkout: --detach does not take a path argument 'second'

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git checkout -b second

Switched to a new branch 'second'

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git branch

  first

  main

* second

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ echo "Hello" > second.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git stash

Saved working directory and index state WIP on second: 2ac5816 removing first.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git checkout first

Switched to branch 'first'

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git checkout second

Switched to branch 'second'

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git stash pop

On branch second

Changes not staged for commit:

  (use "git add <file>..." to update what will be committed)

  (use "git restore <file>..." to discard changes in working directory)

	modified:   second.txt



no changes added to commit (use "git add" and/or "git commit -a")

Dropped refs/stash@{0} (e4ca404d04d1f2a0627769070c00ff3c52586849)

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git add second.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git commit -m 'Changing  second.txt'

[second f8064e2] Changing  second.txt

 1 file changed, 1 insertion(+)

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git push

fatal: The current branch second has no upstream branch.

To push the current branch and set the remote as upstream, use



    git push --set-upstream origin second



ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git push --set-upstream origin second

Enumerating objects: 7, done.

Counting objects: 100% (7/7), done.

Writing objects: 100% (4/4), 313 bytes | 104.00 KiB/s, done.

Total 4 (delta 0), reused 0 (delta 0), pack-reused 0

remote: 

remote: Create a pull request for 'second' on GitHub by visiting:

remote:      https://github.com/Ivan-Diulin/HW2/pull/new/second

remote: 

To github.com:Ivan-Diulin/HW2.git

 * [new branch]      second -> second

branch 'second' set up to track 'origin/second'.

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git checkout first

Switched to branch 'first'

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ echo "Cursor" > second.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git add second.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git commit -m 'Changins second.txt'

[first 35770fb] Changins second.txt

 1 file changed, 1 insertion(+)

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git push --set-upstream origin first

Enumerating objects: 7, done.

Counting objects: 100% (7/7), done.

Writing objects: 100% (4/4), 312 bytes | 312.00 KiB/s, done.

Total 4 (delta 0), reused 0 (delta 0), pack-reused 0

remote: 

remote: Create a pull request for 'first' on GitHub by visiting:

remote:      https://github.com/Ivan-Diulin/HW2/pull/new/first

remote: 

To github.com:Ivan-Diulin/HW2.git

 * [new branch]      first -> first

branch 'first' set up to track 'origin/first'.

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ checkout main

checkout: command not found

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git checkout main

Switched to branch 'main'

Your branch is up to date with 'origin/main'.

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git merge second

Updating 2ac5816..f8064e2

Fast-forward

 cursor_git_hw/second.txt | 1 +

 1 file changed, 1 insertion(+)

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git merge first

Auto-merging cursor_git_hw/second.txt

CONFLICT (content): Merge conflict in cursor_git_hw/second.txt

Automatic merge failed; fix conflicts and then commit the result.

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git push

Total 0 (delta 0), reused 0 (delta 0), pack-reused 0

To github.com:Ivan-Diulin/HW2.git

   2ac5816..f8064e2  main -> main

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git add second.txt

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git commit -m 'Resolved conflict in file second.txt between second and first branches'

[main f45b38c] Resolved conflict in file second.txt between second and first branches

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ git push

Enumerating objects: 10, done.

Counting objects: 100% (10/10), done.

Writing objects: 100% (4/4), 379 bytes | 379.00 KiB/s, done.

Total 4 (delta 0), reused 0 (delta 0), pack-reused 0

To github.com:Ivan-Diulin/HW2.git

   f8064e2..f45b38c  main -> main

ivn@ivn-u22:~/Projects/cursor-py/HW2/cursor_git_hw$ 



