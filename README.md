# Git
## Exercise Code
```
Katelyns-MacBook-Pro:~ katelynmichalove$ git config --global user.name "Katelyn Michalove"
Katelyns-MacBook-Pro:~ katelynmichalove$ git config --global user.email katelynmichalove@gmail.com
Katelyns-MacBook-Pro:~ katelynmichalove$ git config --global color.ui true
Katelyns-MacBook-Pro:~ katelynmichalove$ git config --global push.default simple
Katelyns-MacBook-Pro:~ katelynmichalove$ cat ~/.gitconfig
[user]
	name = Katelyn Michalove
	email = katelynmichalove@gmail.com
[color]
	ui = true
[push]
	default = simple
Katelyns-MacBook-Pro:~ katelynmichalove$ cd ~
Katelyns-MacBook-Pro:~ katelynmichalove$ mkdir -p bloc/shopping_cart
Katelyns-MacBook-Pro:~ katelynmichalove$ cd bloc/shopping_cart
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ pwd
/Users/katelynmichalove/bloc/shopping_cart
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ touch apple.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ ls
apple.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git init .
Initialized empty Git repository in /Users/katelynmichalove/bloc/shopping_cart/.git/
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ ls -al
total 0
drwxr-xr-x  4 katelynmichalove  staff  136 Aug 27 10:46 .
drwxr-xr-x  3 katelynmichalove  staff  102 Aug 27 10:44 ..
drwxr-xr-x  9 katelynmichalove  staff  306 Aug 27 10:46 .git
-rw-r--r--  1 katelynmichalove  staff    0 Aug 27 10:45 apple.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	apple.txt

nothing added to commit but untracked files present (use "git add" to track)
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git add apple.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   apple.txt

Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ touch banana.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ ls
apple.txt	banana.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   apple.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	banana.txt

Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git commit -m "Create the apple.txt file"
[master (root-commit) e6339c6] Create the apple.txt file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 apple.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git add banana.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git commit -m "Add banana.txt"
[master 3615e68] Add banana.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 banana.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git log
commit 3615e689813d4244eee73269a4fad60d72c89079 (HEAD -> master)
Author: Katelyn Michalove <katelynmichalove@gmail.com>
Date:   Mon Aug 27 10:51:30 2018 -0700

    Add banana.txt

commit e6339c6f3368d12f338d1f888b4561e489883162
Author: Katelyn Michalove <katelynmichalove@gmail.com>
Date:   Mon Aug 27 10:49:59 2018 -0700

    Create the apple.txt file
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git show --pretty="format:" --name-only HEAD
banana.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ touch tomatoes.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	tomatoes.txt

nothing added to commit but untracked files present (use "git add" to track)
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ touch .gitignore
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ echo "tomatoes.txt" >> .gitignore
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	.gitignore

nothing added to commit but untracked files present (use "git add" to track)
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git add .gitignore
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   .gitignore

Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git commit -m "add .gitignore"
[master 625bde8] add .gitignore
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git checkout -b new_grocery_list
Switched to a new branch 'new_grocery_list'
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git branch
  master
* new_grocery_list
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ ls
apple.txt	banana.txt	tomatoes.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ touch orange.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git status
On branch new_grocery_list
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	orange.txt

nothing added to commit but untracked files present (use "git add" to track)
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git add orange.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git status
On branch new_grocery_list
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   orange.txt

Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git commit -m "Add orange.txt on new_grocery_list"
[new_grocery_list 9d587f5] Add orange.txt on new_grocery_list
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 orange.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ ls
apple.txt	banana.txt	orange.txt	tomatoes.txt
```
## Assignment
```
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git checkout master
Switched to branch 'master'
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git checkout -b shopping_cart_assignment
Switched to a new branch 'shopping_cart_assignment'
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ ls
apple.txt	banana.txt	tomatoes.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git rm apple.txt
rm 'apple.txt'
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ ls
banana.txt	tomatoes.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ open banana.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ touch lettuce.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ ls
banana.txt	lettuce.txt	tomatoes.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git add lettuce.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git status
On branch shopping_cart_assignment
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	renamed:    apple.txt -> lettuce.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   banana.txt

Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git commit -m "Add lettuce.txt on shopping_cart_assignment"
[shopping_cart_assignment 8133bab] Add lettuce.txt on shopping_cart_assignment
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename apple.txt => lettuce.txt (100%)
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git diff > lettuce.txt
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ cd shopping_cart_assignment
-bash: cd: shopping_cart_assignment: No such file or directory
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git status
On branch shopping_cart_assignment
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   banana.txt
	modified:   lettuce.txt

no changes added to commit (use "git add" and/or "git commit -a")
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git branch
  master
  new_grocery_list
* shopping_cart_assignment
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ git commit -a
[shopping_cart_assignment ca603e6] Assignment Changes
 2 files changed, 8 insertions(+)
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ cat lettuce.txt
diff --git a/banana.txt b/banana.txt
index e69de29..de49619 100644
--- a/banana.txt
+++ b/banana.txt
@@ -0,0 +1 @@
+Git Checkpoint Assignment
\ No newline at end of file
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ history
    1  git config --global user.name "Katelyn Michalove"
    2  git config --global user.email katelynmichalove@gmail.com
    3  git config --global color.ui true
    4  git config --global push.default simple
    5  cat ~/.gitconfig
    6  cd ~
    7  mkdir -p bloc/shopping_cart
    8  cd bloc/shopping_cart
    9  pwd
   10  touch apple.txt
   11  ls
   12  git init .
   13  ls -al
   14  git status
   15  git add apple.txt
   16  git status
   17  touch banana.txt
   18  ls
   19  git status
   20  git commit -m "Create the apple.txt file"
   21  git add banana.txt
   22  git commit -m "Add banana.txt"
   23  git log
   24  git show --pretty="format:" --name-only HEAD
   25  touch tomatoes.txt
   26  git status
   27  touch .gitignore
   28  echo "tomatoes.txt" >> .gitignore
   29  git status
   30  git add .gitignore
   31  git status
   32  git commit -m "add .gitignore"
   33  git checkout -b new_grocery_list
   34  git branch
   35  ls
   36  touch orange.txt
   37  git status
   38  git add orange.txt
   39  git status
   40  git commit -m "Add orange.txt on new_grocery_list"
   41  ls
   42  git checkout master
   43  git checkout -b shopping_cart_assignment
   44  ls
   45  git rm apple.txt
   46  ls
   47  open banana.txt
   48  touch lettuce.txt
   49  ls
   50  git add lettuce.txt
   51  git status
   52  git commit -m "Add lettuce.txt on shopping_cart_assignment"
   53  git diff > lettuce.txt
   54  cd shopping_cart_assignment
   55  git status
   56  git branch
   57  git commit -a
   58  cat lettuce.txt
   59  history
Katelyns-MacBook-Pro:shopping_cart katelynmichalove$ 
```
