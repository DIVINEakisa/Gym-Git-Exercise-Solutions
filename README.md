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
