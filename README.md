# Gym-Git-Exercise-Solutions

## Bundle 1

### Exercise 1

```bash
PS C:\Users\USER\OneDrive\Documents\Gym-Git-Exercise-Solutions> cd ..
PS C:\Users\USER\OneDrive\Documents> mkdir project


    Directory: C:\Users\USER\OneDrive\Documents


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         8/19/2025   6:39 PM                project


PS C:\Users\USER\OneDrive\Documents> cd project
PS C:\Users\USER\OneDrive\Documents\project> git init
Initialized empty Git repository in C:/Users/USER/OneDrive/Documents/project/.git/
PS C:\Users\USER\OneDrive\Documents\project> git add .
PS C:\Users\USER\OneDrive\Documents\project> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html
PS C:\Users\USER\OneDrive\Documents\project> git branch -m master main
PS C:\Users\USER\OneDrive\Documents\project> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html

PS C:\Users\USER\OneDrive\Documents\project> git commit -a -m "New Changes"
[main (root-commit) 412c846] New Changes
 1 file changed, 20 insertions(+)
 create mode 100644 index.html
PS C:\Users\USER\OneDrive\Documents\project> git remote add origin https://github.com/DIVINEakisa/Bundle1--Exercises1.git
PS C:\Users\USER\OneDrive\Documents\project> git remote -v
origin  https://github.com/DIVINEakisa/Bundle1--Exercises1.git (fetch)
origin  https://github.com/DIVINEakisa/Bundle1--Exercises1.git (push)
PS C:\Users\USER\OneDrive\Documents\project> git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 521 bytes | 521.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)

To https://github.com/DIVINEakisa/Bundle1--Exercises1.git
 * [new branch]      main -> main
PS C:\Users\USER\OneDrive\Documents\project> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\USER\OneDrive\Documents\project> git commit -a -m "Adding Style"
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        check.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\USER\OneDrive\Documents\project> git add .
PS C:\Users\USER\OneDrive\Documents\project> git commit -m "Add new File"
[dev 2f3a46c] Add new File
 1 file changed, 9 insertions(+)
 create mode 100644 check.html
PS C:\Users\USER\OneDrive\Documents\project> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\USER\OneDrive\Documents\project> git checkout dev
Switched to branch 'dev'
PS C:\Users\USER\OneDrive\Documents\project> git branch -d test
Deleted branch test (was 2f3a46c).

```

#### Exercises 2

```bash
PS C:\Users\USER\OneDrive\Documents\Gym-Git-Exercise-Solutions> cd ..
PS C:\Users\USER\OneDrive\Documents> cd myProject
PS C:\Users\USER\OneDrive\Documents\myProject> git add .
PS C:\Users\USER\OneDrive\Documents\myProject> git stash
Saved working directory and index state WIP on master: a62e5c1 Adding style
PS C:\Users\USER\OneDrive\Documents\myProject> git stash list
stash@{0}: WIP on master: a62e5c1 Adding style

PS C:\Users\USER\OneDrive\Documents\myProject> git add .
PS C:\Users\USER\OneDrive\Documents\myProject> git stash push -m "About File"
Saved working directory and index state On master: About File
PS C:\Users\USER\OneDrive\Documents\myProject> git stash list
stash@{0}: On master: About File
stash@{1}: WIP on master: a62e5c1 Adding style
PS C:\Users\USER\OneDrive\Documents\myProject> git add .
PS C:\Users\USER\OneDrive\Documents\myProject> git stash push -m "Add New File"
Saved working directory and index state On master: Add New File
PS C:\Users\USER\OneDrive\Documents\myProject> git stash list
stash@{0}: On master: Add New File
stash@{1}: On master: About File
stash@{2}: WIP on master: a62e5c1 Adding style

PS C:\Users\USER\OneDrive\Documents\myProject> git stash pop --index "stash@{1}"
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

Dropped stash@{1} (63a78fcc046f8324841d5aff5eb909a22aae68d3)
PS C:\Users\USER\OneDrive\Documents\myProject> git add home.html
PS C:\Users\USER\OneDrive\Documents\myProject> git commit -m "Index File"
[master 53a4fef] Index File
 1 file changed, 19 insertions(+)
 create mode 100644 home.html

PS C:\Users\USER\OneDrive\Documents\myProject> git push origin master
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 16 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 824 bytes | 824.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/DIVINEakisa/Bundle1--Exercises1.git
   7666d6e..53a4fef  master -> master
PS C:\Users\USER\OneDrive\Documents\myProject> git stash list
stash@{0}: On master: Add New File
PS C:\Users\USER\OneDrive\Documents\myProject> git stash pop "stash@{0}"
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

Dropped stash@{0} (7a5607f28d37ce1145bd39803c75fe2189e67eec)
PS C:\Users\USER\OneDrive\Documents\myProject> git reset --hard
HEAD is now at 53a4fef Index File
PS C:\Users\USER\OneDrive\Documents\myProject> git rm team.html

PS C:\Users\USER\OneDrive\Documents\myProject> git commit -m "Team File Removed"
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)

```

## Bundle 2

### Exercise 1

```bash
git branch
  dev
* main

C:\Users\USER\OneDrive\Documents\myProject>git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

C:\Users\USER\OneDrive\Documents\myProject>git branch
  dev
* ft/bundle-2
  main

C:\Users\USER\OneDrive\Documents\myProject>git add .

C:\Users\USER\OneDrive\Documents\myProject>git commit -m "New File"
[ft/bundle-2 57b1370] New File
 1 file changed, 11 insertions(+)
 create mode 100644 service.html

C:\Users\USER\OneDrive\Documents\myProject>git status
On branch ft/bundle-2
nothing to commit, working tree clean

C:\Users\USER\OneDrive\Documents\myProject>git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 450 bytes | 450.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/DIVINEakisa/Bundle1--Exercises1/pull/new/ft/bundle-2
remote:
To https://github.com/DIVINEakisa/Bundle1--Exercises1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
```

### Exercise 2

```bash

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git pull origin main
From https://github.com/DIVINEakisa/Bundle1--Exercises1
 * branch            main       -> FETCH_HEAD
Already up to date.

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git branch ft/service-redesign

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git checkout ft/service-redesign
M       service.html
Switched to branch 'ft/service-redesign'

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/service-redesign)
$ git add .

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/service-redesign)
$ git commit -m "New Changes On Service"
[ft/service-redesign 853676f] New Changes On Service
 2 files changed, 161 insertions(+), 4 deletions(-)
 create mode 100644 clear

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/service-redesign)
$ git push origin main
Everything up-to-date
USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/service-redesign|MERGING)
$ git fetch origin

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/service-redesign|MERGING)
$ git diff ft/service-redesign
diff --git a/service.html b/service.html
index 41d5096..ce91e3a 100644
--- a/service.html
+++ b/service.html
@@ -3,7 +3,10 @@
   <head>
     <meta charset="UTF-8" />
     <meta name="viewport" content="width=device-width, initial-scale=1.0" />
+<<<<<<< HEAD
     <!-- displays site properly based on user's device -->
+=======
+>>>>>>> c57f2b59b53fdd6933db6c100d6ffcc63b0118e4

     <link
       rel="icon"
@@ -22,8 +25,13 @@
       }
     </style>
   </head>
+<<<<<<< HEAD
   <body bg-hsl(248, 70%, 10%)>
     <!-- Form starts -->
+=======
+
+  <body bg-hsl(248, 70%, 10%)>
+>>>>>>> c57f2b59b53fdd6933db6c100d6ffcc63b0118e4
     <div class="head">
       <h1>Your Journey to Coding Conf 2025 Starts Here!</h1>

@@ -66,6 +74,7 @@
       /><br />
     </form>

+<<<<<<< HEAD
     <!-- Form ends -->

     <!-- Generated tickets starts -->
@@ -78,10 +87,18 @@

     <!-- Generated tickets ends -->

+=======
+    Congrats, Your ticket is ready. We've emailed your ticket to and will send
+    updates in the run up to the event. Coding Conf Jan 31, 2025 / Austin, TX
+>>>>>>> c57f2b59b53fdd6933db6c100d6ffcc63b0118e4
     <div class="attribution">
       Challenge by
       <a href=

C:\Users\USER\OneDrive\Documents\myProject>git pull origin main
From https://github.com/DIVINEakisa/Bundle1--Exercises1
 * branch            main       -> FETCH_HEAD
Already up to date.
C:\Users\USER\OneDrive\Documents\myProject>git merge main
Already up to date.

C:\Users\USER\OneDrive\Documents\myProject>git commit -m "merge main"
On branch ft/service-redesign
nothing to commit, working tree clean

C:\Users\USER\OneDrive\Documents\myProject>git push origin ft/service-redesign
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 16 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 1.90 KiB | 1.90 MiB/s, done.
Total 7 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
To https://github.com/DIVINEakisa/Bundle1--Exercises1.git
   c57f2b5..4c185de  ft/service-redesign -> ft/service-redesign
   PS C:\Users\USER\OneDrive\Documents\Gym-Git-Exercise-Solutions> git commit -m "Add Exercise 2 Bundle 2"
[main e514bcd] Add Exercise 2 Bundle 2
 1 file changed, 107 insertions(+)
PS C:\Users\USER\OneDrive\Documents\Gym-Git-Exercise-Solutions> git push origin main
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 16 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 1.64 KiB | 1.64 MiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/DIVINEakisa/Gym-Git-Exercise-Solutions.git
   8f5d1fa..e514bcd  main -> main
```

## Bundle 3

### Exercise 1

```bash

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents
$ cd myProject

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 5 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git pull origin
Updating 929f6b5..2d457d0
Fast-forward
 clear        | 82 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 service.html | 72 +++++++++++++++++++++++++++++++++++++++++++++++++---
 2 files changed, 150 insertions(+), 4 deletions(-)
 create mode 100644 clear

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/team-page)
$ git add .

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/team-page)
$ git commit -m "Create new file callde team.html"
[ft/team-page 71d54b4] Create new file callde team.html
 1 file changed, 537 insertions(+)
 create mode 100644 team.html

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 4.48 KiB | 4.48 MiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/DIVINEakisa/Bundle1--Exercises1/pull/new/ft/team-page
remote:
To https://github.com/DIVINEakisa/Bundle1--Exercises1.git
 * [new branch]      ft/team-page -> ft/team-page

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/team-page)
$ git log -1 --pretty=format:"%h"
71d54b4

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/contact-page)
$ git cherry-pick 71d54b4
[ft/contact-page a97781c] Create new file callde team.html
 Date: Thu Aug 21 12:07:52 2025 +0200
 1 file changed, 537 insertions(+)
 create mode 100644 team.html

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/contact-page)
$ git status
On branch ft/contact-page
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   team.html

no changes added to commit (use "git add" and/or "git commit -a")

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/contact-page)
$ git add .

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/contact-page)
$ git commit -m "Add Copy Right On The Footer"
[ft/contact-page f2c584e] Add Copy Right On The Footer
 1 file changed, 1 insertion(+), 3 deletions(-)

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 4.75 KiB | 4.75 MiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/DIVINEakisa/Bundle1--Exercises1/pull/new/ft/contact-page
remote:
To https://github.com/DIVINEakisa/Bundle1--Exercises1.git
 * [new branch]      ft/contact-page -> ft/contact-page

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git commit -a -m "Add Faq.html File"
On branch ft/faq-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        faq.html

nothing added to commit but untracked files present (use "git add" to track)

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git add .

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git status
On branch ft/faq-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   faq.html


USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git push origin ft/faq-page
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/DIVINEakisa/Bundle1--Exercises1/pull/new/ft/faq-page
remote:
To https://github.com/DIVINEakisa/Bundle1--Exercises1.git
 * [new branch]      ft/faq-page -> ft/faq-page

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git reverte 71d54b4
git: 'reverte' is not a git command. See 'git --help'.

The most similar command is
        revert

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git revert 71d54b4
error: your local changes would be overwritten by revert.
hint: commit your changes or stash them to proceed.
fatal: revert failed

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ ^C

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git status
On branch ft/faq-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   faq.html


USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git stash
Saved working directory and index state WIP on ft/faq-page: f2c584e Add Copy Right On The Footer

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git revert 71d54b4
CONFLICT (modify/delete): team.html deleted in parent of 71d54b4 (Create new file callde team.html) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert 71d54b4... Create new file callde team.html
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
hint: Disable this message with "git config set advice.mergeConflict false"

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page|REVERTING)
$ git diff
* Unmerged path team.html

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page|REVERTING)
$ git add .

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page|REVERTING)
$ git revert --continue
On branch ft/faq-page
You are currently reverting commit 71d54b4.
  (all conflicts fixed: run "git revert --continue")
  (use "git revert --skip" to skip this patch)
  (use "git revert --abort" to cancel the revert operation)

nothing to commit, working tree clean

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page|REVERTING)
$ git revert --abort

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git push origin ft/faq-page
Everything up-to-date

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git status
On branch ft/faq-page
nothing to commit, working tree clean


```

### Exercise2

```bash
USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git branch
  dev
  ft/bundle-2
  ft/contact-page
* ft/faq-page
  ft/service-redesign
  ft/team-page
  main

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git add .

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git commit -m "Add Paragraph in "
[main 67718a2] Add Paragraph in
 1 file changed, 1 insertion(+)

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 352 bytes | 352.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/DIVINEakisa/Bundle--Exercises.git
To https://github.com/DIVINEakisa/Bundle1--Exercises1.git
   2d457d0..67718a2  main -> main

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/home-page-redesign)
$ git status
On branch ft/home-page-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/home-page-redesign)
$ git add .

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/home-page-redesign)
$ git commit -m "Add Heading And Edit Title"
[ft/home-page-redesign 96fef4f] Add Heading And Edit Title
 1 file changed, 2 insertions(+), 1 deletion(-)


USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/home-page-redesign)
$ git push origin ft/home-page-redesign
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 16 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 5.08 KiB | 2.54 MiB/s, done.
Total 9 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/DIVINEakisa/Bundle--Exercises.git
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting
remote:      https://github.com/DIVINEakisa/Bundle--Exercises/pull/new/ft/home-page-redesign
remote:
To https://github.com/DIVINEakisa/Bundle1--Exercises1.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign

```

## Bundle 4

### Exercise 1

```bash

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git remote -v
origin  https://github.com/DIVINEakisa/Bundle1--Exercises1.git (fetch)
origin  https://github.com/DIVINEakisa/Bundle1--Exercises1.git (push)

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git remote add upstream https://github.com/DIVINEakisa/git-copy.git

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git remote -v
origin  https://github.com/DIVINEakisa/Bundle1--Exercises1.git (fetch)
origin  https://github.com/DIVINEakisa/Bundle1--Exercises1.git (push)
upstream        https://github.com/DIVINEakisa/git-copy.git (fetch)
upstream        https://github.com/DIVINEakisa/git-copy.git (push)


USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git add .

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git commit -m "New Changes On Home Page"
[main a963ed5] New Changes On Home Page
 1 file changed, 1 insertion(+)

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git push origin main
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 16 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (8/8), 1.46 KiB | 213.00 KiB/s, done.
Total 8 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/DIVINEakisa/Bundle--Exercises.git
To https://github.com/DIVINEakisa/Bundle1--Exercises1.git
   ad88569..a963ed5  main -> main

USER@LAPTOP-8BO5UTNO MINGW64 ~/OneDrive/Documents/myProject (main)
$ git push upstream main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 341 bytes | 341.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/DIVINEakisa/git-copy.git
   8b8d609..a963ed5  main -> main

```
